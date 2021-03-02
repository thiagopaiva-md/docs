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

## 4 - Grupos de usuário (visualizar)

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

## 5 - Relatório de Rotas (Em branco)

**Objetivo:** Visualizar os relatório de rotas do Sistema MDM, sem dados preenchidos. Este relatório é útil para um cenário onde a rota precise ser impressa para ser executada manualmente.

Esta requisição é realizada em 2 etapas.

**Etapa 1:** Obter a lista de rotas cadastradas no MDM.

**Nome da operação Etapa 1:** core_getRoutes

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

**Etapa 2:** Obter os relatórios.

**Nome da operação Etapa 1:** core_getBlankRouteReport

**Parâmetros de entrada:**

Nome       |  Tipo
:---------:|:---------------:
databaseAlias    | string
operation        | string
routeId          | string

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

**Em caso de sucesso, o content será um object com os seguintes dados:**

**xml:** representa o arquivo xml com os dados de rotas. Deve ser salvo em disco para visualização com o nome de sua preferência, com **extensão .xml.**\
**xsl:** representa o arquivo xsl com os dados de estilização do relatório. Deve ser salvo em disco para visualização **com o nome styles.xsl**.

## 6 - Relatório de rotas (exibir dados coletados)

**Objetivo:** Visualizar os relatório de rotas do Sistema MDM, contendo os valores coletados pelos operadores.

Esta requisição é realizada em 3 etapas.

**Etapa 1:** Obter a lista de rotas cadastradas no MDM.

**Nome da operação Etapa 1:** core_getRoutes

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

**Etapa 2:** Obter os registros correspondentes da rota selecionada. Será necessário fornecer uma data de início e uma data fim para a busca de registros.

**Nome da operação Etapa 2:** core_getRouteRecords

**Parâmetros de entrada:**

Nome       |  Tipo
:---------:|:---------------:
databaseAlias    | string
operation        | string
routeId          | string
startDateTime    | Date
endDateTime      | Date


**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

**Etapa 3:** Obter o relatório.

**Nome da operação Etapa 3:** core_getRouteDataReport

**Parâmetros de entrada:**

Nome       |  Tipo
:---------:|:---------------:
databaseAlias    | string
operation        | string
recordId         | string
routeId          | string

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

**Em caso de sucesso, o content será um object com os seguintes dados:**

**xml:** representa o arquivo xml com os dados de rotas. Deve ser salvo em disco para visualização com o nome de sua preferência e **com extensão .xml.**\
**xsl:** representa o arquivo xsl com os dados de estilização do relatório. Deve ser salvo em disco para visualização **com o nome style.xsl.**\
**js:** representa o arquivo js que interpreta os anexos. Deve ser salvo em disco para visualização **com o nome relatorio-rotas.js.**\
**attachments:** representa um array JSON com os anexos codificados em base-64. Devem ser salvos em disco para visualização, **convertendo-se base64 para arquivo e com o nome baseado no parâmetro filename.**

## 7 - Relatório de rotas (exibir métricas de tempo de execução)

**Objetivo:** Visualizar os relatório de rotas do Sistema MDM, contendo os valores de tempo gasto pelos operadores.

Esta requisição é realizada em 3 etapas.

**Etapa 1:** Obter a lista de rotas cadastradas no MDM.

**Nome da operação Etapa 1:** core_getRoutes

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

**Etapa 2:** Obter os registros correspondentes da rota selecionada. Será necessário fornecer uma data de início e uma data fim para a busca de registros.

**Nome da operação Etapa 2:** core_getRouteRecords

**Parâmetros de entrada:**

Nome       |  Tipo
:---------:|:---------------:
databaseAlias    | string
operation        | string
routeId          | string
startDateTime    | Date
endDateTime      | Date


**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

**Etapa 3:** Obter o relatório.

**Nome da operação Etapa 3:** core_getRouteTimestampReport

**Parâmetros de entrada:**

Nome       |  Tipo
:---------:|:---------------:
databaseAlias    | string
operation        | string
recordId         | string
routeId          | string

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

**Em caso de sucesso, o content será um object com os seguintes dados:**

**xml:** representa o arquivo xml com os dados de rotas. Deve ser salvo em disco para visualização com o nome de sua preferência, **contendo a extensão .xml.**\
**xsl:** representa o arquivo xsl com os dados de estilização do relatório. Deve ser salvo em disco para visualização **com o nome style.xsl.**
