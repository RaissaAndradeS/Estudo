## <center>Manipulando e organizando resultados de consulta no SQL</center>

Além das instruções básica de ``SELECT``, ``FROM`` e ``WHERE``, o SQL oferece diversas cláusulas adicionais que nos permitem manipular e organizar os resultados de nossas consultas de forma mais avançada. Aqui vamos explorar o ``ORDER BY``, ``GROUP BY``, ``HAVING``, ``JOIN`` e ``UNION``. 

### ORDEY BY em SQL
Permite ordenar os resultados da consulta como base em uma ou mais colunas.

 ```
 SELECT coluna1, coluna2, FROM tabela ORDER BY coluna1, ASC/DESC, coluna2 ASC/DESC;
 ```
 - ASC (Ascending) classifica em ordem crescente (padrão).
 - DESC (Descending) classifica em ordem decrescente.

 Por exemplo na tabela Alunos em ordem crescente de idade: <br>
 ``SELECT * FROM Alunos ORDER BY idade ASC; ``

 ### GROUP BY em SQL
 É usada para agrupar os resultados da consulta com base em uma ou mais colunas. É frequentemente combinada com funções de agregação, como ``COUNT``, ``SUM``, ``AVG``, ``MAX`` e ``MIN``. <br>
``SELECT coluna1, função(coluna2) FROM tabela GROUP BY coluna1;``

Para contar o número de alunos por curso na tabela Alunos: <br>
``SELECT curso_id, COUNT(*) FROM Alunos GROUPY BY curso_id;``

### HAVING em SQL
É usada para filtrar os resultados de uma consulta que contém uma cláusula ``GROUP BY``. Ela permite aplicar condições às funções de agregação. <br>
``SELECT coluna1, função(coluna2) FROM tabela GROUP BR coluna1 HAVING condição;``

Para selecionar os cursos com mais de 10 alunos na tabela Alunos: <br>
``SELECT curso_id, COUNT(*) FROM Alunos GROUP BY curso_id HAVING COUNT (*) > 10;``

### JOIN em SQL
É usada para combinar registros de duas ou mais tabelas com base em uma condição de associação. Existem vários tipos de joins, como ``INNER JOIN``, ``LEFT JOIN``, ``RIGHT JOIN`` e ``FULL JOIN``. A ``INNER JOIN``: <br>

``SELECT colunas FROM tabela1 JOIN tabela2 ON tabela1.coluna = tabela2.coluna; ``

Para selecionar os alunos com seus respectivos cursos da tabela Alunos e Cursos. <br>
``SELECT Alunos.nome, Cursos.nome FROM Alunos JOIN Cursos ON Alunos.cursos_id = Cursos.id; ``

### UNION em SQL
É usada para combinar o resultado de duas ou mais consultas em um único conjunto de resultados. As consultas devem ter a mesma estrutura de colunas. <br>

```
SELECT colunas FROM tabela1
UNION
SELECT colunas FROM tabela2
```

Para selecionar todos os alunos das tabelas Alunos e Parentes: <br>

```
SELECT nome FROM Alunos
UNION
SELECT nome FROM Parentes;
```

Essas são algumas cláusulas mais comuns para manipulação e organização de resultado de consulta. 

## Outros exemplos 

> ORDER BY: <br>
    > Ordem decrescente <br>
``SELECT * FROM Alunos ORDER BY nome DESC;``

> GROUP BY: <br>
    > Contar o número de alunos por curso e mostrar apenas os cursos com mais de 5 alunos <br>
``SELECT curso_id, COUNT (*) FROM Alunos GROUP BY curso_id HAVING COUNT (*) > 5; ``

> HAVNG: <br>
    > Selecionar os cursos cuja a média de idade dos alunos seja maior que 25 <br>
``SELECT curso_id, AVG(idade) as media_idade FROM Alunos GROUP BY curso_id HAVING AVG(idade) > 25;``

> JOIN: <br>
    > Selecionar o alunos com seus respectivos cursos e seus nomes de parentes da tabela Parentes <br>
```
SELECT Alunos.nome, Cursos,nome, Parentes.nome as nome_parente
FROM Alunos
JOIN Cursos ON Alunos.curso_id = Cursos.id
JOIN Parentes ON Alunos.id = Parentes.aluno_id;
```

> UNION: <br>
    > Selecionar todos os nomes de alunos das tabelas Alunos e Parentes <br>
```
SELECT nome FROM Alunos
UNION
SELECT nome FROM Parentes;
```
Esses são alguns exemplos de como usar as cláusulas SQL para realizar consultas mais avançadas nas tabelas.