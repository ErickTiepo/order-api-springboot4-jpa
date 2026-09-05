# 🛒 Order API - Spring Boot

API REST desenvolvida em **Java com Spring Boot** que simula o funcionamento básico do backend de um sistema de pedidos de e-commerce.

O projeto foi desenvolvido durante meus estudos de **Java e desenvolvimento backend**, com o objetivo de praticar Programação Orientada a Objetos, desenvolvimento de APIs REST, persistência de dados e organização de aplicações em camadas.

## 💻 Sobre o projeto

A aplicação possui entidades que representam diferentes partes de um sistema de pedidos:

* Usuários
* Produtos
* Categorias
* Pedidos
* Itens de pedidos
* Pagamentos

A aplicação está organizada em camadas, separando as responsabilidades entre **Controllers, Services e Repositories**.

## 🛠️ Tecnologias utilizadas

* **Java 25**
* **Spring Boot 4.1.1**
* **Spring Data JPA**
* **Hibernate**
* **Spring Web MVC**
* **H2 Database**
* **Maven**

## 📚 Conceitos praticados

### Java

* Programação Orientada a Objetos
* Encapsulamento
* Interfaces
* Enumerações
* Collections
* Streams

### Spring Boot

* Injeção de dependências
* Controllers REST
* Services
* Repositories
* Profiles
* Configuração da aplicação

### JPA / Hibernate

* Mapeamento objeto-relacional
* Entidades
* Chaves primárias e estrangeiras
* Chaves compostas
* Relacionamentos `@OneToMany`
* Relacionamentos `@ManyToOne`
* Relacionamentos `@OneToOne`

### API REST

* Endpoints
* Requisições HTTP
* JSON
* Códigos de status HTTP
* Tratamento de exceções

## 📂 Estrutura do projeto

O código está organizado em camadas:

```text
src
└── main
    └── java
        └── com.erick.orderapi
            ├── config
            ├── entities
            ├── repositories
            ├── resources
            ├── services
            └── exceptions
```

* **`entities`** — Classes que representam as entidades do sistema.
* **`repositories`** — Interfaces responsáveis pelo acesso aos dados através do Spring Data JPA.
* **`services`** — Camada responsável pelas operações e regras da aplicação.
* **`resources`** — Controllers responsáveis pelos endpoints da API.
* **`exceptions`** — Classes utilizadas para tratamento das exceções.
* **`config`** — Configurações utilizadas pela aplicação, incluindo os dados iniciais para testes.

## 🔗 Endpoints

| Método | Endpoint           | Descrição                   |
| ------ | ------------------ | --------------------------- |
| `GET`  | `/users`           | Lista os usuários           |
| `GET`  | `/users/{id}`      | Busca um usuário pelo ID    |
| `GET`  | `/products`        | Lista os produtos           |
| `GET`  | `/products/{id}`   | Busca um produto pelo ID    |
| `GET`  | `/categories`      | Lista as categorias         |
| `GET`  | `/categories/{id}` | Busca uma categoria pelo ID |
| `GET`  | `/orders`          | Lista os pedidos            |
| `GET`  | `/orders/{id}`     | Busca um pedido pelo ID     |

## 🗄️ Banco de dados

O projeto utiliza o **H2 Database**, um banco de dados em memória que permite executar a aplicação sem a necessidade de configurar um servidor de banco de dados externo.

Para facilitar os testes, a aplicação possui uma configuração que insere dados iniciais no banco, incluindo usuários, produtos, categorias, pedidos e pagamentos.

## ▶️ Como executar

### Pré-requisitos

* **Java 25**
* Uma IDE de sua preferência, como IntelliJ IDEA ou Eclipse

O projeto possui **Maven Wrapper**, portanto não é necessário instalar o Maven separadamente.

### 1. Clone o repositório

```bash
git clone https://github.com/ErickTiepo/order-api-springboot4-jpa.git
```

### 2. Acesse a pasta da aplicação

```bash
cd order-api-springboot4-jpa/order-api
```

### 3. Execute o projeto

No Windows:

```bash
mvnw.cmd spring-boot:run
```

No Linux/macOS:

```bash
./mvnw spring-boot:run
```

Também é possível executar a classe `OrderApiApplication.java` diretamente pela IDE.

A aplicação será iniciada em:

```text
http://localhost:8080
```

## 🧪 Testando a API

Após iniciar a aplicação, os endpoints podem ser testados utilizando ferramentas como **Postman**, **Insomnia** ou o navegador para requisições `GET`.

Exemplos:

```http
GET http://localhost:8080/users
```

```http
GET http://localhost:8080/products
```

```http
GET http://localhost:8080/categories
```

```http
GET http://localhost:8080/orders
```

## 👨‍💻 Autor

**Erick Fernando Tiepo do Amaral**

Estudante de **Sistemas de Informação**, com foco nos estudos de **desenvolvimento backend com Java**.

---

⭐ Projeto desenvolvido para fins de estudo e prática de desenvolvimento backend.
