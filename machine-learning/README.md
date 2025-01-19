# Trabalhando com Machine Learning na Prática no Azure ML

Este guia apresenta um passo a passo sobre como configurar o serviço **Azure Machine Learning** para carregar uma base de dados em formato CSV, processar os dados e apresentar os resultados. 

---

## Ferramenta utilizada

- **Azure Machine Learning**
- Acesse em: [ml.azure.com](https://ml.azure.com)

---

## Passo a Passo

### 1. Criação de um Recurso

1. No portal do Azure, clique no símbolo de **+** para criar um recurso.
2. Utilize a barra de pesquisa para buscar por **Azure Machine Learning** e selecione-o.
3. Clique em **Criar** para provisionar o recurso.

![Criação do Recurso](https://github.com/user-attachments/assets/25e1c489-a02e-4a5f-9990-0726c985e47a)

---

### 2. Usando o Recurso no Azure Machine Learning Studio

1. Acesse o recurso criado e clique em **Azure Machine Learning Studio**.

![Acessando o Studio](https://github.com/user-attachments/assets/d0cc252c-3318-4223-b7e2-8e8463dc660f)

2. No Studio, clique em **ML Automatizado** no menu lateral e selecione **Novo trabalho de ML automatizado**.

![Criando um Trabalho](https://github.com/user-attachments/assets/8183531f-b54f-46bb-ae59-7a40514a2b2b)

#### Configuração do Trabalho

- **Nome do Trabalho**: Utilize um nome descritivo, como "Aluguel de Bikes" ou "Bike Rentals".
- **Tipo de Tarefa**: Escolha **Regressão** para prever valores numéricos baseados nos dados.

![Configuração do Trabalho](https://github.com/user-attachments/assets/19ff4ace-417e-48b6-ba08-5eeadf4fb1f3)

---

### 3. Carregando e Configurando os Dados

1. Faça o download do arquivo CSV para teste:
   - [Bike Data CSV](https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/main/data/ml/bike-data.zip)

2. No Studio, selecione **Criar Dados** > **Carregar Arquivo Local** e armazene o arquivo na **Azure Storage Blob**.

![Upload de Dados](https://github.com/user-attachments/assets/7066fba0-6276-4be3-9932-ce9b265771d6)

3. Confirme se os dados foram tabulados corretamente no preview exibido.

![Preview dos Dados](https://github.com/user-attachments/assets/f8fde84e-3009-4188-a38b-0e4723c9ec2e)

4. Avance e selecione os dados carregados. Escolha a coluna de destino, como **rentals**.

![Selecionando Coluna de Destino](https://github.com/user-attachments/assets/72c61554-bcf8-4f7e-a9a1-b043ac20d485)

---

### 4. Configurando a Máquina Virtual e Executando o Trabalho

1. Escolha uma máquina virtual para processar os dados. **Atenção**: Esse serviço pode gerar custos.

![Configuração de Máquina Virtual](https://github.com/user-attachments/assets/e2d81c22-3cab-40ea-b1b2-f0924c5eac8a)

2. Clique em **Enviar Trabalho de Treinamento** e aguarde o processamento.

---

### 5. Conferindo os Resultados

1. Após o treinamento, acesse **Modelos** no menu lateral.
2. Registre o modelo criado utilizando a saída do trabalho.

![Registro do Modelo](https://github.com/user-attachments/assets/0d7047fd-5b56-479d-a4a5-407ff164d69b)

3. Para criar um endpoint de inferência, selecione **Implantar** e configure conforme necessário.

![Implantação do Modelo](https://github.com/user-attachments/assets/3911e3a2-2b31-45d5-94d7-413ac2543164)

---

## Observações

- Caso esteja utilizando o serviço apenas para estudos, **exclua os recursos provisionados** após o uso para evitar custos adicionais.
- Para mais detalhes, consulte a [documentação oficial do Azure Machine Learning](https://learn.microsoft.com/azure/machine-learning/).

---

Aproveite o potencial do Azure Machine Learning para simplificar e otimizar suas aplicações de inteligência artificial!
