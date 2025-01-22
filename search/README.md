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
2. Na barra de pesquisa, procure por **Azure AI Search**.
3. Clique no recurso encontrado e, em seguida, clique em **Criar**.
4. Na tela de configuração:
   - Escolha o plano **Básico** (o custo é menor em relação à versão **Standard**).

---

## Passo 2: Criando o Azure AI Services

1. Novamente, clique em **+** e procure por **Azure AI Services**.
2. Selecione o recurso e clique em **Criar**.

---

## Passo 3: Criando a Conta de Armazenamento

1. Clique em **+** e procure por **Conta de Armazenamento**.
2. Na configuração:
   - **Desempenho**: Padrão
   - **Redundância**: LRS (Locally Redundant Storage)

---

## Configurando a Conta de Armazenamento

1. No recurso da conta de armazenamento, na barra lateral, selecione **Configurações > Configuração**.
2. Habilite a opção **Permitir acesso anônimo ao Blob**. Isso permitirá que outros serviços consultem o armazenamento.
3. Na barra lateral, selecione **Containers** e clique em **+ Container**.
4. Crie um container com o nome **coffeereviews** (como sugerido na documentação oficial da Microsoft).
5. Carregue os arquivos disponíveis no link [https://aka.ms/mslearn-coffee-reviews](https://aka.ms/mslearn-coffee-reviews).

---

## Configurando o Azure AI Search

1. No recurso Azure AI Search, clique em **Importar Dados**.
2. Em **Fonte de Dados**, selecione uma fonte de dados existente.
3. Configure conforme descrito abaixo:

   ![Configuração da Fonte de Dados](inserir-link-da-imagem-aqui)

4. Na aba **Habilidades Cognitivas**:
   - Habilite a opção **OCR**.
   - Ative campos desejados como **Nome de Pessoas**, **Frases-chave**, **Idioma**, etc.
   - Escolha onde os dados de conhecimento serão salvos:
     - Selecione o armazenamento criado.
     - Crie um novo diretório chamado **coffeeconhecimento**.

5. Na aba **Indexador**:
   - Marque os valores **Standard** como filtráveis, o que permitirá pesquisas futuras mais precisas.

6. Certifique-se de que a chave esteja configurada como **Base64** e submeta a criação.

---

## Explorando a Pesquisa

1. Retorne ao recurso de Azure AI Search e clique em **Explorador de Pesquisa**.
2. Você pode usar parâmetros para realizar buscas. Exemplos:
   - `search=locations:'Chicago'` (retorna comentários sobre esta cidade).
   - `search=sentiment:'negative'` (retorna comentários com sentimento negativo).

---

## Considerações Finais

Este exemplo demonstra como criar um serviço de busca por IA de documentos no Azure. Este tipo de solução pode ser extremamente útil para organizações que lidam com grandes volumes de documentos, como serviços públicos, permitindo buscas rápidas e eficientes em bases de dados.

