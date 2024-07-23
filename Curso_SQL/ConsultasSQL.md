##  <center>Consultas Básicas no SQL</center>

Instruções como ``SELECT``,  ``FROM``,  ``WHERE`` para realizar consultas básicas em uma tablea usando SQL. Essas consultas nos permitem recuperar dados específicos de uma tabela, aplicando filtros e condições.

- Sintaxe básica do select

```SELECT coluna1, coluna2, ... From tabela;```

- **SELECT**: indica que queremos selecionar colunas específicas <br>
- **coluna1, coluna2**: são as colunas que desejamos recuperar da tabela <br>
- **FROM tabela**: especifica de qual tabela queremos recuperar os dados <br>

Para selecionar todas as colunas de uma tabela, utilizamos o caractere "``*``"`no lugar das colunas especificas:

```SELECT * FROM tabela;``` <br>
Isso retornará todos os registros e colunas presentes na tabela.

- Selecionando colunas específicas 

Se quisermos recuperar apenas colunas específicas da tabela, devemos listá-las separadas por vírgulas no select 

```SELECT coluna1, coluna2, FROM tabela;``` <br>
Isso retornará apenas as colunas mencionadas na consulta

- Filtros usando a cláusula WHERE

Para aplicar filtro e condições em nossas consultas, utilizamos a cláusula ``WHERE``. Ela permite definir condições que os registros devem atender para serem retornados. 