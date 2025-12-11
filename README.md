# 💰 FinPath

> **"A vida não é linear, seus investimentos também não deveriam ser."**

O **FinPath** é uma plataforma de gestão financeira e simulação de patrimônio projetada para refletir a realidade. Diferente de calculadoras comuns de juros compostos que assumem um aporte fixo por 30 anos, o FinPath introduz o conceito de **Fases de Aporte**, permitindo simular a evolução de carreira (ex: Estagiário → Júnior → Sênior) e como isso impacta a liberdade financeira no longo prazo.

---

## 🚀 O Projeto

Este sistema está sendo construído com uma arquitetura robusta para escalar de um simples simulador para um **SaaS completo de Gestão de Carteira e Controle Financeiro**.

### O Problema
A maioria dos simuladores pergunta: *"Quanto você vai investir por mês?"*.
A realidade é: *"Hoje posso investir R$ 200, mas daqui a 2 anos me formo e posso investir R$ 2.000"*. O FinPath resolve essa lacuna matemática.

---

## 🛠️ Tech Stack & Arquitetura

O projeto utiliza a abordagem **Monorepo** separando as responsabilidades em um ambiente profissional.

### 🧠 Backend (C# .NET 8)
Construído sobre os princípios da **Clean Architecture** (Arquitetura Limpa) para garantir desacoplamento e testabilidade.
- **Framework:** .NET 8 Web API
- **Estrutura:**
  - `Domain`: Entidades e regras de negócio puras (Enterprise Logic).
  - `Application`: Serviços, Casos de Uso e DTOs.
  - `Infrastructure`: Implementação de banco de dados e integrações externas.
  - `Api`: Pontos de entrada REST.

### 🎨 Frontend (React + Vite)
Interface moderna, tipada e de alta performance.
- **Core:** React com TypeScript
- **Build Tool:** Vite (Hot Module Replacement instantâneo)
- **Estilização:** Tailwind CSS v4 (Design System utilitário)

---

## ⚡ Funcionalidades e Roadmap

### ✅ Fase 1: O Simulador Inteligente (Atual)
- [x] Motor de cálculo de Juros Compostos.
- [x] **Linha do Tempo de Aportes:** Criação de múltiplos períodos com valores de aporte distintos.
- [x] Toggle de Reinvestimento: Comparação entre sacar os dividendos vs. Bola de Neve.
- [x] Visualização detalhada da evolução mês a mês.

### 🚧 Fase 2: Gestão de Ativos (Em Desenvolvimento)
- [ ] Sistema de Autenticação e Cadastro (Identity/JWT).
- [ ] Criação de Carteiras (Wallets) personalizadas.
- [ ] Cadastro de ativos reais (Ações, FIIs, Tesouro).
- [ ] Dashboard com gráficos de alocação.

### 🔮 Fase 3: Controle 360º (Futuro)
- [ ] Gestão de Despesas e Contas a Pagar.
- [ ] Integração com Cartões de Crédito (Nubank, Inter).
- [ ] Integração Open Finance.

---

## 📂 Estrutura do Projeto

```text
FinPath/
├── 📂 backend/               # Solução .NET
│   ├── 📂 src/
│   │   ├── 📜 FinPath.Domain       # Entidades (Core)
│   │   ├── 📜 FinPath.Application  # Regras de Negócio (Services)
│   │   ├── 📜 FinPath.Infrastructure
│   │   └── 📜 FinPath.Api          # API Controllers
│
└── 📂 frontend/              # Aplicação React
    ├── 📂 src/
    │   ├── 📂 components/
    │   └── 📜 main.tsx
    └── 📜 tailwind.config.js

---

### 🏁 Como Rodar Localmente
Pré-requisitos
.NET SDK 8.0+

Node.js 18+

1. Rodando a API (Backend)
Bash

cd backend
dotnet restore
dotnet run --project src/FinPath.Api/FinPath.Api.csproj
A API estará rodando em: http://localhost:5000 (ou porta definida pelo .NET)

2. Rodando a Interface (Frontend)
Bash

cd frontend
npm install
npm run dev
O site abrirá em: http://localhost:5173

🤝 Contribuição
Este é um projeto de estudo focado em arquitetura de software e finanças. Sinta-se à vontade para abrir Issues ou Pull Requests.

Desenvolvido por Vinicius Lúcio
