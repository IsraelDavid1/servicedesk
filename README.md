# 🎫 ServiceDesk

> Sistema de gerenciamento de chamados técnicos com autenticação, controle de usuários, dashboard interativo e implantação em containers Docker.

---

## 💻 Sobre o Projeto

O **ServiceDesk** é uma aplicação web desenvolvida para gerenciamento de chamados técnicos, permitindo que usuários registrem solicitações de suporte e que técnicos realizem o acompanhamento e resolução dos atendimentos.

O projeto foi desenvolvido com foco em boas práticas de desenvolvimento moderno, utilizando arquitetura cliente-servidor, containers Docker, integração contínua (CI/CD) e conceitos de DevOps e DevSecOps.

Além da gestão de chamados, o sistema possui autenticação de usuários, dashboard de indicadores, persistência de dados em PostgreSQL e implantação simplificada através de Docker Compose.

---

## 🚀 Tecnologias

### Backend

* Java 21
* Spring Boot
* Spring Security
* JWT Authentication
* Maven

### Frontend

* React
* TypeScript
* Vite
* CSS Modules

### Banco de Dados

* PostgreSQL

### DevOps

* Docker
* Docker Compose
* GitHub Actions

### Segurança

* JWT
* Hash de Senhas
* Controle de Acesso por Perfis

---

## 📦 Como baixar e executar o projeto

### Pré-requisitos

Certifique-se de possuir instalado:

* Git
* Docker
* Docker Compose

---

### 1. Clonar o repositório

```bash
git clone https://github.com/IsraelDavid1/chamados-api.git

cd chamados-api
```

### 2. Configurar variáveis de ambiente

Crie os arquivos:

```bash
.env
```

Configure as variáveis necessárias para:

```env
DB_HOST=postgres
DB_PORT=5432
DB_NAME=servicedesk
DB_USER=postgres
DB_PASSWORD=postgres

JWT_SECRET=sua_chave_secreta
```

### 3. Executar com Docker Compose

```bash
docker compose up -d --build
```

### 4. Verificar containers

```bash
docker ps
```

Containers esperados:

```text
chamados-frontend
chamados-backend
chamados-postgres
```

### 5. Acessar a aplicação

Frontend:

```text
http://localhost
```

Backend:

```text
http://localhost:8080
```

---

## 🛠️ Funcionalidades

### Usuário

* Criar chamados
* Consultar chamados
* Visualizar histórico
* Acompanhar status

### Técnico

* Visualizar chamados
* Atualizar chamados
* Finalizar atendimentos
* Registrar observações técnicas

### Administrador

* Gerenciar usuários
* Editar chamados
* Excluir chamados
* Gerar relatórios

### Dashboard

* Total de chamados
* Chamados em aberto
* Chamados finalizados
* Histórico recente

### Segurança

* Login com autenticação JWT
* Controle de acesso por perfil
* Proteção de rotas
* Criptografia de senhas

---

## 🔄 Pipeline CI/CD

O projeto utiliza **GitHub Actions** para automação do processo de integração contínua.

Etapas do pipeline:

* Build automático
* Validação do código
* Criação da imagem Docker
* Testes automatizados
* Publicação das imagens
* Preparação para deploy

Estrutura:

```text
.github/
└── workflows/
    └── docker-image.yml
```

---

## 📁 Estrutura do Projeto

```text
servicedesk/
│
├── frontend/
│   ├── src/
│   ├── public/
│   └── Dockerfile
│
├── backend/
│   ├── src/
│   ├── pom.xml
│   └── Dockerfile
│
├── docker-compose.yml
│
└── .github/
    └── workflows/
```

---

## 🤝 Como Contribuir

Contribuições são bem-vindas.

1. Faça um Fork do projeto

2. Crie uma branch para sua funcionalidade

```bash
git checkout -b feature/minha-feature
```

3. Faça suas alterações

4. Commit suas mudanças

```bash
git commit -m "feat: nova funcionalidade"
```

5. Envie para seu fork

```bash
git push origin feature/minha-feature
```

6. Abra um Pull Request

---

## 📝 Licença

Este projeto está licenciado sob a licença **MIT**.

Consulte o arquivo:

```text
LICENSE
```

para mais informações.

---

## 👤 Autor

### Israel David

GitHub:

https://github.com/IsraelDavid1

---

⭐ Se este projeto foi útil para você, considere deixar uma estrela no repositório.
