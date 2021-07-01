# MDM API - v4

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

## 5 - Relatórios

### 5.1 - Relatório de Rotas (Em branco)

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

### 5.2 - Relatório de rotas (exibir dados coletados)

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

### 5.3 - Relatório de rotas (exibir métricas de tempo de execução)

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

### 5.4 - Relatório de Limite de Alarmes

**Objetivo:** Visualizar os relatório de limites de alarmes do sistema MDM.

Esta requisição é realizada em 2 etapas.

**Etapa 1:** Obter a lista de equipamentos da árvore de análise.

**Nome da operação Etapa 1:** core_getEquipments

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

**Etapa 2:** Obter o relatório.

**Nome da operação Etapa 2:** core_getAlarmLimitsReport

**Parâmetros de entrada:**

Nome       |  Tipo
:---------:|:---------------:
databaseAlias    | string
operation        | string
equipmentId      | string
equipmentType    | number

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

### 5.5 - Relatório de Pontos Monitorados

**Objetivo:** Visualizar os relatório de Pontos monitorados do sistema MDM.

Esta requisição é realizada em 2 etapas.

**Etapa 1:** Obter a lista de equipamentos da árvore de análise.

**Nome da operação Etapa 1:** core_getEquipments

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

**Etapa 2:** Obter o relatório.

**Nome da operação Etapa 2:** core_getMonitoredPointsReport

**Parâmetros de entrada:**

Nome       |  Tipo
:---------:|:---------------:
databaseAlias    | string
operation        | string
equipmentId      | string

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

### 5.6 - Relatório de Grupos de Pontos Monitorados

**Objetivo:** Visualizar o relatório de grupos de pontos monitorados do sistema MDM.

Esta requisição é realizada em 2 etapas.

**Etapa 1:** Obter a lista de tipos de equipamentos.

**Nome da operação Etapa 1:** core_getEquipmentType

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

**Etapa 2:** Obter o relatório.

**Nome da operação Etapa 2:** core_getMonitoredPointsGroupsReport

**Parâmetros de entrada:**

Nome       |  Tipo
:---------:|:---------------:
databaseAlias    | string
operation        | string
equipmentType    | number

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

### 5.7 - Relatório de Falhas

**Objetivo:** Visualizar o relatório de falhas do sistema MDM.

**Nome da operação:** diag_getFailureReport

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

### 5.8 - Relatório de Funcionamento do Sistema

**Objetivo:** Visualizar o relatório de funcionamento do sistema MDM.

Esta requisição é realizada em 2 etapas.

**Etapa 1:** Obter a lista de tipos de plantas.

**Nome da operação Etapa 1:** core_getEquipments

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

**Etapa 2:** Obter o relatório.

**Nome da operação Etapa 2:** core_getSystemOperationReport

**Parâmetros de entrada:**

Nome       |  Tipo
:---------:|:---------------:
databaseAlias    | string
operation        | string
plantId          | string
startDateTime    | string
endDateTime      | string

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

## 6 - Importar dados

**Objetivo:** Importar dados de registros do Sistema MDM através da interface do EAMON.

**Nome da operação:** file_importRecordData

**Parâmetros de entrada:** 

Nome                     |  Tipo          | Descrição
:-----------------------:|:---------------:|:---------------:
databaseAlias            | string
operation                | string
content                  | string | Conteúdo do arquivo CSV de importação
equipmentId              | string | Id do equipamento a receber os dados de importação
dateFormat               | number | Valores<br/> 0: dd/mm/yyyy<br/>1: mm/dd/yyyy

**Parâmetros de saída:**
Nome               |  Tipo           | Descrição
:-----------------:|:---------------:|:---------------:
status             | number
content            | string ou string[] | Sucesso: string<br/>Erro validação de payload: string<br/>Erro na validação do arquivo: array de string, onde cada posição descreve erro em uma célula específica do arquivo.

## 7 - Buscar registros

**Objetivo:** Realizar a busca de registros armazenados no Sistema MDM.

**Nome da operação:** file_selectRecords

**Parâmetros de entrada:** 

