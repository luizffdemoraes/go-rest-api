<h1 align="center">
Go: desenvolvendo uma API Rest
</h1>

### Índice

- Json, Request, Response e Go
- Roteador, recursos por ID e Docker
- Conexão com banco e exibindo os dados
- Criando, deletando e editando com Gorm
- Middleware e integração com front-end

<h2 align="center">
Json, Request, Response e Go
</h2>

* Entendemos o que é uma API;
* Realizamos uma requisição GET retornando um Json.

<h2 align="center">
Roteador, recursos por ID e Docker
</h2>

* Adicionamos o Gorilla Mux como novo roteador da nossa aplicação;
* Retornamos um único recurso através do id;
* Criamos uma imagem do banco de dados Postgres com Docker e executamos um script SQL que adicionava alguns registros em nosso banco de dados.

O pacote gorilla/mux implementa um roteador de requisições e respostas para corresponder às solicitações de entrada ao seu respectivo manipulador ou handler.

<h2 align="center">
Conexão com banco e exibindo os dados
</h2>

* Instalamos o Gorm;
* Realizamos a conexão da API com banco de dados;
* Alteramos as funções do controller para exibir as informações do banco de dados.

<h2 align="center">
Comandos Docker utilizados.:
</h2>

O comando informa ao Docker para processar o conteúdo do arquivo de composição e configurar os volumes, redes e contêineres especificados

```docker-compose up```

O comando informa ao Docker Compose para executar um shell dentro do contêiner do serviço PostgreSQL

```docker-compose exec postgres sh```

O comando é utilizado para obter o endereço IP associado ao nome do host do sistema. 

```hostname -i```

O comando é utilizado para listar os contêineres em execução no seu ambiente Docker

```docker ps```

O comando docker é utilizado para obter informações detalhadas sobre o contêiner identificado pelo ID "805b500dfa2a" e, em seguida, usa Select-String para filtrar as linhas contendo a palavra-chave "IPAddress".

```docker inspect 805b500dfa2a | Select-String "IPAddress"```

<h2 align="center">
Conexão com banco e exibindo os dados
</h2>

Instalar o gorm

```go get -u gorm.io/gorm```

Instalar o driver do postgres

```go get gorm.io/driver/postgres```

🪲 Erro.: 

```failed to initialize database, got error failed to connect to `host=localhost user=root database=root`: failed SASL auth (FATAL: autenticação do tipo password falhou para usuario "root" (SQLSTATE 28P01))```

 🔨 Correção.:

CTRL + ALT + DEL > Gerenciador de Tarefas > Serviços > postgresql-x e parando o Postgres

<h2 align="center">
Criando, deletando e editando com Gorm
</h2>

* Adicionamos um endpoint com método Post para criar uma nova personalidade e salvá-la no banco de dados;
* Adicionamos um endpoint com método Delete para deletar uma personalidade e removê-la do banco de dados;
* Adicionamos um endpoint com método Put para atualizar uma personalidade e alterá-la no banco de dados.



```go get github.com/gorilla/handlers``` 

### 🛠 Tecnologias

As seguintes ferramentas foram usadas na construção do projeto:

- [Docker](https://www.docker.com/)
- [Gorilla Mux](https://github.com/gorilla/mux)
- [Postgres](https://www.postgresql.org/)