# Relatório mensal - agosto de 2020

# Comunicação entre Sistema MDM x Portal EAMon

## 1 - Protocolo

A comunicação entre o Sistema MDM e o portal EAMon será estabelecida através do protocolo AMQP (Advanced Message Queuing Protocol). O AMQP é uma especificação para troca de mensagens assíncronas que tem como principal característica o fato de favorecer a interoperabilidade entre diferentes plataformas, assim como demanda este projeto.

### 1.1 - Sobre a comunicação

O protocolo AMQP estabelece a comunicação entre os *publishers* (aplicações que são responsáveis por produzir e publicar as mensagens) e os *consumers* (que são aplicações que recebem e processam as mensagens). Em nosso modelo de comunicação, o *consumer* também será capaz de responder ao *publisher*, fornecendo uma resposta quanto ao resultado do processamento. Este padrão de comunicação entre sistemas é denominado *RPC* (Remote Procedure Call, ou Chamada de Procedimento Remoto).