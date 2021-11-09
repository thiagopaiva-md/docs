## Saída - Etapa 2 (Análise sequencial)

**Descrição dos parâmetros de saída em caso de sucesso, presentes no array de objetos "content":**

**Atenção:** A tabela abaixo descreve cada um dos objetos presentes no array.

Nome                           |  Tipo           | Descrição
:-----------------------------:|:---------------:|:-------------
groupedSignals                 | object[]        | Sinais da análise agrupados por pontos monitorados
operationPoints                | object[]        | Os pontos de operação do equipamento

Descrição do Array "grupedSignals", objeto "monitoredPoint":

Nome                     |  Tipo           | Descrição
:-----------------------:|:---------------:|:-------------
id                       | string          | Id do Ponto Monitorado
name                     | string          | Nome do Ponto Monitorado
type                     | integer         | Representa sinal estático (0) ou dinâmico (1)

Descrição do array "grupedSignals", array "signals":

Nome                     |  Tipo           | Descrição
:-----------------------:|:---------------:|:-------------
id                       | string          | Id do sinal gravado
dateTime                 | dateTime        | Data/Hora do sinal gravado
value                    | float[]         | Array de uma posição que representa o valor do sinal gravado
operationPoints          | object[]        | Os pontos de operação do registro ou referência

Descrição do array "operationPoints":

Nome                     |  Tipo           | Descrição
:-----------------------:|:---------------:|:-------------
id                       | string          | Id do ponto de operação, deve ser correlacionado com os pontos de operação<br/> do array groupedSignals.signals.operationPoints
idMonitoredPoint         | string          | Id do ponto monitorado do ponto de operação
name                     | name            | Nome do ponto monitorado do ponto de operação

