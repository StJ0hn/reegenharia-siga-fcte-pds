# SIGA-FCTE — Sistema Acadêmico (Reengenharia)
> Status: Finalizado
## Contexto

Este projeto nasceu como desafio acadêmico na disciplina de PDS (Projeto Detalhado de Software) na UFC — Campus Russas. Em vez de partir do zero, o objetivo foi pegar um sistema legado (originalmente desenvolvido pelo Pedro Arthur, da UnB, com persistência em arquivos `.txt`) e conduzir uma reengenharia completa: migração para banco de dados relacional, nova arquitetura em camadas, e tratamento robusto de erros e segurança.

## Minha Contribuição (John Miguel — Scrum Master & Backend Developer)

- Atuação como Scrum Master, coordenando o time em sprints ágeis
- Camada de serviço: `AlunoService`, `DisciplinaService`, `TurmaService`, `AvaliacaoService`
- Lógica de matrícula com regras de negócio (validações, bloqueios de duplicidade)
- Padrão Observer (`observer/`) para alertas de ausência
- Tratamento centralizado de exceções (`exceptions/`), incluindo `AlunoNaoEncontradoException`, `MatriculaDuplicadaException`, `TurmaLotadaException`
- Apresentação técnica sobre o padrão Factory Method, usando `AlunoFactory.java` como estudo de caso

## Stack

Java 21 · Spring Boot · Spring Data JPA · PostgreSQL · Maven

## Como rodar (Backend)

```bash
mvn clean install
mvn spring-boot:run
```

Configuração do banco em `src/main/resources/application.properties`.

## Como rodar (Front-end)

O front-end (React + TypeScript + Vite):

```bash
npm install
npm run dev
```

## Equipe (Scrum — UFC Russas)

- **Product Owner:** Paulo João
- **Scrum Master:** John Miguel
- **Developers:** Enzo Andrade, Paulo João, John Miguel, Lucas de Souza
