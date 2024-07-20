## <center>Manipulação de Dados</center>

É importante saber como manipular os dados dentro da tabela, aqui tem instruções básicas de SQL para inserir, selecionar, atualizar e excluir dados de uma tabela.

## Inserção de dados
Insert é usado para adicionar novos registros em uma tabela.<br>
``INSERT INTO nome_da_tabela (coluna1, coluna2, ...)`` <br>

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
<br>
## Atualização de dados
## Exclusão de dados 
