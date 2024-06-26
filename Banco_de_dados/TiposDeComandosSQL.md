## <center> Tipos de Comandos SQL </center>
Os comandos SQL padrão para interagir com banco de dados relacionais são: CREATE, SELECT, INSERT, UPDATE, DELETE e DROP. Esses comandos podem ser classificados nos seguintes grupos com base em sua natureza:

###  Linguagem de definição de dados - LDD
É um subconjunto do SQL e uma parte do SGBD. No contexto so SQL, definição de dados ou linguagem de descrição de dados é uma sintaxe para criar e modificar objetos de banco de dados, como tabelas, índices e usuários. As instruções LDD são semelhantes a uma linguagem de programação de computador para definir estruturas de dados, especialmente esquema de banco de dados.<br>

|Comando|Descrição|
|------|----------|
|CREATE|Criar uma nova tabela, uma exibição de uma tabela ou outro objeto no banco de dados.|
|ALTER|Modificar um objeto de banco de dados existente, como uma tabela.|
|DROP|Excluindo uma tabela inteira, uma exibição de uma tabela ou outros objetos no banco de dados.|

### Linguagem de Manipulação de Dados - LMD
É uma linguagem de programação de computador usada para adicionar, excluir e modificar dados em um banco de dados. Uma LMD geralmente é uma sublinguagem de uma linguagem de banco de dados mais ampla, como SQL, com a LMD compreendendo alguns dos operadores da linguagem. <br>

|Comando| Descrição|
|-------|----------|
|INSERT|Cria um registro|
|UPDATE|Modifica registro|
|DELETE|Exclui registro|

### Linguagem de consulta de dados 
É usada para fazer consultas, extrair informações de um banco de dados. É importante que essas consultas aconteçam sem provocar mudanças no banco de dados. O comando é SELECT. <br>

### O que é uma query em SQL?
Consulta é feita para extrair respostas do dados.<br>

```
select * from alunos
select * from professores
select * from matriculas_de_alunos
select * from horarios_de_aula
```
### Como descobrir informações sobre o banco de dados?

Aprendendo informações sobre uma tabela:

- Listar colunas nessa tabela
- Listar índices nessa tabela
- Listar chaves estrangeiras nessa tabela
- Listar chaves estrageiras em outras tabelas apontando pra essa tabela
- Gerando um dicionário e usando o excel