# Relatório mensal - Março de 2021

## Continuação do desenvolvimento da disponibilização de dados do MDM dentro do portal EAMON

Durante o mês de março de 2021, o foco foi a continuação do desenvolvimento das funcionalidades do Sistema MDM que estarão disponíveis para consulta no portal EAMON.

Seguem as funcionalidades:

### Relatórios

#### Relatório de rotas: rotas em branco

O objetivo desta atividade é disponibilizar os dados de uma rota não preenchida. Esta funcionalidade é útil em casos em que não será possível executar a rota eletronicamente, podendo então imprimir a rota em papel e executá-la manualmente.

Entre os dados disponíveis, temos:

- Nome da rota;
- Turno;
- Lista de sistemas a serem preenchidos;
- Lista de pontos monitorados a serem preenchidos, podendo ser:
  - Linhas em branco para preenchimento de valores numéricos, em caso de pontos monitorados instrumentados;
  - Opções de múltipla escolha para pontos monitorados sensitivos.

#### Relatório de rotas: rotas com dados coletados

O objetivo desta atividade é disponibilizar, em formato de relatório, os dados coletados durante uma rota.

Entre os dados disponíveis, temos:

- Nome da rota;
- Turno;
- Lista de sistemas percorridos;
- Lista de pontos monitorados e seus valores coletados, sendo:
  - Valor numérico em caso de pontos monitorados instrumentados;
  - Resposta da pergunta em múltipla escolha, em caso de pontos monitorados sensitivos;
- Desvios de fluxo da rota, caso existam;
- Interrupções da rota, caso existam;
- Métricas básicas de tempo de execução.

#### Relatório de rotas: Métricas de tempo de execução

O objetivo desta atividade é disponibilizar, em formato de relatório, os detalhes das métricas de tempo gastos na execução da rota.

Entre os dados disponíveis, temos:

- Nome da rota;
- Turno;
- Lista de sistemas percorridos;
- Lista detalhada de tempo total da execução da rota;
- Lista detalhada de tempo total de deslocamento entre os sistemas da rota;
- Lista detalhada de tempo de leitura dos pontos monitorados existentes na rota.

#### Relatório de Limites de alarmes

O objetivo desta atividade é disponibilizar, em formato de relatório, os limites de alarmes cadastrados para os grupos de pontos monitorados no Sistema MDM.

Dados disponíveis:

- Informações sobre pontos monitorados e testes
  - Nome do ponto monitorado;
  - Grupo de Pontos;
  - Unidade do tipo de sensor;
  - Nome do alarme configurado;
  - NMA do alarme configurado;
  - Teste a ser executado;
  - Valor de alarme;
