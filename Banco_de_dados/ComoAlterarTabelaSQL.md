## <center>Como alterar tabela em SQL</center>

Depois de criar uma tabela em banco de dados, podemos alterar a estrutura com uso da clásula ``ALTER TABLE``. Nota se que essa alteração é sempre sobre a estrutura da tabela, e não sobre os dados da tabela.
Essa alteração da tabela é efetuada de duas formas: ou acrescentando um novo campo ``ADD`` ou alterando a propriedade de um campo já existente ``MODIFY``. O comando ``ALTER TABLE`` segue essa sintaxe:

```
ALTER TABLE Nome_Tabela
ADD Nome_Campo Nova_Regra
MODIFY Nome_campo Nova_Regra
```
## Operação Update
A operação ``Update`` ou ``Modify`` é usada para mudar os valores de um ou mais atributos em uma tupla ou tuplas de alguma relação R. É necessário especificar uma condição nos atributos da relação para selecionar a tupla a ser modificada.

> 1. Modificar o SALARIO da tupla de EMPREGADO com SSN = '993242134' para 24000. <br>
> 2. __Aceitavél__ <br>
> 3. Modificar o DNO da tupla de EMPREGADO com SSN = '9997787654' para 5. <br> 
> 4. __Inaceitável, porque viola a integridade referencial.__  <br>

Modificar um valor de chave primária é similar a remover uma tupla e inserir outra em seu lugar, porque usamos para identificá-las. Se um atributo de chave estrangeira for modificado, o SGBD deverá se certificar de que o novo valor refere-se a uma tupla existente na relação que foi referida ou é **NULL**. Quando uma restrição de integridade referencial é especificada na DDL, o SGBD permitirá ao usuário escolher as opções distintas para tratar uma violação causada por Delete e uma causada por Update.

## ADD 
O ``ADD`` é usado para adicionar um novo campo em uma tabela, onde devemos definir seu tipo da mesma forma como fazemos ao criar um campo em uma nova tabela. Exemplo : <br>

- Inserir mais um campo chamado Telefone Comercial no final da tabela Cliente.

```
ALTER TABLE Cliente
ADD Tel_Comercial INT;
```
Campos com tamanhos definidos, devem ter seu tamanho especificado. Caso vá insterir mais um campo VarChar, chamado por exemplo de Nome da Mãe em nossa tabela Ciente fazemos:

```
ALTER TABLE Cliente
ADD Nome_Mae VARCHAR(60);
```
Campo que seja inserido antes ou depois de um determinado campo de nossa tabela, é usada essa sintaxe:

```
ALTER TABLE Nome_Tabela
ADD Nome_Campo Nova_Regra [FIRST|AFTER] Campo_Determinado;
```
Se tiver ``FIRST``, o novo campo será criado antes do campo escolhido da tabela. Se for ``AFTER`` no campo Nome_Mae o campo do Nome do Cliente: 

```
ALTER TABLE Cliente
ADD Nome_Mae VARCHAR(60)AFTER Nome;
```
Alguns gerenciadores usam ``ADD COLUMN`` ao invés de somente ``ADD``. Podemos utilizar ``ADD`` para adicionar por exemplo uma chave primária em uma tabela. Caso queira uma chave primária também: 

```
ALTER TABLE Cliente
ADD PRIMARY KEY(Nome);
```
Se for para eliminar uma coluna da nossa tabela: 

```
ALTER TABLE Nome_Tabela
DROP nome_campo;
```
Novamente, alguns gerenciadores também usam ``DROP COLUMN`` ao invés de somente ``DROP``. <br>
Se for para alterar/mudar o nome da tabela que vai trabalhar, usamos: 

```
ALTER TABLE Cliente
rename to novoNomeDaTabela;
```
Para mudar/alterar nome de uma das colunas já existentes na tabela, usa: 

```
ALTER TABLE Cliente 
change colunm antigoNomeDaColuna novoNomeDaColuna tipoDeDadoDessaColuna e AsContrains;
```

## MODIFY
É usado para modificar as propriedade de um campo em uma tabela. Por exemplo, devemos modificar o tamanho de nosso campo Nome na tabela Cliente, de 60 para 100.

```
ALTER TABLE Cliente 
MODIFY Nome(100);
```
Alteração no tipo de um campo, exemplo tipo do campo Nome de VarChar para Char.
```
ALTER TABLE Cliente
MODIFY Nome CHAR (100);
```