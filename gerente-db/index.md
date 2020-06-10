# Documentação Gerente DB

## Select

### Json de entrada

O Json de entrada deve conter:

```
{
  table: string; // O nome da tabela a consultar
  where?: [      // Array de condições para filtrar a consulta
    {      
      type?: string = 'and' | 'or'; // Se omitido será and
      condition: string;
      params: object;
    }
  ] 
  relations?: [ // Array de relacionamentos a incluir com inner join ou left join
    {  
      join: string = 'innerJoin' | 'leftJoin';
      relation: string;
      alias: string;  
    }
  ]
}
```
Os campos com "?" são opcionais.

#### Exemplo

```
{
  "table": "rota",
  "where": [
    {
      "condition": "idGrupoUsuario = :idGrupoUsuario",
      "param": { "idGrupoUsuario": "{1065F9D1-F24F-42A2-8A92-6B96A1C7CD79}" },
    },
    {
      "condition": "tipoRota = :tipoRota",
      "param": { "tipoRota": 110000 },
    },
  ],
  "relations": [
    {
      "join": "innerJoin",
      "relation": "rota.executaRota",
      "alias": "executaRota",
    },
  ],
}
 ```

Esta entrada produzirá a seguinte query:

```
select * from rota 
inner join executarota 
  on ROTA.ID = EXECUTAROTA.IDROTA
where ROTA.IDGRUPOUSUARIO = '{1065F9D1-F24F-42A2-8A92-6B96A1C7CD79}'
  and ROTA.TIPOROTA = 110000

```

