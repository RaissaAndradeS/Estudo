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
Se quiser que um camo seja de auto-incremento, deve colocar AUTO_INCREMENT na frente do campo determinado:

```
CREATE TABLE nome_tabela
(
nome_campo_1 tipo_1 NOT NULL AUTO_INCREMENT,
nome_campo_2 tipo_2,
...
nome_campo_n tipo_n,
PRIMARY KEY (campo_x,...)

);
```

## Tipos de Dados 
Tipos de dados definem os tipos de informações que podem ser inseridas em um campo. Somente dados do mesmo tipo do campo poderão ser inseridos. Os tipos suportados por um banco de dados podem variar de SGBD para SGBD. Abaixo estão os principais tipos encontrados: 

| Tipo         | Explicação                                                             | Valores permitidos                             | Exemplo       |
|--------------|------------------------------------------------------------------------|------------------------------------------------|---------------|
| BOOLEAN      | Armazena um bit de informação, utilizado para verdadeiro ou falso.     | Verdadeiro/falso                               | true/false    |
| VARCHAR(n)   | Uma string com tamanho máximo n                                        | [0-9a-zA-Z]+{n}                                | "foo"         |
| CHAR(n)      | Uma string com tamanho fixo n                                          | [0-9a-zA-Z]{n}                                 | "foo"         |
| SMALLINT     | Número inteiro com 16 bits de precisão                                 | \-?[0-9]+                                      | 584           |
| INTEGER      | Número inteiro com 32 bits de precisão                                 | \-?[0-9]+                                      | -8748         |
| FLOAT        | Número decimal                                                         | \-?[0-9]+[\.[0-9]+]?                           | 48.96         |
| NUMBER(n,[d])| Um número com n dígitos (e d dígitos decimais se mencionado)           | \-?[0-9]+[\.[0-9]+]?                           | 484.65        |
| DATE         | Uma data (Padrão americano)                                            | [0-9][0-9][0-9][0-9]\-[0-1][0-9]\-[0-3][0-9]   | 2009-03-24    |
| TIME         | Um período de sessenta minutos; 1/24 de um dia                         | [0-2][0-9]\:[0-5][0-9]\:[0-5][0-9]             | 11:24:56      |
| TIMESTAMP    | Data e hora                                                            | [0-9]+                                         | 18648689595962|
| BLOB         | Qualquer dado                                                          | Qualquer                                       |               |

## Exemplo 
Como exemplo do uso do comando CREATE TABLE, um exemplo é a necessidade de uma tabela que deva ter dados dos clientes de uma loja.

```
CREATE TABLE Cliente
(
Codigo INT NOT NULL AUTO_INCREMENT,
Nome VARCHAR (60) NOT NULL,
Data_Nascimento DATE,
Telefone CHAR (8),
PRIMARY KEY (Codigo) 
);
```
Nesse comando, criamos uma tabela chamada Cliente, essa tabela contém 4 campos, o primeiro campo é o Código do cliente, esse campo vai ser utilizado como chave primária de forma que não poderá se repetir nunca.
E ele deve ser sempre preenchido (NOT NULL), é numérico do tipo inteiro (INT) e deve auto-incrementar de acordo com o número de clientes que for incluido.<br>
O campo Nome é do tipo VARCHAR(60), ou seja, aceita dados alfa-numéricos com até 60 caracteres. No entanto se um nome for inserido com menos de 60 caracteres, o número de bytes consumidos pelo campo será de acordo com o nome inserido. <br>

