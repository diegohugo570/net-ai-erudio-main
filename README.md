# 🤖 .NET AI — Integração com Inteligência Artificial em Aplicações .NET

Projeto backend desenvolvido com **.NET** que demonstra a integração com modelos de Inteligência Artificial, permitindo a criação de APIs inteligentes com geração de texto, respostas automatizadas e aplicações baseadas em LLMs.

O objetivo é fornecer uma base prática para desenvolvimento de soluções com IA no ecossistema Microsoft.

---

## 🚀 Tecnologias Utilizadas

### 🔙 Backend
- .NET 6+ / .NET 7+ / .NET 8  
- ASP.NET Core  
- Minimal APIs / Controllers  
- Dependency Injection  

### 🧠 Inteligência Artificial
- OpenAI API (ChatGPT)  
- Azure OpenAI *(opcional)*  
- Outros provedores compatíveis  

### ⚙️ Ferramentas
- Swagger / OpenAPI  
- Logging nativo do .NET  
- IConfiguration (configuração de ambiente)  

---

## ⚙️ Como Rodar o Projeto Localmente

### 1️⃣ Clonar o Repositório

```bash
git clone <url-do-repositorio>
cd net-ai-erudio-main
```
2️⃣ Configurar Variáveis de Ambiente

Você precisará de uma chave de API (OpenAI ou Azure OpenAI).

📌 appsettings.json
{
  "OpenAI": {
    "ApiKey": "SUA_API_KEY_AQUI",
    "Model": "gpt-4"
  }
}

Ou via variável de ambiente:

export OPENAI_API_KEY=SUA_API_KEY_AQUI

3️⃣ Restaurar Dependências
```
dotnet restore
```
4️⃣ Executar a Aplicação
```
dotnet run
```
Servidor disponível em:
```
👉 http://localhost:5000
```
```
👉 http://localhost:5001
 (HTTPS)
 ```

5️⃣ Acessar Swagger
```
👉 http://localhost:5000/swagger
```

📡 Endpoints Principais

🔹 Geração de Texto
POST /api/ai/generate

Body:

{
  "prompt": "Explique o que é .NET"
}
🔹 Chat com IA
POST /api/ai/chat
🔹 Health Check
GET /health

---

🧠 Decisões Técnicas

- ASP.NET Core foi escolhido pela performance e maturidade no desenvolvimento de APIs.

- Uso de Dependency Injection nativo para desacoplamento.

- Integração com IA feita via serviços isolados, facilitando manutenção.

- Estrutura organizada em camadas:

- Controllers → entrada HTTP

- Services → lógica de negócio

- Config → integração com IA

- Configuração via appsettings.json e variáveis de ambiente.

---

📦 Funcionalidades Implementadas

- 🤖 Integração com OpenAI
- 💬 Chat com IA
- 🧠 Geração de texto
- 📡 API REST documentada com Swagger
- ⚙️ Configuração flexível

---

🏗️ Estrutura do Projeto
```
.
├── Controllers/
├── Services/
├── Models/
├── Config/
├── Program.cs
├── appsettings.json
└── README.md
```

---

🚀 Deploy

- Backend (.NET)

- dotnet publish -c Release -o out
- dotnet out/YourApp.dll
- Docker
- docker build -t net-ai-app .
- docker run -p 5000:5000 net-ai-app
- Cloud
- Azure App Service
- AWS
- Render / Railway

---

🔐 Segurança

- Nunca versionar API Keys
- Utilizar Azure Key Vault ou Secrets Manager
- Implementar autenticação em produção
- Monitorar uso de tokens

---

📈 Possíveis Evoluções

- 🔐 Autenticação com JWT

- 🧠 Memória de conversação

- 📊 Observabilidade (logs + métricas)

- 🔍 RAG com embeddings

- ⚡ Cache de respostas

- 🌐 Integração com frontend (Blazor / React)

---

🎯 Objetivo do Projeto

- Aprender integração de IA com .NET
- Criar APIs inteligentes
- Servir como base para aplicações reais com IA
- Demonstrar uso de LLMs no ecossistema Microsoft

---

📚 Referências

- https://learn.microsoft.com/dotnet
- https://platform.openai.com/docs
- https://learn.microsoft.com/azure/ai-services
---
