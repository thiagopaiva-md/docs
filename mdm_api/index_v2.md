# MDM API - v2

**OBS:** Para todas as chamadas, o código de retorno status será: 200 - Sucesso ou 500 - Erro.

## 1 - Árvore de análise

**Objetivo:** Trazer para o EAMon toda a informação da árvore de análise do Sistema MDM, incluindo a estrutura de equipamentos, subsistemas, componentes e pontos monitorados.

**Nome da operação:** core_getMonitoredPointsTree

**Parâmetros de entrada:** 

Nome                     |  Tipo
:-----------------------:|:---------------:
databaseAlias            | string
operation                | string

**Parâmetros de saída:**
Nome               |  Tipo
:-----------------:|:---------------:
status             | number
content            | object[]

## 2 - Executar análise personalizada

**Objetivo:** Executar, dentro da interface do EAMon, uma análise personalizada cadastrada no Sistema MDM.

Esta requisição será realizada em 2 etapas.

**Etapa 1:** Obter a lista de análises cadastradas no MDM.

**Nome da operação Etapa 1:** core_getCustomAnalysis

**Parâmetros de entrada:**
Nome       |  Tipo
:---------:|:---------------:
databaseAlias    | string
operation        | string

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

**Etapa 2:** Executar a análise solicitada.

**Nome da operação Etapa 2:** core_getCustomAnalysisData

**Parâmetros de entrada:**
Nome       |  Tipo
:---------:|:---------------:
databaseAlias    | string
operation        | string
analysisId       | string

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

## 3 - Turnos (visualizar)

**Objetivo:** Trazer para o EAMon os dados de turnos cadastrados.

**Nome da operação:** core_getShifts

**Parâmetros de entrada:** 

Nome                     |  Tipo
:-----------------------:|:---------------:
databaseAlias            | string
operation                | string

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

## 4 - Turnos (visualizar)

**Objetivo:** Trazer para o EAMon os dados de grupos de usuários cadastrados.

**Nome da operação:** core_getUserGroups

**Parâmetros de entrada:** 

Nome                     |  Tipo
:-----------------------:|:---------------:
databaseAlias            | string
operation                | string

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]
