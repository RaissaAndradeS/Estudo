## <center>Como criar tabelas em SQL</center>

Uma tarefa essencial de banco de dados relacional é criar tabelas para armazenar os dados de forma organizada. Utilizamos o SQL para definir a estrutura das tabelas, incluido as colunas, os tipos de dados, as restrições e os relacionamentos entre elas.

## Create Table
```
CREATE TABLE nome_da_tabela (
    nome_coluna1 tipo_dado1 restricoes,
    nome_coluna2 tipo_dado2 restricoes
    ...
);
```
> CREATE TABLE: Indica o início do comando para criar uma tabela. <br>

> nome_da_tabela: Especifica o nome da tabela que será criada. <br>

> nome_da_coluna: Define o nome de uma coluna dentro da tabela. <br>

> tipo_dado: Especifica o tipo de dado que será armazenado na coluna. <br>

> restricoes: Define as restrições opcionais para a coluna, como restrição de chave primária ('PRIMARY KEY'), restrição de chave estrangeira ('FOREIGN KEY'), restrição de valor único ('UNIQUE'), entre outras.<br>

## Exemplo de criação de tabela
Tabela Alunos para demonstrar a criação de uma tabela.

- ID: Identificador único do aluno
- Nome: Nome do aluno
- Idade: Idade do aluno
- Curso: Curso do aluno

```
CREATE TABLE Alunos (
    ID INT PRIMARY KEY,
    Nome VARCHAR (50),
    Idade INT,
    Curso VARCHAR(100)
);
```
Nesse exemplo, estamos criado a tabela ``Alunos`` como as colunas ``ID``, ``Nome``, ``Idade`` e ``Curso``. A coluna ``ÌD`` é definida como chave primária usando a restrição ``PRIMARY KEY``. As colunas ``Nome`` e ``Curso`` são do tipo ``VARCHAR``, que armazena strings de tamanho variável e as colunas ``Idade`` e ``ID`` são do tipo ``INT`` que armazena valores inteiros.<br>
Ao criarmos uma tabela, é importante definir os tipos de dados corretos para cada coluna, garantindo a consistência e intedridade dos dados armazenados.
