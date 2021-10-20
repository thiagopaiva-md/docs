# 13 - Níveis dos tanques de óleo

**Objetivo:** Calcular os níveis atuais dos reservatórios dos tanques de óleo.

## Entrada

**Nome da operação:** core_getOilTankLevels

**Parâmetros de entrada:**

Nome                     |  Tipo           | Opcional     | Descrição
:-----------------------:|:---------------:|:------------:|:------------
databaseAlias            | string         | Não           | O alias da base de dados utilizada no momento da chamada.
operation                | string         | Não           | core_getOilTankLevels

**JSON de exemplo - parâmetros de entrada**

```
{
  "databaseAlias": "ILS",
  "operation": "core_getOilTankLevels",
}
```

## Saída

**Descrição dos parâmetros de saída em caso de sucesso, presentes no array de objetos "content":**

**Atenção:** A tabela abaixo descreve cada um dos objetos presentes no array.

Nome                     |  Tipo           | Opcional     | Descrição
:-----------------------:|:---------------:|:------------:|:------------
id                       | string         | Não           | Representa o id do ponto monitorado.
name                     | string         | Não           | Representa o nome do ponto monitorado.
value                    | float          | Não           | O valor do cálculo dos níveis de óleo.

**JSON de exemplo - parâmetros de saída**

