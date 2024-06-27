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

### Segurança de Dados 
O SGBD tem recursos de segurança para evitar acesso não autorizado e proteger a confidencialidade dos dados.

- Gerenciamento de contas de usuário com credenciais como nome de usuário/senha para autenticação.
- Conceder e revogar privilégios de acesso a usuários e funções.
- Aplicar controle de acesso a objetos do banco de dados como tabelas, procedimentos, visualizações, etc.
- Auditar atividades do usuário para vigilância de segurança.
- Criptografar dados sensíveis no banco de dados ou tráfego de rede com algoritmos de criptografia.
- Mascarar dados para proteção de privacidade por meio da obfuscação de campos sensíveis.

