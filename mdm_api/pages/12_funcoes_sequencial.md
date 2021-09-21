# 12 - Funções de análise sequencial

**Objetivo:** Executar as funções de análise sequencial do sistema MDM.

## Entrada

**Nome da operação:** core_getSequentialAnalysisFunction

**Atenção:** As funções aqui descritas aplicam-se apenas a pontos monitorados dinâmicos, ou seja, com número de amostras maior que 1. Pontos estáticos (número de amostras = 1) **não se aplicam**.

**Parâmetros de entrada:**

Nome                     |  Tipo           | Opcional     | Descrição
:-----------------------:|:---------------:|:------------:|:------------
databaseAlias            | string         | Não           | O alias da base de dados utilizada no momento da chamada.
operation                | string         | Não           | core_getSequentialAnalysisFunction
itemAnalysisType         | string         | Não           | Valores válidos:<br/> record / reference 
functionName             | string         | Não           | O nome da função a ser chamada.<br> Valores válidos descritos abaixo.
equipmentId              | string         | Não           | O id do equipamento do ponto monitorado que está chamando a função.
signalIds                | string[]       | Não           | Ids dos sinais que geraram a análise sequencial e deseja-se recalcular a função. 

**Funções aplicáveis no parâmetro "functionName":**

- picoapico
- maximo
- minimo
- media
- desvio
- rms
- freq0_40
- freq40_50
- freq50_100
- freq_1xRPM
- freq_2xRPM
- freq_50_1xRPM
- freq_25_1xRPM
- freq_mult_inf
- freq_mult_sup
- freq_impares
- freq_nat_estator
- freq_nat_rotor
- freq_rede
- freq_elet_mult_sup
- freq_rpmxsap_esc
- freq_muito_altas
- freq_pp
- 2xfreq_pp
- freq_pp_d
- freq_nat_pd
- freq_pp_cav
- 2xfreq_pp_cav
- bpfi
- bpfo
- bsf
- ftfi
- ftfo
- bpfienvelope
- bpfoenvelope
- bsfenvelope
- ftfienvelope
- ftfoenvelope
- soma_freqs
- fase_1xRPM
- rmsintegral

**JSON de exemplo - parâmetros de entrada**

```
{
  "databaseAlias": "ILS",
  "operation": "core_getSequentialAnalysisFunction",
  "itemAnalysisType": "record",
  "functionName": "rmsintegral",
  "equipmentId": "{B64F8035-C1B5-4B73-B491-6325E6080A8B}",
  "signalIds": ["{19E63622-A10B-534D-8BC9-892EBF515AA8}"],
}
```

**Exemplo no MDM:**\
[Seleção de função](img/12_Funcao_Sequencial.jpg)

## Saída

**Descrição dos parâmetros de saída em caso de sucesso, presentes no array de objetos "content":**

**Atenção:** A tabela abaixo descreve cada um dos objetos presentes no array.

Nome                     |  Tipo           | Opcional     | Descrição
:-----------------------:|:---------------:|:------------:|:------------
id                       | string         | Não           | Representa o id do sinal recalculado.<br/> (O mesmo em cada um dos parâmetros de entrada "signalIds").
value                    | float          | Não           | O valor final de cálculo da função solicitada para o sinal específico.

**JSON de exemplo - parâmetros de saída**
```
{
  "status":200,
  "content":
    [
      {
        "id": "{19E63622-A10B-534D-8BC9-892EBF515AA8}",
        "value": 8.6917
      }
    ]
}
```
