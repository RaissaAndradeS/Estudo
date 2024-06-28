## <center>Como criar tabela em SQL</center>

Podemos criar uma tabela qualquer dentro de um banco de dados, a sintaxe é:

```
CREATE TABLE nome_tabela
(
nome_campo_1 tipo_1,
nome_campo_2 tipo_2,
...
nome_campo_n tipo_n,
PRIMARY KEY (campo_x,...)

);
```

CREATE TABLE é o comando para criação da tabela e deve ser seguida pelo nome que daremos à tabela. Dentro do comando, devemos definir os nomes dos campos de acordo com a conveniência do banco de dados, e determinar o tipo de dado que poderá ser incluído nesse campo. Abaixo os tipos de dados estão especificados os tipos mais comuns encontrados nos SGBDs. PRIMARY KEY define a chave primária da tabela, isso é, o campo que serve como chave da tabela e que não pode ser repetido.

Para um campo ser preenchido obrigatoriamente, devemos inserir NOT NULL na frente do campo determinado.

```
CREATE TABLE nome_tabela
(
nome_campo_1 tipo_1 NOT NULL,
nome_campo_2 tipo_2,
...
nome_campo_n tipo_n,
PRIMARY KEY (campo_x,...)

);
```