```
{
	"status": 200,
	"content": [
		{
			"id": "{12CF4795-C278-4917-ADCB-67765C48BCDA}",
			"name": "TN-NO-REPO_XP32",
			"value": 202
		},
		{
			"id": "{B59B8658-C2F4-45D5-B44F-6370884ED21D}",
			"name": "TN-NO-REPO_S4-R46",
			"value": 206
		},
		{
			"id": "{463C7C53-A897-446C-96B5-6A3012337258}",
			"name": "TN-NO-REPO_R829",
			"value": 204
		},
		{
			"id": "{CD1238AB-E9A2-4ACD-B6C4-2820AF3EEE57}",
			"name": "TN-NO-REPO_VG32",
			"value": 208
		},
		{
			"id": "{9E074212-1529-4FD7-AA3C-918D721E1A51}",
			"name": "TN-NO-REPO_TT68",
			"value": 209
		},
		{
			"id": "{CB4A8665-4311-45D9-993A-ED8E2D0E8941}",
			"name": "TN-NO-REPO_AV",
			"value": 201
		},
		{
			"id": "{7CF96760-BD5E-4794-8572-79758ADBE8CA}",
			"name": "TN-NO-REPO_OD",
			"value": 205
		},
		{
			"id": "{9102B094-6E93-495C-8416-8468208C5325}",
			"name": "TN-NO-REPO_G634",
			"value": 203
		},
		{
			"id": "{0B74EDB1-3B9D-4D45-8151-206ECAD17204}",
			"name": "TN-NO-REPO_RR2",
			"value": 207
		},
		{
			"id": "{843DF944-B841-4A39-B3F6-CDE1D34977F3}",
			"name": "TN-NO-ATUAL_R829",
			"value": 48
		},
		{
			"id": "{07759414-7F9B-4D3F-8225-5106A9A40BC6}",
			"name": "TN-NO-ATUAL_S4-R46",
			"value": 50
		},
		{
			"id": "{C225AEE4-0ABB-475F-A1C4-8BF5988D7DB2}",
			"name": "TN-NO-ATUAL_G634",
			"value": 47
		},
		{
			"id": "{582CD183-4ACB-4053-B218-CF84ADD42642}",
			"name": "TN-NO-ATUAL_OD",
			"value": 49
		},
		{
			"id": "{0114DBA7-6F18-4039-9DFF-08B323F60C4E}",
			"name": "TN-NO-ATUAL_VG32",
			"value": 52
		},
		{
			"id": "{8D5BBF67-2756-4763-A582-A9885B15B5B7}",
			"name": "TN-NO-ATUAL_XP32",
			"value": 46
		},
		{
			"id": "{0E240042-9613-4131-98C4-F499CFCEF602}",
			"name": "TN-NO-ATUAL_RR2",
			"value": 51
		},
		{
			"id": "{64929249-412B-420A-9B85-A036085ED5DD}",
			"name": "TN-NO-ATUAL_AV",
			"value": 45
		},
		{
			"id": "{5CDC9500-B460-434F-B3A2-7666DC3CC7CA}",
			"name": "TN-NO-ATUAL_TT68",
			"value": 53
		},
		{
			"id": "{0D6442CA-1E1F-496E-9FBA-CAB77ECCE199}",
			"name": "TN-NO-CONS_XP32",
			"value": 122
		},
		{
			"id": "{41C18265-8D4C-4605-B5DC-14FBD25EB6F5}",
			"name": "TN-NO-CONS_TT68",
			"value": 129
		},
		{
			"id": "{5A241482-1063-4E24-87AC-AE8CFBD1B878}",
			"name": "TN-NO-CONS_RR2",
			"value": 127
		},
		{
			"id": "{92CF0C05-D9C1-49D5-B2A1-F243ABE64CBB}",
			"name": "TN-NO-CONS_G634",
			"value": 123
		},
		{
			"id": "{FB420399-6CAF-47D4-819D-80A5F3486D4B}",
			"name": "TN-NO-CONS_AV",
			"value": 121
		},
		{
			"id": "{86423904-3E57-4191-9CB3-D929B5E7A468}",
			"name": "TN-NO-CONS_R829",
			"value": 124
		},
		{
			"id": "{74217620-758A-4533-A623-BF517F9DD3AD}",
			"name": "TN-NO-CONS_VG32",
			"value": 128
		},
		{
			"id": "{D5A946DE-5180-4CDA-89CD-1B3003A74A45}",
			"name": "TN-NO-CONS_S4-R46",
			"value": 126
		},
		{
			"id": "{15328CF8-E64A-41B5-A513-B78979DBAF98}",
			"name": "TN-NO-CONS_OD",
			"value": 125
		},
		{
			"id": "{900308EE-3199-46E0-97FC-8AE6FFF2402C}",
			"name": "VT-NO-TX_XP32",
			"value": 0.025416666666666668
		},
		{
			"id": "{09B1CDD1-3208-4D14-A23E-1C08C6C8C638}",
			"name": "VT-NO-TX_TT68",
			"value": 0.0028666666666666668
		},
		{
			"id": "{E0AE23E7-5239-4FAD-AE1D-4EF1277E83E8}",
			"name": "VT-NO-TX_RR2",
			"value": 4.535714285714286
		},
		{
			"id": "{EF9824A2-056B-4CBA-8118-F48874B58EBD}",
			"name": "VT-NO-TX_G634",
			"value": 0.0615
		},
		{
			"id": "{5950EABB-C944-4DD2-8EDD-22D478BC9350}",
			"name": "VT-NO-TX_AV",
			"value": 0.001960149036125061
		},
		{
			"id": "{7CB749B5-ADDA-4887-8FC3-71DC5AA16FE5}",
			"name": "VT-NO-TX_R829",
			"value": 31
		},
		{
			"id": "{DAE69A11-1341-448F-BAAD-0E03274B93F5}",
			"name": "VT-NO-TX_VG32",
			"value": 0.02666666666666667
		},
		{
			"id": "{D42444A6-AE4C-4B82-BA82-2B0D2444EF99}",
			"name": "VT-NO-TX_S4-R46",
			"value": 4.5
		},
		{
			"id": "{2986F24A-1FF5-40F9-82B9-B697D94B1D59}",
			"name": "VT-NO-TX_OD",
			"value": 0.0625
		},
		{
			"id": "{041CD839-9A2A-9A4A-8B77-113CB0C284A6}",
			"name": "VT-NO-ETQE_S4-R46",
			"value": 206
		},
		{
			"id": "{8834EE1B-D692-D642-B4A8-0289BA81A2F5}",
			"name": "VT-NO-ETQE_RR2",
			"value": 207
		},
		{
			"id": "{5B3CAB38-D34B-7E43-AB43-DC6CDBDCEA39}",
			"name": "VT-NO-ETQE_VG32",
			"value": 208
		},
		{
			"id": "{9EBD943E-95B2-6B4E-9796-EBB626FD3D67}",
			"name": "VT-NO-ETQE_AV",
			"value": 201
		},
		{
			"id": "{A17A8034-5EF1-4C44-B93E-4DFDC3359B25}",
			"name": "VT-NO-ETQE_R829",
			"value": 204
		},
		{
			"id": "{EBF0A210-2DE9-824C-AB9D-B6C79E0833FF}",
			"name": "VT-NO-ETQE_G634",
			"value": 203
		},
		{
			"id": "{89758B0F-3319-D041-B837-B2584CD93C7A}",
			"name": "VT-NO-ETQE_XP32",
			"value": 202
		},
		{
			"id": "{B648210E-2791-4240-BE26-9BDD4B931652}",
			"name": "VT-NO-ETQE_TT68",
			"value": 209
		},
		{
			"id": "{BA1EB384-DFD5-7E46-B5B6-BD30BA41F616}",
			"name": "VT-NO-ETQE_OD",
			"value": 205
		}
	]
}
```
