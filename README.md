# Support Tickets API

API REST para gerenciamento de tickets de suporte construída em Node.js puro (sem frameworks externos), utilizando módulos nativos como `http`, `crypto`, e persistência em arquivo JSON.

## 🚀 Tecnologias

- [Node.js](https://nodejs.org/) (ES Modules)
- Persistência em arquivo JSON

## 📌 Rotas da API

### Tickets

- `POST /tickets` - Cria um novo ticket de suporte
  - **Body:** `{ "equipment": "Computador", "description": "Computador não liga", "user_name": "João Vitor" }`
- `GET /tickets` - Lista todos os tickets (suporta query params, ex: `/tickets?status=open`)
- `PUT /tickets/:id` - Atualiza as informações de um ticket
  - **Body:** `{ "equipment": "Notebook", "description": "Tela quebrada" }`
- `PATCH /tickets/:id/close` - Fecha o status do ticket para `closed`
- `DELETE /tickets/:id` - Remove um ticket pelo ID

## 🛠️ Como rodar o projeto

1. Clone o repositório:
```bash
git clone https://github.com/jvcv2807/support-tickets.git
cd support-tickets
```

2. Execute o servidor em modo de desenvolvimento:
```bash
npm run dev
```

O servidor estará rodando em `http://localhost:3333`.
