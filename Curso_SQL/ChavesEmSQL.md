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
    
 )
 ```