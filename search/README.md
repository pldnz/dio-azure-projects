# Provisionando um Serviço de Pesquisa por AI no Azure

Este guia passo a passo ensina a criar e configurar um serviço de pesquisa por AI no Azure. Siga os passos abaixo para provisionar os recursos necessários e configurar o ambiente.

## Recursos Necessários

Você precisará criar os seguintes recursos no Azure:

1. **Azure AI Search**
2. **Azure AI Services**
3. **Conta de Armazenamento**

---

## Passo 1: Criando o Azure AI Search

1. No portal Azure, clique no símbolo de **+** para adicionar um novo recurso.
![Captura de tela 2025-01-21 204146](https://github.com/user-attachments/assets/e94b8440-24f9-452c-ae28-9df45a693a93)

2. Na barra de pesquisa, procure por **Azure AI Search**.
3. Clique no recurso encontrado e, em seguida, clique em **Criar**.
![Captura de tela 2025-01-21 204146](https://github.com/user-attachments/assets/3a846b3e-9bde-4f3c-b6ae-96dd822ecb87)

4. Na tela de configuração:
   - Escolha o plano **Básico** (o custo é menor em relação à versão **Standard**).
![Captura de tela 2025-01-21 204341](https://github.com/user-attachments/assets/d294ea83-7bf9-4409-8051-545b5cbe7f61)


---

## Passo 2: Criando o Azure AI Services

1. Novamente, clique em **+** e procure por **Azure AI Services**.
![Captura de tela 2025-01-21 204551](https://github.com/user-attachments/assets/fb2c7584-572f-4c75-a2c9-0dd35ac9ba64)

2. Selecione o recurso e clique em **Criar**.
![Captura de tela 2025-01-21 204635](https://github.com/user-attachments/assets/64489f71-f90e-4002-bd76-78cfee6b2b6e)


---

## Passo 3: Criando a Conta de Armazenamento

1. Clique em **+** e procure por **Conta de Armazenamento**.
![Captura de tela 2025-01-21 204821](https://github.com/user-attachments/assets/601261e1-7c7d-434e-a6c0-7e151178f68b)

2. Na configuração:
   - **Desempenho**: Padrão
   - **Redundância**: LRS (Locally Redundant Storage)
![Captura de tela 2025-01-21 204949](https://github.com/user-attachments/assets/2aa7a2e5-de48-40b4-9ee6-d032cd7b0f18)


---

## Configurando a Conta de Armazenamento

1. No recurso da conta de armazenamento, na barra lateral, selecione **Configurações > Configuração**.
![Captura de tela 2025-01-21 205126](https://github.com/user-attachments/assets/05e7e372-4447-4baa-a542-f054def73275)

2. Habilite a opção **Permitir acesso anônimo ao Blob**. Isso permitirá que outros serviços consultem o armazenamento.
![Captura de tela 2025-01-21 205144](https://github.com/user-attachments/assets/f311c60f-08f7-43ce-b378-48878a4480c3)

3. Na barra lateral, selecione **Containers** e clique em **+ Container**.
![Captura de tela 2025-01-21 205258](https://github.com/user-attachments/assets/484852ed-5c99-4454-a0eb-ddde75b23806)

4. Crie um container com o nome **coffeereviews** (como sugerido na documentação oficial da Microsoft).
![Captura de tela 2025-01-21 205353](https://github.com/user-attachments/assets/3bd55042-2b92-4545-ac3f-bbee8df51d04)

5. Carregue os arquivos disponíveis no link [https://aka.ms/mslearn-coffee-reviews](https://aka.ms/mslearn-coffee-reviews).
![Captura de tela 2025-01-21 210016](https://github.com/user-attachments/assets/a48cf656-7d66-4fe3-b911-9d70a49ad5c5)


---

## Configurando o Azure AI Search

1. No recurso Azure AI Search, clique em **Importar Dados**.
![Captura de tela 2025-01-21 210122](https://github.com/user-attachments/assets/fe5d442d-7f9e-4c4c-ad47-a5c48769f0fa)

2. Em **Fonte de Dados**, selecione uma fonte de dados existente.
![Captura de tela 2025-01-21 210145](https://github.com/user-attachments/assets/53f97f54-ce31-4cbb-9140-e59f6e735dd3)

3. Configure conforme descrito abaixo:
![Captura de tela 2025-01-21 210457](https://github.com/user-attachments/assets/b2187cb3-c2e9-4cdb-b2d0-96b148b84d5d)

4. Na aba **Habilidades Cognitivas**:
   - Habilite a opção **OCR**.
![Captura de tela 2025-01-21 210654](https://github.com/user-attachments/assets/dd64ebf1-94f6-4017-a14e-b3d9ffce21bc)

   - Ative campos desejados como **Nome de Pessoas**, **Frases-chave**, **Idioma**, etc.
![Captura de tela 2025-01-21 210731](https://github.com/user-attachments/assets/7a506927-75be-488b-9021-1c0b53e9834b)

   - Escolha onde os dados de conhecimento serão salvos:
     - Selecione o armazenamento criado.
     - Crie um novo diretório chamado **coffeeconhecimento**.
![Captura de tela 2025-01-21 210917](https://github.com/user-attachments/assets/4a78c12b-7943-43a9-8ff7-48d40ee739f0)


5. Na aba **Indexador**:
   - Marque os valores **Standard** como filtráveis, o que permitirá pesquisas futuras mais precisas.
![Captura de tela 2025-01-21 211015](https://github.com/user-attachments/assets/e9905dfc-fc20-414c-a572-171c4320006d)
![Captura de tela 2025-01-21 211118](https://github.com/user-attachments/assets/811d25cb-02fa-4266-949b-e62d1c419ed2)



6. Certifique-se de que a chave esteja configurada como **Base64** e submeta a criação.
![Captura de tela 2025-01-21 211151](https://github.com/user-attachments/assets/5bb02eb2-d7fb-4988-9e66-8b924f8924f0)

---

## Explorando a Pesquisa

1. Retorne ao recurso de Azure AI Search e clique em **Explorador de Pesquisa**.
![Captura de tela 2025-01-21 211319](https://github.com/user-attachments/assets/65ff9e0c-8aee-429a-9af2-6d8e9390fe99)

2. Você pode usar parâmetros para realizar buscas. Exemplos:
   - `search=locations:'Chicago'` (retorna comentários sobre esta cidade).
   - `search=sentiment:'negative'` (retorna comentários com sentimento negativo).
![Captura de tela 2025-01-21 211319](https://github.com/user-attachments/assets/8c4d7242-befa-4c5a-b592-207d66ef1f81)


---

## Considerações Finais

Este exemplo demonstra como criar um serviço de busca por IA de documentos no Azure. Este tipo de solução pode ser extremamente útil para organizações que lidam com grandes volumes de documentos, como serviços públicos, permitindo buscas rápidas e eficientes em bases de dados.

