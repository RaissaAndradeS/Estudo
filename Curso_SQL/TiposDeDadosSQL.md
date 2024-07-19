## <center>Tipos de dados no SQL</center>

Os  tipos de dados são usados para definir o tipo de valor que uma coluna pode armazenar em uma tabela do banco de daos. É importante entender os diferentes tipos de dados para garantir a correta representação e manipulação dos dados em seu sistema.

## Tipos de dados numéricos 

- INTEGER: representa números inteiros como 1, 10, -5 <br> ``idade INTEGER``
- DECIMAL/NUMERIC: representa números decimais com precisão fixa <br> ``preco DECIMAL (10, 2)``
- FLOAT/DOUBLE: representa números de ponto flutuante com precisão variável <br> ``valor DOUBLE``

## Tipos de dado de texto

- CHAR: representa uma sequência de caracteres de tamanho fixo ``nome CHAR(50)`` <br>
- VARCHAR: representa uma sequência de caracteres de tamanho variável ``descricao VARCHAR(255)`` <br>
- TEXT: representa uma sequência de caracteres de comprimento ilimitado ``observacoes TEXT`` <br>

## Tipos de dados de data e hora

- DATE: representa uma data no formato 'YYYY-MM-DD' ``data_nascimento DATE`` <br>
- TIME: representa um horário no formato 'HH:MM:SS' ``hora_chegada TIME`` <br>
- TIMESTAMP: representa uma data e hora combinadas ``data_hora TIMESTAMP`` <br>

## Tipos de dados booleanos
Para valores booleanos (verdadeiro/falso) tem o tipo ``BOOLEAN``. Esse tipo de dado pode assumir os valores TRUE ou FALSE. ``aprovado BOOLEAN`` <br>

## Outros tipos de dados

- BLOB: usado para armazenar dados binários, como imagens ou arquivos ``foto BLOB``
- ENUM: usado para definir um conjunto de valores permitidos ``estado_civil ENUM('solteiro','casado','divorciado')`` <br>

Os tipos de dados podem variar dependendo do sistema de gerenciamento de banco de dados que você está usando. Certifique se de consultar a documentação específica do seu sistema para obter informações detalhadas sobre os tipos de dados suportados. <br>
Ao definir as colunas em suas tabelas, é importante escolher o tipo de dado correto para garantir a precisão e integridade dos dados armazenados.


