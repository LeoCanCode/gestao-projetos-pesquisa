> Projeto: MVP - Sistema de Gestão de Projetos de Pesquisa
> Repositório: research-group-manager
> Sprint: Sprint 1
> Equipe: Leonardo, Bruno, Helena

---

## Sobre o Projeto

MVP de aplicação web para gerenciamento de projetos de pesquisa,
permitindo que o chefe do grupo cadastre projetos, atribua atividades
aos membros e visualize o andamento de cada projeto e tarefa.

---

## Tecnologias Utilizadas

- **Backend:** Node.js + Express
- **Frontend:** HTML, CSS e JavaScript
- **Banco de Dados:** PostgreSQL
- **Gerenciador de Pacotes:** npm

---

## Pre-requisitos

Antes de iniciar, certifique-se de ter instalado em sua maquina:

- Node.js v20+
- npm v9+
- PostgreSQL v15+

Para verificar se ja possui as ferramentas instaladas, execute:

    node -v
    npm -v
    psql --version

---

## Instalacao

### 1. Clone o repositorio

    git clone https://github.com/seu-usuario/research-group-manager.git
    cd research-group-manager

### 2. Instale as dependencias

    npm install

### 3. Configure o banco de dados

Acesse o PostgreSQL e crie o banco de dados:

    CREATE DATABASE research_group_manager;

Em seguida, execute o script de criacao das tabelas:

    psql -U postgres -d research_group_manager -f database/schema.sql

O arquivo schema.sql ira criar as seguintes tabelas:

- projetos — armazena os projetos de pesquisa cadastrados
- atividades — armazena as atividades vinculadas a cada projeto
- membros — armazena os membros do grupo de pesquisa
- atividade_membro — tabela associativa entre atividades e membros (N:M)

### 4. Configure as variaveis de ambiente

Crie um arquivo .env na raiz do projeto com base no arquivo
de exemplo .env.example:

    cp .env.example .env

Edite o arquivo .env com as suas configuracoes:

    # Servidor
    PORT=3000

    # Banco de Dados
    DB_HOST=localhost
    DB_PORT=5432
    DB_NAME=research_group_manager
    DB_USER=postgres
    DB_PASSWORD=sua_senha_aqui

### 5. Inicie a aplicacao

    npm start

A aplicacao estara disponivel em:

    http://localhost:3000

---

## Uso

### Paginas disponiveis

| Rota                          | Descricao                                    |
|-------------------------------|----------------------------------------------|
| GET /                         | Pagina inicial — listagem de projetos        |
| GET /projetos/novo            | Formulario de cadastro de novo projeto       |
| GET /projetos/:id             | Detalhes de um projeto e suas atividades     |
| GET /atividades/nova          | Formulario de cadastro de nova atividade     |
| POST /projetos                | Endpoint para salvar um novo projeto         |
| POST /atividades              | Endpoint para salvar uma nova atividade      |
| POST /atividades/:id/status   | Endpoint para atualizar o status de atividade|

---

### Funcionalidades

#### Cadastrar um Projeto

1. Acesse http://localhost:3000/projetos/novo
2. Preencha os campos obrigatorios:
   - **Titulo** — nome do projeto de pesquisa
   - **Descricao** — breve descricao do projeto
   - **Data de Inicio** — data de inicio do projeto (formato DD/MM/AAAA)
   - **Status** — status atual do projeto (Ativo, Pausado ou Concluido)
3. Clique em Cadastrar Projeto
4. Voce sera redirecionado para a listagem de projetos

---

#### Listar Projetos

1. Acesse http://localhost:3000 ou http://localhost:3000/projetos
2. Todos os projetos cadastrados serao exibidos com:
   - Titulo
   - Status atual
   - Data de inicio
3. Clique em um projeto para visualizar seus detalhes e atividades

---

#### Cadastrar uma Atividade

1. Acesse a pagina de detalhes de um projeto
2. Clique em Nova Atividade
3. Preencha os campos obrigatorios:
   - **Titulo** — nome da atividade
   - **Descricao** — descricao da tarefa
   - **Responsavel** — membro do grupo atribuido a atividade
   - **Status** — status inicial (A fazer, Em andamento ou Concluida)
4. Clique em Cadastrar Atividade

---

#### Atualizar Status de uma Atividade

1. Na pagina de detalhes do projeto, localize a atividade desejada
2. Clique em Alterar Status
3. Selecione o novo status:
   - A fazer → Em andamento
   - Em andamento → Concluida
4. Confirme a alteracao

> Atencao: a transicao de status segue uma ordem linear
> e nao pode ser revertida.

---

## Estrutura do Projeto

    research-group-manager/
    │
    ├── database/
    │   └── schema.sql              # Script de criacao das tabelas
    │
    ├── public/
    │   ├── css/
    │   │   └── style.css           # Estilos da aplicacao
    │   └── js/
    │       └── main.js             # Scripts do frontend
    │
    ├── src/
    │   ├── controllers/
    │   │   ├── projetoController.js
    │   │   └── atividadeController.js
    │   ├── models/
    │   │   ├── Projeto.js
    │   │   └── Atividade.js
    │   ├── routes/
    │   │   ├── projetos.js
    │   │   └── atividades.js
    │   └── app.js                  # Configuracao principal do Express
    │
    ├── views/
    │   ├── projetos/
    │   │   ├── index.html          # Listagem de projetos
    │   │   ├── novo.html           # Formulario de cadastro
    │   │   └── detalhes.html       # Detalhes do projeto
    │   └── atividades/
    │       └── nova.html           # Formulario de cadastro de atividade
    │
    ├── .env.example                # Exemplo de configuracao de ambiente
    ├── .gitignore
    ├── package.json
    ├── SPRINT_BACKLOG.md
    ├── DAILY_LOGS.md
    └── RETROSPECTIVE.md

---

## Equipe

| Membro   | Papel                        |
|----------|------------------------------|
| Leonardo | Scrum Master / Product Owner |
| Bruno    | Developer                    |
| Helena   | QA (Quality Assurance)       |

---

## Licenca

> Este projeto foi desenvolvido para fins academicos como parte
> da disciplina de Engenharia de Software.

---

*Documento elaborado por: Helena (QA)*
*Ultima atualizacao: Dia 6 da Sprint*
