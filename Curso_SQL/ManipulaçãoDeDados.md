## <center>Manipulação de Dados</center>

É importante saber como manipular os dados dentro da tabela, aqui tem instruções básicas de SQL para inserir, selecionar, atualizar e excluir dados de uma tabela.

## Inserção de dados
Insert é usado para adicionar novos registros em uma tabela.<br>
```
INSERT INTO nome_da_tabela (coluna1, coluna2, ...)
VALUES (valor1, valor2...);
```

Pontos chave do comando Insert: <br>
``INSERT INTO``: inicio do comando de inserção <br>
``nome_da_tabela``: especifica o nome da tabela em que os dados serão inseridos <br>
``coluna1, coluna2``: lista as colunas nas quais os valores serão inseridos <br>
``VALUES``: inicio dos valores que serão inseridos <br>
``valor1, valor2``: lista os valores correspondentes às colunas especificadas <br>

Na tabela de Alunos, ficaria algo assim: 

```
INSERT INTO Alunos (ID, Nome, Idade, Curso)
VALUES(1, 'Clara', 20, 'Engenharia de Software')
```
O valor 1 é da coluna ID, Clara é da coluna Nome, 20 é da coluna Idade e Engenharia de Software é da coluna Curso.

## Seleção de dados
Select é usado para recuperar dados de uma tabela, permitindo selecionar colunas específicas ou todas as colunas de uma tabela. <br>

```
SELECT coluna1, coluna2, ...
FROM nome_da_tabela
WHERE condição;
``` 

``SELECT``: inicio do comando de seleção <br>
``coluna1, coluna2``: lista as colunas que serão recuperadas, o ``*`` pode ser usado para selecionar todas as colunas <br>
``FROM``: indica a tabela da qual os dados serão selecionados <br> 
``nome_da_tabela``: especifica o nome da tabela <br>
``WHERE``: permite filtrar os resultados com base em uma condição.

```
SELECT Nome, Idade, Curso
FROM Alunos;
```

## Atualização de dados
Update é usado para modificar os dados existentes em uma tabela. <br>

```
UPDATE nome_da_tabela
SET coluna1 = novo_valor1, coluna2 = novo_valor2, ...
WHERE condição
```

``UPDATE``: inicio do comando de atualização <br>
``nome_da_tabela``: especifica o nome da tabela em que os dados serão atualizados <br>
``SET``: indica o inicio das atualizações que serão feitas <br>
``coluna1, coluna2``: lista as colunas que serão atualizadas <br>
``novo_valor1, novo_valor2``: lista os novos valores que substituirão os valores existentes <br>
``WHERE``: permite filtrar os registros que serão atualizados com base em uma condição <br>

```
UPDATE Alunos
SET Idade = 21
WHERE ID = 1;
```

## Exclusão de dados 

Delete é usado para remover registros de uma tabela. <br>

```
DELETE FROM nome_da_tabela
WHERE condição;
```
``DELETE FROM``: inicio do comando de exclusão <br>
``nome_da_tabela``: especifica o nome da tabela que os registro serão excluídos <br>
``WHERE``: permite filtrar os registros que serão excluídos com base em uma condição <br>

```
DELETE FROM Alunos
WHERE ID = 1;
```
