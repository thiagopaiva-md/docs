## Árvore de análise

**Objetivo:** Trazer para o EAMon toda a informação da árvore de análise do Sistema MDM, incluindo a estrutura de equipamentos, subsistemas, componentes e pontos monitorados.

**Nome da operação:** core_getMonitoredPointsTree

**Parâmetros de entrada:** 

Nome                     |  Tipo           | Opcional     | Descrição
:-----------------------:|:---------------:|:------------:|:------------
databaseAlias            | string         | Não           | O alias da base de dados utilizada no momento da chamada.
operation                | string         | Não           | core_getMonitoredPointsTree  

**JSON de exemplo - parâmetros de entrada:**
```
{
  "databaseAlias": "ILS",
  "operation": "core_getOilTankLevels",
}
```

## Saída

**Descrição dos parâmetros de saída em caso de sucesso, presentes no array de objetos "content":**

**Atenção:** A tabela abaixo descreve cada um dos objetos presentes no array.

**Primeiro nível no JSON:** Plantas

Nome               |  Tipo           | Descrição
:-----------------:|:---------------:|:-------------
id                 | string              | Id da planta
nome               | string              | Nome da planta
endereco           | string              | Endereço da planta
empresa            | string              | Nome da empresa
equipamentos       | object<Equipment>[] | Array de objetos equipamento desta planta, apresentado a seguir
  
**Segundo nível no JSON:** Equipamentos

Nome               |  Tipo           | Descrição
:-----------------:|:---------------:|:-------------
id                 | string              | Id da planta
idPlanta           | string              | Id da planta associada ao equipamento
idAnalisador       | string              | Id do analisador associado ao equipamento
idUnidadeAquisicao | string              | Id da unidade de aquisição associada ao equipamento
nome               | string              | Nome do equipamento
fabricante         | string              | Nome do fabricante
modelo             | string              | Modelo do equipamento
descricao          | string              | Descricao do equipamento
localizacao        | string              | Localização do equipamento
nroSerie           | string              | Número de série do equipamento
tipoEquipamento    | integer             | Numeral do tipo de equipamento
subsistemas        | object<Subsystem>[] | Array de objetos subsistema deste equipamento, apresentado a seguir
  
**Terceiro nível no JSON:** Subsistemas

Nome               |  Tipo           | Descrição
:-----------------:|:---------------:|:-------------
id                 | string              | Id do subsistema
idEquipamento      | string              | Id do equipamento associado ao subsistema
nome               | string              | Nome do subsistema
descricao          | string              | Descrição do subsistema
componentes        | object<Component>[] | Array de objetos componente deste subsistema, apresentado a seguir
  
**Terceiro nível no JSON:** Componentes

Nome               |  Tipo           | Descrição
:-----------------:|:---------------:|:-------------
id                 | string                   | Id do subsistema
idSubsistema       | string                   | Id do subsistema associado ao componente
nome               | string                   | Nome do componente
descricao          | string                   | Descrição do componente
pontosMonitorados  | object<MonitoredPoint>[] | Array de objetos pontos monitorados deste componente, apresentado a seguir
  
**Quarto nível no JSON:** Pontos Monitorados

Nome                     |  Tipo           | Descrição
:-----------------------:|:---------------:|:-------------
id                       | string                   | Id do ponto monitorado
idCanal                  | string                   | Id do canal associado ao ponto monitorado
idTipoSensor             | string                   | Id do Tipo Sensor associado ao ponto monitorado
idPlanoMedicao           | string                   | Id do plano de medição associado ao ponto monitorado
idComponente             | string                   | Id do componente associado ao ponto monitorado
idGrupoPontosMonitorados | string                   | Id do grupo de pontos associado ao ponto monitorado
nome                     | string                   | Nome do ponto monitorado
descricao                | string                   | Descrição do ponto monitorado
localizacao              | string                   | Localização do ponto monitorado
direcao                  | integer                  | Direção do ponto monitorado em graus (0, 90, 180, 270)
ativo                    | integer                  | Indica se o ponto está ativo (0 ou 1)
tipoSensor               | object<SensorType>[]     | Array de objetos tipo sensor deste ponto monitorado, apresentado a seguir
  
**Quinto nível no JSON:** Tipo Sensor
  
Nome               |  Tipo           | Descrição
:-----------------:|:---------------:|:-------------
id                 | string                   | Id do tipo sensor
nome               | string                   | Nome do tipo sensor
unidadeStr         | string                   | Unidade de medição do tipo sensor em string
unidade            | string                   | Unidade de medição do tipo sensor em numérico
tipoSensor         | integer                  | Tipo do transdutor
taxaAmostragem     | integer                  | Taxa de amostragem do sensor
nroAmostras        | string                   | Número de amostras do sensor
  
**JSON de exemplo - parâmetros de saída**
  
