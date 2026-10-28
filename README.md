<div align="center">

<img src="https://capsule-render.vercel.app/api?type=venom&color=0:00ffe7,50:ff0064,100:0a0a0f&height=190&section=header&text=IAGO%20BARROS&fontSize=58&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Backend%20%7C%20Go%20%7C%20PHP%2FLaravel%20%7C%20Linux&descAlignY=59&descSize=16" width="100%" alt="Iago Barros — Backend, Go, PHP/Laravel, Linux" />

**Desenvolvedor backend · Fortaleza, CE**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/iagobarrosg)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=flat-square&logo=laravel&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

</div>

---

## `// sobre`

Sou **Iago de Barros Gomes**, desenvolvedor com foco em **backend e sistemas de gestão**.

Passei mais de uma década no chão de fábrica, operando linhas de embalagem e robôs paletizadores. É de lá que vem o jeito como penso software: processo real, dado consistente, rastreabilidade e o custo de uma parada.

Hoje desenvolvo e mantenho sistemas corporativos em **PHP/Laravel/Filament + PostgreSQL**, colaboro em produto **React + Supabase** e construo projetos próprios em **Go, Java e C** — de APIs em produção a um compilador escrito do zero.

---

## `// experiência`

### 🏢 Ynnovar Facilities — Estágio em TI · set/2026 – atual

Único desenvolvedor da empresa: cuido do código, do deploy e da manutenção dos sistemas internos.

**Sistema de gestão financeira e operacional**
- Módulos de **lançamentos financeiros, contratos, centros de custo, orçamentos e provisionamentos**.
- Modelagem de **colaboradores, escalas, equipes e ocorrências**, com regras de acesso por perfil.
- **Testes automatizados, análise estática e verificações de segurança** no pipeline de CI.
- Integridade financeira, trilha de auditoria, backups, migrações e procedimentos de deploy.

**Site institucional**
- Manutenção e evolução em produção (VPS Linux): atualização de dependências, segurança de formulários, fluxo de deploy.

`PHP` · `Laravel` · `Filament` · `PostgreSQL` · `GitHub Actions` · `Linux`

> Código privado — descrição em nível de responsabilidade, sem expor código ou dados internos.

### 🤝 DataHosp (KeyCore) — Colaborador

Produto web **multi-tenant** de gestão de hospedagem.

- Mapeamento do caminho **interface → serviços → banco**, incluindo políticas RLS e RPCs em PL/pgSQL.
- Documentação técnica de **seis fluxos** da aplicação (autenticação, hospedagem, pedidos, catálogo, relatórios) — **PR #22**, incorporado em out/2026.
- Fluxo de time: issues, branches dedicadas, code review e pull requests.

`React` · `TypeScript` · `Vite` · `Supabase` · `PostgreSQL` · `RLS`

---

## `// projetos em destaque`

### 🏭 [Projeto MES](https://github.com/Iagobarros211256/projeto-mes) — Manutenção e produção industrial
Backend para uma fábrica de biscoitos fictícia, modelado a partir do que vivi na operação: **paradas de máquina, ordens de serviço** (máquina de estados), **manutenção preventiva, estoque de peças, apontamento de produção e dashboard**.
- Monólito modular, **RBAC com 5 perfis** (Spring Security), 8 migrations **Flyway**
- Notificações em tempo real via **WebSocket/STOMP** disparadas só após o commit da transação
- Testes unitários e de integração com **Testcontainers** (Postgres real)

`Java 21` · `Spring Boot 3` · `PostgreSQL` · `Flyway` · `Testcontainers` · `Docker`

### 🛒 [Volurya](https://github.com/Iagobarros211256/volurya) — API de e-commerce em Go · [em produção](https://volurya.onrender.com)
API para produtos, pedidos e clientes de uma banda.
- **JWT** com bcrypt, cookies HttpOnly e rotação de refresh token
- Pagamentos com **Stripe**, e-mails transacionais, testes contra **PostgreSQL** real
- Clean Architecture simplificada, **Docker**, CI no **GitHub Actions** e deploy no Render

`Go` · `Gin` · `PostgreSQL` · `Stripe` · `Docker` · `GitHub Actions`

### 🛡️ [wp-threat-kit](https://github.com/Iagobarros211256/wp-threat-kit) — Detecção de backdoor em WordPress
Kit defensivo nascido da análise de um site comprometido real.
- **wphunter**: scanner de IOC em Go, só leitura, com saída JSON para CI
- Regras **YARA** validadas e um **lab Docker isolado** (rede sem saída) com demonstrador benigno
- Write-up das técnicas de evasão e lições aplicadas a Laravel, Go e Supabase

`Go` · `YARA` · `Docker` · `Segurança defensiva`

### 🔎 [Stego](https://github.com/Iagobarros211256/stego) — Base de conhecimento pessoal com IA local
RAG 100% offline sobre documentos locais, rodando numa RX 580 via Vulkan.
- Busca híbrida: **vetorial + BM25 (FTS5)** fundidas por Reciprocal Rank Fusion
- Respostas com citação do trecho de origem — e recusa quando não encontra
- Integrado a um [desktop pet](https://github.com/Iagobarros211256/linux-desktop-gremlin) (fork com monitor de sistema e atalho no KDE) em PySide6

`Python` · `SQLite` · `sqlite-vec` · `Ollama` · `PySide6`

### ⚙️ [Ytsejam](https://github.com/Iagobarros211256/ytsejam) — Linguagem de programação compilada, escrita em C
Linguagem própria, inspirada na simplicidade de Go, com compilador nativo para Linux x86-64 — sem LLVM.
- **Lexer e parser** (descida recursiva, AST completa, recuperação de erro) com suíte de testes
- Em andamento: análise semântica e geração de assembly x86-64 via GNU Binutils

`C17` · `x86-64` · `ELF` · `GNU Binutils`

---

## `// stack`

| Área | Tecnologias e práticas |
|---|---|
| **Backend** | Go, PHP/Laravel/Filament, Java/Spring Boot, Python, APIs REST |
| **Frontend** | React, TypeScript, Tailwind CSS |
| **Dados** | PostgreSQL, Supabase (RLS, RPC), SQLite, Flyway |
| **Qualidade** | Testes unitários e de integração, Testcontainers, análise estática, code review |
| **Infra** | Linux, Docker, GitHub Actions, Render, VPS, Bash |
| **Estudando** | Sistemas distribuídos, cloud, compiladores, sistemas operacionais |

---

## `// contato`

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LINKEDIN-iagobarrosg-ff0064?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0a0a0f)](https://www.linkedin.com/in/iagobarrosg)

<sub>Software para problemas reais, com atenção à engenharia por trás de cada entrega.</sub>

</div>
