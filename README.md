# E-commerce Frontend - Interface de Teste

Interface web responsiva desenvolvida em React para testar e interagir com as APIs do sistema E-commerce Backend. Criada especificamente como ferramenta de apoio para validação e demonstração das funcionalidades da API.

## 🎯 Objetivo

Este frontend foi desenvolvido com foco em **facilitar os testes das APIs** do backend, proporcionando uma interface visual intuitiva para:

- ✅ **Testar todos os endpoints** das APIs
- 🔍 **Visualizar respostas** em tempo real  
- 📝 **Validar funcionalidades** de CRUD
- 🔗 **Demonstrar relacionamentos** entre entidades
- 🚀 **Simular fluxos** completos de e-commerce

## 🛠️ Tecnologias

- **React 19** com **TypeScript** - Interface moderna e tipada
- **Vite** - Build tool rápido para desenvolvimento
- **React Router** - Navegação entre páginas
- **Axios** - Cliente HTTP para consumir APIs
- **CSS Módulos** - Estilização responsiva

## 📱 Funcionalidades

### Páginas de Teste por Módulo

#### 🧑‍💼 **Clientes** (`/clientes`)
- Formulário de criação com validações
- Lista todos os clientes cadastrados
- Edição inline de dados
- Exclusão com confirmação
- Visualização de vendas relacionadas

#### 📦 **Produtos** (`/produtos`)
- Criação com preço e estoque inicial
- Lista com informações de estoque
- Atualização de dados (exceto estoque)
- Remoção de produtos
- Status do estoque em tempo real

#### 📊 **Estoque** (`/estoques`)
- Visualização de todos os itens
- Atualização de quantidades
- Alertas de estoque baixo
- Histórico de movimentações

#### 📋 **Pedidos** (`/pedidos`)
- Criação vinculada a vendas e produtos
- Lista com detalhes completos
- Informações de cliente e produto
- Atualização de quantidades
- Cancelamento de pedidos

#### 💰 **Vendas** (`/vendas`)
- Criação de novas vendas
- Visualização com pedidos inclusos
- Atualização de status
- Cálculo automático de totais
- Fluxo completo de venda

### 🎨 Interface

- **Design Responsivo** - Funciona em desktop, tablet e mobile
- **Navegação Intuitiva** - Menu lateral com todos os módulos
- **Feedback Visual** - Loading states e mensagens de sucesso/erro
- **Formulários Inteligentes** - Validação em tempo real
- **Tabelas Dinâmicas** - Ordenação e busca integrada

## 🚀 Instalação e Uso

### Pré-requisitos
- **Node.js 18+**
- **Backend API** rodando (local ou produção)

### Setup Rápido

1. **Clone e instale**
```bash
git clone <seu-repositorio-frontend>
cd ecommerce-frontend-teste
npm install
```

2. **Configure a API**
```bash
# Crie .env na raiz
VITE_API_URL=http://localhost:3000
# ou para produção:
# VITE_API_URL=https://sua-api.railway.app
```

3. **Inicie o servidor**
```bash
npm run dev
```

4. **Acesse no navegador**
```
http://localhost:5173
```

## 🔧 Configuração da API

### Variáveis de Ambiente

```env
# URL da API Backend
VITE_API_URL=http://localhost:3000

# Timeout das requisições (opcional)
VITE_API_TIMEOUT=5000
```

### Configuração do Axios

```typescript
// src/services/api.ts
import axios from 'axios';

const api = axios.create({
  baseURL: import.meta.env.VITE_API_URL || 'http://localhost:3000',
  timeout: 5000,
  headers: {
    'Content-Type': 'application/json',
  }
});
```

## 📋 Casos de Teste Disponíveis

### 🔄 **Fluxo Completo de Venda**
1. Criar cliente na aba "Clientes"
2. Adicionar produtos na aba "Produtos" 
3. Verificar estoque na aba "Estoque"
4. Criar venda na aba "Vendas"
5. Adicionar pedidos na aba "Pedidos"
6. Finalizar venda alterando status

### ✅ **Validações Testáveis**
- Campos obrigatórios em formulários
- Validação de email e telefone únicos
- Preços negativos em produtos
- Quantidades inválidas em pedidos
- Status de vendas inválidos

### 🔗 **Relacionamentos Visíveis**
- Vendas mostram nome do cliente
- Pedidos exibem produto e cliente
- Estoque vinculado a produtos
- Totais calculados automaticamente

## 📁 Estrutura

```
src/
├── components/      # Componentes reutilizáveis
├── pages/           # Clientes|Produtos|Estoque|Pedidos|Vendas
├── services/api.ts  # Config Axios
└── types/           # TypeScript types
```

## 🚦 Como Usar

### Desenvolvedores Backend
1. Inicie sua API local
2. Configure `VITE_API_URL` 
3. Use o frontend para testar endpoints
4. Valide respostas na interface

### Demonstrações
1. Deploy em Vercel/Netlify
2. Configure para API de produção  
3. Apresente funcionalidades visualmente

---

**📱 Interface para testar APIs | React + TypeScript + Vite**

> Ferramenta de apoio - foco principal nas APIs backend** com cache
- [ ] **Testes automatizados** E2E

---

**📱 Interface prática para testar APIs | React + TypeScript + Vite**

> **Nota**: Este frontend é uma ferramenta de apoio. O foco principal está no desenvolvimento e robustez das APIs backend.