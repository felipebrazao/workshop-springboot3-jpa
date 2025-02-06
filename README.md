# Workshop Spring Boot 3 + JPA

## Descrição
Este projeto é um workshop prático de **Spring Boot 3** com **JPA (Java Persistence API)**, demonstrando a criação de uma API REST com persistência em banco de dados. O projeto cobre conceitos essenciais como mapeamento de entidades, operações CRUD e integração com um banco de dados relacional.

## Tecnologias Utilizadas

- Java 17+
- Spring Boot 3
- Spring Data JPA
- H2 Database / PostgreSQL / MySQL
- Maven
- Spring Web

## Instalação e Configuração

### Pré-requisitos

Antes de rodar o projeto, certifique-se de ter instalado:

- Java 17+
- Maven
- PostgreSQL ou MySQL (caso deseje usar um banco externo)

### Clonar o repositório

```bash
git clone https://github.com/felipebrazao/workshop-springboot3-jpa.git
cd workshop-springboot3-jpa
```

### Configurar o banco de dados

Se estiver usando um banco relacional, edite o **application.properties**:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/seu_banco
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
```

Para usar o H2 Database:

```properties
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
```

### Executar o projeto

```bash
mvn spring-boot:run
```

A API estará disponível em:

```
http://localhost:8080
```

## Endpoints da API

| Método  | Endpoint       | Descrição                |
|---------|--------------|--------------------------|
| **GET** | `/users`      | Lista todos os usuários  |
| **GET** | `/users/{id}` | Busca um usuário por ID  |
| **POST** | `/users`     | Cria um novo usuário     |
| **PUT**  | `/users/{id}` | Atualiza um usuário      |
| **DELETE** | `/users/{id}` | Remove um usuário     |

## Funcionalidades Implementadas

- CRUD de usuários
- Persistência de dados com Spring Data JPA
- Configuração do ambiente com Spring Boot 3

## Melhorias Futuras

- Implementação de autenticação com Spring Security + JWT
- Documentação da API com Swagger
- Testes unitários com JUnit 5 e Mockito
  
## Licença
  Este projeto está licenciado sob a Licença MIT.



