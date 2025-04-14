# Capudo123
# 📘 Projeto: Sistema de Gerenciamento de Usuários e Postagens
Este projeto implementa um sistema simples para cadastro de usuários e postagens, utilizando um banco de dados relacional.
## 🧰 Tecnologias Utilizadas

- **Banco de Dados**: MySQL
- **Linguagem**: Node.js
- **ORM**: Sequelize
- **Outros**: Express, JWT

## 🗂️ Estrutura do Banco de Dados

### 🔸 Tabela `usuarios`

| Campo          | Tipo     | Descrição                     |
|----------------|----------|-------------------------------|
| `id`           | INT      | Chave primária                |
| `nome`         | VARCHAR  | Nome do usuário               |
| `email`        | VARCHAR  | E-mail único do usuário       |
| `senha`        | VARCHAR  | Senha criptografada           |
| `data_criacao` | DATETIME | Data de criação do cadastro   |


### 🔹 Tabela `postagens`

| Campo          | Tipo     | Descrição                                     |
|----------------|----------|-----------------------------------------------|
| `id`           | INT      | Chave primária                                |
| `usuario_id`   | INT      | Chave estrangeira, referência à tabela `usuarios` |
| `titulo`       | VARCHAR  | Título da postagem                            |
| `conteudo`     | TEXT     | Texto completo da postagem                    |
| `data_criacao` | DATETIME | Data da criação da postagem                   |

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
## 🤝 Contribuindo
1. **Faça um fork do repositório**:
   - Crie uma cópia do repositório na sua própria conta do GitHub. Isso permite que você faça alterações sem afetar o repositório original até que as alterações sejam aprovadas.
   - Para fazer um fork, clique no botão **"Fork"** no canto superior direito da página do repositório no GitHub.

2. **Crie uma branch para a sua feature**:
   - Após fazer o fork, crie uma nova branch para trabalhar em suas modificações. Isso ajuda a manter seu código organizado e facilita a colaboração.
   - Para criar uma nova branch, você pode usar o comando:
     ```bash
     git checkout -b nome-da-sua-branch
     ```

3. **Faça suas alterações e commit**:
   - Depois de fazer as modificações necessárias no código ou na documentação, salve suas alterações e crie um commit com uma mensagem descritiva.
   - Por exemplo:
     ```bash
     git commit -m "feat: adicionado novo recurso X"
     ```
   - **`feat:`** indica que você está adicionando uma nova funcionalidade (se for um bug fix, use `fix:` ou `bugfix:`).

4. **Envie suas alterações para o repositório remoto**:
   - Após o commit, você precisará enviar suas alterações para o seu repositório remoto (fork) no GitHub.
   - Para isso, use o comando:
     ```bash
     git push origin nome-da-sua-branch
     ```

5. **Abra um Pull Request (PR)**:
   - No GitHub, vá até a página do seu repositório forkado e clique na opção **"Compare & pull request"**.
   - Isso permitirá que você envie suas alterações para o repositório original.
   - Adicione uma descrição detalhada sobre o que foi modificado, o motivo das alterações e como elas melhoram o projeto.

6. **Aguarde a revisão**:
   - Depois de abrir o Pull Request, os mantenedores do projeto revisarão seu código. Se tudo estiver correto, eles irão fazer o merge da sua branch com o repositório principal.
   - Se houver feedback ou ajustes necessários, o mantenedor pode pedir alterações adicionais. Se isso acontecer, faça as alterações, commit e envie novamente para o seu fork.

---

## 🚧 Código de Conduta

Por favor, siga o nosso **Código de Conduta** ao contribuir com este projeto. Queremos garantir que todos os colaboradores tenham uma experiência positiva e respeitosa.

Se você estiver participando de discussões ou revisões de código, trate os outros com respeito e seja construtivo ao fornecer feedback.

---

## 💡 Sugestões e Bugs

Se você encontrar um bug ou tiver uma sugestão de melhoria para o projeto, por favor, abra um **issue** no repositório com a descrição detalhada.

- Para abrir um novo **issue**: Clique na aba **"Issues"** no GitHub e depois em **"New issue"**. Descreva o problema ou a melhoria que deseja sugerir.

## 🧾 Licença

Distribuído sob a licença MIT. Veja `LICENSE` para mais informações.

## 🔗 Sobre o README

Este README foi estruturado com auxílio do [readme.so](https://readme.so), uma ferramenta visual para criação de documentações em Markdown.
