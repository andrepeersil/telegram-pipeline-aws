# telegram-pipeline-aws
Este projeto visa o desenvolvimento de um Pipeline de Dados, com o objetivo de capturar, armazenar e transformar mensagens provenientes de um grupo no Telegram. O pipeline será responsável por ingerir os dados em intervalos de 24h, realizar o processamento e armazenamento em uma infraestrutura de dados otimizada para suportar consultas eficientes.

Foi usado a API do Telegram para a extração das mensagens de um grupo, através de um bot, também criando nativamente dentro do Telegram. Com o uso de Webhook e da AWS API Gateway os dados crus no formato JSON foram extraídos e com uma função da AWS Lambda foram armazenados em um Bucket na Amazon S3.

Também foi realizado a etapa de ETL, onde foi criada uma segunda função com a AWS Lambda que transformou os dados crus(JSON), foram transformados no formato Parquet e armazenados em um segundo Bucket Amazon S3.

Na última etapa os dados foram extraídos dentro do AWS Athena, para consultas SQL.

Arquitetura do projeto:
<img src="https://i.ibb.co/CzmH3mt/diagrama.jpg" alt="arquitetura">

