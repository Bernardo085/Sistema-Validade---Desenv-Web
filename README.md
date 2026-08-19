# Sistema de Gerenciamento de Validade de Produtos

Sistema full-stack para controle de validade de produtos, voltado para pequenos e médios comércios. Automatiza o acompanhamento de lotes, gera alertas de vencimento e centraliza indicadores de estoque em um dashboard.

> Projeto acadêmico desenvolvido durante o curso de Ciência da Computação (UNIFOR).

<!-- Adicione aqui 1-2 prints ou um GIF do dashboard/telas principais. Isso é o que mais chama atenção de quem abre o repositório. -->
<!-- ![dashboard](caminho/para/imagem.png) -->

## Funcionalidades

- Autenticação de usuários com JWT e controle de acesso por papel (role-based access)
- CRUD completo de produtos, categorias, lotes e movimentações de estoque
- Verificação automática diária de validade (job agendado com `node-cron`), com atualização de status dos lotes
- Geração de alertas com níveis de severidade (crítico / atenção)
- Dashboard com indicadores em tempo real: lotes ativos, vencendo em breve, vencidos e alertas pendentes
- Relatórios filtráveis por data, produto e status

<!-- Se/quando implementar exportação em PDF/CSV ou lógica FEFO, adicione aqui -->

## Tecnologias

**Backend:** Node.js • Express • TypeScript • MongoDB (Mongoose) • JWT • bcrypt • node-cron
**Frontend:** React • TypeScript • Vite • React Router • Bootstrap

## Arquitetura

O backend segue uma arquitetura em camadas:

```
routes → controllers → services → repositories → models
                ↓
         dtos (request/response) + mappers
```

Essa separação isola regras de negócio (services) do acesso a dados (repositories) e da camada HTTP (controllers), facilitando manutenção e testes.

## Como rodar o projeto

### Pré-requisitos
- Node.js 18+
- MongoDB (local ou Atlas)

### Backend
```bash
cd backend
npm install
# configure as variáveis de ambiente (ver .env.example, se existir)
npm run dev
```

### Frontend
```bash
cd frontend
npm install
npm run dev
```

<!-- Se houver variáveis de ambiente necessárias (ex: MONGO_URI, JWT_SECRET), documente aqui -->

## Status do projeto

Em desenvolvimento — próximos passos incluem [ex: exportação de relatórios, lógica de priorização FEFO, testes automatizados].

## Autor

Bernardo Pinheiro Guerra Ramos
[LinkedIn](https://www.linkedin.com/in/bernardopinheiroguerra/) • [GitHub](https://github.com/Bernardo085)
