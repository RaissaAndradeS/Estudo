## Considerações de design de banco de dados 

- Como organizar dados?
- O que é uma Entidade?
- O que é um Atributo de uma Entidade?
- Como pensar para obter um bom design?
- Pensando de acordo com a perspectiva de um programador.
- Pensando de acordo com a perspectiva de um DBA.

## Introdução ao Banco de Dados 

### O que são dados? 
Dados são fatos ou números conhecidos que tem significado imlícito. Também pode ser definida como representação de fatos, conceitos ou instruções de maneira formal, adequada para compreensão e processamento. Os dados podem ser representados em alfabatos (AZ, az), dígitos (0-9) e caracteres especiais (+, -, #, $). <br>

__Exemplo:__ 25, "Pedro", etc.

### O que é Banco de dados? 
Banco de dados é uma coleção de dados inter-relacionados que ajudam na eficiência inserção, recuperação e eliminação dos dados a partir de banco de dados. Organiza os dados em forma de tabelas, visualizações, esquemas, relatórios e etc. <br>

__Exemplo:__ O banco de dados de uma universidade.

## O que é SGBD?
SGBD ou Sistema de Gerenciamento de Banco de dados é um aplicativo de software usado para acessar, criar e gerir banco de dados. Com SGBD, pode criar, recuperar e atualizar dados nos bancos de dados com facilidade.<br>
Um SGBD consiste em um grupo de comandos para manipular o banco de dados e atua como uma interface entre os usuários finais e o banco de dados.<br>
Todos os sistemas de gerenciamento de banco de dados relacional (SGBD) como MySQL, Ms Acess, Oracle, Sybase, Informix, Postgres e SQL Server usam SQL.<br>

Banco de dados - SGBD - API

### Vantagens do SGBD
1 - Controla a redundância do Banco de dados. <br>
2 - Compartilhamento de Dados. <br>
3 - Fácil manutenção. <br>
4 - Reduz tempo. <br>
5 - Cópia de segurança. <br>
6 - Múltiplo do utilizador de interface. <br>

### Desvantagens do SGBD
1 - Custo alto de Hardware e Software. <br>
2 - Tamanho. <br>
3 - Complexidade. <br>
4 - Maior impacto de falha. <br>

## SQL - Banco de dados Relacional 
Bancos de dados relacinal possuem diversos conceitos que devem ser aprendidos e compreendidos. <br>
A unidade principal por trás de um banco de dados relacional tem como função aumentar a precisão, aumentar a eficiência de como os dados são armazenados. Por exemplo, os nomes de cada uma das milhões de pessoas que imigraram para os Estados Unidos das Ilhas Ellis durante o século XX foram escritos à mão e guardados em uma grande quantidade de folhas de papel. Pessoas da cidade de Londres tiveram seu país de origem definido como Inglaterra ou Grã-Bretanha ou Reino Unido ou ainda alguma dessas formas abreviadas. Múltiplas maneiras de guardar a mesma informação geram confusão quando houver a necessidade de saber algo simples como quantas pessoas vieram do país Tal? <br>
A solução moderna para esse problema é o banco de dados. Um único registro é dado para cada país. Por exemplo, uma lista de referência que deve ser chamada de tabela de país. Quando alguém precisar indicar o Reino Unido, será necessário apenas ter uma escolha disponível. Ter disponível uma simples lista de letras ou string "Reino Unido" como única representação do país. **Um banco de dados relacional é simplesmente uma coleção de listas que distribuem alguma parte da informação.**<br>
Banco de dados armazenam dados de um sistema de informação. Nós reagrupamos dados através de grupos de dados comparáveis (todos os empregados, todos os projetos, todos os escritórios). Para cada grupo de dados comparáveis, é criada uma *tabela*. Essa tabela é especialmente desenhada para atender esses tipos de dados (seus atributos). Exemplo, uma tabela nomeada *empregados* que guarda todos os empregados seria feita assim:


| **EMPREGADOS** |  |
|----------|---------------|
| ID empregado (a chave primária)  | Um número inteiro  |
| Primeiro nome (uma coluna)  | Uma string de caracteres (uma coluna tipo)  |
| Último nome | Uma string de caracteres  |
| Telefone  | 10 números |
| Endereço | Uma string de caracteres  | 
<br>

E os funcionários da empresa seriam armazenados assim:

| Empregados |  || | | |
|----------|----------|----------|----------|----------|----------|
| ID Empregado  | Primeiro nome   | Último nome   | Telefone   | Endereço   | 
| 1 (Um valor de coluna)  | Big   | Boss   | 9988881213   | big.boss@aleatorio.com  | 
| 2  | Pedro   | Tavares  | 9188775656   | pedro.tavares@aleatorio.com   | 
| 3 | Junior   | Bosi  | 5688333434   | junior.bosi@aleatorio.com | 
| 4 | Pedro   | Silva   | 2123234545   | pedro.silva@aleatorio.com   | 
| 5  | Henrique   | Santos   | 1198985454   | henrique.santos@aleatorio.com   | 
<br>

Os dados guardados em uma tabela são chamados de *entidades*. Como uma tabela é usualmente representada como uma matriz, os atributos do dados (primeiro nome, último nome, ...) são chamados de *colunas* e os registros (cada um dos empregados) são chamadas de *linhas*. Uma chave primária é normalmente sublinhada. Qualquer atributo único (por exemplo, endereço)  ou grupo de atributos (como primeiro nome e último nome) podem ser a chave primária de uma tabela, mas isso é recomendado para a técnica do *id*, como no exemplo *id_empregado* como chave primária. A função da chave primária é simplesmente diferenciar uma das linhas ou registros que fazem parte de uma tabela.

Agora uma segunda tabela chamada *projeto* que guardará os projetos da empresa:

| **EMPREGADO** |  |
|----------|---------------|
| ID empregado  | Um número inteiro  |
| Primeiro nome  | Uma string de caracteres  |
| Último nome | Uma string de caracteres  |
| Telefone  | 10 números |
| Endereço | Uma string de caracteres  | 
<br>

| **PROJETO** |  |
|----------|---------------|
| ID projeto  | Um inteiro  |
| nome  | Uma string de caracteres  |
| data-da-criação | uma data  |
| data-termino  | uma data |
| # gerente | um inteiro  | 
<br>

E os projetos da companhia seriam armazenados no banco da seguinte forma:

| Empregado |  || | | |
|----------|----------|----------|----------|----------|----------|
| ID Empregado  | Primeiro nome   | Último nome   | Telefone   | Endereço   | 
| 1   | Big   | Boss   | 9988881213   | big.boss@aleatorio.com  | 
| 2  | Pedro   | Tavares  | 9188775656   | pedro.tavares@aleatorio.com   | 
| 3 | Junior   | Bosi  | 5688333434   | junior.bosi@aleatorio.com | 
| 4 | Pedro   | Silva   | 2123234545   | pedro.silva@aleatorio.com   | 
| 5  | Henrique   | Santos   | 1198985454   | henrique.santos@aleatorio.com   | 
<br>

| Projetos |  || | | |
|----------|----------|----------|----------|----------|----------|
| ID project  |  nome   | data-criação   | data-término   | #gerente   | 
| 1   |  Google  | 1998-09-08   | NULL   | 5  | 
| 2  | Linux  | 1991-01-01 | NULL   | 3  | 
| 3 | Wikipedia | 2001-01-01  | NULL   | 4| 
| 4 | CRM  | 2015-09-14   | NULL   | 5  | 
<br>

**id_project** é a chave primária da tabela projeto e *#gerente* é a chave **estrangeira**. Uma chave estrageira é uma chave primária de uma tabela, fazendo referência ou ligação com algum valor de outra tabela. Fazendo isso, o projeto Google está conectado ao empregado Henrique Santos. Essa conexão se chama **relacionamento**. Uma chave estrangeira é usada por "#". Veja qu vários projetos podem ter o MESMO gerente. Nesse caso, Henrique Santos é gerente do projeto 1 e 5, logo um mesmo empregado por ser gerente de VÁRIOS projetos.<br>
Vamos criar várias ligações. Faremos uma tabela de **junção**. Uma tabela de junção é uma tabela que não é usada para guardar dados e sim LIGAÇÕES entre as entidades de outras tabelas. É a tabela onde as ligações ou relacionamentos entre as tabelas são guardadas. Vamos fazer uma tabela chamada **membros** que liga empregados com projeto:

| empregado |                    |
|---------------|-------------------------|
| id_empregado  | um inteiro              |
| primeiro-nome | uma string de caracteres|
| último-nome   | uma string de caracteres|
| telefone      | 10 números              |
| endereço      | uma string de caracteres|

|membros||
|-------|------|
|# id_empregado|um inteiro|
|# id_projeto | um inteiro|

| projeto |                   |
|--------------|-------------------------|
| id_projeto   | um inteiro              |
| nome         | uma string de caracteres|
| data-criação | uma data                |
| data-término | uma data                |
| gerente      | um inteiro              |

E agora como ficaria os empregados e os projetos:

| id_employee | primeiro-nome | último-nome    | telefone | endereço                        |
|-------------|---------------|----------------|----------|---------------------------------|
| 1           | Big           | BOSS           | 936854270| big.boss@company.com            |
| 2           | Augusto       | XAVIER         | 936854271| augusto.xavier@company.com      |
| 3           | Linus         | TORVALDS       | 936854272| linus.torvalds@company.com      |
| 4           | Jimmy         | WALES          | 936854273| jimmy.wales@company.com         |
| 5           | Larry         | PAGE           | 936854274| larry.page@company.com          |
| 6           | Max           | THE GOOGLER    | 936854275| max.the-googler@company.com     |
| 7           | Jenny         | THE WIKIPEDIAN | 936854276| jenny.the-wikipedian@company.com|

|projeto|||||
|------------|------------|--------------|--------------|---------|
| id_project | nome       | data-criação | data-término | gerente |
| 1          | Google     | 1998-09-08   | NULL         | 5       |
| 2          | Linux      | 1991-01-01   | NULL         | 3       |
| 3          | Wikipedia  | 2001-01-01   | NULL         | 4       |
| 4          | CRM        | 2015-09-14   | NULL         | 5       |

|membros||
|--------------|------------|
| id_empregado | id_projeto |
| 3            | 2          |
| 2            | 1          |
| 4            | 3          |
| 5            | 1          |
| 2            | 3          |
| 6            | 1          |
| 7            | 3          |
| 5            | 4          |

Um empregado pode estar ligado com vários projetos e um projeto pode ser associado a vários empregados, isso é impossível com APENAS uma chave estrangeira. Uma tabela de junção não tem chave primária própria. Sua chave primária é o par de chaves estrangeiras, esse relacionamento é ÚNICO. Uma tabela de junção pode ligar mais de duas tabelas contendo entidade por mais colunas.