```
{
	"status": 200,
	"content": {
		"groupedSignals": [
			{
				"monitoredPoint": {
					"id": "{51D241E1-65C0-40A5-9EEE-64E726F4489D}",
					"name": "TT-MGS-PATIM_OFFLINE/Segmentos/Mancal Guia Superior/UG02",
					"type": 0
				},
				"signals": [
					{
						"id": "{017A9E94-B6CA-BF45-8898-E89F5967292C}",
						"dateTime": "2020-12-17T20:49:27.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{04CB3C18-CDF0-4E49-AF55-E9501EE342E9}",
						"dateTime": "2020-10-28T19:44:25.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							33
						]
					},
					{
						"id": "{0978429D-FC5E-DB4E-96E6-CEF1B74C828A}",
						"dateTime": "2020-12-18T18:14:56.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{14AB63D0-7A33-E24B-B324-4B5302810F6E}",
						"dateTime": "2020-10-14T01:40:37.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							4
						]
					},
					{
						"id": "{1695641A-3110-6547-AEA8-404A1ECE68BC}",
						"dateTime": "2020-10-28T19:44:25.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							33
						]
					},
					{
						"id": "{2C90A9B9-EDCE-5342-BEA2-B2EFA9A0B3A5}",
						"dateTime": "2020-10-14T21:06:10.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							24
						]
					},
					{
						"id": "{360E353C-A3BD-254B-ABA7-F704BBEFD20F}",
						"dateTime": "2020-11-24T18:50:34.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							23
						]
					},
					{
						"id": "{42107467-0828-704F-8C0E-99F1A36B78C2}",
						"dateTime": "2020-10-22T22:12:37.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{42350B58-98FF-9B45-B56A-93D63E3EAFCB}",
						"dateTime": "2020-10-14T21:06:10.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							24
						]
					},
					{
						"id": "{48300850-3D06-C849-86DD-DA78650FFFF5}",
						"dateTime": "2020-10-28T12:47:57.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							2
						]
					},
					{
						"id": "{487A5519-2028-6342-8591-C425A00BAF5A}",
						"dateTime": "2020-12-17T20:24:16.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							13
						]
					},
					{
						"id": "{493D6B24-50C7-E644-A026-E0EED223751C}",
						"dateTime": "2020-10-22T22:12:37.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{4A57085C-E88F-4F46-8A38-10AE0B6EB73E}",
						"dateTime": "2020-10-14T21:06:10.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							24
						]
					},
					{
						"id": "{4B777E46-FD57-FA46-9CE0-75BE90B59952}",
						"dateTime": "2020-10-15T23:23:15.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							1
						]
					},
					{
						"id": "{54DAA955-3FF3-1A4E-B0DB-9D971C14CFB9}",
						"dateTime": "2020-10-22T13:52:47.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{5FCE9A4F-5440-C94B-94C7-38964FD5BD99}",
						"dateTime": "2020-10-14T21:06:10.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							24
						]
					},
					{
						"id": "{6B336467-9873-CC46-BE8E-33AEA558D428}",
						"dateTime": "2020-10-22T13:52:47.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{6D9C6716-42C2-144C-9D4E-003C93954F40}",
						"dateTime": "2020-10-17T18:30:21.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							1
						]
					},
					{
						"id": "{6DDA6F8B-9AD4-E44B-85FD-225AF1F5CF4B}",
						"dateTime": "2020-10-28T12:47:57.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							2
						]
					},
					{
						"id": "{6F49E779-4DEE-0942-BD1D-506065438BBF}",
						"dateTime": "2020-10-14T21:06:10.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							24
						]
					},
					{
						"id": "{78D8AF2C-93D2-0948-BD70-FDFE841A1ABD}",
						"dateTime": "2020-10-31T12:47:44.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							5
						]
					},
					{
						"id": "{82708297-AAAD-D440-A246-27CD1E970D00}",
						"dateTime": "2020-10-17T15:05:53.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							30
						]
					},
					{
						"id": "{868713FA-27DF-6746-B398-2DCE809444C7}",
						"dateTime": "2020-10-28T00:55:27.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							35
						]
					},
					{
						"id": "{8FDB66FC-B328-1D4D-B435-5A6BC41E978F}",
						"dateTime": "2020-10-22T22:12:37.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{91EF8C40-519A-9249-89F2-ECF6F97F316D}",
						"dateTime": "2020-10-15T23:44:27.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							10
						]
					},
					{
						"id": "{9230D88F-395F-E143-80F2-721AC0FC784E}",
						"dateTime": "2020-10-22T13:52:47.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{9AB28604-2A71-E04B-88D9-F1ECEB69B8B4}",
						"dateTime": "2020-10-28T12:47:57.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							2
						]
					},
					{
						"id": "{9F5A362E-8D88-424A-AE88-8CCEAB30D30B}",
						"dateTime": "2020-10-14T21:06:10.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							24
						]
					},
					{
						"id": "{A1441E4F-D5B8-EE4C-9E31-0000FA574C38}",
						"dateTime": "2020-10-14T21:06:10.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							24
						]
					},
					{
						"id": "{A7B01EC0-D923-594F-8B25-007F1E210575}",
						"dateTime": "2020-10-22T13:52:47.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{ACAF1178-CA1B-C245-AD56-F77DB234F19F}",
						"dateTime": "2020-10-28T12:47:57.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							2
						]
					},
					{
						"id": "{AD7E6BA4-D35E-BE45-B6FD-22FBB5DB5C0D}",
						"dateTime": "2020-10-22T13:52:47.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{B0C962FC-CD60-514B-8893-808C91853214}",
						"dateTime": "2020-12-17T22:40:00.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{B114A413-3AC4-BD49-AC89-8A724CEBD420}",
						"dateTime": "2020-10-14T21:06:10.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							24
						]
					},
					{
						"id": "{B195906F-B9EF-D64A-8929-6E18417FF652}",
						"dateTime": "2020-10-28T12:47:57.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							2
						]
					},
					{
						"id": "{B6548CDD-9004-6E49-B6C1-0213B481B0E6}",
						"dateTime": "2020-10-28T17:01:11.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{B8FF23C0-4102-344E-AA6D-311A98E12691}",
						"dateTime": "2020-11-06T15:52:17.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{B9C82555-D054-3040-8EDB-1FB109421049}",
						"dateTime": "2020-10-15T23:44:27.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							10
						]
					},
					{
						"id": "{BD3FFA68-2E0F-4149-89B7-9916A6A623B7}",
						"dateTime": "2020-10-16T18:58:46.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							24
						]
					},
					{
						"id": "{C5A813C6-1E77-4D44-B97A-6799845955BE}",
						"dateTime": "2020-10-28T12:47:57.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							2
						]
					},
					{
						"id": "{C72B388F-7937-3442-B465-D9C36B802494}",
						"dateTime": "2020-10-14T21:06:10.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							24
						]
					},
					{
						"id": "{DC53566D-858A-E14C-8942-0B1887BFF80A}",
						"dateTime": "2020-10-15T20:07:48.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							59
						]
					},
					{
						"id": "{DEC46A10-FEA9-8B4D-9E42-F47F60838EAB}",
						"dateTime": "2020-10-22T13:52:47.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{E0AB16C5-B843-254D-BDD9-2105868B5706}",
						"dateTime": "2020-10-28T12:47:57.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							2
						]
					},
					{
						"id": "{E325C03D-025F-DC49-B2D5-C0E40830A55E}",
						"dateTime": "2020-10-28T12:47:57.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							2
						]
					},
					{
						"id": "{E75820CE-FBF2-E242-9A77-5BB860BBBC70}",
						"dateTime": "2020-10-22T13:52:47.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{E79D4AF0-8CE8-354C-8891-336E1D441017}",
						"dateTime": "2020-10-14T17:46:23.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							2
						]
					},
					{
						"id": "{E8053C84-4F85-6A45-AB38-52CE71AF4ABC}",
						"dateTime": "2020-10-28T17:01:11.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{F25D2165-27C3-0344-B606-95B609CD2E40}",
						"dateTime": "2020-10-14T21:06:10.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							24
						]
					},
					{
						"id": "{F836DA0E-344B-5B44-993C-A4D54BEEEB32}",
						"dateTime": "2020-10-15T23:44:27.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							10
						]
					},
					{
						"id": "{FA1EAB72-E573-9C45-B663-B6B6555301B6}",
						"dateTime": "2020-11-06T16:50:53.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							27
						]
					},
					{
						"id": "{FCE241A9-2CAB-A34C-A72A-D2DD50AB49D2}",
						"dateTime": "2020-10-22T22:12:37.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{FD848133-1949-1940-9B96-A034D3EE5696}",
						"dateTime": "2020-10-16T13:22:03.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							27
						]
					},
					{
						"id": "{000503C8-F78F-FF47-8A49-8DFD4B412EED}",
						"dateTime": "2019-10-20T22:38:03.000Z",
						"operationPoints": [],
						"value": [
							51.9000015258789
						]
					},
					{
						"id": "{01CE7DAA-C4E0-A247-80BD-85125C92ABD4}",
						"dateTime": "2019-11-28T00:59:41.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{01E69EDD-A281-5A43-B14E-615C4A331299}",
						"dateTime": "2019-10-27T14:45:02.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{044162A4-0C59-4B46-9DA6-56B205F0CC22}",
						"dateTime": "2019-10-29T18:36:42.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{044A5EED-FC72-C649-86EB-FC1515B8DE27}",
						"dateTime": "2019-10-21T18:43:55.000Z",
						"operationPoints": [],
						"value": [
							51.9000015258789
						]
					},
					{
						"id": "{04DA153F-830F-EC47-B4B2-EFA8F60448EE}",
						"dateTime": "2019-11-23T21:43:56.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{05A22E78-537C-AD4C-916A-4BF1B0920865}",
						"dateTime": "2019-11-17T21:21:44.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{061ADA85-9F9F-C446-BA63-05F0C1F70FC9}",
						"dateTime": "2019-10-29T10:22:17.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{082D1CE4-BC24-0346-9CF0-31DFC154E188}",
						"dateTime": "2019-10-21T10:24:56.000Z",
						"operationPoints": [],
						"value": [
							51.9000015258789
						]
					},
					{
						"id": "{097BF09C-F527-134A-A3C2-DE3947BC25EB}",
						"dateTime": "2019-11-13T22:02:55.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{09A08C74-AF38-E049-AB37-40BC33C0F7BD}",
						"dateTime": "2019-11-29T18:02:08.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{0B43F8D6-B026-C245-957F-115F4741AB6A}",
						"dateTime": "2019-11-15T17:10:32.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{0B660F31-D397-FF44-97EA-9376C1C04837}",
						"dateTime": "2019-11-03T09:33:51.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{0B833AB9-64CC-A344-B3FA-47C6A1E4D63E}",
						"dateTime": "2019-11-01T17:55:32.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{0B8E5813-194F-414D-B12D-4FDB984EFD7B}",
						"dateTime": "2019-11-02T01:46:13.000Z",
						"operationPoints": [],
						"value": [
							52.5999984741211
						]
					},
					{
						"id": "{0CA9274E-77A8-624C-BD4C-EB7BC5BA011A}",
						"dateTime": "2019-11-11T14:39:35.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{0E3216B7-9A39-9749-93E5-C5AA587316AD}",
						"dateTime": "2019-10-24T06:43:12.000Z",
						"operationPoints": [],
						"value": [
							52.5
						]
					},
					{
						"id": "{0E5FC3F9-BF10-E644-B698-712FB88F424E}",
						"dateTime": "2019-11-29T09:06:25.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{0F4698E3-311A-B542-B62E-7D10223847CA}",
						"dateTime": "2019-11-14T14:43:34.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{0FC7C146-5B06-6548-B8CE-793ABC0C5670}",
						"dateTime": "2019-11-24T09:09:40.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{0FED0EA3-DD98-9241-A474-E81388D09625}",
						"dateTime": "2019-11-05T17:40:14.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{11138FB6-6AB7-6645-8029-06D0A6FC1ACC}",
						"dateTime": "2019-11-21T21:06:38.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{12674200-5A0B-DB44-A3D7-BB8EAAE11500}",
						"dateTime": "2019-11-17T09:13:33.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{1302BB88-C740-5A4A-B9D8-EACD829373A5}",
						"dateTime": "2019-11-03T14:50:27.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{1442CE10-9259-D64D-978B-E9B914F1FC1B}",
						"dateTime": "2019-11-06T17:38:23.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{15399DF2-244C-C34B-8F8B-72DEDC73C2F0}",
						"dateTime": "2019-11-11T14:39:52.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{1603FC6E-BAE2-5F46-A209-EDA80F6ABCED}",
						"dateTime": "2019-10-21T18:46:23.000Z",
						"operationPoints": [],
						"value": [
							52.0999984741211
						]
					},
					{
						"id": "{1648415E-C9A4-C043-9850-BDFC8C930CB6}",
						"dateTime": "2019-10-29T05:30:40.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{16E2EC24-B069-5343-8F3F-C416E66E059E}",
						"dateTime": "2019-11-20T09:18:05.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{171DA714-08FE-A641-BE19-38BFCAA6636F}",
						"dateTime": "2019-11-09T21:39:55.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{17CEE0AE-AE1D-B74D-9C25-3D04FBEDF224}",
						"dateTime": "2019-10-25T22:58:25.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{1861C89C-B43D-5C4A-B759-8AE2F9846036}",
						"dateTime": "2019-11-02T14:57:53.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{18DE7EDE-CABE-3249-9BE2-87B95E155089}",
						"dateTime": "2019-10-24T22:11:15.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{1943E045-F7B5-7F4D-AD0E-8A70A75042DC}",
						"dateTime": "2019-10-23T13:11:05.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{199A1C92-321B-F04D-A288-7076AD887D2D}",
						"dateTime": "2019-11-27T16:56:05.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{1A79CE13-E46A-8944-A5FD-F85A838F846C}",
						"dateTime": "2019-11-19T01:18:16.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{1AA05889-775E-4A48-ACAA-47E7040B182B}",
						"dateTime": "2019-11-26T17:39:25.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{1CE56AA7-C0E7-7749-B278-C418D89D6237}",
						"dateTime": "2019-10-18T19:13:51.000Z",
						"operationPoints": [],
						"value": [
							51
						]
					},
					{
						"id": "{1EBF031A-4976-6646-B285-B8212BDBEF60}",
						"dateTime": "2019-11-16T13:17:28.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{20F8A76D-A4EB-4D41-BFE4-EE815C92AD49}",
						"dateTime": "2019-11-06T13:41:15.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{21E9B8A4-7C42-FD44-8AF0-DE5BF9C9D549}",
						"dateTime": "2019-11-23T21:43:56.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{22FEF271-12EA-F544-93CE-3C1137D566DF}",
						"dateTime": "2019-11-25T13:34:37.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{23264B60-4CE6-C545-A3BE-97F89FD9874B}",
						"dateTime": "2019-11-10T17:46:14.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{246D14A9-CBE9-C044-83C2-C44248371EC6}",
						"dateTime": "2019-11-17T01:24:26.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{25760748-CD0E-9240-A8EC-0ABDA822146D}",
						"dateTime": "2019-10-29T13:51:08.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{262A1356-3634-A841-87BE-894F2B4EF8B7}",
						"dateTime": "2019-11-30T21:00:48.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{2652F5AF-A399-EC49-88AE-F6179814EBD9}",
						"dateTime": "2019-10-29T11:27:44.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{27A76A81-5D22-C546-A35E-CFE22423AC0A}",
						"dateTime": "2019-10-25T03:26:24.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{27AD554D-2651-4041-BF68-9D15F7F607FF}",
						"dateTime": "2019-10-30T22:31:34.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{27E64FF7-2637-EB45-BF0A-F26FB68CF5D2}",
						"dateTime": "2019-11-07T21:50:13.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{29FE65B5-715A-1542-8A09-F66496CB6B8F}",
						"dateTime": "2019-10-30T13:36:29.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{2A4E587C-025C-A34F-B55B-F1957B3C9C95}",
						"dateTime": "2019-10-24T01:47:25.000Z",
						"operationPoints": [],
						"value": [
							52.5
						]
					},
					{
						"id": "{2C97B53D-666D-EC40-9939-EEC2A8B6A801}",
						"dateTime": "2019-10-25T11:10:34.000Z",
						"operationPoints": [],
						"value": [
							51
						]
					},
					{
						"id": "{2CE4BB2F-640C-0241-9817-6AFB6BC7C92B}",
						"dateTime": "2019-11-16T17:23:50.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{2DA05E75-1AB6-F648-9F75-9D8308A37893}",
						"dateTime": "2019-10-18T14:29:34.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{2E325AAF-2FCC-9E40-968E-5621C0466154}",
						"dateTime": "2019-11-07T18:04:43.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{30F1AA8E-65C7-8044-B449-25053263DE1E}",
						"dateTime": "2019-11-21T02:13:19.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{320C068B-F6E8-CB49-BF2E-3FA3AA759ACD}",
						"dateTime": "2019-11-12T05:39:46.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{3279E04B-25C6-EC44-B673-DFA2C19B6A5B}",
						"dateTime": "2019-11-22T13:21:05.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{357D23E6-F006-AB41-AFC2-7E473B5C1D91}",
						"dateTime": "2019-10-25T14:21:54.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{359BA54F-3BA8-6346-A3C7-FDCDB7AD371A}",
						"dateTime": "2019-10-20T19:23:02.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{362831E5-73E2-8C44-A1FF-B8770508CFD1}",
						"dateTime": "2019-11-30T01:15:20.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{3686F5B6-0138-A044-89E3-87D8E1801EC9}",
						"dateTime": "2019-11-16T09:06:05.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{368BA057-789B-9343-993E-0E35555FDECD}",
						"dateTime": "2019-11-21T17:04:13.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{381AC023-62AD-E640-B83A-99621C7CF57D}",
						"dateTime": "2019-11-09T01:26:17.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{38D91FC5-1457-8149-BAEE-1289C3E93FE4}",
						"dateTime": "2019-11-25T17:09:04.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{38DFE2F0-42E7-B64C-9895-DF7A5348B7FE}",
						"dateTime": "2019-11-17T05:40:14.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{3908C4D6-794A-A642-8A85-9B240753014E}",
						"dateTime": "2019-11-26T05:29:59.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{39B4A65B-AE53-DE41-B5A5-8CAB5D0F1E34}",
						"dateTime": "2019-11-16T01:44:29.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{3A1ABA41-F4E0-9F45-B369-729A2860E25E}",
						"dateTime": "2019-11-27T13:47:51.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{3A98E8D4-F8A8-544E-B92E-F98C9E9A5C18}",
						"dateTime": "2019-11-02T17:38:20.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{3B29D24D-FFAA-8743-A593-342D6E59C0F0}",
						"dateTime": "2019-11-13T17:42:48.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{3BDB1020-6DED-754C-B664-9AC473DFDF9E}",
						"dateTime": "2019-10-29T05:30:07.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{3D231172-1EB6-6D4D-B14F-A42561C48BB4}",
						"dateTime": "2019-11-23T05:25:42.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{3F3EB5AE-21EF-484C-842E-34C47F83F148}",
						"dateTime": "2019-10-19T06:37:43.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{3F731D9A-2598-FC46-A79D-F1CAB9A29EEF}",
						"dateTime": "2019-10-28T20:00:59.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{3FF07912-CF94-8E45-B066-586DD76A5B08}",
						"dateTime": "2019-10-27T22:34:25.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{4045ED1F-5F74-6543-B964-66CE311C27DF}",
						"dateTime": "2019-11-06T02:14:25.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{407E2414-EAFE-A747-96B7-CBCFF4DE49D0}",
						"dateTime": "2019-10-20T20:05:13.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{41425B27-B6B1-0146-963E-5BFE1A9BC771}",
						"dateTime": "2019-11-20T20:48:55.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{41EFF3EB-8491-464F-9F44-85E6F7AD5C8A}",
						"dateTime": "2019-11-05T01:53:52.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{43549CB5-2E6E-AF48-8C87-B3F8045463A4}",
						"dateTime": "2019-11-21T13:55:12.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{43BE0112-14D6-2141-BFD4-CAA4FDEA9367}",
						"dateTime": "2019-11-26T13:25:24.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{441DB7A0-6EDC-B347-990C-56D0053DD9E3}",
						"dateTime": "2019-11-28T05:28:48.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{44919409-B7EF-6C4D-BC1B-92D615B5F4ED}",
						"dateTime": "2019-10-21T22:21:53.000Z",
						"operationPoints": [],
						"value": [
							52.2000007629395
						]
					},
					{
						"id": "{44C9E8EF-8656-CD4C-AAAA-8D195A3736CB}",
						"dateTime": "2019-10-21T18:44:56.000Z",
						"operationPoints": [],
						"value": [
							51
						]
					},
					{
						"id": "{44D4BBF3-C45B-F64D-9F45-8D4A23E027D3}",
						"dateTime": "2019-11-20T17:16:01.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{46D7475E-7DCE-4044-BF58-CAFCF59274C5}",
						"dateTime": "2019-11-25T01:09:58.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{475C8873-7233-1E40-B1BA-EA00D9ECDFD9}",
						"dateTime": "2019-11-19T13:11:23.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{475C88A2-97DA-D04B-BD73-3E396B5C1EC9}",
						"dateTime": "2019-10-18T02:24:36.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{497606DE-3943-104B-981A-D9888BB69AB8}",
						"dateTime": "2019-11-28T09:08:24.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{49F5E019-8BAD-7542-835D-F077D9F24005}",
						"dateTime": "2019-11-02T05:53:57.000Z",
						"operationPoints": [],
						"value": [
							52.5
						]
					},
					{
						"id": "{4AE233AE-A7F1-734D-B25E-10C8CC855CF3}",
						"dateTime": "2019-11-08T22:31:21.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{4E201857-F233-CE41-9F1D-C58F1061FC99}",
						"dateTime": "2019-11-29T04:17:55.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{4E324946-9BA8-4749-A3B4-A957FC19C3A8}",
						"dateTime": "2019-11-27T05:36:19.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{4FA9F521-25EA-9F40-91E9-4BDA1900B2B0}",
						"dateTime": "2019-11-08T14:16:23.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{503B0210-A402-B749-BEB7-ECD459464988}",
						"dateTime": "2019-11-25T09:23:01.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{50BD9232-0E46-124E-9BA2-537941CEA9C8}",
						"dateTime": "2019-10-21T03:24:16.000Z",
						"operationPoints": [],
						"value": [
							51.9000015258789
						]
					},
					{
						"id": "{51CA9C99-4118-1646-8E21-4C40D3CCD6E0}",
						"dateTime": "2019-11-12T10:17:54.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{52018D91-1FB9-1146-AB5A-AF2A05408C32}",
						"dateTime": "2019-11-11T01:43:48.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{5322F1B4-4DF0-0E4C-A718-83BA40C2E078}",
						"dateTime": "2019-10-23T06:10:46.000Z",
						"operationPoints": [],
						"value": [
							52.7000007629395
						]
					},
					{
						"id": "{53529E01-4AE5-4240-9E00-4838C7E8C6BE}",
						"dateTime": "2019-11-30T04:28:20.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{53BFD6D5-A736-E847-88E6-171512164B32}",
						"dateTime": "2019-10-29T10:15:52.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{53D2326D-EA28-2B49-8BAD-4AE9E1A4FF2D}",
						"dateTime": "2019-11-10T14:38:40.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{53F448B6-0467-3D4C-ADCC-881C837B781C}",
						"dateTime": "2019-11-29T13:10:35.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{5478CFA7-97F9-0E40-8AAA-081779A5CE49}",
						"dateTime": "2019-11-01T14:55:30.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{55806B86-DC0F-4C4D-9A37-04203BE53BB7}",
						"dateTime": "2019-10-19T01:57:44.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{55A2242E-98C8-324C-81FD-876493775183}",
						"dateTime": "2019-11-23T13:52:29.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{5628A67C-E723-7A4E-86E6-3CA76E84D09F}",
						"dateTime": "2019-10-21T18:45:26.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{5777CCB6-6C95-914B-A6FF-35CB9EF84015}",
						"dateTime": "2019-12-02T01:00:16.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{58CFA6A1-57F1-3246-B151-AD8BA666DBCC}",
						"dateTime": "2019-11-19T21:31:23.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{599E880F-48BF-4546-A343-CA804C7B61A6}",
						"dateTime": "2019-10-19T22:04:46.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{5B86EF27-9880-7546-90C8-8A0CC1C37C0D}",
						"dateTime": "2019-10-26T14:26:48.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{5BB0EB9F-51B0-604D-BD8A-2C93A79EB56A}",
						"dateTime": "2019-11-22T13:21:05.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{5C025284-2F48-AC46-9B96-1649F59830CF}",
						"dateTime": "2019-11-27T20:59:35.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{5EC5F23E-EE90-8B40-996B-71256F941365}",
						"dateTime": "2019-11-29T00:48:59.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{5F57B5E4-65D8-F74C-9BEA-4DD912FD2537}",
						"dateTime": "2019-11-13T17:44:21.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{603CFB97-32E7-0649-B975-16CBAD60113D}",
						"dateTime": "2019-10-27T01:01:30.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{60A43CB9-A03B-E640-8435-01C30F95403E}",
						"dateTime": "2019-11-17T17:06:25.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{64EE7770-A564-1C4E-9E0F-CB5544560A78}",
						"dateTime": "2019-11-15T13:20:34.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{67C1D5E3-FEDD-E148-807A-EC78884F3A7C}",
						"dateTime": "2019-11-13T05:40:48.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{681B12B8-804B-CE4D-9C98-62E328E1429A}",
						"dateTime": "2019-11-03T22:32:25.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{68950C96-1ED1-FB41-85D5-151E25D93A24}",
						"dateTime": "2019-10-16T18:48:32.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{6A607CBB-031B-5C46-BA64-532747F7BFDC}",
						"dateTime": "2019-11-23T17:16:21.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{6BE26CC7-25A1-164E-86DB-10DA76B45B2B}",
						"dateTime": "2019-11-24T14:02:24.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{6C3C0CA8-9645-5740-BEE2-0437BC80C1DD}",
						"dateTime": "2019-11-07T01:34:49.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{6DA06662-8101-EF47-9A9A-A6698026A165}",
						"dateTime": "2019-12-01T20:33:44.000Z",
						"operationPoints": [],
						"value": [
							52.5
						]
					},
					{
						"id": "{6E46FADC-290B-B246-8B32-FF03FD23BAE9}",
						"dateTime": "2019-10-26T06:13:10.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{6ED74338-33ED-214F-AA25-4121FFA66AB2}",
						"dateTime": "2019-11-04T05:43:35.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{7041C46D-A647-5645-A1C0-13E73B6CCA3C}",
						"dateTime": "2019-10-29T10:17:40.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{70E186AA-D4A4-444D-9B81-C504E46E02DA}",
						"dateTime": "2019-11-20T01:04:04.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{72CBB0E7-3738-EE41-8666-79DDB626883B}",
						"dateTime": "2019-10-19T22:04:17.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{7371A7BC-0B8E-ED44-BE56-44A02E1C1122}",
						"dateTime": "2019-11-25T22:00:56.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{73861027-FBAD-FC42-AEAB-B7F07BB72F33}",
						"dateTime": "2019-10-21T09:53:06.000Z",
						"operationPoints": [],
						"value": [
							51.9000015258789
						]
					},
					{
						"id": "{741F1431-5509-2643-9DFF-49C98A9D4662}",
						"dateTime": "2019-11-27T20:59:35.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{746DD027-3686-814D-8740-8F205AABDB33}",
						"dateTime": "2019-10-25T22:59:19.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{74AE48D2-ECAD-EE48-BBB0-B68D0D8A5248}",
						"dateTime": "2019-11-08T17:56:58.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{7613039D-401E-E749-B9F7-8BC64FC39E7E}",
						"dateTime": "2019-11-19T09:06:22.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{77B16697-A5D2-5643-AE93-BA857D95379A}",
						"dateTime": "2019-11-30T13:01:14.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{780685F5-BE74-EC45-B0E6-030F4C4499B6}",
						"dateTime": "2019-11-06T02:12:02.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{783512AA-160C-4141-A529-336D7CF9447C}",
						"dateTime": "2019-11-12T22:05:41.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{7D56FA9A-2AE8-E444-9447-6A8CB2A54BE2}",
						"dateTime": "2019-11-22T08:58:16.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{7E543BEE-0211-B641-BE34-CCCDF3E875BC}",
						"dateTime": "2019-11-22T21:05:29.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{7EA12B6D-0A5F-1041-895A-E14B83A693CE}",
						"dateTime": "2019-11-04T21:59:37.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{7EAB1B3E-0671-3E48-BEFC-9190305A4B6A}",
						"dateTime": "2019-10-31T06:22:32.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{800B3CDC-6D16-5446-A020-40E7567B53F7}",
						"dateTime": "2019-10-28T20:00:31.000Z",
						"operationPoints": [],
						"value": [
							51
						]
					},
					{
						"id": "{806E2F26-8DE4-834E-840E-F8E143BA6B36}",
						"dateTime": "2019-10-17T02:17:51.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{81140A5C-17BE-E84C-A827-6616CB41C53E}",
						"dateTime": "2019-11-21T09:28:12.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{825E144E-D85D-CA47-8D7C-1B8FDC1F5E44}",
						"dateTime": "2019-10-31T13:55:10.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{82898A1B-0C5B-F54E-AD87-6D04745D0D29}",
						"dateTime": "2019-11-14T01:36:36.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{82986287-9EE7-E542-A4E6-1FEC2AFCA2B0}",
						"dateTime": "2019-11-06T22:04:20.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{83A105B0-C806-344A-BDEB-83B4778AF66D}",
						"dateTime": "2019-10-22T18:39:52.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{83E55AC1-4B3C-2F46-9FCA-D368BE8B9DBF}",
						"dateTime": "2019-11-17T09:13:33.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{8597C96C-CF81-3D4B-9956-2FB475F8E72F}",
						"dateTime": "2019-11-25T05:09:30.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{86BF61C3-C26A-BC4A-A76F-A67714E04263}",
						"dateTime": "2019-11-15T09:17:55.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{877F83E4-0395-E04D-9BC6-35ED5506BB78}",
						"dateTime": "2019-10-31T17:57:20.000Z",
						"operationPoints": [],
						"value": [
							52.7000007629395
						]
					},
					{
						"id": "{880E6D7F-AEB1-0440-9B6C-FA7C598C8118}",
						"dateTime": "2019-11-24T17:18:44.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{889852BC-4B46-3145-A4EB-95C93186D1CB}",
						"dateTime": "2019-10-30T01:48:35.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{88DFE820-3962-A540-9676-C813EB8E0D16}",
						"dateTime": "2019-10-20T22:58:04.000Z",
						"operationPoints": [],
						"value": [
							51.9000015258789
						]
					},
					{
						"id": "{88F1ADAE-A38F-9847-BC08-8CC7D094202B}",
						"dateTime": "2019-11-06T05:30:06.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{89657C82-8895-2348-B0FC-7009D229AF7A}",
						"dateTime": "2019-11-03T18:05:36.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{8C0642D4-D818-3C4C-B76E-CA3DAC0E0088}",
						"dateTime": "2019-11-21T05:12:24.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{8D1F117B-1718-F94A-A03C-4AC6F98CD9AE}",
						"dateTime": "2019-11-17T12:06:49.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{8DB9E78C-29D8-7A45-BAA9-0BB25E392064}",
						"dateTime": "2019-11-10T05:34:22.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{8E2880A0-3D12-2D47-8950-FEE6F0065F41}",
						"dateTime": "2019-11-10T14:37:50.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{8EADB8D2-9B7E-BF4F-982B-90F92987127E}",
						"dateTime": "2019-11-09T14:03:55.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{8EE8A0E1-4148-A148-8B2D-9EE540B2AF37}",
						"dateTime": "2019-10-17T19:54:33.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{8EF64DAE-3F22-3F4C-80AE-1B6716C12941}",
						"dateTime": "2019-11-28T12:56:19.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{8EFDEAD9-D890-1F42-8B26-BD5EDB207C79}",
						"dateTime": "2019-11-16T05:20:20.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{8FC27FD2-9854-DE45-BB75-A97EA1AB719D}",
						"dateTime": "2019-11-23T01:18:41.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{9175E3FA-C2E6-7742-8223-142738009536}",
						"dateTime": "2019-11-18T01:19:24.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{92373F27-35DE-EF4E-974F-4AD9A126C43A}",
						"dateTime": "2019-11-23T09:31:56.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{92C30494-25BA-B64D-A6E1-B8BD2037BA48}",
						"dateTime": "2019-11-07T05:54:58.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{93C27201-6198-984A-B3F0-BC3FD1EEE6C8}",
						"dateTime": "2019-11-11T22:01:39.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{93E6E2EF-BF2A-5D4F-A4CA-2E3B8F24CFE9}",
						"dateTime": "2019-11-13T20:35:45.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{944BF346-B4D3-6049-8580-8CB34652A8F1}",
						"dateTime": "2019-10-19T09:19:35.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{9571FF00-1CFE-6547-A7D6-29543617C617}",
						"dateTime": "2019-10-29T14:53:54.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{977B1F31-A04B-6248-9E6C-DF160634658E}",
						"dateTime": "2019-10-21T10:34:57.000Z",
						"operationPoints": [],
						"value": [
							51.9000015258789
						]
					},
					{
						"id": "{985E2449-EEBD-644F-BF46-8C8C350690C1}",
						"dateTime": "2019-11-26T01:32:15.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{98683C4F-2FF9-2D46-BE58-3A245E3A2B96}",
						"dateTime": "2019-10-23T17:35:42.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{99267CF5-5BD0-D54A-A9DC-131DBA5C08F7}",
						"dateTime": "2019-10-21T10:14:20.000Z",
						"operationPoints": [],
						"value": [
							51.9000015258789
						]
					},
					{
						"id": "{9AA176DA-5097-A34C-9482-900F68B9C796}",
						"dateTime": "2019-11-04T01:37:33.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{9B36E381-DB86-7747-A31C-6F50EAF14B35}",
						"dateTime": "2019-11-03T02:10:36.000Z",
						"operationPoints": [],
						"value": [
							52.9000015258789
						]
					},
					{
						"id": "{9B961B91-0338-9440-BB93-9D0EB7645D9F}",
						"dateTime": "2019-10-15T17:55:47.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{9C1FF2E5-73E2-6742-8D66-EDA44F764032}",
						"dateTime": "2019-11-18T20:53:35.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{9C5F22CD-3A27-F74A-B1EE-90B85A625334}",
						"dateTime": "2019-11-13T02:06:05.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{9DBBBE3A-086E-8742-892C-30D78E192580}",
						"dateTime": "2019-11-09T05:51:07.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{9EB5D284-CA62-FA4E-BF8F-812EDE0E108B}",
						"dateTime": "2019-10-27T06:28:03.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{9FC9EDFB-96B4-BD4A-A09E-F85381DB69C1}",
						"dateTime": "2019-11-13T14:16:54.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{A0ABF095-08F2-3545-91B9-575F7B5F30E2}",
						"dateTime": "2019-11-25T17:09:04.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{A1701A43-A9B5-9A48-9E44-7105B6C7F760}",
						"dateTime": "2019-11-24T21:18:24.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{A181E0E6-18B6-6749-A5FC-7345AA9DB42E}",
						"dateTime": "2019-11-19T17:51:02.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{A26FFD3F-233F-9347-9DB1-9FFB5A1889A2}",
						"dateTime": "2019-11-01T11:28:03.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{A34FE7DB-F134-EE4F-B35F-5468E2F4E1A7}",
						"dateTime": "2019-10-21T18:46:02.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{A3B799F0-13E2-6A4B-ADCD-12BB34E6CE90}",
						"dateTime": "2019-11-18T09:13:02.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{A64788B3-8592-8740-8D7E-F4157C29F479}",
						"dateTime": "2019-10-24T17:32:38.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{A802A1DE-DC67-0A40-8FE8-2F9D4FF10289}",
						"dateTime": "2019-11-05T13:58:54.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{A924863A-9D81-FF4D-A3BE-FBD8017BB8E2}",
						"dateTime": "2019-11-12T22:06:05.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{AB91D903-1FA7-DE42-9208-6C4721CFC024}",
						"dateTime": "2019-11-24T05:25:39.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{AC333AB4-C854-0041-B758-233FB1712A58}",
						"dateTime": "2019-11-05T05:05:27.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{AD2C8E7E-95F8-2B40-B5EF-4ADB7D00F872}",
						"dateTime": "2019-10-22T22:50:38.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{AEA50DEF-D582-3448-9B92-73DEB853E7F1}",
						"dateTime": "2019-11-22T05:37:32.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{AF944CE7-8777-534B-99D6-BC3997ECB19B}",
						"dateTime": "2019-12-01T13:48:14.000Z",
						"operationPoints": [],
						"value": [
							52.5
						]
					},
					{
						"id": "{AFD41C7F-DC68-A940-AE5D-D76BF6A9F602}",
						"dateTime": "2019-11-09T17:28:26.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{B1C888D6-0CB5-6040-8685-1A117D4ADFF1}",
						"dateTime": "2019-10-29T10:23:46.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{B3033034-5574-F94B-BD6C-BE15AF08B83A}",
						"dateTime": "2019-11-08T14:16:04.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{B34B4E68-D501-294C-84E4-11236698F9E1}",
						"dateTime": "2019-11-22T01:44:43.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{B4638B2D-4800-1747-8161-57C0F9C4CA94}",
						"dateTime": "2019-10-19T14:29:31.000Z",
						"operationPoints": [],
						"value": [
							51.5999984741211
						]
					},
					{
						"id": "{B5857AFF-D476-0140-8C56-196F25400059}",
						"dateTime": "2019-11-28T20:57:47.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{B9BAC833-73C0-1C4C-8E03-1A93654308C5}",
						"dateTime": "2019-10-15T22:37:59.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{BB3FADBD-38AD-C947-9A22-A8427A99B962}",
						"dateTime": "2019-11-18T17:12:39.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{BD8962A1-DA15-2E4A-B614-9401C46520D0}",
						"dateTime": "2019-11-10T21:05:48.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{BD93E5E6-1498-C84F-A979-EAD871BAF20F}",
						"dateTime": "2019-10-31T21:57:52.000Z",
						"operationPoints": [],
						"value": [
							53.0999984741211
						]
					},
					{
						"id": "{BDDA4883-25B7-D84B-A3C2-3E6C270B945E}",
						"dateTime": "2019-12-01T05:17:16.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{BED1ADFF-90DF-F846-9F42-FC9C088994DF}",
						"dateTime": "2019-10-22T13:15:19.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{BF1B2F5D-759A-0A44-A120-F1B7C44E63CE}",
						"dateTime": "2019-10-26T17:21:16.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{C000813E-F0C6-0F4A-A0F5-835F6028193E}",
						"dateTime": "2019-10-23T10:46:11.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{C078B6DD-6940-9C4C-B1DF-1D647F5F2108}",
						"dateTime": "2019-11-14T06:15:37.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{C1862D31-E8C9-ED41-BBC6-D47650EC3B88}",
						"dateTime": "2019-11-11T22:01:24.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{C1B1E30D-85AD-4A4E-BE8C-2AF1B9FA6AD5}",
						"dateTime": "2019-10-20T21:12:10.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{C1E31247-A044-FD4C-AFB1-4372BB45F1FF}",
						"dateTime": "2019-10-26T21:45:07.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{C435E7D7-44D1-EC40-BBB4-0EEE6D206D00}",
						"dateTime": "2019-10-17T21:13:54.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{C4A7829F-2048-7D4A-8D3C-4C9FF2D92585}",
						"dateTime": "2019-11-12T05:39:29.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{C4C97924-60E3-5848-A21A-1FF536CEA3A8}",
						"dateTime": "2019-11-05T09:59:03.000Z",
						"operationPoints": [],
						"value": [
							53.5999984741211
						]
					},
					{
						"id": "{C62D1210-42E2-E841-AF1C-62E2CABB261D}",
						"dateTime": "2019-11-10T01:49:16.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{C6B443E3-00BB-E840-A8AF-082A4AFDE56C}",
						"dateTime": "2019-10-22T10:53:17.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{C792DE57-893E-B747-B429-3CEBCBC01A38}",
						"dateTime": "2019-11-14T21:51:13.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{C79EAFDE-BA07-0B42-A2E6-1BD6075C8C22}",
						"dateTime": "2019-11-15T01:09:35.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{C8317C39-C36D-334A-87BC-B1F7695491AD}",
						"dateTime": "2019-11-01T22:33:10.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{C9943D68-8F20-124B-94FC-D5B43968ADC8}",
						"dateTime": "2019-11-09T14:04:57.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{C9C9E975-D0AE-284F-9AE0-DC8A32B8ED41}",
						"dateTime": "2019-10-16T22:40:31.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{CA4B5FC8-2B14-6341-89E8-F2E9D7D01406}",
						"dateTime": "2019-10-28T01:01:44.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{CF16A099-484F-0448-8275-CE16649E2E67}",
						"dateTime": "2019-11-12T14:53:29.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{CF7E0FDC-7301-2249-8B86-339897D02E78}",
						"dateTime": "2019-10-28T21:48:36.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{D06D48D6-1890-F340-8A08-9EB00F498CF2}",
						"dateTime": "2019-10-28T20:00:11.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{D0F53133-652C-1D40-A92C-C52EE4CAD277}",
						"dateTime": "2019-11-07T14:11:18.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{D37D523A-8C6F-BA4A-B739-3D2B9C724B56}",
						"dateTime": "2019-10-22T18:46:54.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{D3CF1346-123C-C347-8C18-A7A6D9989003}",
						"dateTime": "2019-10-30T18:37:16.000Z",
						"operationPoints": [],
						"value": [
							53.2000007629395
						]
					},
					{
						"id": "{D52FE1C3-123E-0647-8DC5-CFE977588C7C}",
						"dateTime": "2019-11-24T01:04:56.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{D5DFDA5A-6653-CA47-8A43-58C7BA7C9D96}",
						"dateTime": "2019-11-06T10:17:55.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{D604A0C0-3DBA-C348-95CE-A0703B45A43D}",
						"dateTime": "2019-10-28T04:46:54.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{D621937B-4BC0-9C40-A278-B0627E4528A5}",
						"dateTime": "2019-11-15T21:19:26.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{D7C43FB8-0237-7E4C-92BB-EB904F10BC2E}",
						"dateTime": "2019-10-29T22:55:00.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{D82FB522-4755-A541-8A02-BB3015E9C322}",
						"dateTime": "2019-10-27T18:36:30.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{D9029529-E7FD-7341-9E6E-ADF671BFEAE1}",
						"dateTime": "2019-11-02T09:26:46.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{DA569EDE-48DB-EC45-9AFD-F9CD4ADA88EB}",
						"dateTime": "2019-11-27T09:18:44.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{DB675990-6314-0D4B-81B0-B9362B6D6EB4}",
						"dateTime": "2019-10-26T02:04:14.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{DE32506D-A6B7-C94F-A901-BFCFEADE5B17}",
						"dateTime": "2019-11-12T10:42:37.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{DEF224A6-0BA4-834E-85BA-74A88E78240A}",
						"dateTime": "2019-10-21T17:00:50.000Z",
						"operationPoints": [],
						"value": [
							51.9000015258789
						]
					},
					{
						"id": "{DFAC33C9-1B52-854B-86D7-40975D9DF0F8}",
						"dateTime": "2019-10-20T22:48:04.000Z",
						"operationPoints": [],
						"value": [
							51.9000015258789
						]
					},
					{
						"id": "{E0A5874D-CAA5-2F41-9245-0B6B703292FA}",
						"dateTime": "2019-11-11T05:40:06.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{E0C5D992-EB7D-614D-9D04-801F06C3733F}",
						"dateTime": "2019-11-20T05:00:53.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{E25BEE10-241B-BF45-8347-AE04726E9194}",
						"dateTime": "2019-11-16T21:06:54.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{E28843C8-121A-9948-B850-654C3DBC6543}",
						"dateTime": "2019-11-18T13:42:19.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{E28EAE67-FABF-8D47-B6B9-882CDD419E1B}",
						"dateTime": "2019-12-01T09:56:32.000Z",
						"operationPoints": [],
						"value": [
							53.0999984741211
						]
					},
					{
						"id": "{E3935BF3-3B7C-DA43-8311-1CF5A9E2E8B7}",
						"dateTime": "2019-10-29T14:52:12.000Z",
						"operationPoints": [],
						"value": [
							52.7999992370605
						]
					},
					{
						"id": "{E41647E4-C984-254E-89FF-C333E6DFC013}",
						"dateTime": "2019-11-14T18:19:28.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{E4C2904E-A676-7B40-B302-1C85A64C8E18}",
						"dateTime": "2019-11-18T05:23:26.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{E571F1B0-DABA-E046-B63D-3024CE3110DB}",
						"dateTime": "2019-11-21T21:06:38.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{E6CEAFFE-5B30-AD49-87A1-02EF519DD60F}",
						"dateTime": "2019-10-18T14:29:13.000Z",
						"operationPoints": [],
						"value": [
							51
						]
					},
					{
						"id": "{E97C5D35-657C-7D43-9265-5E0E6BF0E984}",
						"dateTime": "2019-10-18T06:36:59.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{E9D58BB4-AB8A-174E-91B9-8CE387CF8B3B}",
						"dateTime": "2019-10-29T13:32:59.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{E9F20847-1AFE-C04E-B9C7-E47590BD4C30}",
						"dateTime": "2019-11-25T13:34:37.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{EA53CBE0-8A4B-F444-A949-5352A980870A}",
						"dateTime": "2019-11-02T22:40:31.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{EB48C3F7-FBC8-524B-96E5-4CB1DAE41B4A}",
						"dateTime": "2019-10-20T10:54:53.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{EBD814E8-BEBE-4A4B-9FDA-492CEE384D3B}",
						"dateTime": "2019-10-20T05:25:21.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{EF98FC36-1981-1946-A41C-986DBA0B1C77}",
						"dateTime": "2019-10-31T06:22:05.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{F0741640-ED51-5949-9238-6E3DBBAD6BB9}",
						"dateTime": "2019-11-12T10:07:48.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{F1B79728-AFC2-4442-9ED7-623A83065067}",
						"dateTime": "2019-10-23T03:16:30.000Z",
						"operationPoints": [],
						"value": [
							52.7999992370605
						]
					},
					{
						"id": "{F3EE9FB9-0FDA-8646-AFB5-1D244DD7B09F}",
						"dateTime": "2019-10-30T13:27:49.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{F3F0B93B-AFD3-4E4E-AD90-75ECD199EA01}",
						"dateTime": "2019-11-01T11:28:47.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{F40A147E-3F27-4847-94EB-36280B680D85}",
						"dateTime": "2019-11-27T01:11:25.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{F5749C9F-29F4-3C4D-98B6-2465F0C5B686}",
						"dateTime": "2019-10-17T06:28:43.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{F6AA23EC-9997-564A-B3E2-BD21488E82D8}",
						"dateTime": "2019-11-05T22:48:39.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{F756D997-1BE6-D74D-9607-BD26E9FBD220}",
						"dateTime": "2019-11-28T16:57:41.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{F844696A-599B-4B44-9465-556E0DF228E7}",
						"dateTime": "2019-11-07T11:21:59.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{F9380AD1-69D6-A24A-A829-52357751061F}",
						"dateTime": "2019-11-03T06:00:47.000Z",
						"operationPoints": [],
						"value": [
							52.7000007629395
						]
					},
					{
						"id": "{FA2E784F-A9C7-B141-A0B0-6257A51C5C4A}",
						"dateTime": "2019-11-13T17:48:48.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{FA55C83E-ED5F-B345-B451-933D6BB4CB0E}",
						"dateTime": "2019-11-29T21:39:38.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{FA64A704-30D3-794D-8A0C-A1326B45A440}",
						"dateTime": "2019-11-19T05:33:19.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{FAE6C075-C540-924D-86A6-BEBFE75011DB}",
						"dateTime": "2019-11-20T13:06:39.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{FB3494AC-B725-4849-A4DF-5837C4E967CA}",
						"dateTime": "2019-11-08T06:31:12.000Z",
						"operationPoints": [],
						"value": [
							51
						]
					},
					{
						"id": "{FBC04C39-560E-914C-BB02-E91A558715D4}",
						"dateTime": "2019-12-01T01:13:39.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{FC0DA64B-BC78-3247-9627-2E82657DD1C9}",
						"dateTime": "2019-10-20T01:36:38.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{FC4CF08D-66A2-F44F-811B-4CA08E42DBB8}",
						"dateTime": "2019-10-23T22:03:27.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{FCD2E9ED-C29E-114B-B77E-2E980D5A439F}",
						"dateTime": "2019-11-15T05:08:40.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{008E67E9-FE44-E24D-8085-CA45B03D9EEC}",
						"dateTime": "2020-05-08T20:52:21.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{012F807E-B316-F24B-93DB-7CCFC5DEE6F0}",
						"dateTime": "2020-06-13T04:59:13.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.0999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{0277ADD1-482C-0E44-9A53-3031735072E0}",
						"dateTime": "2020-06-14T19:13:41.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 144.60000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{02980839-CED2-6340-93CF-BD54D83FA436}",
						"dateTime": "2020-04-27T20:52:43.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 131.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.29998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{03B15A2E-974D-414E-82AC-A50886B8F1E1}",
						"dateTime": "2020-06-17T13:49:49.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 167.10000610351563
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{0450418E-E8BC-DC4C-9A2C-53AE079238CD}",
						"dateTime": "2020-05-30T05:36:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{047BAFC4-961B-9A49-807C-1FDF6C38C754}",
						"dateTime": "2020-05-16T18:35:10.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 161
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 43.79998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{04CBC367-86B8-EC47-B202-68BFEAD13B71}",
						"dateTime": "2020-06-11T21:20:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{06463DCD-7219-D74E-A967-D832C7FCF0E8}",
						"dateTime": "2020-05-17T05:17:17.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							50.5
						]
					},
					{
						"id": "{067553A6-1A1C-204C-915F-6BCDEEB6014D}",
						"dateTime": "2020-05-10T05:09:34.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{06BB83BF-DFE3-894C-BBC3-12B6FC7D6A65}",
						"dateTime": "2020-06-26T05:31:02.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.9000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{06E7065F-927C-5D4E-899B-1F68CDF30921}",
						"dateTime": "2020-05-23T11:50:00.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 168.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{078B14CF-F7B2-7642-8467-C40D5006A21F}",
						"dateTime": "2020-06-01T21:01:03.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 131.39999389648438
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.9000244140625
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{080FB32F-2811-634A-B39E-B150F5FAFD2C}",
						"dateTime": "2020-05-17T00:59:58.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.800000190734863
							}
						],
						"value": [
							50.7000007629395
						]
					},
					{
						"id": "{0879993E-C50C-194B-AA72-8131A0A3EBFA}",
						"dateTime": "2020-06-22T05:07:26.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{0901429B-07F6-B549-8DB6-6680749A8B3E}",
						"dateTime": "2020-05-16T20:26:05.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{0ADD0622-3EE8-E04C-B334-3FF7F39C3ED2}",
						"dateTime": "2020-06-01T22:15:15.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{0B2E247F-C38B-894D-A219-53816E15CFEB}",
						"dateTime": "2020-05-30T13:57:07.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{0BDC7C91-8152-764C-8BD8-896B7E12FC69}",
						"dateTime": "2020-05-06T01:12:02.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{0D30EFA9-5081-0D4F-870A-CA28141EB171}",
						"dateTime": "2020-06-02T05:21:58.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.800000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							}
						],
						"value": [
							50.2000007629395
						]
					},
					{
						"id": "{0E139CC9-F9D3-5448-8E6E-C9D86B201A97}",
						"dateTime": "2020-06-19T11:03:38.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 141.8000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.399993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{0EE39471-A1BE-1846-AAAD-C17BC908C9DE}",
						"dateTime": "2020-05-04T13:40:18.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{13C98CA4-0A8D-3649-9A3E-77D20680081E}",
						"dateTime": "2020-05-15T21:12:32.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 145.89999389648438
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{156D564E-5C0E-E246-8508-BC5475F7526C}",
						"dateTime": "2020-05-09T12:57:45.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{15FBF4EC-CCF2-D44E-ABC0-CE7EEBFFDC2E}",
						"dateTime": "2020-04-27T06:43:53.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{178B1241-13A5-884E-BB83-BC3C0B76D82F}",
						"dateTime": "2020-05-11T05:18:30.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{17B6ADC3-5DFB-CB41-9C38-AD4653D20FAD}",
						"dateTime": "2020-04-28T18:35:26.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 43.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 160.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{180A07AE-82C1-0548-AD6D-754557D73AE6}",
						"dateTime": "2020-05-12T13:24:34.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.4000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 145.60000610351563
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1A98DC5A-8B02-D543-8C31-3B0FCFD09A33}",
						"dateTime": "2020-05-13T05:05:36.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{1AB808ED-C4FC-744D-918F-08AFDC836D1C}",
						"dateTime": "2020-06-05T05:39:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1ADEBC24-5629-5D4F-BA15-8F3C4212DD7F}",
						"dateTime": "2020-06-14T14:25:44.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.900000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.199981689453128
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1BA1A6A9-1B30-ED41-8A01-FF36D9962D6A}",
						"dateTime": "2020-04-26T14:52:22.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 157.8000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.399993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1BFF1CE8-4CFD-FF4C-BC32-55862065FB35}",
						"dateTime": "2020-05-09T01:39:43.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1C9ED6E5-6470-A145-B33C-899C5B79AD19}",
						"dateTime": "2020-04-27T20:52:43.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 129.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.29998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{1CACBD56-59CB-834B-B6D4-A1BE467F5391}",
						"dateTime": "2020-05-11T01:19:01.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1CBA7E40-76B0-5B40-961E-DC1B7EF84F87}",
						"dateTime": "2020-05-07T01:46:48.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{1D0E4AA3-92D5-9041-9711-4B395CFF3D35}",
						"dateTime": "2020-05-08T10:07:25.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 43.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 162.39999389648438
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1D27777F-0519-124F-997A-4B519A3EF81D}",
						"dateTime": "2020-05-18T21:42:30.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1D4298EE-9921-0841-AE9F-6BC370594583}",
						"dateTime": "2020-06-17T21:06:13.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1D523889-9479-FF44-9455-629D8901A010}",
						"dateTime": "2020-06-09T10:55:46.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.9000244140625
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1DA4740F-1535-9944-A10F-58AF91FA504C}",
						"dateTime": "2020-05-31T22:05:14.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1E11D60A-D351-7649-A38E-7B5AAA79F6C8}",
						"dateTime": "2020-06-19T21:13:36.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1EBA8A3F-936A-1A4A-9F23-03636FD9D758}",
						"dateTime": "2020-06-05T14:48:28.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 133.8000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1F76C0FC-BCFE-194E-A9E9-8BD5D2967979}",
						"dateTime": "2020-06-08T12:02:02.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 145.8000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2001C3C0-D64C-8946-875B-D3229523F9E0}",
						"dateTime": "2020-05-04T05:43:48.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{20BB72E7-1DA3-2A41-848C-58F9128A8BC6}",
						"dateTime": "2020-06-04T19:16:43.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 166.39999389648438
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2138FC90-B8AD-5C40-B49B-E342D8036807}",
						"dateTime": "2020-06-09T13:39:03.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 166.6999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.70001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2157A805-3EA5-FD47-818A-458C9F968322}",
						"dateTime": "2020-05-05T13:52:21.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.300018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{218EB47B-3C34-C74D-81A4-037813BF7BB0}",
						"dateTime": "2020-04-26T21:08:03.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 164.1999969482422
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{21931A64-9ED0-4440-BB8A-7B9FCD21829D}",
						"dateTime": "2020-06-07T21:49:55.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.4000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 130.8000030517578
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{21A9C32D-F827-264D-B66D-318F735504F5}",
						"dateTime": "2020-05-11T20:56:57.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.20001220703125
							}
						],
						"value": [
							50.2999992370605
						]
					},
					{
						"id": "{24DECE98-9381-B44C-8946-1822E66FA9DE}",
						"dateTime": "2020-06-01T06:55:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{24DF00C3-3737-C342-BF96-A9DD2749E2D5}",
						"dateTime": "2020-06-05T05:39:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{27E9E167-8168-9047-90A4-910B6C8ACC75}",
						"dateTime": "2020-05-18T03:34:34.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2902C4C8-27AF-CA46-811A-70B32670CEB1}",
						"dateTime": "2020-06-04T01:47:28.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2916D431-5DF6-094B-8674-B5FADAFD73AA}",
						"dateTime": "2020-04-26T06:33:19.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{293DBB87-88ED-3947-85E1-D108CD66E992}",
						"dateTime": "2020-05-22T05:02:13.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2AB062A5-8378-6F4E-B195-4CCBF0BF1F28}",
						"dateTime": "2020-06-24T01:17:24.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2B8F1732-D716-214F-BBC7-6D821557B659}",
						"dateTime": "2020-04-30T14:10:45.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 43.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 163.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2C0D6B70-94CF-8B48-A40E-2036F75C5065}",
						"dateTime": "2020-04-27T10:16:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 163.1999969482422
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2C7C1CDE-5C11-414C-B822-8E2919D494DC}",
						"dateTime": "2020-05-17T14:25:10.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2CE250B7-AAB1-C548-B6CA-91A7DFD203A6}",
						"dateTime": "2020-05-10T01:06:25.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.4000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{2E2D432C-0091-C540-A110-0F378C0BCCFB}",
						"dateTime": "2020-05-23T05:40:16.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.800000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2E80B458-F4D8-F84E-93C3-0AF93FF4467B}",
						"dateTime": "2020-06-07T19:25:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 144.39999389648438
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3027E115-85C0-4F4B-AA69-DD5461C5B6C4}",
						"dateTime": "2020-05-31T21:43:17.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{30F03C19-D530-0E4A-BACE-8EE1DF17D6E6}",
						"dateTime": "2020-04-28T05:17:12.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 133.1999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{3124111E-B59E-7648-BE55-1A8CF2E15737}",
						"dateTime": "2020-05-20T04:56:02.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{312AC8EF-096C-154E-B996-2B80DEAF48DC}",
						"dateTime": "2020-05-27T21:41:18.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 159.89999389648438
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.70001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{31ABC7A9-401C-5C44-9784-C30A07D88C73}",
						"dateTime": "2020-06-25T05:30:21.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.9000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{320032D7-C61D-B745-8C11-63FCBAD6B4CC}",
						"dateTime": "2020-06-03T14:44:43.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.9000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 142.39999389648438
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3302ACC1-FA25-BB41-9302-3648B7D10006}",
						"dateTime": "2020-05-24T01:26:57.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							50.2000007629395
						]
					},
					{
						"id": "{33751653-056D-E645-9EF5-9538C2ED4E03}",
						"dateTime": "2020-05-20T21:09:56.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{352F5F81-B6A4-C441-AACE-88F27125EA66}",
						"dateTime": "2020-06-06T05:59:51.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3813F3A6-5ED0-0C4B-924C-72D42888C1FE}",
						"dateTime": "2020-06-20T21:47:12.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{383DACD7-1F44-A94B-B02B-C64E2797C478}",
						"dateTime": "2020-05-05T09:11:06.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{385556D1-C117-484B-8DDB-C5F3CC514E45}",
						"dateTime": "2020-06-05T00:57:57.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.800000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{392CF582-72A6-2740-AFD0-C70C351D262C}",
						"dateTime": "2020-05-02T22:28:53.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{39A6FD3D-B80D-3E41-B91A-60E39E29A7DB}",
						"dateTime": "2020-05-07T06:04:47.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{39BAD4EE-15D4-5B48-85A8-F09134689F69}",
						"dateTime": "2020-05-25T18:36:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 131.1999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.9000244140625
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{39EC93C9-78AE-3844-A860-D382276537FC}",
						"dateTime": "2020-06-20T17:04:14.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3A5C7572-F200-374A-921D-C90B910ECD5E}",
						"dateTime": "2020-05-15T14:30:35.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 163.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3B9D6935-E6DF-B441-98EA-34A2715A8335}",
						"dateTime": "2020-06-17T13:49:28.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 166.60000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.70001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3BEB681C-B6FD-D34C-BBEF-60496834F98A}",
						"dateTime": "2020-06-10T05:51:53.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3C794BF7-D70C-534E-94D9-F9546F25A236}",
						"dateTime": "2020-05-06T12:47:19.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 138.10000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 43.899993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3CCFFDCC-1840-9547-8F69-13CE63C9AF17}",
						"dateTime": "2020-04-26T17:25:00.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 154
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{3DC785AA-2C2D-8B4E-8FB6-B6D196B36B80}",
						"dateTime": "2020-05-07T14:34:04.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.300018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3E36DD37-A167-F745-96E1-7B71ED269E81}",
						"dateTime": "2020-04-27T06:12:01.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{3F219747-7216-AC40-943C-F7CF05F9D983}",
						"dateTime": "2020-06-24T09:34:28.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3F3171FE-A5FF-384E-B1B7-3DF9DDE489DA}",
						"dateTime": "2020-06-03T21:16:24.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.800018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3FAEF510-633B-CA40-B024-122AADE3AA55}",
						"dateTime": "2020-05-23T14:11:06.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 168.10000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{40493E0F-5FFE-F543-9F95-FFB8DD90E6A0}",
						"dateTime": "2020-06-23T21:39:16.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							44
						]
					},
					{
						"id": "{40787711-C7B3-134E-B1A9-F7CD44CDCCC1}",
						"dateTime": "2020-06-04T19:28:01.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 150.39999389648438
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{434E4B4C-89F6-934E-895A-719E251544F9}",
						"dateTime": "2020-05-19T21:15:41.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 148.60000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{44C8F0B5-2F35-EF43-9633-45E9CEB2608B}",
						"dateTime": "2020-04-27T16:42:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 128.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.199981689453128
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{4537B7A9-735F-1648-A51F-0E3D85FC7849}",
						"dateTime": "2020-06-05T05:39:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{45C393D5-4A1E-B84B-8043-310A6DEA8829}",
						"dateTime": "2020-05-20T21:09:56.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{476A93D5-37D4-D644-86F6-C80838EBCA87}",
						"dateTime": "2020-04-29T13:55:27.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.699981689453128
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{48D4A479-6C47-054B-A9FF-E42E46E73039}",
						"dateTime": "2020-06-17T21:03:52.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{4B20D9AB-8F11-704F-9A7F-B885B98D91B3}",
						"dateTime": "2020-05-16T13:10:45.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 132.1999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{4C0CAEC8-BDA0-6940-AAF9-8555B27B3F32}",
						"dateTime": "2020-05-28T17:24:25.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 168
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.100006103515628
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{4C8ABABD-12BD-464A-AA82-C6630876E1E5}",
						"dateTime": "2020-06-14T01:03:21.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{4D9244BA-57F9-F64A-8528-C516CD1855B6}",
						"dateTime": "2020-05-16T12:25:51.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 165.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.199981689453128
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{4DDC3C8B-D707-254B-B75F-E3F7996C739D}",
						"dateTime": "2020-05-08T13:18:27.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{4E127DB9-8F28-6E44-BE85-C07F7E65AF15}",
						"dateTime": "2020-05-18T10:22:40.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{50193320-524A-014F-A025-D88096526FFF}",
						"dateTime": "2020-05-29T22:21:44.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 130.89999389648438
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.70001220703125
							}
						],
						"value": [
							49.7000007629395
						]
					},
					{
						"id": "{528C7F64-A10A-F948-8AF3-A416D189749D}",
						"dateTime": "2020-05-02T01:11:20.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{5353A788-7DCE-2442-BC25-6E67E8813F1D}",
						"dateTime": "2020-06-06T13:32:44.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							49.5999984741211
						]
					},
					{
						"id": "{53739C62-EC3C-244B-910D-9B477828B915}",
						"dateTime": "2020-05-21T17:08:08.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{55008E79-6982-CB46-B86B-3557F0EBCDAB}",
						"dateTime": "2020-05-26T12:11:59.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 131.89999389648438
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{5520AF6C-6F48-B042-A1D7-F7305879A656}",
						"dateTime": "2020-04-29T05:10:44.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{57386F64-10F8-4940-8DEB-836036A69424}",
						"dateTime": "2020-05-07T06:09:26.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{5764FAC3-F370-0E4A-A944-5ED663357113}",
						"dateTime": "2020-05-01T22:44:20.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{5792CBB3-85E3-654C-A818-9357E0C33BD6}",
						"dateTime": "2020-06-20T01:29:22.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{5796562F-D8CC-5249-A477-93EDCEA2C084}",
						"dateTime": "2020-06-26T13:02:14.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{57E71223-FEAF-7E49-A9ED-C75B325192C9}",
						"dateTime": "2020-05-15T06:14:54.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{59C722C7-FEAE-2E4C-BF89-4D4F46550C9A}",
						"dateTime": "2020-05-19T13:26:09.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{5B751A71-E0A5-9440-A894-61B2107DEBD3}",
						"dateTime": "2020-05-20T08:57:45.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 150.8000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.699981689453128
							}
						],
						"value": [
							49.9000015258789
						]
					},
					{
						"id": "{5BE2BD1A-289D-9548-BFE9-DAABE3C86817}",
						"dateTime": "2020-06-26T20:24:09.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{5DE96363-1E24-0141-B295-6634CBC635DC}",
						"dateTime": "2020-05-19T19:16:50.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 129.1999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.399993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{5DF379BC-6FDB-D445-AB56-18AE96DC8BB8}",
						"dateTime": "2020-06-04T05:35:38.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{5E2C1467-AA19-B24E-BC30-F759AC6C7930}",
						"dateTime": "2020-05-05T01:58:34.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{5F29EE0A-8C06-0C4E-B2BB-2C3838525254}",
						"dateTime": "2020-05-04T21:05:42.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 43.6
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 162.3
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{60122702-5399-3E45-BA76-E023A7F0DEC0}",
						"dateTime": "2020-06-17T21:31:21.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{604274AA-1BE4-CE44-B9BC-6E7E15623FFF}",
						"dateTime": "2020-05-05T20:47:21.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.300018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{6076A987-8F1B-184E-858D-93875B8720AF}",
						"dateTime": "2020-05-21T17:08:08.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{60930070-BD1F-5640-9832-D5CBCFB8D61D}",
						"dateTime": "2020-06-22T01:06:43.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{60C1275A-0263-3348-9E84-9ABA02302B4F}",
						"dateTime": "2020-06-05T18:31:28.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{61722D5D-2027-424A-956E-946E3D8BDD79}",
						"dateTime": "2020-05-07T21:44:21.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.20001220703125
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{625B2FAE-217F-F349-8779-1DE8EFCF0252}",
						"dateTime": "2020-06-12T05:07:21.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.800000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{63A6DE41-E0DD-9F48-8252-B2BA4998C4DA}",
						"dateTime": "2020-04-29T01:14:54.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{64121AC9-00A0-F24A-968D-911AF311DC9D}",
						"dateTime": "2020-05-18T02:58:43.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{64136596-2233-A641-82CC-5F21F7FB453A}",
						"dateTime": "2020-05-02T22:28:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{64BAE899-7EC9-1040-A017-C15CCD7F8E44}",
						"dateTime": "2020-05-07T05:58:29.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{655EEE05-B842-BD4C-B8A2-1F08CAB30919}",
						"dateTime": "2020-06-25T02:05:44.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{65ECADAF-888D-F147-8F3B-0F0FAF592391}",
						"dateTime": "2020-06-22T21:21:07.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{6611C9FF-B6F2-E146-B313-23A99930540B}",
						"dateTime": "2020-05-08T04:22:52.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{66566081-FEED-064C-A7FD-4BDC40636D46}",
						"dateTime": "2020-05-24T07:01:35.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{66BCEAD3-E439-5846-8989-AE6A8A72CF84}",
						"dateTime": "2020-05-02T05:59:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{671AA0CB-75E1-FA47-B3D6-4248BCC5E075}",
						"dateTime": "2020-06-21T05:07:26.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{68E56A4F-AEDF-2346-8221-42AE3797908B}",
						"dateTime": "2020-05-27T18:52:16.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 129.8000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.300018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{69571DEE-CC81-F641-B18B-55892A1444FE}",
						"dateTime": "2020-05-27T13:04:14.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 130.3000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.9000244140625
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{69C04A16-FC9E-7447-97C8-CD2FC721479A}",
						"dateTime": "2020-05-17T21:25:50.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{6AA98373-2530-8145-8CC3-6438E258423D}",
						"dateTime": "2020-06-26T12:49:21.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{6C5DDCBF-1928-5840-B5D8-C914AB801D98}",
						"dateTime": "2020-05-20T14:58:54.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 155.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.699981689453128
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{6C7295E9-8FB6-C545-9022-F1673C8502A2}",
						"dateTime": "2020-04-27T13:08:36.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 126.69999694824219
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.100006103515628
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{6C8B8279-846C-904A-98A6-C90081E27996}",
						"dateTime": "2020-06-18T12:41:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{6D8CA0AF-96E4-084A-B3F8-146E79CC4A82}",
						"dateTime": "2020-05-31T02:24:30.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{6D93579B-EDE3-FA4C-AB8A-F1F3FC85CA23}",
						"dateTime": "2020-05-22T05:02:13.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{6DA481C7-9716-C142-BBE1-F102B37B9125}",
						"dateTime": "2020-06-02T01:14:53.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							}
						],
						"value": [
							50.2999992370605
						]
					},
					{
						"id": "{6E3B04F4-57D3-D341-9660-4F19D188DD6D}",
						"dateTime": "2020-06-01T06:55:55.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{6FF68751-C6D3-BD45-B740-3F7E71ADCF29}",
						"dateTime": "2020-05-17T16:56:35.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 163.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{706B4F6F-D778-5D4B-B1E6-C51373C8E32F}",
						"dateTime": "2020-05-16T05:10:11.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -5
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{71B09CA8-96B9-6A49-8D30-C89AB25876B9}",
						"dateTime": "2020-05-20T17:40:44.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 142.39999389648438
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{73D93188-3506-004F-B9C7-D3EDA0C13142}",
						"dateTime": "2020-06-27T06:28:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{75CCDDB0-C628-F643-804F-742EB4C97953}",
						"dateTime": "2020-06-22T21:21:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 138.89999389648438
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{774C9CB0-7A0B-7745-9349-B17659E2BD4E}",
						"dateTime": "2020-05-22T01:05:02.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.800000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{77513B19-F72D-0143-918A-C0B6C25AEB84}",
						"dateTime": "2020-06-02T14:33:18.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 167.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{77AEA1F9-8C2C-2943-98EB-93769C947CD8}",
						"dateTime": "2020-06-16T12:51:53.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{77F0A051-BB21-2A40-8211-6C5E11833F17}",
						"dateTime": "2020-05-20T21:09:56.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{782FB259-1174-0B45-BFF8-F2112DD73EA8}",
						"dateTime": "2020-05-11T13:44:26.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{792BF283-5A51-7F4D-9C2C-6E9163855038}",
						"dateTime": "2020-06-15T19:11:32.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{793A77C2-8E3C-DA40-B782-E0D6EF9D9075}",
						"dateTime": "2020-05-19T01:49:49.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{79F9419D-9021-BA41-804E-259F3367F00C}",
						"dateTime": "2020-05-26T14:11:09.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.800018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 131.6999969482422
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{7A390A5E-8325-D44B-891F-C3900BA53BBC}",
						"dateTime": "2020-04-29T14:33:16.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{7AF98959-4909-CF47-9E14-852B272AB109}",
						"dateTime": "2020-05-14T05:28:36.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							50.5
						]
					},
					{
						"id": "{7B9B9819-B4D7-4944-928F-7C49198AA088}",
						"dateTime": "2020-06-24T13:36:18.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{7D2400A6-C8D3-9D48-8DC7-03B9339E1F36}",
						"dateTime": "2020-05-09T14:02:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.800018310546878
							}
						],
						"value": [
							50.0999984741211
						]
					},
					{
						"id": "{7E9FA929-9713-FE47-8497-53E556314746}",
						"dateTime": "2020-06-22T21:21:07.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{7F074A01-34A5-454A-B66C-36E877163B82}",
						"dateTime": "2020-04-29T13:55:48.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.699981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{7F1A302B-BC31-B644-A810-A555D5073CF4}",
						"dateTime": "2020-05-27T21:41:18.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 154.89999389648438
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.800018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{7FDDB513-6D85-5049-9B59-E8AF6FB097D1}",
						"dateTime": "2020-06-03T05:45:52.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{812F0914-6C15-EB41-AB12-F0BB692ED671}",
						"dateTime": "2020-06-09T17:38:03.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 144.1999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.70001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{824D1532-5494-0E49-9561-C57CE285709C}",
						"dateTime": "2020-05-28T14:17:11.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.9000244140625
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{82563C95-5E6F-544D-8B2D-7511A5D1FF99}",
						"dateTime": "2020-05-20T21:09:56.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{82BCEADA-3950-A040-B77E-57C97CE03162}",
						"dateTime": "2020-05-20T21:09:56.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{8474F853-F46D-C143-AAA4-EC31321DDD83}",
						"dateTime": "2020-04-30T14:11:08.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 43.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 163.60000610351563
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{86CA03E3-623B-D646-A885-D33532ADC321}",
						"dateTime": "2020-06-19T01:13:03.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{86DAC615-498E-974D-87AD-9526953B822D}",
						"dateTime": "2020-05-08T13:18:27.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 160.8000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 43.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{874444A4-2740-E84A-A373-50816600C9DB}",
						"dateTime": "2020-05-12T05:07:30.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.4000244140625
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{8748B872-DD0F-0841-B2A3-AB29A9651B68}",
						"dateTime": "2020-05-31T05:33:37.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{876AA130-013F-C54E-AD97-615C1185E1CA}",
						"dateTime": "2020-06-03T01:34:27.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.900000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{8953F448-1CD3-9448-A17A-A80F34D433C6}",
						"dateTime": "2020-06-08T04:57:03.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.9000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{897B1C96-B059-1246-9B4F-A4008C373669}",
						"dateTime": "2020-06-24T13:36:18.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{8BA4127F-C820-AF4F-8B9F-6DD44A72313F}",
						"dateTime": "2020-05-06T20:46:23.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{8BB68C50-F8E6-484F-95D7-77D9F069DCA5}",
						"dateTime": "2020-05-03T10:08:46.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{8BCF66F6-37B9-8849-94C7-27CB540572E2}",
						"dateTime": "2020-05-20T21:09:56.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{8BD0856A-761D-8A4B-BC1E-55F9C03A2F3C}",
						"dateTime": "2020-06-05T12:00:54.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.800018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 125.9000015258789
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{8C2EDC49-F965-CB49-9F5A-9B0066088049}",
						"dateTime": "2020-04-28T14:11:33.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 134.10000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{8C73EBBF-1A87-7B4F-8C5E-AA82F60209F1}",
						"dateTime": "2020-06-16T21:08:16.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.4000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{8F2E6579-C215-984D-9954-2A0BB020459C}",
						"dateTime": "2020-04-28T01:34:17.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 128.39999389648438
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{9028FCE8-E226-6445-81D9-B5B9BE5B5B2A}",
						"dateTime": "2020-06-06T20:13:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{91EB1B33-A779-6342-981D-AB0175CC619B}",
						"dateTime": "2020-06-16T20:36:50.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{924195EF-7522-7244-8158-543B02251726}",
						"dateTime": "2020-05-01T10:54:08.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{92B70C38-B0C0-5E4A-A2EF-E80A3099EB5E}",
						"dateTime": "2020-06-27T12:56:44.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.0999755859375
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{93561EC2-1523-AA42-B7A0-63192B8E2900}",
						"dateTime": "2020-05-10T14:49:48.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.4000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							50.2999992370605
						]
					},
					{
						"id": "{9389E204-EC88-344E-AE21-44160733178F}",
						"dateTime": "2020-06-08T17:30:28.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 164.10000610351563
							}
						],
						"value": [
							49.7999992370605
						]
					},
					{
						"id": "{9677D785-3BB3-814B-BA32-DF46E4720FAA}",
						"dateTime": "2020-06-15T19:11:32.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5999755859375
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{96E5B806-CA0A-E045-B0CD-F440F113DC09}",
						"dateTime": "2020-06-08T21:12:46.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.9000244140625
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{96EAA79F-C487-B846-8475-ECC7C9CA544A}",
						"dateTime": "2020-05-06T20:27:17.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.100006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{98BE19E6-B48B-7E4A-8288-B6DFE8D4F54D}",
						"dateTime": "2020-05-20T01:17:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{99180169-FCD7-A442-8913-94E0C70F971A}",
						"dateTime": "2020-06-23T05:44:37.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{99352B2D-86C8-F241-8933-C79F788C33C6}",
						"dateTime": "2020-04-27T20:52:43.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.0999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 134.39999389648438
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{99BF73FB-F2EC-0147-927C-419C77858C0F}",
						"dateTime": "2020-05-25T02:45:15.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{99F4F61B-111D-D04A-8509-95D191A203D1}",
						"dateTime": "2020-06-12T13:51:54.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{9C17A5D5-94B9-F54B-AEB8-A1F1FBF4A4F9}",
						"dateTime": "2020-05-06T05:11:14.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{9C37B45C-A3A5-7B49-BE91-173DEEAE9DDA}",
						"dateTime": "2020-06-07T05:04:52.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{9C79E93E-0590-3D4F-8762-E78B010DE9D4}",
						"dateTime": "2020-06-10T01:18:18.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{9CC34F71-B938-E04D-A3EE-4F0C49258057}",
						"dateTime": "2020-05-20T21:09:56.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{9D9C4E66-EB06-1C45-AA6B-59CDAF09EA9B}",
						"dateTime": "2020-06-21T22:01:19.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A05983F4-8DD1-1F48-9E9C-F5AF5576FC4D}",
						"dateTime": "2020-05-10T21:13:02.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A1922F4A-BA30-734A-96F7-B89D49AF5C67}",
						"dateTime": "2020-05-01T04:56:33.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{A2F85E29-3438-4D43-A929-7566018A541F}",
						"dateTime": "2020-06-16T01:51:15.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{A3051004-3509-A64A-BA55-F107222CE4FE}",
						"dateTime": "2020-05-07T21:21:42.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 43.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 162.6999969482422
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A360B6D1-2021-8E4C-BE39-E2F1CB945082}",
						"dateTime": "2020-06-15T19:11:32.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A5407D08-F018-0A44-B2CB-EED01575F080}",
						"dateTime": "2020-05-15T14:35:58.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 157.89999389648438
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A6A87425-CD4F-2D4D-93EB-096FBE5269F3}",
						"dateTime": "2020-06-06T19:51:13.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 149.10000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.800018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A6E330DC-FA0E-C840-AC15-11655E7FC8B7}",
						"dateTime": "2020-05-29T03:33:46.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A6F88AF2-2EEC-9A4F-BAB2-E5144B00DE4B}",
						"dateTime": "2020-06-19T17:13:48.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A758670B-E5A5-744A-B50E-D03BD533965D}",
						"dateTime": "2020-04-29T21:16:23.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 43.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 162.3000030517578
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{A7DFCD89-5164-2D4B-8C63-3D5E9E561ACC}",
						"dateTime": "2020-06-06T13:15:52.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A86F05EC-F4C5-5F44-AD3C-EFEEBB80A215}",
						"dateTime": "2020-05-30T14:17:13.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.4000244140625
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A9356150-8152-1D45-B9AA-4E6756F0DBA4}",
						"dateTime": "2020-06-07T09:42:38.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							49.5
						]
					},
					{
						"id": "{AB350031-84B1-994C-9DAF-E583484EDB57}",
						"dateTime": "2020-06-13T21:36:05.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.800000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5999755859375
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{AC71B8E0-2BF5-C444-948A-B55A8A92079B}",
						"dateTime": "2020-04-28T20:53:37.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 154.6999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 43.9000244140625
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{AD0864BE-C596-7848-998A-D17A300586D6}",
						"dateTime": "2020-05-17T10:31:08.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{AD9FB77F-1092-F742-A86A-B12291AA6DF0}",
						"dateTime": "2020-05-07T11:17:24.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{ADE90CA2-661A-AB48-806C-3C264A88435D}",
						"dateTime": "2020-04-28T11:20:01.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 43.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 147.39999389648438
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{AE668303-CD1F-1543-B5CC-AFC31C225BB0}",
						"dateTime": "2020-06-14T06:03:20.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.0999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{AE6E0554-6EFD-6549-B456-402147F4767B}",
						"dateTime": "2020-06-19T14:36:36.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 145.3000030517578
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{AEC3B1F5-85EB-BC46-AF75-26E1DCDD793A}",
						"dateTime": "2020-05-14T21:16:47.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 163.3000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.0999755859375
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{AF537AD8-1176-3A4B-A720-FB7C57046C1C}",
						"dateTime": "2020-06-22T21:21:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{B0596C3B-0403-D245-9CBA-057A0B70C409}",
						"dateTime": "2020-05-15T01:22:42.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							50.4000015258789
						]
					},
					{
						"id": "{B07A49AA-05D9-6940-B554-67F189845232}",
						"dateTime": "2020-05-29T17:22:10.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 148.8000030517578
							}
						],
						"value": [
							49.2999992370605
						]
					},
					{
						"id": "{B0A539BB-0397-E348-AC1F-BD62C9511F7A}",
						"dateTime": "2020-04-26T01:50:12.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{B183C842-3AAE-7F4E-B0E2-526693841217}",
						"dateTime": "2020-06-25T13:15:45.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.9000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 167.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{B2AAF12C-21C6-DE41-81C3-CF4E0FC86AE4}",
						"dateTime": "2020-06-08T03:10:54.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.9000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{B38512D8-5194-374C-B724-09F44262606E}",
						"dateTime": "2020-06-24T05:23:01.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{B3A1A8D6-362C-8942-8C6F-5D5037B09D20}",
						"dateTime": "2020-05-14T13:55:16.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 163.60000610351563
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{B3C38FB2-59D9-0D45-BC79-0B77D694AEB2}",
						"dateTime": "2020-06-18T14:30:15.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 148.6999969482422
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{B4D12C61-BF3F-F745-9EF7-EBCA0E886BB6}",
						"dateTime": "2020-05-22T20:50:19.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 147.60000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							}
						],
						"value": [
							50.0999984741211
						]
					},
					{
						"id": "{B5B992DC-0E46-0541-A0AD-1E558A55200F}",
						"dateTime": "2020-06-25T19:51:19.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{B6D95D51-5D3A-1441-9CCB-541D250DD15E}",
						"dateTime": "2020-05-13T13:10:56.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.0999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 162.6999969482422
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{B8D3ACF9-45C8-0A48-8B0D-36696BD2A058}",
						"dateTime": "2020-05-23T01:20:29.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{BA13E143-8563-8441-9FEA-17808B0CA525}",
						"dateTime": "2020-04-29T17:16:44.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{BABE7A6B-1326-DD4A-BDB8-A17720F16AE3}",
						"dateTime": "2020-05-05T06:00:54.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.7
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{BB9000E7-531D-BF40-9895-4B8E1AEFB13C}",
						"dateTime": "2020-04-30T17:00:51.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 163.39999389648438
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{BC4BEFA5-28AB-CD42-A90F-4371061DECAC}",
						"dateTime": "2020-05-09T21:04:23.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.9000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{BD7CC5BB-35FE-D84D-A50F-F194258848E2}",
						"dateTime": "2020-05-10T16:56:20.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{BD8D83CF-5C01-7E48-B292-6BCC3CADBB0C}",
						"dateTime": "2020-05-16T03:29:16.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.900000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{BDA5C021-AEF9-5540-884B-C3E09E1C1BDF}",
						"dateTime": "2020-06-14T12:43:53.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{BDB07F99-F2EE-5044-BFD5-1F3021C3D52E}",
						"dateTime": "2020-06-12T21:23:33.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{BE445CF6-2830-824B-A363-BAB3150D83DE}",
						"dateTime": "2020-05-08T18:43:19.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 43.800018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 131.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{C0CE4AA1-ED86-7F41-B6C5-79ED3B38611A}",
						"dateTime": "2020-05-03T01:06:18.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.2
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{C12D7A11-BFFF-2947-810D-85B1E0A73C60}",
						"dateTime": "2020-05-25T05:13:57.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							49.5
						]
					},
					{
						"id": "{C1C13ABA-3B6E-3D4D-8E48-0F71A58E4D35}",
						"dateTime": "2020-05-20T21:09:56.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{C487477A-AC99-8A4D-AFEA-133AFE1FC4C9}",
						"dateTime": "2020-05-14T10:38:55.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{C504202F-6217-6B4A-B53A-64757E12FE95}",
						"dateTime": "2020-05-16T05:10:11.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{C54601F0-8DA8-0549-9FD4-DFC963488C82}",
						"dateTime": "2020-04-29T05:10:44.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{C58A1CE8-9F9E-B945-BFAF-8B092587286A}",
						"dateTime": "2020-05-08T05:28:13.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{C5DE9E1D-6689-5B41-89E9-4DB630C5754C}",
						"dateTime": "2020-06-15T13:57:19.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{C692599B-5A87-4145-9C88-9ACA199CB413}",
						"dateTime": "2020-05-28T05:05:43.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{C71E7997-6188-0842-98C4-EF22F53A8E92}",
						"dateTime": "2020-05-09T17:11:10.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 133.10000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.100006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{C8626795-4A1B-F44C-9009-D23D9EFDB4B3}",
						"dateTime": "2020-06-07T14:52:39.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							-99990
						]
					},
					{
						"id": "{C8FC9C0E-B0F2-5C45-9826-AE28DF1B3EB1}",
						"dateTime": "2020-05-01T21:56:27.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{CA14CEC4-71E2-B447-B6B8-D619C1DD60ED}",
						"dateTime": "2020-05-30T18:16:37.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							}
						],
						"value": [
							49.5
						]
					},
					{
						"id": "{CA5889E6-E824-6849-8441-20EAAAEC169B}",
						"dateTime": "2020-05-05T21:25:37.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.399993896484378
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{CA8686CE-4088-3D4D-82D0-9CA7A12E4B2F}",
						"dateTime": "2020-06-11T05:07:55.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{CC366B57-D50A-DA46-99F2-4DED3D767151}",
						"dateTime": "2020-06-17T05:47:00.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.9000244140625
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{CD4EE6D4-AF13-F347-A74B-A9940D988350}",
						"dateTime": "2020-06-20T04:57:28.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{CE82B3F5-1655-B74C-98E3-0F83F1FC8C4A}",
						"dateTime": "2020-06-15T11:39:27.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5999755859375
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{CF6E4FC5-A093-3849-81FC-74450387305B}",
						"dateTime": "2020-04-30T21:17:21.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 162.6999969482422
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{CFBE81F2-7013-604B-9918-114082E44AFC}",
						"dateTime": "2020-05-29T13:35:12.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{D0E46DBA-DF25-F049-925C-2F00D892A103}",
						"dateTime": "2020-05-19T13:31:19.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							}
						],
						"value": [
							49.7999992370605
						]
					},
					{
						"id": "{D12C4C87-7C9B-0045-A24F-878EE7EC2C09}",
						"dateTime": "2020-05-03T14:30:47.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 127.0999984741211
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{D178D308-75EA-9040-AB5D-3C8D151AFF71}",
						"dateTime": "2020-06-23T03:42:08.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{D1CE58F9-09C0-8648-8480-DCA1E9F38169}",
						"dateTime": "2020-05-14T01:04:38.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							50.5999984741211
						]
					},
					{
						"id": "{D1D639F1-91E7-2E48-829F-21323670C017}",
						"dateTime": "2020-05-09T02:04:11.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{D32651A2-3DD7-E646-83C7-E2E203CEBB2D}",
						"dateTime": "2020-06-12T01:05:33.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.0999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.800000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{D3D87007-47FF-E841-BA8B-7F808B2D829B}",
						"dateTime": "2020-05-01T13:47:12.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{D629113D-3F91-F449-9311-2F04F9B1B3CE}",
						"dateTime": "2020-06-16T13:16:14.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{D637551F-689B-5747-9156-2D37CDE4AEAB}",
						"dateTime": "2020-06-06T01:15:58.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.900000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{D72839BC-3F3A-084E-8B89-2441772DE34E}",
						"dateTime": "2020-04-26T09:10:53.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 142.89999389648438
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.70001220703125
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{D7C8325B-F20A-B14E-8081-D3148BB0BDCB}",
						"dateTime": "2020-05-20T21:09:56.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{D86D1A9A-AFBA-0A40-B432-998D6B7C4400}",
						"dateTime": "2020-05-19T04:58:12.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{D923A88E-D978-504E-816D-C58A1962A10D}",
						"dateTime": "2020-06-25T13:24:29.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 162.6999969482422
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{D9448D09-4F3D-6341-922E-AFF2EA6B290A}",
						"dateTime": "2020-05-30T21:14:29.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							}
						],
						"value": [
							49.5
						]
					},
					{
						"id": "{D9C067E9-553B-534F-BCC5-68E76895E48B}",
						"dateTime": "2020-05-13T01:01:47.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{DA395D8D-FF1D-2547-87C4-69D913C760F8}",
						"dateTime": "2020-05-13T09:48:59.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{DAB7B383-D892-1542-895F-4930C94D2B25}",
						"dateTime": "2020-05-15T19:09:00.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 137.1999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.0999755859375
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{DC7D2584-1133-2C48-87AA-A638A9E8DB22}",
						"dateTime": "2020-05-06T10:22:01.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 163.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 43.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{DCBE2399-03D6-B043-AB97-24F495A58ED7}",
						"dateTime": "2020-06-22T21:21:07.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{DE321395-FD25-284C-9066-A8FA49364681}",
						"dateTime": "2020-06-13T11:20:40.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.0999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{E2EBDD06-4D48-1841-A9FF-E99562A8E4A3}",
						"dateTime": "2020-06-25T19:51:19.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{E2EE44BF-7D10-5744-BAF6-29CB9601BB95}",
						"dateTime": "2020-06-11T01:06:59.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{E393003D-5597-BE48-9D2E-712C22FAB458}",
						"dateTime": "2020-06-26T01:54:09.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.9000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{E3A68705-A914-2941-8F6C-95908A332985}",
						"dateTime": "2020-05-25T10:28:18.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{E3A89D04-B13C-164F-BE44-AE69ACF0C5A2}",
						"dateTime": "2020-05-03T17:05:01.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 166.10000610351563
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{E3BBFE79-0875-9843-9705-B583F75633B1}",
						"dateTime": "2020-06-21T21:52:38.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{E4BE7067-C437-0B48-939D-854C3D3EE059}",
						"dateTime": "2020-05-30T01:35:49.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.900000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.9000244140625
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{E534C64C-B206-4D43-A03C-769328165C5C}",
						"dateTime": "2020-05-12T17:36:25.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 43.9000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 164
							}
						],
						"value": [
							50.4000015258789
						]
					},
					{
						"id": "{E59C4762-0F9A-4C48-B018-8A36B81F4697}",
						"dateTime": "2020-05-12T21:25:00.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50.7000007629395
						]
					},
					{
						"id": "{E6681D50-1ED1-EA4B-9512-7A964A74FC2E}",
						"dateTime": "2020-05-12T05:07:30.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.4000244140625
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{E9ABB005-2B1D-E940-A21A-B3844ABC7056}",
						"dateTime": "2020-05-22T20:40:19.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 167.39999389648438
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{E9D08FD7-D1B9-3344-844B-075024F4E072}",
						"dateTime": "2020-05-20T21:09:56.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{E9D85007-F1F3-294D-8D76-044C37C7152C}",
						"dateTime": "2020-05-21T20:56:49.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							49.9000015258789
						]
					},
					{
						"id": "{EAD141CF-7487-7E41-8E89-7269198F2977}",
						"dateTime": "2020-05-04T01:33:34.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{EC02F22A-C24B-0B4B-A544-0FA0D5370CE4}",
						"dateTime": "2020-06-15T19:11:32.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5999755859375
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{ED822D7C-079A-6E43-8DD9-6945DA238087}",
						"dateTime": "2020-05-25T13:42:21.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{ED893361-2134-A346-A10E-AE10DA9AE18B}",
						"dateTime": "2020-06-21T01:06:54.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{EEAD5166-3510-C94D-B2ED-E4CE2D892408}",
						"dateTime": "2020-06-18T21:10:27.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{EFB9D178-574E-9B48-90A0-EBCAB411D16D}",
						"dateTime": "2020-05-18T21:36:55.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F14C9461-A94A-DF42-864A-B7243FCDF4A4}",
						"dateTime": "2020-05-15T06:16:03.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F235619C-45F0-9643-BAB6-03F3AE3B1523}",
						"dateTime": "2020-06-14T06:03:20.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.0999755859375
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F2B4E3A4-D12A-9A45-9526-04B588B0C4EF}",
						"dateTime": "2020-05-28T20:45:28.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F2D2AA97-6027-D442-B212-408508B6DBFE}",
						"dateTime": "2020-06-20T13:41:24.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F3521FD9-AE11-7345-88B5-F9EA36E9CC8C}",
						"dateTime": "2020-06-24T19:18:09.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F359CF6D-DFD1-C84D-8CB8-E32EC68D0AB8}",
						"dateTime": "2020-06-10T14:18:03.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F402FE18-ADF9-204A-A4BE-3A11988C0C85}",
						"dateTime": "2020-05-29T13:37:39.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F4B0B65B-3A00-5E4F-9B6D-1B3A8C95AF06}",
						"dateTime": "2020-06-10T14:19:02.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F4B57B34-0FC6-3E41-AAD0-5BC75B1BE8F1}",
						"dateTime": "2020-06-04T19:28:01.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 146.60000610351563
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F4E57D8E-5F7C-374B-807C-C264E0B065F5}",
						"dateTime": "2020-06-26T20:19:02.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.800018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F52799DE-B441-7248-B964-B5A176820206}",
						"dateTime": "2020-05-03T05:10:53.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{F5C02701-20ED-E642-93C9-D91287A83C77}",
						"dateTime": "2020-05-03T21:38:12.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{F620128D-F719-C143-91BB-A8D2E938ED80}",
						"dateTime": "2020-06-11T18:07:26.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 110.5999984741211
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F66DD236-A41B-4D49-9E13-3CCCC923C47F}",
						"dateTime": "2020-05-01T01:24:02.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{F6F9D32F-7683-1546-AA55-EC21909E85A6}",
						"dateTime": "2020-05-14T17:14:42.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 136.3000030517578
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F8821CC2-C21F-8047-A773-798ACF648A85}",
						"dateTime": "2020-06-19T05:17:23.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F8C658DA-DBDC-3144-9AA2-621DDAF96DDF}",
						"dateTime": "2020-06-18T05:27:05.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F90CFE03-F4CA-2F4A-9F8C-1CBCE9085F34}",
						"dateTime": "2020-05-30T13:58:01.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{FDF4313A-1365-974E-9145-1AA15C922099}",
						"dateTime": "2020-06-18T17:16:46.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 168.10000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.399993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{FDF6D7B0-5713-DD46-8072-E81E94778141}",
						"dateTime": "2020-05-10T09:31:52.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							50.2999992370605
						]
					},
					{
						"id": "{FE9276A6-BB60-8144-B2F8-DCA3FA08CA35}",
						"dateTime": "2020-06-13T05:26:58.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.0999755859375
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{FED8E9EB-2F41-FE4C-9FEB-9E2C7C4E46BA}",
						"dateTime": "2020-05-11T17:21:07.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							50.2000007629395
						]
					},
					{
						"id": "{00738C8B-0C16-FB47-81C2-7D49CBD4439A}",
						"dateTime": "2020-01-24T12:00:32.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{00E1A621-A23E-8046-AED9-677E6D23B038}",
						"dateTime": "2020-02-04T01:17:58.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{014882B8-EF9A-7C42-970E-ECD69264B49F}",
						"dateTime": "2020-02-13T21:26:27.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{0150B3B8-6C4E-334B-9ED2-2A61AFE50864}",
						"dateTime": "2020-02-09T21:08:04.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.1
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.3
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{019C423B-8DB8-B149-8EB9-AAF61A927682}",
						"dateTime": "2020-02-09T14:03:07.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{0236D876-64B2-084D-AED0-B4F44B0946B3}",
						"dateTime": "2020-02-09T09:13:43.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{024CB1FA-9388-B64D-800C-E93D6611877A}",
						"dateTime": "2020-02-27T05:48:24.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{028C9A97-FE59-5E49-B6CE-61F6FCBDEB85}",
						"dateTime": "2020-02-26T17:51:30.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 128
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{03036331-C67C-3842-8ABD-613274A2ED5A}",
						"dateTime": "2020-02-27T13:35:46.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{03154D6C-D9B2-6B4C-8996-5CCCB0A70A02}",
						"dateTime": "2020-02-21T05:49:45.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{056C2CAA-FA54-944A-AA7D-01D5BA27B31C}",
						"dateTime": "2020-02-19T12:51:53.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 163.60000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.199981689453128
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{065F0E6C-E10B-8548-9B39-343EC54CF6C9}",
						"dateTime": "2020-01-20T05:06:02.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{0696C3FF-3562-F34F-8863-CCC31CCD4A5D}",
						"dateTime": "2020-02-15T09:35:45.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 140
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{06B2FC9C-066A-F64D-ABA2-C6167502B4BA}",
						"dateTime": "2020-02-05T01:36:08.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 164.1999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.20001220703125
							}
						],
						"value": [
							54
						]
					},
					{
						"id": "{06CD49A2-DFC9-BC4F-8C93-FEEE418338AA}",
						"dateTime": "2020-02-13T17:41:01.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 131.89999389648438
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{076974D3-F512-F444-B53B-32E7C5C09B68}",
						"dateTime": "2020-02-29T14:47:06.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.9000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{07EB800A-B0CF-014F-94FD-7D3766DD0F59}",
						"dateTime": "2020-01-25T13:23:05.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{080C40B4-F1B0-4E40-A6CA-45A251DE21F3}",
						"dateTime": "2020-02-14T17:54:02.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 166.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.399993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{083E3765-3BD3-5F43-88B3-05F493D13F93}",
						"dateTime": "2020-02-16T04:46:06.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{097F4726-7305-B547-841E-1FDE0978691E}",
						"dateTime": "2020-02-16T13:18:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{0ADA69CC-5980-4240-AA93-3B0CF158F907}",
						"dateTime": "2020-01-20T21:18:46.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{0B1605A9-2519-1749-84AE-6F17DF16CF11}",
						"dateTime": "2020-03-01T21:21:45.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{1198A118-515E-4E4A-8054-8D65A845CC36}",
						"dateTime": "2020-02-29T06:20:53.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{11AE1749-CCD3-4340-88F0-ACC2D1C740B3}",
						"dateTime": "2020-02-29T14:43:38.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.9000244140625
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{124A4BA1-E870-5B4C-A72A-55525A500600}",
						"dateTime": "2020-02-13T21:26:27.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.700000047683716
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{12ED6FA8-1566-984E-8119-0AAE68AC8B90}",
						"dateTime": "2020-02-25T17:27:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{13C48BB0-0081-434C-A597-0B228BB1A92F}",
						"dateTime": "2020-02-13T01:05:23.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{14029D74-5F3B-8045-BC82-FFDFEEF6CCCE}",
						"dateTime": "2020-02-13T21:26:27.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{140A42D5-31DB-1046-B789-741C13D9D24A}",
						"dateTime": "2020-02-06T21:30:30.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 162.60000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 43.899993896484378
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{145E28F6-91FF-1244-8165-3B97A0DD4C88}",
						"dateTime": "2020-02-04T13:22:22.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 167.1999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{154945CB-5FF8-7F42-BC39-A047473367CC}",
						"dateTime": "2020-02-13T17:41:01.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 132.1999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5999755859375
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{15AD9FF4-DB8D-AE46-820B-44EF0BAE6821}",
						"dateTime": "2020-02-26T05:22:38.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{16A35867-B2EC-FB4E-90CE-9F7701AE2DF1}",
						"dateTime": "2020-02-12T17:30:32.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{16D7DDB9-38F8-B041-912E-ACC3FBF7ED51}",
						"dateTime": "2020-03-01T09:31:19.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							51.9000015258789
						]
					},
					{
						"id": "{1CC0D35C-79B9-E14E-B580-97F8666D735A}",
						"dateTime": "2020-02-24T01:01:26.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{1D99C13E-A6B8-5741-BDCA-4C2F86102DD6}",
						"dateTime": "2020-01-26T05:55:26.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{1DA92FF2-4E1D-2D43-992A-FC34E7B57F5C}",
						"dateTime": "2020-01-21T01:02:28.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{1E12F5D4-B8D9-B346-B672-ECD365AFBF93}",
						"dateTime": "2020-02-07T01:05:54.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{1EA005F7-C60D-4348-A264-DEE16BC48BE3}",
						"dateTime": "2020-02-05T16:38:19.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 163.8000030517578
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1F03220A-162D-1748-8647-94A2D12A3373}",
						"dateTime": "2020-01-24T05:03:57.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{1F2124FF-E4F8-184E-AA70-8D05C4769A40}",
						"dateTime": "2020-01-20T03:05:27.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{20BB7958-3A9E-E644-964C-B44E3E06C72A}",
						"dateTime": "2020-02-01T05:37:18.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{213756D1-C934-B349-8DC2-F71CB6BBBF2A}",
						"dateTime": "2020-02-25T05:15:53.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{21DE4563-9E02-2C44-89A6-2A2BB4F76661}",
						"dateTime": "2020-01-20T11:20:12.000Z",
						"operationPoints": [],
						"value": [
							52.5999984741211
						]
					},
					{
						"id": "{22CC0B40-9B46-9F40-8894-7A8D228A04C9}",
						"dateTime": "2020-01-31T21:08:34.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{232A34D6-05C3-F04D-9F9C-D4D32C8C7B2A}",
						"dateTime": "2020-02-18T17:55:59.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.699981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 161.1999969482422
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{23CBE537-090E-AB4C-8F57-ABA50F77CF1D}",
						"dateTime": "2020-01-19T21:07:49.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{24480179-C21E-3947-B301-D5C53C9C627E}",
						"dateTime": "2020-01-28T17:17:25.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 147
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.300018310546878
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{24A46139-BEB3-384F-94DF-D2FC1434B42A}",
						"dateTime": "2020-01-21T21:09:45.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{24E6911C-A7AC-B44D-9E64-9A6904B04777}",
						"dateTime": "2020-01-24T10:03:25.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{25EFF5C5-8542-6145-A673-BA0ED7433A77}",
						"dateTime": "2020-01-29T20:44:25.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{2603F180-7541-D342-A1D9-65B34D9289F0}",
						"dateTime": "2020-02-23T22:20:15.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{278C032A-B2E8-804B-BA74-DD838E57C019}",
						"dateTime": "2020-01-23T21:08:26.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{27DF816C-3938-A449-8224-82B414675314}",
						"dateTime": "2020-02-04T05:56:25.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{27FE0EF9-C1DB-6349-8862-C41F9BD76438}",
						"dateTime": "2020-02-12T21:20:02.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{2A0BFB18-51AB-EA4D-9EAC-1DA14B60BEBB}",
						"dateTime": "2020-01-23T17:11:49.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{2BD871BB-ADA2-3A4E-9565-59A0F67F5284}",
						"dateTime": "2020-03-02T05:37:11.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 160.1999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{2C512691-22A1-7A44-A1AA-BE26C2E3F6B4}",
						"dateTime": "2020-01-28T05:40:44.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							52.7999992370605
						]
					},
					{
						"id": "{2D61A95A-CCF2-C248-88A2-635E24C8C82F}",
						"dateTime": "2020-01-21T21:09:45.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{2D9C6975-138D-594B-B6F9-D5647FBE0AF7}",
						"dateTime": "2020-02-13T21:26:27.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{2DD06186-D0EF-5C42-92F2-A00D9A8BB51C}",
						"dateTime": "2020-02-26T12:59:51.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 156.3000030517578
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{2E5543DF-9A2B-1B42-A605-040E635B6297}",
						"dateTime": "2020-02-11T21:08:30.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							52.5
						]
					},
					{
						"id": "{2E5D34E3-BDCC-4C48-90DA-5FC5428934AC}",
						"dateTime": "2020-02-06T06:02:24.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{2F4BF090-CE6D-D347-99B5-15D1AC0B64D6}",
						"dateTime": "2020-02-25T14:30:08.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{304C47A2-4A7C-F34C-9130-8765EA2F27EE}",
						"dateTime": "2020-02-06T06:02:24.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{308228E0-8F2D-1141-B4C8-A0E94616ED48}",
						"dateTime": "2020-01-29T09:17:44.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{3165CC86-1BAF-1C43-83A7-6730D3A9388E}",
						"dateTime": "2020-02-19T21:10:47.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.4000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 122.9000015258789
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{3169FC2B-FA66-294D-AB45-7871E2052105}",
						"dateTime": "2020-02-23T14:05:43.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 162.1999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{327614AA-1411-B54F-AB63-1A4890985DEE}",
						"dateTime": "2020-01-20T13:50:39.000Z",
						"operationPoints": [],
						"value": [
							52.7000007629395
						]
					},
					{
						"id": "{3417E5C7-EC62-794C-9769-B30CAA8486B7}",
						"dateTime": "2020-02-25T01:03:42.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{34929DA2-2B97-5042-A7B7-4B4F7A7B05DC}",
						"dateTime": "2020-02-06T14:19:13.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 161.39999389648438
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3629A667-86AC-5049-9D2F-E289D6ACADA6}",
						"dateTime": "2020-02-14T01:04:26.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{368C6C1B-9101-4C46-BFA3-BFD909508E06}",
						"dateTime": "2020-01-26T00:59:23.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{374B058D-31EA-0944-AAD6-2B956EA8135C}",
						"dateTime": "2020-02-02T18:11:12.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{380CEB7E-54C3-464C-B682-C10D7A7DC503}",
						"dateTime": "2020-01-25T01:16:46.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							}
						],
						"value": [
							52.5
						]
					},
					{
						"id": "{387564F1-7495-EB40-BC12-6DCADBC0C332}",
						"dateTime": "2020-02-14T09:28:07.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 131.3000030517578
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{39E7AF7F-1799-E14D-9B8B-FEC5E82AB90B}",
						"dateTime": "2020-01-29T17:23:57.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{3C351249-3CE8-9E4F-A932-438DEBC12068}",
						"dateTime": "2020-01-23T05:05:52.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{3C888934-8972-2147-AF90-52E1739E040D}",
						"dateTime": "2020-02-29T01:02:15.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{3E2C9950-B834-A546-914F-BBBED8350B13}",
						"dateTime": "2020-02-13T13:29:55.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.699981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.5
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{3F21F879-CF36-7C40-8D07-D255A4560337}",
						"dateTime": "2020-02-21T13:32:49.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 128.89999389648438
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{3F2C973D-B83B-9D43-BEB9-E14423038DC8}",
						"dateTime": "2020-02-02T13:41:41.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{3F548DF1-D699-1541-B5C4-AAB822A4EA8E}",
						"dateTime": "2020-02-14T21:47:03.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 140.6999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5999755859375
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{3FCC66BB-D1CF-0845-991A-875E8EA75917}",
						"dateTime": "2020-02-06T01:48:57.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{405103F7-37FD-2645-BE19-3E572E129A82}",
						"dateTime": "2020-01-18T01:05:40.000Z",
						"operationPoints": [],
						"value": [
							53.0999984741211
						]
					},
					{
						"id": "{40DC34CE-79F3-234D-8E56-1190B7521927}",
						"dateTime": "2020-01-21T04:59:32.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{4257F49C-2AED-F447-AB12-6A7E547587E3}",
						"dateTime": "2020-01-31T01:23:57.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{4358E30D-0EA1-394B-B7FB-44FEBD911AE1}",
						"dateTime": "2020-02-29T17:04:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.4000244140625
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{43BD8149-0232-9B4D-9FE7-77EBECB387F8}",
						"dateTime": "2020-02-22T04:12:32.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{43CA6D64-1FA2-CF4B-BD09-CB38D11F5F81}",
						"dateTime": "2020-02-12T17:30:32.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{43E5B46D-BA0E-D145-AC1A-B73415732F5C}",
						"dateTime": "2020-01-30T04:11:40.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{458EE82F-670B-FD4E-930B-FB83E71FEB99}",
						"dateTime": "2020-02-17T17:35:37.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{46B3239E-5B3E-FA49-9700-FB9E8067B4CF}",
						"dateTime": "2020-01-21T14:34:42.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{471FCD35-1FE9-2645-B6A4-1E1A11759E06}",
						"dateTime": "2020-02-23T14:05:43.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.100006103515628
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{4759ADB0-AE6D-154D-9FD0-9116B407108D}",
						"dateTime": "2020-01-28T13:13:02.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{48071B44-5E82-5845-A06F-2DE3381A1657}",
						"dateTime": "2020-01-20T17:29:44.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{4899280A-E61E-1A4F-B70B-E1C0D578868E}",
						"dateTime": "2020-02-24T05:09:03.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{4B689922-68C5-4146-B8D2-A82E7EFE81A7}",
						"dateTime": "2020-01-14T21:41:14.000Z",
						"operationPoints": [],
						"value": [
							52.9000015258789
						]
					},
					{
						"id": "{4B7EAF13-CE76-7747-8B86-1CBC22A60925}",
						"dateTime": "2020-02-27T04:27:34.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{4B8C510D-E1B7-304D-9DC3-F046D39AD36A}",
						"dateTime": "2020-02-17T09:10:22.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{4C95E602-235A-CA42-B25A-B76BE53FA7D8}",
						"dateTime": "2020-02-20T13:42:30.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 142.6999969482422
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{4D5CDFB7-65C4-DA42-BC7A-25AF1E2A6DBB}",
						"dateTime": "2020-02-08T13:10:20.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{4D758BBC-3543-BB4D-87FB-009B376EC138}",
						"dateTime": "2020-02-13T13:29:55.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 130.6999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{4DDD5EC2-D75D-E345-A1F7-D6C6967EE7F7}",
						"dateTime": "2020-02-08T09:04:12.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{4E2C26E9-A353-6A4D-B292-3B4870660A2C}",
						"dateTime": "2020-02-13T17:41:01.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 133.3000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{4F1F9A67-3FE7-6B44-9721-D76A2E37252F}",
						"dateTime": "2020-01-14T21:41:14.000Z",
						"operationPoints": [],
						"value": [
							52.9000015258789
						]
					},
					{
						"id": "{4FDEDA6B-7A88-DB48-8C9A-F7B9558A5AB6}",
						"dateTime": "2020-01-24T21:51:23.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							}
						],
						"value": [
							52.5
						]
					},
					{
						"id": "{52946DB3-BD5D-FD48-9EE8-778D38D04134}",
						"dateTime": "2020-02-11T04:36:13.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{52C5E8C8-6668-DD4F-8968-1333B537AE90}",
						"dateTime": "2020-02-05T16:39:25.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 163.39999389648438
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{53EBC112-15E8-3D48-91B7-C176327FAFF5}",
						"dateTime": "2020-01-16T01:03:00.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{546E6D57-69E4-B947-88EC-823890B9569B}",
						"dateTime": "2020-01-25T05:38:15.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							52.2999992370605
						]
					},
					{
						"id": "{565231C2-66A6-0544-9C68-40A49212F050}",
						"dateTime": "2020-02-22T09:09:03.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{5846D740-78BA-F147-9496-2B50BF320B27}",
						"dateTime": "2020-02-20T17:46:47.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.699981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{597F3D42-2096-F242-A466-BF83EC3F8EB3}",
						"dateTime": "2020-01-24T12:00:32.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{5A5415BF-3657-1248-8BFF-77FD1E75DF09}",
						"dateTime": "2020-02-03T05:12:37.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{5BA445F8-EB98-AB4F-AD6B-E6E9EC6CE0A7}",
						"dateTime": "2020-01-15T21:24:48.000Z",
						"operationPoints": [],
						"value": [
							53.2000007629395
						]
					},
					{
						"id": "{5D0038D0-7EF9-0746-9AF1-331A9D5E8339}",
						"dateTime": "2020-02-11T17:49:25.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							52.5
						]
					},
					{
						"id": "{5D678D8A-FF79-7B49-8740-5AD4926C7416}",
						"dateTime": "2020-03-01T22:21:33.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{5DB789A9-2F68-6E47-BF2E-9C3A49ABD627}",
						"dateTime": "2020-02-20T21:13:59.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.4000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 144.10000610351563
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{5F8A1C22-A7BB-F04B-898B-1A8E03ECB7FC}",
						"dateTime": "2020-02-11T11:56:14.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{609242A2-D44A-304E-9D26-AA342FED13F4}",
						"dateTime": "2020-02-07T21:09:00.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 136.6999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{6138A9D7-EF4C-6F45-A93A-2917E091A8A6}",
						"dateTime": "2020-01-29T05:07:35.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{64420D2C-4F5B-1040-BA00-189E1C812232}",
						"dateTime": "2020-02-23T17:08:33.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{646002B5-6641-5A4B-97F8-223BDEA61C4F}",
						"dateTime": "2020-01-30T10:22:15.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{6480364A-0ABD-014E-9A91-5C23CCAC315F}",
						"dateTime": "2020-01-16T09:19:25.000Z",
						"operationPoints": [],
						"value": [
							51
						]
					},
					{
						"id": "{654749DF-682D-7542-BBD1-7C33A47EB4C0}",
						"dateTime": "2020-02-17T06:05:56.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{66745F71-FDA8-7A48-963B-63CBC796B98D}",
						"dateTime": "2020-01-26T13:41:55.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{66C38A7A-6DFF-4F4A-B849-BC2D6366973C}",
						"dateTime": "2020-02-23T01:04:57.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{672BA48A-8205-6644-964B-1A267E70B68B}",
						"dateTime": "2020-02-17T13:07:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 167.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.199981689453128
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{67459D2D-213A-2D4C-BE65-71BD1A8A97DB}",
						"dateTime": "2020-02-23T09:55:16.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{6750E93A-BABD-FD49-AD90-BA878477C543}",
						"dateTime": "2020-02-12T05:08:47.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{681CF389-A76B-D04D-9DE5-A68070999DA8}",
						"dateTime": "2020-01-18T21:09:16.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{69265B9D-21F9-5341-92F4-D02EA5223C17}",
						"dateTime": "2020-02-12T17:30:32.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{6A8B8FDF-DFFC-9645-AB92-DE0FC5F52C71}",
						"dateTime": "2020-01-30T13:38:36.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{6C4A62A0-27D6-0745-A3DA-4C1507D570BF}",
						"dateTime": "2020-01-19T04:50:30.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{6D18FA83-89E8-1E4B-8679-6DBD5BB4DD71}",
						"dateTime": "2020-02-16T17:26:25.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{6D3ED082-28F8-264C-A518-5B99497212C6}",
						"dateTime": "2020-02-17T21:26:04.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 140.8000030517578
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{6DAD9B41-89CA-664F-8C8A-90253BEAA845}",
						"dateTime": "2020-01-28T01:15:36.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							52.9000015258789
						]
					},
					{
						"id": "{6DB6E4B2-6947-074F-AD94-A6385D030BA4}",
						"dateTime": "2020-02-24T17:06:14.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 153
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{6EA30E57-8385-BA41-BD1B-8A29C7F8D598}",
						"dateTime": "2020-02-12T13:40:43.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{6EBCBD9B-99A0-D24F-93CD-85FEE5A08B7D}",
						"dateTime": "2020-01-18T13:25:02.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{6EF3796B-8396-F448-AA95-83D0811F75A9}",
						"dateTime": "2020-02-18T21:16:55.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 127.5999984741211
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5999755859375
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{7035C213-D008-1D4D-A042-AD18E8D1F84D}",
						"dateTime": "2020-02-03T21:36:07.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 137.39999389648438
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{71CA84B1-74F4-C747-8722-53FAF6B7D1B6}",
						"dateTime": "2020-02-29T06:19:26.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{71DC1EA2-424B-DE42-9EF0-540CD91FE774}",
						"dateTime": "2020-02-23T14:05:43.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{71F02B26-DBA4-5D45-B9DD-0E7CADC031D8}",
						"dateTime": "2020-02-04T17:49:11.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 164.1999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.20001220703125
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{720AD0B8-CD6D-C540-A94D-C174AB54749E}",
						"dateTime": "2020-02-08T01:30:28.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{723FDCE8-C81C-D842-9778-0E4307D37E11}",
						"dateTime": "2020-02-15T13:41:22.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 129.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{74B5CF9D-D30E-0444-800B-49972AA79F0E}",
						"dateTime": "2020-02-15T05:11:14.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{75571A1E-FC4E-C143-A97E-0F63C6B25FA7}",
						"dateTime": "2020-02-05T22:01:14.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 156.60000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.100006103515628
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{76BAFC3A-DB28-9F46-9E75-A9304BA4DDEA}",
						"dateTime": "2020-02-19T09:41:11.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 163.8000030517578
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{77228FFA-338B-B342-8403-3623532663DE}",
						"dateTime": "2020-02-07T10:10:06.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.70001220703125
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{7758E9E3-C2A0-CD4A-8EC1-89561556BF11}",
						"dateTime": "2020-02-12T09:21:49.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{77B15C9D-1A71-AC4E-B383-B756CCE6E910}",
						"dateTime": "2020-02-01T17:11:17.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{78ABF7FD-2BC3-3644-BCDD-8B3A855554F7}",
						"dateTime": "2020-02-26T06:13:04.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{78EA6A78-07AE-AD4F-8AE0-D0DE7986A7BC}",
						"dateTime": "2020-02-24T13:42:11.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{7980C950-047B-E34C-AF65-6A12D2E4DF2F}",
						"dateTime": "2020-01-28T21:44:50.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 133.6999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{79D1FAEC-6D28-854D-B367-8D994E2CABA6}",
						"dateTime": "2020-02-09T09:13:43.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{7A65E6F2-D488-9A42-A79C-9B4AAB4BF3A7}",
						"dateTime": "2020-02-13T21:26:27.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{7AB3327A-CA9C-5747-ACC6-CAC395DBAA47}",
						"dateTime": "2020-02-22T05:12:08.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{7B62E18B-2C7C-F541-8BBC-122478FEBBF7}",
						"dateTime": "2020-01-24T19:01:12.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.70001220703125
							}
						],
						"value": [
							52.2999992370605
						]
					},
					{
						"id": "{7B6702C0-BCB4-3F46-9A40-D509CBA3F52A}",
						"dateTime": "2020-02-22T17:06:13.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{7BC63EAF-9E04-B642-AAF3-3E8A4D8AD85E}",
						"dateTime": "2020-02-27T13:04:35.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{7BF8BEEB-7B1F-3F44-AF64-129436A97D8E}",
						"dateTime": "2020-01-17T13:19:44.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{7C01ED6D-9D1E-B044-9C08-46E1C03FD9CE}",
						"dateTime": "2020-01-31T09:17:35.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.70001220703125
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{7C1528B7-D111-9C46-B333-5E414D31051A}",
						"dateTime": "2020-01-16T21:45:07.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{7CB238C0-FC7A-4D41-B748-7033D33AE14C}",
						"dateTime": "2020-01-19T17:09:14.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{7DFAF60E-8B87-9545-92D4-1683C4201E33}",
						"dateTime": "2020-01-29T01:16:46.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{7EC77AC9-1561-DB41-9506-A0904264F963}",
						"dateTime": "2020-01-26T17:20:56.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{7EFD8F62-FFFA-2F4B-AFDD-F01CE91E7386}",
						"dateTime": "2020-01-18T17:05:40.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{7F3A7240-1CA1-0C42-AEA0-F6047E541C24}",
						"dateTime": "2020-02-12T17:30:32.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{7F8D5E7C-4C5C-AC45-8CDE-9D20C2B7ACC6}",
						"dateTime": "2020-02-25T08:22:42.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{80940D15-31B9-1C4A-8F8D-B95B9A0C7551}",
						"dateTime": "2020-02-22T13:32:43.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{81B8B0DF-F692-4049-972F-2FD8BC7B3C88}",
						"dateTime": "2020-02-21T21:13:52.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.9000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{81D332BB-7B06-594C-A0D1-9FF9AC8BCEE2}",
						"dateTime": "2020-01-21T14:34:56.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{81DABD2C-21BD-D24A-9755-2EB59554F1E8}",
						"dateTime": "2020-01-18T05:49:15.000Z",
						"operationPoints": [],
						"value": [
							53.0999984741211
						]
					},
					{
						"id": "{81E28606-88E6-1C41-92A0-D92EC9D20DA5}",
						"dateTime": "2020-02-10T21:11:39.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{82390776-288B-3B4A-AC9C-175D371E870A}",
						"dateTime": "2020-01-16T13:19:12.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{83DB3A64-69AB-2E45-B556-2622D017AC00}",
						"dateTime": "2020-01-22T11:21:41.000Z",
						"operationPoints": [],
						"value": [
							52.7000007629395
						]
					},
					{
						"id": "{849E05BE-4663-7040-8932-2887B9504778}",
						"dateTime": "2020-02-10T13:20:42.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.9000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 133.1999969482422
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{86412DBE-780F-9E41-835C-1A1E8AE7B5DB}",
						"dateTime": "2020-02-23T05:17:52.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{8805A1C6-C18B-AD48-9F33-A920455286B0}",
						"dateTime": "2020-01-16T05:15:01.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{8BFDFDB0-EF8A-A146-BF99-B9B0BD3D9D0C}",
						"dateTime": "2020-02-13T05:16:45.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{8CD16360-DC08-A64C-9159-C88ED4661628}",
						"dateTime": "2020-01-22T00:58:08.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{8D26B0D0-FB65-F943-9F5D-DA9FC57CEE86}",
						"dateTime": "2020-02-09T05:48:35.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{8D80511D-B1FC-CE4E-8F16-60E1BE829DD6}",
						"dateTime": "2020-02-25T05:15:53.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{8DEB96A3-794D-7B49-A727-08C36D387014}",
						"dateTime": "2020-01-30T21:12:13.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{8DF32078-AB69-F941-99A1-2C69A1764221}",
						"dateTime": "2020-01-24T12:00:32.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{8E1AD3AB-3E60-7C42-B64E-0C49598663E0}",
						"dateTime": "2020-01-19T09:18:11.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{8E6FCBBA-6008-D74D-A2C7-786CD8F05411}",
						"dateTime": "2020-01-19T14:19:07.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{8E889FEC-C96B-A44E-B137-8D8F606AC7B4}",
						"dateTime": "2020-02-01T11:37:25.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{8ECA9811-54D5-2E43-BFD3-05D36A99932B}",
						"dateTime": "2020-02-15T17:04:30.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{90063767-267B-424B-BAD6-F594D1A62634}",
						"dateTime": "2020-01-29T13:09:42.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.800018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{9113C5B4-C51C-1D4A-B51A-0F7424291A49}",
						"dateTime": "2020-02-07T13:06:45.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{91765AF3-260A-5149-BC8C-348F0415AB05}",
						"dateTime": "2020-02-26T21:38:22.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 128.1999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{91A74231-0D0D-7540-BD13-B42AACA7B7D8}",
						"dateTime": "2020-02-15T21:22:03.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 147.60000610351563
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{920005E4-BDE8-B848-B882-45A9C64EE3FD}",
						"dateTime": "2020-02-05T17:15:53.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 143.10000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.399993896484378
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{932F5FB6-5A85-F04B-ABDF-83651215B751}",
						"dateTime": "2020-01-15T05:33:27.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{933E5D9B-EF14-0C46-8C32-B78AFF03CA81}",
						"dateTime": "2020-02-09T01:44:19.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{9563DB3C-1580-134A-B3FF-F8C9D63D8016}",
						"dateTime": "2020-01-24T12:00:32.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{96A9636F-4D06-954E-A3D2-67DDF8460FED}",
						"dateTime": "2020-01-16T17:12:35.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{96F707D4-C7DA-6246-B6F4-CA0060D916C7}",
						"dateTime": "2020-01-28T13:26:23.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 167
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{9741880E-CFF5-A646-842B-EB901F3CD8CF}",
						"dateTime": "2020-01-22T17:56:07.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{97E1815C-E3DF-0F40-A133-9E08A99C721F}",
						"dateTime": "2020-01-22T20:23:19.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{98EF6237-58FA-A640-AC17-4D35B6055555}",
						"dateTime": "2020-02-03T11:56:22.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{9CA6C29D-3A61-DB46-B77C-AAD32D1520CC}",
						"dateTime": "2020-02-17T01:00:02.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{9D007EDC-6054-EF4B-8557-3D08473EC6C4}",
						"dateTime": "2020-01-15T01:04:15.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{9D34A64A-D833-6A43-AB58-0E8245EC7BE0}",
						"dateTime": "2020-02-08T21:34:41.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{9DA7CE67-C2B9-494B-8600-7B41CE08E25A}",
						"dateTime": "2020-01-24T12:00:32.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{9DD369E6-F598-524F-A4D0-35C91385AE98}",
						"dateTime": "2020-02-10T06:27:03.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A11C82ED-E021-9345-B9AE-289DF7794E4B}",
						"dateTime": "2020-01-17T17:55:17.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{A2BB1867-5144-B049-B5AF-881A6D526D18}",
						"dateTime": "2020-01-15T10:03:15.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{A2ECD991-8455-7A46-BF8A-58B602C12A2E}",
						"dateTime": "2020-01-23T01:04:51.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{A3DE6764-40C5-A64B-8F4B-8BC781663B27}",
						"dateTime": "2020-02-08T05:20:34.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.1
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.8
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{A50DBC62-1416-3D4B-9453-E2A9180BD22B}",
						"dateTime": "2020-02-04T13:36:14.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 163.8000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{A5714633-B6CD-AD4B-B36B-D01844B2054B}",
						"dateTime": "2020-02-12T09:21:49.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{A5EECF8E-E975-E640-A61B-A93DDD95E013}",
						"dateTime": "2020-02-08T17:03:21.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{A7BBC39C-F102-E841-BADA-2A9E84463057}",
						"dateTime": "2020-02-10T14:01:29.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 133.3000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.9000244140625
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A7D42E97-62D1-B54E-8903-A4C9B768B3B8}",
						"dateTime": "2020-02-28T17:35:10.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 167.6999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{A83D015C-5281-7B4E-9CD0-807595567C4D}",
						"dateTime": "2020-02-16T06:50:13.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A85A2A47-1ED0-9A42-920C-A65B77BC5CC2}",
						"dateTime": "2020-02-19T00:49:42.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{AB202080-6884-F748-B3B2-C85A760EE660}",
						"dateTime": "2020-02-02T22:07:01.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{AB6FF7CC-15EA-4243-9BF5-B596C215A2D4}",
						"dateTime": "2020-02-01T13:31:32.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.29998779296875
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{ABD3E443-D886-8747-906C-0FABE6445F15}",
						"dateTime": "2020-02-02T01:08:44.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{AC82DB93-3244-7947-BB00-4334E1142D6B}",
						"dateTime": "2020-01-23T09:41:23.000Z",
						"operationPoints": [],
						"value": [
							52.5
						]
					},
					{
						"id": "{ACD42635-B864-2744-A490-C6BFEE26A6CB}",
						"dateTime": "2020-01-15T12:52:31.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{ACE1DA76-4E46-7141-B103-66C2304CA984}",
						"dateTime": "2020-01-31T21:08:34.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{ADE5D0BF-EA72-4B4C-A87D-195D5617CBEF}",
						"dateTime": "2020-02-02T05:09:19.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{AE1A114A-F0D8-B04A-BCD0-BDDD1C396C82}",
						"dateTime": "2020-02-28T21:34:41.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{AE29600A-1885-E742-8044-39060B94252F}",
						"dateTime": "2020-02-14T04:54:47.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{AF99F563-F5B5-FF4A-9626-B7D11945ECFF}",
						"dateTime": "2020-02-05T13:13:46.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 162.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.20001220703125
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{B39260AE-8F18-6447-A2CC-C759BCC046D6}",
						"dateTime": "2020-01-22T13:57:07.000Z",
						"operationPoints": [],
						"value": [
							52.5999984741211
						]
					},
					{
						"id": "{B50F94B3-96D8-DB4E-BA84-119F620FF57A}",
						"dateTime": "2020-02-13T09:35:02.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.0999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 163.6999969482422
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{B53162F7-0B09-A041-A715-148AF20257D3}",
						"dateTime": "2020-01-23T13:17:04.000Z",
						"operationPoints": [],
						"value": [
							52.5
						]
					},
					{
						"id": "{B564E6FD-6993-EF4E-AB80-154A415F2301}",
						"dateTime": "2020-02-14T14:35:45.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 166.60000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5999755859375
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{B58F0822-0770-E84A-8E73-54A33452FAD0}",
						"dateTime": "2020-02-16T21:21:43.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.0999755859375
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{B662804A-7B18-1143-8980-134C994FDC8D}",
						"dateTime": "2020-02-03T01:05:59.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{B785D851-8884-A246-BF02-0B93E935DE64}",
						"dateTime": "2020-02-02T08:57:03.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{BA679CAA-078F-DD42-A39F-F69A2E7176C2}",
						"dateTime": "2020-01-31T13:50:54.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{BA89C2C8-C311-2B4F-AECB-B6B48310722D}",
						"dateTime": "2020-01-30T01:18:24.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{BD87B0AE-DF24-9748-8433-149F398B0C01}",
						"dateTime": "2020-02-20T05:52:11.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{BFCDB57D-3322-A94F-9960-177FA0D9FA9D}",
						"dateTime": "2020-02-25T21:21:42.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 154.6999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{C0778635-D8A1-3840-83E1-3C43C4CB7736}",
						"dateTime": "2020-02-23T14:05:43.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{C0959DE6-2EDB-C142-9B88-93DE31555C01}",
						"dateTime": "2020-01-27T01:07:55.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.4000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							52.7999992370605
						]
					},
					{
						"id": "{C0988030-D74C-E94A-855E-9EBFA1CB7176}",
						"dateTime": "2020-02-06T13:39:04.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 161.39999389648438
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.399993896484378
							}
						],
						"value": [
							55
						]
					},
					{
						"id": "{C0B3BDAD-B0DC-2746-AE88-810C2DB50260}",
						"dateTime": "2020-02-01T21:30:37.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.800018310546878
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{C0F372FA-E567-224B-B90F-49FDC749A2D2}",
						"dateTime": "2020-02-24T09:06:26.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{C294F669-20A3-7949-856B-4E7958334FFD}",
						"dateTime": "2020-02-23T09:55:16.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.0999755859375
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{C355EAFB-63C6-8B41-8F5B-837F3C900F91}",
						"dateTime": "2020-02-10T17:05:16.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 132.6999969482422
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{C503A508-DF8C-784C-8C91-052B8DC70972}",
						"dateTime": "2020-02-15T01:02:34.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{C53D6E62-A580-AF4C-ABD4-0CBBF7708F62}",
						"dateTime": "2020-02-22T21:21:51.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{C5B1BE81-758D-6F40-B2CC-CE915B856BB4}",
						"dateTime": "2020-02-18T09:12:49.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 162.8000030517578
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{C5FC56AE-9486-504E-BCDA-8BD92D0D30DB}",
						"dateTime": "2020-01-26T21:23:30.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{C7B7CA6C-AE70-5643-91B7-731466446705}",
						"dateTime": "2020-01-24T01:01:46.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{C7CC303A-5FBA-8945-957C-71D452AEC36C}",
						"dateTime": "2020-02-13T00:13:20.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{C930E087-BE06-CA42-9191-974F29692DF7}",
						"dateTime": "2020-02-01T11:40:48.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{CC9B7E90-1CE9-D042-978F-A50F8E18424E}",
						"dateTime": "2020-01-26T13:00:56.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{CCF0A83C-1C9C-9845-847B-D7633AF9A044}",
						"dateTime": "2020-01-17T09:20:18.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{CEAD8B61-7E88-9E43-A3AC-C555373D7410}",
						"dateTime": "2020-01-27T21:37:36.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{CF55B19D-96BD-A941-B8CE-0BB06F1BD8B0}",
						"dateTime": "2020-02-15T09:35:45.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 140.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.699981689453128
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{CFB0C7B6-A8B6-1049-A975-1B741FA9D7A3}",
						"dateTime": "2020-02-13T13:29:55.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{D242863B-8BB8-F04E-B5DD-DD26CA4242A0}",
						"dateTime": "2020-02-03T13:37:18.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 161
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{D395B6AA-FEB5-3242-AD48-92340B6B7A4E}",
						"dateTime": "2020-03-01T05:40:36.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.4000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{D498D1E1-4102-AF49-8D4A-56F71AA2A78B}",
						"dateTime": "2020-02-10T17:05:16.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 132.39999389648438
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.70001220703125
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{D4B76A03-CD73-F941-8194-C54FBDB89F70}",
						"dateTime": "2020-02-06T06:02:24.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{D4E8BD50-20C7-FD4E-88F6-ECF4C080EB06}",
						"dateTime": "2020-02-29T14:46:19.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.9000244140625
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{D52C2643-F724-C044-9A47-B73BCD2784FD}",
						"dateTime": "2020-01-25T08:21:02.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{D6B29B62-0A04-F545-AD43-ADB1649290CA}",
						"dateTime": "2020-01-21T17:33:07.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{D75BBAB6-3A25-864B-B2B7-9AF0AD00E770}",
						"dateTime": "2020-01-30T17:09:03.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{D7C9E02D-C1D6-0044-9EE6-498C75199BE6}",
						"dateTime": "2020-02-06T20:36:56.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 160.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{D89F1ABB-51B9-034A-86CD-9C732AFCC798}",
						"dateTime": "2020-02-19T17:05:17.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{D90F98B6-384D-9D42-96AD-7B9407727127}",
						"dateTime": "2020-02-12T21:20:02.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{D934854A-94B1-6148-8CC7-AF739437972D}",
						"dateTime": "2020-01-17T05:39:51.000Z",
						"operationPoints": [],
						"value": [
							53.2999992370605
						]
					},
					{
						"id": "{D936A3FF-BB1B-2F46-91FD-A47BF3C9D15D}",
						"dateTime": "2020-01-14T17:09:09.000Z",
						"operationPoints": [],
						"value": [
							52.7000007629395
						]
					},
					{
						"id": "{DA627A9D-A275-E54F-B78D-1C8D68C7BC30}",
						"dateTime": "2020-02-27T13:04:35.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{DAF321C4-7AE8-8848-B85C-ABD392E4E68D}",
						"dateTime": "2020-02-12T09:21:49.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{DBD23B88-61A3-BD43-ACC4-E65B45DF0DB7}",
						"dateTime": "2020-02-16T09:09:40.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5999755859375
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{DCCD3ACA-DC2E-6349-8D9C-EA9C3FC612AC}",
						"dateTime": "2020-03-01T06:26:28.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.4000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{DDD5E469-8E9A-024C-A776-C83A5D960DAF}",
						"dateTime": "2020-01-27T05:42:59.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							52.7000007629395
						]
					},
					{
						"id": "{DF205D87-F057-0940-BC5B-CC9A2CED2851}",
						"dateTime": "2020-01-15T17:47:11.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{E18ACD22-04AB-1949-8161-5CA1B5657E45}",
						"dateTime": "2020-02-21T04:30:47.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{E270B8E8-AFC6-6C4A-842A-1444D2E1E7F7}",
						"dateTime": "2020-02-21T20:14:00.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 133
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{E301F730-1875-3C43-9475-19020D8DDDAA}",
						"dateTime": "2020-02-19T05:53:36.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{E43862BF-68D9-0C4E-9F0E-FB85C8B64446}",
						"dateTime": "2020-02-09T17:03:43.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.9000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{E47A252C-FF53-CD47-9D6D-B2D137002324}",
						"dateTime": "2020-02-11T01:57:44.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{E743909C-7379-234A-BD28-810760F3F304}",
						"dateTime": "2020-02-11T13:30:46.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.4000244140625
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{E92110EC-D9F8-714E-A940-C81DACAB0FAA}",
						"dateTime": "2020-02-07T05:44:43.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{EA200899-D700-1A44-A985-9764651E28B0}",
						"dateTime": "2020-01-25T17:34:39.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							52.5
						]
					},
					{
						"id": "{EBE5144D-2C53-3344-97BD-F6B51C3B88A8}",
						"dateTime": "2020-02-23T14:05:43.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{ED008ACC-7310-1F44-8129-20098D602BA9}",
						"dateTime": "2020-02-20T14:11:30.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 143.60000610351563
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{ED455CE1-8FB5-E94A-BBE7-4F497DE5E65C}",
						"dateTime": "2020-01-19T04:44:34.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{EDEF37A3-FAF7-BC4E-AFB7-1526CD122726}",
						"dateTime": "2020-02-13T13:29:55.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 131.89999389648438
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{EE350163-1590-9D44-ADBC-87C5176791E7}",
						"dateTime": "2020-02-25T08:22:42.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.199981689453128
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{EE6ACB48-674B-B74A-9EF7-5CF801566023}",
						"dateTime": "2020-03-01T21:21:45.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{EE9C2F22-3004-544F-B81A-98B8E723FFD6}",
						"dateTime": "2020-01-18T09:07:35.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{EEDDBA65-78F0-8744-9E9C-BAA9BE85B5D5}",
						"dateTime": "2020-02-05T13:13:46.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 162.6999969482422
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{F01474B7-821B-9348-AA01-07EA745447B8}",
						"dateTime": "2020-02-13T13:29:55.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.4000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.699981689453128
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{F0B5A797-C2EC-C645-B330-3671BEEE5F04}",
						"dateTime": "2020-02-29T21:07:43.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{F3011239-E838-CF49-B907-F13A752A2E0F}",
						"dateTime": "2020-02-12T01:11:14.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.6
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{F5C14C7C-BE33-1F4E-961D-291476BD4819}",
						"dateTime": "2020-02-05T05:25:13.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 164
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.20001220703125
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{F7AFA117-A588-4946-B459-25F351DC4C46}",
						"dateTime": "2020-02-23T05:17:52.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{F83B415E-30EF-A448-95EA-28F531024913}",
						"dateTime": "2020-01-25T21:29:05.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 130.3000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.800018310546878
							}
						],
						"value": [
							52.5
						]
					},
					{
						"id": "{F8A59956-7A29-0C41-8918-49EBAD6FA31C}",
						"dateTime": "2020-01-17T01:08:29.000Z",
						"operationPoints": [],
						"value": [
							53.5
						]
					},
					{
						"id": "{F8D5A3A9-B113-4542-B1F7-D7610E5B32C0}",
						"dateTime": "2020-01-27T18:02:21.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.70001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F9327D97-01A4-2144-8EB7-8C2154D76046}",
						"dateTime": "2020-02-10T02:00:32.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.9000244140625
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{FCBA5E52-31CB-CB4E-8A61-1329E67FD1C0}",
						"dateTime": "2020-02-21T14:50:44.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 135.60000610351563
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{FCD8452E-CCAE-7C40-A18C-F46561057DBA}",
						"dateTime": "2020-02-24T21:51:32.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 167.60000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							}
						],
						"value": [
							55
						]
					},
					{
						"id": "{FCFEAAA0-2060-8B4E-AD9F-7EF623A8B316}",
						"dateTime": "2020-02-01T00:32:39.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{FD90237C-2D59-FC45-810B-CF3C7D71D8CD}",
						"dateTime": "2020-01-25T01:16:46.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							}
						],
						"value": [
							52.5
						]
					},
					{
						"id": "{FF3F2024-0852-2C41-B6C1-CE85446807B5}",
						"dateTime": "2020-02-18T13:11:58.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 166
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.5
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{00F50814-7972-4A4B-BB1F-B5E09197198A}",
						"dateTime": "2020-03-29T05:01:19.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.800000190734863
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{01CD2605-0FB3-AB43-8029-83801558C78E}",
						"dateTime": "2020-03-23T05:08:04.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{0232A94A-6202-8D4F-9494-2A7F8B45F522}",
						"dateTime": "2020-03-27T20:54:50.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{0247AF98-4BE5-F141-951A-347AD761CE66}",
						"dateTime": "2020-04-06T22:24:37.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{02B76E58-CBD6-A341-9D23-8DF2B2BF77D7}",
						"dateTime": "2020-04-04T01:14:05.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -5.599999904632568
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{02E0EBC7-25B8-9844-84F1-CAA68A09496F}",
						"dateTime": "2020-04-04T10:27:24.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{0358C614-1F77-7447-A4AE-D84CB652D5E1}",
						"dateTime": "2020-03-09T09:04:19.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{05FA7A96-0E44-6F41-9A7B-599A6C122D4B}",
						"dateTime": "2020-04-11T21:20:41.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{06816974-6C89-8C4C-8999-D5398153FFF0}",
						"dateTime": "2020-04-13T10:38:49.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.9000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 133
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{090519C4-11C5-204E-99F6-9E98B76E4D02}",
						"dateTime": "2020-04-21T17:13:29.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{092A5378-0779-FE43-AA03-17F552910C5E}",
						"dateTime": "2020-04-25T16:47:16.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{0A39C28D-6112-3C41-87E1-6DC582B830DB}",
						"dateTime": "2020-03-03T21:31:36.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 131.89999389648438
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{0C78E351-D293-0746-BD2E-3502831BA260}",
						"dateTime": "2020-04-11T05:11:21.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{0C8DDFB2-F479-1F40-B183-1636D80D986F}",
						"dateTime": "2020-03-18T13:13:11.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 167.39999389648438
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{0CAAE41E-918F-A145-9E9B-07F5B99B2DBC}",
						"dateTime": "2020-03-03T17:40:49.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 168.1999969482422
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{0D701A60-6125-0D4C-86E7-D4EEC4AFD977}",
						"dateTime": "2020-03-09T05:50:07.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{0DE21172-B249-4C43-86FD-F529CE3AA67C}",
						"dateTime": "2020-03-24T13:27:10.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							-99990
						]
					},
					{
						"id": "{0E69DC4F-B3BD-C44D-8C70-CDEB97BC9706}",
						"dateTime": "2020-03-23T09:21:35.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.800000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.199981689453128
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{0EEF023A-2CD6-B140-8DEC-1E654DB6D1C6}",
						"dateTime": "2020-03-05T01:25:34.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							}
						],
						"value": [
							52.5999984741211
						]
					},
					{
						"id": "{0F98D4B8-81D7-8941-9358-7300BE956F30}",
						"dateTime": "2020-03-12T05:04:59.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.199981689453128
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{1061D2B8-A924-D141-9E77-402F898A007D}",
						"dateTime": "2020-03-26T17:57:47.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{124F4998-DF9F-7046-A98D-D1F59658FCCA}",
						"dateTime": "2020-03-30T09:21:32.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 167.8000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{12E02018-D351-784C-973F-765E1865C6C0}",
						"dateTime": "2020-03-24T22:36:03.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 164.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{12EAC1C7-C5EE-574F-A6BB-E1924D3D90FC}",
						"dateTime": "2020-03-24T22:35:24.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 162
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{13FBE91D-5BE6-EA46-AE6E-4A040EA9EFF9}",
						"dateTime": "2020-03-23T13:49:13.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{14A8C6E8-C663-9947-9D41-2A835C97D0ED}",
						"dateTime": "2020-04-08T17:32:10.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 172.39999389648438
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.0999755859375
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{14B819C4-3BF6-1A43-9B83-D337AF01DB71}",
						"dateTime": "2020-03-24T13:24:46.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.0999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.800000190734863
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{15F59D23-76B0-1C4E-8A8F-ABA7E1A2151F}",
						"dateTime": "2020-03-30T17:07:03.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.0999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 152.60000610351563
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{162A838F-4D73-FD42-966B-9114590F9010}",
						"dateTime": "2020-03-23T21:30:18.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							}
						],
						"value": [
							51.0999984741211
						]
					},
					{
						"id": "{16522F04-AF4A-7247-8788-06F16B449D2B}",
						"dateTime": "2020-04-16T14:55:57.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{16C3C712-A6FF-5B4E-8922-1CFA7BCB0A2F}",
						"dateTime": "2020-04-01T14:52:52.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.0999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{17777BD8-0A6F-4642-BC5A-962262C794DA}",
						"dateTime": "2020-04-18T09:08:43.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{17A08960-8613-7A43-9609-ADEF7384F4F8}",
						"dateTime": "2020-03-10T17:34:34.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 160.1999969482422
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{195DE1BE-12F2-3945-8D99-A9B985C6407F}",
						"dateTime": "2020-04-03T22:37:49.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1A256620-D944-7649-907E-1B8BFFC084CC}",
						"dateTime": "2020-04-01T06:11:26.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{1A7F71E8-F00D-3B4D-BC02-B97B1660BDB8}",
						"dateTime": "2020-03-19T06:38:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1A88E8C9-B068-0043-A557-0F3D38B910E9}",
						"dateTime": "2020-03-16T05:33:19.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							51.5
						]
					},
					{
						"id": "{1BDA066D-D534-B842-982E-128206E9E12F}",
						"dateTime": "2020-03-05T21:59:25.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{1C5F3C8E-73AF-A442-B9CC-D09351C4F108}",
						"dateTime": "2020-04-07T13:13:48.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{1DA05856-0D54-4649-AAD3-94DE6888AAD4}",
						"dateTime": "2020-03-04T21:51:20.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 157.1999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{1F9CF8C3-A72A-5B41-A7A9-332345E289BF}",
						"dateTime": "2020-03-04T06:28:42.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.0999755859375
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{205408EF-869A-4B49-ADAF-D850676AFF34}",
						"dateTime": "2020-03-24T05:07:57.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -5.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5999755859375
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{21122FC2-285F-B640-BFA8-00249596A633}",
						"dateTime": "2020-04-24T04:36:52.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{2200180B-A637-8945-815E-053AAE9E2FB9}",
						"dateTime": "2020-03-04T13:52:36.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 157.60000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{22135F52-2E86-174A-AD81-13040E66984C}",
						"dateTime": "2020-03-25T04:38:05.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							}
						],
						"value": [
							51.5
						]
					},
					{
						"id": "{22170417-4DB4-924C-9BD0-97E23892FEAF}",
						"dateTime": "2020-04-16T17:53:08.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.800018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 133.8000030517578
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2263B5B0-1BEA-4A41-A717-D06CDD5AA354}",
						"dateTime": "2020-04-16T21:18:17.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{227982C5-A3C3-E645-89E0-F551DB94BA07}",
						"dateTime": "2020-03-17T06:19:34.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2367E297-5482-274A-B83C-7BCE4D12C4D4}",
						"dateTime": "2020-03-04T14:30:48.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 157.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{23E8CE18-DE4B-9247-BB56-7EF10E486F7D}",
						"dateTime": "2020-04-02T22:44:29.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 166.8000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2414D2C8-EA8D-4043-8786-F15F0CD3E62B}",
						"dateTime": "2020-03-06T09:01:40.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 131.60000610351563
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{2438E049-4ECF-0C4A-8F38-F7BDC061B8DF}",
						"dateTime": "2020-04-14T14:37:12.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 130.6999969482422
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{25A544EA-66FA-C84B-832F-3DEE1F969033}",
						"dateTime": "2020-03-12T21:14:49.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							51.9000015258789
						]
					},
					{
						"id": "{263293E8-45B4-BA4A-9153-86146D7FE33F}",
						"dateTime": "2020-03-03T13:59:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 170
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{286DA172-71A6-0541-9079-B816B0CEF06E}",
						"dateTime": "2020-04-25T06:00:57.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{28ADFB11-27CB-D44F-9CAC-C67F8CF41DC5}",
						"dateTime": "2020-03-20T14:07:05.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{28F6EF9F-D40E-8A4A-9FDE-8E8063CD2EA8}",
						"dateTime": "2020-03-22T14:22:11.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.0999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2B36A5DA-46B5-0E4E-BBBC-6DFFCBD2E90B}",
						"dateTime": "2020-04-03T05:09:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -5.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{2BDC1D26-DB54-2A44-BA81-BF7E2CAC7DED}",
						"dateTime": "2020-04-25T05:28:12.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{2D1EF386-EB24-894C-9911-172DBE5A33CC}",
						"dateTime": "2020-04-24T04:30:39.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2D78171E-C5E4-1B49-AA41-919A6D054E0F}",
						"dateTime": "2020-04-16T14:59:46.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2DC89576-A839-6A44-A8CA-DA4F528D5286}",
						"dateTime": "2020-03-12T17:07:18.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							51.9000015258789
						]
					},
					{
						"id": "{2E71A7E0-12EF-E642-8F29-89BBA2506F87}",
						"dateTime": "2020-04-15T12:43:32.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2E7819C3-B8C8-634E-960C-C14B54BAB564}",
						"dateTime": "2020-03-20T13:15:55.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							51.2000007629395
						]
					},
					{
						"id": "{2EC0A6D9-CDDB-DB45-9FA4-14D2E9FC682F}",
						"dateTime": "2020-04-12T05:06:18.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.100006103515628
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{2F140D30-4658-F84F-8298-473D6518FA0B}",
						"dateTime": "2020-03-15T13:22:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{2FB1F27D-B10E-A34B-8441-074E6B235C84}",
						"dateTime": "2020-04-19T17:01:09.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2FEDEB01-D3B6-C84A-8254-604311E6E3D4}",
						"dateTime": "2020-03-10T21:04:49.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 166
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{30A58A97-FDC7-CD48-B78E-F13C7F7B9E51}",
						"dateTime": "2020-03-06T18:49:01.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 169.89999389648438
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3112FFF7-2133-8041-A274-BC69EAEF0757}",
						"dateTime": "2020-03-31T05:25:39.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{31C98E80-4658-3B4B-BFE6-6390BC9F1938}",
						"dateTime": "2020-03-08T06:25:20.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.70001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{32AEBF36-FCB8-084F-80F3-EBB38FE50DDF}",
						"dateTime": "2020-04-16T06:23:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{33D8AB73-87A2-624F-980E-98EB6099E266}",
						"dateTime": "2020-04-14T22:29:48.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{33FE72F2-D7ED-0348-B90C-7CCBD82C7120}",
						"dateTime": "2020-04-24T21:46:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 159
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.300018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3443D179-D80A-AE4A-8C7C-F14564B4C3DB}",
						"dateTime": "2020-03-05T16:39:23.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 146.10000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							}
						],
						"value": [
							55
						]
					},
					{
						"id": "{344ED880-5C1D-2A44-A61B-08E5BCAF8308}",
						"dateTime": "2020-03-04T01:01:56.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{35A39D09-8436-B144-B23F-27DF72A6325B}",
						"dateTime": "2020-03-08T13:07:56.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.79998779296875
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{368D016E-AE00-8042-B8F8-E63005027F45}",
						"dateTime": "2020-03-05T09:43:28.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 168
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{38096CF1-F371-C945-B429-B683E6D9148E}",
						"dateTime": "2020-03-12T01:14:49.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{3871CDFE-B0C9-1042-8D66-0384BC6EB8FA}",
						"dateTime": "2020-03-30T01:21:36.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{391F5676-487E-E246-A92F-BB15C157EF74}",
						"dateTime": "2020-04-14T14:33:05.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 131.1999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3B49B345-1500-4246-8D8C-7165A1978490}",
						"dateTime": "2020-03-07T05:24:16.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.699981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							52.5
						]
					},
					{
						"id": "{3C364118-2E7D-1449-8734-DF47D3BB7CEB}",
						"dateTime": "2020-03-30T21:11:04.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 167.89999389648438
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{3C9E17C1-DF0F-9841-9A18-98FEC5E31E06}",
						"dateTime": "2020-04-11T18:39:55.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{3CA46EB4-D57C-3C48-B718-A7F7D837F416}",
						"dateTime": "2020-04-09T17:08:40.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{3CA914A8-540A-A44C-85A6-940E3B13A16D}",
						"dateTime": "2020-03-03T05:04:21.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{3D2D962B-8D63-D647-B22D-D7F17F1F7A26}",
						"dateTime": "2020-04-02T21:21:29.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 167
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{3D771032-2D2C-1745-9831-CE38525FA928}",
						"dateTime": "2020-03-20T17:38:07.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{3D9C00DD-42F1-E34B-A9DF-1795777233EA}",
						"dateTime": "2020-03-18T05:57:14.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{3DF14EAF-4175-2048-93CE-F429EB4BD76C}",
						"dateTime": "2020-04-12T17:08:52.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 171.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3E16C194-3CAB-7B44-AC40-D918235BD1F8}",
						"dateTime": "2020-04-09T21:14:12.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 133.60000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							}
						],
						"value": [
							60
						]
					},
					{
						"id": "{3E38A20F-F635-6445-95B3-31709BC3E251}",
						"dateTime": "2020-03-29T01:03:45.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{3E65537B-4BB9-3040-8548-4E99C8B97F7F}",
						"dateTime": "2020-03-28T21:07:04.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 131.89999389648438
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{3EBE14CB-2ACD-224A-A56F-07D5B7019E7A}",
						"dateTime": "2020-03-05T05:10:33.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.199981689453128
							}
						],
						"value": [
							52.5
						]
					},
					{
						"id": "{3F8D66A6-AE55-A040-B750-DE16BFC114C1}",
						"dateTime": "2020-03-02T14:36:53.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 132.10000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.0999755859375
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{40791A61-D693-C443-9854-F5C55A2414B4}",
						"dateTime": "2020-04-08T09:17:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{4092EC6D-7CC0-ED42-A700-34407B7CCFB9}",
						"dateTime": "2020-03-08T21:20:24.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 146.6999969482422
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{419405D6-D9BC-4C44-88B1-562522E55CD1}",
						"dateTime": "2020-04-23T01:10:02.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{427357A8-27D9-864C-B9A2-F323DDCC2993}",
						"dateTime": "2020-04-11T01:20:29.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{43042E40-FFBF-FF4C-AAAD-9A58674E8027}",
						"dateTime": "2020-04-19T01:15:41.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{43E8DD2C-A471-5E42-BF5C-D5F84A549EF3}",
						"dateTime": "2020-04-12T14:10:03.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.4000244140625
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{456D5416-BBB7-734A-A3F0-2FC5E33E52D7}",
						"dateTime": "2020-03-15T21:59:16.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{45F9832A-4C66-1D49-AD83-66B49B2F5AD4}",
						"dateTime": "2020-04-21T14:46:45.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{4617B542-FE3E-BA4A-BBF3-01070DB8178D}",
						"dateTime": "2020-04-06T16:39:11.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 165.8000030517578
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{461C41B7-907E-B541-B2AB-44C2B9735974}",
						"dateTime": "2020-03-26T06:34:32.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{47322D61-F99C-B146-B579-E405E876FF84}",
						"dateTime": "2020-03-17T05:35:18.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{474DAC57-DCAD-B348-A224-A16F9187BCC1}",
						"dateTime": "2020-04-09T21:14:12.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 128.6999969482422
							}
						],
						"value": [
							60
						]
					},
					{
						"id": "{48AC5745-0CCF-CC41-B103-6268AD79930F}",
						"dateTime": "2020-03-19T03:54:29.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.20001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{4903EEE3-D3D2-5B47-8FF3-2D664916C3E9}",
						"dateTime": "2020-03-28T09:18:23.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{49B1DFA6-9DBE-D84E-BF2A-838333EE1320}",
						"dateTime": "2020-03-17T21:15:43.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 168.3000030517578
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{4A3C02CD-7410-C24B-A430-9D13A674B35D}",
						"dateTime": "2020-04-18T21:18:47.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{4B4DFA0F-2562-8344-8207-69906D8B53B4}",
						"dateTime": "2020-03-07T01:50:04.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{4EDBFAB8-76F1-7A4B-B3A6-09DA9E027A40}",
						"dateTime": "2020-04-23T05:48:29.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{4F6700B1-2C3C-5448-974C-E0AC780346C5}",
						"dateTime": "2020-03-15T09:15:50.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{4FA2451E-C4AF-944F-8A25-59A127124F26}",
						"dateTime": "2020-03-18T09:26:55.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{50415C1C-0625-6E45-A55D-7BC42B3127F3}",
						"dateTime": "2020-03-07T13:32:26.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{505F9521-B8B0-8842-BFBE-C93910895F54}",
						"dateTime": "2020-04-24T09:25:33.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{50DB9825-80F2-ED4B-B59F-77653BF2ECEF}",
						"dateTime": "2020-03-15T05:10:33.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							51.5999984741211
						]
					},
					{
						"id": "{511DC137-3D37-BE4F-B89B-471DC6024AFB}",
						"dateTime": "2020-04-21T21:34:34.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.700000047683716
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{5131A921-6EE2-2F45-A214-12035279CDCD}",
						"dateTime": "2020-04-13T05:04:11.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{519D938C-D7E9-C14C-85E4-AD015188E482}",
						"dateTime": "2020-04-19T20:59:27.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 129
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{51D77F02-9352-AB4D-BA42-75B52005DF12}",
						"dateTime": "2020-03-28T13:10:17.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{52345434-36BE-C148-A533-41E61B4058AD}",
						"dateTime": "2020-03-05T13:16:54.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 139
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{538E1C44-1526-9B48-9085-9C27A6521406}",
						"dateTime": "2020-03-11T02:17:55.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{550E3518-3829-4547-9906-8D6507FC9BF5}",
						"dateTime": "2020-03-20T05:18:02.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.0999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{55E2706C-E5ED-DB43-9F83-6211600E9683}",
						"dateTime": "2020-03-14T13:07:39.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{55FC5809-91D7-F34F-AB76-CD83453600D6}",
						"dateTime": "2020-03-21T05:40:22.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -5
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{566C4F08-75DE-2848-8352-6FE84C61C804}",
						"dateTime": "2020-04-06T05:27:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{56860CFC-00BB-2949-9A98-204752A1A5A0}",
						"dateTime": "2020-04-06T14:22:02.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 141.60000610351563
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{58373D23-ED26-E44F-90FD-76E5965F8249}",
						"dateTime": "2020-03-13T21:20:11.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 133
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							51.9000015258789
						]
					},
					{
						"id": "{5B51633D-DCB6-8B4F-A63B-437A2CAF6095}",
						"dateTime": "2020-04-08T21:52:38.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 134.89999389648438
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{5D210562-C078-A745-8B98-2FD83AAF3DAC}",
						"dateTime": "2020-04-17T06:47:50.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{5D2369B7-70D8-F24B-82E3-5B83A27FE616}",
						"dateTime": "2020-03-31T21:07:22.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.900000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{5F286CCA-F61B-2847-883C-97CC07B8F325}",
						"dateTime": "2020-04-23T22:50:45.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.700000047683716
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{5F5AA0C6-7B8E-C243-A5DB-C52C479573B5}",
						"dateTime": "2020-03-13T13:43:33.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 169.60000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{644FEA4B-D9C2-C14B-B988-B1F14C2D4D55}",
						"dateTime": "2020-04-02T21:21:29.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 166.89999389648438
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{646B0C93-A981-604F-B796-4E6BE36B86BC}",
						"dateTime": "2020-04-09T13:55:11.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{651AA441-F4A8-5E4B-9B78-C288CF4CA4D3}",
						"dateTime": "2020-03-06T01:50:20.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							52.5
						]
					},
					{
						"id": "{651B0F77-E1F5-A440-8289-99E4775F40DA}",
						"dateTime": "2020-04-21T04:44:05.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{6592C9E5-9CFC-F746-9332-33EC44204BE2}",
						"dateTime": "2020-03-14T17:52:52.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{65C93D92-746E-C745-A6B5-D7C6DD615609}",
						"dateTime": "2020-03-26T12:52:37.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{66CBBDC8-A976-484E-BB76-4EF5E72E8FF3}",
						"dateTime": "2020-03-08T06:12:01.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{6774EA91-D53D-7F4F-8492-CB2AD9382812}",
						"dateTime": "2020-04-15T17:04:10.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 148.89999389648438
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{683F1941-C778-5D48-B32A-240616E922C5}",
						"dateTime": "2020-04-02T05:10:36.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.0999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{68AF11D9-B817-544B-AA43-9BE8D2210E7C}",
						"dateTime": "2020-03-22T09:26:55.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{699A4C16-7C70-DC42-91D3-666A86696971}",
						"dateTime": "2020-03-03T01:03:54.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							}
						],
						"value": [
							53
						]
					},
					{
						"id": "{69F20922-E3A1-3846-91A0-AF1FD3DA41BD}",
						"dateTime": "2020-04-21T09:51:00.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{6AD2FE37-B1EB-F24A-8AF6-850398903CCD}",
						"dateTime": "2020-03-25T10:14:51.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 169.1999969482422
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{6C9E117B-9743-714B-A1DA-5215141194FD}",
						"dateTime": "2020-03-25T00:03:45.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{6CCECDA7-34FE-0A41-B2E1-FF1415419891}",
						"dateTime": "2020-04-21T21:34:34.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{6CE7F1F6-6EDC-D543-898A-42A062A67EE4}",
						"dateTime": "2020-04-24T14:28:30.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{6CFDC781-D444-EB41-A5E0-E802510E6752}",
						"dateTime": "2020-03-09T18:08:06.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 168.10000610351563
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{6D776B71-4DD8-3A41-80C4-6BA34124FA26}",
						"dateTime": "2020-03-28T17:16:58.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 172.6999969482422
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{6E763659-071E-DC4B-B1DE-8910067DA1B9}",
						"dateTime": "2020-03-11T21:08:17.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 130.6999969482422
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{6F6E9041-CC43-044B-A854-BE668970D777}",
						"dateTime": "2020-03-20T01:34:58.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{714AC271-E9A9-B447-8EEF-862317EB9C49}",
						"dateTime": "2020-04-06T03:33:56.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{768C7E2D-DC3F-0547-8FB2-FDC4FFBEB562}",
						"dateTime": "2020-03-23T01:04:05.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{76C302E1-B8AC-2745-99EC-A54F989F00F7}",
						"dateTime": "2020-03-31T17:20:44.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{79E1B8D4-96BE-B14B-8706-CF4A06F48447}",
						"dateTime": "2020-04-15T21:27:27.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 128.10000610351563
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{7A87F11C-212D-544F-8F0C-4255BF58540B}",
						"dateTime": "2020-04-12T09:37:50.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.4000244140625
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{7AB43F84-574F-7C41-BB7E-87FD0D61D005}",
						"dateTime": "2020-03-22T21:14:12.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 129.8000030517578
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{7B5B43B2-0812-EA46-B3F3-991A27C8E94A}",
						"dateTime": "2020-03-24T09:36:30.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{7C58FD4E-8812-2847-8667-6CC8EA07E63F}",
						"dateTime": "2020-04-22T17:46:43.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 126.30000305175781
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{7C8CF99D-21AF-B545-B4EB-97A875DF46C0}",
						"dateTime": "2020-04-15T04:57:06.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{7D446AF0-ADBE-0B4B-9AD4-213AF7BD9730}",
						"dateTime": "2020-04-18T17:03:47.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 126.80000305175781
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{7D6C42AF-D6AD-C541-BFEE-053BEA5CBE55}",
						"dateTime": "2020-04-09T09:17:56.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{7D8BB1D8-3F33-A64F-8126-D126669E328D}",
						"dateTime": "2020-04-25T13:40:02.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.800018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{7E0AA55D-B30B-B746-9C54-D25D2A5F6E6A}",
						"dateTime": "2020-03-13T09:37:04.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 144.6999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{81790DCA-02E6-994F-B452-D81245F29B2F}",
						"dateTime": "2020-03-25T21:53:13.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.5999999046325685
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{8262E48B-3AA6-A74B-A030-3876E150130C}",
						"dateTime": "2020-04-06T14:19:42.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 140.10000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{82DC61EC-F7CE-6A40-90BE-3223D1269EE6}",
						"dateTime": "2020-04-25T20:58:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{832803C5-0165-3840-A705-2A52A9E64E87}",
						"dateTime": "2020-04-01T01:26:22.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{83CFE733-5642-514C-90A1-C55A518B71F2}",
						"dateTime": "2020-03-24T01:05:50.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{8440D66A-6CD8-F241-A8DB-0274173C1A39}",
						"dateTime": "2020-03-27T17:11:29.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.900000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{845F0A16-9CFF-E943-8136-F3C4A1B8F020}",
						"dateTime": "2020-04-11T14:30:43.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{84A94A80-B80B-2846-938A-1D65BCF90C39}",
						"dateTime": "2020-03-29T16:46:08.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -5.199999809265137
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{8521EE41-5669-F44A-AE73-19D2C49B8718}",
						"dateTime": "2020-04-16T05:37:04.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{85C8CB7B-218E-7543-8809-1B00DE97FF54}",
						"dateTime": "2020-03-21T17:03:00.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{85FC3909-9B27-1941-AF79-E729F9C31BDC}",
						"dateTime": "2020-04-03T21:58:24.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.800000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{8649EA31-691A-CC47-932E-9E15C5EF28DD}",
						"dateTime": "2020-03-18T17:10:52.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.0999755859375
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{86A376B5-6A89-274B-81FF-44BAB09AE1C4}",
						"dateTime": "2020-04-09T06:20:58.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{86FE4622-8F9F-D049-824E-88C9B828A496}",
						"dateTime": "2020-04-15T04:58:26.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{87C84C88-38A6-624B-898F-03221E725029}",
						"dateTime": "2020-04-09T00:55:28.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 128.39999389648438
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{883B996B-FAA3-954E-8843-D003747601A3}",
						"dateTime": "2020-03-02T13:49:35.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.0999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 138.60000610351563
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{883EA9E3-524F-1D42-8B2F-89D5D3079022}",
						"dateTime": "2020-04-21T01:00:46.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{88BAF2E3-9515-4F41-88EE-F92E3845DD04}",
						"dateTime": "2020-04-03T11:38:59.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.900000095367432
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{89629C45-8422-2543-8A75-CDA5DA435946}",
						"dateTime": "2020-03-07T09:44:21.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{89756EC0-928C-3645-8379-099EBD2C1D58}",
						"dateTime": "2020-04-01T14:07:06.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.0999755859375
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{8A9A3903-6191-E248-8DD4-CDD6234D670F}",
						"dateTime": "2020-04-08T01:16:14.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{8ABFE8F2-D630-AF46-8648-E98D957C610B}",
						"dateTime": "2020-03-27T05:31:26.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.800000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{8B577D8C-FF7B-244B-94C9-E0A91C115FC2}",
						"dateTime": "2020-03-16T13:59:40.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 166
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.699981689453128
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{8B6615E2-F5CF-8A48-8C22-7349C1CEE1C5}",
						"dateTime": "2020-04-10T14:10:40.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{8C04CCCC-AE2B-494C-8ADB-C7494D5C5BD4}",
						"dateTime": "2020-03-25T00:04:23.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{8CA64091-BCC0-0A47-9F6E-2E97C5491BD6}",
						"dateTime": "2020-03-19T21:41:50.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 132.89999389648438
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{8DA5D80F-428A-EF47-B65F-A9DB23A7B969}",
						"dateTime": "2020-03-20T14:01:32.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{8EA68DBC-005B-D64E-9269-296683C7FCEC}",
						"dateTime": "2020-04-22T05:06:46.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{8EE03FE4-C022-FA42-A2BB-40697434F754}",
						"dateTime": "2020-04-23T22:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.700000047683716
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{8EECB3C7-AD11-E640-89C8-5D0890FA0545}",
						"dateTime": "2020-03-16T21:07:48.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 135.3000030517578
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{8F0991B2-56B4-9F42-9B96-90908984AE79}",
						"dateTime": "2020-03-11T17:30:43.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 138
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{8F483CD4-5989-E34E-AC7B-BA82A04F3AD7}",
						"dateTime": "2020-04-13T13:02:36.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 165.89999389648438
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.70001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{905E66B8-8929-7E4F-9364-A907AA71D576}",
						"dateTime": "2020-03-09T02:59:16.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.79998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{9109001E-D463-D445-ABB1-13A0F79B4A40}",
						"dateTime": "2020-03-12T09:16:21.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{91E807D6-B96E-0A43-BCE0-70718C252046}",
						"dateTime": "2020-03-29T13:07:18.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{9210639D-79F1-8C40-82DB-358487053430}",
						"dateTime": "2020-03-13T01:00:42.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{9275DDF4-143C-2048-BA30-A3D2F0707626}",
						"dateTime": "2020-03-27T20:54:50.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{9313322B-8C5B-8144-B744-EA49455B7CCF}",
						"dateTime": "2020-04-03T01:02:55.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{94EF1A57-8F4F-BB46-9132-54447C7A15E0}",
						"dateTime": "2020-04-04T21:55:58.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 158.10000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{98F777F0-C214-2D48-817F-881B11B427AA}",
						"dateTime": "2020-04-25T12:22:18.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.70001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{99AAADE1-593B-754B-B650-5FAC980347AB}",
						"dateTime": "2020-04-08T04:48:16.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{99CE5EB3-0810-D343-8EF5-722B02A201D7}",
						"dateTime": "2020-03-08T18:11:08.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{9A63C589-2745-874F-AAE6-11C2D3A601C8}",
						"dateTime": "2020-04-12T20:54:49.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 130.39999389648438
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{9AC4CCD2-DEBB-9741-8D65-670C108A2DCB}",
						"dateTime": "2020-04-04T13:16:19.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{9D13422B-01D4-F943-B552-BA5283AFB6AF}",
						"dateTime": "2020-03-31T01:29:00.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{9E08027A-743C-A347-BA42-AEEC2AA616BF}",
						"dateTime": "2020-04-19T13:17:41.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{9EBF4D67-99E8-9744-8C55-071BA8EEB8BA}",
						"dateTime": "2020-03-18T06:25:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{9F9EFAD3-9415-FE49-87D7-F7CD82E7FAD9}",
						"dateTime": "2020-04-07T21:04:03.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.9000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 167.60000610351563
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A0CD0E33-C939-C247-9A85-9170BE9DD1D5}",
						"dateTime": "2020-04-22T21:09:58.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.0999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A377E821-2F39-9046-8D73-BFFAE5CEBE8C}",
						"dateTime": "2020-04-10T09:53:43.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{A42AD66B-8367-4C40-A4E0-108B2956D39C}",
						"dateTime": "2020-04-14T01:49:32.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{A46376E8-D0D1-854A-B2C8-2BB3D9D6B48C}",
						"dateTime": "2020-03-25T13:43:44.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 170.6999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{A5940859-E6D9-9E41-B29C-C9E4BF2B671B}",
						"dateTime": "2020-04-11T14:31:23.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A5F0E949-FD0E-614B-8A49-FE130412B7B9}",
						"dateTime": "2020-03-16T13:34:24.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 164.1999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.699981689453128
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A66ED1C3-4515-0041-986B-FC6188BA2D80}",
						"dateTime": "2020-03-18T21:42:09.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 138.10000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.0999755859375
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{A71B581E-144E-014A-BF8A-34A23A2B9567}",
						"dateTime": "2020-03-17T12:21:17.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 168.6999969482422
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A7A5E686-A453-7441-A49B-E88FBA423842}",
						"dateTime": "2020-04-23T14:40:01.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 136.10000610351563
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A7D0A394-37FD-A645-B961-65C8AE089AE3}",
						"dateTime": "2020-04-13T01:07:55.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{A8CA1675-620B-DB4C-91F2-15EA27AB11D9}",
						"dateTime": "2020-03-06T21:16:49.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{A989AFCA-407A-7646-BFDC-00CD17D28076}",
						"dateTime": "2020-03-26T14:04:47.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{AA0D92F2-82D1-0E4A-8770-D8ED03762DF3}",
						"dateTime": "2020-03-20T21:04:41.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 131.89999389648438
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{AD06479C-CA56-F641-AC80-F7A727DB8A33}",
						"dateTime": "2020-03-23T09:21:35.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -5.099999904632568
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{AD0BB830-7B01-454F-A6E7-25520043CEE0}",
						"dateTime": "2020-04-22T14:11:48.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{ADDA734B-DD31-124F-856C-9EEB4626180A}",
						"dateTime": "2020-04-14T17:50:10.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{AE2CA04B-BD63-1944-BF3D-BC163F45B11F}",
						"dateTime": "2020-04-02T01:00:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.800000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{AE5B6022-6C7B-294D-A121-DB80D517E381}",
						"dateTime": "2020-04-04T05:32:40.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							}
						],
						"value": [
							51.2000007629395
						]
					},
					{
						"id": "{AF7F18E3-9C5D-654A-8A07-04D9D74EBD1B}",
						"dateTime": "2020-03-14T01:04:13.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 127.0999984741211
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{B0618A7E-02EF-7041-B5EB-D47ECCBBAE20}",
						"dateTime": "2020-04-19T13:57:34.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{B194295E-509D-1042-8093-EC83F46C50B6}",
						"dateTime": "2020-04-07T06:39:46.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{B1C64A0E-4B96-E345-8DCF-E373388E213C}",
						"dateTime": "2020-04-20T14:31:05.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{B39E0B56-9EB1-1340-AED3-C1BB32DDD937}",
						"dateTime": "2020-03-06T05:17:46.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.100006103515628
							}
						],
						"value": [
							52.5
						]
					},
					{
						"id": "{B3B67528-7921-AE4E-9240-F4672D1E1C72}",
						"dateTime": "2020-03-15T01:06:32.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							}
						],
						"value": [
							51.5
						]
					},
					{
						"id": "{B4E658FB-1A74-7A47-A524-131FD6180E83}",
						"dateTime": "2020-03-12T13:54:30.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{B5478086-EF3C-7E45-8974-AFB3E95720A5}",
						"dateTime": "2020-03-31T10:19:05.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{B562B338-90A9-244B-A559-22FC5BEDA23A}",
						"dateTime": "2020-04-10T05:56:04.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{B64D27C7-BF5E-434F-9634-60BB649B1D24}",
						"dateTime": "2020-04-04T18:02:44.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 168.3000030517578
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{B6D5684F-465F-2444-8BC4-3BFDC327E59B}",
						"dateTime": "2020-04-08T13:22:25.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{B710371C-1E2B-AB4C-A91E-13D53A036CCD}",
						"dateTime": "2020-03-14T05:12:17.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{B7386599-C430-6543-AEF7-FFA7A7319613}",
						"dateTime": "2020-04-10T22:09:38.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{B74C4A4E-0F61-F344-91A4-962DB2220EAA}",
						"dateTime": "2020-03-17T17:14:22.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 167.39999389648438
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{B94F4C2F-7DC3-6844-B284-61482E611411}",
						"dateTime": "2020-04-05T17:24:29.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 169.6999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{BA0DB79F-F186-A945-A733-E8CD51655A44}",
						"dateTime": "2020-04-07T09:39:12.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{BA64F419-593A-1846-91E1-1126138695C6}",
						"dateTime": "2020-04-17T01:25:23.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.20001220703125
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{BB2899E5-C1D5-094E-B06B-A3BAFD04F042}",
						"dateTime": "2020-03-27T06:07:19.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.800000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{BB8DC36D-6DD3-E241-9406-6AEDD37FC650}",
						"dateTime": "2020-03-29T05:01:19.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.800000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{BCCFEB19-7F00-724F-80CE-3A7DE2D227E4}",
						"dateTime": "2020-04-12T01:01:03.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.9000244140625
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{BDCF1A90-E37B-2041-ADEF-1BF0A3E365EA}",
						"dateTime": "2020-03-30T05:09:52.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{BEB199BD-0373-5349-8459-D87556578AAB}",
						"dateTime": "2020-04-23T14:36:21.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 132.10000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{BEC3ADFC-CA67-4C4A-AB74-5D500B07C8FC}",
						"dateTime": "2020-04-17T09:48:03.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{BF699104-AF62-F544-9715-0523E24F8D9E}",
						"dateTime": "2020-04-13T10:40:22.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.9000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 131.39999389648438
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{BFAFD9DD-FB8E-084F-ABE4-A9DA0E74E32A}",
						"dateTime": "2020-03-11T04:49:07.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{C0E07F68-4BC3-834C-81FE-08C14C878807}",
						"dateTime": "2020-04-05T21:34:41.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.0999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 139.60000610351563
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{C12EC2CA-1393-C848-8A6D-5651CA29DA03}",
						"dateTime": "2020-03-07T18:10:23.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{C174EA56-E8A8-F249-862E-D3AB1A2ADD8D}",
						"dateTime": "2020-03-21T01:27:57.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{C2C11E89-582A-EE49-A4E1-B64805C616B5}",
						"dateTime": "2020-04-19T06:19:07.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{C352D098-70B8-CE4A-90E3-B952E19F1C36}",
						"dateTime": "2020-04-01T21:33:48.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{C424CFD5-0EE7-6C42-B846-518FC60AF7DE}",
						"dateTime": "2020-03-21T21:00:39.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 130.1999969482422
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{C4FF06AB-C599-A945-A189-25C5841A6721}",
						"dateTime": "2020-04-05T05:23:30.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.199981689453128
							}
						],
						"value": [
							51.2000007629395
						]
					},
					{
						"id": "{C6A43C4D-6B8B-B644-8745-73A4ADE3CF73}",
						"dateTime": "2020-04-05T08:55:56.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.900000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.0999755859375
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{C87246AB-A2C9-C444-B8AD-D3E4F3BDAB5D}",
						"dateTime": "2020-04-20T05:33:57.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{C8A1F066-2FEC-694D-A888-46FA3C10250C}",
						"dateTime": "2020-04-17T13:05:34.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{C90FBEFB-F258-6C48-AE26-33AB5CF720D5}",
						"dateTime": "2020-03-09T21:43:36.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 166.1999969482422
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{CBA11E1B-DB4F-914C-A1D6-CFECFD178221}",
						"dateTime": "2020-03-02T17:22:08.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 134
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{CBBBB8FA-AE18-734D-86CF-CCAAF4C1DCE0}",
						"dateTime": "2020-04-02T15:07:27.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 131.89999389648438
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{CBF05C98-ABD1-624C-8EB5-98207A65217A}",
						"dateTime": "2020-03-21T14:04:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							}
						],
						"value": [
							51.2999992370605
						]
					},
					{
						"id": "{CC07E4A2-85B0-334F-A01F-7BE9E60646E2}",
						"dateTime": "2020-03-10T13:00:20.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 131.60000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							51.5
						]
					},
					{
						"id": "{CC8B0C2F-F378-9A44-9750-D619F874AAA6}",
						"dateTime": "2020-03-07T21:46:16.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{CD073DFB-2C2B-1249-9D34-CEB0F88AF6E1}",
						"dateTime": "2020-03-21T10:20:05.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							}
						],
						"value": [
							51.4000015258789
						]
					},
					{
						"id": "{CDAF41EE-E453-4642-A9E5-59072C142C02}",
						"dateTime": "2020-04-17T09:51:14.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{CE3E63B8-C4E1-C04D-901E-D503C28AF674}",
						"dateTime": "2020-03-03T17:40:49.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 168.3000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{CF2876DA-E73E-9447-98AF-C27AE5539F2F}",
						"dateTime": "2020-03-13T05:06:24.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{CFD52628-9A7D-BD48-A157-E3F061B2B7CE}",
						"dateTime": "2020-04-20T17:02:43.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{D0A9E8DE-3F6B-BF4E-9047-4E8E256E8EB5}",
						"dateTime": "2020-03-14T21:58:20.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{D1858A17-6691-D443-9075-6D706AF4FAB9}",
						"dateTime": "2020-04-20T14:30:25.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{D2F6E3B6-4510-6946-9DF9-06DBC5204B8B}",
						"dateTime": "2020-04-15T05:38:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{D3237BB3-2976-AB43-994A-20AA726E370E}",
						"dateTime": "2020-03-31T17:20:44.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{D41B4E32-5BD5-7C45-8A6C-5E4F105721DC}",
						"dateTime": "2020-03-26T06:33:56.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{D851FA15-3496-DC4B-ABEC-03EFBB355A63}",
						"dateTime": "2020-04-18T14:12:38.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{D99458C2-D05F-1147-BDBF-CE91D47C2D46}",
						"dateTime": "2020-03-13T17:07:15.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 150.3000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							}
						],
						"value": [
							51.7999992370605
						]
					},
					{
						"id": "{DA06479F-2640-5A4C-9F88-DF3C93735C2A}",
						"dateTime": "2020-04-14T05:31:29.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.800000190734863
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{DB587173-9570-4645-9316-CB4D1D73B8C5}",
						"dateTime": "2020-03-20T13:15:55.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							51.2000007629395
						]
					},
					{
						"id": "{DBF2906B-B243-EE44-9274-6BA021917851}",
						"dateTime": "2020-03-03T14:27:02.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 170.1999969482422
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{DC90B0E4-563D-7441-A133-D8C09A7CE103}",
						"dateTime": "2020-04-20T01:17:11.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{DD343D7F-8F70-374D-9614-AE1533FE6B9E}",
						"dateTime": "2020-03-29T09:07:18.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{DE7F7739-BEA7-4B49-920B-EDC10AE0A527}",
						"dateTime": "2020-03-09T13:08:36.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 132.39999389648438
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{DFEF2B9E-BE91-534F-A28F-44ECAB05B09C}",
						"dateTime": "2020-04-24T22:28:54.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 158.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{E2411EA5-FEC2-9148-B867-975BE8920C89}",
						"dateTime": "2020-03-06T13:39:49.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 169.89999389648438
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{E3753785-F749-5E4C-A2DB-A8E192DA833F}",
						"dateTime": "2020-03-02T21:38:08.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 133.1999969482422
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{E3A6DBC5-0B02-154C-A7DD-0167EF050FCA}",
						"dateTime": "2020-04-24T06:04:09.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{E4049AE9-A43D-6842-8674-A83FFC095551}",
						"dateTime": "2020-04-20T21:03:08.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.100006103515628
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{E614C4A5-61F3-2F4D-A7FA-31917BB409E7}",
						"dateTime": "2020-04-22T01:04:04.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{E65217E2-DDA4-E74A-A529-E6E74D0D9811}",
						"dateTime": "2020-04-05T13:03:56.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{E7130314-A421-3046-9C66-6446E5EA8797}",
						"dateTime": "2020-03-08T09:30:29.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.70001220703125
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{E71AEE3E-DFBB-9540-BD6F-7790127428BB}",
						"dateTime": "2020-03-29T20:39:32.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{E84465FE-62CD-0149-A3B7-A9E525BBAF9D}",
						"dateTime": "2020-03-16T02:02:23.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							}
						],
						"value": [
							51.5999984741211
						]
					},
					{
						"id": "{E93DEF71-45F3-704E-857D-A09C2800FBF6}",
						"dateTime": "2020-04-13T22:00:43.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 166.89999389648438
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{EA5F3E93-64EA-7A4A-8E4E-533CCF43BCC7}",
						"dateTime": "2020-03-22T05:10:43.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{EAF59D9D-827D-E445-BE45-83F9D6DBD932}",
						"dateTime": "2020-04-24T09:25:33.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{EBEB3076-89A3-A740-B2AA-CEF98F593773}",
						"dateTime": "2020-03-16T17:11:12.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 152.8000030517578
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{EC02E13F-CBF0-AD44-B29D-54CD67100DD9}",
						"dateTime": "2020-04-15T13:22:15.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{ECA403F2-B590-3248-A13D-2C6071D24221}",
						"dateTime": "2020-03-14T09:19:33.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.799999952316284
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{EEDA4C94-B978-7048-A54E-FFE767C9B4DC}",
						"dateTime": "2020-04-13T17:25:39.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 167.3000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.800018310546878
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{EF6C10C4-2790-944D-9338-FC0F8E748C23}",
						"dateTime": "2020-03-02T06:30:25.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 159.6999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{EF8F4105-332A-D742-A76B-499017C21C94}",
						"dateTime": "2020-04-03T13:01:57.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{F128D236-94C9-B541-951B-2C472A8B500F}",
						"dateTime": "2020-03-19T17:37:04.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 126.0999984741211
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{F1E263D6-57ED-CA49-A673-2E2FB6A5BD79}",
						"dateTime": "2020-04-10T21:30:17.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5999755859375
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{F2D6C059-0A0F-BF41-8A3E-AB1213E0E61B}",
						"dateTime": "2020-04-07T06:07:45.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{F301BE84-62F9-CE43-A930-13A6DE1B1D84}",
						"dateTime": "2020-03-22T18:11:11.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F33C8194-CE62-444C-8FC7-90FA5421568C}",
						"dateTime": "2020-03-04T22:43:38.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F38B4DF4-EA3F-7741-81C7-EE59205FBB21}",
						"dateTime": "2020-04-22T13:39:19.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F458935C-AF0D-B14C-B98B-E0EEC61687CC}",
						"dateTime": "2020-04-10T00:50:29.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 132.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{F4755DE6-740A-414F-B52E-DBDF26FB64D8}",
						"dateTime": "2020-04-07T17:45:41.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{F49E3976-CEDE-414D-9A78-D9C577816D9D}",
						"dateTime": "2020-03-22T01:21:09.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							}
						],
						"value": [
							52
						]
					},
					{
						"id": "{F62091CD-A2D6-7C4C-AF71-D1C0DCAA2B24}",
						"dateTime": "2020-03-22T21:19:17.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.0999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.800000190734863
							}
						],
						"value": [
							50.9000015258789
						]
					},
					{
						"id": "{F8422E8C-B051-C042-B84D-DA74E7161D5D}",
						"dateTime": "2020-03-20T13:15:55.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							51.2000007629395
						]
					},
					{
						"id": "{F96ED741-5419-0146-B1C5-F86D07BCA4F7}",
						"dateTime": "2020-03-23T17:14:27.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.900000095367432
							}
						],
						"value": [
							51.2000007629395
						]
					},
					{
						"id": "{FA3CDCF7-E403-AB4F-92D1-D18E89D3BB5A}",
						"dateTime": "2020-04-02T21:21:29.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 166.5
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{FA592BE2-431D-4547-9DAB-124EA1696698}",
						"dateTime": "2020-04-01T17:30:34.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{FB3E2388-76D6-F84B-B5E7-AC95A0F50E1D}",
						"dateTime": "2020-03-15T17:42:58.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{FB68278C-B266-1143-8FA3-FCF505F7481C}",
						"dateTime": "2020-03-13T21:20:11.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 130.1999969482422
							}
						],
						"value": [
							51.9000015258789
						]
					},
					{
						"id": "{FC47363F-2572-8047-9996-F970839F4B80}",
						"dateTime": "2020-03-06T01:50:20.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							52.5
						]
					},
					{
						"id": "{FC834FD9-2229-574D-BCFD-FC1CBE7ECFB5}",
						"dateTime": "2020-03-17T14:00:56.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 129.3000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{FEA42A8E-64E8-6442-B109-517E619BAA54}",
						"dateTime": "2020-03-26T21:40:45.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{FED7ABA6-A5DE-C74D-A6F4-BE9652F12841}",
						"dateTime": "2020-03-30T13:31:07.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 168.89999389648438
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{FFBAB23B-A548-5A44-B441-92557EB9A6A0}",
						"dateTime": "2020-03-25T19:22:00.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.5999999046325685
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							51
						]
					},
					{
						"id": "{0046C7F2-100D-604A-B36D-B556F550C400}",
						"dateTime": "2020-08-05T22:42:12.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{00C4C9CE-7DAB-1E41-9FB9-AFD8F93E3AA4}",
						"dateTime": "2020-07-01T21:39:43.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 167
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{010864B2-F852-DE47-8ABD-4BF72902C88A}",
						"dateTime": "2020-06-30T01:27:08.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{01AD0125-9AD0-0745-9238-45E64F770F37}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{024B89E5-FF9E-114A-8825-DBBDA16756D1}",
						"dateTime": "2020-08-07T21:00:28.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.5999999046325685
							}
						],
						"value": [
							46
						]
					},
					{
						"id": "{02D3D26D-98F3-1B4B-9497-69B4B6C2D7DD}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{03DA2107-891C-0244-A0D8-D73B4BA27009}",
						"dateTime": "2020-07-13T22:36:16.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{046FFEB4-5423-CF44-8069-72B1F4C18C5D}",
						"dateTime": "2020-08-09T18:32:04.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 151
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{05062DB0-C794-4D48-93AF-82D44F74E9B0}",
						"dateTime": "2020-07-05T20:18:02.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{05696CCE-11B1-864F-8257-5E5CB81E1D7A}",
						"dateTime": "2020-07-08T21:08:19.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 162.8000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{0718EBE8-68DA-A540-A4DF-EA1D1BB705D8}",
						"dateTime": "2020-06-28T21:07:54.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.700000047683716
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{080E346A-8752-F249-B1CF-E8FFEC474ECC}",
						"dateTime": "2020-08-04T05:47:49.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{0863680F-D38D-F445-B897-4079004EA602}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{09117D1A-9CD5-E343-ABE3-EA5EE9765D4D}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{09B26C84-F0AE-1646-BB9B-486B71B978CF}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{09D7B3D6-F9CA-1A40-9256-A5582FC73032}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{09DAFADB-58A9-C643-9252-8845B969E74E}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{0A324914-A035-C24E-99B3-3DBB10147AAE}",
						"dateTime": "2020-06-30T14:50:32.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{0BE5D5BA-246F-9C4D-A77F-574FA099CBBE}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{0C3221B0-1E82-F04A-9F96-7FC07D61CD65}",
						"dateTime": "2020-07-11T16:43:16.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{0C394A4B-7A92-9547-8C2C-99C0E7543933}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{0D4CFFBC-83A0-B543-95C1-8A68496A9392}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{0D6DA229-7450-6C42-A2DF-7B636195C989}",
						"dateTime": "2020-08-07T05:56:52.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.4000244140625
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{0F2F0941-2B13-E942-A683-E32B39A6E8EE}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{0F617AE7-B1FE-274E-8EC8-38C6425E61ED}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{108DD38C-BB23-0A45-B889-0FE3E137F767}",
						"dateTime": "2020-07-08T21:08:19.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 129
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{10A4E442-1CB6-CB41-AC0F-414E7C6A6671}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{10B947DB-11C7-BD49-A4EA-BF331C0E8C70}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{10C37697-33CD-6249-AB2F-5393F2FED73C}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{114EE977-6903-1948-85B5-AF7BDA7ADD19}",
						"dateTime": "2020-07-19T13:21:44.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{11559D41-822A-7340-9692-CB9DF351E4BD}",
						"dateTime": "2020-08-11T21:30:40.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{11D7BD67-D9EA-BB45-ADED-DD35B4770357}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{12D2AC14-C9DC-0F48-841F-D35B2A39E667}",
						"dateTime": "2020-07-16T13:29:56.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{13986065-AA38-A945-B6D0-FC811BF34C21}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{15098642-0616-7042-8431-D46222EC926C}",
						"dateTime": "2020-07-18T13:07:45.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							44
						]
					},
					{
						"id": "{15EDAD30-3A8E-704D-ACD0-27AB8143C2FC}",
						"dateTime": "2020-06-29T06:32:56.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{16B0FD6B-FBBB-1849-8407-0BF2D41779A7}",
						"dateTime": "2020-08-12T10:52:59.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 169.10000610351563
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{18D6BF2F-D484-0749-867A-6B8396003D48}",
						"dateTime": "2020-07-02T01:05:44.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{19190BC9-C61A-7E4A-BA6D-0419240FC8C8}",
						"dateTime": "2020-07-25T21:59:37.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.9000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1966A692-CD3E-2345-9082-68426A79A5A2}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{19F3FDA2-A2BB-9547-B0DB-5F647DFFB8A7}",
						"dateTime": "2020-07-27T13:32:02.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1A3FA760-F440-4246-96B1-15E022FE4C15}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{1A891EDC-CA5B-0549-A3CC-8ABDEAC467B0}",
						"dateTime": "2020-07-20T14:02:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1ABAE82E-B314-E64D-8179-C923BBDDBED0}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{1B960EE8-72C7-F545-BD1C-AE71078CF8C9}",
						"dateTime": "2020-07-02T04:59:40.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1BB3A392-F51A-4543-BDC4-DF4FC0C10DEE}",
						"dateTime": "2020-07-31T05:30:55.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{1C08237D-B57E-8745-9B78-676409FFB47B}",
						"dateTime": "2020-07-07T21:16:01.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							49.2999992370605
						]
					},
					{
						"id": "{1C20B5FF-5F41-4F43-90B6-287243E66C89}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{1CAE8FAC-3D32-1740-A344-E766A3BA6DE5}",
						"dateTime": "2020-10-09T14:11:45.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							3655
						]
					},
					{
						"id": "{1CB1560D-44F8-F942-A936-5829BC20C3F4}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{1DBEC6B1-5294-2E41-AAE6-83348D7F2939}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{1DE9E323-B168-8344-95A8-6067B6FAAA7B}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{1E68FCBF-6F46-1545-A312-3E3098338FCB}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{1EE9FBF5-6E3B-F34C-8B38-BCCD675D3F60}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{1F9BB289-0D39-FA42-B923-7996DA0430BC}",
						"dateTime": "2020-06-27T21:40:43.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{1FB925A3-B19A-094A-8582-F14F75D8DEA7}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{20528B83-1130-F14C-81B6-3D7E72C93DC0}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{210F0A34-7FD7-DF42-B040-2EA62D219725}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{21406541-CF3E-5F48-B1AD-EC2EB418BD3C}",
						"dateTime": "2020-06-28T06:42:37.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{217086FF-8AF0-2740-986B-2210E7858BCE}",
						"dateTime": "2020-07-09T01:05:19.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							49.7999992370605
						]
					},
					{
						"id": "{22A13D3E-0AF9-9344-8929-A22128EF8BA3}",
						"dateTime": "2020-06-28T09:36:11.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{256818D6-D7E0-3246-AAF1-52D691B7D242}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{2613063E-0EB2-D94D-AF4E-A13847C18F9B}",
						"dateTime": "2020-08-08T06:38:33.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{26AE54D2-4615-1E4F-931B-7666030CB394}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{26F8746F-725A-834B-883E-7994AF5F823C}",
						"dateTime": "2020-07-31T22:27:47.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.9000244140625
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{286013A2-FB3E-1C4D-9AEB-484073E04037}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{28BD22D5-FC00-194D-8EFA-069B878397BB}",
						"dateTime": "2020-08-13T06:14:25.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{28C520F5-4BF3-8149-BBAC-0A99750FB9FC}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{28CBEB9C-21FB-304E-AD36-3FBC7322DFDE}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{299C0F63-D734-B944-A13D-3B7A419EA3C5}",
						"dateTime": "2020-07-21T22:23:54.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2BCEC8AF-46E4-304A-B142-DCBDC713C8CF}",
						"dateTime": "2020-08-05T05:54:49.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2BE52909-60E5-DA4D-9971-86B01AEC08E7}",
						"dateTime": "2020-07-24T14:36:33.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.4000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 162.3000030517578
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2DB0FFDC-543B-0F4C-A2D8-7A075CB7D66C}",
						"dateTime": "2020-08-01T22:36:26.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{2E113723-88F9-ED49-B0A2-B3235BBDDC4D}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{2FF3377F-5B2F-8849-B940-A75FCEA026F3}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{3054B2FA-79D8-1C4A-8C71-069BA78EDAE2}",
						"dateTime": "2020-07-17T05:53:57.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{308A7042-7202-6C4C-8632-F8BBB6392BDF}",
						"dateTime": "2020-07-16T17:10:17.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 143.8000030517578
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{3149AB56-3148-9C4B-8405-E2AB46451E4E}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{32AFD30D-4A37-CD47-80A1-B7D25D6DFFB8}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{32F8DF22-F5E9-604C-87AF-3FC2E172374D}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{33D4778F-E3BB-784A-AEB0-CE38E3D7A0D7}",
						"dateTime": "2020-07-22T14:30:08.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{363134CE-D84F-E54B-821E-3E4E52C16CA7}",
						"dateTime": "2020-07-28T05:41:36.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.100006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{378E05D7-3AC5-2941-BD9D-2D4404242C0E}",
						"dateTime": "2020-08-01T03:19:08.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.4000244140625
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{38DE0141-7352-214A-AFEF-8F0940A402EE}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{3A19152B-8896-2E4C-B5FE-6FD8A40D35D9}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{3A3F0652-CF3A-FD4B-B3E3-96DE8A37F3CB}",
						"dateTime": "2020-06-30T21:55:30.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3A935E10-6B1E-594E-9D13-05B0DC387000}",
						"dateTime": "2020-10-08T22:47:12.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							25
						]
					},
					{
						"id": "{3B06AA64-680D-D94E-91F2-1B8EF462560B}",
						"dateTime": "2020-06-28T14:19:52.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3B32BB6F-A58D-7748-AED6-2CC2C9580558}",
						"dateTime": "2020-06-29T17:30:16.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 131.8000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3B7E7E2B-D409-B343-A16F-51341AF9157F}",
						"dateTime": "2020-07-13T22:37:01.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3BA9FAB1-77EF-E84B-9C4D-5E0A67D84D6E}",
						"dateTime": "2020-07-14T13:07:46.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							}
						],
						"value": [
							49.2000007629395
						]
					},
					{
						"id": "{3BC177D1-076B-3948-BF9E-A1AD45516C5F}",
						"dateTime": "2020-06-30T14:49:34.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3D7C64FE-E60D-2F46-944D-2878E4067F19}",
						"dateTime": "2020-07-23T05:15:42.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3E0860AF-3A88-194F-9622-CEF81B6C3705}",
						"dateTime": "2020-07-19T05:20:59.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							49.5
						]
					},
					{
						"id": "{3F8EE3FD-B64D-0C44-B114-547A2EF4309B}",
						"dateTime": "2020-08-02T22:05:01.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{3FA2D006-991D-5B41-8A21-A3D4647C0D52}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{3FB8FD36-81DD-A745-B718-494616E4E7A9}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{3FD5AE92-66D8-6B4C-A3C9-7C515F88133A}",
						"dateTime": "2020-07-21T13:21:41.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 160.10000610351563
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{421F0C63-BB84-4E43-8307-936AB90052CD}",
						"dateTime": "2020-07-17T17:29:36.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							}
						],
						"value": [
							49.5
						]
					},
					{
						"id": "{42A9810D-EB8D-4147-9F47-61FD4750BA55}",
						"dateTime": "2020-08-05T21:21:34.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.4000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{4370BE1A-F01B-F441-9B79-1FD962207557}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{43726466-0AE3-7041-9342-9267AD97EB87}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{443F57E9-A069-FA43-9994-8B97BD46FCF7}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{45A475D6-3942-3940-AF05-964B06A95EF9}",
						"dateTime": "2020-07-26T17:10:10.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							49.5999984741211
						]
					},
					{
						"id": "{470D9363-BF95-3248-AB6C-984E7D3057B8}",
						"dateTime": "2020-07-15T01:45:50.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.4000244140625
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{47A631F0-D997-8244-AA90-ED32EE4B5123}",
						"dateTime": "2020-08-12T05:45:36.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 139.5
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{484EC4DB-680E-C044-8213-60E3237F51C5}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{492A4D82-38B1-5948-B2FC-8CF1C6140196}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{4935A399-36FF-0446-AE15-FEC615650F0A}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{49CAEA3F-AA32-BC49-856B-C3C0AD7B69D7}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{4C444E8C-9AA7-C843-9FEF-7E56019AC98E}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{4E96557C-E3FA-9744-9ED1-D3307FB3D790}",
						"dateTime": "2020-07-19T01:07:56.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							}
						],
						"value": [
							49.5999984741211
						]
					},
					{
						"id": "{4ED71384-C663-D54A-84B2-098E39EADD6E}",
						"dateTime": "2020-07-24T14:03:25.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 161.8000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{4F199DF6-F0B2-F246-B4B1-EB91D5E4F314}",
						"dateTime": "2020-07-22T06:08:43.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.600006103515628
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{503C6C4A-C392-034E-AA70-956ED5DC327D}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{50C2C694-BBD8-5545-BA24-6F17AAFECE6D}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{50CE124A-7192-9246-B96C-95E56F007870}",
						"dateTime": "2020-07-26T21:32:41.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							49.5
						]
					},
					{
						"id": "{52ED0D1E-6D13-374F-986F-11785E5BD0DE}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{534C7102-D246-FA4B-A58D-EFA5FECC12C3}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{53F22B29-D221-F54D-BB68-50ADA3462466}",
						"dateTime": "2020-07-14T02:56:53.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{546FEF3F-13B8-1E4C-9C60-A43714A1F7DD}",
						"dateTime": "2020-07-02T14:20:24.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.699981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{55835168-A153-3944-97FB-F7DFA2078C4B}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{55BB3658-28A0-8045-B5BF-B3BE4E8A8B14}",
						"dateTime": "2020-07-07T05:03:49.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.100006103515628
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{56881AD1-5703-1641-B614-1EB182B31521}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{56A94B89-6D0B-194D-8760-596B729F4167}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{56E91492-C26B-7F44-BBEB-B092F7106FB4}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{578F273F-FF56-E541-8942-1E5EEA68214A}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{57A4BF4A-501A-944D-8A00-7204F547DD3C}",
						"dateTime": "2020-07-06T13:02:55.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{581C1C1B-ABA3-874E-80AC-8EE03F1B26D8}",
						"dateTime": "2020-07-28T14:36:19.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.4000244140625
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{5941E683-CCAC-BB4C-809A-05D1F15D5454}",
						"dateTime": "2020-07-04T14:40:40.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{5A8C4981-1904-2F46-A7F0-5745DD0EEBF2}",
						"dateTime": "2020-07-15T20:14:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{5B740424-D9E8-704F-9A08-8615CFC373B1}",
						"dateTime": "2020-07-15T05:40:52.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{5C0236AF-049E-3746-A054-2D7BC7C44EED}",
						"dateTime": "2020-07-04T22:07:54.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{5C5F8585-3C40-8E4E-A330-F0C2F0208629}",
						"dateTime": "2020-07-16T01:44:46.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{5C8BD146-EE98-C843-B169-49DF936E8610}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{5CCA5D3F-55C9-3A42-A89F-47D3D099F9D8}",
						"dateTime": "2020-08-10T20:51:14.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{5CF689A9-2C72-B442-8B40-598629FEBA3F}",
						"dateTime": "2020-07-09T01:05:19.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							}
						],
						"value": [
							49.7999992370605
						]
					},
					{
						"id": "{5D0B4A7C-5A59-2F47-9369-5270561F8FE8}",
						"dateTime": "2020-07-19T21:03:14.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{5DE400BB-E6CA-1F4B-BF5D-74D9B2E89067}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{5ED39078-94B3-9E4F-8764-18556A229687}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{5F719E0A-8FC5-7241-AEF3-A3A071463BA1}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{61815F3B-361F-D749-9577-89DA48976B49}",
						"dateTime": "2020-08-10T13:17:47.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{629FB6AA-0F35-3B4E-AA3E-AA29E100D4D4}",
						"dateTime": "2020-08-10T01:51:25.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{63880558-2234-054E-9DC0-73A9399AEF2A}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{64672BD7-1856-5142-AF03-28AB2E2428BE}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{64C44CDC-7860-F24B-8241-46EAC6A8A7B0}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{650748FB-A652-C548-92A4-46E9FBD6EF4A}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{658F64F2-50DD-8141-8850-A5606E647C50}",
						"dateTime": "2020-08-13T06:13:52.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{6663A3FD-F75A-EF4E-8F5E-05E27D037526}",
						"dateTime": "2020-07-26T05:23:18.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.4000244140625
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{672A4241-327F-4D4E-BBDC-C7606ABB195E}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{674878D2-321E-8F49-85BD-5663D515C86F}",
						"dateTime": "2020-07-10T05:59:52.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							}
						],
						"value": [
							49.0999984741211
						]
					},
					{
						"id": "{67B542E8-A1C5-8641-BF20-4A558EE87DCA}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{6816E0D8-0CD0-DF46-8040-74FEB7523BDB}",
						"dateTime": "2020-07-21T05:43:59.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{68A75717-A091-A040-82A5-B8860D2B4610}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{698D8E25-E7CF-214B-BA59-2A5D4EA5FBFF}",
						"dateTime": "2020-08-13T14:18:03.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 1
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{69C52224-9CF5-A941-9B8F-32D6F5FB3227}",
						"dateTime": "2020-07-16T21:18:46.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 151.10000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{6B142AAA-8216-AF49-A1C4-EECA1E77E381}",
						"dateTime": "2020-07-10T13:36:42.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							48
						]
					},
					{
						"id": "{6E10A0AA-E75E-134B-93FB-51E01D5F11EE}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{6E63B876-1987-3F4F-B3A8-0C4450DA5761}",
						"dateTime": "2020-08-06T22:41:19.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{70457A34-7D62-2B49-96E2-C73FC8F1597E}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{714C0DF2-C99F-6341-BBF3-7B52790EA774}",
						"dateTime": "2020-07-29T14:08:19.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{72C56ADD-AD76-F546-B267-8302876CC447}",
						"dateTime": "2020-07-10T22:09:48.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{72D790EB-0D6F-C74C-B41F-2BC9DCA22A00}",
						"dateTime": "2020-08-12T22:07:12.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 159.10000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{743FB0D2-8086-444C-AEB1-B2FD23F2DCE8}",
						"dateTime": "2020-08-12T22:08:30.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 154
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{75068A3A-50C2-9C45-829D-0F4809A43B1B}",
						"dateTime": "2020-07-25T12:11:05.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{7586E404-582C-DA43-9F36-A98F008107DC}",
						"dateTime": "2020-07-23T06:37:17.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{766F54CF-411F-B54A-83C9-9FF1642AA1E4}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{782844BB-366D-774A-AB4E-AFC989DD59F4}",
						"dateTime": "2020-06-30T21:52:03.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{791E55C3-7F65-1B45-A81A-72B49CA20CFE}",
						"dateTime": "2020-07-04T06:08:34.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.199981689453128
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{792120AF-F62A-0042-8051-19C2C4448F69}",
						"dateTime": "2020-07-02T12:54:22.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{7986BF83-DC7C-0441-B2EC-81320D43FADD}",
						"dateTime": "2020-07-25T13:09:06.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							49.9000015258789
						]
					},
					{
						"id": "{7A04A381-2372-A546-9463-55DB3A00CC62}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{7A593A05-5F77-BB49-B026-FC550070EBB8}",
						"dateTime": "2020-07-06T06:08:09.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{7A9286FD-913C-884E-82F2-DEE8144B0F94}",
						"dateTime": "2020-07-06T21:18:06.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							49.2999992370605
						]
					},
					{
						"id": "{7AE4B20B-4074-8B42-BDE8-7D85C37B9300}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{7B75F71A-4FA2-0547-880A-78E82F7A0B92}",
						"dateTime": "2020-06-28T04:09:15.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{7BE57A3E-4BEE-EA45-8444-C546C790D803}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{7C10284C-B848-004F-8D0B-E2F6593274CF}",
						"dateTime": "2020-07-05T11:42:04.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.199981689453128
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{7C1A8F9B-B1F7-8D49-B8F1-2984E3E4512E}",
						"dateTime": "2020-07-17T13:07:04.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{7E9D636B-0F0C-9245-9FEF-65B3B42C5B73}",
						"dateTime": "2020-08-06T20:31:12.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{80C57BB6-0601-924C-8785-4DF252647B34}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{80D1BC23-F631-4D4A-B424-3D56353DED3B}",
						"dateTime": "2020-07-01T20:59:12.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 167.10000610351563
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{814A4497-ABF1-0445-A4FF-042130F9928F}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{814E2020-155B-F940-83F3-EAE203274CBC}",
						"dateTime": "2020-08-04T22:29:07.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5999755859375
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{81C6129B-EE31-9741-AEEA-28952D23D266}",
						"dateTime": "2020-07-11T05:09:25.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{81C8CA5A-D0CB-0A4F-810D-EAAFDAC82838}",
						"dateTime": "2020-06-27T13:09:29.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.0999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{8283B314-76BE-5948-9BF5-A4752587A0ED}",
						"dateTime": "2020-07-05T14:12:42.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.100006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							49.2999992370605
						]
					},
					{
						"id": "{82DD45D1-DE3A-DD4A-80D0-DD33BD6AAC69}",
						"dateTime": "2020-07-23T14:54:41.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{82E0C128-9D63-8B4C-A740-7AF5AE45F382}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{83C15FAA-C0F7-1B47-A07D-E6D3A64FAF10}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{85FC7CD2-DE5C-D24B-AF7F-259D318E1DEC}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{88175F97-C885-D440-9C0C-22139392EB65}",
						"dateTime": "2020-07-08T12:02:58.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 131.60000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{889DEAE8-9CE2-EE45-AFC0-639AEAA39BC6}",
						"dateTime": "2020-08-02T06:27:18.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{892A56DE-0141-7440-B99B-24EB74F6BAB0}",
						"dateTime": "2020-06-28T17:10:09.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{89ECA7BC-969F-264E-A362-D16E36330834}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{8A1B6BBF-CF3F-2D47-99B9-CF708811628D}",
						"dateTime": "2020-07-18T21:01:30.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.899993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{8A7CE7C4-0E5B-5E4D-B152-8F7ECFEF70B2}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{8CF40520-6C35-AC46-A6BC-F17BD9AFB492}",
						"dateTime": "2020-07-17T21:20:25.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 144.6999969482422
							}
						],
						"value": [
							49.0999984741211
						]
					},
					{
						"id": "{8D167E09-9F14-F547-92D2-026BE3DE9F89}",
						"dateTime": "2020-07-14T05:43:39.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{8D9C8BB1-43BF-BA48-9C97-2C5DC16546A9}",
						"dateTime": "2020-08-07T21:56:42.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.700000047683716
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{8E66A614-93CE-5443-A1CD-A0997C78A5D0}",
						"dateTime": "2020-08-08T06:32:36.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{8E761D43-F990-EC47-B435-EBC4D0BC1CC5}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{8EAE3CD3-5C84-7A40-A8A5-32EA20B6ED46}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{8F9BE47B-9D52-AD41-A113-FFB86308D962}",
						"dateTime": "2020-08-10T01:05:51.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{9228B0E9-3192-DB4D-8762-DA4FC4666AE6}",
						"dateTime": "2020-07-08T21:08:19.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 133.3000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{922ECB52-80C4-3541-AEA7-61A82D62C93B}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{92EAE15F-7B68-1C4C-BF60-2825FBDF0E97}",
						"dateTime": "2020-08-12T06:30:30.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 139.89999389648438
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{9347D22B-7097-5246-8A3F-C6DEEC6B3BD2}",
						"dateTime": "2020-08-01T19:58:12.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.9000244140625
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{93ACAB48-1C5A-CC4D-A544-C01598D9D488}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{94054142-3E14-1A46-914F-3B60E79F5D79}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{949B3D7B-BA3B-894F-BAF8-6602DED8D04F}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{954D1BD8-2EC1-FB4B-98AA-3DECFE9123DF}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{95B1CA65-30DD-5A45-8C10-5AD3223D045D}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{96719E80-6F6B-5940-A546-96F59477CB72}",
						"dateTime": "2020-08-10T13:17:47.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{96AC031B-67A0-1842-9528-EB04A4E1DD23}",
						"dateTime": "2020-07-09T17:15:05.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{96C26AAE-E0CB-1E4C-BF96-7AA838BC4BC0}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{97B3F55B-A870-504A-AFCB-C1AEB3C4BC65}",
						"dateTime": "2020-07-08T21:08:19.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 150.5
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{99255015-598C-AF47-9DF2-5333D242C2A2}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{99FD102F-292E-7F48-8411-7C80FD97C76B}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{9A769F85-6D8B-7441-9419-7567663B9F8A}",
						"dateTime": "2020-07-07T18:57:54.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{9BA3F28F-141C-EE41-B397-1A06765540AF}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{9BB259AE-4725-554F-AF07-0AFF0353DE26}",
						"dateTime": "2020-06-27T21:07:55.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 44.899993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 167.3000030517578
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{9C2B4CE9-D10A-F343-81C5-DE9FB3FFDB18}",
						"dateTime": "2020-07-13T14:33:45.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{9C501841-4458-AA46-9541-DC0500EC06B5}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{9DDC16F9-BEC9-CF48-B944-5E1540AFFA12}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{9E5D2419-5436-B844-A19F-13270084048B}",
						"dateTime": "2020-08-03T03:04:19.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.699981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{9EDE3079-B71C-FB40-ACC8-CC310DE063BE}",
						"dateTime": "2020-07-25T12:14:11.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{9EE22DB3-6B31-C64D-9C23-B86EFE6EE102}",
						"dateTime": "2020-07-24T05:04:34.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.4000244140625
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{9FB29978-39B4-BD4C-BC1A-ABAFA6CB8A12}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{A01BFEF6-FB89-2346-96FF-541D0F6BCB0B}",
						"dateTime": "2020-07-14T18:47:29.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{A139C72A-0644-1C4F-AEEA-D1C04110C360}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{A1E83320-7FB6-0A49-81CF-E63E8580F18A}",
						"dateTime": "2020-07-26T13:10:02.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A2AE8398-4E45-9F4F-BF90-1787B674EDF2}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{A350DD63-2975-2644-B250-412E82595B0E}",
						"dateTime": "2020-07-01T13:23:29.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 143.6999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{A41B0426-17A5-4E48-BC99-BD75BB770FA5}",
						"dateTime": "2020-07-11T01:04:05.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{A62C0E7F-1D9C-8D45-990C-22B0217BBD6F}",
						"dateTime": "2020-08-03T22:02:28.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.0999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A6C9E9E0-5D09-124E-B92E-32F3565172A8}",
						"dateTime": "2020-07-11T21:26:45.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{A709D63B-7923-1445-9226-C17195BEA247}",
						"dateTime": "2020-07-08T14:49:15.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 133.1999969482422
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A79A8992-2BEB-0C47-A532-FE4F44451879}",
						"dateTime": "2020-07-20T17:25:36.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{A804C0DA-73F6-834F-9278-2021C28CDF82}",
						"dateTime": "2020-07-19T20:47:40.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A834F91B-A270-A14B-95C4-39EE1F0022AD}",
						"dateTime": "2020-07-07T13:08:40.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{A92B10CB-FFEC-524F-ABB3-C82DE1A7DB62}",
						"dateTime": "2020-07-06T17:01:29.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 159.60000610351563
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							}
						],
						"value": [
							49.2000007629395
						]
					},
					{
						"id": "{A9861F71-2F0F-E14D-ACEB-683FB680D7F6}",
						"dateTime": "2020-07-27T05:59:46.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.9000000953674318
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A9AA9F75-C4A8-D74F-A57A-600E708FEFF5}",
						"dateTime": "2020-07-30T22:44:27.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.9000244140625
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{A9D88148-00B0-1A46-946A-9B3B4D9E8A0C}",
						"dateTime": "2020-07-20T05:20:48.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							49.5
						]
					},
					{
						"id": "{AA1C65B4-D6EC-C240-9780-3B0DF423F26F}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{AA4C42FC-23DF-6344-89D9-F14BA2D8A74C}",
						"dateTime": "2020-07-29T01:52:10.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							-99991
						]
					},
					{
						"id": "{AAE34538-CEDD-BB46-9B37-04E3B2772DAD}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{AB6AAF3F-F75C-7E48-91DD-4E7360D057C1}",
						"dateTime": "2020-07-01T01:05:16.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.79998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{ACB238EA-37DE-2340-9BB1-95E13F6E1A87}",
						"dateTime": "2020-08-02T06:22:46.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5999755859375
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{AE8B1794-3713-8444-8EB8-2235C6581482}",
						"dateTime": "2020-07-08T17:18:27.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 133.39999389648438
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{AF3A9B69-C45A-254D-B081-93E3345809C6}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{B05C0D34-D587-364C-B358-367138861D34}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{B1413686-3BB1-E643-A4BC-217A545A6C30}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{B1B87090-E438-7548-B58A-4ECF5570C9CD}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{B1F73EC0-B145-BD4E-A3FB-C2A575FAE61E}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{B297A894-82C8-2A42-8BFC-C1E5C5B1B6EB}",
						"dateTime": "2020-07-24T19:44:25.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{B5304E3B-476E-1241-8BB2-58D1FD2E1109}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{B54AF871-4C1A-6A46-BC8D-97957AFC6C8F}",
						"dateTime": "2020-08-06T13:32:28.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.4000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{B6502B06-11E2-B04E-8B97-4BFEA3DFCB11}",
						"dateTime": "2020-07-05T05:37:18.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{B6AFDB9D-3B8C-074F-9A88-3973489DC6D3}",
						"dateTime": "2020-07-15T13:09:12.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							49.2999992370605
						]
					},
					{
						"id": "{B734F4E1-232D-F646-A466-6C03F9FD720C}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{B7BA2B00-C912-7E4D-9801-371E614C7320}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{B8BAD2AE-BBDA-2A49-AAED-F503823E0B5C}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{B9E5A3DC-224C-B248-B541-D59B1BD75747}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{B9FFE7B4-9E82-634B-82DA-969FFD70F12F}",
						"dateTime": "2020-08-02T14:10:16.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{BA29B679-8C8A-D44A-93B0-E613DFA28B6D}",
						"dateTime": "2020-07-10T00:56:43.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							4.30000019073486
						]
					},
					{
						"id": "{BADD7C52-5950-394D-A6A1-C1A38E6FB7E8}",
						"dateTime": "2020-08-09T01:10:39.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{BB2D4A3F-1BC9-EF4E-ABF4-19ED9A88547F}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{BB4536E3-D1E2-8A49-9BB5-29A33AAC076D}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{BC56FC7D-1286-C94F-A412-330C2FF2124B}",
						"dateTime": "2020-07-04T06:25:48.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{BC869E12-11B2-FF49-8DB0-CFB8DA888F1A}",
						"dateTime": "2020-08-02T20:26:56.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.199981689453128
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{BD3313B5-024F-E34C-ABD6-410A695B0CED}",
						"dateTime": "2020-07-25T01:13:23.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{BDACB826-715E-FC4A-AA36-C6D35FC056D9}",
						"dateTime": "2020-07-01T05:10:39.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{BE0A9D6E-0419-0E44-A7F6-BB7E75B8F6CF}",
						"dateTime": "2020-08-09T18:32:04.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.20001220703125
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{BE10E8FE-B02E-6D4F-BAF2-5FEBEA35DB96}",
						"dateTime": "2020-07-26T01:38:10.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{BE21A4B0-78BD-2749-9989-DCD58C48BAF4}",
						"dateTime": "2020-07-16T05:39:35.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.4000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{BE338BAF-D8BF-5441-9AD5-DD8FA712B227}",
						"dateTime": "2020-08-09T20:30:37.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{BFCAC8B0-0FF5-7443-A9B6-2A0F3F69B5E2}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{C0008051-BF3E-B044-8425-F0090C6F2B46}",
						"dateTime": "2020-08-03T06:21:22.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.699981689453128
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{C0A9D79B-3665-B748-AF6A-B2E90117005D}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{C24580D5-ACA6-0B40-9851-A32A667D78BB}",
						"dateTime": "2020-07-31T01:28:39.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.4000244140625
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{C305F5F5-F38F-8147-9554-49AAB939168E}",
						"dateTime": "2020-08-09T05:22:07.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.4000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{C3115DB8-6C7C-7643-8419-07C438E22895}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{C3B8BB4E-001C-F443-BD5A-C9546D8FAABC}",
						"dateTime": "2020-07-20T01:04:42.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							49.5999984741211
						]
					},
					{
						"id": "{C4A93F6B-0F14-A548-A3AC-97ADFCA9A152}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{C4E9A5D7-4875-FF4F-95E0-98C1A0F3F42D}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{C6297548-D10E-A44C-BDA1-3B77AE7D7F9C}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{C64482C0-75ED-4447-8702-250FF5B0DBC1}",
						"dateTime": "2020-07-13T13:49:54.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{C64ED621-9E6B-A545-A048-5BBFF08642A6}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{C6B658C1-20A9-7445-9836-11A5717C25A8}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{C6D9D73D-5181-E441-9392-86323B9E174B}",
						"dateTime": "2020-07-06T09:25:43.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{C703780D-2F87-7147-B6FB-EBE41983BC6F}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{C7BF69CA-EACF-FD48-815D-CADA33A192CA}",
						"dateTime": "2020-07-24T11:46:52.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 160.6999969482422
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{C8BD7118-EF31-E345-ADC1-50ADE753A712}",
						"dateTime": "2020-07-23T20:38:41.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{C8EE0A3A-6D59-BA43-8A5E-06F02323AB6F}",
						"dateTime": "2020-07-18T04:34:41.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{C93A8D01-F36C-DC43-9379-9134D157AD46}",
						"dateTime": "2020-07-28T20:51:21.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{C9DB3E94-61F8-E64B-A16A-6AF4C830ADBF}",
						"dateTime": "2020-07-31T22:10:15.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.9000244140625
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{CA3F1D65-79AC-6447-B11B-B2E4E04D8ECF}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{CAF3C3DA-D829-844F-9615-D1AF06F6E531}",
						"dateTime": "2020-08-06T06:06:35.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.9000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{CB5B8010-BF2C-914D-8692-5DC047EA91A8}",
						"dateTime": "2020-07-21T20:10:53.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 8.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{CB7F31C3-6EEC-5F48-961D-71408E165482}",
						"dateTime": "2020-08-11T14:35:53.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{CBA94C19-9FED-CF47-ACE9-8D0E88F970BA}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{CC6025C9-22C4-1644-83C0-348030E6ECB2}",
						"dateTime": "2020-07-11T01:04:05.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{CD036523-7903-1249-B6CC-D52CA9DA4695}",
						"dateTime": "2020-08-01T05:43:00.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{CDDF3C36-50FA-E640-98C5-351CC84EF19C}",
						"dateTime": "2020-08-07T18:51:07.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 174.3000030517578
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{CDEF9253-C15B-5944-80A1-F67F7D0932D6}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{CEFBBA2D-312A-BF4B-9871-72D7504960D2}",
						"dateTime": "2020-08-11T22:40:29.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{CF19AF5F-7908-4143-AA65-AFAC9BBD69C9}",
						"dateTime": "2020-10-05T22:03:13.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							36
						]
					},
					{
						"id": "{CF813F88-6E83-8E40-8BAF-76ADB4A12957}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{CF97BF92-C293-174B-8E63-3F6CB8214BDA}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{D1EB36D9-E0A1-3648-A979-88D59992F55E}",
						"dateTime": "2020-07-25T05:30:52.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{D29A4283-0BE4-FB49-9FC6-B635B89DA2B8}",
						"dateTime": "2020-08-07T14:47:17.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -3.700000047683716
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{D2EFBF2F-F6A4-E04F-B4C8-98BB27F31E45}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{D30ABC8E-73EE-0642-863F-C15229D81F83}",
						"dateTime": "2020-08-09T18:32:04.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.399993896484378
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{D6176D96-698C-024B-8CFC-1C4675AFECA9}",
						"dateTime": "2020-08-08T21:06:45.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{D67D5D85-4EFA-3842-A7A5-420D72D37E59}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{D6D35B9E-A4CA-F04B-8072-505689130744}",
						"dateTime": "2020-07-27T22:13:57.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{D6F2F153-78E9-924B-9D7D-6AF03E00197E}",
						"dateTime": "2020-07-24T19:44:25.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.4000244140625
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{D80A0500-F556-3E40-B05A-18756527C003}",
						"dateTime": "2020-07-24T19:44:25.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{D828822C-5F21-0B44-B4E7-2D66F1051F71}",
						"dateTime": "2020-08-04T01:27:45.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{D8B00FA8-36BA-0D49-AA12-965D615E5B46}",
						"dateTime": "2020-07-20T21:21:13.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{D963A319-8613-6444-87FA-56282AAEFDBE}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{DB00BCF6-159B-2F4B-9C21-DF8A04124339}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{DBD0BA84-6EFB-BA4A-A801-BA88D63EFBF6}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{DC418114-7105-0843-82C6-88636EC8CF3C}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{DD3A5ED6-4AFF-0845-B436-A0AE7F4DF7EB}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{DD880AE2-97B9-274B-B2A6-B445B2B333E2}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{DD9E2D15-9ADD-A14E-B47B-5DBAD6125996}",
						"dateTime": "2020-07-01T20:59:12.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 167.10000610351563
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{DEEBB493-5CFC-C740-81CC-16BAF0F0B55C}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{DF5BD25C-A352-8B4B-AB06-F36489040A45}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{E00D31AE-BD2E-E646-B407-806565B4F28E}",
						"dateTime": "2020-10-09T13:39:49.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							8
						]
					},
					{
						"id": "{E154620A-9508-BD4C-8606-1451888DF177}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{E1A54BB4-5552-A043-9B22-1A1933818CE5}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{E1C8C310-F2A0-E043-8B43-D5889647945D}",
						"dateTime": "2020-07-06T01:34:57.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.800000190734863
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{E25135E4-9B97-DE4F-BE15-D8D174C376F2}",
						"dateTime": "2020-06-30T05:26:13.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.400000095367432
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{E3852FCA-1548-664C-BFAD-D7A28E9D094F}",
						"dateTime": "2020-06-29T21:12:38.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.199981689453128
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{E6600FB1-DA9D-1148-86C7-66C9F04D2475}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{E69FC2BC-7643-7248-A8A0-23BF950165E5}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{E6A0171D-6EA6-E248-BD8F-38AED8BC62DA}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{E7BC6396-BA38-484F-A5C7-8257489152E1}",
						"dateTime": "2020-08-03T05:32:30.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.699981689453128
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{E81D52DA-94E0-814B-93B4-4C53A3D9237D}",
						"dateTime": "2020-08-08T18:38:59.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.4000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 148.89999389648438
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{E9929BDD-E812-5E4B-81DD-5B1B68E993B3}",
						"dateTime": "2020-07-05T01:45:04.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.29998779296875
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.099999904632568
							}
						],
						"value": [
							48
						]
					},
					{
						"id": "{EAC091EE-8638-A842-A400-E5724D6966B7}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{EAD87329-1861-5D4E-8E5C-A42BBC3BB3FC}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{EB1C2EE7-734E-C342-B80C-A67A5275B9E7}",
						"dateTime": "2020-08-05T14:46:12.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5999755859375
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{EDAD2F5F-4809-6346-A14B-83E6AA4028F2}",
						"dateTime": "2020-08-01T14:12:14.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.199981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{EDCDFFE4-4865-2B49-93D4-8DBCD9E3CBE4}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{EEA22074-8AE3-7F43-A673-F85577FBCD95}",
						"dateTime": "2020-07-29T17:49:21.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{EF5B90C2-8323-1344-BD12-A92AA5B5121C}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{EFD3D50A-E91F-D241-9127-44CB459EBB26}",
						"dateTime": "2020-07-24T19:44:25.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F0182D9E-B735-DA44-B15A-D58430E2A131}",
						"dateTime": "2020-07-18T20:47:18.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F1370D7C-B634-8943-92A0-2BCE9F4A0864}",
						"dateTime": "2020-07-22T04:08:33.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.699999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.399993896484378
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F149819C-0C74-8E4D-B0C5-EBE2459A9802}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{F394EE18-27F9-F744-ABA0-DC58C2109FBE}",
						"dateTime": "2020-07-28T22:01:47.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F3BE32A3-1EFF-9548-BE90-4C1DEA1DEA20}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{F3CCB7B2-4A70-FC4B-A325-206AF16F5E98}",
						"dateTime": "2020-07-29T06:44:17.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							}
						],
						"value": [
							-99991
						]
					},
					{
						"id": "{F3D6C88C-643E-804D-97C6-7B30DE21EAEB}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{F437A788-09DF-E343-A38C-0071A03C422E}",
						"dateTime": "2020-07-08T05:26:17.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.20001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{F62587B1-3188-3841-B5E5-141DD51596B3}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{F6D9F400-B301-1A46-AC8B-D01DFA4CB409}",
						"dateTime": "2020-07-08T21:08:19.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 134.8000030517578
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{F73D605A-35B2-3441-8930-0C0F6B012017}",
						"dateTime": "2020-07-25T12:12:53.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.800018310546878
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F7BF077E-C2B4-934D-BAD5-17F53DD8656F}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{F8C372E9-2788-C74F-96A3-3B25B96A2A74}",
						"dateTime": "2020-07-21T01:24:16.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.300018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F906AE78-0629-7947-9091-E0CB852A5D6F}",
						"dateTime": "2020-08-08T14:45:04.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.600006103515628
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{F90BCEA5-BCE1-AC4E-9CEE-7068F4A4743F}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{F9A3708C-FC4A-B64C-AB08-F169EFAB244C}",
						"dateTime": "2020-07-22T21:04:25.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.300000190734863
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.300018310546878
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F9B9AE86-5283-4F41-977A-0A278787C537}",
						"dateTime": "2020-07-04T14:39:50.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{F9BBE7FA-8D1A-EE4F-B6BB-36266B3C646D}",
						"dateTime": "2020-06-29T06:39:53.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.699981689453128
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.599999904632568
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{FB6F698F-CD15-D542-9CE6-AC40503DD83A}",
						"dateTime": "2020-07-10T13:36:42.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							}
						],
						"value": [
							48
						]
					},
					{
						"id": "{FB7453FD-7D72-BE46-81EE-7A5E836704A0}",
						"dateTime": "2020-07-27T22:15:10.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.70001220703125
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							-99991
						]
					},
					{
						"id": "{FCF1F573-6B6B-A446-BEE5-9DD929E43C6F}",
						"dateTime": "2020-07-24T14:43:14.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.4000244140625
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 162.10000610351563
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{FD43CB65-8609-9245-BD11-175C62DB56F0}",
						"dateTime": "2020-07-24T13:51:21.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 161.60000610351563
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{FD6BFD9C-252A-A445-AC21-C77AB6BC387D}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{FDD321A3-D4B4-F342-930E-6F0E22D2B5CB}",
						"dateTime": "2020-07-09T05:46:25.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.5
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 46.20001220703125
							}
						],
						"value": [
							49.7000007629395
						]
					},
					{
						"id": "{FE86526A-DC06-6B41-B93A-B910D0BC9002}",
						"dateTime": "2020-07-07T09:13:13.000Z",
						"operationPoints": [
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -4.199999809265137
							},
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							}
						],
						"value": [
							49
						]
					},
					{
						"id": "{FEAF9B0C-6B04-E848-AEB6-8A706669A2AD}",
						"dateTime": "2020-08-04T14:47:44.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": 45.5
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": 0.10000000149011612
							}
						],
						"value": [
							50
						]
					},
					{
						"id": "{FF792EE8-ACA7-5B44-87F5-9E13C42CF431}",
						"dateTime": "2020-10-13T19:08:31.000Z",
						"operationPoints": [
							{
								"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
								"value": -99999999999
							},
							{
								"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
								"value": -99999999999
							}
						],
						"value": [
							null
						]
					},
					{
						"id": "{0023086C-5F83-7F43-AF29-98C0FE942336}",
						"dateTime": "2019-12-02T21:12:56.000Z",
						"operationPoints": [],
						"value": [
							53.4000015258789
						]
					},
					{
						"id": "{0140399C-290C-404D-BE63-A2B5A98A3871}",
						"dateTime": "2019-12-19T17:41:37.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{038CD360-74AB-4941-AA0B-915B56279611}",
						"dateTime": "2019-12-18T14:19:20.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{03D52098-A452-6548-9CB3-BA63EAA905E4}",
						"dateTime": "2020-01-08T05:27:05.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{065E667E-AC1E-E244-8DA6-74F0EEC64F4A}",
						"dateTime": "2020-01-02T05:43:58.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{0690C3D9-AF1C-B54A-8959-97313AAA4841}",
						"dateTime": "2019-12-07T05:44:00.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{06E1B3D4-56E3-6946-AA30-8797B6B50861}",
						"dateTime": "2019-12-16T05:26:06.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{079A51B6-B24A-B344-B0C8-26BF9C3DFCA8}",
						"dateTime": "2019-12-24T14:57:39.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{07B9D43E-BA31-6D4A-861E-90063044E20A}",
						"dateTime": "2019-12-14T21:25:23.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{094D14BF-459D-C04C-86C6-6EAA254EB4FC}",
						"dateTime": "2020-01-03T18:36:13.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{0AF3A008-3B8D-D44C-B4CB-DCA5CFA24285}",
						"dateTime": "2019-12-17T09:15:55.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{0B5D444E-275B-C344-BB2E-265705AF3B51}",
						"dateTime": "2019-12-19T06:23:17.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{0DE3EFE2-FBD3-874F-A5D8-40F2EE09CB0A}",
						"dateTime": "2019-12-14T21:25:23.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{0FB1DED4-8C3F-0F4C-A327-5932F440E4E3}",
						"dateTime": "2019-12-24T05:11:23.000Z",
						"operationPoints": [],
						"value": [
							53.5
						]
					},
					{
						"id": "{112A695F-08E9-F749-B7CB-64E98A4B0F92}",
						"dateTime": "2020-01-08T23:25:10.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{11C257E4-D7A8-0A40-9788-2F6457C0FC56}",
						"dateTime": "2019-12-06T13:28:00.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{11F7163A-F57B-9945-8122-F699D45C0E3A}",
						"dateTime": "2020-01-09T21:35:53.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{120D0C4A-BB8D-E34C-B34B-274AFA3A610C}",
						"dateTime": "2019-12-28T09:29:07.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{12998C1F-F6BB-E842-8C48-B18B3EA45F4F}",
						"dateTime": "2020-01-06T14:22:29.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{136D5429-3B46-E148-A2D1-A0D48411570C}",
						"dateTime": "2019-12-22T01:15:14.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{14AC2B26-4F92-BA4F-878C-ED49DCC14EF0}",
						"dateTime": "2019-12-20T21:21:00.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{15046B69-6039-0644-99BB-2D0C8BC2E257}",
						"dateTime": "2020-01-05T17:10:27.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{1625B5A0-312C-DF4D-9FA0-93BCA0AB7407}",
						"dateTime": "2019-12-12T13:31:08.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{17B26DA4-8D10-7341-B50D-1636B77F1D60}",
						"dateTime": "2019-12-12T01:12:55.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{18749343-6547-B74F-B0E5-C357D30DE520}",
						"dateTime": "2019-12-20T01:23:35.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{1890A2F8-C40B-CC45-B704-6B8DCDD61C4F}",
						"dateTime": "2019-12-11T05:29:10.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{1A08A49F-3066-2F43-885E-D9817812DD79}",
						"dateTime": "2020-01-02T02:37:34.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{1F514E8B-6E23-4446-AACA-3C9192767CDB}",
						"dateTime": "2020-01-13T05:04:32.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{214F6E61-E8D8-E241-8B3D-8096F05923CB}",
						"dateTime": "2019-12-28T01:32:15.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{237119E3-C5B6-1F47-981D-1396C110A81E}",
						"dateTime": "2019-12-14T21:25:23.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{23FA1334-222F-C842-8EE8-F327F6F57595}",
						"dateTime": "2019-12-26T06:20:11.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{24CCACF3-5E3C-754D-B7AA-E018AD85C853}",
						"dateTime": "2019-12-28T13:45:13.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{278136BB-33A9-454B-BB65-65A34E72FB12}",
						"dateTime": "2020-01-07T01:03:24.000Z",
						"operationPoints": [],
						"value": [
							53.0999984741211
						]
					},
					{
						"id": "{278FA335-3347-304A-AF50-8C3AEECE1718}",
						"dateTime": "2020-01-06T22:07:30.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{2AC15A45-29D6-204D-B644-A0A792A711D3}",
						"dateTime": "2020-01-11T09:03:37.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{2D0600FB-0AA0-E440-BAC8-EB2B4E2FAA99}",
						"dateTime": "2019-12-06T21:47:22.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{2D0F49F6-ED83-9240-B7AD-07DC762E9E63}",
						"dateTime": "2019-12-04T21:20:09.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{2D31AB89-27CA-8644-8E83-D61562F7BC30}",
						"dateTime": "2019-12-25T17:50:20.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{30E35B02-3BC1-F44E-A1DE-F1B758ED686D}",
						"dateTime": "2019-12-16T16:53:35.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{32250DE3-7C5B-F640-89B6-2505AA98B808}",
						"dateTime": "2019-12-16T10:59:07.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{32D4856F-011E-BC41-BC44-2BBAC13E9D0A}",
						"dateTime": "2019-12-23T13:50:58.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{352C53F9-D096-9B4B-962F-1C8D0975CABC}",
						"dateTime": "2019-12-11T01:15:15.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{3549CA75-34B9-D448-BF05-10362D329D2E}",
						"dateTime": "2019-12-10T21:04:41.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{36248E68-DC92-1248-B01D-09E18C989A53}",
						"dateTime": "2019-12-15T05:41:43.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{36D68370-41D1-7147-A47F-58A0B8870BBA}",
						"dateTime": "2020-01-09T04:56:00.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{385418FD-380F-1846-A057-6D0DB9E2E42D}",
						"dateTime": "2020-01-07T18:34:29.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{38D0A0F6-D574-8548-A756-AEA23800ADDA}",
						"dateTime": "2020-01-09T13:15:15.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{394E54D5-F078-D84F-8BCB-74FBCC705C53}",
						"dateTime": "2019-12-25T13:33:50.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{39BC32B0-D527-7641-AFC8-A832ECCDC93F}",
						"dateTime": "2019-12-28T21:26:13.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{3BE99D35-A3C1-0440-A44A-A9C5653536AC}",
						"dateTime": "2019-12-24T18:28:47.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{3D60216F-689F-0F45-9040-35536FE1912E}",
						"dateTime": "2019-12-14T17:30:51.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{3D6D6D2A-F381-1245-8BEA-30E04868CCB0}",
						"dateTime": "2020-01-14T05:04:46.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{3E59691B-521E-A14D-96C9-726C1558FA96}",
						"dateTime": "2020-01-03T05:05:50.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{3E871C02-0C94-6048-B803-85A37771592A}",
						"dateTime": "2020-01-11T13:09:29.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{3E9CB5D0-1492-344E-8338-C9A2080D2529}",
						"dateTime": "2019-12-31T13:01:03.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{3EA0E322-A450-714C-B62F-C0D3EA6F2C24}",
						"dateTime": "2020-01-07T20:51:15.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{3FA1EAB2-BFB5-494D-B9AC-2504804C0F3A}",
						"dateTime": "2020-01-02T13:46:50.000Z",
						"operationPoints": [],
						"value": [
							52.7000007629395
						]
					},
					{
						"id": "{3FD46096-D4C4-5745-B842-89EA0F1103B3}",
						"dateTime": "2019-12-22T21:51:57.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{408512F3-7A92-F849-A5CD-20A6200F6C5B}",
						"dateTime": "2020-01-04T01:09:06.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{40F5225B-2E71-D540-9E07-12F81A7350D3}",
						"dateTime": "2020-01-07T13:13:39.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{41C4C984-F1DF-2C4D-B6A7-A748B7DC11D0}",
						"dateTime": "2019-12-11T14:52:02.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{42091481-C806-5D40-90AC-6E0F65916096}",
						"dateTime": "2019-12-13T08:42:14.000Z",
						"operationPoints": [],
						"value": [
							52.7000007629395
						]
					},
					{
						"id": "{42A15B46-6D7D-B84E-8F67-87C060FE92AC}",
						"dateTime": "2020-01-04T17:21:10.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{43177070-B8CF-D844-B7DE-A62ACDF0BBE9}",
						"dateTime": "2020-01-12T13:28:49.000Z",
						"operationPoints": [],
						"value": [
							52.7999992370605
						]
					},
					{
						"id": "{4333CF7D-42C9-1E41-9F12-FA101929BA8E}",
						"dateTime": "2019-12-12T05:25:00.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{43D73BE4-EF9E-C740-8CB1-F9CED80C8C58}",
						"dateTime": "2020-01-03T01:10:39.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{4435E443-A5B2-094D-8D83-5665379243D5}",
						"dateTime": "2019-12-02T05:22:30.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{448E7B27-E4F2-6C40-A983-CD813A9DA956}",
						"dateTime": "2020-01-02T16:59:39.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{44B2A4A1-6C4A-A041-B496-7EBA18AC18A6}",
						"dateTime": "2020-01-12T01:48:41.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{4524A3DD-B81C-1040-8A35-545DE33F9E00}",
						"dateTime": "2019-12-10T01:10:44.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{457F1CCB-9677-0142-81D7-F9A11D8AFF30}",
						"dateTime": "2019-12-03T21:46:54.000Z",
						"operationPoints": [],
						"value": [
							53.2000007629395
						]
					},
					{
						"id": "{472FAACE-8659-E84B-9242-9D09DA25AFB7}",
						"dateTime": "2019-12-07T21:23:18.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{47795A8D-FB97-C543-9EBC-74A52EB8BC20}",
						"dateTime": "2020-01-14T01:23:53.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{47F3E341-ED0E-3A49-AB42-D1C2A12F9BAD}",
						"dateTime": "2019-12-04T01:07:51.000Z",
						"operationPoints": [],
						"value": [
							53.2999992370605
						]
					},
					{
						"id": "{48739D5A-E1AA-EB42-A99C-246A01953574}",
						"dateTime": "2019-12-25T05:11:40.000Z",
						"operationPoints": [],
						"value": [
							53.2000007629395
						]
					},
					{
						"id": "{489EDE03-4B33-F44B-9A11-4885701C01BC}",
						"dateTime": "2019-12-13T12:54:50.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{4A07E9DD-183E-514B-9356-248189A1404D}",
						"dateTime": "2020-01-11T17:17:57.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{4B0C3C87-B75E-F942-AFF2-D17F776F7AF5}",
						"dateTime": "2019-12-18T05:59:04.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{4C2A5A3C-ABF3-5641-A0A4-A80262059FA9}",
						"dateTime": "2020-01-09T15:59:02.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{4C2B1B42-CD2E-BF46-AFAF-BA3348A4200B}",
						"dateTime": "2019-12-02T17:05:27.000Z",
						"operationPoints": [],
						"value": [
							53.5999984741211
						]
					},
					{
						"id": "{4C32A63C-FB5F-D64D-B56C-ADBAB6EAA412}",
						"dateTime": "2019-12-27T01:52:53.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{4D03696B-23BB-5D47-8977-AD1AEC878E1B}",
						"dateTime": "2019-12-14T17:30:51.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{4D3E3599-7AC8-1242-B375-693E6BABD760}",
						"dateTime": "2019-12-14T21:25:23.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{4FCB945D-4884-9247-AC26-E7C368D67085}",
						"dateTime": "2019-12-30T05:28:18.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{5151BC39-FA65-704C-A3BB-FD314F8A7503}",
						"dateTime": "2019-12-18T21:12:49.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{53B8F7CD-99AB-D241-9016-3CB7563D461B}",
						"dateTime": "2020-01-05T13:37:58.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{5425EC59-41D5-0F44-AE01-7E639CE8950C}",
						"dateTime": "2019-12-21T17:09:47.000Z",
						"operationPoints": [],
						"value": [
							52.7999992370605
						]
					},
					{
						"id": "{54518833-70E8-DB48-B146-4163FBCE13AD}",
						"dateTime": "2019-12-31T05:24:46.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{54CE6D24-8A12-1E40-84EF-9581E9437A60}",
						"dateTime": "2019-12-05T05:11:15.000Z",
						"operationPoints": [],
						"value": [
							53.5
						]
					},
					{
						"id": "{5602F5A7-1ACD-0745-827D-E443216E6A4A}",
						"dateTime": "2019-12-15T01:24:37.000Z",
						"operationPoints": [],
						"value": [
							53.2999992370605
						]
					},
					{
						"id": "{56771E60-520F-C446-A138-C9F32A80F660}",
						"dateTime": "2019-12-23T21:19:13.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{56982E5D-188A-5A4E-B7C8-03CB289C1128}",
						"dateTime": "2019-12-24T22:33:15.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{5781B4FA-DA30-DB49-BCDF-A779D292C09A}",
						"dateTime": "2019-12-03T14:15:20.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{57DE9A40-DBC8-914B-B8F2-5EDB0A4CB293}",
						"dateTime": "2020-01-02T05:43:58.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{581AFBDC-24E3-C748-B003-9D0CE79CD1EC}",
						"dateTime": "2019-12-30T13:01:27.000Z",
						"operationPoints": [],
						"value": [
							52.7000007629395
						]
					},
					{
						"id": "{584EEE79-7689-7C4D-9C04-0C1D07730B50}",
						"dateTime": "2019-12-22T09:25:55.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{5ADE695E-F849-0349-B4B2-C6C143893105}",
						"dateTime": "2019-12-12T08:59:47.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{5B31EC7D-13DB-C24D-8ECF-677DBBCE0E06}",
						"dateTime": "2019-12-14T17:30:51.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{5BEA15C3-C012-3B4C-9EF6-0051AA927A77}",
						"dateTime": "2019-12-14T17:30:51.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{5C3BF8BC-7283-7046-B083-06537EDF8FA5}",
						"dateTime": "2019-12-14T21:25:23.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{5D2F4B43-961B-6E47-B5B5-07C83A9F5E15}",
						"dateTime": "2020-01-01T06:06:30.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{5D85C08A-4B20-C44E-A3E0-F8D3F0443F90}",
						"dateTime": "2019-12-14T17:30:51.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{5EA0D592-1FB6-CF48-B07D-000EE3430166}",
						"dateTime": "2019-12-09T05:34:19.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{5EAD9433-661A-8B40-859F-4E39EEAE7654}",
						"dateTime": "2019-12-29T02:07:11.000Z",
						"operationPoints": [],
						"value": [
							53.5
						]
					},
					{
						"id": "{5F391F44-DE39-284C-920E-697F4C928E1E}",
						"dateTime": "2020-01-11T05:16:40.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{5F556E2A-0D92-144A-8BD0-429AED7BDAC7}",
						"dateTime": "2019-12-14T21:25:23.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{5F62615A-8C58-0A47-9D97-0B66CC9F15E1}",
						"dateTime": "2020-01-10T01:20:14.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{5FE8C02A-2487-F14C-B4E5-198BEB218C76}",
						"dateTime": "2020-01-11T02:57:13.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{60816A6A-7CDE-E04A-9171-7D9EF419D6A8}",
						"dateTime": "2020-01-01T09:34:13.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{6129CEA7-BCC9-8D45-8F9B-E5147CE70958}",
						"dateTime": "2019-12-17T01:04:46.000Z",
						"operationPoints": [],
						"value": [
							53.5
						]
					},
					{
						"id": "{626E4743-D6B4-EC44-B7E6-ED9A4ACE1F5F}",
						"dateTime": "2019-12-07T17:31:46.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{628AE9D1-1696-4A41-BE38-5CF70E045F07}",
						"dateTime": "2019-12-27T21:20:33.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{639646F5-E23E-AD4C-ADFD-16E464A0853A}",
						"dateTime": "2019-12-10T09:13:47.000Z",
						"operationPoints": [],
						"value": [
							53.2000007629395
						]
					},
					{
						"id": "{6445C45D-F417-C046-9968-4B7216318FC0}",
						"dateTime": "2019-12-23T01:37:00.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{6447BF13-3707-2044-B231-81CE42F30376}",
						"dateTime": "2019-12-05T21:46:48.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{64503D1A-5E70-C34C-8943-5A1B36226642}",
						"dateTime": "2019-12-04T05:11:23.000Z",
						"operationPoints": [],
						"value": [
							53.2000007629395
						]
					},
					{
						"id": "{661252F2-0AD0-774E-AE56-8480B3EB772B}",
						"dateTime": "2019-12-14T21:25:23.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{66D87E50-76CA-C547-BE67-4102217F3981}",
						"dateTime": "2020-01-14T13:42:16.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{671EDE10-7EBA-AD4D-B843-C100CDF309B0}",
						"dateTime": "2019-12-31T17:05:55.000Z",
						"operationPoints": [],
						"value": [
							53.4000015258789
						]
					},
					{
						"id": "{677C2085-5592-624A-ADEB-42416D518A6F}",
						"dateTime": "2019-12-14T17:30:51.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{67A4DF7D-3826-9E43-9A64-2A79EC9B2D61}",
						"dateTime": "2019-12-23T05:16:16.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{687CF813-A338-6246-9263-7D400AC755A9}",
						"dateTime": "2020-01-01T13:34:45.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{68AADCCA-DAD6-0743-B6CF-9A10B9DA601B}",
						"dateTime": "2019-12-02T14:15:25.000Z",
						"operationPoints": [],
						"value": [
							53.7000007629395
						]
					},
					{
						"id": "{68C6D7E2-FD4B-FA44-A943-15F65E888AA4}",
						"dateTime": "2020-01-08T20:02:01.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{690EE3AA-1559-3D4F-90B3-9D3A2EB3E414}",
						"dateTime": "2019-12-08T13:57:02.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{697FE754-E462-3945-8074-3CEDF6D307B2}",
						"dateTime": "2019-12-31T21:00:25.000Z",
						"operationPoints": [],
						"value": [
							53.2999992370605
						]
					},
					{
						"id": "{69D9A8D5-C0F9-E343-9622-CCB5176C3ECA}",
						"dateTime": "2019-12-07T12:43:50.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{6B1956C8-5604-F543-9BAA-3A6B666D94CA}",
						"dateTime": "2019-12-24T09:29:42.000Z",
						"operationPoints": [],
						"value": [
							53.2000007629395
						]
					},
					{
						"id": "{6BE31976-A3C2-B343-8C87-452377B24F43}",
						"dateTime": "2019-12-05T08:56:52.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{6C6C9F1A-DBA6-2B4A-920A-CCC623328DBC}",
						"dateTime": "2020-01-12T22:07:21.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{6CC7B2EE-0A50-2640-84DB-67FE10D6343C}",
						"dateTime": "2019-12-13T01:03:42.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{6CCF2123-38C6-0949-926B-55353A11F36D}",
						"dateTime": "2019-12-18T13:56:01.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{6CE87E64-8EDD-1C4C-8369-2F228B2B1333}",
						"dateTime": "2019-12-06T14:03:18.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{6EB7E6A2-94BA-9443-B9F8-9F2F2CDACFC6}",
						"dateTime": "2019-12-04T08:40:22.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{6EE9DB76-851D-DB42-8C91-1B7FDF855F11}",
						"dateTime": "2019-12-03T16:51:39.000Z",
						"operationPoints": [],
						"value": [
							52.2000007629395
						]
					},
					{
						"id": "{70621351-7B47-3B4C-8E32-C2B81F060C9D}",
						"dateTime": "2019-12-14T21:25:23.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{706561FB-C319-3541-ACC9-966CCB48ABB8}",
						"dateTime": "2019-12-31T01:17:58.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{706E6B2A-EFCF-B44A-8619-FC77EA54B7F9}",
						"dateTime": "2019-12-21T01:13:23.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{70A862D0-FB6B-6C4F-9FD2-ACE92664108B}",
						"dateTime": "2019-12-14T21:25:23.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{71D45843-A693-B64F-A91E-8BB0E04AA979}",
						"dateTime": "2019-12-25T09:18:19.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{73BE76B9-E623-3049-A34B-F17DF8AE7146}",
						"dateTime": "2020-01-13T22:07:51.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{74CE95CB-39BF-CA4D-A3C6-969D9348BDE9}",
						"dateTime": "2020-01-05T13:37:58.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{75F51EA1-6AF8-0E40-A8F9-9C8649512857}",
						"dateTime": "2019-12-30T09:04:36.000Z",
						"operationPoints": [],
						"value": [
							53.2000007629395
						]
					},
					{
						"id": "{75F8FBFB-DF8E-A14B-A8A3-4EECB88922BE}",
						"dateTime": "2019-12-24T01:22:22.000Z",
						"operationPoints": [],
						"value": [
							53.2999992370605
						]
					},
					{
						"id": "{767F0056-5AE9-264E-A15C-FBD3AC2701EC}",
						"dateTime": "2019-12-20T05:57:48.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{76AFB36D-43CF-7B4B-9E60-DBB659F0FDF4}",
						"dateTime": "2019-12-14T17:30:51.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{77B4348A-EBE0-F145-808D-7A92865318CF}",
						"dateTime": "2020-01-12T18:09:51.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{79CD7FA5-EAF2-D34C-81CD-38D485C5F59A}",
						"dateTime": "2019-12-05T17:48:27.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{7AB6A298-D393-9041-B07D-A5745724465D}",
						"dateTime": "2019-12-11T09:12:45.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{7B3000FB-70DF-D04D-897E-D5C7D39699DA}",
						"dateTime": "2020-01-10T21:03:58.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{7B4657BC-6F72-DC4E-8B44-EEB723C713A1}",
						"dateTime": "2019-12-14T21:25:23.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{7C7084FB-BAA9-8F45-8D76-DC3984D03C9E}",
						"dateTime": "2019-12-31T09:47:26.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{7C8A53DE-4973-ED4D-BA2B-8069BCFDA243}",
						"dateTime": "2019-12-26T20:25:32.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{7E076461-7E6B-C148-B813-F16669A531DE}",
						"dateTime": "2019-12-29T05:34:52.000Z",
						"operationPoints": [],
						"value": [
							53.2999992370605
						]
					},
					{
						"id": "{7E61B62E-9C58-F843-96DD-569A35D59A85}",
						"dateTime": "2020-01-11T21:04:03.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{7EB2CF73-1DF6-9543-A576-9D440D74DA43}",
						"dateTime": "2019-12-09T20:37:42.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{7F022FE7-42B2-E549-9F28-1FD49A790ED4}",
						"dateTime": "2019-12-07T14:26:19.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{7F0E8D3C-BC6C-4C49-8D03-355492C23971}",
						"dateTime": "2019-12-09T16:43:35.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{7F3A0B6E-BD16-0242-9636-555FA92A0C82}",
						"dateTime": "2019-12-03T05:57:21.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{80CEC91B-B824-664A-A612-D5DF9E67D637}",
						"dateTime": "2020-01-02T10:44:22.000Z",
						"operationPoints": [],
						"value": [
							52.5999984741211
						]
					},
					{
						"id": "{842BBB57-0242-6A4D-AF30-D05F4B403607}",
						"dateTime": "2019-12-18T05:59:04.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{858CB9DC-B7E3-5A4D-8EDE-C2F50341BC7C}",
						"dateTime": "2019-12-18T21:12:49.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{85D9B432-2710-A74A-BE0F-397EC56161AC}",
						"dateTime": "2020-01-06T18:45:37.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{86140E29-6133-824C-AADB-3E88BB6EAAA5}",
						"dateTime": "2019-12-10T13:11:28.000Z",
						"operationPoints": [],
						"value": [
							53.0999984741211
						]
					},
					{
						"id": "{8696330A-7063-0B4A-82F9-AC27B3704FA4}",
						"dateTime": "2019-12-20T16:15:11.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{87BA8FA3-51FC-C94C-9548-E324AE5AFDDB}",
						"dateTime": "2019-12-27T09:07:43.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{8ABC5879-2281-8043-87C5-B9E32F3F505D}",
						"dateTime": "2019-12-20T13:15:26.000Z",
						"operationPoints": [],
						"value": [
							52.2999992370605
						]
					},
					{
						"id": "{8CCBEC4B-1AEC-0C4B-B237-B849A0CE1E33}",
						"dateTime": "2019-12-26T14:12:28.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{8F6127ED-230A-A640-8A7D-8F5F9CFCB3C8}",
						"dateTime": "2019-12-14T17:30:51.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{90727512-8BA1-C940-9376-D6B1026273B0}",
						"dateTime": "2020-01-05T05:23:00.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{90730207-7B47-EB46-8743-B18D1E2D24B6}",
						"dateTime": "2019-12-08T21:15:59.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{909DE750-FB9A-0A48-B476-93C53688C5A2}",
						"dateTime": "2019-12-25T01:19:42.000Z",
						"operationPoints": [],
						"value": [
							53.2000007629395
						]
					},
					{
						"id": "{919DC2CE-B5BD-AA4A-A99C-EE293FE8F0AF}",
						"dateTime": "2019-12-29T09:02:44.000Z",
						"operationPoints": [],
						"value": [
							53.2000007629395
						]
					},
					{
						"id": "{91B962F9-009E-FC4B-A2F3-111A45FCC22F}",
						"dateTime": "2020-01-03T10:53:51.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{93B8D97D-2A86-504D-B2CC-E30011A21CAE}",
						"dateTime": "2019-12-10T17:42:50.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{93C4B830-AF6C-3847-A9F2-9EAD159CED29}",
						"dateTime": "2020-01-08T14:10:12.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{94E57D87-07E1-204F-B328-0334AB467DCE}",
						"dateTime": "2019-12-29T12:59:32.000Z",
						"operationPoints": [],
						"value": [
							53.2999992370605
						]
					},
					{
						"id": "{95269324-8884-3146-B989-24F5C1B72C45}",
						"dateTime": "2020-01-05T01:16:41.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{952DFF23-386B-984E-803F-AE387FFCDE4A}",
						"dateTime": "2020-01-12T09:06:29.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{9865246C-9BC5-B54A-ACFB-9F32D36B8E5C}",
						"dateTime": "2020-01-05T13:37:58.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{9869FB4C-0C24-9141-90BF-15F5A4587028}",
						"dateTime": "2019-12-14T21:25:23.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{995D03B9-CF9F-0347-A00B-43D0212493B7}",
						"dateTime": "2020-01-11T12:08:45.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{9BBF3744-A861-9A4C-94F1-5F339F86AF44}",
						"dateTime": "2019-12-21T05:21:54.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{9BC0F0D7-9ADF-F14A-B3D3-DCAA5F02F946}",
						"dateTime": "2019-12-24T01:22:22.000Z",
						"operationPoints": [],
						"value": [
							53.2999992370605
						]
					},
					{
						"id": "{9C7194AB-B9F7-5D4A-90FB-689AEF0AB0E2}",
						"dateTime": "2019-12-17T05:47:40.000Z",
						"operationPoints": [],
						"value": [
							53.2999992370605
						]
					},
					{
						"id": "{9D061FAA-5773-344F-85D7-A868E564C499}",
						"dateTime": "2019-12-04T05:11:23.000Z",
						"operationPoints": [],
						"value": [
							53.2000007629395
						]
					},
					{
						"id": "{9E68E9F1-45FF-2F4A-9340-E8DB05471445}",
						"dateTime": "2019-12-20T09:05:05.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{9EE589B0-A049-6F4D-997D-4A376CA71BA9}",
						"dateTime": "2019-12-27T06:01:35.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{9F454B7B-1D30-6445-A79B-DD93588878B1}",
						"dateTime": "2019-12-06T17:32:47.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{9FDFBB20-6BAA-7D47-8683-93A6FCF5ACAD}",
						"dateTime": "2019-12-14T05:45:20.000Z",
						"operationPoints": [],
						"value": [
							53.5
						]
					},
					{
						"id": "{A04A692E-001A-A449-A1BD-13429975CE7B}",
						"dateTime": "2019-12-09T13:08:48.000Z",
						"operationPoints": [],
						"value": [
							52.7999992370605
						]
					},
					{
						"id": "{A0AD4850-05B5-9246-8338-E5C7A12422FD}",
						"dateTime": "2019-12-29T21:18:39.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{A306C5CE-7105-9F47-A0EF-8B5810002EBE}",
						"dateTime": "2019-12-04T13:48:46.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{A527E050-02EE-564D-BEA3-F33A3875FA90}",
						"dateTime": "2019-12-12T21:12:18.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{A62521F7-6C74-C64B-B428-A47200B15715}",
						"dateTime": "2020-01-01T05:35:43.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{A874A667-A2E0-B743-8DBA-319357325834}",
						"dateTime": "2020-01-06T14:23:00.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{A9D88F25-8C12-D946-A701-52D054EBC335}",
						"dateTime": "2019-12-03T13:55:42.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{AA0FF176-77C3-6A4F-B46E-C5A42DB8D1A9}",
						"dateTime": "2020-01-06T01:11:41.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{ABDD0DC2-0B05-154D-9B11-7F3FC8704A09}",
						"dateTime": "2019-12-19T21:10:59.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{AC522AF3-84CF-4D4B-86F3-861316291146}",
						"dateTime": "2020-01-06T05:29:48.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{AC72C2E6-82B4-B843-8E42-DECE8790676A}",
						"dateTime": "2020-01-14T09:01:20.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{AD3D8818-AC74-D243-B5D0-FCB31FB05FD4}",
						"dateTime": "2019-12-18T17:25:55.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{AD6E7CAB-827B-EA4A-9D39-7BED1013392F}",
						"dateTime": "2020-01-04T05:08:06.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{AFCD1369-94FC-0848-918B-1CC07BD01985}",
						"dateTime": "2019-12-11T17:10:40.000Z",
						"operationPoints": [],
						"value": [
							53.0999984741211
						]
					},
					{
						"id": "{AFE74E17-F6B1-154F-80E8-935389FD9670}",
						"dateTime": "2020-01-04T13:37:31.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{B1F9887D-2038-C24D-927E-7DA5227D8CAF}",
						"dateTime": "2019-12-26T21:37:55.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{B3978F27-553B-1A4E-B64D-CE51CAFE4981}",
						"dateTime": "2019-12-19T13:14:57.000Z",
						"operationPoints": [],
						"value": [
							52.7999992370605
						]
					},
					{
						"id": "{B3A515CB-5A1A-3C48-BF82-88C5108E8F56}",
						"dateTime": "2019-12-22T21:08:06.000Z",
						"operationPoints": [],
						"value": [
							52.5
						]
					},
					{
						"id": "{B3CD02FD-C739-0443-B5B2-C50B4638AE4D}",
						"dateTime": "2019-12-14T17:30:51.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{B5BD15C2-C869-A54C-9548-424F9B427FE1}",
						"dateTime": "2020-01-10T21:53:32.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{B7377D8F-AA13-844E-98C3-D8AA38AE1548}",
						"dateTime": "2019-12-06T05:13:34.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{B8398A52-5B1D-B44F-A8DE-BE2423EB4BD5}",
						"dateTime": "2019-12-09T13:08:48.000Z",
						"operationPoints": [],
						"value": [
							52.7999992370605
						]
					},
					{
						"id": "{B911C527-E0FA-C249-B95F-4E894B4FB017}",
						"dateTime": "2020-01-05T21:08:00.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{B9C60DD9-0256-AB4D-8477-A499F3AF4A52}",
						"dateTime": "2020-01-09T23:20:06.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{BB0E7ACF-18DC-344A-BE1C-679D0D3AEB8A}",
						"dateTime": "2020-01-10T06:08:30.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{BD309CAE-0677-5F44-9BC2-6C1278EB5EE3}",
						"dateTime": "2020-01-03T21:45:17.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{BE8A06E8-D489-E54D-B98C-147064C049B5}",
						"dateTime": "2020-01-07T15:22:15.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{BED008E9-3A29-1842-AB89-5CFC8BD9C070}",
						"dateTime": "2019-12-09T01:04:06.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{BFFD678B-3929-6347-B40F-CA2E0C7A369A}",
						"dateTime": "2019-12-30T17:40:45.000Z",
						"operationPoints": [],
						"value": [
							52.7000007629395
						]
					},
					{
						"id": "{C0498313-04D0-3B45-9415-C92BC93BA921}",
						"dateTime": "2019-12-19T06:23:40.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{C0561B54-6334-DD48-8D6E-50F8CF93EE0D}",
						"dateTime": "2019-12-26T14:22:19.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{C0EAEB41-DF6E-804B-BDCE-5CC63658F15B}",
						"dateTime": "2019-12-16T22:05:53.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{C0EF3DCC-4ED6-2E41-9E8A-CE44A44DC299}",
						"dateTime": "2019-12-23T18:59:23.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{C2017075-4963-0B41-BE60-698C78CF8899}",
						"dateTime": "2019-12-27T16:54:46.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{C22C5E84-8F5B-6149-BDE3-5C698AC7053C}",
						"dateTime": "2019-12-07T01:14:31.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{C36ED516-1800-CF47-B47D-BF767B61A8AF}",
						"dateTime": "2020-01-13T01:05:43.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{C3B9D99D-3BEA-6A4C-97C2-448FD411DA9E}",
						"dateTime": "2019-12-13T05:54:45.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{C5BF2140-A85E-FC46-8E8A-38DC0C6E800E}",
						"dateTime": "2019-12-18T05:59:04.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{C78DE9F5-5811-3E43-92DE-CEF67B5CECBE}",
						"dateTime": "2019-12-27T13:07:27.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{C8251908-13BE-2749-B976-C9C0734E0D98}",
						"dateTime": "2019-12-21T09:08:02.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{C84D9E07-F373-5A49-8BAE-ED7330286074}",
						"dateTime": "2019-12-14T17:30:51.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{C882B3A0-58C0-7943-B0E1-9B16B1ECB29D}",
						"dateTime": "2019-12-07T17:31:46.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{C9097014-A54A-364A-ACFB-141F687EAAFB}",
						"dateTime": "2019-12-26T01:19:56.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{CB74DEB7-7A7A-9D49-AE8B-91E9C4250C7C}",
						"dateTime": "2019-12-11T21:14:00.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{CB79456D-1C54-2F46-B3A1-552FC3FA1339}",
						"dateTime": "2019-12-08T17:20:58.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{CB9AB7FB-CA40-714E-ACE5-14E0E591556C}",
						"dateTime": "2019-12-03T06:13:23.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{CBF9A314-A6D8-E341-9F47-1B29E3E96C4A}",
						"dateTime": "2019-12-08T09:30:19.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{CF57B446-4479-9A45-B931-84DB7445DC29}",
						"dateTime": "2019-12-28T17:10:27.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{D0849A83-7880-524B-B269-047E69528B3C}",
						"dateTime": "2019-12-14T17:30:51.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{D0BC9C84-FD17-5E40-B86B-1C39094C5C50}",
						"dateTime": "2019-12-17T14:10:56.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{D0FE47D2-EC59-7341-8686-53DE87B2FFDF}",
						"dateTime": "2019-12-14T21:25:23.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{D53B8E96-0681-C24B-83BE-F7F9855631A3}",
						"dateTime": "2019-12-23T09:36:23.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{D68092DD-B960-7C4F-9212-B9C82CE8D86B}",
						"dateTime": "2019-12-22T06:22:49.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{D70F263B-7D0E-BB4B-9D72-A34529CAB4F1}",
						"dateTime": "2020-01-12T05:15:32.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{D7320D04-1AFB-5B45-AE54-BFC542A9E227}",
						"dateTime": "2020-01-09T01:06:48.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{D7BDB347-DE86-7740-9B76-45525216EE8C}",
						"dateTime": "2020-01-07T05:24:54.000Z",
						"operationPoints": [],
						"value": [
							53.7000007629395
						]
					},
					{
						"id": "{D7FCB0B8-501A-E94C-8674-718196EE56E4}",
						"dateTime": "2019-12-26T13:34:06.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{D8D10A68-4292-AC41-AB8F-F4F6019B569A}",
						"dateTime": "2020-01-02T05:43:58.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{DA5CF7D1-51FD-6241-9DF4-38BA03A31784}",
						"dateTime": "2019-12-14T01:12:58.000Z",
						"operationPoints": [],
						"value": [
							53.5
						]
					},
					{
						"id": "{DB0ACF5D-2CC2-DC4A-9543-4EEE82AD2F01}",
						"dateTime": "2019-12-20T13:15:26.000Z",
						"operationPoints": [],
						"value": [
							52.2999992370605
						]
					},
					{
						"id": "{DB16D142-0EB0-1246-A580-493E7F7AEDA0}",
						"dateTime": "2019-12-16T02:14:55.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{DD9B234B-8D0E-434C-876A-1ECB90BF5FD7}",
						"dateTime": "2020-01-03T13:24:08.000Z",
						"operationPoints": [],
						"value": [
							52.7000007629395
						]
					},
					{
						"id": "{DFA2699A-4C07-674C-8F46-72452A152948}",
						"dateTime": "2019-12-14T17:30:51.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{E09E6AED-A898-F140-B361-4002C37880DF}",
						"dateTime": "2020-01-08T09:22:13.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{E115EB21-F1C3-9C47-AC16-D10C6E491941}",
						"dateTime": "2019-12-04T17:28:02.000Z",
						"operationPoints": [],
						"value": [
							52.5
						]
					},
					{
						"id": "{E1195256-2DDF-9046-AB59-51D380022E90}",
						"dateTime": "2019-12-08T05:57:43.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{E1AB973A-226E-4348-A932-38870E77D135}",
						"dateTime": "2019-12-16T10:59:07.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{E54653BF-5CC4-9445-9D91-EE3F275378B9}",
						"dateTime": "2019-12-14T21:25:23.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{E5D8CC29-558F-DD45-A807-5A1190E1050F}",
						"dateTime": "2019-12-21T21:07:47.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{E7FDA762-4BA8-5D45-AB89-B86E167A84E9}",
						"dateTime": "2019-12-15T18:37:23.000Z",
						"operationPoints": [],
						"value": [
							47.2999992370605
						]
					},
					{
						"id": "{E874D026-4719-7349-A7BB-FB113573C8B8}",
						"dateTime": "2019-12-05T01:16:09.000Z",
						"operationPoints": [],
						"value": [
							53.5
						]
					},
					{
						"id": "{E8F05A86-351A-0E4E-A034-402FF997A28B}",
						"dateTime": "2020-01-08T01:06:34.000Z",
						"operationPoints": [],
						"value": [
							53.5
						]
					},
					{
						"id": "{E90EAC7B-864F-C840-B12E-E449C57C51CB}",
						"dateTime": "2020-01-05T09:03:43.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{EAD4D906-9250-8F4A-93AD-F9061CE0A6A6}",
						"dateTime": "2020-01-13T18:16:21.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{EB3CCF90-1D7C-5C49-8C59-EC9EBA59DB3F}",
						"dateTime": "2019-12-10T05:21:14.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{EB412678-6A52-E243-AEBB-AFF02D2DFF8F}",
						"dateTime": "2019-12-08T01:56:01.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{EB59A474-2710-BE4A-B4B9-63DD72111BE8}",
						"dateTime": "2020-01-10T15:00:32.000Z",
						"operationPoints": [],
						"value": [
							50
						]
					},
					{
						"id": "{EBEB03B7-3E5B-B947-A510-C8260FC684BC}",
						"dateTime": "2020-01-04T13:37:31.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{EC2D7E38-18A8-A84A-9184-0E51BB8C8DAA}",
						"dateTime": "2019-12-09T09:07:44.000Z",
						"operationPoints": [],
						"value": [
							52.9000015258789
						]
					},
					{
						"id": "{ED81B927-2256-EB48-B4D5-7E6186572FE9}",
						"dateTime": "2020-01-01T13:34:45.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{EE2B40BB-288D-D543-8EE7-C2A5D8AF500A}",
						"dateTime": "2019-12-05T13:32:17.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{F053948D-61AE-0E4F-9A99-E120482B081E}",
						"dateTime": "2019-12-25T22:18:34.000Z",
						"operationPoints": [],
						"value": [
							53.2000007629395
						]
					},
					{
						"id": "{F0D7AA8A-9BB3-D044-BAD8-B59624498821}",
						"dateTime": "2019-12-21T13:29:36.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{F610B072-CF98-324D-A9EA-9E94E9A82FF1}",
						"dateTime": "2019-12-06T01:24:47.000Z",
						"operationPoints": [],
						"value": [
							54
						]
					},
					{
						"id": "{F7D8F7EC-66F0-E64C-AA5B-D46A28236748}",
						"dateTime": "2019-12-29T16:37:18.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{F8F63F4D-E123-C449-8E14-BA0A778CA49E}",
						"dateTime": "2019-12-14T17:30:51.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{F8FCEDFB-F4A2-6C43-900B-34DD0DEDD39A}",
						"dateTime": "2019-12-15T21:51:10.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{F9B0D778-1609-CC47-A500-68F11ADC0EAF}",
						"dateTime": "2019-12-16T13:02:01.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{F9D9AD53-9C97-964A-A1DB-07CAEBF7F449}",
						"dateTime": "2019-12-30T21:10:32.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{FA22EFD8-C924-0948-AE32-B296AB29C42B}",
						"dateTime": "2020-01-04T09:27:08.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{FA2CD3E5-CC9A-6A40-89C8-A15654766857}",
						"dateTime": "2020-01-01T17:07:21.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{FA7193CD-98CE-7648-B91F-DA6B0F0A9024}",
						"dateTime": "2020-01-04T20:53:22.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{FE3E3C36-C58A-0049-8D57-526513626275}",
						"dateTime": "2019-12-30T01:16:48.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					},
					{
						"id": "{FEF04530-FCDE-7E4E-ABD9-75E959A0FAD1}",
						"dateTime": "2020-01-01T21:08:56.000Z",
						"operationPoints": [],
						"value": [
							52
						]
					},
					{
						"id": "{FF93511E-63DE-E34F-B17B-9E9C856A93E4}",
						"dateTime": "2020-01-02T21:21:34.000Z",
						"operationPoints": [],
						"value": [
							53
						]
					}
				]
			},			
			
		],
		"operationPoints": [
			{
				"id": "{9579F423-31D1-4CAB-95A4-AC9E52FDA5A9}",
				"idMonitoredPoint": "{52EA7F98-291A-4D48-BFBF-6F36113ED7BD}",
				"name": "TN-UG-QUEDA_SDSC"
			},
			{
				"id": "{9D834B91-C637-4F6C-82E3-6D75E181E496}",
				"idMonitoredPoint": "{C60CA818-3808-43FF-A2EA-7C49E50A0425}",
				"name": "TE-POT_AT_SDSC"
			}
		]
	}
}
```

**Exemplo no MDM:**\
[Análise sequencial](../images/AnaliseSequencial.jpg)\
