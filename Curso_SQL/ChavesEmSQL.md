## <center> Chaves Primárias e Estrangeiras</center>

Chaves primárias e estrangeiras são conceitos fundamentais em banco de dados relacionais. Elas são usadas para estabelecer relacionamentos entre tabelas, garantir a integridade dos dados e consistência referencial.

## Chaves Primárias 

Uma chave primária é um campo ou conjunto de campos que identifica exclusivamente cada registro em uma tabela. Ela garante a unicidade dos registros e é usada para acessar, vincular e manipular os dados de uma tabela. A chave primária é definida durante a criação da tabela e pode ser composta por um único campo ou vários campos combinados.

No exemplo da tabela Alunos para entender como criar uma chave primária.

```
CREATE TABLE Alunos (
    id INT PRIMARY KEY,
    nome VARCHAR(100),
    idade INT,
    curso_id INT
);
```
## Chaves Estrangeiras 

Uma chave estrangeira é um campo em uma tabela que se refere à chave primária de outra tabela. Ela estabelece um relacionamento entre as tabelas, permitindo a integridade referencial entre elas. As chaves estrangeiras são usadas para garantir que os dados relacionados sejam consistentes e que não haja referências a registros inexistentes.
 
 Utilizando as tabelas "Cursos" e "Parentes" como exemplo para entender como criar chaves estrangeiras. A tabela "Cursos" contém informações sobre os cursos oferecidos, e a tabela "Parentes" contém informações sobre os parentes dos alunos.

 ```
 CREATE TABLE Cursos (
    id INT PRIMARY KEY,
    nome VARCHAR (100),
    departamento VARCHAR(100)
 );

 CREATE TABLE Parentes (
    id INT PRIMARY KEY,
    aluno_id INT,
    nome VARCHAR(100),
    relação VARCHAR(100),
    FOREING KEY (aluno_id) REFERENCES Alunos(id)
 )
 ```
 No exemplo acima, a tabela "Parentes" possui uma chave estrangeira "aluno_id" que faz referência à chave primária "id" da tabela "Alunos". Isso estabelece um relacionamento entre tabelas, onde cada parente está associado a um aluno existente. <br>

 ## Benefícios das chaves primárias e estrangeiras 

O uso de chaves primárias e estrangeiras traz vários benefícios para o design do seu banco de dados e para a integridade dos dados armazenados:

- Unicidade dos registros: a chave primária garante que cada registro em uma table seja único e identificável de forma exclusiva.

- Integridade referencia: as chaves estrangeiras garantem que não haja referências a registros inexistentes em tabelas relacionadas. Isso mantém a consistência dos dados e evita registros órfãos.

- Relacionamento entre tabelas: as chaves estrangeiras permitem estabelecer relacionamentos entre tabelas, fornecendo uma maneira de conectar informações relacionadas em diferentes entidades.

- Consultas e manipulação de dados: as chaves primárias e estrangeiras facilitam a consulta e manipulação de dados em várias tabelas usando instruções SQL, como JOINs.

- Integridade dos dados: o uso correto de chaves primárias e estrangeiras ajuda a manter a integridade do dados, evitando inserções, atualizações ou exclusões indesejadas ou inconsistentes. 
