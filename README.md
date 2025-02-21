# Cardápio API

Este projeto é uma API REST para gerenciamento de um cardápio, desenvolvida com **Spring Boot**, **Java**, **Lombok** e **Oracle Database**.

## Tecnologias Utilizadas

- **Java 17**
- **Spring Boot**
- **Spring Data JPA**
- **Lombok**
- **Oracle Database**
- **HikariCP** (Gerenciador de conexão com o banco)

## Configuração do Banco de Dados

A API utiliza um banco de dados Oracle. Para configurar a conexão, edite o arquivo `application.properties`:

```properties
spring.datasource.url=jdbc:oracle:thin:@localhost:1521/XEPDB1
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.datasource.driver-class-name=oracle.jdbc.OracleDriver
spring.jpa.hibernate.ddl-auto=update
```

## Endpoints da API

### Buscar todos os alimentos

```http
GET /food
```

Retorna uma lista com todos os alimentos cadastrados.

#### Exemplo de Resposta

```json
[
  {
    "id": 1,
    "title": "Pizza Margherita",
    "image": "https://example.com/pizza.jpg",
    "price": 29.99
  }
]
```

### Adicionar um novo alimento

```http
POST /food
```

Envia um JSON no corpo da requisição para adicionar um novo alimento.

#### Exemplo de Corpo da Requisição

```json
{
  "title": "Hamburguer",
  "image": "https://example.com/hamburguer.jpg",
  "price": 19.99
}
```

## Como Executar o Projeto

1. Clone o repositório:

   ```sh
   git clone https://github.com/diegoestefan/menu.git
   ```

2. Acesse a pasta do projeto:

   ```sh
   cd cardapio-api
   ```

3. Configure o banco de dados no `application.properties`.

4. Execute o projeto:

   ```sh
   mvn spring-boot:run
   ```

5. A API estará disponível em `http://localhost:8080/food`.


