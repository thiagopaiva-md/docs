# 12 - Funções de análise sequencial

**Objetivo:** Executar as funções de análise sequencial do sistema MDM.

**Nome da operação:** core_getSequentialAnalysisFunction

**Atenção:** As funções aqui descritas aplicam-se apenas a pontos monitorados dinâmicos, ou seja, com número de amostras maior que 1. Pontos estáticos (número de amostras = 1) **não se aplicam**.

**Parâmetros de entrada:**

Nome                     |  Tipo           | Opcional     | Descrição
:-----------------------:|:---------------:|:------------:|:------------
databaseAlias            | string         | Não
operation                | string         | Não           | core_getSequentialAnalysisFunction
itemAnalysisType         | string         | Não           | Valores válidos:<br/> record / reference 
functionName             | string         | Não           | O nome da função a ser chamada.<br> Valores válidos descritos abaixo.
equipmentId              | string         | Não           | O id do equipamento do ponto monitorado que está chamando a função.
signalIds                | string[]       | Não           | Ids dos sinais que geraram a análise sequencial e deseja-se recalcular a função. 
