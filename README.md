# api-spring — Lista de Tarefas 01 (Spring Boot + Thymeleaf + H2)

## Como executar
- Windows: `.\mvnw.cmd spring-boot:run`
- Linux/macOS: `./mvnw spring-boot:run`

(Se a pasta nao tiver o `mvnw`, gere o projeto no start.spring.io ou use `mvn spring-boot:run`.)

## Enderecos
- Interface web:  http://localhost:8080/tarefas
- API REST:       http://localhost:8080/api/tarefas
- Console H2:     http://localhost:8080/h2-console  (JDBC URL: jdbc:h2:mem:testdb, user: sa, senha vazia)

## Teste da API (YARC ou curl)
curl -i http://localhost:8080/api/tarefas
curl -i -X POST http://localhost:8080/api/tarefas -H "Content-Type: application/json" -d '{"descricao":"Estudar Spring Boot","concluida":false}'
curl -i -X PUT http://localhost:8080/api/tarefas/1 -H "Content-Type: application/json" -d '{"descricao":"Estudar Spring Boot (Finalizado)","concluida":true}'
curl -i -X DELETE http://localhost:8080/api/tarefas/1
