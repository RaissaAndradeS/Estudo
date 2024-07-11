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
