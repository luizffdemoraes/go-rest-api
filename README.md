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

### 🛠 Tecnologias

As seguintes ferramentas foram usadas na construção do projeto:

- [Docker](https://www.docker.com/)
- [Gorilla Mux](https://github.com/gorilla/mux)
- [Postgres](https://www.postgresql.org/)