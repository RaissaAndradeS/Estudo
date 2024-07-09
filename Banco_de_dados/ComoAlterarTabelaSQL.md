## <center>Como alterar tabela em SQL</center>

Depois de criar uma tabela em banco de dados, podemos alterar a estrutura com uso da clásula ``ALTER TABLE``. Nota se que essa alteração é sempre sobre a estrutura da tabela, e não sobre os dados da tabela.
Essa alteração da tabela é efetuada de duas formas: ou acrescentando um novo campo ``ADD`` ou alterando a propriedade de um campo já existente ``MODIFY``. O comando ``ALTER TABLE`` segue essa sintaxe:

```
ALTER TABLE Nome_Tabela
ADD Nome_Campo Nova_Regra
MODIFY Nome_campo Nova_Regra
```
