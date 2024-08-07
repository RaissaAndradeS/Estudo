## <center>Organização de Arquivos em SGBD</center>

Diz sobre a disposição dos dados em um arquivo ou tabela de banco de dados. Na ciência da computação, a organização de arquivos é um conceito importante usado no design e implementação de sistemas de arquivos e sistemas de gerenciamento de banco de dados. A forma como os dados são organizados em um arquivo ou tabela pode ter um impacto significativo na eficiência e velocidade de acesso e recuperação de dados.

## Os quatros tipos de organização 

### Organização Sequencial de Arquivos
Os dados são armazenados sequencialmente em um arquivo ou tabela. Aui os dados são acessados sequencialmente na prdem em que são armazenados, começando do inicio do arquivo e seguindo em direção ao final.

![Sequencial](assets/organização/sequencial.png)

### Organização de Arquivos Indexada
Os dados são armazenados em um arquivo ou tabela com um índice. O indice é uma estrutura de dados que contém ponteiros para a localização dos dados dentro do arquivo ou tabela, facilitando e acelerando a busca por registros específicos.

![Indexada](assets/organização/indexada.png)

### Organização de Arquivos de Hash
Os dados são armazenados em um arquivo ou tabela usando uma função de hash. A função de hash converte um valor de chave em um código de hash, que é usado para mapear a chave para a localização no arquivo ou tabela onde os dados são armazenados.

![Hash](assets/organização/hash.png)

### Organização de Arquivos Clusterizados
Na organização de arquivos clusterizados, os dados são armazenados em um arquivo ou tabela com base nos valores de uma ou mais colunas, chamadas de chave de clustering. A chave de clustering determina a ordem física na qual os dados são armazenados no disco. <br>
A escolha da organização de arquivos depende de vários fatores, como o tipo de dados armazenados, a frequência e os tipos de consultas realizadas nos dados e os recursos de hardware disponíveis. Portanto, escolher a organização de arquivos certa é fundamentel para o desempenho e eficiência de um sistema de computador.

