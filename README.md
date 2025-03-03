# Service Registry - Microservices

Este repositório armazena um **Service Registry** utilizado para registrar e monitorar as instâncias de microservices em um ambiente distribuído. No momento, o Service Registry está monitorando dois microservices:

- **ead-authuser**: Responsável pela gestão de autenticação e usuários.
- **ead-course**: Responsável pela gestão de cursos na plataforma EAD.

## Tecnologias Utilizadas

- **Spring Cloud Netflix Eureka**: Implementação do Service Discovery para registro e descoberta de serviços.
- **Java 17**: Linguagem de programação utilizada para desenvolvimento.
- **Spring Boot**: Framework para construção do microservice.

### Clonando o Repositório
```bash
git clone https://github.com/Igorgcf/EAD-Service-Registry.git
```

### Configuração do Eureka Server
Certifique-se de que o arquivo `application.yml` ou `application.properties` está corretamente configurado para atuar como um **Eureka Server**.

Exemplo de configuração em `application.yml`:
```yaml
server:
  port: 8761

Spring:
  application:
    name: ead-service-registry
  output:
    ansi:
      enabled: Always

eureka:
  client:
    registerWithEureka: false
    fetchRegistry: false
```

### Acessando o Painel do Eureka

Após iniciar a aplicação, acesse o painel do Eureka para visualizar os microservices registrados:

```
http://localhost:8761
```

## Microservices Registrados
Atualmente, os seguintes microservices estão configurados para registrar-se no Service Registry:

- **ead-authuser**: `http://localhost:8087`
- **ead-course**: `http://localhost:8082`

## Technologies Used

- Java version 17
- Spring Boot
- Spring Cloud Netflix Eureka
- Maven
- IntelliJ IDEA

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request to the repository.

When contributing to this project, please follow the existing code style, [commit conventions](https://www.conventionalcommits.org/en/v1.0.0/), and submit your changes in a separate branch.

Contribuições são bem-vindas! Se você encontrar algum problema ou tiver sugestões de melhorias, abra um problema ou envie uma solicitação pull ao repositório.

Ao contribuir para este projeto, siga o estilo de código existente, [convenções de commit](https://medium.com/linkapi-solutions/conventional-commits-pattern-3778d1a1e657), e envie suas alterações em uma branch separada.
