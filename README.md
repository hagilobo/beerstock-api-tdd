# 🍺 Beer Stock REST API (TDD)

Projeto desenvolvido como parte do programa **Expert Class da Digital Innovation One (DIO)**, focado na aplicação prática do **Test-Driven Development (TDD)** e no desenvolvimento de testes unitários e de integração para APIs REST em Java.

Este projeto representa a **solução completa** do desafio de gerenciar um estoque de cervejas (Beer Stock), comprovada por uma suíte de 30 testes.

## ✨ Destaques e Funcionalidades

O desenvolvimento seguiu rigorosamente o ciclo **Vermelho-Verde-Refatorar** do TDD, garantindo a robustez das regras de negócio.

* **API RESTful:** Endpoints para gerenciamento completo do recurso `Beer`.
* **CRUD Básico:** Implementação das operações de **Criação**, **Listagem**, **Busca por Nome** e **Exclusão** de cervejas.
* **Gestão de Estoque (TDD):** Implementação das operações **`PATCH`** para:
    * **Incremento de Estoque:** Valida o estoque máximo da cerveja (`BeerStockExceededException`).
    * **Decremento de Estoque:** Garante que o estoque não se torne negativo, lançando exceção se a quantidade for insuficiente.
* **Tratamento de Exceções:** Validação de erros de negócio, como cerveja já registrada, estoque excedido e cerveja não encontrada.

## 🛠️ Tecnologias e Testes

| Categoria | Tecnologia | Uso |
| :--- | :--- | :--- |
| **Linguagem** | Java 14+ | Linguagem principal de desenvolvimento. |
| **Framework** | Spring Boot | Facilita a criação de APIs REST. |
| **Persistência** | Spring Data JPA / H2 | Banco de dados em memória para testes e desenvolvimento. |
| **Testes Unitários** | **JUnit 5 & Mockito** | Testes de unidade e mocks para a camada de Serviço (`BeerService`). |
| **Testes de Integração** | **MockMvc** | Simulação de chamadas HTTP para validar a camada Controller. |

## 🚀 Como Executar e Validar

### 1. Testar o Projeto (Comprovação)

Para executar a suíte completa de **30 testes** (unitários e de integração) e comprovar a funcionalidade do código, utilize o comando:

```bash
mvn clean test
