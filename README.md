# Projeto: Construindo um Pipeline para coletar os dados do Covid no Brasil 

## Motivação do Projeto
 
Desenvolver um pipeline de dados que colete os dados diários do covid de uma api  a fim de acompanhar a evolução da pandemia no Brasil. 

## Descrição do Projeto 

Este projeto será criado em três passos:

  * Coleta dos dados via API por meio do Python;  
  * Processamento dos dados utilizando spark;
  * Realizando a ingestão de dados em banco postgree;

Ambientes utilizados: Azure Databricks e Database. 

## 1 Etapa:

A coleta de dados foi realizada por meio do Python, utilizando a biblioteca requests foi possível consumir os dados direto da url da api. 

![image](https://user-images.githubusercontent.com/89877903/177430387-20beb8cb-e35a-4fa3-aae1-12793e6299ee.png)


## 2 Etapa: 

Após a etapa de extração, foi realizado alguns tratamento de dados utilizando Spark, alguns passos estão contidos abaixo.

![image](https://user-images.githubusercontent.com/89877903/177430501-7f12df9e-df60-4622-b7ed-7f479d2dd9ca.png)

### 3 Passo:

Com os dados no formato desejado, foi realizado o insert nos dados, o ambiente utilizado foi postgee hospedado dentro da azure.

![image](https://user-images.githubusercontent.com/89877903/177430654-099b7326-f831-4a3b-9003-ee3847a7098d.png)


### Resultado: 

Por fim, realizei uma consulta para validar se os dados foram inseridos corretamente:

![image](https://user-images.githubusercontent.com/89877903/177430791-9191d61b-6483-46aa-b698-86e5eeb7f8fc.png)


Pipeline finalizado, basta agendar para que seja executado todos os dias , assim conseguiremos realizar esse acompanhamento com a granularidade de um dia. 