Nome                     |  Tipo           | Opcional             | Descrição
:-----------------------:|:---------------:|:---------------:|:---------------:
databaseAlias            | string          | Não
operation                | string          | Não             | file_selectRecords
startDateTime            | Date/Time       | Não             | Intervalo Inicial da busca
endDateTime              | Date/Time       | Não             | Intervalo Final da busca
type                     | int             | Não             | 0: Busca por pontos monitorados<br/>1: Busca por equipamentos<br/>2: Busca registros de diagnóstico
monitoredPointIds        | string[]        | Sim             | Deve estar presente caso type = 0
equipmentId              | string          | Sim             | Deve estar presente caso type = 1 ou type = 2 

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

**Exemplo no MDM:**\
[Buscar registro por ponto monitorado](images/BuscarRegistrosPorPontos.jpg)\
[Buscar registro por equipamento ou diagnóstico](images/BuscarRegistrosPorEquipamento.jpg)

## 8 - Buscar referências

**Objetivo:** Realizar a busca de referências armazenados no Sistema MDM.

**Nome da operação:** file_selectReferences

**Parâmetros de entrada:** 

Nome                     |  Tipo           | Opcional             | Descrição
:-----------------------:|:---------------:|:---------------:|:---------------:
databaseAlias            | string          | Não
operation                | string          | Não             | file_selectRecords
startDateTime            | Date/Time       | Não             | Intervalo Inicial da busca
endDateTime              | Date/Time       | Não             | Intervalo Final da busca
type                     | int             | Não             | 0: Busca por pontos monitorados<br/>1: Busca por equipamentos
monitoredPointIds        | string[]        | Sim             | Deve estar presente caso type = 0
equipmentId              | string          | Sim             | Deve estar presente caso type = 1

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

**Exemplo no MDM:**\
[Buscar referências por ponto monitorado](images/BuscarReferenciasPorPontoMonitorado.jpg)\
[Buscar referências por equipamento](images/BuscarReferenciasPorEquipamento.jpg)


## 9 - Análise comparativa

**Objetivo:** Realizar análise de sinais dinâmicos do Sistema MDM.

Esta requisição é realizada em 2 etapas.

**Etapa 1:** Obter a lista de registros ou a lista de referências.

Para detalhes desta etapa, confira os itens 7 ou 8.

**ATENÇÃO: Para análise comparativa, deve-se utilizar a busca de registros ou referências baseada em pontos monitorados (type = 0). Não utilizar a busca por equipamentos.**

**Etapa 2:** Realizar a análise.

**Nome da operação Etapa 2:** core_getComparativeAnalysis

**Parâmetros de entrada:** 

Nome                     |  Tipo           | Opcional             | Descrição
:-----------------------:|:---------------:|:---------------:|:---------------:
databaseAlias            | string          | Não
operation                | string          | Não             | core_getComparativeAnalysis
type                     | string          | Não             | "record" - Análise utilizando registros<br/>"reference" - Análise utilizando referências
monitoredPointIds        | string[]        | Não             | Pontos Monitorados utilizados na busca de registros ou referências da etapa 1
recordOrReferenceIds     | string[]        | Não             | Ids dos registros ou referências obtidos na etapa 1

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

**Exemplo no MDM:**\
[Análise comparativa](images/AnaliseComparativa.jpg)

## 10 - Análise sequencial

**Objetivo:** Realizar análise de sinais estáticos no MDM.

Esta requisição é realizada em 2 etapas.

**Etapa 1:** Obter a lista de registros ou a lista de referências.

Para detalhes desta etapa, confira os itens 7 ou 8.

**ATENÇÃO: Para análise sequencial, deve-se utilizar a busca de registros ou referências baseada em pontos monitorados (type = 0). Não utilizar a busca por equipamentos.**

**Etapa 2:** Realizar a análise.

**Nome da operação Etapa 2:** core_getSequentialAnalysis

**Parâmetros de entrada:** 

Nome                     |  Tipo           | Opcional             | Descrição
:-----------------------:|:---------------:|:---------------:|:---------------:
databaseAlias            | string          | Não
operation                | string          | Não             | core_getSequentialAnalysis
type                     | string          | Não             | "record" - Análise utilizando registros<br/>"reference" - Análise utilizando referências
monitoredPointIds        | string[]        | Não             | Pontos Monitorados utilizados na busca de registros ou referências da etapa 1
recordOrReferenceIds     | string[]        | Não             | Ids dos registros ou referências obtidos na etapa 1

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

**Exemplo no MDM:**\
[Análise sequencial](images/AnaliseSequencial.jpg)
