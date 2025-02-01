# Azure Function - HTTP Trigger

Este projeto contém uma Azure Function criada com o runtime .NET e utilizando um gatilho HTTP.

## Pré-requisitos

- Azure Functions Core Tools
- .NET SDK
- Conta na Azure
- CLI do Azure instalada

## Como criar a Azure Function

1. Abra o VS Code e pressione `Ctrl + Shift + P`.
2. Escolha `Azure Functions: Create New Project`.
3. No terminal, dentro do diretório do projeto, execute:
   ```sh
   func init --worker-runtime dotnet
   ```
4. Crie uma nova função HTTP Trigger:
   ```sh
   func new
   ```
   Escolha a opção `HttpTrigger`.

## Como executar localmente

Para rodar a função localmente, utilize o comando:

```sh
func start
```

## Como publicar na Azure

Para publicar a função no Azure, use o nome do aplicativo configurado:

```sh
func azure functionapp publish nome_do_aplicativo
```

Substitua `nome_do_aplicativo` pelo nome do seu aplicativo no Azure, se necessário.

## Acesso à Aplicação

O aplicativo agora está disponível e pode ser acessado utilizando a chave padrão (default).

---

Agora sua função está implantada e pronta para uso!
