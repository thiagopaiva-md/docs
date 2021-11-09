# Relatório mensal - Novembro de 2021

## Continuação do desenvolvimento da disponibilização de dados do MDM dentro do portal EAMON

Durante o mês de novembro de 2021, o foco foi a continuação do desenvolvimento das funcionalidades do Sistema MDM que estarão disponíveis para consulta no portal EAMON.

Seguem as funcionalidades:

## 1 - Níveis dos tanques de óleo

O objetivo desta funcionalidade é disponibilizar no portal EAMon Lion os níveis dos tanques de reservatórios de  óleo.

São utilizados 3 tipos de pontos monitorados para cálculos desses níveis, que serão apresentados a seguir.

### 1.1 - Pontos monitorados offline

Estes pontos monitorados representam os valores que são cadastrados no editor de formulário e lidos no módulo formulário web do sistema MDM.

### 1.2 - Pontos monitorados virtuais

Estes pontos monitorados representam uma operação matemática com base em um ou mais pontos monitorados offline, e o resultado desta operação representa a taxa de consumo de óleo.

### 1.3 - Pontos monitorados virtualizados

Estes pontos monitorados representam operações matemáticas mais complexas, onde os cálculos são efetuados no ANAQ. O resultado dessas operações representa o valor do estoque de óleo.

## 2 - Funções da análise sequencial

O objetivo desta funcionalidade é disponibilizar no portal EAMon Lion as diversas funções presentes na ferramenta de análise sequencial e que são aplicáveis em sinais dinâmicos.

Funções aplicáveis:

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
