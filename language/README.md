# Guia de Criação e Utilização do Serviço de Linguagem no Azure

Este guia descreve o passo a passo para criar e utilizar um serviço de linguagem no portal do Azure e realizar análises de sentimentos.

---

## 1. Criando o Recurso de Serviço de Linguagem

1. Acesse o portal do Azure.
2. Clique no botão **+** para criar um novo recurso.
3. Na barra de pesquisa, digite **"serviço de linguagem"** e selecione a opção correspondente.
4. Clique em **"Create"** para iniciar a criação do recurso.
5. Na próxima tela, clique em **"Continue to create your resource"**.
6. Preencha os seguintes campos no formulário de criação:
   - **Assinatura:** Selecione sua assinatura.
   - **Grupo de Recursos:** Escolha um grupo existente ou crie um novo.
   - **Região:** Selecione a região desejada.
   - **Nome:** Defina um nome para o recurso.
7. Clique em **"Examinar e criar"**. Se todas as informações estiverem corretas, o botão **"Criar"** será habilitado.
8. Clique em **"Criar"** para finalizar o processo.

---

## 2. Acessando o Language Studio

1. Após a criação, o recurso estará disponível dentro do grupo de recursos selecionado.
2. Acesse o recurso e clique em **"Get started with Language Studio"**.

---

## 3. Analisando Sentimentos

1. No **Language Studio**, selecione a opção **"Classify text"**.
2. Escolha **"Analyze sentiment and mine opinions"**.
3. Configure a análise:
   - **Idioma do Texto:** Selecione o idioma do texto que será analisado.
   - **Input:** Insira o texto na área de entrada disponível.
4. Após o processamento, os resultados serão exibidos:
   - Análise detalhada frase por frase.
   - Um arquivo JSON com os valores da análise.

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
