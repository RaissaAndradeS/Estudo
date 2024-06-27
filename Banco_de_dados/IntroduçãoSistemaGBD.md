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

### Controle de Acesso Multiusuário 
O SGBD coordena o acesso de vários usuários e processos concorrentes para garantir a integridade dos dados. Os mecanismos usados são: 

- Controle de concorrência para evitar atualizações perdidas por meio de bloqueio, ordenação de carimbo de data/hora, etc.
- Níveis de isolamento para isolar transações de leituras incorretas ou outras operações conflitantes.
- Atomicidade para possibilitar a execução de transações tudo ou nada.
- Durabilidade para persistir todas as alterações confirmadas mesmo após falhas.
- Consistência para manter a correção dos dados entre transações.
- Isso garante as propriedades ACID que orientam transações de banco de dados confiáveis.

### Backup e Recuperação 
O SGDB fornece utilitários para fazer backup de dados e matadados regularmente e restaurá-los quando necessário. Isso inclui:

- Backup online ou offline dos arquivos do banco de dados, logs de transações e configurações.
- Recuperção até um ponto no tempo para restaurar o banco de dados a um estado consistente anterior.
- Recuperação baseada em log usando logs de transações para desfazer transações não confirmadas após uma falha.
- Arquivamento de dados antigos e backups para retenção de longo prazo e fins de descobreta eletrônica.
- Capacidades de espelhamento e replicação para manter cópias redundantes de dados em locais remotos.

### Integridade de Dados 
O SGBD valida os dados para garantir que atendam às restrições de integridade definidas:

- Integridade da entidade via chaves primárias que identificam exclusivamente linhas.
- Integridade referencial entre tabelas relacionadas com base em chaves estrangeiras.
- Integridade de domínio para validar formatos de dados, intervalos e valores aceitáveis.
- Restrições personalizadas usando condições de verificação para linhas.
- Restrições complexas que abrangem várias tabelas, como restrições de junção exponencial.
- Isso impede que dados incorretos sejam armazenados no banco de dados.

## Suporte a Transações 
O SGBD agrupa operações em transações que são executadas de forma confiável como uma unidade única:

- Inicia uma transação, termina com commit/rollback com base no sucesso.
- Mantém isolamento para que as alterações não sejam visíveis até o commit.
- Recupera transações falhadas para o estado consistente anterior.
- Bloqueia os dados acessados para evitar operações conflitantes.
- Registra etapas da transações para recuperação de falhas e auditoria.
- Isso garante que as alterações de uma transação seja aplicada ou descartada de forma confiável.

### Recuperação de Falhas 
O SGBD recupera o banco de dados de forma confiável após falhas ou crashes inesperados:

- Usa log de transações antecipadas para refazer alterações confirmadas.
- Desfaz alterações não confirmadas rolando para trás usando log.
- Restaura arquivos de dados corrompidos ou danificados a partir de backups conforme necessário.
- Libera bloqueos e limpa após transações falhadas.
- Reinicia transações que estavam ativas durante uma falha após a recuperação.
- Isso restaura o banco de dados para o último estado confirmado, garantido durabilidade.

### Controle de Concorrência
O SGBD coordena o acesso por usuários e processos concorrentes:

- Métodos baseados em bloqueio como bloqueio de duas fases para evitar leituras incorretas.
- Métodos otimistas como controle de concorrência de várias versões detectando conflitos no momento do commit.
-
-
-
