# Documentação Gerente DB

O Json de entrada de todos os comandos devem ter, **obrigatoriamente, o campo table.**

- **table**: O nome da tabela. Tipo dado: string; 

## Select

### Condição

- **where**: Json object. Condições para filtrar a consulta. **Comando opcional.** Sintaxe:

  - **type**: string. o tipo de conjunção entre condições. Valores permitidos: "and" | "or". Só é considerado da segunda condição em diante.
  - **condition**: string. A condição propriamente dita, no formato de query params.
  - **param**: Json object. Os valores dos parâmetros da query do campo acima. Sintaxe:
    - **nome do campo**: variant.
    
**Exemplo**
```
 "table": "rota",
 "where": [
   {
     "condition": "idGrupoUsuario = :idGrupoUsuario",
     "param": { "idGrupoUsuario": "{1065F9D1-F24F-42A2-8A92-6B96A1C7CD79}" },
   },
   {
     "condition": "tipoRota = :tipoRota",
     "param": { "tipoRota": 110000 },
     "type": "or"
   },
 ]
```

O exemplo acima produzirá a seguinte query:

```
select * from ROTA 
  where IDGRUPOUSUARIO = @0 OR TIPOROTA = @1; -- PARAMS: {@0: "{1065F9D1-F24F-42A2-8A92-6B96A1C7CD79}", @1: 110000}
```

### Relacionamentos

- **relations?**: Array Json para incluir como inner join ou left join. **Comando opcional.** Sintaxe:
  - **join**: string. Valores possíveis: "innerJoin" | "leftJoin"
  - **relation**: string. O nome da tabela de relacionamento.
  - **alias?**: string. O apelido da tabela de relacionamento.
  
**Exemplo**
```
 "table": "rota",
 "relations": [
   {
     "join": "innerJoin",
     "relation": "rota.executaRota",
     "alias": "executaRota"     
   },   
 ]
```

O exemplo acima produzirá a seguinte query:

```
select * from ROTA 
  inner join executaRota executaRota 
  on executaRota.idRota = ROTA.id;
```

### Ordenação

- **orderBy?**: Array para ordenação da consulta. **Comando opcional.** Sintaxe:
  - **field**: string. Nome do campo para ordenação.
  - **order?**: string. Campo para ordenação ascendente ou descendente. Valores permitidos: 'ASC' | 'DESC' (Atenção: Upper case!)
  
**Exemplo**
```
 "table": "rota",
 "orderBy": [
   {
     "field": "nome",     
   },
   {
     "field": "tipoRota",
     "order": 'DESC'
   },
 ]
```

O exemplo acima produzirá a seguinte query:

```
select * from ROTA 
  order by nome ASC, tipoRota DESC;
```

### Limitação de resultados

- **take?**: Limitação de resultados, equivale ao comando "top". **Comando opcional.**

**Exemplo**
```
 "table": "rota",
 "take": 10
```

O exemplo acima produzirá a seguinte query:

```
select top(10) * from ROTA;  
```

## Update

### Condição

- **where**: Json object. Condições para filtrar a consulta. **Comando opcional porém recomendável.** Sintaxe:

  - **type**: string. o tipo de conjunção entre condições. Valores permitidos: "and" | "or". Só é considerado da segunda condição em diante.
  - **condition**: string. A condição propriamente dita, no formato de query params.
  - **param**: Json object. Os valores dos parâmetros da query do campo acima. Sintaxe:
    - **nome do campo**: variant.
    
- **set**: Json object. Os valores para atualização. **Comando obrigatório.**
    
**Exemplo**
```
 "table": "rota",
 "where": [
   {
     "condition": "idGrupoUsuario = :idGrupoUsuario",
     "param": { "idGrupoUsuario": "{1065F9D1-F24F-42A2-8A92-6B96A1C7CD79}" },
   },   
 ]
 "set": { "tipoRota": 110002, "periodicidadeDias": 107000 }
```

O exemplo acima produzirá a seguinte query:

```
update from ROTA 
  set TIPOROTA = @0, PERIDICIDADEDIAS = @1 
  where idGrupoUsuario = @2 
  -- PARAMS: {@0: 110002, @1: 107000, @2: "{1065F9D1-F24F-42A2-8A92-6B96A1C7CD79}"}
```

## Insert

### valores

- **values**: Array de Json object com os valores a inserir. **Campo obrigatório.**
    
**Exemplo**
```
 "table": "rota",
 "values": [
   {
     "name": "Rota Posto 1 - Turno dia",
     "descricao": { "Rota turno do dia do posto 1" }
   },   
   {
     "name": "Rota Posto 1 - Turno noite",
     "descricao": { "Rota turno da noite do posto 1" }
   },
 ] 
```

O exemplo acima produzirá a seguinte query:

```
update from ROTA 
  set TIPOROTA = @0, PERIDICIDADEDIAS = @1 
  where idGrupoUsuario = @2 
  -- PARAMS: {@0: 110002, @1: 107000, @2: "{1065F9D1-F24F-42A2-8A92-6B96A1C7CD79}"}
```
