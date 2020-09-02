# Relatório mensal - agosto de 2020

# Comunicação entre Sistema MDM x Portal EAMon

## 1 - Protocolo

A comunicação entre o Sistema MDM e o portal EAMon será estabelecida através do protocolo AMQP (Advanced Message Queuing Protocol). O AMQP é uma especificação para troca de mensagens assíncronas que tem como principal característica o fato de favorecer a interoperabilidade entre diferentes plataformas, assim como demanda este projeto.

### 1.1 - Sobre a comunicação

O protocolo AMQP estabelece a comunicação entre os *publishers* (aplicações que são responsáveis por produzir e publicar as mensagens) e os *consumers* (que são aplicações que recebem e processam as mensagens). Em nosso modelo de comunicação, o *consumer* também será capaz de responder ao *publisher*, fornecendo uma resposta quanto ao resultado do processamento. Este padrão de comunicação entre sistemas é denominado *RPC* (Remote Procedure Call, ou Chamada de Procedimento Remoto).

Realizando um estudo de caso em nossa aplicação, o Portal EAMon atua como *publisher* (aquele que realiza a requisição) e o serviço do Sistema MDM atua como *consumer* (serviço responsável por receber e processar a requisição e, em nosso caso, também informar o resultado do processamento).

A arquitetura da comunicação RPC é ilustrada conforme a figura a seguir:

<p align="center">
  <img src="images/RPC.jpg" />
</p>

### 1.2 - Comunicação entre os sistemas

A disponibilização de informações será realizada do lado do sistema MDM a partir de um novo módulo, denominado "Gerente EAMon". O portal deverá realizar as requisições para este componente. A seguir, serão listadas as informações disponibilizadas do Sistema MDM para consulta no portal EAMon.

A arquitetura da comunicação entre EAMon e o gerente é ilustrada a seguir:

<p align="center">
  <img src="images/Arq_Gerente.jpg" />
</p>

## 2 - Detalhes das funcionalidades

### 2.1 - Importar dados

**Objetivo:** Relizar a importação de uma planilha excel com dados de registro, em formato csv pré-definido, para o banco de dados do Sistema MDM.

**Parâmetros de entrada:**

Nome       |  Tipo
:---------:|:---------------:
plantId    | string
operation  | number
inputData  | string

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string

### 2.2 - Executar análise personalizada

**Objetivo:** Executar, dentro da interface do EAMon, uma análise personalizada cadastrada no Sistema MDM.

Esta requisição será realizada em 2 etapas.

**Etapa 1:** Obter a lista de análises cadastradas no MDM.

**Parâmetros de entrada:**
Nome       |  Tipo
:---------:|:---------------:
plantId    | string
operation  | number

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

**Etapa 2:** Consultar os sinais

**Parâmetros de entrada:**
Nome       |  Tipo
:---------:|:---------------:
plantId    | string
operation  | number
analysisId | string
poId?      | string

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

**Atenção:** A primeira resposta (padrão) para a plotagem será com os dados de data e hora. Caso o desejo seja plotagem por pontos de operação, a requisição da etapa 2 deverá ser repetida, desta vez fornecendo o parâmetro "poId", que se refere ao ID do ponto de operação.

### 2.3 - Atributos

**Objetivo:** Visualizar os atributos cadastrados no Sistema MDM.

**Parâmetros de entrada:**
Nome       |  Tipo
:---------:|:---------------:
plantId    | string
operation  | number

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

### 2.4 - Ferramentas de análise

#### 2.4.1 - Análise comparativa
