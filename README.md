# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

Bem-vindo ao meu projeto de Previsão de Estoque Inteligente na AWS com SageMaker Canvas. Este projeto se trata da aplicação prática de meus conhecimentos desenvolvidos ao longo do Bootcamp Nexa - Machine Learning para Iniciantes na AWS, realizado na plataforma DIO.me.

## Dataset

O dataset utilizado foi um dos próprios disponibilizados no template do projeto:
[dataset-1000-com-preco-promocional-e-renovacao-estoque.csv](https://github.com/user-attachments/files/16415030/dataset-1000-com-preco-promocional-e-renovacao-estoque.csv)

## Meu Modelo de ML

- Quick Builded
- Average Weighted Quantile Loss (wQL): 0.154
- Mean Absolute Percent Error (MAPE): 1.789
- Weighted Absolute Percent Error (WAPE): 0.250
- Root Mean Square Error (RMSE): 25.934
- Mean Absolute Scaled Error (MASE): 0.961

Foi objetivada a previsão de três dias.
Nos termos das margens de erros resultantes, é perceptível que a precisão das previsões tem relação direta com a forma da qual o modelo de ML foi construído, assim como também depende da quantidade de informações constantes nos datasets. 
Neste cenário, seria possível alcançar uma maior precisão nas previsões com um alongamento do dataset e uma Standard Build.

## Impacto das Colunas

Concluiu-se que a coluna PRECO tem 17.39% de impacto na QUANTIDADE_ESTOQUE.

## Resultados e Previsões

Optei por exportar as previsões dos próximos três dias, abordando os cinco primeiros itens do estoque.

### Item 1000

![1000](https://github.com/user-attachments/assets/0efc4768-96ac-4d2b-89b4-6b25bd02e6d2)

### Item 1001

![1001](https://github.com/user-attachments/assets/78d6612c-c382-4d85-a6a5-d4528f4be3cb)

### Item 1002

![1002](https://github.com/user-attachments/assets/0b24449d-f693-4056-88d0-26e7f0fa8985)

### Item 1003

![1003](https://github.com/user-attachments/assets/3088c8d4-5825-4e7a-9210-1a3856df96a5)

### Item 1004

![1004](https://github.com/user-attachments/assets/06118b02-fad9-439b-b266-6a1cf7eb552c)

## Síntese

Temos aqui como critério do dataset o fato de que o estoque de um determinado item é reposto (100) quando sua quantidade é zerada.
Embora o modelo criado tenha resultado em dados não tão realistas no caso o Item 1000, onde previu-se a reposição em situações em que não a haveria, é conclusível que as previsões dos outros itens mostram estatísticas das quais podem propor diversos insights valiosos, capazes de trazer vantagens consideráveis em um caso real.

É nestes termos que o Amazon SageMaker Canvas se mostra como uma ferramenta capaz de trazer muita vantagem competitiva ao seu usuário, principalmente em utilizações preditivas ou analíticas, visto que um modelo de Machine Learning é capaz de visualizar dados e padrões de forma em que um ser humano seria muitas vezes inábil.
