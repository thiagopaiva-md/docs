# Relatório mensal - Setembro de 2021

## Continuação do desenvolvimento da disponibilização de dados do MDM dentro do portal EAMON

Durante o mês de setembro de 2021, o foco foi a continuação do desenvolvimento das funcionalidades do Sistema MDM que estarão disponíveis para consulta no portal EAMON.

Seguem as funcionalidades:

## Publicações de atualizações da árvore de análise do Sistema MDM

O objetivo desta funcionalidade é disponibilizar, de forma automática, as atualizações que acontecem na árvore de análise do MDM, para que as alterações se reflitam na árvore do portal EAMon Lion. Para isso, foi criado um mecanismo de notificação dentro do Sistema MDM: Toda vez que uma alteração é realizada na árvore analítica, uma mensagem é entregue no barramento do RabbitMQ, permanecendo à espera de ser consumida pelo serviço do portal. Caso uma nova atualização seja publicado e já existam mensagens não consumidas na fila, as mensagens não consumidas são substituídas pela nova, assegurando que a atualização mais recente seja sempre a que estará disponível no barramento.
