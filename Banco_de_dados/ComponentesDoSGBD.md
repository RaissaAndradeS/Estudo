## <center> Componentes do Sistema de Gerenciamento de Banco de Dados</center>

Um SGBD inclui vários componentes que trabalham juntos para gerenciar e manter o banco de dados. 

## Gerenciador de Armazenamento de Dados
O GAD zela de como os dados são fisicamente armazenados no disco. 

- Gerenciamento de alocação de espaço em disco para arquivos de banco de dados.
- Criação, exclusão e modificação dos arquivos de armazenamento do banco de dados.
- Definição da estrutura de registros e layout para armazenamento de dados.
- Interação com o sistema operacional para operações de leitura/gravação de arquivos.
- Gerenciamento de buffers e caches para bloco de dados. Exemplo, InnoBD no MySQL e as tabelas de heap no SQL Server usam diferentes gerenciadores de armazenamento de dados.

## Dicionário de Dados
É um repositório centralizado de metadados que contém definições de todos os objetos do banco de dados. Nesse repositório contém:

- Esquemas de banco de dados relacionamentos.
- Tipos de dados dos atributos.
- Restrições como chave primárias, chaves estrangeiras, verificações e etc.
- Índice, partições, visualizações, gatilhos e outros objetos.
- Autorização do SGBD para usar metadados. Ele fornece isolamento entre armazenamento físico e visualizações lógicas de dados.

## Processador de Consultas 
Esse interpreta e executa consultas para SGBD.

- Análise de consultas - Converte instruções SQL ou de outra linguagem de consulta em código interpretável.
- Otimização de consultas - Seleciona o plano de consultas mais eficiente com base em diferentes algoritmos.
- Execução de consultas - Recupera registros do banco de dados usando caminhos de acesso conforme o plano de consulta. Exemplo, o MySQL usa um módulo de otimização de consultas que gera e armazena em cache planos de consulta.

## Gerenciador de Transações
Esse é responsável por gerenciar transações no sistema de banco de dados.

- Iniciação, confirmação e reversão de transações.
- Manutenção do isolamento entre transações via controle de concorrência.
- Detecção e resolução de deadlock entre transações conflitantes.
- Recuperação de falhas de transações. Exemplo, MySQL depende de mecanismo de armazenamento como o InnoBD para lidar com o gerenciamento de transações.

## Gerenciador de Segurança 
Controla o acesso ao banco de dados autenticando usuário e autorizando operações. 

- Gerenciamento de contas de usuário - Criar, modificar, excluir usuários.
- Controle de acesso - Concender ou revogar privilégio de acesso do usuário.
- Gerenciamento de senhas - Definir regras de política de senha.
- Auditoria - Registrar atividades do usuário para auditoria.
- Criptografia - Criptografar dados em repouso ou em trânsito. Exemplo, o Oracle Database fornece segurança avançada por meio de produtos como Oracle Label Security.

## Gerenciador de Acesso a Dados 
Essa interface permite permite que usuários e aplicativos externos acessem e manipulem dados no banco de dados.

- Linguagens de consulta como SQL, APIs NoSQL e etc.
- Interface programáticas como JDBC, ODBC, ADO.NET.
- Serviços da web, mensagens e outros protocolos de comunicação. Exemplo, o MongoDB fornece acesso a dados via shell do MongoDB, drivers para várias linguagens e APIs REST.

## Gerenciador de Buffer
Gerencia cache de Buffer do banco de dados que armazena temporariamente páginas de dados na memória para acesso mais rápido.

- Armazenamento em cache de páginas de dados frequentemente usadas no disco.
- Aplicação de políticas de substituição de buffer como LRU para gerenciar o cache.
- Coordenação como o gerenciador de armazenamento para buscar páginas de dados.
- Gravação de páginas modificadas do buffer no disco. Exemplo, o InnoDB usa um pool de buffers para armazenar em cache páginas de dados e índices.

## Serviço de Logging 
Registra todas as transações, operações e modificações no banco de dados em um arquivo de log.

- Reversão de transações em caso de falha.
- Recuperação do banco de dados para um estado consistente após uma falha.
- Replicação de alterações de dados para servidores escravos.
- Auditoria de acesso e alterações no banco de dados. Exemplo, o MongoDB usa oplog para replicação e o WiredTiger usa logging de antemão.

## Ferramentas de Administração 
O SGBD tem algumas utilidades administrativas para tarefas.

- Gerenciamento de usuários, permissões e acesso.
- Capacidade de backup e restauração.
- Inicialização e configuração do banco de dados.
- Monitoramento de atividades e desempenho atuais.
- Gerenciamento de buffers de memória, armazenamento, consultas, etc. Exemplo, o MySQL vem com o MySQL Workbench para administração.

Esses componentes atuam em conjunto para fornecer funcionalidades amplas de gerenciamento de banco de dados em uma variedade de ambientes e aplicações.