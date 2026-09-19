<div align="center">

<img src="https://capsule-render.vercel.app/api?type=venom&color=0:00ffe7,50:ff0064,100:0a0a0f&height=200&section=header&text=IAGO%20BARROS&fontSize=60&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Backend%20%C2%B7%20Go%20%C2%B7%20Java%20%C2%B7%20Compiladores&descAlignY=58&descSize=17&descAlign=50" width="100%"/>

[![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)](#)
[![Java](https://img.shields.io/badge/Java%2021-ED8B00?style=flat-square&logo=openjdk&logoColor=white)](#)
[![Spring](https://img.shields.io/badge/Spring%20Boot%203-6DB33F?style=flat-square&logo=springboot&logoColor=white)](#)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)](#)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](#)
[![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)](#)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-iagobarrosg-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/iagobarrosg)
![Fortaleza](https://img.shields.io/badge/Fortaleza,%20CE-BR-0a0a0f?style=flat-square)
![Aberto a propostas](https://img.shields.io/badge/aberto%20a%20propostas-00ffe7?style=flat-square&labelColor=0a0a0f)

</div>

---

## `// sobre`

Sou **Iago de Barros Gomes**, desenvolvedor backend em Fortaleza. Venho da operação industrial e migrei para software — o que significa que já vivi do outro lado do sistema: parada de linha, ordem de serviço, apontamento de produção, o custo real de um minuto de máquina parada. Hoje escrevo os sistemas que resolvem isso.

Gosto de problemas onde a resposta não está pronta no Stack Overflow. Por isso meus projetos principais são compiladores: escrever um lexer, um parser e um gerador de código do zero ensina mais sobre linguagens, memória e arquitetura do que qualquer curso.

Trabalho com **Go** e **Java/Spring Boot** no backend, Linux no dia a dia, e disciplina de engenharia nos projetos pessoais: ADRs para decisões, testes de verdade, CI no GitHub Actions.

---

## `// projetos`

### 🔧 [Ytsejam](https://github.com/Iagobarros211256/ytsejam) — Compilador C17 → ELF x86-64

Compilador de um subconjunto de C17 que gera **binário ELF nativo para Linux x86-64**, sem LLVM: geração de código própria, montagem via GNU Binutils.

- Lexer e parser recursivo-descendente escritos à mão, com recuperação de erros
- ~97 testes automatizados; bug de string não terminada encontrado e coberto por teste de regressão
- Decisões registradas em ADR (codegen próprio, memória em stack no MVP)
- Critério de MVP: compilar Fibonacci recursivo e `echo $?` retornar `55`

`C` · `x86-64 Assembly` · `GNU Binutils` · `ELF`

### ☕ [Golshi](https://github.com/Iagobarros211256/golshi) — Linguagem OO que compila para bytecode JVM

Linguagem orientada a objetos própria, com compilador em Java que emite **arquivos `.class` reais** via biblioteca ASM — rodam em qualquer JVM.

- Suporte a classes, herança, interfaces, polimorfismo e generics
- Despacho de métodos delegado à JVM (`invokevirtual` / `invokeinterface`)
- `COMPUTE_FRAMES` do ASM para geração de stack map frames
- Gradle + Java 21 + JUnit 5 + GitHub Actions CI

`Java 21` · `ASM` · `Gradle` · `JUnit 5`

### 🏭 [Sistema de Gestão de Manutenção (MES)](https://github.com/Iagobarros211256/projeto-mes) — Java + Spring Boot

Sistema de manutenção industrial para uma fábrica fictícia, construído como monólito modular. É o projeto onde minha bagagem de chão de fábrica aparece no domínio.

- Ordens de serviço com máquina de estados (`ABERTA → EM_ANDAMENTO → CONCLUÍDA/CANCELADA`)
- Módulo de paradas de máquina e dashboard de **OEE** (Disponibilidade × Performance × Qualidade)
- Notificações em tempo real com WebSocket/STOMP disparadas após commit da transação
- Spring Security com RBAC, migrações Flyway, Criteria API para filtros dinâmicos
- Testes de integração com **Testcontainers** contra PostgreSQL real

`Java 21` · `Spring Boot 3` · `PostgreSQL` · `Flyway` · `React` · `TypeScript`

### 🛒 [Volurya API](https://github.com/Iagobarros211256/volurya-api) — Backend de e-commerce em Go

API REST para loja de merch de banda: catálogo, pedidos e autenticação.

`Go` · `PostgreSQL` · `Docker`

---

<details>
<summary><code>// outros projetos em andamento</code></summary>

<br>

| Projeto | O que é |
|---|---|
| **Library Lending System** | Sistema de empréstimo de biblioteca em Go, com regra autoimposta de usar **só a biblioteca padrão** — `net/http` puro, `database/sql` com SQL cru, sem ORM e sem framework |
| **Counterparts** | Sistema contábil/financeiro com dashboard para a mesma fábrica fictícia do projeto MES |
| **Discipline** | Ponto eletrônico e folha de pagamento (estilo ADP) |
| **Stego** | RAG pessoal rodando local com Ollama sobre meu acervo de documentos |
| **Distro própria** | Construção de uma distribuição Linux a partir do Linux From Scratch |

</details>

---

## `// stack`

**Linguagens** — Go · Java 21 · C · TypeScript · SQL · Bash

**Backend** — Spring Boot 3 · REST · WebSocket/STOMP · JWT / Spring Security

**Dados** — PostgreSQL · MySQL · Flyway · JPA / Criteria API

**Infra & testes** — Docker · Testcontainers · JUnit 5 · GitHub Actions · Linux

---

## `// contato`

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LINKEDIN-iagobarrosg-ff0064?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0a0a0f)](https://www.linkedin.com/in/iagobarrosg)
[![Email](https://img.shields.io/badge/EMAIL-fale%20comigo-00ffe7?style=for-the-badge&logo=gmail&logoColor=black&labelColor=0a0a0f)](mailto:SEU-EMAIL@exemplo.com)

</div>

<div align="center">

<details>
<summary><code>// estatísticas</code></summary>

<br>

<img src="https://github-readme-stats.vercel.app/api?username=Iagobarros211256&show_icons=true&theme=tomorrow_night&hide_border=true&bg_color=0a0a0f&title_color=00ffe7&icon_color=ff0064&text_color=a0a0cc" />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Iagobarros211256&layout=compact&theme=tomorrow_night&hide_border=true&bg_color=0a0a0f&title_color=00ffe7&text_color=a0a0cc&langs_count=6" />

</details>

<img src="https://capsule-render.vercel.app/api?type=venom&color=0:0a0a0f,50:ff0064,100:00ffe7&height=110&section=footer" width="100%"/>

</div>
