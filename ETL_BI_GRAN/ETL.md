Business Intelligence - ETL

Esse é o processo entre as fontes de dados originais OLTP e o DW. 

Etapas:

    Extração - um banco de dados, planinhas, api, redes sociais são fontes de dados das organizações e eles estão em OLTP. 
    - Extração de dadosdas fontes de dado.
    - Identificação de fontes de dados.
    - Conexão e acesso aos dados.
    - Extração dos dados.
    - Notificação de atualização. -> de quanto em quanto tempo os dados precisam ser atualizados? de quanto em quanto tempo precisa rodar um etl para atualizar o dw? 
    - Extração gradual ou completa. -> Completa geralmente é a primeira, depois que todos os dados já estiverem no dw, a extração é gradual.
    - Principais fontes: 
        - Bancos de dados relacionais.
        - Arquivos CSV.
        - Arquivos Excel.
        - Fontes recebidas via API.
        - Sistemas ERP ou CRM.
        - Logs.
        - Sistema de legados.
        - Fontes de dados externas.

    Transformação - a transformação é a segunda etapa e guiada pelas regras de negócios. 
        - Realizada na Staging Area.
        - Baseada nas regas de negócio.
        - Limpeza de dados:
            - Tratamento de ruídos.
            - Dados duplicados.
            - Erros de formatação.
            - Valores ausentes.
            - Outliers (Ponto fora da curva)
        - Padronização e formatação:
            - Padronização de medidas e formatos.
            - Normalização de dados.
        - Trasformações relacionadas a segurança.
        - Filtragem e seleção.
        - Enriquecimento de dados.
        - Transformação de dados: 
            - Agregações.
            - Cálculo de campos derivados. 
            - Transformação de tipos de dados.
    
    Carga:
        - Carga de dados no DW ou no Data Mart.
        - Carregamento em lote ou em tempo real.
        - Modelagem do esquema.
        - Carregamento inicial.
        - Atualizações incrementais.
        - Validação dos dados.
        - Avaliação da qualidade dos dados.
        - Indexação de dados.
        - Otimização de dados.

ELT - Um novo fluxo de transformação de dados. A carga ocorre antes da transformação. 
Extrai os dados e já carrega no Data Lake e e só transforma o que de fato precisa levar para o DW.

ETL - Voltado ao DW.
ELT -  Voltado mais para Machine Learning.

ELT 
    - Alternativa mais recente ao ETL.
    - Extração:
        - Identificação das fontes de dados.
        - Conexão e acesso a dados.
    - Carga:
        - Carregamento Inical no Data Lake.
        - Estruturação dos dados.
    - Transformação dos dados: 
        - Preparação e transformação dos dados.
        - Uso de recursos nativos do ambiente de destino. Diferente do ETL que toda transformação é dendo do banco de dados intermediário da stage area.

ETL X ELT 

    ELT : 
        - Pipepiles com menos maturidade 
        - Menos profissionais habilitados.
        - Foco em dados semi-estruturados e não estruturados.
        - Foco em grandes bases de dados.
        - Engenheiros de dados focam apenas na extração e carga.
        - Os dados sempre estão disponíveis.
        - Mais adaptado a data lakes.
        - Reduz o tempo de carga dos dados. 
        - Baixo custo de manutenção do repositório de dados.
        - Menos segurança no processo.
        - Transformação ocorre no ambiente de destino.
        - Transformação é mais rápida.
        - Transformação é feita por especialistas do negócio.
        - Permite a passagem de dados não estruturados para a Análise.
        - Análises mais demoradas e menos estáveis.
        - Esquema gravado no momento de análise (leitura).
        
    



