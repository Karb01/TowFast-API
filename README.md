# 🚗 TowFast-API (.NET 8)

**TowFast-API** é uma aplicação backend desenvolvida em **.NET 8** para gerenciar serviços de guincho e assistência veicular.  
Ela oferece endpoints RESTful para cadastro, autenticação, gerenciamento de solicitações e integração com sistemas externos.

---

## 🔍 Visão Geral

O projeto adota uma **arquitetura em camadas**, separando responsabilidades em:

- **Controllers**
- **Models**
- **DbContext** (Entity Framework Core)

Utiliza o **SQL Server** como banco de dados principal e gera documentação automatizada com o **Swagger**.

---

## ✅ Funcionalidades

- Cadastro e autenticação de usuários (Motorista e Guincho)
- Gerenciamento de solicitações de guincho
- Atualização de status dos serviços e localização em tempo real
- Integração com *stored procedures* no SQL Server
- Documentação automática via **Swagger**

---

## 🛠️ Tecnologias Utilizadas

- **.NET 8** (ASP.NET Core Web API)
- **Entity Framework Core**
- **SQL Server**
- **Swashbuckle** (Swagger)
- **BCrypt.Net** (Hash de senha)
- **CORS** configurado para acesso externo

---

## 📁 Estrutura de Pastas

```
TowFast_API/
├── Controllers/      # Endpoints da API (ex: LogarController)
├── Context/          # DbContext (TowFastDbContext)
├── Models/           # Modelos de domínio (Cliente, Guincho, Veiculo, etc)
├── Properties/       # launchSettings.json e configs do projeto
├── TowFast_API.csproj
└── appsettings.json  # Configurações e connection strings
```

---

## 🗂️ Principais Arquivos

- **Program.cs** – Inicialização da aplicação  
- **Startup.cs** – Configuração de serviços, Swagger, CORS e pipeline  
- **TowFastDbContext.cs** – Contexto do EF Core  
- **Controllers/LogarController.cs** – Autenticação, registro, status e solicitações  
- **Models/** – Entidades como Usuário, Veículo, Endereço, Solicitação

---

## ⚙️ Instalação

1. Clone este repositório:
   ```bash
   git clone [https://github.com/seu-usuario/TowFast-API.git](https://github.com/Karb01/TowFast-API.git)
   ```

2. Restaure os pacotes NuGet:
   ```bash
   dotnet restore
   ```

3. Configure a string de conexão no arquivo `appsettings.json`:
   ```json
   "ConnectionStrings": {
     "SqlTowFast": "Server=SEU_SERVIDOR;Database=TowFast;Trusted_Connection=True;TrustServerCertificate=Yes"
   }
   ```

4. Execute as migrações (se necessário):
   ```bash
   dotnet ef database update
   ```

---

## 🚀 Execução

Inicie a API com o comando:

```bash
dotnet run --project TowFast_API
```

Acesse a documentação Swagger em:  
`https://localhost:5001/swagger` *(ou conforme sua configuração)*

---

## 🧪 Testando Endpoints

Você pode usar o arquivo `TowFast_API.http` para testar os endpoints diretamente do **Visual Studio** ou **VS Code**.

---

## 🤝 Contribuição

Contribuições são muito bem-vindas!  
Abra uma *issue* ou envie um *pull request*.

---

## 📝 Licença

Este projeto está licenciado sob a **MIT License**.
