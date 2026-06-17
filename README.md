# Desafio TDD Event City

Projeto desenvolvido como desafio do curso **Java Spring Expert** da [DevSuperior](https://devsuperior.com.br), aplicando o desenvolvimento orientado a testes (TDD) para implementar as funcionalidades a partir dos testes de integração já existentes.

## Sobre o projeto

Sistema de eventos e cidades com relação N-1. A implementação foi feita de forma que todos os testes de integração (`CityControllerIT` e `EventControllerIT`) passem.

## Modelo de domínio

- **City** → id, name
- **Event** → id, name, date, url, city (N-1)

## Endpoints

| Método | Rota | Status | Descrição |
|---|---|---|---|
| GET | `/cities` | 200 | Lista cidades ordenadas por nome |
| POST | `/cities` | 201 | Insere nova cidade |
| DELETE | `/cities/{id}` | 204 | Deleta cidade existente |
| DELETE | `/cities/{id}` | 404 | Cidade não encontrada |
| DELETE | `/cities/{id}` | 400 | Cidade com eventos vinculados (integridade) |
| PUT | `/events/{id}` | 200 | Atualiza evento existente |
| PUT | `/events/{id}` | 404 | Evento não encontrado |

## Tecnologias utilizadas

- Java
- Spring Boot 3
- Spring Data JPA
- H2 Database
- JUnit 5 (testes de integração)
- Maven

## Como executar os testes

```bash
git clone https://github.com/pedrotrevisan/desafio-tdd-event-city.git
cd desafio-tdd-event-city
./mvnw test
```

## Como executar a aplicação

```bash
./mvnw spring-boot:run
```

## Autor

**Pedro Henrique Trevisan**

[![GitHub](https://img.shields.io/badge/GitHub-pedrotrevisan-black)](https://github.com/pedrotrevisan)
