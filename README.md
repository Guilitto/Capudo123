# Capudo123# 📘 Projeto: Sistema de Gerenciamento de Usuários e Postagens

Este projeto implementa um sistema simples para cadastro de usuários e postagens, utilizando um banco de dados relacional.

---

## 🧰 Tecnologias Utilizadas

- **Banco de Dados**: MySQL
- **Linguagem**: Node.js
- **ORM**: Sequelize
- **Outros**: Express, JWT

---

## 🗂️ Estrutura do Banco de Dados

### 🔸 Tabela `usuarios`

| Campo          | Tipo     | Descrição                     |
|----------------|----------|-------------------------------|
| `id`           | INT      | Chave primária                |
| `nome`         | VARCHAR  | Nome do usuário               |
| `email`        | VARCHAR  | E-mail único do usuário       |
| `senha`        | VARCHAR  | Senha criptografada           |
| `data_criacao` | DATETIME | Data de criação do cadastro   |

---

### 🔹 Tabela `postagens`

| Campo          | Tipo     | Descrição                                     |
|----------------|----------|-----------------------------------------------|
| `id`           | INT      | Chave primária                                |
| `usuario_id`   | INT      | Chave estrangeira, referência à tabela `usuarios` |
| `titulo`       | VARCHAR  | Título da postagem                            |
| `conteudo`     | TEXT     | Texto completo da postagem                    |
| `data_criacao` | DATETIME | Data da criação da postagem                   |

---

## ⚙️ Como Executar o Projeto

```bash
# Clone o repositório
git clone https://github.com/Guilitto/app_2a.git

# Entre na pasta do projeto
cd app_2a

# Instale as dependências
npm install

# Configure o banco de dados (MySQL) no arquivo .env ou config.js

# Execute as migrações do banco
npx sequelize-cli db:migrate

# Inicie o servidor
npm start
