# Trabalhando com Machine Learning na Prática no Azure ML

Este manual tem como propósito trazer um breve resumo de como configurar o serviço de Machine Learning do Azure para ler uma base de dados em um arquivo CSV e apresentar os resultados:

## Ferramenta utilizada

Azure Machine Learning
Disponível em: ml.azure.com

## Detalhamento

### 1 Criação de um recurso
Primeiro devemos criar um recurso clicando no símbolo de + 

![Captura de tela 2025-01-18 180110](https://github.com/user-attachments/assets/3a75708b-9f8c-40b4-8a5e-d29765cb7ff5)

Em seguida utilizar a barra de pesquisa para buscar e selecionar por Azure Machine Learning, em seguida criar o recurso

![image](https://github.com/user-attachments/assets/25e1c489-a02e-4a5f-9990-0726c985e47a)

### 2 Usando o recurso
Com o Recurso de Machine Learning disponível, devemos entrar no mesmo e navegar para o Azure Machine Learning Studio

![image](https://github.com/user-attachments/assets/d0cc252c-3318-4223-b7e2-8e8463dc660f)

Dentro do Studio, iremos criar um novo ML automatizado, para isso basta escolhe-lo na aba lateral e em seguida clicar em Novo trabalho de ML automatizado

![image](https://github.com/user-attachments/assets/8183531f-b54f-46bb-ae59-7a40514a2b2b)

Nas configurações básicas vamos inserir o nome do trabalho, neste caso como segui o passo a passo da própria doc da Microsoft, o nome será aluguel de bikes ou bike rentals

![image](https://github.com/user-attachments/assets/fdef85d8-f417-4071-852c-2adf8f892140)

No próximo passo devemo escolher o tipo de tarefa, neste caso será regressão:

![image](https://github.com/user-attachments/assets/19ff4ace-417e-48b6-ba08-5eeadf4fb1f3)

Em seguida, clique em criar para selecionar os dados que irá utilizar, neste caso irei utilizar um CSV baixado de https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/main/data/ml/bike-data.zip
Utilize o tipo tabular:

![image](https://github.com/user-attachments/assets/7066fba0-6276-4be3-9932-ce9b265771d6)

Em seguida, escolha de arquivos locais, para que possa selecionar o arquivo e armazenar dentro da Azure Storage Blob:

![image](https://github.com/user-attachments/assets/98579cdc-ea5c-4514-baf8-f7b493d9d7d0)
![image](https://github.com/user-attachments/assets/9886b701-db3c-4057-8d4e-b744644a8b78)

Após selecionar, se os dados estiverem tabulados corretamente, teremos um preview como na tela a seguir:

![image](https://github.com/user-attachments/assets/f8fde84e-3009-4188-a38b-0e4723c9ec2e)

Basta seguir avançando até o final neste momento. Após isso estaremos de volta nesta tela, onde deverá escolher os dados e avançar:

![image](https://github.com/user-attachments/assets/012fb284-8e31-4bb4-a790-d2bf1465fe2e)

Em seguida iremos selecionar a coluna de destino, neste caso "rentals):

![image](https://github.com/user-attachments/assets/72c61554-bcf8-4f7e-a9a1-b043ac20d485)

As demais configurações devem ser assim:

![image](https://github.com/user-attachments/assets/b9845ca8-40c0-49d2-a18f-a80ba7df71be)

Na tela seguinte, deveremos informar qual máquina virtual irá examinar os dados, atente-se neste momento que é cobrado um valor pela utilização do serviço:

![image](https://github.com/user-attachments/assets/e2d81c22-3cab-40ea-b1b2-f0924c5eac8a)

Em seguida basta ir para o passo examinar e clicar em Enviar Trabalho de treinamento e esperar uns minutinhos enquanto o Azure processa os dados.

### 3 Conferindo o resultado do processamento

Para encontrar a saída do processamento, basta ir no menu lateral em modelos.
A primeira vez que você acessar, deverá criar um Modelo e registrar, neste caso selecionando de uma saída de trabalho. Em seguida seu recurso estará disponível:

![image](https://github.com/user-attachments/assets/0d7047fd-5b56-479d-a4a5-407ff164d69b)

Para geramos um ponto de extremidade, precisaremos selecionar Implantar:

![image](https://github.com/user-attachments/assets/3911e3a2-2b31-45d5-94d7-413ac2543164)
![image](https://github.com/user-attachments/assets/2eec665a-08a3-4284-a710-201735f63a65)


Importante, caso esteja usando apenas para estudos, exclua os recursos após a aprendizagem para não gerar custos adicionais.






