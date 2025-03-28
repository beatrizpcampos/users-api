# users-api

## Descrição
Este projeto é uma API de gerenciamento de usuários desenvolvida em Java, utilizando Spring Boot e outras tecnologias para criação de um serviço robusto de cadastro e autenticação.

## Tecnologias Utilizadas
- Java
- Spring Boot
- Spring Security
- JPA/Hibernate
- Banco de Dados H2
- Maven

## Funcionalidades
- Cadastro de usuários
- Autenticação e autorização
- Metodos http Create e Read
- Validação de dados
- Tratamento de exceções

## Pré-requisitos
- JDK 
- Maven
- IDE de desenvolvimento IntelliJ

## Configuração do Projeto
1. Clone o repositório
```bash
git clone https://github.com/beatrizpcampos/users-api.git
```

2. Instale as dependências
```bash
# mvn clean install
```

3. Configure o banco de dados H2

- Adicione no seu pom.xml:
<dependency>
    <groupId>com.h2database</groupId>
    <artifactId>h2</artifactId>
    <scope>runtime</scope>
</dependency>

- Configuração do application.properties
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=password

- Habilitar console H2
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console

- Configurações JPA
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.jpa.hibernate.ddl-auto=update
Acessando o Console H2

- URL do Console: http://localhost:8080/h2-console
JDBC URL: jdbc:h2:mem:testdb
Username: sa
Password: password

## Como Executar
```bash
# mvn spring-boot:run
```

## Endpoints
- `POST /login`: Efetua o login caso o usuario ja esteja cadastrado
- `POST /register`: Criar novo usuário
- `GET /user`: Permite que se o usuario estiver logado consiga acessar a pagina inicial
  
## Contribuição
1. Faça um fork do projeto
2. Crie uma branch para sua feature
3. Commit suas alterações
4. Push para sua branch
5. Abra um Pull Request
