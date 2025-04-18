# 🎮 GameHub API

Bem-vindo à **GameHub API** — uma RESTful API desenvolvida em **Golang** para cadastro e gerenciamento de jogos. Este projeto é parte da série de vídeos do canal [AlmusttyADev](https://www.youtube.com/@MusttyDev), voltado para quem quer aprender Go na prática, com um projeto real e moderno.

---

## 🚀 Tecnologias Utilizadas

- **[Go](https://golang.org/)** — Linguagem principal da aplicação
- **[PostgreSQL](https://www.postgresql.org/)** — Banco de dados relacional
- **[Docker](https://www.docker.com/)** — Containerização e orquestração do ambiente
- **[Ent](https://entgo.io/)** — ORM para Go com foco em performance e tipagem forte
- **[Gin](https://gin-gonic.com/)** — Framework web
- **[JWT](https://jwt.io/)** — Autenticação via token
- **[Logrus](https://github.com/sirupsen/logrus)** — Logging estruturado

---

## 📁 Estrutura do Projeto

```bash
gamehub-api/
├── cmd/                    # Ponto de entrada da aplicação (main.go)
├── internal/               # Domínio interno da aplicação
│   ├── api/                # Camada de comunicação HTTP
│   │   ├── handlers/       # Controladores das rotas (HTTP Handlers)
│   │   └── services/       # Lógica de negócio (serviços da aplicação)
│   ├── communication/      # Modelos de entrada e saída
│   │   ├── request/        # Estruturas para entrada (DTOs de request)
│   │   └── response/       # Estruturas para saída (DTOs de response)
│   └── infrastructure/     # Camada de infraestrutura
│       ├── repository/     # Integração com banco de dados via Ent
│       ├── middleware/     # Middlewares do Gin (auth, logger, etc)
│       ├── security/       # Segurança (JWT, hash de senhas, etc)
│       └── webserver/      # Inicialização do servidor e rotas
├── pkg/                    # Pacotes utilitários reutilizáveis (logger, config, etc)
├── .env                    # Variáveis de ambiente
├── docker-compose.yml      # Docker Compose para ambiente local
├── Dockerfile              # Dockerfile para build da API
└── go.mod / go.sum         # Gerenciador de dependências do Go
```

---

## ⚙️ Funcionalidades

- [x] Cadastro de jogos (nome, descrição, plataforma, etc)
- [x] Listagem, edição e remoção de jogos
- [x] Autenticação via JWT
- [x] Middleware de autenticação
- [x] Docker para ambiente isolado
- [x] Log estruturado com Logrus

---

## 🐳 Como rodar com Docker

```bash
# Subir containers com Docker Compose
docker-compose up --build
```

---

## 🔐 Autenticação

O projeto utiliza **JWT** para autenticação de usuários.

- Após login, o usuário receberá um token.
- Este token deve ser enviado no header `Authorization: Bearer <token>` para acessar rotas protegidas.

---

## 📦 Futuras Melhorias

- [ ] Documentação com Swagger
- [ ] Paginação e filtros na listagem de jogos
- [ ] Upload de imagens para os jogos
- [ ] Testes automatizados

---

## 📹 Aprenda com o Projeto

Este projeto é usado como material para o canal **[AlmusttyADev](https://www.youtube.com/@MusttyDev)** no YouTube. A ideia é ensinar **Go** na prática com um projeto real, aplicando boas práticas e tecnologias modernas.
