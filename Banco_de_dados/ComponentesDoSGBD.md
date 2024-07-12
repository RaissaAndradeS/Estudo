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
