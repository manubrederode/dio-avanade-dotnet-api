# DIO - Trilha .NET - API e Entity Framework
www.dio.me

## Desafio de projeto
Para este desafio, foi preciso usar os conhecimentos adquiridos no módulo de API e Entity Framework, da trilha .NET da DIO.

## Contexto
Construir um sistema gerenciador de tarefas, onde podemos cadastrar uma lista de tarefas que permitirá organizar melhor a rotina.

Essa lista de tarefas precisa ter um CRUD, ou seja, deverá permitir obter os registros, criar, salvar e deletar esses registros.

A aplicação deverá ser do tipo Web API ou MVC.

A classe principal, a classe de tarefa, deve ser a seguinte:

![Diagrama da classe Tarefa](diagrama.png)

Gerar a migration para atualização no banco de dados.

## Métodos esperados
É esperado que se crie os métodos conforme a seguir:

**Swagger**

![Métodos Swagger](swagger.png)


**Endpoints**


| Verbo  | Endpoint                | Parâmetro | Body          |
|--------|-------------------------|-----------|---------------|
| GET    | /Tarefa/{id}            | id        | N/A           |
| PUT    | /Tarefa/{id}            | id        | Schema Tarefa |
| DELETE | /Tarefa/{id}            | id        | N/A           |
| GET    | /Tarefa/ObterTodos      | N/A       | N/A           |
| GET    | /Tarefa/ObterPorTitulo  | titulo    | N/A           |
| GET    | /Tarefa/ObterPorData    | data      | N/A           |
| GET    | /Tarefa/ObterPorStatus  | status    | N/A           |
| POST   | /Tarefa                 | N/A       | Schema Tarefa |

Esse é o schema (model) de Tarefa, utilizado para passar para os métodos que exigirem

```json
{
  "id": 0,
  "titulo": "string",
  "descricao": "string",
  "data": "2022-06-08T01:31:07.056Z",
  "status": "Pendente"
}
```