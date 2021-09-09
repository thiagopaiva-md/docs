# Relatório mensal - Setembro de 2021

## Continuação do desenvolvimento da disponibilização de dados do MDM dentro do portal EAMON

Durante o mês de setembro de 2021, o foco foi a continuação do desenvolvimento das funcionalidades do Sistema MDM que estarão disponíveis para consulta no portal EAMON.

Seguem as funcionalidades:

## 1 - Disponibilização de relatórios

### 1.1 - Relatório de grupos de pontos monitorados

O objetivo desta funcionalidade é disponibilizar no portal EAMon Lion o relatório de grupos de pontos monitorados disponível no Sistema MDM.

Entre os dados disponíveis, temos:

- Nome do grupo de pontos moniorados
- Nome dos pontos monitorados que compõem o grupo
- Testes do grupo de pontos
- NMA do grupo de pontos

### 1.2 - Relatório de falhas

O objetivo desta funcionalidade é disponibilizar no portal EAMon Lion o relatório de falhas disponível no Sistema MDM, listando todas as falhas cadastradas no sistema.

Entre os dados disponíveis, temos:

- Nome da falha
- Descrição
- Análise
- Recomendação
- Variáveis
- Termos

### 1.3 - Relatório de Funcionamento do Sistema

O objetivo desta funcionalidade é disponibilizar no portal EAMon Lion o relatório de funcionamento dos equipamentos, disponível no Sistema MDM.

Entre os dados disponíveis, temos para cada equipamento:

- **Sistema funcionando sem alarme**
  -  Análise normal sem alarme
  -  Máquina parada

- **Sistema funcionando com alarme**

- **Sistema funcionando com limitações**
  - Analise sem referência
  - Equipamento com Ponto de Operação Estabilizando

- **Sistema não funcionando**
  - Falha - SDSC
  - Falha - CRIO
  - Falha de comunicação
  - Desligado

Importante ressaltar que os dados do equipamento são representados por cada equipamento cadastrado no banco de Dados do Sistema MDM, onde cada tópico é representado por valores percentuais referente ao período do relatório gerado.

### 1.4 - Relatório de alarmados

O objetivo desta funcionalidade é disponibilizar no portal EAMon Lion o relatório de pontos monitorados alarmados com base em registros previamente selecionados.

Entre os dados disponíveis, temos:

- **Para testes de valores absolutos**
  - Datas dos registros que dispararam o alarme
  - Pontos de operação do equipamento, relativos aos registros
  - Valor do registro
  - Valor do alarme
  - Nome do alarme

- **Para testes de variações percentuais**\
Todos os dados presentes nos testes de valores absolutos, mais:
  - Valor da referência
  - Valor Alarmado
  - NMA
  - Data das referências utilizadas no testes
  - Pontos de operação do equipamento, relativos às referências

## 2 - Ferramenta de análise Comparativa

O objetivo desta funcionalidade é disponibilizar no portal EAMon Lion a ferramenta de análise comparativa do Sistema MDM.

A Ferramenta de Análise Comparativa permite ao usuário do Sistema MDM realizar comparações entre sinais do mesmo equipamento sob diferentes condições operativas, ou mesmo de diferentes equipamentos. Estes sinais podem ser armazenados como Referência, ou que foram armazenados devido à ocorrência de eventos de alarmes. Os sinais são apresentados no domínio do tempo (tempo versus amplitude) e sob a forma de espectros ou espectro cruzado (frequência versus amplitude). 

Esta funcionalidade consiste em duas etapas:

- Realizar a requisição para consultar as análises cadastradas e disponíveis para consulta;
- Com base nos dados retornados, selecionar a consulta desejada e aguardar a plotagem dos dados.

## 3 - Executar diagnóstico

O objetivo desta funcionalidade é disponibilizar no portal EAMon Lion a funcionalidade de execução de diagnóstico do Sistema MDM.

A execução de diagnóstico do MDM é baseado em lógica Fuzzy, uma técnica de lógica multivalorada, na qual os valores verdade das variáveis podem ser qualquer número real entre 0 (correspondente ao valor falso) e 1 (correspondente ao valor verdadeiro), diferentemente do que se verifica na chamada lógica *booleana*, onde os valores lógicos podem ser apenas 0 ou 1. Assim, podemos representar uma temperatura de 78°C como "0.9 elevada" e uma temperatura de 50°C como "Não elevada".

Esta funcionalidade consiste em duas etapas:

- Realizar a requisição para consultar os registros aplicáveis para o diagnóstico;
- Com base nos registros retornados, executar o diagnóstico.

## 4 - Publicações de atualizações da árvore de análise do Sistema MDM

O objetivo desta funcionalidade é disponibilizar, de forma automática, as atualizações que acontecem na árvore de análise do MDM, para que as alterações se reflitam na árvore do portal EAMon Lion. Para isso, foi criado um mecanismo de notificação dentro do Sistema MDM: Toda vez que uma alteração é realizada na árvore analítica, uma mensagem é entregue no barramento do RabbitMQ, permanecendo à espera de ser consumida pelo serviço do portal. Caso uma nova atualização seja publicado e já existam mensagens não consumidas na fila, as mensagens não consumidas são substituídas pela nova, assegurando que a atualização mais recente seja sempre a que estará disponível no barramento.
