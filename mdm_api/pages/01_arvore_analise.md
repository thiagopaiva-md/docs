## 1 - Árvore de análise

**Objetivo:** Trazer para o EAMon toda a informação da árvore de análise do Sistema MDM, incluindo a estrutura de equipamentos, subsistemas, componentes e pontos monitorados.

**Nome da operação:** core_getMonitoredPointsTree

**Parâmetros de entrada:** 

Nome                     |  Tipo           | Opcional     | Descrição
:-----------------------:|:---------------:|:------------:|:------------
databaseAlias            | string         | Não
operation                | string         | Não           | core_getMonitoredPointsTree  

**Parâmetros de saída:**

Nome               |  Tipo           | Descrição
:-----------------:|:---------------:|:-------------
status             | number          | 
content            | object[]        | 

**Exemplo no MDM:**\
[Árvore de análise](images/ArvoreAnalise.jpg)
