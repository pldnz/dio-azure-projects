# Guia de Criação e Utilização do Serviço de Linguagem no Azure

Este guia descreve o passo a passo para criar e utilizar um serviço de linguagem no portal do Azure e realizar análises de sentimentos.

---

## 1. Criando o Recurso de Serviço de Linguagem

1. Acesse o portal do Azure.
2. Clique no botão **+** para criar um novo recurso.
![Captura de tela 2025-01-19 202807](https://github.com/user-attachments/assets/8f696cec-2d8b-40df-96f5-0a075942323b)

3. Na barra de pesquisa, digite **"serviço de linguagem"** e selecione a opção correspondente.
4. Clique em **"Create"** para iniciar a criação do recurso.
![Captura de tela 2025-01-19 202844](https://github.com/user-attachments/assets/3f5b6136-b521-4aac-9f5f-b0ede951dc46)

5. Na próxima tela, clique em **"Continue to create your resource"**.
![Captura de tela 2025-01-19 202920](https://github.com/user-attachments/assets/15da2ac9-d1f2-4cef-9eb6-5e7fa1ebaab9)

6. Preencha os seguintes campos no formulário de criação:
   - **Assinatura:** Selecione sua assinatura.
   - **Grupo de Recursos:** Escolha um grupo existente ou crie um novo.
   - **Região:** Selecione a região desejada.
   - **Nome:** Defina um nome para o recurso.
7. Clique em **"Examinar e criar"**. Se todas as informações estiverem corretas, o botão **"Criar"** será habilitado.
![Captura de tela 2025-01-19 202956](https://github.com/user-attachments/assets/43036b62-5811-4e3c-9962-f547673aecf9)

8. Clique em **"Criar"** para finalizar o processo.
![Captura de tela 2025-01-19 203140](https://github.com/user-attachments/assets/b6d6c787-d5cb-48a3-b733-b2b8a4548e1a)

---

## 2. Acessando o Language Studio

1. Após a criação, o recurso estará disponível dentro do grupo de recursos selecionado.
2. Acesse o recurso e clique em **"Get started with Language Studio"**.
![Captura de tela 2025-01-19 203243](https://github.com/user-attachments/assets/e7ca3351-e34b-417a-9afd-937b749f63e1)
![Captura de tela 2025-01-19 203310](https://github.com/user-attachments/assets/19b3fd24-938e-43ee-ab91-a34b3f927194)

---

## 3. Analisando Sentimentos

1. No **Language Studio**, selecione a opção **"Classify text"**.
2. Escolha **"Analyze sentiment and mine opinions"**.
![Captura de tela 2025-01-19 203349](https://github.com/user-attachments/assets/0fe8b645-2392-4a61-9e98-976ccf19426f)
 
3. Configure a análise:
   - **Idioma do Texto:** Selecione o idioma do texto que será analisado.
   - **Input:** Insira o texto na área de entrada disponível.
![Captura de tela 2025-01-19 203607](https://github.com/user-attachments/assets/72dc3b58-2401-457d-a69e-715c2ea5187e)

4. Após o processamento, os resultados serão exibidos:
   - Análise detalhada frase por frase.
   - Um arquivo JSON com os valores da análise.
![Captura de tela 2025-01-19 203654](https://github.com/user-attachments/assets/12568fbc-fe1a-478c-8a7b-359a77589241)

---

## 4. Estrutura de Diretórios

Neste projeto, temos dois diretórios com os respectivos documentos:

- **input.txt:** Contém o texto utilizado para análise.
- **output.json:** Contém o resultado da análise.

---

## Observações

- Certifique-se de que o grupo de recursos e a região selecionados atendam às suas necessidades.
- A análise de sentimentos permite entender melhor a percepção geral e a opinião das frases inseridas.

Explore outras funcionalidades do Language Studio para enriquecer suas análises!
