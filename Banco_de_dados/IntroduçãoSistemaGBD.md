## <center>Introdução a Sistema de Gerenciamento de Banco de Dados</center>

Um Sistema de Gerenciamento de Banco de Dados (SGBD) é um programa de software que permite aos usuários interagir com um banco de dados para armazenar, recuperar e manipular dados. O SGBD serve como uma interface entre o banco de dados e os usuários ou programas de aplicação. Ele possibilita aos usuários criar, modificar e manter o banco de dados, e como controlar o acesso aos dados.<br>

### Recursos do SGBD
#### Armazenamento de dados: 
O SGBD gerencia como os dados são fisicamente armazenados e recuperados do armazenamento em disco. <br>

 Principais reponsabilidades:<br>

- Definir o esquema lógico e as estruturas de dados internas para organizar os dados no disco. Isso inclui tabelas, índices, partições e etc.
- Gerenciar a alocação de espaço de armazenamento para arquivo e objeto do banco de dados. Expandir o armazenamento conforme necessário.
- Criar e manter arquivos de dados e atribuir identificadores exclusivos a cada página ou bloco de dados. 
- Interagir com o sistema operacional e gerenciar os buffers para leitura de blocos de dados do disco e gravação no disco.
- Manter mapeamentos entre objetos lógicos como tabelas e locais físicos de armazenamento de dados.
