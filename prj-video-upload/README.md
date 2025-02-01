# 📌 Visão Geral

Este projeto consiste em uma solução para upload, armazenamento e exibição de vídeos e thumbnails utilizando **Azure CosmosDB**, **Azure Storage** e **Azure Functions**. O sistema é dividido em duas partes:

- **Backend**: Implementado em **C#** com **Azure Functions** para manipulação de uploads e consulta de dados.
- **Frontend**: Uma página **HTML e CSS** simples que consome as APIs para listar e exibir vídeos.

---

## 🚀 Tecnologias Utilizadas

- **Azure Functions**: Para criação das APIs de upload e exibição.
- **Azure CosmosDB**: Para armazenar os metadados dos vídeos.
- **Azure Storage Account**: Para armazenar os arquivos de vídeo e thumbnails.
- **HTML e CSS**: Para o frontend.
- **Visual Studio e Visual Studio Code**: Para desenvolvimento e execução local.

---

## 📡 APIs Disponíveis

### 1️⃣ FnPostDatabase
Salva os metadados dos vídeos no **CosmosDB**.

### 2️⃣ FnPostStorage
Realiza o upload dos vídeos e thumbnails no **Azure Storage**.

### 3️⃣ FnGetAllMovies
Lista todos os vídeos armazenados.

### 4️⃣ FnGetMovieDetail
Retorna os detalhes de um vídeo específico com base no **ID**.

---

## ⚙️ Configurações para Execução

### 🌐 Configuração do Ambiente Azure
1. Crie uma instância do **Azure CosmosDB**.
2. Crie uma **Storage Account** para armazenar os arquivos.
3. Configure as **Azure Functions** no portal do Azure para as quatro funções descritas.
4. Adicione as configurações necessárias no arquivo `local.settings.json`.

### 💻 Execução Local
1. Abra o projeto no **Visual Studio**.
2. Configure as funções **FnGetAllMovies** e **FnGetMovieDetail** para rodarem juntas.
3. Certifique-se de que todas as dependências do projeto estão instaladas.

### 🎨 Execução do Frontend
1. Coloque o arquivo `api.html` na raiz do projeto.
2. Utilize um servidor local para rodar a página HTML.
   - Exemplo: Use a extensão **Live Server** no **Visual Studio Code**.
   - Acesse: `http://127.0.0.1:5500/api.html`.

---

## 🔍 Como Testar

### 📤 Upload de Arquivos
1. Utilize as APIs **FnPostDatabase** e **FnPostStorage** para realizar uploads de metadados e arquivos (vídeos e thumbnails).

### 📺 Listagem e Exibição
1. Acesse a página HTML.
2. Confirme que os vídeos estão sendo listados corretamente com thumbnails e títulos.
3. Clique em um card para reproduzir o vídeo.

---

## 📌 Observações
- Certifique-se de que os endpoints das APIs **FnGetAllMovies** e **FnGetMovieDetail** estão configurados corretamente na página HTML.
- No **Visual Studio**, é possível configurar o **Multiple Startup Projects** para rodar as duas **Azure Functions** ao mesmo tempo.



