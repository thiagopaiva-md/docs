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

## 2 - Publicações de atualizações da árvore de análise do Sistema MDM

O objetivo desta funcionalidade é disponibilizar, de forma automática, as atualizações que acontecem na árvore de análise do MDM, para que as alterações se reflitam na árvore do portal EAMon Lion. Para isso, foi criado um mecanismo de notificação dentro do Sistema MDM: Toda vez que uma alteração é realizada na árvore analítica, uma mensagem é entregue no barramento do RabbitMQ, permanecendo à espera de ser consumida pelo serviço do portal. Caso uma nova atualização seja publicado e já existam mensagens não consumidas na fila, as mensagens não consumidas são substituídas pela nova, assegurando que a atualização mais recente seja sempre a que estará disponível no barramento.

## 
