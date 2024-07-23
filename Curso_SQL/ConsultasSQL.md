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

```SELECT * FROM tabela WHERE coluna = valor;```
Isso retornará apenas os registros que atendem à condição especificada.

- Usando operadores de comparação

Podemos utilizar operadores de comparação para criar condições mais complexas em nossa cláusula WHERE. 

``=`` __igual a__ <br>
``<>`` __diferente de__ <br>
``<`` __menor que__ <br>
``>`` __maior que__ <br>
``<=`` __menor ou igual a__ <br>
``>=`` __maior ou igual a__ <br>

Na tabela Alunos suponha que tenha as colunas "nome", "idade" e "curso". Para selecionar todos os alunos com idade maior que 20, podemos usar a seguinte consulta: 

```SELECT * FROM Alunos WHERE idade > 20;```

- Filtro usando o operador LIKE

O operador LIKE é usado para fazer buscas com padrões em uma coluna

```SELECT * FROM tabela WHERE coluna LIKE 'valor%';``` <br>
Isso retornará os registros em que a coluna começa com o valor especificado.

Exemplo com a tabela Alunos:<br>
Suponha que a tabela Alunos tenha a coluna "nome". Para selecionar todos os alunos cujo nome comeca com "Jo", podemos usar

```SELECT * FROM Alunos WHERE nome LIKE 'Jo%';```

- Usando operadores lógicos 

Podemos combinar várias condições usando operadores lógicos, como ``AND`` e ``OR``

```SELECT * FROM tabela WHERE condicao1 AND condicao2;```<br>
Isso retornará os registros que atendem a ambas condições especificadas.
