# Documentação Gerente DB

## Select

### Json de entrada

O Json de entrada deve conter:

```
{
  table: string; // O nome da tabela a consultar
  where?: {      // Condições para filtrar a consulta
    condition: string;
    params: object;
  } 
  relations?: {  // Relacionamentos a incluir com inner join ou left join
    join: string = 'innerJoin' | 'leftJoin';
    relation: string;
    alias: string;
  }
}
```
Os campos com "?" são opcionais.