```
{
	"status": 200,
	"content": [
		{
			"id": "{B751541E-6D27-4D30-B9E6-FB05E4E193E7}",
			"nome": "Demo",
			"endereco": null,
			"empresa": null,
			"equipamentos": [
				{
					"id": "{1E244B3D-6CA2-42F8-A344-3ABD3632157D}",
					"idPlanta": "{B751541E-6D27-4D30-B9E6-FB05E4E193E7}",
					"idAnalisador": null,
					"idUnidadeAquisicao": "{0A862223-C063-42FE-AF21-F3EBE6B40E7C}",
					"nome": "Protótipo",
					"fabricante": "",
					"modelo": "",
					"descricao": "",
					"localizacao": 2001,
					"nroSerie": "",
					"tipoEquipamento": 68009,
					"subsistemas": [
						{
							"id": "{8814BBA5-C22E-45D2-9261-97F1B08DB967}",
							"idEquipamento": "{1E244B3D-6CA2-42F8-A344-3ABD3632157D}",
							"nome": "Mancais",
							"descricao": "",
							"componentes": [
								{
									"id": "{B2A82CA4-E08F-41CC-9135-6AB65A7037FE}",
									"idSubsistema": "{8814BBA5-C22E-45D2-9261-97F1B08DB967}",
									"nome": "Lado Acoplamento",
									"descricao": "",
									"pontosMonitorados": [
										{
											"id": "{3EEBFCC5-2634-46F8-BF15-3E8C151E943D}",
											"idCanal": "{C830FA66-7C14-41A3-A6E0-AF9A185D0EC8}",
											"idTipoSensor": "{2BC94B62-4F8E-43D7-8F64-64060EFC23DC}",
											"idPlanoMedicao": null,
											"idComponente": "{B2A82CA4-E08F-41CC-9135-6AB65A7037FE}",
											"idGrupoPontosMonitorados": null,
											"nome": "SA-LA-000",
											"descricao": "",
											"localizacao": "",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "mm/s²",
												"id": "{2BC94B62-4F8E-43D7-8F64-64060EFC23DC}",
												"nome": "Acelerometro baixa",
												"tipoSensor": 4001,
												"unidade": 69080,
												"taxaAmostragem": 2000,
												"nroAmostras": 4096
											}
										}
									]
								},
								{
									"id": "{336F3F2C-2E3D-4B90-AB62-ABF8A0A624BB}",
									"idSubsistema": "{8814BBA5-C22E-45D2-9261-97F1B08DB967}",
									"nome": "Lado Oposto",
									"descricao": "",
									"pontosMonitorados": [
										{
											"id": "{897EC672-B108-4E9F-9049-7963B64043AA}",
											"idCanal": "{C830FA66-7C14-41A3-A6E0-AF9A185D0EC8}",
											"idTipoSensor": "{C83CC460-7777-4377-B16E-09DBD9725D23}",
											"idPlanoMedicao": "{24235ADB-D41D-4E5E-BFA3-64EB82FC02E9}",
											"idComponente": "{336F3F2C-2E3D-4B90-AB62-ABF8A0A624BB}",
											"idGrupoPontosMonitorados": null,
											"nome": "SD-LO-000",
											"descricao": "",
											"localizacao": "",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "µm",
												"id": "{C83CC460-7777-4377-B16E-09DBD9725D23}",
												"nome": "deslocamento",
												"tipoSensor": 4000,
												"unidade": 69004,
												"taxaAmostragem": 2000,
												"nroAmostras": 4096
											}
										},
										{
											"id": "{91186FC2-C873-4031-8C08-0A4FF35C61EB}",
											"idCanal": "{10515ABC-C159-4DEC-AB35-82D2337E0B9B}",
											"idTipoSensor": "{C83CC460-7777-4377-B16E-09DBD9725D23}",
											"idPlanoMedicao": "{24235ADB-D41D-4E5E-BFA3-64EB82FC02E9}",
											"idComponente": "{336F3F2C-2E3D-4B90-AB62-ABF8A0A624BB}",
											"idGrupoPontosMonitorados": null,
											"nome": "SD-LO-090",
											"descricao": "",
											"localizacao": "",
											"direcao": 90,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "µm",
												"id": "{C83CC460-7777-4377-B16E-09DBD9725D23}",
												"nome": "deslocamento",
												"tipoSensor": 4000,
												"unidade": 69004,
												"taxaAmostragem": 2000,
												"nroAmostras": 4096
											}
										}
									]
								}
							]
						},
						{
							"id": "{5D8F2087-FD56-454D-91BE-3DB12AAAAC80}",
							"idEquipamento": "{1E244B3D-6CA2-42F8-A344-3ABD3632157D}",
							"nome": "Sistema de Controle",
							"descricao": "",
							"componentes": [
								{
									"id": "{BB634B01-5F72-4B2E-82AF-9FC5D42DBCBC}",
									"idSubsistema": "{5D8F2087-FD56-454D-91BE-3DB12AAAAC80}",
									"nome": "RV",
									"descricao": "",
									"pontosMonitorados": [
										{
											"id": "{464C75F3-CBCA-4C24-A379-6CEC8E859F40}",
											"idCanal": "{FC396ECD-519C-4736-89ED-5FFBD0DBE4B2}",
											"idTipoSensor": "{1369BBE5-0723-439D-B0CE-BFB44DF03703}",
											"idPlanoMedicao": null,
											"idComponente": "{BB634B01-5F72-4B2E-82AF-9FC5D42DBCBC}",
											"idGrupoPontosMonitorados": null,
											"nome": "Rotação",
											"descricao": "",
											"localizacao": "",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{1369BBE5-0723-439D-B0CE-BFB44DF03703}",
												"nome": "RVDT",
												"tipoSensor": 4017,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						}
					]
				},
				{
					"id": "{70674D65-25BA-464F-B60C-879087990E61}",
					"idPlanta": "{B751541E-6D27-4D30-B9E6-FB05E4E193E7}",
					"idAnalisador": null,
					"idUnidadeAquisicao": null,
					"nome": "UG1",
					"fabricante": "x",
					"modelo": "",
					"descricao": "",
					"localizacao": 0,
					"nroSerie": "",
					"tipoEquipamento": 68000,
					"subsistemas": [
						{
							"id": "{62BA8438-7A6D-446B-B914-6A6E133069EA}",
							"idEquipamento": "{70674D65-25BA-464F-B60C-879087990E61}",
							"nome": "Circulação Óleo ME",
							"descricao": "Subsistema de circulação de óleo do mancal de escora - ME",
							"componentes": [
								{
									"id": "{4255F59B-9489-453C-B899-0DC3546FF325}",
									"idSubsistema": "{62BA8438-7A6D-446B-B914-6A6E133069EA}",
									"nome": "Bomba",
									"descricao": "Bomba",
									"pontosMonitorados": [
										{
											"id": "{2A083FFA-5281-49A1-8E7E-6DA3D98F47F5}",
											"idCanal": null,
											"idTipoSensor": "{D8718BC9-CAA3-4EFE-ABF7-D9E166D8EBFD}",
											"idPlanoMedicao": null,
											"idComponente": "{4255F59B-9489-453C-B899-0DC3546FF325}",
											"idGrupoPontosMonitorados": null,
											"nome": "TL-ME-B1PRINC",
											"descricao": "44 - Bomba 1 ME  Ligada (1), Desligada(0)",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "m",
												"id": "{D8718BC9-CAA3-4EFE-ABF7-D9E166D8EBFD}",
												"nome": "Lógico",
												"tipoSensor": 4011,
												"unidade": 69001,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{07335986-5796-44AE-B2DE-368130F09A2A}",
											"idCanal": null,
											"idTipoSensor": "{D8718BC9-CAA3-4EFE-ABF7-D9E166D8EBFD}",
											"idPlanoMedicao": null,
											"idComponente": "{4255F59B-9489-453C-B899-0DC3546FF325}",
											"idGrupoPontosMonitorados": null,
											"nome": "TL-ME-B2PRINC",
											"descricao": "45 - Bomba 2 ME  Ligada (1), Desligada(0)",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "m",
												"id": "{D8718BC9-CAA3-4EFE-ABF7-D9E166D8EBFD}",
												"nome": "Lógico",
												"tipoSensor": 4011,
												"unidade": 69001,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{109C2387-7F86-4AAC-BAE7-841000D35AFD}",
											"idCanal": null,
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{4255F59B-9489-453C-B899-0DC3546FF325}",
											"idGrupoPontosMonitorados": null,
											"nome": "TP-ME-BB",
											"descricao": "46 - Pressão Bomba Óleo do ME",
											"localizacao": "Bomba ME",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{F2796E68-DDE6-4C15-A2F7-920D8A8BC493}",
									"idSubsistema": "{62BA8438-7A6D-446B-B914-6A6E133069EA}",
									"nome": "Filtro",
									"descricao": "Filtro",
									"pontosMonitorados": [
										{
											"id": "{80F18426-F5E5-416D-935D-D3735606FBE9}",
											"idCanal": null,
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{F2796E68-DDE6-4C15-A2F7-920D8A8BC493}",
											"idGrupoPontosMonitorados": null,
											"nome": "TP-ME-OL_ANTES",
											"descricao": "47 - Pressão de óleo antes do filtro",
											"localizacao": "ME",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{D217E132-97C9-4150-98B9-525EABAFAECC}",
											"idCanal": null,
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{F2796E68-DDE6-4C15-A2F7-920D8A8BC493}",
											"idGrupoPontosMonitorados": null,
											"nome": "TP-ME-OL_DEPOIS",
											"descricao": "48 - Pressão de óleo depois do filtro",
											"localizacao": "ME",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{42150B9D-F397-4027-B518-71130C2D4921}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F2796E68-DDE6-4C15-A2F7-920D8A8BC493}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-ME-AG_ANTES",
											"descricao": "52 - Temp Agua antes do Trocador de Calor",
											"localizacao": "Filtro ME",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{AF9A71A5-909B-423D-983D-44F29B44AEE3}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F2796E68-DDE6-4C15-A2F7-920D8A8BC493}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-ME-AG_DEPOIS",
											"descricao": "53 - Temp Agua depois do Trocador de calor.",
											"localizacao": "FILTRO ME",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{E5F46119-3138-4299-BA45-2C710FBDDA37}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F2796E68-DDE6-4C15-A2F7-920D8A8BC493}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-ME-OL_ANTES",
											"descricao": "51 - Temp Oleo antes do Trocador de Calor",
											"localizacao": "Filtro ME",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{79C49330-A2E8-48EC-8155-93F841028A7E}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F2796E68-DDE6-4C15-A2F7-920D8A8BC493}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-ME-OL_DEPOIS",
											"descricao": "49 - Temp Oleo depois dos  filtros do Mancal de Escora.",
											"localizacao": "Filtro RV",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{16C80D11-6000-4E27-B6CD-E14B29A50EEB}",
									"idSubsistema": "{62BA8438-7A6D-446B-B914-6A6E133069EA}",
									"nome": "Tanque",
									"descricao": "Tanque externo de óleo",
									"pontosMonitorados": [
										{
											"id": "{D0844D5C-054B-4556-BF4E-1FC6ACD69EC8}",
											"idCanal": null,
											"idTipoSensor": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
											"idPlanoMedicao": null,
											"idComponente": "{16C80D11-6000-4E27-B6CD-E14B29A50EEB}",
											"idGrupoPontosMonitorados": "{68EB6FF8-55A9-4404-854C-11D0C6B2BBC8}",
											"nome": "TN-ME-OL_TANQEXT",
											"descricao": "50 -  Nivel Oleo ME Tanque Externo 0 - Baixo; 1 - Normal; 2 - Alto",
											"localizacao": "ME",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "mm",
												"id": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
												"nome": "Transdutor de Nivel (mm)",
												"tipoSensor": 4007,
												"unidade": 69003,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						},
						{
							"id": "{9B7ABD59-CC15-4244-9E4E-49CE13C38B2B}",
							"idEquipamento": "{70674D65-25BA-464F-B60C-879087990E61}",
							"nome": "Gerador Eletrico",
							"descricao": "Gerador Eletrico",
							"componentes": [
								{
									"id": "{B0FD25A4-7884-4481-A99F-FCF460ED82F4}",
									"idSubsistema": "{9B7ABD59-CC15-4244-9E4E-49CE13C38B2B}",
									"nome": "Enrolamento do Estator",
									"descricao": "Enrolamento do estator do gerador",
									"pontosMonitorados": [
										{
											"id": "{7C15EAD7-7B0A-4117-9947-B5090A57AC19}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{B0FD25A4-7884-4481-A99F-FCF460ED82F4}",
											"idGrupoPontosMonitorados": "{26D3510D-2E50-4A91-B7AC-F97C1F97DFBD}",
											"nome": "TT-GER-CO01",
											"descricao": "78 - GP Cobre 1 (TUG7)",
											"localizacao": "Enrolamento Estator",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{ACAA8199-DDCB-42CF-83D1-856CF4391087}",
									"idSubsistema": "{9B7ABD59-CC15-4244-9E4E-49CE13C38B2B}",
									"nome": "Núcleo do Estator",
									"descricao": "Núcleo do estator do gerador",
									"pontosMonitorados": [
										{
											"id": "{27992461-4A33-4DBE-AC22-F7F726C09E70}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{ACAA8199-DDCB-42CF-83D1-856CF4391087}",
											"idGrupoPontosMonitorados": "{26D3510D-2E50-4A91-B7AC-F97C1F97DFBD}",
											"nome": "TT-GER-AUX-CO02",
											"descricao": "81 - GA COBRE 2 (TUG 11)",
											"localizacao": "Núcleo do Estator",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{B5B86249-A103-4EF7-BF0B-7CEB2BF8DFD6}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{ACAA8199-DDCB-42CF-83D1-856CF4391087}",
											"idGrupoPontosMonitorados": "{26D3510D-2E50-4A91-B7AC-F97C1F97DFBD}",
											"nome": "TT-GER-CO02",
											"descricao": "81 - GA Cobre 2 (TUG11)",
											"localizacao": "Estator",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{51094F25-4E69-4195-B09B-F30044E276B6}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{ACAA8199-DDCB-42CF-83D1-856CF4391087}",
											"idGrupoPontosMonitorados": "{3F228924-77F6-41FD-B1DC-25B5DB9B43A1}",
											"nome": "TT-GER-FE01",
											"descricao": "79 -  GP Ferro 1 (TUG9)",
											"localizacao": "Estator",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{2D65167B-2D3B-401B-AB2A-99ABE78F2C53}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{ACAA8199-DDCB-42CF-83D1-856CF4391087}",
											"idGrupoPontosMonitorados": "{3F228924-77F6-41FD-B1DC-25B5DB9B43A1}",
											"nome": "TT-GER-FE04",
											"descricao": "80 - GP Ferro 4 (TUG10)",
											"localizacao": "Nucleo Estator",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{7E4C269B-98A6-4C86-B4F7-8D5211F9B6C7}",
									"idSubsistema": "{9B7ABD59-CC15-4244-9E4E-49CE13C38B2B}",
									"nome": "Sistema de Frenagem",
									"descricao": "Sistema de Frenagem",
									"pontosMonitorados": [
										{
											"id": "{6CA324DA-F820-4E6F-ACE3-D2F5302F1F1B}",
											"idCanal": null,
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{7E4C269B-98A6-4C86-B4F7-8D5211F9B6C7}",
											"idGrupoPontosMonitorados": null,
											"nome": "TP-RV-AR_FRENAG",
											"descricao": "17 - Pressao Ar de Frenagem",
											"localizacao": "Sistema Frenagem Gerador",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						},
						{
							"id": "{DFAA154F-06D5-4614-879A-E3F94E7606D3}",
							"idEquipamento": "{70674D65-25BA-464F-B60C-879087990E61}",
							"nome": "ME",
							"descricao": "Mancal de escora",
							"componentes": [
								{
									"id": "{9797AE42-2C4C-4267-82EC-B9CBCF928361}",
									"idSubsistema": "{DFAA154F-06D5-4614-879A-E3F94E7606D3}",
									"nome": "Cuba",
									"descricao": "Cuba de óleo do mancal de escora",
									"pontosMonitorados": [
										{
											"id": "{ACB491BD-4FAB-466A-8F23-60DB06BF98A6}",
											"idCanal": null,
											"idTipoSensor": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
											"idPlanoMedicao": null,
											"idComponente": "{9797AE42-2C4C-4267-82EC-B9CBCF928361}",
											"idGrupoPontosMonitorados": "{730806AC-50FA-457B-8F05-0BC57E602B5A}",
											"nome": "TN-ME-OLEO",
											"descricao": "71 - Nível Óleo ME Cuba",
											"localizacao": "Cuba",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "mm",
												"id": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
												"nome": "Transdutor de Nivel (mm)",
												"tipoSensor": 4007,
												"unidade": 69003,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{E5DE1260-7F20-4013-8077-9EDA042CD6EA}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{9797AE42-2C4C-4267-82EC-B9CBCF928361}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-ME-OL_FRIO",
											"descricao": "36 - Temp Oleo Frio (TC10) ",
											"localizacao": "ME Saida do TC",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{72956FA4-C036-446C-AA83-60F9A6D064C8}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{9797AE42-2C4C-4267-82EC-B9CBCF928361}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-ME-OL_QUENTE1",
											"descricao": "37 - Oleo Quente ME 1 (TC08)",
											"localizacao": "ME",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{59568331-03CF-43AD-AB54-75A6B483B31B}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{9797AE42-2C4C-4267-82EC-B9CBCF928361}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-ME-OL_QUENTE2",
											"descricao": "38 - Oleo Quente ME 2 (TC09)",
											"localizacao": "ME",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{74FF0133-D8F4-465D-824F-8909747B2DCD}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{9797AE42-2C4C-4267-82EC-B9CBCF928361}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-ME-OLEO",
											"descricao": "84 - ME ÓLEO (TUG14)",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{A341AEF2-C52A-464A-9030-4F7DD529285C}",
									"idSubsistema": "{DFAA154F-06D5-4614-879A-E3F94E7606D3}",
									"nome": "Segmentos",
									"descricao": "Segmentos",
									"pontosMonitorados": [
										{
											"id": "{6BECAB3B-1FAA-437C-999A-579F0FFDD571}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{A341AEF2-C52A-464A-9030-4F7DD529285C}",
											"idGrupoPontosMonitorados": "{08470672-FF9A-4F60-985A-5F15DD2EC877}",
											"nome": "TT-ME-SEG01",
											"descricao": "39 - Temp Ponto 1 ME (TC06) ",
											"localizacao": "???",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{5A44A74C-6A11-4911-A02B-68BDFF2BC9DD}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{A341AEF2-C52A-464A-9030-4F7DD529285C}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-ME-SEG01_TUG",
											"descricao": "72 - ME SEG 1 (TUG1)",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{E4899362-D8DF-46DD-AE95-76953C2014B3}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{A341AEF2-C52A-464A-9030-4F7DD529285C}",
											"idGrupoPontosMonitorados": "{08470672-FF9A-4F60-985A-5F15DD2EC877}",
											"nome": "TT-ME-SEG02",
											"descricao": "40 - Temp Ponto 2 ME (TC07)",
											"localizacao": "???",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{D4A47148-BE69-4B1E-8E2C-3940CED879BE}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{A341AEF2-C52A-464A-9030-4F7DD529285C}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-ME-SEG08",
											"descricao": "73 - ME SEG 8 (TUG2)",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						},
						{
							"id": "{63D4C03B-A1A8-4775-AB7A-AEC80E24B647}",
							"idEquipamento": "{70674D65-25BA-464F-B60C-879087990E61}",
							"nome": "MGG",
							"descricao": "Mancal de guia do gerador",
							"componentes": [
								{
									"id": "{4B88A044-76BE-45A3-82FE-854227DC7884}",
									"idSubsistema": "{63D4C03B-A1A8-4775-AB7A-AEC80E24B647}",
									"nome": "Cuba",
									"descricao": "Cuba",
									"pontosMonitorados": [
										{
											"id": "{E86C1248-C458-44A9-B28F-310C43D89449}",
											"idCanal": null,
											"idTipoSensor": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
											"idPlanoMedicao": null,
											"idComponente": "{4B88A044-76BE-45A3-82FE-854227DC7884}",
											"idGrupoPontosMonitorados": "{1043F68A-9935-4FD6-BD54-6418F5A69A30}",
											"nome": "TN-MGG-OLEO",
											"descricao": "70 - Nível Óleo MGG",
											"localizacao": "Cuba",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "mm",
												"id": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
												"nome": "Transdutor de Nivel (mm)",
												"tipoSensor": 4007,
												"unidade": 69003,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{B01557F5-F8CC-43A0-BA52-315D8534BC83}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{4B88A044-76BE-45A3-82FE-854227DC7884}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-MGG-OLEO_TUG",
											"descricao": "86 - MGG ÓLEO (TUG16)",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{7C6F7B8E-F05D-41C2-B212-D33353925835}",
									"idSubsistema": "{63D4C03B-A1A8-4775-AB7A-AEC80E24B647}",
									"nome": "Eixo",
									"descricao": "Eixo",
									"pontosMonitorados": [
										{
											"id": "{D8B17CCF-D490-4649-B545-3826D8BB4398}",
											"idCanal": "{DF00F3D6-2ECE-4DDE-8788-1C6C34FE04FB}",
											"idTipoSensor": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
											"idPlanoMedicao": null,
											"idComponente": "{7C6F7B8E-F05D-41C2-B212-D33353925835}",
											"idGrupoPontosMonitorados": null,
											"nome": "FASOR-X",
											"descricao": null,
											"localizacao": "Acima do mancal",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "µm",
												"id": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
												"nome": "Proximidade",
												"tipoSensor": 4000,
												"unidade": 69004,
												"taxaAmostragem": 125,
												"nroAmostras": 4096
											}
										},
										{
											"id": "{F7D916E6-0585-4EF2-A00C-4B69911EB0B6}",
											"idCanal": "{C830FA66-7C14-41A3-A6E0-AF9A185D0EC8}",
											"idTipoSensor": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
											"idPlanoMedicao": "{8C6948F9-9672-487E-859D-C928CF5FB450}",
											"idComponente": "{7C6F7B8E-F05D-41C2-B212-D33353925835}",
											"idGrupoPontosMonitorados": "{336D5296-A2EC-453C-B10F-C802DC857DD6}",
											"nome": "SD1-MGG-000R-X",
											"descricao": "",
											"localizacao": "Suporte esp no mancal",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "µm",
												"id": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
												"nome": "Proximidade",
												"tipoSensor": 4000,
												"unidade": 69004,
												"taxaAmostragem": 125,
												"nroAmostras": 4096
											}
										},
										{
											"id": "{A99DB7C5-8CBC-46CF-99F9-A6BF561F85A0}",
											"idCanal": "{10515ABC-C159-4DEC-AB35-82D2337E0B9B}",
											"idTipoSensor": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
											"idPlanoMedicao": "{8C6948F9-9672-487E-859D-C928CF5FB450}",
											"idComponente": "{7C6F7B8E-F05D-41C2-B212-D33353925835}",
											"idGrupoPontosMonitorados": "{336D5296-A2EC-453C-B10F-C802DC857DD6}",
											"nome": "SD1-MGG-090R-Y",
											"descricao": "",
											"localizacao": "Suporte esp no mancal",
											"direcao": 90,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "µm",
												"id": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
												"nome": "Proximidade",
												"tipoSensor": 4000,
												"unidade": 69004,
												"taxaAmostragem": 125,
												"nroAmostras": 4096
											}
										}
									]
								},
								{
									"id": "{BE38785A-26CC-4F32-8410-544B1EAE9733}",
									"idSubsistema": "{63D4C03B-A1A8-4775-AB7A-AEC80E24B647}",
									"nome": "Segmentos",
									"descricao": "Segmentos",
									"pontosMonitorados": [
										{
											"id": "{30625D26-D3F2-4C76-997C-A212FBD9891B}",
											"idCanal": null,
											"idTipoSensor": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
											"idPlanoMedicao": null,
											"idComponente": "{BE38785A-26CC-4F32-8410-544B1EAE9733}",
											"idGrupoPontosMonitorados": "{336D5296-A2EC-453C-B10F-C802DC857DD6}",
											"nome": "Cópia de SD1-MGG-000R-X",
											"descricao": "",
											"localizacao": "Suporte esp no mancal",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "µm",
												"id": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
												"nome": "Proximidade",
												"tipoSensor": 4000,
												"unidade": 69004,
												"taxaAmostragem": 125,
												"nroAmostras": 4096
											}
										},
										{
											"id": "{69EE6460-2EE0-43D6-B887-16891B8C4186}",
											"idCanal": null,
											"idTipoSensor": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
											"idPlanoMedicao": null,
											"idComponente": "{BE38785A-26CC-4F32-8410-544B1EAE9733}",
											"idGrupoPontosMonitorados": "{336D5296-A2EC-453C-B10F-C802DC857DD6}",
											"nome": "Cópia de SD1-MGG-090R-Y",
											"descricao": "",
											"localizacao": "Suporte esp no mancal",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "µm",
												"id": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
												"nome": "Proximidade",
												"tipoSensor": 4000,
												"unidade": 69004,
												"taxaAmostragem": 125,
												"nroAmostras": 4096
											}
										},
										{
											"id": "{F4ED2A37-8EB8-4437-BB3F-D6B344374856}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{BE38785A-26CC-4F32-8410-544B1EAE9733}",
											"idGrupoPontosMonitorados": "{AED653F3-E111-41F7-BA67-09C40B63D62C}",
											"nome": "TT-MGG-OLEO",
											"descricao": "35 - Temp Oleo MGG (TC5)",
											"localizacao": "Cuba MGG",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{B0166252-AFF2-441D-AB22-0E2928302766}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{BE38785A-26CC-4F32-8410-544B1EAE9733}",
											"idGrupoPontosMonitorados": "{0F0C5523-B7E8-4817-A580-F6EEC5C84ED8}",
											"nome": "TT-MGG-SEG01",
											"descricao": "31 - Temp SEG 1 (TC1)",
											"localizacao": "?????",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{6EFB552A-F63F-4B51-ACA3-96A6A2D12D6F}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{BE38785A-26CC-4F32-8410-544B1EAE9733}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-MGG-SEG01_TUG",
											"descricao": "74 - MGG SEG 1 (TUG3)",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{D18C40C5-B20E-45E9-8B63-A511319FD77B}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{BE38785A-26CC-4F32-8410-544B1EAE9733}",
											"idGrupoPontosMonitorados": "{0F0C5523-B7E8-4817-A580-F6EEC5C84ED8}",
											"nome": "TT-MGG-SEG02",
											"descricao": "32 - Temp SEG 2 (TC2)",
											"localizacao": "????",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{9A966007-EAE3-40DC-8B0C-F37D45D3E8F1}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{BE38785A-26CC-4F32-8410-544B1EAE9733}",
											"idGrupoPontosMonitorados": "{0F0C5523-B7E8-4817-A580-F6EEC5C84ED8}",
											"nome": "TT-MGG-SEG03",
											"descricao": "33 - Temp SEG 3 (TC3)",
											"localizacao": "????",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{07678450-62AF-4619-866E-500F31A4553F}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{BE38785A-26CC-4F32-8410-544B1EAE9733}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-MGG-SEG03_TUG",
											"descricao": "75 - MGG SEG 3 (TUG4)",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{3B0D048E-F116-4DDB-976F-45664620C7F1}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{BE38785A-26CC-4F32-8410-544B1EAE9733}",
											"idGrupoPontosMonitorados": "{0F0C5523-B7E8-4817-A580-F6EEC5C84ED8}",
											"nome": "TT-MGG-SEG04",
											"descricao": "34 - Temp SEG 4 (TC4)",
											"localizacao": "?????",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						},
						{
							"id": "{1D184865-DA44-41A0-B8F5-0D9E9A5FF2DE}",
							"idEquipamento": "{70674D65-25BA-464F-B60C-879087990E61}",
							"nome": "MGT",
							"descricao": "Mancal de guia da turbina",
							"componentes": [
								{
									"id": "{11AB191A-F8E1-4AFC-A00E-6D1B1A0D1E07}",
									"idSubsistema": "{1D184865-DA44-41A0-B8F5-0D9E9A5FF2DE}",
									"nome": "Cuba",
									"descricao": "Cuba de óleo do mancal guia da turbina",
									"pontosMonitorados": [
										{
											"id": "{1F786FF1-5E66-40AE-9464-7CEF48798689}",
											"idCanal": null,
											"idTipoSensor": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
											"idPlanoMedicao": null,
											"idComponente": "{11AB191A-F8E1-4AFC-A00E-6D1B1A0D1E07}",
											"idGrupoPontosMonitorados": "{2ECF3E3E-759F-4846-AB8D-F17E117FEF6F}",
											"nome": "TN-MGT-OLEO",
											"descricao": "69 - Nível Óleo MGT",
											"localizacao": "Cuba",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "mm",
												"id": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
												"nome": "Transdutor de Nivel (mm)",
												"tipoSensor": 4007,
												"unidade": 69003,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{FC23A2EC-2986-490D-BE5E-30CCF3F0968E}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{11AB191A-F8E1-4AFC-A00E-6D1B1A0D1E07}",
											"idGrupoPontosMonitorados": "{75F68571-F5F4-4D0F-AE86-98EF0C81B5D5}",
											"nome": "TT-MGT-OLEO",
											"descricao": "28 - Temp Oleo MGT",
											"localizacao": "MGT",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{7630116E-2D0F-4518-BFB7-BCFB179BFAC0}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{11AB191A-F8E1-4AFC-A00E-6D1B1A0D1E07}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-MGT-OLEO_TUG",
											"descricao": "85 - MGT ÓLEO (TUG15)",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{C76892BD-0DF1-4A56-879A-1752E37C11C7}",
									"idSubsistema": "{1D184865-DA44-41A0-B8F5-0D9E9A5FF2DE}",
									"nome": "Eixo",
									"descricao": "Eixo",
									"pontosMonitorados": [
										{
											"id": "{4C87CD1E-31EC-43F4-856D-880C8391B89A}",
											"idCanal": "{4EC95CF6-1D8A-42AF-821D-F799D026F965}",
											"idTipoSensor": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
											"idPlanoMedicao": "{D100DB9B-D187-45F7-9707-94F763F73546}",
											"idComponente": "{C76892BD-0DF1-4A56-879A-1752E37C11C7}",
											"idGrupoPontosMonitorados": "{7917DE49-2AFD-4FA4-AA42-D134337BE99F}",
											"nome": "SD3-MGT-000R-X",
											"descricao": "",
											"localizacao": "Suporte esp no mancal",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "µm",
												"id": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
												"nome": "Proximidade",
												"tipoSensor": 4000,
												"unidade": 69004,
												"taxaAmostragem": 125,
												"nroAmostras": 4096
											}
										},
										{
											"id": "{46D8C0C0-F26A-499D-BE64-EA4F253799DB}",
											"idCanal": "{79A672B7-4E85-46AE-AA11-4E798BC5DFB3}",
											"idTipoSensor": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
											"idPlanoMedicao": "{D100DB9B-D187-45F7-9707-94F763F73546}",
											"idComponente": "{C76892BD-0DF1-4A56-879A-1752E37C11C7}",
											"idGrupoPontosMonitorados": "{7917DE49-2AFD-4FA4-AA42-D134337BE99F}",
											"nome": "SD3-MGT-090R-Y",
											"descricao": "",
											"localizacao": "Suporte esp no mancal",
											"direcao": 90,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "µm",
												"id": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
												"nome": "Proximidade",
												"tipoSensor": 4000,
												"unidade": 69004,
												"taxaAmostragem": 125,
												"nroAmostras": 4096
											}
										},
										{
											"id": "{E7B4BF52-913D-4F76-8733-57C61F63B290}",
											"idCanal": "{8A439A71-65B8-49D9-BD0B-C4BB9A50CE71}",
											"idTipoSensor": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
											"idPlanoMedicao": null,
											"idComponente": "{C76892BD-0DF1-4A56-879A-1752E37C11C7}",
											"idGrupoPontosMonitorados": "{1D8BDF94-7C3B-4BC9-B82C-57943173C1AB}",
											"nome": "SD4-MGT-AX",
											"descricao": null,
											"localizacao": "Suporte esp próximo ao  MGT",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "µm",
												"id": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
												"nome": "Proximidade",
												"tipoSensor": 4000,
												"unidade": 69004,
												"taxaAmostragem": 125,
												"nroAmostras": 4096
											}
										}
									]
								},
								{
									"id": "{F10D9DE7-F0C1-42CC-B742-CBAA922A3DFA}",
									"idSubsistema": "{1D184865-DA44-41A0-B8F5-0D9E9A5FF2DE}",
									"nome": "Segmentos",
									"descricao": "Segmentos",
									"pontosMonitorados": [
										{
											"id": "{B7D93607-502E-4055-B7BC-E355576C4297}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F10D9DE7-F0C1-42CC-B742-CBAA922A3DFA}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-MGT-SEG01",
											"descricao": "76 - MGT SEG 1 (TUG5)",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{58921FE6-F7F4-4F24-AC43-72E83245D311}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F10D9DE7-F0C1-42CC-B742-CBAA922A3DFA}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-MGT-SEG03",
											"descricao": "77 - MGT SEG 3 (TUG6)",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{73218240-AC25-41DF-A4DB-4C4FF34F85A9}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F10D9DE7-F0C1-42CC-B742-CBAA922A3DFA}",
											"idGrupoPontosMonitorados": "{557FEA5D-BF59-4293-8F1D-31D262C3FCFA}",
											"nome": "TT-MGT-SEG04",
											"descricao": "27 - Temp MGT Segmento 04 (TC14)",
											"localizacao": "Segmento 04",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{6C4D751F-8EF4-43EE-8125-24547477E0B9}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F10D9DE7-F0C1-42CC-B742-CBAA922A3DFA}",
											"idGrupoPontosMonitorados": "{557FEA5D-BF59-4293-8F1D-31D262C3FCFA}",
											"nome": "TT-MGT-SEG10",
											"descricao": "26 - Temp MGT Segmento 10 (TC13)",
											"localizacao": "Segmento 10",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						},
						{
							"id": "{A4E81FD9-6F23-4FD0-9345-FCA4050184C3}",
							"idEquipamento": "{70674D65-25BA-464F-B60C-879087990E61}",
							"nome": "Regulador Velocidade",
							"descricao": "Subsistema do regulador de velocidade",
							"componentes": [
								{
									"id": "{68A4F7C6-5AF8-40AF-A4B6-80D1E6D7A391}",
									"idSubsistema": "{A4E81FD9-6F23-4FD0-9345-FCA4050184C3}",
									"nome": "Bomba",
									"descricao": "",
									"pontosMonitorados": [
										{
											"id": "{DFE091B5-7D8E-48CD-9164-5D3C981E9A80}",
											"idCanal": null,
											"idTipoSensor": "{E4ED1EB9-2172-4EFA-8B0C-D8FC50FAB02C}",
											"idPlanoMedicao": null,
											"idComponente": "{68A4F7C6-5AF8-40AF-A4B6-80D1E6D7A391}",
											"idGrupoPontosMonitorados": "{D0B0F7BE-6A92-4BD9-8C1F-4651599D4318}",
											"nome": "TI-RV-CIRC_OL",
											"descricao": "9 - Tempo de Circulacao de Óleo no RV",
											"localizacao": "Bombas RV",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "s",
												"id": "{E4ED1EB9-2172-4EFA-8B0C-D8FC50FAB02C}",
												"nome": "Intermitência",
												"tipoSensor": 4012,
												"unidade": 69014,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{7B606219-6912-4BC6-9844-4DEDD1A524DA}",
											"idCanal": null,
											"idTipoSensor": "{E4ED1EB9-2172-4EFA-8B0C-D8FC50FAB02C}",
											"idPlanoMedicao": null,
											"idComponente": "{68A4F7C6-5AF8-40AF-A4B6-80D1E6D7A391}",
											"idGrupoPontosMonitorados": "{F3629985-A73A-404C-B506-177CF389A0FA}",
											"nome": "TI-RV-DESL-OLINF",
											"descricao": "",
											"localizacao": "Bomba de Infiltração de Óleo",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "s",
												"id": "{E4ED1EB9-2172-4EFA-8B0C-D8FC50FAB02C}",
												"nome": "Intermitência",
												"tipoSensor": 4012,
												"unidade": 69014,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{44F0305D-4F75-4352-8F8E-3A8DB3F1504E}",
											"idCanal": null,
											"idTipoSensor": "{E4ED1EB9-2172-4EFA-8B0C-D8FC50FAB02C}",
											"idPlanoMedicao": null,
											"idComponente": "{68A4F7C6-5AF8-40AF-A4B6-80D1E6D7A391}",
											"idGrupoPontosMonitorados": "{17034116-A61F-4130-ADD8-5CDD4B1D2160}",
											"nome": "TI-RV-LIG-OLINF",
											"descricao": "",
											"localizacao": "Bomba de Infiltração de Óleo",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "s",
												"id": "{E4ED1EB9-2172-4EFA-8B0C-D8FC50FAB02C}",
												"nome": "Intermitência",
												"tipoSensor": 4012,
												"unidade": 69014,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{5219C02E-FEE0-4C9B-9039-DBF8580450B7}",
											"idCanal": null,
											"idTipoSensor": "{E4ED1EB9-2172-4EFA-8B0C-D8FC50FAB02C}",
											"idPlanoMedicao": null,
											"idComponente": "{68A4F7C6-5AF8-40AF-A4B6-80D1E6D7A391}",
											"idGrupoPontosMonitorados": "{0AB07AF6-5F37-473E-A73D-C2A2AA41898B}",
											"nome": "TI-RV-REP_OL",
											"descricao": "8 - Tempo de Reposição de Óleo no RV",
											"localizacao": "Bombas RV",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "s",
												"id": "{E4ED1EB9-2172-4EFA-8B0C-D8FC50FAB02C}",
												"nome": "Intermitência",
												"tipoSensor": 4012,
												"unidade": 69014,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{C50FC0A3-B677-43F4-AE4E-CEDE71202432}",
											"idCanal": null,
											"idTipoSensor": "{D8718BC9-CAA3-4EFE-ABF7-D9E166D8EBFD}",
											"idPlanoMedicao": null,
											"idComponente": "{68A4F7C6-5AF8-40AF-A4B6-80D1E6D7A391}",
											"idGrupoPontosMonitorados": "{7313A727-12F8-48B3-AAF8-60277BD00DED}",
											"nome": "TL-RV-B1PRINC",
											"descricao": "10 - Bomba 1 RV  Ligada (1), Desligada(0)",
											"localizacao": "Regulador de Velocidade",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "m",
												"id": "{D8718BC9-CAA3-4EFE-ABF7-D9E166D8EBFD}",
												"nome": "Lógico",
												"tipoSensor": 4011,
												"unidade": 69001,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{BB0D22CC-0BE8-4C92-8BD6-8582A66A4633}",
											"idCanal": null,
											"idTipoSensor": "{D8718BC9-CAA3-4EFE-ABF7-D9E166D8EBFD}",
											"idPlanoMedicao": null,
											"idComponente": "{68A4F7C6-5AF8-40AF-A4B6-80D1E6D7A391}",
											"idGrupoPontosMonitorados": "{7313A727-12F8-48B3-AAF8-60277BD00DED}",
											"nome": "TL-RV-B2PRINC",
											"descricao": "11 - Bomba 2 RV  Ligada (1), Desligada(0)",
											"localizacao": "Regulador de Velocidade",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "m",
												"id": "{D8718BC9-CAA3-4EFE-ABF7-D9E166D8EBFD}",
												"nome": "Lógico",
												"tipoSensor": 4011,
												"unidade": 69001,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{0415C6BE-5CFD-4D3A-8089-D1E248D8ABFC}",
									"idSubsistema": "{A4E81FD9-6F23-4FD0-9345-FCA4050184C3}",
									"nome": "Outros",
									"descricao": "Demais componentes do regulador de velocidade",
									"pontosMonitorados": [
										{
											"id": "{8DE8CA17-109F-4054-8D63-C9E5F0AF7ACA}",
											"idCanal": "{2155ECCA-6CDC-49ED-82E4-1BC454E09F0F}",
											"idTipoSensor": "{88B04C27-09D3-4761-BB34-2A1A01353BB0}",
											"idPlanoMedicao": null,
											"idComponente": "{0415C6BE-5CFD-4D3A-8089-D1E248D8ABFC}",
											"idGrupoPontosMonitorados": "{64242151-2641-4E45-AA1C-50C2BCF2ADF8}",
											"nome": "Potencia Ativa",
											"descricao": "1 - Potência ativa",
											"localizacao": "RV",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "MW",
												"id": "{88B04C27-09D3-4761-BB34-2A1A01353BB0}",
												"nome": "Potência",
												"tipoSensor": 4015,
												"unidade": 69098,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{789DE493-5B53-4DCA-84F6-4D8282A5CE0B}",
											"idCanal": "{BDF21D84-CE3E-4754-9E54-6291575AD8B0}",
											"idTipoSensor": "{C595F409-C6CF-43F1-8938-FD4B90E17F4C}",
											"idPlanoMedicao": null,
											"idComponente": "{0415C6BE-5CFD-4D3A-8089-D1E248D8ABFC}",
											"idGrupoPontosMonitorados": null,
											"nome": "Queda",
											"descricao": "2 - Queda ",
											"localizacao": "RV",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "m",
												"id": "{C595F409-C6CF-43F1-8938-FD4B90E17F4C}",
												"nome": "Transdutor de Queda",
												"tipoSensor": 4007,
												"unidade": 69001,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{938DA2B3-0193-4E18-AC71-61982127245B}",
											"idCanal": null,
											"idTipoSensor": "{D303D1ED-1DAD-4FC0-8B13-CF81DA3E4776}",
											"idPlanoMedicao": null,
											"idComponente": "{0415C6BE-5CFD-4D3A-8089-D1E248D8ABFC}",
											"idGrupoPontosMonitorados": "{D05173E3-2BD2-4004-A4E1-B626BD04FA87}",
											"nome": "TE-GER-COR_AUX",
											"descricao": "67 - Corrente do gerador auxiliar - A",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "A",
												"id": "{D303D1ED-1DAD-4FC0-8B13-CF81DA3E4776}",
												"nome": "Transdutor de Corrente",
												"tipoSensor": 4014,
												"unidade": 69011,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{C8CD30FF-435C-425C-8D9A-4C60EA341CA5}",
											"idCanal": null,
											"idTipoSensor": "{D303D1ED-1DAD-4FC0-8B13-CF81DA3E4776}",
											"idPlanoMedicao": null,
											"idComponente": "{0415C6BE-5CFD-4D3A-8089-D1E248D8ABFC}",
											"idGrupoPontosMonitorados": "{D05173E3-2BD2-4004-A4E1-B626BD04FA87}",
											"nome": "TE-GER-COR_PRINC",
											"descricao": "66 - Corrente gerador principal - A",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "A",
												"id": "{D303D1ED-1DAD-4FC0-8B13-CF81DA3E4776}",
												"nome": "Transdutor de Corrente",
												"tipoSensor": 4014,
												"unidade": 69011,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{7E803E36-7209-4065-BA21-FC5B63164A38}",
											"idCanal": null,
											"idTipoSensor": "{3C0FEE76-1609-49C4-A590-F4665B91ABB4}",
											"idPlanoMedicao": null,
											"idComponente": "{0415C6BE-5CFD-4D3A-8089-D1E248D8ABFC}",
											"idGrupoPontosMonitorados": "{D05173E3-2BD2-4004-A4E1-B626BD04FA87}",
											"nome": "TE-GER-PREAT",
											"descricao": "64 - Potência reativa",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "VAR",
												"id": "{3C0FEE76-1609-49C4-A590-F4665B91ABB4}",
												"nome": "Potência Reativa",
												"tipoSensor": 4015,
												"unidade": 69099,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{3EE3D6DB-1F62-4A37-9FF4-712A73071C94}",
											"idCanal": null,
											"idTipoSensor": "{83B596C7-9335-4229-8692-DACCB8E71445}",
											"idPlanoMedicao": null,
											"idComponente": "{0415C6BE-5CFD-4D3A-8089-D1E248D8ABFC}",
											"idGrupoPontosMonitorados": "{D05173E3-2BD2-4004-A4E1-B626BD04FA87}",
											"nome": "TE-GER-TEN",
											"descricao": "65 - Tensão - kV",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "kV",
												"id": "{83B596C7-9335-4229-8692-DACCB8E71445}",
												"nome": "Transdutor de Tensão (kV)",
												"tipoSensor": 4013,
												"unidade": 69112,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{08E58DE0-FABD-4A39-91EF-CB4AAACFC7DA}",
											"idCanal": null,
											"idTipoSensor": "{08C04645-F979-4A66-9139-6379FF7CA3C4}",
											"idPlanoMedicao": null,
											"idComponente": "{0415C6BE-5CFD-4D3A-8089-D1E248D8ABFC}",
											"idGrupoPontosMonitorados": "{D05173E3-2BD2-4004-A4E1-B626BD04FA87}",
											"nome": "TE-GER-TEN_AUX",
											"descricao": "68 - Tensão do gerador auxiliar - V",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "V",
												"id": "{08C04645-F979-4A66-9139-6379FF7CA3C4}",
												"nome": "Transdutor de Tensão(V)",
												"tipoSensor": 4013,
												"unidade": 69111,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{2FEB5FF0-FCC1-48A7-A58C-4211A06FE64E}",
											"idCanal": null,
											"idTipoSensor": "{E468DEFD-C234-4F8A-AFFD-7C33B9FF0EFD}",
											"idPlanoMedicao": null,
											"idComponente": "{0415C6BE-5CFD-4D3A-8089-D1E248D8ABFC}",
											"idGrupoPontosMonitorados": null,
											"nome": "TH-UG-HTRAB",
											"descricao": "5 - Horimetro da Unidade Geradora",
											"localizacao": "",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "h",
												"id": "{E468DEFD-C234-4F8A-AFFD-7C33B9FF0EFD}",
												"nome": "Horímetro",
												"tipoSensor": 4010,
												"unidade": 69012,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{A2280A4F-18EA-45D1-825A-FFDD65D1A540}",
											"idCanal": null,
											"idTipoSensor": "{686E425A-8016-4A7F-9546-6975E835E2CC}",
											"idPlanoMedicao": null,
											"idComponente": "{0415C6BE-5CFD-4D3A-8089-D1E248D8ABFC}",
											"idGrupoPontosMonitorados": null,
											"nome": "TN-UG-JUS",
											"descricao": "4 - Nível jusante",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "m",
												"id": "{686E425A-8016-4A7F-9546-6975E835E2CC}",
												"nome": "Transdutor de Nível (m)",
												"tipoSensor": 4007,
												"unidade": 69001,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{62A444AC-5F95-45A5-BEDD-C8A9E0400D7B}",
											"idCanal": null,
											"idTipoSensor": "{686E425A-8016-4A7F-9546-6975E835E2CC}",
											"idPlanoMedicao": null,
											"idComponente": "{0415C6BE-5CFD-4D3A-8089-D1E248D8ABFC}",
											"idGrupoPontosMonitorados": null,
											"nome": "TN-UG-MON",
											"descricao": "3 - Nível montante",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "m",
												"id": "{686E425A-8016-4A7F-9546-6975E835E2CC}",
												"nome": "Transdutor de Nível (m)",
												"tipoSensor": 4007,
												"unidade": 69001,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{A62EC2AC-9FF0-4E22-B9B4-FE2B378E6CFD}",
											"idCanal": null,
											"idTipoSensor": "{3E6511F2-D6B1-457C-BA82-3F659B4FB2D0}",
											"idPlanoMedicao": null,
											"idComponente": "{0415C6BE-5CFD-4D3A-8089-D1E248D8ABFC}",
											"idGrupoPontosMonitorados": null,
											"nome": "TO-RV-BALANC",
											"descricao": "15 - RV - Balance - %",
											"localizacao": "RV",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{3E6511F2-D6B1-457C-BA82-3F659B4FB2D0}",
												"nome": "Posição (%)",
												"tipoSensor": 4016,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{360BA2A7-6740-44CC-8EBE-4B3AD0382170}",
											"idCanal": null,
											"idTipoSensor": "{3E6511F2-D6B1-457C-BA82-3F659B4FB2D0}",
											"idPlanoMedicao": null,
											"idComponente": "{0415C6BE-5CFD-4D3A-8089-D1E248D8ABFC}",
											"idGrupoPontosMonitorados": null,
											"nome": "TO-RV-DIST",
											"descricao": "14 - Abertura do Distribuidor (%)",
											"localizacao": "RV",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{3E6511F2-D6B1-457C-BA82-3F659B4FB2D0}",
												"nome": "Posição (%)",
												"tipoSensor": 4016,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{01B6298B-EF27-4C6A-BE92-0127715B6D81}",
											"idCanal": null,
											"idTipoSensor": "{523F445B-77A4-4D20-AA81-99DA1012BADE}",
											"idPlanoMedicao": null,
											"idComponente": "{0415C6BE-5CFD-4D3A-8089-D1E248D8ABFC}",
											"idGrupoPontosMonitorados": null,
											"nome": "TR-UG-ROT",
											"descricao": "16 - Rotacao UG (RPM)",
											"localizacao": "RV",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "rpm",
												"id": "{523F445B-77A4-4D20-AA81-99DA1012BADE}",
												"nome": "Transdutor de Rotação",
												"tipoSensor": 4018,
												"unidade": 69060,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{08960637-178A-4FBF-A08A-D65AFDD2616B}",
									"idSubsistema": "{A4E81FD9-6F23-4FD0-9345-FCA4050184C3}",
									"nome": "Tanque",
									"descricao": "Tanque de óleo do regulador de velocidade",
									"pontosMonitorados": [
										{
											"id": "{3FB291AB-39BF-4271-96F7-28CA74A4495B}",
											"idCanal": null,
											"idTipoSensor": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
											"idPlanoMedicao": null,
											"idComponente": "{08960637-178A-4FBF-A08A-D65AFDD2616B}",
											"idGrupoPontosMonitorados": null,
											"nome": "TN-RV-ACUM",
											"descricao": "13 - Nível Óleo Acumulador RV",
											"localizacao": "Acumulador",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "mm",
												"id": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
												"nome": "Transdutor de Nivel (mm)",
												"tipoSensor": 4007,
												"unidade": 69003,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{4A187518-0F5C-4B8D-9140-7BC75FA1CE19}",
											"idCanal": null,
											"idTipoSensor": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
											"idPlanoMedicao": null,
											"idComponente": "{08960637-178A-4FBF-A08A-D65AFDD2616B}",
											"idGrupoPontosMonitorados": "{F516F74F-E122-47F6-AB13-AD88E339E49B}",
											"nome": "TN-RV-OLEO",
											"descricao": "12 - Nível de Óleo Reservatório do RV",
											"localizacao": "Reservatório do RV",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "mm",
												"id": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
												"nome": "Transdutor de Nivel (mm)",
												"tipoSensor": 4007,
												"unidade": 69003,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{7AAEE5E5-C0D8-49CA-8614-C399E9BD006E}",
											"idCanal": null,
											"idTipoSensor": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
											"idPlanoMedicao": null,
											"idComponente": "{08960637-178A-4FBF-A08A-D65AFDD2616B}",
											"idGrupoPontosMonitorados": null,
											"nome": "TN-RV-OLFUGA",
											"descricao": "30 - Nivel de oleo de Fuga RV",
											"localizacao": "RV",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "mm",
												"id": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
												"nome": "Transdutor de Nivel (mm)",
												"tipoSensor": 4007,
												"unidade": 69003,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{4C2B351F-648F-46E6-88E2-0F8B0EB8F623}",
											"idCanal": null,
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{08960637-178A-4FBF-A08A-D65AFDD2616B}",
											"idGrupoPontosMonitorados": null,
											"nome": "TP-RV-CIRC",
											"descricao": "6 - Pressao de Circulacao Acumulador RV",
											"localizacao": "AcumuladorRV",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{999AADB4-21FD-429A-9CD5-F0D80E332EC0}",
											"idCanal": null,
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{08960637-178A-4FBF-A08A-D65AFDD2616B}",
											"idGrupoPontosMonitorados": null,
											"nome": "TP-RV-REPO",
											"descricao": "7 - Pressao de Reposicao Acumulador RV",
											"localizacao": "Acumulador RV",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{1436FEED-EA65-4A22-99B6-0FCF77CF51AC}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{08960637-178A-4FBF-A08A-D65AFDD2616B}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-RV-OLEO",
											"descricao": "54 - Temp Oleo RV",
											"localizacao": "RV",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						},
						{
							"id": "{58BD198B-F77C-44F9-9BAB-299D77EB29AF}",
							"idEquipamento": "{70674D65-25BA-464F-B60C-879087990E61}",
							"nome": "Resfriamento Gerador",
							"descricao": "Subsistema de resfriamento da carcaça do gerador",
							"componentes": [
								{
									"id": "{C1C6E4F6-8C58-4998-9C72-AAC531BC6750}",
									"idSubsistema": "{58BD198B-F77C-44F9-9BAB-299D77EB29AF}",
									"nome": "Tiristores",
									"descricao": "",
									"pontosMonitorados": [
										{
											"id": "{E90AE9BE-545E-4A92-901F-9BE0F09796FB}",
											"idCanal": null,
											"idTipoSensor": "{D8718BC9-CAA3-4EFE-ABF7-D9E166D8EBFD}",
											"idPlanoMedicao": null,
											"idComponente": "{C1C6E4F6-8C58-4998-9C72-AAC531BC6750}",
											"idGrupoPontosMonitorados": null,
											"nome": "TL-TIR-B1PRINC",
											"descricao": "55 -  Bomba 1 TIR Ligada (1), Desligada(0)",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "m",
												"id": "{D8718BC9-CAA3-4EFE-ABF7-D9E166D8EBFD}",
												"nome": "Lógico",
												"tipoSensor": 4011,
												"unidade": 69001,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{13B3C055-24C6-4490-A396-1C44F00B5F9C}",
											"idCanal": null,
											"idTipoSensor": "{D8718BC9-CAA3-4EFE-ABF7-D9E166D8EBFD}",
											"idPlanoMedicao": null,
											"idComponente": "{C1C6E4F6-8C58-4998-9C72-AAC531BC6750}",
											"idGrupoPontosMonitorados": null,
											"nome": "TL-TIR-B2PRINC",
											"descricao": "56 -  Bomba 1 TIR Ligada (1), Desligada(0)",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "m",
												"id": "{D8718BC9-CAA3-4EFE-ABF7-D9E166D8EBFD}",
												"nome": "Lógico",
												"tipoSensor": 4011,
												"unidade": 69001,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{2F6D3160-C74C-4353-880C-F611671A2566}",
											"idCanal": null,
											"idTipoSensor": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
											"idPlanoMedicao": null,
											"idComponente": "{C1C6E4F6-8C58-4998-9C72-AAC531BC6750}",
											"idGrupoPontosMonitorados": null,
											"nome": "TN-TIR-AG",
											"descricao": "63 - Nivel de Agua no Reservatorio TIR  0-Baixo  1-Normal  2-Alto ",
											"localizacao": "Tiristores",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "mm",
												"id": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
												"nome": "Transdutor de Nivel (mm)",
												"tipoSensor": 4007,
												"unidade": 69003,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{EF2F98C4-3BB1-4CE0-BD0D-B8D946C3DCE6}",
											"idCanal": null,
											"idTipoSensor": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
											"idPlanoMedicao": null,
											"idComponente": "{C1C6E4F6-8C58-4998-9C72-AAC531BC6750}",
											"idGrupoPontosMonitorados": null,
											"nome": "TO-TIR-TESTAG",
											"descricao": "62 - Teste de agua Tiristores",
											"localizacao": "Tiristores",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
												"nome": "outros",
												"tipoSensor": 4011,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{1754FD36-CE24-4C1C-A767-9D7D935FFDD5}",
											"idCanal": null,
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{C1C6E4F6-8C58-4998-9C72-AAC531BC6750}",
											"idGrupoPontosMonitorados": null,
											"nome": "TP-TIR-AGBRUTA",
											"descricao": "57 - Pressao de Agua Bruta tiristores",
											"localizacao": "Tiristores",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{6BE122B9-2D76-46CC-B977-E86E1C8732B8}",
											"idCanal": null,
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{C1C6E4F6-8C58-4998-9C72-AAC531BC6750}",
											"idGrupoPontosMonitorados": null,
											"nome": "TP-TIR-AGDEST",
											"descricao": "58 - Pressao de agua destilada tiristores",
											"localizacao": "Tiristores",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{CFFCC101-62F4-47CA-B1A0-E9C4D1FA23E8}",
											"idCanal": null,
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{C1C6E4F6-8C58-4998-9C72-AAC531BC6750}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-TIR-AG_FORCADA",
											"descricao": "60 - Temp Agua Destilada quente forcada",
											"localizacao": "Tiristores",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{88ABD3D6-8E6E-4687-9047-A4E4C9F24061}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{C1C6E4F6-8C58-4998-9C72-AAC531BC6750}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-TIR-AG_FRIA",
											"descricao": "61 - Temp Agua destilada fria",
											"localizacao": "Tiristores",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{AF4035F4-B4B2-4CDF-8452-D3DEB456873D}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{C1C6E4F6-8C58-4998-9C72-AAC531BC6750}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-TIR-AG_NORMAL",
											"descricao": "59 - Temp agua destilada quente normal",
											"localizacao": "Tiristores",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{DE7E1169-6692-46BC-B6F2-413ADED0167D}",
									"idSubsistema": "{58BD198B-F77C-44F9-9BAB-299D77EB29AF}",
									"nome": "Trocador de calor",
									"descricao": "Trocadores de calor da carcaça do gerador",
									"pontosMonitorados": [
										{
											"id": "{EB6C1DE6-EFDF-4A26-A02B-CE02144A8F52}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{DE7E1169-6692-46BC-B6F2-413ADED0167D}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-GER-AF",
											"descricao": "82 - AR FRIO (TUG12)",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{84FE0B1F-34B5-419A-B758-475ABB5FC386}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{DE7E1169-6692-46BC-B6F2-413ADED0167D}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-GER-AQ",
											"descricao": "83 - AR QUENTE (TUG13)",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{DB6FE186-C919-4481-B053-5C0C72EE51E1}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{DE7E1169-6692-46BC-B6F2-413ADED0167D}",
											"idGrupoPontosMonitorados": "{4C40A215-464F-4632-AB22-F83CA6A77C3D}",
											"nome": "TT-GER-AQ01",
											"descricao": "41 - Ar Quente 1 (TC11)",
											"localizacao": "??",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{BD05CED5-53BE-4928-8224-EB8AAF2B4A0E}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{DE7E1169-6692-46BC-B6F2-413ADED0167D}",
											"idGrupoPontosMonitorados": "{4C40A215-464F-4632-AB22-F83CA6A77C3D}",
											"nome": "TT-GER-AQ02",
											"descricao": "42 - Ar Quente 2 (TC12)",
											"localizacao": "??",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{E6ABA5ED-8681-4FEF-8501-CDE7CBD8633C}",
											"idCanal": null,
											"idTipoSensor": "{D8718BC9-CAA3-4EFE-ABF7-D9E166D8EBFD}",
											"idPlanoMedicao": null,
											"idComponente": "{DE7E1169-6692-46BC-B6F2-413ADED0167D}",
											"idGrupoPontosMonitorados": null,
											"nome": "TU-GER",
											"descricao": "43 - Detector de Humidade",
											"localizacao": "Gerador",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "m",
												"id": "{D8718BC9-CAA3-4EFE-ABF7-D9E166D8EBFD}",
												"nome": "Lógico",
												"tipoSensor": 4011,
												"unidade": 69001,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						},
						{
							"id": "{47EAD7C9-76D9-4C16-B03D-9B75323CD995}",
							"idEquipamento": "{70674D65-25BA-464F-B60C-879087990E61}",
							"nome": "Transformador elevador",
							"descricao": "Transformador elevador",
							"componentes": [
								{
									"id": "{693395A6-7070-408D-9972-3C5E61B60E99}",
									"idSubsistema": "{47EAD7C9-76D9-4C16-B03D-9B75323CD995}",
									"nome": "Sistema Anti-Incêndio",
									"descricao": "",
									"pontosMonitorados": [
										{
											"id": "{6FC58EA9-80BA-4A46-99D0-E982A5F25DD7}",
											"idCanal": null,
											"idTipoSensor": "{E468DEFD-C234-4F8A-AFFD-7C33B9FF0EFD}",
											"idPlanoMedicao": null,
											"idComponente": "{693395A6-7070-408D-9972-3C5E61B60E99}",
											"idGrupoPontosMonitorados": null,
											"nome": "TH-TRAFO-INCENDIO",
											"descricao": "",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "h",
												"id": "{E468DEFD-C234-4F8A-AFFD-7C33B9FF0EFD}",
												"nome": "Horímetro",
												"tipoSensor": 4010,
												"unidade": 69012,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{0EA53A68-7684-4D81-A075-A0EE0DED725D}",
											"idCanal": null,
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{693395A6-7070-408D-9972-3C5E61B60E99}",
											"idGrupoPontosMonitorados": null,
											"nome": "TP-TRAFO-INCENDIO-AG",
											"descricao": "",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{E159A959-E643-4943-B2DA-8EC2375FC098}",
											"idCanal": null,
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{693395A6-7070-408D-9972-3C5E61B60E99}",
											"idGrupoPontosMonitorados": null,
											"nome": "TP-TRAFO-INCENDIO-AR",
											"descricao": "",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{1BB22AE4-FAEB-4D65-8C1A-FEDB28D4A36C}",
									"idSubsistema": "{47EAD7C9-76D9-4C16-B03D-9B75323CD995}",
									"nome": "Transformador",
									"descricao": "",
									"pontosMonitorados": [
										{
											"id": "{C3B73C93-35F4-40DB-9F85-F2302ED9F055}",
											"idCanal": null,
											"idTipoSensor": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
											"idPlanoMedicao": null,
											"idComponente": "{1BB22AE4-FAEB-4D65-8C1A-FEDB28D4A36C}",
											"idGrupoPontosMonitorados": null,
											"nome": "TN-TRANSF-OLEO",
											"descricao": "89 - Nivel do transformador  0-Baixo  1-Normal  2-Alto",
											"localizacao": "Transformador Elevador",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "mm",
												"id": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
												"nome": "Transdutor de Nivel (mm)",
												"tipoSensor": 4007,
												"unidade": 69003,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{B80C9E45-3FE9-4CBD-BC60-CD44739DBE4D}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{1BB22AE4-FAEB-4D65-8C1A-FEDB28D4A36C}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-TRANSF-ENROL",
											"descricao": "87 - Temperatura do Enrolamento do Transformador",
											"localizacao": "Enrolamento Transformador",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{C0370712-FCD4-4CB8-B9C2-00C0DA317BDF}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{1BB22AE4-FAEB-4D65-8C1A-FEDB28D4A36C}",
											"idGrupoPontosMonitorados": null,
											"nome": "TT-TRANSF-OLEO",
											"descricao": "88 - Temp do oleo do transformador elevador",
											"localizacao": "Transformador",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						},
						{
							"id": "{4E9CDECE-95F4-4284-9B28-7192EF6DFD5D}",
							"idEquipamento": "{70674D65-25BA-464F-B60C-879087990E61}",
							"nome": "Turbina",
							"descricao": "Turbina",
							"componentes": [
								{
									"id": "{31DEEA9B-18EA-4EAF-AD45-4B8BF3766A70}",
									"idSubsistema": "{4E9CDECE-95F4-4284-9B28-7192EF6DFD5D}",
									"nome": "caixa espiral",
									"descricao": "caixa espiral",
									"pontosMonitorados": [
										{
											"id": "{723260B9-4550-4215-B3A5-9AFE02263E46}",
											"idCanal": null,
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{31DEEA9B-18EA-4EAF-AD45-4B8BF3766A70}",
											"idGrupoPontosMonitorados": "{5DD0FD68-CF09-4BE7-B5BE-FC4D93CB6D8E}",
											"nome": "TP-T-CXE",
											"descricao": "23 - Pressao Caixa Espiral",
											"localizacao": "Caixa Espiral",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{476EAF19-B679-4608-B136-96A6D3B03BEA}",
											"idCanal": null,
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{31DEEA9B-18EA-4EAF-AD45-4B8BF3766A70}",
											"idGrupoPontosMonitorados": null,
											"nome": "TP-T-RODA",
											"descricao": "24 - Pressao sobre a roda",
											"localizacao": "Turbina",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{706C9B37-B78D-41E4-9F57-895B2BC3E435}",
									"idSubsistema": "{4E9CDECE-95F4-4284-9B28-7192EF6DFD5D}",
									"nome": "tampa da turbina",
									"descricao": "tampa da turbina",
									"pontosMonitorados": [
										{
											"id": "{9A96A327-7D65-4041-853D-24FB1A771F87}",
											"idCanal": null,
											"idTipoSensor": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
											"idPlanoMedicao": null,
											"idComponente": "{706C9B37-B78D-41E4-9F57-895B2BC3E435}",
											"idGrupoPontosMonitorados": "{37A407A6-C8FC-4C73-A84B-F9DBB4A126F5}",
											"nome": "TN-T-AG01",
											"descricao": "29 - Nivel de agua infiltrada na tampa da turbina",
											"localizacao": "Tampa da Turbina",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "mm",
												"id": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
												"nome": "Transdutor de Nivel (mm)",
												"tipoSensor": 4007,
												"unidade": 69003,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{10DE2CCF-4A3B-42C4-90D4-202DFBD2C6E9}",
											"idCanal": null,
											"idTipoSensor": "{2E1E4628-4F56-4569-AA31-94E40D581991}",
											"idPlanoMedicao": null,
											"idComponente": "{706C9B37-B78D-41E4-9F57-895B2BC3E435}",
											"idGrupoPontosMonitorados": null,
											"nome": "TO-TT-POS",
											"descricao": "19 - Curso do Servomotor (mm)",
											"localizacao": "Turbina",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "mm",
												"id": "{2E1E4628-4F56-4569-AA31-94E40D581991}",
												"nome": "Posição (mm)",
												"tipoSensor": 4016,
												"unidade": 69003,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{374FCB8D-A84D-4F73-9929-1CFAA59480AE}",
											"idCanal": null,
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{706C9B37-B78D-41E4-9F57-895B2BC3E435}",
											"idGrupoPontosMonitorados": null,
											"nome": "TP-T-ABERT",
											"descricao": "20 - Pressao de Abertura",
											"localizacao": "Turbina",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{77BE7251-D17D-44BB-B2EE-1F95FDC50FBE}",
											"idCanal": null,
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{706C9B37-B78D-41E4-9F57-895B2BC3E435}",
											"idGrupoPontosMonitorados": null,
											"nome": "TP-T-FECHA",
											"descricao": "21 - Pressao Fechamento",
											"localizacao": "Turbina",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{764EF190-4598-4061-84AD-30D0BFF2BAB4}",
											"idCanal": null,
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{706C9B37-B78D-41E4-9F57-895B2BC3E435}",
											"idGrupoPontosMonitorados": "{E43588DC-709A-466D-90A0-BD6B16718149}",
											"nome": "TP-T-TT",
											"descricao": "25 - Pressao Tampa Turbina",
											"localizacao": "Tampa da Turbina",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{DBE07D96-6508-4083-9B69-8EB9724B1894}",
									"idSubsistema": "{4E9CDECE-95F4-4284-9B28-7192EF6DFD5D}",
									"nome": "tubo de succao",
									"descricao": "tubo de succao",
									"pontosMonitorados": [
										{
											"id": "{54E2AC8B-039C-4D56-B391-C171B85E6F90}",
											"idCanal": null,
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{DBE07D96-6508-4083-9B69-8EB9724B1894}",
											"idGrupoPontosMonitorados": "{58E2F95E-C0E0-47CA-B5F8-CF8198BDC942}",
											"nome": "TP-T-SUC",
											"descricao": "22 - Pressao Tubo Succao",
											"localizacao": "Tubo de Sucção",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{F26B608D-D19B-4053-A80D-ADE8986B52A7}",
									"idSubsistema": "{4E9CDECE-95F4-4284-9B28-7192EF6DFD5D}",
									"nome": "Vedacao do Eixo",
									"descricao": "Vedação do Eixo",
									"pontosMonitorados": [
										{
											"id": "{023E47E2-CBFA-4C8C-A959-77E400132405}",
											"idCanal": null,
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{F26B608D-D19B-4053-A80D-ADE8986B52A7}",
											"idGrupoPontosMonitorados": null,
											"nome": "TP-T-AG_VEDACAO",
											"descricao": "18 - Manometro de pressao da agua de vedacao",
											"localizacao": "Junta de vedação",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						}
					]
				},
				{
					"id": "{EFB8143D-C02E-4474-941B-1B0A943A2EE8}",
					"idPlanta": "{B751541E-6D27-4D30-B9E6-FB05E4E193E7}",
					"idAnalisador": null,
					"idUnidadeAquisicao": null,
					"nome": "UG2",
					"fabricante": "x",
					"modelo": "",
					"descricao": "",
					"localizacao": 0,
					"nroSerie": "",
					"tipoEquipamento": 68000,
					"subsistemas": [
						{
							"id": "{AA96F999-3CA9-4E4B-B0EF-12E0478E0903}",
							"idEquipamento": "{EFB8143D-C02E-4474-941B-1B0A943A2EE8}",
							"nome": "Circulação Óleo ME",
							"descricao": "Subsistema de circulação de óleo do ME",
							"componentes": [
								{
									"id": "{B8572CB6-A2C1-4CB3-B6CC-720B27BA3F8A}",
									"idSubsistema": "{AA96F999-3CA9-4E4B-B0EF-12E0478E0903}",
									"nome": "Bomba",
									"descricao": "Bomba de circulação de óleo do ME",
									"pontosMonitorados": [
										{
											"id": "{758C4ABA-8199-49C9-B5E5-F0C0276707D1}",
											"idCanal": "{68EA6A2F-9B19-4D4F-BDF4-DB21AF886F2A}",
											"idTipoSensor": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
											"idPlanoMedicao": null,
											"idComponente": "{B8572CB6-A2C1-4CB3-B6CC-720B27BA3F8A}",
											"idGrupoPontosMonitorados": "{7313A727-12F8-48B3-AAF8-60277BD00DED}",
											"nome": "TL-ME-CIRC_OL_B1PRINC",
											"descricao": null,
											"localizacao": "Mancal de Escora",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
												"nome": "outros",
												"tipoSensor": 4011,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{3F2567B9-2979-4002-B766-039A48925364}",
											"idCanal": "{33BFFD9F-B0A6-4FC7-ADB2-8B97A05CDA7B}",
											"idTipoSensor": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
											"idPlanoMedicao": null,
											"idComponente": "{B8572CB6-A2C1-4CB3-B6CC-720B27BA3F8A}",
											"idGrupoPontosMonitorados": "{7313A727-12F8-48B3-AAF8-60277BD00DED}",
											"nome": "TL-ME-CIRC_OL_B2PRINC",
											"descricao": null,
											"localizacao": "Mancal de Escora",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
												"nome": "outros",
												"tipoSensor": 4011,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{956E6626-EABE-40FE-9CDD-8BAB1247480E}",
									"idSubsistema": "{AA96F999-3CA9-4E4B-B0EF-12E0478E0903}",
									"nome": "Tanque",
									"descricao": "Tanque de óleo do ME",
									"pontosMonitorados": [
										{
											"id": "{B1B8E4A8-D9A9-43F2-B188-F64395FB2E67}",
											"idCanal": "{DF36424C-4AFA-405C-A6E6-16CE1723E31D}",
											"idTipoSensor": "{E096C366-B10F-4793-9641-5B49128F43EC}",
											"idPlanoMedicao": null,
											"idComponente": "{956E6626-EABE-40FE-9CDD-8BAB1247480E}",
											"idGrupoPontosMonitorados": "{68EB6FF8-55A9-4404-854C-11D0C6B2BBC8}",
											"nome": "TN-ME-OL_TANQEXT",
											"descricao": "",
											"localizacao": "Tanque Externo",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{E096C366-B10F-4793-9641-5B49128F43EC}",
												"nome": "Transdutor de Nível (%)",
												"tipoSensor": 4007,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{7FB8A746-4A9D-4DA9-BE8F-F42C7846441F}",
											"idCanal": "{F7246074-7B3A-4CB8-8F4C-EC0A45A33CF3}",
											"idTipoSensor": "{E096C366-B10F-4793-9641-5B49128F43EC}",
											"idPlanoMedicao": null,
											"idComponente": "{956E6626-EABE-40FE-9CDD-8BAB1247480E}",
											"idGrupoPontosMonitorados": "{D5C31694-0445-42A1-BE54-3DB6C1A83D52}",
											"nome": "TN-ME-TOC",
											"descricao": "",
											"localizacao": "Tanque de Captação de Vazamento",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{E096C366-B10F-4793-9641-5B49128F43EC}",
												"nome": "Transdutor de Nível (%)",
												"tipoSensor": 4007,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{C7434DD5-127B-4EEC-83DC-73947DCA8B3B}",
									"idSubsistema": "{AA96F999-3CA9-4E4B-B0EF-12E0478E0903}",
									"nome": "Trocador",
									"descricao": "Trocador de calor do ME",
									"pontosMonitorados": [
										{
											"id": "{44A7CC25-9EA8-427C-9470-13C1DE8EAE9D}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{C7434DD5-127B-4EEC-83DC-73947DCA8B3B}",
											"idGrupoPontosMonitorados": "{A2A09AA5-6C6B-486A-9473-AE549883CCFA}",
											"nome": "SV-ME-DTAG",
											"descricao": "",
											"localizacao": "Trocador de Calor",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{97DE6173-A2E3-4C99-93C9-7B453F0A0EE6}",
											"idCanal": "{579B69DF-1A28-4490-BD1F-E76F3361CF2E}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{C7434DD5-127B-4EEC-83DC-73947DCA8B3B}",
											"idGrupoPontosMonitorados": "{C4EF0694-1F03-4600-BDF6-6E5019F8FDE2}",
											"nome": "TT-ME-ASAI",
											"descricao": null,
											"localizacao": "Saída do TC",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{D83FF519-61B2-429E-8AB2-2FE9E339E3C7}",
											"idCanal": "{99F1B08F-0FF1-465C-972E-7328EC13AD8B}",
											"idTipoSensor": "{E38C8E96-479C-48AF-BD35-DBA7A535C3D1}",
											"idPlanoMedicao": null,
											"idComponente": "{C7434DD5-127B-4EEC-83DC-73947DCA8B3B}",
											"idGrupoPontosMonitorados": "{9B5B7607-B115-44DF-9987-7CB3C7D47044}",
											"nome": "TV-ME-AGTC",
											"descricao": null,
											"localizacao": "Entrada do TC ",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "cm³/s",
												"id": "{E38C8E96-479C-48AF-BD35-DBA7A535C3D1}",
												"nome": "Transdutor de Vazão",
												"tipoSensor": 4008,
												"unidade": 69030,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{A5919277-3FE2-4261-9E15-1FB554F57F89}",
											"idCanal": "{7C036D33-BE88-4382-B6B6-FBF20B3DBA0A}",
											"idTipoSensor": "{E38C8E96-479C-48AF-BD35-DBA7A535C3D1}",
											"idPlanoMedicao": null,
											"idComponente": "{C7434DD5-127B-4EEC-83DC-73947DCA8B3B}",
											"idGrupoPontosMonitorados": "{757D7746-581C-4309-815D-EC8649A733AF}",
											"nome": "TV-ME-OL_CIRC",
											"descricao": null,
											"localizacao": "Mancal de Escora",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "cm³/s",
												"id": "{E38C8E96-479C-48AF-BD35-DBA7A535C3D1}",
												"nome": "Transdutor de Vazão",
												"tipoSensor": 4008,
												"unidade": 69030,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						},
						{
							"id": "{4F28730D-4101-400E-89EC-DE1DE245BFE2}",
							"idEquipamento": "{EFB8143D-C02E-4474-941B-1B0A943A2EE8}",
							"nome": "Circulação Óleo MGG",
							"descricao": "Subsistema de circulação de óleo do MGG",
							"componentes": [
								{
									"id": "{3B8FA4A5-7F29-436A-AD42-8423DDBD01EC}",
									"idSubsistema": "{4F28730D-4101-400E-89EC-DE1DE245BFE2}",
									"nome": "Trocador",
									"descricao": "Trocador de calor do MGG",
									"pontosMonitorados": [
										{
											"id": "{EA41217C-47B1-4F66-B529-8430DEB4B693}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{3B8FA4A5-7F29-436A-AD42-8423DDBD01EC}",
											"idGrupoPontosMonitorados": "{A2A09AA5-6C6B-486A-9473-AE549883CCFA}",
											"nome": "SV-MGG-DTAG",
											"descricao": "",
											"localizacao": "Trocador de Calor",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{7E38B5C1-51CA-41E1-A6C0-641C30475384}",
											"idCanal": "{9985A6C0-7E4E-461B-9BA0-B0A6B9B3959E}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{3B8FA4A5-7F29-436A-AD42-8423DDBD01EC}",
											"idGrupoPontosMonitorados": "{F54DDEB1-5530-4450-A651-D68C86511040}",
											"nome": "TT-MGG-ASAI",
											"descricao": null,
											"localizacao": "Saída do TC",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{45D969DF-0229-4A7F-91E5-0627ADB14365}",
											"idCanal": "{610F6413-9FFC-4098-BF29-9FD289CE0986}",
											"idTipoSensor": "{E38C8E96-479C-48AF-BD35-DBA7A535C3D1}",
											"idPlanoMedicao": null,
											"idComponente": "{3B8FA4A5-7F29-436A-AD42-8423DDBD01EC}",
											"idGrupoPontosMonitorados": "{9F587C7D-144B-43E2-9466-E073071DF84F}",
											"nome": "TV-MGG-AGTC",
											"descricao": null,
											"localizacao": "Entrada do TC",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "cm³/s",
												"id": "{E38C8E96-479C-48AF-BD35-DBA7A535C3D1}",
												"nome": "Transdutor de Vazão",
												"tipoSensor": 4008,
												"unidade": 69030,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						},
						{
							"id": "{9C8A0B18-561B-450B-B7B6-DD137DF95189}",
							"idEquipamento": "{EFB8143D-C02E-4474-941B-1B0A943A2EE8}",
							"nome": "Circulação Óleo MGT",
							"descricao": "Subsistema de circulação de óleo do MGT",
							"componentes": [
								{
									"id": "{83915932-7982-4DEC-BDD2-7C4767FFC24F}",
									"idSubsistema": "{9C8A0B18-561B-450B-B7B6-DD137DF95189}",
									"nome": "Bomba",
									"descricao": "Bomda circulação de óleo do MGT",
									"pontosMonitorados": [
										{
											"id": "{8F7BB8F0-DB0C-4672-813B-BC6BD9EE8274}",
											"idCanal": "{BC6AA8CA-2569-4A37-88F3-AA39C6A6EE9B}",
											"idTipoSensor": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
											"idPlanoMedicao": null,
											"idComponente": "{83915932-7982-4DEC-BDD2-7C4767FFC24F}",
											"idGrupoPontosMonitorados": "{7313A727-12F8-48B3-AAF8-60277BD00DED}",
											"nome": "TL-MGT-CIRC_OL_B1PRINC",
											"descricao": null,
											"localizacao": "Mancal Guia da Turbina",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
												"nome": "outros",
												"tipoSensor": 4011,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{FCAE2D39-A1C9-40ED-8090-B603FB425D47}",
											"idCanal": "{A9AC132B-E8B6-4508-A767-D18E2DFA0E52}",
											"idTipoSensor": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
											"idPlanoMedicao": null,
											"idComponente": "{83915932-7982-4DEC-BDD2-7C4767FFC24F}",
											"idGrupoPontosMonitorados": "{7313A727-12F8-48B3-AAF8-60277BD00DED}",
											"nome": "TL-MGT-CIRC_OL_B2PRINC",
											"descricao": null,
											"localizacao": "Mancal Guia da Turbina",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
												"nome": "outros",
												"tipoSensor": 4011,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{B7D250EB-A0D3-4F13-A3AA-D0FA3AF40426}",
									"idSubsistema": "{9C8A0B18-561B-450B-B7B6-DD137DF95189}",
									"nome": "Trocador",
									"descricao": "Trocador de calor do MGT",
									"pontosMonitorados": [
										{
											"id": "{DCCB9D59-8E8F-4E6F-B86A-8A94535D59B9}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{B7D250EB-A0D3-4F13-A3AA-D0FA3AF40426}",
											"idGrupoPontosMonitorados": "{A2A09AA5-6C6B-486A-9473-AE549883CCFA}",
											"nome": "SV-MGT-DTAG",
											"descricao": "",
											"localizacao": "Trocador de Calor",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{86879BDA-467D-4BB6-9795-224B5B21CFCA}",
											"idCanal": "{14075008-31AB-40C9-84E5-B54EC6DF908B}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{B7D250EB-A0D3-4F13-A3AA-D0FA3AF40426}",
											"idGrupoPontosMonitorados": "{88426D04-4782-4824-9376-693921CFBF18}",
											"nome": "TT-MGT-ASAI",
											"descricao": null,
											"localizacao": "Saída do TC",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{314C7C2E-4AC1-4C3F-9B64-741A8555C203}",
											"idCanal": "{915188F4-F92A-4A8E-AAFB-E2F402F6914A}",
											"idTipoSensor": "{E38C8E96-479C-48AF-BD35-DBA7A535C3D1}",
											"idPlanoMedicao": null,
											"idComponente": "{B7D250EB-A0D3-4F13-A3AA-D0FA3AF40426}",
											"idGrupoPontosMonitorados": "{ABC2336F-B226-43FF-A8AC-4520E7EEC929}",
											"nome": "TV-MGT-AGTC",
											"descricao": null,
											"localizacao": "Entrada do TC",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "cm³/s",
												"id": "{E38C8E96-479C-48AF-BD35-DBA7A535C3D1}",
												"nome": "Transdutor de Vazão",
												"tipoSensor": 4008,
												"unidade": 69030,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						},
						{
							"id": "{BE29C09C-3A5D-4DBA-A56B-8C6FAC799C94}",
							"idEquipamento": "{EFB8143D-C02E-4474-941B-1B0A943A2EE8}",
							"nome": "Gerador Eletrico",
							"descricao": "Gerador Eletrico",
							"componentes": [
								{
									"id": "{40413AAC-679A-48BF-8802-BA59B36B8DF4}",
									"idSubsistema": "{BE29C09C-3A5D-4DBA-A56B-8C6FAC799C94}",
									"nome": "Enrolamento do estator",
									"descricao": "Enrolamento do estator",
									"pontosMonitorados": [
										{
											"id": "{7F5859B1-7A8C-434D-B682-1CE72D6DF571}",
											"idCanal": "{67AE74E4-4C29-4AC2-BFC2-17461DE5A33E}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{40413AAC-679A-48BF-8802-BA59B36B8DF4}",
											"idGrupoPontosMonitorados": "{26D3510D-2E50-4A91-B7AC-F97C1F97DFBD}",
											"nome": "TT-GER-CO01",
											"descricao": null,
											"localizacao": "Cobre ponto 01",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{C796F2A2-6D2D-4700-BA55-79CEB11FEE01}",
											"idCanal": "{720D9C52-55AA-41AA-8993-AE20DE943C97}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{40413AAC-679A-48BF-8802-BA59B36B8DF4}",
											"idGrupoPontosMonitorados": "{26D3510D-2E50-4A91-B7AC-F97C1F97DFBD}",
											"nome": "TT-GER-CO04",
											"descricao": null,
											"localizacao": "Cobre ponto 04",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{E0A648A7-6441-4CC9-A229-9C9F1AA4F4B5}",
											"idCanal": "{87B7BC5A-D3D0-4C77-ADFA-7CC339C4A685}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{40413AAC-679A-48BF-8802-BA59B36B8DF4}",
											"idGrupoPontosMonitorados": "{26D3510D-2E50-4A91-B7AC-F97C1F97DFBD}",
											"nome": "TT-GER-CO07",
											"descricao": null,
											"localizacao": "Cobre ponto 07",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{C732B72F-300B-4F5F-9938-0D0C6691A7E6}",
											"idCanal": "{607C9952-C34A-4B7F-AC5B-4DFEF1682CAB}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{40413AAC-679A-48BF-8802-BA59B36B8DF4}",
											"idGrupoPontosMonitorados": "{26D3510D-2E50-4A91-B7AC-F97C1F97DFBD}",
											"nome": "TT-GER-CO10",
											"descricao": null,
											"localizacao": "Cobre ponto 10",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{89828CF6-30F1-4361-BED1-EA988EF5D95E}",
											"idCanal": "{768EB51E-6F8F-4530-9F6A-0830EA4B587B}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{40413AAC-679A-48BF-8802-BA59B36B8DF4}",
											"idGrupoPontosMonitorados": "{26D3510D-2E50-4A91-B7AC-F97C1F97DFBD}",
											"nome": "TT-GER-CO13",
											"descricao": null,
											"localizacao": "Cobre ponto 13",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{70F145FF-1139-4669-B6B1-116D244BA9CB}",
											"idCanal": "{6B3A4EA4-F503-423E-BDFE-D13994F7C541}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{40413AAC-679A-48BF-8802-BA59B36B8DF4}",
											"idGrupoPontosMonitorados": "{26D3510D-2E50-4A91-B7AC-F97C1F97DFBD}",
											"nome": "TT-GER-CO16",
											"descricao": null,
											"localizacao": "Cobre ponto 16",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{22A5A185-5810-46A6-BE2C-E0C2E6C48970}",
											"idCanal": "{18A9C1BB-0446-41E2-8372-D0170D571BA9}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{40413AAC-679A-48BF-8802-BA59B36B8DF4}",
											"idGrupoPontosMonitorados": "{26D3510D-2E50-4A91-B7AC-F97C1F97DFBD}",
											"nome": "TT-GER-CO19",
											"descricao": null,
											"localizacao": "Cobre ponto 19",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{C523B020-B96D-4FD8-BE21-E6E5D3C88755}",
											"idCanal": "{143763D0-DE91-401C-8EBB-0CF7A96EBE1B}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{40413AAC-679A-48BF-8802-BA59B36B8DF4}",
											"idGrupoPontosMonitorados": "{26D3510D-2E50-4A91-B7AC-F97C1F97DFBD}",
											"nome": "TT-GER-CO22",
											"descricao": null,
											"localizacao": "Cobre ponto 22",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{F8810C9E-D00D-42EA-B918-54806945B8F2}",
									"idSubsistema": "{BE29C09C-3A5D-4DBA-A56B-8C6FAC799C94}",
									"nome": "Enrolamento do Rotor",
									"descricao": "Enrolamento do rotor",
									"pontosMonitorados": [
										{
											"id": "{F95EE76B-BBB5-47AE-BC2E-D16891516768}",
											"idCanal": "{68377E7A-5486-43B9-A5FC-8B57DFF5C7FF}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F8810C9E-D00D-42EA-B918-54806945B8F2}",
											"idGrupoPontosMonitorados": "{29C071F9-11E1-440F-829D-5EBF76A7A205}",
											"nome": "TT-ROTOR-TEN",
											"descricao": null,
											"localizacao": "Rotor",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{22B9DB15-833D-441E-AA83-805DC0BE540D}",
									"idSubsistema": "{BE29C09C-3A5D-4DBA-A56B-8C6FAC799C94}",
									"nome": "Excitação",
									"descricao": "Excitação do rotor gerador - tiristores",
									"pontosMonitorados": [
										{
											"id": "{5C83A275-E9B6-4EA7-BCB0-5F4AE16E80A8}",
											"idCanal": "{B5485BC5-F2E5-4F0B-9D1D-34420D0C35EB}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{22B9DB15-833D-441E-AA83-805DC0BE540D}",
											"idGrupoPontosMonitorados": "{26D3510D-2E50-4A91-B7AC-F97C1F97DFBD}",
											"nome": "TT-GER-CO_EXC",
											"descricao": null,
											"localizacao": "Cobre",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{5662EBC4-B2D5-4A7D-B65B-461A886A746A}",
									"idSubsistema": "{BE29C09C-3A5D-4DBA-A56B-8C6FAC799C94}",
									"nome": "Núcleo do estator",
									"descricao": "Núcleo do estator",
									"pontosMonitorados": [
										{
											"id": "{FF6F9DD3-55A7-451B-92F2-524C0FB135C1}",
											"idCanal": "{7B5A8A74-FD56-4C7D-8533-57A66437362C}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{5662EBC4-B2D5-4A7D-B65B-461A886A746A}",
											"idGrupoPontosMonitorados": "{3F228924-77F6-41FD-B1DC-25B5DB9B43A1}",
											"nome": "TT-GER-FE01",
											"descricao": null,
											"localizacao": "Ferro ponto 01",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{177F8635-299D-4F5F-B9C3-A244BEE776A5}",
											"idCanal": "{225955AC-4077-484F-8CBB-1E0CA2F37445}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{5662EBC4-B2D5-4A7D-B65B-461A886A746A}",
											"idGrupoPontosMonitorados": "{3F228924-77F6-41FD-B1DC-25B5DB9B43A1}",
											"nome": "TT-GER-FE02",
											"descricao": null,
											"localizacao": "Ferro ponto 02",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{74F4013E-EE6D-45A7-8E94-5D2DEA0B6208}",
											"idCanal": "{F1C21CAC-B535-4EC7-92D4-A5A1E49DAD0A}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{5662EBC4-B2D5-4A7D-B65B-461A886A746A}",
											"idGrupoPontosMonitorados": "{3F228924-77F6-41FD-B1DC-25B5DB9B43A1}",
											"nome": "TT-GER-FE03",
											"descricao": null,
											"localizacao": "Ferro ponto 03",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{9FD69988-5DD2-4A88-99A2-B703A0056FFE}",
											"idCanal": "{D0AB2A14-E9EA-4214-91FB-165BD01FFE39}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{5662EBC4-B2D5-4A7D-B65B-461A886A746A}",
											"idGrupoPontosMonitorados": "{3F228924-77F6-41FD-B1DC-25B5DB9B43A1}",
											"nome": "TT-GER-FE05",
											"descricao": null,
											"localizacao": "Ferro ponto 05",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{7FB52C61-93B0-4848-A56D-30F5A8BDABE1}",
											"idCanal": "{F3C8C0A1-35D0-4780-ACBC-E47B74F9AB35}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{5662EBC4-B2D5-4A7D-B65B-461A886A746A}",
											"idGrupoPontosMonitorados": "{3F228924-77F6-41FD-B1DC-25B5DB9B43A1}",
											"nome": "TT-GER-FE07",
											"descricao": null,
											"localizacao": "Ferro ponto 07",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{227ADAA2-25F0-4B93-BE87-8FA884777DFF}",
											"idCanal": "{B895E09C-83FC-4CE0-AB3D-6E750CF0ACED}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{5662EBC4-B2D5-4A7D-B65B-461A886A746A}",
											"idGrupoPontosMonitorados": "{3F228924-77F6-41FD-B1DC-25B5DB9B43A1}",
											"nome": "TT-GER-FE08",
											"descricao": null,
											"localizacao": "Ferro ponto 08",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{A9FDBF67-4BC3-417C-B57E-FA316A6AA462}",
											"idCanal": "{0143F014-E839-4A0B-9230-60F223EE7916}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{5662EBC4-B2D5-4A7D-B65B-461A886A746A}",
											"idGrupoPontosMonitorados": "{3F228924-77F6-41FD-B1DC-25B5DB9B43A1}",
											"nome": "TT-GER-FE09",
											"descricao": null,
											"localizacao": "Ferro ponto 09",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{C635233E-A2FE-416C-A418-6754A8DFD0A8}",
											"idCanal": "{F0612DF7-71CE-4B54-87CE-00BFD515FF0E}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{5662EBC4-B2D5-4A7D-B65B-461A886A746A}",
											"idGrupoPontosMonitorados": "{3F228924-77F6-41FD-B1DC-25B5DB9B43A1}",
											"nome": "TT-GER-FE11",
											"descricao": null,
											"localizacao": "Ferro ponto 11",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						},
						{
							"id": "{E7F6F756-29BB-4645-8AF5-2A5F2C4FB05D}",
							"idEquipamento": "{EFB8143D-C02E-4474-941B-1B0A943A2EE8}",
							"nome": "Injeção Óleo ME",
							"descricao": "Subsistema de injeção de óleo no ME",
							"componentes": [
								{
									"id": "{00C9B0CA-F800-4D03-9574-7F1A0F511F64}",
									"idSubsistema": "{E7F6F756-29BB-4645-8AF5-2A5F2C4FB05D}",
									"nome": "Bomba",
									"descricao": "Bomba de injeção de óleo do ME",
									"pontosMonitorados": [
										{
											"id": "{DB4DE0A0-3DEB-4954-AE8A-A9BB266DF15C}",
											"idCanal": "{1EF20F1D-CACB-4241-8870-846F38D5CAC7}",
											"idTipoSensor": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
											"idPlanoMedicao": null,
											"idComponente": "{00C9B0CA-F800-4D03-9574-7F1A0F511F64}",
											"idGrupoPontosMonitorados": "{7313A727-12F8-48B3-AAF8-60277BD00DED}",
											"nome": "TL-ME-INJ_OL_B1PRINC",
											"descricao": null,
											"localizacao": "Mancal de Escora",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
												"nome": "outros",
												"tipoSensor": 4011,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{076E01A9-40B3-4AF3-99ED-F550537B8383}",
											"idCanal": "{3D1EDE61-6466-41D0-ADA5-713AB1E35D3D}",
											"idTipoSensor": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
											"idPlanoMedicao": null,
											"idComponente": "{00C9B0CA-F800-4D03-9574-7F1A0F511F64}",
											"idGrupoPontosMonitorados": "{7313A727-12F8-48B3-AAF8-60277BD00DED}",
											"nome": "TL-ME-INJ_OL_B2PRINC",
											"descricao": null,
											"localizacao": "Mancal de Escora",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
												"nome": "outros",
												"tipoSensor": 4011,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						},
						{
							"id": "{E1984891-CF07-4638-A649-564F0BA64D46}",
							"idEquipamento": "{EFB8143D-C02E-4474-941B-1B0A943A2EE8}",
							"nome": "ME",
							"descricao": "Mancal de escora",
							"componentes": [
								{
									"id": "{4E5FA6C8-FE99-4108-BD26-DC6542152A6B}",
									"idSubsistema": "{E1984891-CF07-4638-A649-564F0BA64D46}",
									"nome": "Cuba",
									"descricao": "Cuba de óleo do ME",
									"pontosMonitorados": [
										{
											"id": "{E5107449-6F0A-4692-868E-06168B0F19A6}",
											"idCanal": "{EAFD409D-DBAE-4682-B909-D683B1BBA466}",
											"idTipoSensor": "{E096C366-B10F-4793-9641-5B49128F43EC}",
											"idPlanoMedicao": null,
											"idComponente": "{4E5FA6C8-FE99-4108-BD26-DC6542152A6B}",
											"idGrupoPontosMonitorados": "{730806AC-50FA-457B-8F05-0BC57E602B5A}",
											"nome": "TN-ME-OL_CUBA",
											"descricao": "",
											"localizacao": "Cuba",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{E096C366-B10F-4793-9641-5B49128F43EC}",
												"nome": "Transdutor de Nível (%)",
												"tipoSensor": 4007,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{959F04FF-3C48-48C7-894A-EFCF9191784C}",
											"idCanal": "{EB6B236A-395F-4C68-A352-72C6CB9634A9}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{4E5FA6C8-FE99-4108-BD26-DC6542152A6B}",
											"idGrupoPontosMonitorados": "{45616DFD-D721-4E1D-B53B-7FFC2CB08766}",
											"nome": "TT-ME-OL_CUBA",
											"descricao": null,
											"localizacao": "Cuba",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{354AFB26-6BD3-4DCC-B01B-BC9A8EADC39D}",
									"idSubsistema": "{E1984891-CF07-4638-A649-564F0BA64D46}",
									"nome": "Segmentos",
									"descricao": "Segmentos do ME",
									"pontosMonitorados": [
										{
											"id": "{7441BFE7-7F3C-42B4-9EEF-338DD31D770D}",
											"idCanal": "{E36D1FF3-4999-4F0B-A7BE-46379EC71F92}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{354AFB26-6BD3-4DCC-B01B-BC9A8EADC39D}",
											"idGrupoPontosMonitorados": "{08470672-FF9A-4F60-985A-5F15DD2EC877}",
											"nome": "TT-ME-SEG01",
											"descricao": null,
											"localizacao": "Segmento 01",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{FFB3EAC1-0048-46A7-B088-CE9458056BF5}",
											"idCanal": "{F3FFEE52-64E9-4475-BE76-329B971C9B85}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{354AFB26-6BD3-4DCC-B01B-BC9A8EADC39D}",
											"idGrupoPontosMonitorados": "{08470672-FF9A-4F60-985A-5F15DD2EC877}",
											"nome": "TT-ME-SEG03",
											"descricao": null,
											"localizacao": "Segmento 03",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{EB64C2B0-D8EE-4AA5-93C1-28A77F23D534}",
											"idCanal": "{30663AA1-9940-4C2E-B455-A1246B50FD98}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{354AFB26-6BD3-4DCC-B01B-BC9A8EADC39D}",
											"idGrupoPontosMonitorados": "{08470672-FF9A-4F60-985A-5F15DD2EC877}",
											"nome": "TT-ME-SEG05",
											"descricao": null,
											"localizacao": "Segmento 05",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{4B45A289-1E9E-447F-83A2-DDE6C706724E}",
											"idCanal": "{EFF10A47-CF53-4D3E-9FAD-60ED6AE2D287}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{354AFB26-6BD3-4DCC-B01B-BC9A8EADC39D}",
											"idGrupoPontosMonitorados": "{08470672-FF9A-4F60-985A-5F15DD2EC877}",
											"nome": "TT-ME-SEG07",
											"descricao": null,
											"localizacao": "Segmento 07",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{78B5D1EA-8FCE-465C-80B3-5A98F63A38FF}",
											"idCanal": "{EF20616F-F99D-4CEF-9023-060CAB649F9A}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{354AFB26-6BD3-4DCC-B01B-BC9A8EADC39D}",
											"idGrupoPontosMonitorados": "{08470672-FF9A-4F60-985A-5F15DD2EC877}",
											"nome": "TT-ME-SEG09",
											"descricao": null,
											"localizacao": "Segmento 09",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{289A8F66-55E7-496C-8BEC-A124A3D5842F}",
											"idCanal": "{03BAE59C-FC36-4F1C-A3A4-97978F83B6D3}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{354AFB26-6BD3-4DCC-B01B-BC9A8EADC39D}",
											"idGrupoPontosMonitorados": "{08470672-FF9A-4F60-985A-5F15DD2EC877}",
											"nome": "TT-ME-SEG11",
											"descricao": null,
											"localizacao": "Segmento 11",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{49893203-3569-4612-8A17-2F98BBDFAAF2}",
											"idCanal": "{E718B4E3-FC7C-4A3F-9536-2F3956E1E5FD}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{354AFB26-6BD3-4DCC-B01B-BC9A8EADC39D}",
											"idGrupoPontosMonitorados": "{08470672-FF9A-4F60-985A-5F15DD2EC877}",
											"nome": "TT-ME-SEG13",
											"descricao": null,
											"localizacao": "Segmento 13",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{09A62FA0-B437-42B0-B354-25E61E69BDFF}",
											"idCanal": "{794449B2-815C-47C7-BEAA-3E73CD6AF757}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{354AFB26-6BD3-4DCC-B01B-BC9A8EADC39D}",
											"idGrupoPontosMonitorados": "{08470672-FF9A-4F60-985A-5F15DD2EC877}",
											"nome": "TT-ME-SEG15",
											"descricao": null,
											"localizacao": "Segmento 15",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						},
						{
							"id": "{EBE58FA1-B34C-4CFA-8C3B-7605BD7BCB43}",
							"idEquipamento": "{EFB8143D-C02E-4474-941B-1B0A943A2EE8}",
							"nome": "MGG",
							"descricao": "Mancal de guia do gerador",
							"componentes": [
								{
									"id": "{FA15260D-600D-4AD4-B1B0-252D999EA6C6}",
									"idSubsistema": "{EBE58FA1-B34C-4CFA-8C3B-7605BD7BCB43}",
									"nome": "Cuba",
									"descricao": "Cuba de óleo do MGG",
									"pontosMonitorados": [
										{
											"id": "{66887447-C2DA-444C-8EF5-2414B57C96B0}",
											"idCanal": "{323FEB07-33FD-4B57-A16A-105175A40F34}",
											"idTipoSensor": "{E096C366-B10F-4793-9641-5B49128F43EC}",
											"idPlanoMedicao": null,
											"idComponente": "{FA15260D-600D-4AD4-B1B0-252D999EA6C6}",
											"idGrupoPontosMonitorados": "{1043F68A-9935-4FD6-BD54-6418F5A69A30}",
											"nome": "TN-MGG-OL_CUBA",
											"descricao": "",
											"localizacao": "Cuba",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{E096C366-B10F-4793-9641-5B49128F43EC}",
												"nome": "Transdutor de Nível (%)",
												"tipoSensor": 4007,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{00D40CA5-DBEF-44F7-BDBA-722C550E3A7B}",
											"idCanal": "{D98EEEEF-F5FB-4A67-9B4B-995545EDD086}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{FA15260D-600D-4AD4-B1B0-252D999EA6C6}",
											"idGrupoPontosMonitorados": "{AED653F3-E111-41F7-BA67-09C40B63D62C}",
											"nome": "TT-MGG-OL_CUBA",
											"descricao": null,
											"localizacao": "Cuba",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{CEF5490E-3200-4EF9-BA7C-3241749A3761}",
											"idCanal": "{5A63ACF3-FBFD-49BB-A725-C282563752A9}",
											"idTipoSensor": "{E38C8E96-479C-48AF-BD35-DBA7A535C3D1}",
											"idPlanoMedicao": null,
											"idComponente": "{FA15260D-600D-4AD4-B1B0-252D999EA6C6}",
											"idGrupoPontosMonitorados": "{C6790CEA-4CCF-41B3-9D46-0D5DD411C3CC}",
											"nome": "TV-MGG-OL_CUBA",
											"descricao": null,
											"localizacao": "Cuba",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "cm³/s",
												"id": "{E38C8E96-479C-48AF-BD35-DBA7A535C3D1}",
												"nome": "Transdutor de Vazão",
												"tipoSensor": 4008,
												"unidade": 69030,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{3AF645C0-7F0C-4752-8BB7-E286421E866D}",
									"idSubsistema": "{EBE58FA1-B34C-4CFA-8C3B-7605BD7BCB43}",
									"nome": "Eixo",
									"descricao": "Eixo",
									"pontosMonitorados": [
										{
											"id": "{3C3F9D27-8FD5-4197-9EDF-5A91BB35A7EA}",
											"idCanal": "{15F72FD6-0B96-41A4-851A-2751DC1359F5}",
											"idTipoSensor": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
											"idPlanoMedicao": null,
											"idComponente": "{3AF645C0-7F0C-4752-8BB7-E286421E866D}",
											"idGrupoPontosMonitorados": null,
											"nome": "FASOR-X",
											"descricao": null,
											"localizacao": "Acima do mancal",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "µm",
												"id": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
												"nome": "Proximidade",
												"tipoSensor": 4000,
												"unidade": 69004,
												"taxaAmostragem": 125,
												"nroAmostras": 4096
											}
										},
										{
											"id": "{70E357D0-20B8-4584-9BD7-5134B11A3E3C}",
											"idCanal": "{103A8D08-8753-446A-A9E4-14FF68439ADD}",
											"idTipoSensor": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
											"idPlanoMedicao": "{549552E1-7AFE-40F7-99A5-3F9053744B1A}",
											"idComponente": "{3AF645C0-7F0C-4752-8BB7-E286421E866D}",
											"idGrupoPontosMonitorados": "{1D8BDF94-7C3B-4BC9-B82C-57943173C1AB}",
											"nome": "SD1-MGG-000R-X",
											"descricao": "JUSANTE",
											"localizacao": "Suporte esp no mancal",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "µm",
												"id": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
												"nome": "Proximidade",
												"tipoSensor": 4000,
												"unidade": 69004,
												"taxaAmostragem": 125,
												"nroAmostras": 4096
											}
										},
										{
											"id": "{11D698D5-A5DB-46A4-8D8C-C944B3774AF8}",
											"idCanal": "{9F292996-82C9-429E-96FB-0F29366E1C03}",
											"idTipoSensor": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
											"idPlanoMedicao": "{549552E1-7AFE-40F7-99A5-3F9053744B1A}",
											"idComponente": "{3AF645C0-7F0C-4752-8BB7-E286421E866D}",
											"idGrupoPontosMonitorados": "{1D8BDF94-7C3B-4BC9-B82C-57943173C1AB}",
											"nome": "SD1-MGG-090R-Y",
											"descricao": "margem Esquerda",
											"localizacao": "Suporte esp no mancal",
											"direcao": 90,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "µm",
												"id": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
												"nome": "Proximidade",
												"tipoSensor": 4000,
												"unidade": 69004,
												"taxaAmostragem": 125,
												"nroAmostras": 4096
											}
										}
									]
								},
								{
									"id": "{63CAE046-783E-4446-B1FC-85F9835367AD}",
									"idSubsistema": "{EBE58FA1-B34C-4CFA-8C3B-7605BD7BCB43}",
									"nome": "Segmentos",
									"descricao": "Segmentos do MGG",
									"pontosMonitorados": [
										{
											"id": "{E03A8A3A-C153-4EBE-930F-B3C0A8B3494B}",
											"idCanal": "{E6983D87-0B73-4348-8A99-5C36A759F4F6}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{63CAE046-783E-4446-B1FC-85F9835367AD}",
											"idGrupoPontosMonitorados": "{0F0C5523-B7E8-4817-A580-F6EEC5C84ED8}",
											"nome": "TT-MGG-SEG01",
											"descricao": null,
											"localizacao": "Segmento 01",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{7DAE7666-04C5-4CB9-8DF1-8615A6352299}",
											"idCanal": "{4D4C061B-6983-4DA2-BA03-F3BFFDDB0E18}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{63CAE046-783E-4446-B1FC-85F9835367AD}",
											"idGrupoPontosMonitorados": "{0F0C5523-B7E8-4817-A580-F6EEC5C84ED8}",
											"nome": "TT-MGG-SEG02",
											"descricao": null,
											"localizacao": "Segmento 02",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{AB561FF8-5AB6-42C5-84BF-037805418FEA}",
											"idCanal": "{7108CAE6-A308-4C80-9313-78F3B5C65CED}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{63CAE046-783E-4446-B1FC-85F9835367AD}",
											"idGrupoPontosMonitorados": "{0F0C5523-B7E8-4817-A580-F6EEC5C84ED8}",
											"nome": "TT-MGG-SEG03",
											"descricao": null,
											"localizacao": "Segmento 03",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{3DB0203D-6E5B-4700-A596-1D9C3C36F4A9}",
											"idCanal": "{17969EC3-2D16-47CB-88D1-D46A93D9ABDB}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{63CAE046-783E-4446-B1FC-85F9835367AD}",
											"idGrupoPontosMonitorados": "{0F0C5523-B7E8-4817-A580-F6EEC5C84ED8}",
											"nome": "TT-MGG-SEG05",
											"descricao": null,
											"localizacao": "Segmento 05",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{B2FC22EA-B1F2-48CA-B400-C2957F964E37}",
											"idCanal": "{0745FFAE-BC68-4BB3-A824-49796DEE4A02}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{63CAE046-783E-4446-B1FC-85F9835367AD}",
											"idGrupoPontosMonitorados": "{0F0C5523-B7E8-4817-A580-F6EEC5C84ED8}",
											"nome": "TT-MGG-SEG06",
											"descricao": null,
											"localizacao": "Segmento 06",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{EFC91412-9184-4984-9275-00D25E688630}",
											"idCanal": "{AC5B4D5E-D405-466C-A8E1-6F4B0936544A}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{63CAE046-783E-4446-B1FC-85F9835367AD}",
											"idGrupoPontosMonitorados": "{0F0C5523-B7E8-4817-A580-F6EEC5C84ED8}",
											"nome": "TT-MGG-SEG08",
											"descricao": null,
											"localizacao": "Segmento 08",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						},
						{
							"id": "{78932000-7EAE-412C-B30C-BFB8CB0F0A50}",
							"idEquipamento": "{EFB8143D-C02E-4474-941B-1B0A943A2EE8}",
							"nome": "MGT",
							"descricao": "Mancal de guia da turbina",
							"componentes": [
								{
									"id": "{C2203FEA-EB9C-4EA7-B4CB-CC00A3D29B07}",
									"idSubsistema": "{78932000-7EAE-412C-B30C-BFB8CB0F0A50}",
									"nome": "Cuba",
									"descricao": "Cuba de óleo do MGT",
									"pontosMonitorados": [
										{
											"id": "{010063D4-7413-439D-A805-1A84AEDC093A}",
											"idCanal": "{8C4441BB-B1AF-4815-99D0-B9DEA1F16141}",
											"idTipoSensor": "{E096C366-B10F-4793-9641-5B49128F43EC}",
											"idPlanoMedicao": null,
											"idComponente": "{C2203FEA-EB9C-4EA7-B4CB-CC00A3D29B07}",
											"idGrupoPontosMonitorados": "{2ECF3E3E-759F-4846-AB8D-F17E117FEF6F}",
											"nome": "TN-MGT-OL_CUBA",
											"descricao": "",
											"localizacao": "Cuba",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{E096C366-B10F-4793-9641-5B49128F43EC}",
												"nome": "Transdutor de Nível (%)",
												"tipoSensor": 4007,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{BF5C57C1-17BA-4D31-9404-E1721CBDE479}",
											"idCanal": "{7708D3C2-04C0-4CA2-8546-6F2234787479}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{C2203FEA-EB9C-4EA7-B4CB-CC00A3D29B07}",
											"idGrupoPontosMonitorados": "{4097AADF-7193-455D-876A-C4DA9212DFE6}",
											"nome": "TT-MGT-OL_CUBA",
											"descricao": "",
											"localizacao": "Cuba",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{3243E5F1-D8DD-4A83-B830-188B31BE83AE}",
											"idCanal": "{3E28CCE8-3877-4F43-B81D-751193967AA3}",
											"idTipoSensor": "{E38C8E96-479C-48AF-BD35-DBA7A535C3D1}",
											"idPlanoMedicao": null,
											"idComponente": "{C2203FEA-EB9C-4EA7-B4CB-CC00A3D29B07}",
											"idGrupoPontosMonitorados": "{BA893247-8F3D-4C36-A1DD-D109A430566E}",
											"nome": "TV-MGT-OL_CUBA",
											"descricao": null,
											"localizacao": "Cuba",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "cm³/s",
												"id": "{E38C8E96-479C-48AF-BD35-DBA7A535C3D1}",
												"nome": "Transdutor de Vazão",
												"tipoSensor": 4008,
												"unidade": 69030,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{97A7C58C-1274-406F-961F-83DD15A376A7}",
									"idSubsistema": "{78932000-7EAE-412C-B30C-BFB8CB0F0A50}",
									"nome": "Eixo",
									"descricao": "Eixo",
									"pontosMonitorados": [
										{
											"id": "{06732887-77BC-47D7-9EBA-AFF5931CD7D7}",
											"idCanal": "{10551EAD-A44B-499D-AF2C-B951CEA1D3C6}",
											"idTipoSensor": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
											"idPlanoMedicao": "{94EFAE9E-E30F-446C-917A-72C4722D13C0}",
											"idComponente": "{97A7C58C-1274-406F-961F-83DD15A376A7}",
											"idGrupoPontosMonitorados": "{1D8BDF94-7C3B-4BC9-B82C-57943173C1AB}",
											"nome": "SD3-MGT-000R-X",
											"descricao": null,
											"localizacao": "Suporte esp no mancal",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "µm",
												"id": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
												"nome": "Proximidade",
												"tipoSensor": 4000,
												"unidade": 69004,
												"taxaAmostragem": 125,
												"nroAmostras": 4096
											}
										},
										{
											"id": "{990EC5F7-F5E0-412C-AA78-2BB5AEC793EF}",
											"idCanal": "{2EC91B12-82F5-414E-B9F2-E16B7C9DD799}",
											"idTipoSensor": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
											"idPlanoMedicao": "{94EFAE9E-E30F-446C-917A-72C4722D13C0}",
											"idComponente": "{97A7C58C-1274-406F-961F-83DD15A376A7}",
											"idGrupoPontosMonitorados": "{1D8BDF94-7C3B-4BC9-B82C-57943173C1AB}",
											"nome": "SD3-MGT-090R-Y",
											"descricao": null,
											"localizacao": "Suporte esp no mancal",
											"direcao": 90,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "µm",
												"id": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
												"nome": "Proximidade",
												"tipoSensor": 4000,
												"unidade": 69004,
												"taxaAmostragem": 125,
												"nroAmostras": 4096
											}
										},
										{
											"id": "{485D530B-EB03-4739-9554-7D4C8E17AC96}",
											"idCanal": "{171C62A9-0D48-4ADD-9E90-B8C2E75F2D12}",
											"idTipoSensor": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
											"idPlanoMedicao": null,
											"idComponente": "{97A7C58C-1274-406F-961F-83DD15A376A7}",
											"idGrupoPontosMonitorados": "{1D8BDF94-7C3B-4BC9-B82C-57943173C1AB}",
											"nome": "SD4-MGT-AX",
											"descricao": null,
											"localizacao": "Suporte esp próximo ao  MGT",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "µm",
												"id": "{6EF1C1F3-C4F5-47DB-A060-262F4DB3F78F}",
												"nome": "Proximidade",
												"tipoSensor": 4000,
												"unidade": 69004,
												"taxaAmostragem": 125,
												"nroAmostras": 4096
											}
										}
									]
								},
								{
									"id": "{3C413FD7-F73F-4CF6-8F35-8A7B249D2D24}",
									"idSubsistema": "{78932000-7EAE-412C-B30C-BFB8CB0F0A50}",
									"nome": "Segmentos",
									"descricao": "Segmentos do MGT",
									"pontosMonitorados": [
										{
											"id": "{CA21BEDF-28B1-4C3A-9E45-F5B569347F02}",
											"idCanal": "{CD807883-CFF1-4598-95FE-629CD0B9D0C9}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{3C413FD7-F73F-4CF6-8F35-8A7B249D2D24}",
											"idGrupoPontosMonitorados": "{557FEA5D-BF59-4293-8F1D-31D262C3FCFA}",
											"nome": "TT-MGT-SEG01",
											"descricao": null,
											"localizacao": "Segmento 01",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{B4092A6A-8620-46B3-8FB4-7C85645395B8}",
											"idCanal": "{49946E75-F97A-47F7-BA40-9F28669692D4}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{3C413FD7-F73F-4CF6-8F35-8A7B249D2D24}",
											"idGrupoPontosMonitorados": "{557FEA5D-BF59-4293-8F1D-31D262C3FCFA}",
											"nome": "TT-MGT-SEG02",
											"descricao": null,
											"localizacao": "Segmento 02",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{B3A49D89-D420-404B-96B3-3A1C8CFC6AE4}",
											"idCanal": "{427A6C01-A2A2-40B3-8A94-EEE7F1E4E5FA}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{3C413FD7-F73F-4CF6-8F35-8A7B249D2D24}",
											"idGrupoPontosMonitorados": "{557FEA5D-BF59-4293-8F1D-31D262C3FCFA}",
											"nome": "TT-MGT-SEG03",
											"descricao": null,
											"localizacao": "Segmento 03",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{094E7BC2-990C-4BA2-8E4D-D836D7D922A4}",
											"idCanal": "{FC02F872-F179-4017-A7DC-C633F05D65DF}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{3C413FD7-F73F-4CF6-8F35-8A7B249D2D24}",
											"idGrupoPontosMonitorados": "{557FEA5D-BF59-4293-8F1D-31D262C3FCFA}",
											"nome": "TT-MGT-SEG05",
											"descricao": null,
											"localizacao": "Segmento 05",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						},
						{
							"id": "{0D481E3F-0EC4-40D5-BF87-953C05A01FFD}",
							"idEquipamento": "{EFB8143D-C02E-4474-941B-1B0A943A2EE8}",
							"nome": "Regulador de velocidade",
							"descricao": "Subsistema do regulador de velocidade",
							"componentes": [
								{
									"id": "{27A924BE-B3D3-4B89-8108-CCE903C4664C}",
									"idSubsistema": "{0D481E3F-0EC4-40D5-BF87-953C05A01FFD}",
									"nome": "Bomba",
									"descricao": "Bombas do regulador de velocidade",
									"pontosMonitorados": [
										{
											"id": "{95F23053-80F9-4F61-8029-D77E01CEC1B9}",
											"idCanal": null,
											"idTipoSensor": "{E4ED1EB9-2172-4EFA-8B0C-D8FC50FAB02C}",
											"idPlanoMedicao": null,
											"idComponente": "{27A924BE-B3D3-4B89-8108-CCE903C4664C}",
											"idGrupoPontosMonitorados": "{D0B0F7BE-6A92-4BD9-8C1F-4651599D4318}",
											"nome": "SV-RV-CIRC_OL-MIN",
											"descricao": "Ponto adicionado porque coleta direta é feita pelo PLC e esta em segundos",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "s",
												"id": "{E4ED1EB9-2172-4EFA-8B0C-D8FC50FAB02C}",
												"nome": "Intermitência",
												"tipoSensor": 4012,
												"unidade": 69014,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{E809D44D-6A37-4343-8365-27BED0946B52}",
											"idCanal": null,
											"idTipoSensor": "{E4ED1EB9-2172-4EFA-8B0C-D8FC50FAB02C}",
											"idPlanoMedicao": null,
											"idComponente": "{27A924BE-B3D3-4B89-8108-CCE903C4664C}",
											"idGrupoPontosMonitorados": "{0AB07AF6-5F37-473E-A73D-C2A2AA41898B}",
											"nome": "SV-RV-REP_OL-MIN",
											"descricao": "Ponto adicionado porque coleta direta é feita pelo PLC e esta em segundos",
											"localizacao": "",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "s",
												"id": "{E4ED1EB9-2172-4EFA-8B0C-D8FC50FAB02C}",
												"nome": "Intermitência",
												"tipoSensor": 4012,
												"unidade": 69014,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{34AA02CB-E517-4B7C-8AA1-EA4E4DC39F19}",
											"idCanal": "{8DF397A6-8395-4F64-A75A-C603AD4E25C0}",
											"idTipoSensor": "{E4ED1EB9-2172-4EFA-8B0C-D8FC50FAB02C}",
											"idPlanoMedicao": null,
											"idComponente": "{27A924BE-B3D3-4B89-8108-CCE903C4664C}",
											"idGrupoPontosMonitorados": null,
											"nome": "TI-RV-CIRC_OL",
											"descricao": "",
											"localizacao": "Bombas RV",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "s",
												"id": "{E4ED1EB9-2172-4EFA-8B0C-D8FC50FAB02C}",
												"nome": "Intermitência",
												"tipoSensor": 4012,
												"unidade": 69014,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{42A02005-289B-4CA6-88E1-161C74FCAA7D}",
											"idCanal": "{00619BDD-F3B3-4089-ACCD-F52EB442C88A}",
											"idTipoSensor": "{E4ED1EB9-2172-4EFA-8B0C-D8FC50FAB02C}",
											"idPlanoMedicao": null,
											"idComponente": "{27A924BE-B3D3-4B89-8108-CCE903C4664C}",
											"idGrupoPontosMonitorados": "{F3629985-A73A-404C-B506-177CF389A0FA}",
											"nome": "TI-RV-DESL-OLINF",
											"descricao": "",
											"localizacao": "Bomba de Infiltração de Óleo",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "s",
												"id": "{E4ED1EB9-2172-4EFA-8B0C-D8FC50FAB02C}",
												"nome": "Intermitência",
												"tipoSensor": 4012,
												"unidade": 69014,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{B0386AAE-EF1A-4C89-8F55-691170B0B56E}",
											"idCanal": "{7F6EE7B6-6BE5-4694-9AFC-F699984919EF}",
											"idTipoSensor": "{E4ED1EB9-2172-4EFA-8B0C-D8FC50FAB02C}",
											"idPlanoMedicao": null,
											"idComponente": "{27A924BE-B3D3-4B89-8108-CCE903C4664C}",
											"idGrupoPontosMonitorados": "{17034116-A61F-4130-ADD8-5CDD4B1D2160}",
											"nome": "TI-RV-LIG-OLINF",
											"descricao": "",
											"localizacao": "Bomba de Infiltração de Óleo",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "s",
												"id": "{E4ED1EB9-2172-4EFA-8B0C-D8FC50FAB02C}",
												"nome": "Intermitência",
												"tipoSensor": 4012,
												"unidade": 69014,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{E55A14D1-AB14-4701-9101-420AC1FFBFC8}",
											"idCanal": "{D7B6B695-99BB-473F-8204-AB4F2A1F0A2F}",
											"idTipoSensor": "{E4ED1EB9-2172-4EFA-8B0C-D8FC50FAB02C}",
											"idPlanoMedicao": null,
											"idComponente": "{27A924BE-B3D3-4B89-8108-CCE903C4664C}",
											"idGrupoPontosMonitorados": null,
											"nome": "TI-RV-REP_OL",
											"descricao": "",
											"localizacao": "Bombas RV",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "s",
												"id": "{E4ED1EB9-2172-4EFA-8B0C-D8FC50FAB02C}",
												"nome": "Intermitência",
												"tipoSensor": 4012,
												"unidade": 69014,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{D2E61E12-A28C-456E-8CE5-76715BC402A9}",
											"idCanal": "{37266D29-56DF-4ADF-BC14-B2628FCD5CC4}",
											"idTipoSensor": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
											"idPlanoMedicao": null,
											"idComponente": "{27A924BE-B3D3-4B89-8108-CCE903C4664C}",
											"idGrupoPontosMonitorados": "{7313A727-12F8-48B3-AAF8-60277BD00DED}",
											"nome": "TL-RV-B1PRINC",
											"descricao": null,
											"localizacao": "Regulador de Velocidade",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
												"nome": "outros",
												"tipoSensor": 4011,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{037B4980-8B3D-4ACA-B0BB-9BA6C6B4F865}",
											"idCanal": "{24E62685-0DB4-4D1D-B5FF-0DADBFBDC58A}",
											"idTipoSensor": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
											"idPlanoMedicao": null,
											"idComponente": "{27A924BE-B3D3-4B89-8108-CCE903C4664C}",
											"idGrupoPontosMonitorados": "{7313A727-12F8-48B3-AAF8-60277BD00DED}",
											"nome": "TL-RV-B2PRINC",
											"descricao": null,
											"localizacao": "Regulador de Velocidade",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
												"nome": "outros",
												"tipoSensor": 4011,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{0707C8AB-5666-41A9-9BF0-D0C94D48C8C8}",
									"idSubsistema": "{0D481E3F-0EC4-40D5-BF87-953C05A01FFD}",
									"nome": "Outros",
									"descricao": "Demais componentes do regulador de velocidade",
									"pontosMonitorados": [
										{
											"id": "{498D4772-A989-4660-8DBB-AABF180A4992}",
											"idCanal": "{BBDD204C-ED17-4B5C-A428-05EEF19ED777}",
											"idTipoSensor": "{88B04C27-09D3-4761-BB34-2A1A01353BB0}",
											"idPlanoMedicao": null,
											"idComponente": "{0707C8AB-5666-41A9-9BF0-D0C94D48C8C8}",
											"idGrupoPontosMonitorados": "{5FB27552-CB06-42EA-94D1-DE4507724344}",
											"nome": "Potencia Ativa",
											"descricao": "",
											"localizacao": "RV",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "MW",
												"id": "{88B04C27-09D3-4761-BB34-2A1A01353BB0}",
												"nome": "Potência",
												"tipoSensor": 4015,
												"unidade": 69098,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{E637CD47-C7F7-499A-BBAF-31C2414EA307}",
											"idCanal": "{BDF21D84-CE3E-4754-9E54-6291575AD8B0}",
											"idTipoSensor": "{C595F409-C6CF-43F1-8938-FD4B90E17F4C}",
											"idPlanoMedicao": null,
											"idComponente": "{0707C8AB-5666-41A9-9BF0-D0C94D48C8C8}",
											"idGrupoPontosMonitorados": null,
											"nome": "Queda",
											"descricao": null,
											"localizacao": "RV",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "m",
												"id": "{C595F409-C6CF-43F1-8938-FD4B90E17F4C}",
												"nome": "Transdutor de Queda",
												"tipoSensor": 4007,
												"unidade": 69001,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{D8D68122-4117-4BE9-B41C-64FA1F55FF68}",
											"idCanal": "{374CAC93-0475-4C61-AAFF-1308E838B04A}",
											"idTipoSensor": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
											"idPlanoMedicao": null,
											"idComponente": "{0707C8AB-5666-41A9-9BF0-D0C94D48C8C8}",
											"idGrupoPontosMonitorados": "{8D93E8D4-A310-4452-8148-785054F5DCD0}",
											"nome": "TE-UG-FREQ",
											"descricao": null,
											"localizacao": "Unidade Geradora",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
												"nome": "outros",
												"tipoSensor": 4011,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{27827BB3-BA71-436C-B9C5-635D70BA2099}",
											"idCanal": "{BBDD204C-ED17-4B5C-A428-05EEF19ED777}",
											"idTipoSensor": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
											"idPlanoMedicao": null,
											"idComponente": "{0707C8AB-5666-41A9-9BF0-D0C94D48C8C8}",
											"idGrupoPontosMonitorados": "{D05173E3-2BD2-4004-A4E1-B626BD04FA87}",
											"nome": "TE-UG-POT_AT",
											"descricao": null,
											"localizacao": "Unidade Geradora",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
												"nome": "outros",
												"tipoSensor": 4011,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{3F7FBE65-A45D-44A1-88BB-BE7784078079}",
											"idCanal": "{1A843610-6025-4DF6-B05A-2199A146FE4A}",
											"idTipoSensor": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
											"idPlanoMedicao": null,
											"idComponente": "{0707C8AB-5666-41A9-9BF0-D0C94D48C8C8}",
											"idGrupoPontosMonitorados": "{7313A727-12F8-48B3-AAF8-60277BD00DED}",
											"nome": "TL-UG-GER",
											"descricao": null,
											"localizacao": "Gerador",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
												"nome": "outros",
												"tipoSensor": 4011,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{AE5CEE34-6DE0-4C02-8A5F-DA7B5A5D22C1}",
											"idCanal": "{5D307632-30D1-4EB8-9C99-DAA665079C12}",
											"idTipoSensor": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
											"idPlanoMedicao": null,
											"idComponente": "{0707C8AB-5666-41A9-9BF0-D0C94D48C8C8}",
											"idGrupoPontosMonitorados": "{7313A727-12F8-48B3-AAF8-60277BD00DED}",
											"nome": "TL-UG-VAZIO",
											"descricao": null,
											"localizacao": "Unidade Geradora",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
												"nome": "outros",
												"tipoSensor": 4011,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{A63569B3-2517-4047-8703-60CDCDA01DDE}",
											"idCanal": "{5E6ED91C-A002-4EC5-A49E-54C00A3F410A}",
											"idTipoSensor": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
											"idPlanoMedicao": null,
											"idComponente": "{0707C8AB-5666-41A9-9BF0-D0C94D48C8C8}",
											"idGrupoPontosMonitorados": "{7313A727-12F8-48B3-AAF8-60277BD00DED}",
											"nome": "TL-UG-VAZIO_EXC",
											"descricao": null,
											"localizacao": "UG",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
												"nome": "outros",
												"tipoSensor": 4011,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{8B861C23-4203-4FCF-B0C1-FDE5959C26F8}",
											"idCanal": "{1B179562-DD98-4B29-AD1F-643AACDD4C91}",
											"idTipoSensor": "{E38C8E96-479C-48AF-BD35-DBA7A535C3D1}",
											"idPlanoMedicao": null,
											"idComponente": "{0707C8AB-5666-41A9-9BF0-D0C94D48C8C8}",
											"idGrupoPontosMonitorados": "{8D93E8D4-A310-4452-8148-785054F5DCD0}",
											"nome": "TV-UG-TURB",
											"descricao": null,
											"localizacao": "Unidade Geradora",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "cm³/s",
												"id": "{E38C8E96-479C-48AF-BD35-DBA7A535C3D1}",
												"nome": "Transdutor de Vazão",
												"tipoSensor": 4008,
												"unidade": 69030,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{A2F8BE8F-D056-4621-9A60-D356FAA9239D}",
									"idSubsistema": "{0D481E3F-0EC4-40D5-BF87-953C05A01FFD}",
									"nome": "Tanque",
									"descricao": "Tanque de óleo hidráulico do RV",
									"pontosMonitorados": [
										{
											"id": "{5DA51DF1-FA62-427B-A3AD-436F06122828}",
											"idCanal": "{A08491CD-E821-4696-946F-4A535E1254A8}",
											"idTipoSensor": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
											"idPlanoMedicao": null,
											"idComponente": "{A2F8BE8F-D056-4621-9A60-D356FAA9239D}",
											"idGrupoPontosMonitorados": "{D97B8389-23F1-4814-807D-405984ECCE1D}",
											"nome": "TN-ACUM-OLEO",
											"descricao": null,
											"localizacao": "Acumulador",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "mm",
												"id": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
												"nome": "Transdutor de Nivel (mm)",
												"tipoSensor": 4007,
												"unidade": 69003,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{C56BFB54-DC92-417B-8FB6-86826D0379DD}",
											"idCanal": "{C78291D0-7EF8-4BDE-93D6-0619B487C938}",
											"idTipoSensor": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
											"idPlanoMedicao": null,
											"idComponente": "{A2F8BE8F-D056-4621-9A60-D356FAA9239D}",
											"idGrupoPontosMonitorados": "{F516F74F-E122-47F6-AB13-AD88E339E49B}",
											"nome": "TN-RV-OLEO",
											"descricao": null,
											"localizacao": "Reservatório do RV",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "mm",
												"id": "{9C7F808A-4E5D-4691-AC85-7A59637152AD}",
												"nome": "Transdutor de Nivel (mm)",
												"tipoSensor": 4007,
												"unidade": 69003,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{ACC8F39A-8BAA-424D-B2FA-618771E7D0E8}",
											"idCanal": "{E9527F9E-80E1-4490-BF4A-99628871B030}",
											"idTipoSensor": "{E096C366-B10F-4793-9641-5B49128F43EC}",
											"idPlanoMedicao": null,
											"idComponente": "{A2F8BE8F-D056-4621-9A60-D356FAA9239D}",
											"idGrupoPontosMonitorados": "{BDF337D2-50D1-4501-A035-97B3BEC97CE7}",
											"nome": "TN-RV-TOI",
											"descricao": "",
											"localizacao": "Tanque de Infiltração",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{E096C366-B10F-4793-9641-5B49128F43EC}",
												"nome": "Transdutor de Nível (%)",
												"tipoSensor": 4007,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{2FB17C8F-045A-4BE6-A737-4533A12E4E5C}",
											"idCanal": "{0DD86476-BE1A-497D-A057-27975BD3F18F}",
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{A2F8BE8F-D056-4621-9A60-D356FAA9239D}",
											"idGrupoPontosMonitorados": "{F46BA040-CF3E-4451-A7E4-CBBB4E471A1A}",
											"nome": "TP-ACUM-OLEO",
											"descricao": null,
											"localizacao": "Acumulador",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{404124FE-7C46-44E6-A44D-8DC481DDABCB}",
											"idCanal": "{EA64A92C-128A-4E8C-9DD0-5DAB1DBC32AA}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{A2F8BE8F-D056-4621-9A60-D356FAA9239D}",
											"idGrupoPontosMonitorados": "{4097AADF-7193-455D-876A-C4DA9212DFE6}",
											"nome": "TT-RV-OLEO",
											"descricao": null,
											"localizacao": "Reservatório do RV",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						},
						{
							"id": "{A28D43CA-4608-492A-902B-6F45E82F5B09}",
							"idEquipamento": "{EFB8143D-C02E-4474-941B-1B0A943A2EE8}",
							"nome": "Resfriamento do Gerador",
							"descricao": "Subsistema de resfriamento do gerador",
							"componentes": [
								{
									"id": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
									"idSubsistema": "{A28D43CA-4608-492A-902B-6F45E82F5B09}",
									"nome": "Trocador de calor",
									"descricao": "Trocadores de calor da carcaça do gerador",
									"pontosMonitorados": [
										{
											"id": "{B493F0E5-F482-4798-861E-D2E8CA948847}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{B101FF3D-3E55-4147-827D-A4B28AA0B2B9}",
											"nome": "SV-GER-DTAG",
											"descricao": "",
											"localizacao": "Trocador de Calor",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{A70B4161-8757-40C8-A817-5010BD46FD2F}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{CA36C972-8950-46DE-AA33-CE63E4A4086F}",
											"nome": "SV-GER-DTAR01",
											"descricao": "diferença de temperatura do ar do tc 01",
											"localizacao": "Trocador de Calor ponto 01",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{C54CF0F2-E6BC-4B18-BA11-B9CD73F60B73}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{CA36C972-8950-46DE-AA33-CE63E4A4086F}",
											"nome": "SV-GER-DTAR04",
											"descricao": "",
											"localizacao": "Trocador de Calor ponto 04",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{E79A0F09-6F0A-4DC7-98D2-03BDFC9D90FF}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{CA36C972-8950-46DE-AA33-CE63E4A4086F}",
											"nome": "SV-GER-DTAR07",
											"descricao": "",
											"localizacao": "Trocador de Calor ponto 07",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{E68FB937-2DE9-40F0-8ECA-8BCCDA9C4868}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{CA36C972-8950-46DE-AA33-CE63E4A4086F}",
											"nome": "SV-GER-DTAR10",
											"descricao": "",
											"localizacao": "Trocador de Calor ponto 10",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{AC4FAADA-36BD-4C44-BC05-B3FC4B57F41A}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{CA36C972-8950-46DE-AA33-CE63E4A4086F}",
											"nome": "SV-GER-DTAR13",
											"descricao": "",
											"localizacao": "Trocador de Calor ponto 13",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{806D4ADA-7B8C-41CF-A8B8-AACE0FD0919B}",
											"idCanal": null,
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{CA36C972-8950-46DE-AA33-CE63E4A4086F}",
											"nome": "SV-GER-DTAR16",
											"descricao": "",
											"localizacao": "Trocador de Calor ponto 16",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{6C03EF4C-EE55-4AA6-B1D8-F701DC12FB91}",
											"idCanal": "{5E5DB4D5-EB9F-493D-BD77-701D5340BE16}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{39040552-3990-42C7-9D7A-75FD95F070F2}",
											"nome": "TT-GER-AENT",
											"descricao": null,
											"localizacao": "Entrada dos TCs",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{BCCF2004-A29F-4DE9-B16E-A2D58349A68A}",
											"idCanal": "{2EC560A4-FBCD-41A2-BEA9-2C90228CB33F}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{415A4932-9ABC-4ECB-ADE9-E497B50965BE}",
											"nome": "TT-GER-AF01",
											"descricao": null,
											"localizacao": "Saída TC ponto 01",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{4B96D4A9-8AA6-4D20-9299-8057BFF36430}",
											"idCanal": "{B81C8109-2FD3-44FE-A382-8529E4AA8097}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{415A4932-9ABC-4ECB-ADE9-E497B50965BE}",
											"nome": "TT-GER-AF04",
											"descricao": null,
											"localizacao": "Saída TC ponto 04",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{D92A44EE-99C9-4A93-BB22-AE5700C531BB}",
											"idCanal": "{4FFD2AB3-220A-4896-83CE-CDD88F7CD622}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{415A4932-9ABC-4ECB-ADE9-E497B50965BE}",
											"nome": "TT-GER-AF07",
											"descricao": null,
											"localizacao": "Saída TC ponto 07",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{4D2D4D1B-38CD-4821-9EB0-87D18D47A105}",
											"idCanal": "{DE53C20E-3ED7-4B00-A3C8-3E03A477DF87}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{415A4932-9ABC-4ECB-ADE9-E497B50965BE}",
											"nome": "TT-GER-AF10",
											"descricao": null,
											"localizacao": "Saída TC ponto 10",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{7781F77A-A5F8-4C91-BA1E-D0D3274C0E01}",
											"idCanal": "{EBCA83A9-70C3-4261-9BA3-07F752AF351E}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{415A4932-9ABC-4ECB-ADE9-E497B50965BE}",
											"nome": "TT-GER-AF13",
											"descricao": null,
											"localizacao": "Saída TC ponto 13",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{3341AE4A-16E8-4515-B84E-77AED59BB69F}",
											"idCanal": "{D9DCBF1B-714F-4DEB-A4BD-897D436BD552}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{415A4932-9ABC-4ECB-ADE9-E497B50965BE}",
											"nome": "TT-GER-AF16",
											"descricao": null,
											"localizacao": "Saída TC ponto 16",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{1F587CF1-AB82-44BA-94CD-CD286C12A61B}",
											"idCanal": "{25429471-0745-4DC7-B8CF-EA0C80F68E6C}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{4C40A215-464F-4632-AB22-F83CA6A77C3D}",
											"nome": "TT-GER-AQ01",
											"descricao": null,
											"localizacao": "EntradaTC ponto 01",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{11B2B6F0-ECCE-49D3-84E2-8210AD0B933A}",
											"idCanal": "{8BDB2F5E-4C5A-4854-8D7B-197967217251}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{4C40A215-464F-4632-AB22-F83CA6A77C3D}",
											"nome": "TT-GER-AQ04",
											"descricao": null,
											"localizacao": "EntradaTC ponto 04",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{0A0CEA15-E053-46CD-825A-BE704730E0E3}",
											"idCanal": "{FC396ECD-519C-4736-89ED-5FFBD0DBE4B2}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{4C40A215-464F-4632-AB22-F83CA6A77C3D}",
											"nome": "TT-GER-AQ07",
											"descricao": null,
											"localizacao": "EntradaTC ponto 07",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{1094780D-17B6-42F4-A504-5B88D5F311DD}",
											"idCanal": "{0E908766-8726-4D15-B595-8416CCA239E0}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{4C40A215-464F-4632-AB22-F83CA6A77C3D}",
											"nome": "TT-GER-AQ10",
											"descricao": null,
											"localizacao": "EntradaTC ponto 10",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{8DDC9522-0AD5-4255-AB7F-3BD3F59D7A0E}",
											"idCanal": "{C5FBF096-526E-4B00-80E7-E6D974F127C3}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{4C40A215-464F-4632-AB22-F83CA6A77C3D}",
											"nome": "TT-GER-AQ13",
											"descricao": null,
											"localizacao": "EntradaTC ponto 13",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{01381202-BA7F-460B-A69C-52D26FA45381}",
											"idCanal": "{A4DE7621-D4D3-4BDC-8624-B28B09CA8ED3}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{4C40A215-464F-4632-AB22-F83CA6A77C3D}",
											"nome": "TT-GER-AQ16",
											"descricao": null,
											"localizacao": "EntradaTC ponto 16",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{942BBD94-8CF5-4BCA-B8E8-659F14779983}",
											"idCanal": "{4BA65DF9-5FB9-4935-B1E9-5C71E29D3C07}",
											"idTipoSensor": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{A9CEE327-277B-4970-8ABC-8E47568C6DF1}",
											"nome": "TT-GER-ASAI",
											"descricao": null,
											"localizacao": "Saída dos TCs",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "º C",
												"id": "{A02CEA9B-908B-4C86-ABBD-3936C395CB8D}",
												"nome": "Termopar",
												"tipoSensor": 4005,
												"unidade": 69075,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{06F96498-3889-422F-92DA-6FFB129D4F10}",
											"idCanal": "{454AE0DA-46A1-4393-9E49-F6990DB39263}",
											"idTipoSensor": "{E38C8E96-479C-48AF-BD35-DBA7A535C3D1}",
											"idPlanoMedicao": null,
											"idComponente": "{F5418479-22DE-493D-B967-4D8D9C592C4C}",
											"idGrupoPontosMonitorados": "{B00BD986-C862-481F-A82A-031453ED0335}",
											"nome": "TV-GER-AGUA",
											"descricao": null,
											"localizacao": "Entrada dos TCs",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "cm³/s",
												"id": "{E38C8E96-479C-48AF-BD35-DBA7A535C3D1}",
												"nome": "Transdutor de Vazão",
												"tipoSensor": 4008,
												"unidade": 69030,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						},
						{
							"id": "{029A89B0-FFF1-45D1-8320-E61B04A98408}",
							"idEquipamento": "{EFB8143D-C02E-4474-941B-1B0A943A2EE8}",
							"nome": "Turbina",
							"descricao": "Turbina",
							"componentes": [
								{
									"id": "{A705547A-BA3F-4023-8034-D277012523A8}",
									"idSubsistema": "{029A89B0-FFF1-45D1-8320-E61B04A98408}",
									"nome": "caixa espiral",
									"descricao": "caixa espiral",
									"pontosMonitorados": [
										{
											"id": "{60AF1DF9-0F57-4FFD-80EE-699CFB4505AE}",
											"idCanal": "{74FDA0EA-459A-453C-8FE8-CA471130B9B5}",
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{A705547A-BA3F-4023-8034-D277012523A8}",
											"idGrupoPontosMonitorados": "{5DD0FD68-CF09-4BE7-B5BE-FC4D93CB6D8E}",
											"nome": "TP-T-CXE",
											"descricao": null,
											"localizacao": "Caixa Espiral",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{D023774E-155C-44DB-9DBD-221833F0E818}",
											"idCanal": "{2D252D97-0F4A-431B-A516-95B56489C357}",
											"idTipoSensor": "{E38C8E96-479C-48AF-BD35-DBA7A535C3D1}",
											"idPlanoMedicao": null,
											"idComponente": "{A705547A-BA3F-4023-8034-D277012523A8}",
											"idGrupoPontosMonitorados": "{3B84C1A7-4437-42D4-AEDC-2CA3DF21652D}",
											"nome": "TV-T-CXE",
											"descricao": null,
											"localizacao": "Caixa Espiral",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "cm³/s",
												"id": "{E38C8E96-479C-48AF-BD35-DBA7A535C3D1}",
												"nome": "Transdutor de Vazão",
												"tipoSensor": 4008,
												"unidade": 69030,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{F7D29B4B-5E99-4C75-9E47-E26E44C1C2CF}",
									"idSubsistema": "{029A89B0-FFF1-45D1-8320-E61B04A98408}",
									"nome": "tampa da turbina",
									"descricao": "tampa da turbina",
									"pontosMonitorados": [
										{
											"id": "{40A42A54-3E10-45C9-A4F7-1CE757D3F253}",
											"idCanal": "{AB0109E8-5123-4308-AB27-AB76982C65A6}",
											"idTipoSensor": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
											"idPlanoMedicao": null,
											"idComponente": "{F7D29B4B-5E99-4C75-9E47-E26E44C1C2CF}",
											"idGrupoPontosMonitorados": "{3D00E8E2-9EB2-42B6-8EAA-8ED50603D58C}",
											"nome": "TI-T-DESL-AGUA",
											"descricao": "",
											"localizacao": "Tampa da Turbina",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
												"nome": "outros",
												"tipoSensor": 4011,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{29C41D3A-55A2-4AAB-8800-A2C073602541}",
											"idCanal": "{1E33A361-3BE7-4A8E-8A2F-BD1C1E58E6E8}",
											"idTipoSensor": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
											"idPlanoMedicao": null,
											"idComponente": "{F7D29B4B-5E99-4C75-9E47-E26E44C1C2CF}",
											"idGrupoPontosMonitorados": "{DBED8A3B-AF94-4E8A-9DFE-0A05476F0028}",
											"nome": "TI-T-LIG-AGUA",
											"descricao": "",
											"localizacao": "Tampa da Turbina",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
												"nome": "outros",
												"tipoSensor": 4011,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{CF8171DE-51EC-48BB-9391-B112CAD52D17}",
											"idCanal": "{F3E833A7-C0CB-4EC4-BE17-FC2AA3FD4A54}",
											"idTipoSensor": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
											"idPlanoMedicao": null,
											"idComponente": "{F7D29B4B-5E99-4C75-9E47-E26E44C1C2CF}",
											"idGrupoPontosMonitorados": "{7313A727-12F8-48B3-AAF8-60277BD00DED}",
											"nome": "TL-TT-AG_B1PRINC",
											"descricao": null,
											"localizacao": "Tampa da Turbina",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
												"nome": "outros",
												"tipoSensor": 4011,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{37276E1C-C113-406E-A79D-C7BDA68F9BE4}",
											"idCanal": "{79016D88-34DF-4B1B-A5B9-6D5015D165DD}",
											"idTipoSensor": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
											"idPlanoMedicao": null,
											"idComponente": "{F7D29B4B-5E99-4C75-9E47-E26E44C1C2CF}",
											"idGrupoPontosMonitorados": "{7313A727-12F8-48B3-AAF8-60277BD00DED}",
											"nome": "TL-TT-AG_B2PRINC",
											"descricao": null,
											"localizacao": "Tampa da Turbina",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{5F02611B-AFB1-4044-B075-E4CF76A6AA19}",
												"nome": "outros",
												"tipoSensor": 4011,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{AE43A179-067F-4D2E-8C06-7667F9FA8B83}",
											"idCanal": "{7CBCCE5B-589A-4A97-8857-D1A3B25C3589}",
											"idTipoSensor": "{E096C366-B10F-4793-9641-5B49128F43EC}",
											"idPlanoMedicao": null,
											"idComponente": "{F7D29B4B-5E99-4C75-9E47-E26E44C1C2CF}",
											"idGrupoPontosMonitorados": "{37A407A6-C8FC-4C73-A84B-F9DBB4A126F5}",
											"nome": "TN-T-AG01",
											"descricao": "",
											"localizacao": "Tampa da turbina",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{E096C366-B10F-4793-9641-5B49128F43EC}",
												"nome": "Transdutor de Nível (%)",
												"tipoSensor": 4007,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{30026468-F340-4E7A-912A-1F037AD87121}",
											"idCanal": "{7D0BD6C2-ED31-4E3D-9F07-5E04B0CE601C}",
											"idTipoSensor": "{E096C366-B10F-4793-9641-5B49128F43EC}",
											"idPlanoMedicao": null,
											"idComponente": "{F7D29B4B-5E99-4C75-9E47-E26E44C1C2CF}",
											"idGrupoPontosMonitorados": "{37A407A6-C8FC-4C73-A84B-F9DBB4A126F5}",
											"nome": "TN-T-AG02",
											"descricao": "",
											"localizacao": "Tampa da turbina",
											"direcao": 0,
											"ativo": 0,
											"tipoSensor": {
												"unidadeStr": "%",
												"id": "{E096C366-B10F-4793-9641-5B49128F43EC}",
												"nome": "Transdutor de Nível (%)",
												"tipoSensor": 4007,
												"unidade": 69135,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										},
										{
											"id": "{96934ACE-6F93-4BBF-A58D-4CA855E2E7F9}",
											"idCanal": "{1A414C0A-4B57-45D5-9268-60E85DE36680}",
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{F7D29B4B-5E99-4C75-9E47-E26E44C1C2CF}",
											"idGrupoPontosMonitorados": "{E43588DC-709A-466D-90A0-BD6B16718149}",
											"nome": "TP-T-TT",
											"descricao": null,
											"localizacao": "Tampa da Turbina",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{06531F7D-A08F-4946-9981-5883AA6A89FE}",
									"idSubsistema": "{029A89B0-FFF1-45D1-8320-E61B04A98408}",
									"nome": "tubo de succao",
									"descricao": "tubo de succao",
									"pontosMonitorados": [
										{
											"id": "{DC0729B1-9B83-445E-8073-28CA18D0B283}",
											"idCanal": "{5048786B-51E2-4DA7-834C-7D3F4801D2AC}",
											"idTipoSensor": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
											"idPlanoMedicao": null,
											"idComponente": "{06531F7D-A08F-4946-9981-5883AA6A89FE}",
											"idGrupoPontosMonitorados": "{58E2F95E-C0E0-47CA-B5F8-CF8198BDC942}",
											"nome": "TP-T-SUC",
											"descricao": null,
											"localizacao": "Tubo de Sucção",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "bar",
												"id": "{6A6374EF-6D06-421D-949B-12D1F607E8FA}",
												"nome": "Transdutor de Pressao Estatica",
												"tipoSensor": 4006,
												"unidade": 69087,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								},
								{
									"id": "{B6AEA75A-2168-4309-961D-B7FB16DA44ED}",
									"idSubsistema": "{029A89B0-FFF1-45D1-8320-E61B04A98408}",
									"nome": "turbina",
									"descricao": "turbina",
									"pontosMonitorados": [
										{
											"id": "{FBEB02DE-0E4A-4FD9-A388-286EEF946A6D}",
											"idCanal": "{7B078EFF-2691-444D-95E8-8675A47EF291}",
											"idTipoSensor": "{E38C8E96-479C-48AF-BD35-DBA7A535C3D1}",
											"idPlanoMedicao": null,
											"idComponente": "{B6AEA75A-2168-4309-961D-B7FB16DA44ED}",
											"idGrupoPontosMonitorados": "{AB3BCC42-364B-4D27-930F-CFF6C52D9384}",
											"nome": "TV-T-AGX",
											"descricao": null,
											"localizacao": "Gaxeta",
											"direcao": 0,
											"ativo": 1,
											"tipoSensor": {
												"unidadeStr": "cm³/s",
												"id": "{E38C8E96-479C-48AF-BD35-DBA7A535C3D1}",
												"nome": "Transdutor de Vazão",
												"tipoSensor": 4008,
												"unidade": 69030,
												"taxaAmostragem": 1,
												"nroAmostras": 1
											}
										}
									]
								}
							]
						}
					]
				}
			]
		}
	]
}  
```

**Exemplo no MDM:**\
[Árvore de análise](../images/ArvoreAnalise.jpg)
