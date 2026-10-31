<div align="center">

<a href="https://www.utkudemirtas.tech">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&pause=1000&color=58A6FF&center=true&vCenter=true&width=600&lines=Hi+there%2C+I'm+Utku+%F0%9F%91%8B;Fullstack+Dev+%C2%B7+Backend+%26+DevOps;Real-time+%C2%B7+Distributed+%C2%B7+CI%2FCD" alt="Typing SVG" />
</a>

<p>
  <a href="https://www.utkudemirtas.tech"><img src="https://img.shields.io/badge/Portfolio-utkudemirtas.tech-58A6FF?style=for-the-badge&logo=vercel&logoColor=white" /></a>
  <a href="https://linkedin.com/in/utkudemirtas"><img src="https://img.shields.io/badge/LinkedIn-Utku_Demirta%C5%9F-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="https://medium.com/@urthella1"><img src="https://img.shields.io/badge/Medium-@urthella1-12100E?style=for-the-badge&logo=medium&logoColor=white" /></a>
  <a href="mailto:utkudemirtas0@gmail.com"><img src="https://img.shields.io/badge/Email-utkudemirtas0%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
</p>

</div>

---

### 👨‍💻 About me

```ts
const utku = {
  role:        "Fullstack Developer · Backend & DevOps",
  location:    "Konya, Türkiye",
  currently:   ["okutgitsin.com, a live-streamed vehicle-auction platform (launching soon)", "penpick.com.tr, a marketplace for pen collectors (launching soon)", "Reveil, an AI habit-tracking app"],
  shipped:     ["A distributed-systems series: CRDT sync, rate limiting, sagas, RAG, job queues"],
  learning:    ["Distributed systems", "AI · Data Science"],
  collab:      ["Interactive web experiences", "Anything that ships ✨"],
  reach:       "utkudemirtas0@gmail.com",
};
```

---

### 🏆 Flagship: [okutgitsin.com](https://okutgitsin.com)

> **🔨 okut: a live-streamed group vehicle-auction platform.**
> An admin opens a **live broadcast**, puts N cars up for auction, and users join with **tokens** and bid in real time.
> A Redis + **Lua** atomic bid engine handles millisecond-level bidding, **Socket.IO** broadcasts every offer, and
> **LiveKit** powers the camera/mic streams. Escrow deposit flow (HELD → REFUNDED/FORFEITED), IBAN verification,
> expert reports, a dealer dashboard, admin analytics, and Resend-powered transactional email.

`NestJS 11` · `Next.js 16` · `React 19` · `PostgreSQL + Prisma` · `Redis + Lua` · `Socket.IO` · `LiveKit` · `Turborepo` · `Deployed on Vercel`

<sub>Source is private; launching soon, the waitlist is open at <a href="https://okutgitsin.com">okutgitsin.com</a>.</sub>

---

### 🖋️ Flagship: [penpick.com.tr](https://penpick.com.tr)

> **🖋️ Penpick: a marketplace for pen collectors.**
> Buy and sell pens safely: the buyer's payment is held by Penpick until the pen is delivered. Fixed-price listings and
> **timed auctions** with scheduled endings, a launch perk that waives the first sale's commission for the first 100 members
> (granted under **Postgres advisory locks** so exactly 100 get it), username + password auth with e-mail/SMS verification,
> an admin panel, and a **React Native (Expo)** mobile app on the same API.

`Next.js 16` · `React 19` · `TypeScript` · `Prisma 7` · `Neon Postgres` · `Tailwind v4` · `Expo` · `Resend` · `Deployed on Vercel`

<sub>Source is private; launching soon, the waitlist is open at <a href="https://penpick.com.tr">penpick.com.tr</a>.</sub>

---

### 🧩 Backend & distributed-systems series

Five from-scratch builds around the problems that show up in real backends: concurrent state, distributed limits, partial failure, retrieval and job scheduling. Each one ships with tests and a runnable demo.

<table>
<tr>
<td width="50%" valign="top">

#### [✍️ realtime-collab-editor](https://github.com/Urthella/realtime-collab-editor)
**Google-Docs-style collaborative editor.** Yjs CRDTs synced over a custom y-websocket protocol server, live cursors and presence, JWT auth with viewer/editor sharing, and **debounced snapshot persistence** with version history instead of a write per keystroke.

`TypeScript` · `React` · `Tiptap` · `Yjs` · `WebSocket` · `Express` · `SQLite / Postgres`

</td>
<td width="50%" valign="top">

#### [🚦 distributed-rate-limiter](https://github.com/Urthella/distributed-rate-limiter)
**API gateway with three rate-limiting algorithms** (fixed window, token bucket, sliding window log), each with an in-memory and a **Redis + Lua** store so limits hold across replicas. Uses Redis server time to sidestep clock drift, with Prometheus metrics, a Grafana dashboard and a k6 load test.

`TypeScript` · `Node.js` · `Redis + Lua` · `Prometheus` · `Grafana` · `Docker`

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### [🔎 rag-codebase-qa](https://github.com/Urthella/rag-codebase-qa)
**Ask questions about a codebase, get answers with `file:line` citations.** tree-sitter AST chunking by function and class, hybrid **BM25 + vector** retrieval fused with RRF, strict grounding prompts, and an eval harness where hybrid retrieval reaches **94% hit@3**.

`Python` · `FastAPI` · `tree-sitter` · `pgvector` · `Claude / OpenAI`

</td>
<td width="50%" valign="top">

#### [📦 event-driven-order-system](https://github.com/Urthella/event-driven-order-system)
**Five microservices coordinating an order saga.** Failed steps trigger **compensating transactions** (refund, stock release), a transactional inbox keeps consumers idempotent under at-least-once delivery, and W3C trace context follows each order across every service.

`TypeScript` · `Node.js` · `RabbitMQ` · `OpenTelemetry` · `Jaeger` · `Docker`

</td>
</tr>
<tr>
<td colspan="2" valign="top">

#### [⚙️ job-queue-orchestrator](https://github.com/Urthella/job-queue-orchestrator)
**A mini Celery built from scratch.** Race-safe job claiming (SQLite `BEGIN IMMEDIATE` with an atomic `UPDATE ... RETURNING`, Postgres `FOR UPDATE SKIP LOCKED`), exponential backoff with a dead-letter queue, heartbeats plus a reaper that recovers jobs from crashed workers, and a **DAG workflow engine** with a live dashboard.

`Python` · `asyncio` · `FastAPI` · `SQLite` · `PostgreSQL`

</td>
</tr>
</table>

---

### 🧪 Latest builds

Smaller, focused repos across Rust, Go, TypeScript and Nix. Every one has CI, and all but the Nix configs ship a reproducible Nix dev shell.

| Repo | What it does | Stack |
|---|---|---|
| [mcp-postgres-guard](https://github.com/Urthella/mcp-postgres-guard) | MCP server that lets AI agents query Postgres without being able to break it: read-only, one statement at a time, time and row limits | `Go` · `MCP` · `Postgres` |
| [mcp-tcmb-kur](https://github.com/Urthella/mcp-tcmb-kur) | MCP server for the Central Bank of Türkiye's daily exchange rates, with history and no API key | `Go` · `MCP` |
| [llm-gateway-go](https://github.com/Urthella/llm-gateway-go) | One OpenAI-compatible endpoint for all your LLM providers: fallback, per-client keys and limits, response cache, Prometheus metrics | `Go` · `LLM` |
| [baited](https://github.com/Urthella/baited) | Harmless traps that test whether your coding agent hands over your `.env`, with a fake secret and a local listener. Includes a small pilot on Claude Code and Codex CLI | `TypeScript` · `Claude Code` · `Codex CLI` |
| [gcra-lite](https://github.com/Urthella/gcra-lite) | Dependency-free GCRA rate limiter: one atomic per limiter, plus a keyed limiter for per-user quotas | `Rust` |
| [backend-agent-skills](https://github.com/Urthella/backend-agent-skills) | Agent Skills for Postgres migration review, k6 load test plans and incident response, linted in CI with skill-lint | `Agent Skills` · `Postgres` · `k6` |
| [nixos-wsl-dev](https://github.com/Urthella/nixos-wsl-dev) | My Windows dev machine as a NixOS-WSL flake: the whole Linux side rebuilds from the repo | `Nix` · `NixOS` |
| [agent-memory-sqlite](https://github.com/Urthella/agent-memory-sqlite) | Persistent memory for coding agents as an MCP server: SQLite FTS5, BM25 + recency ranking, zero native deps | `TypeScript` · `MCP` · `SQLite` |
| [context-compressor](https://github.com/Urthella/context-compressor) | `ctxc`: shrinks test and build logs to an LLM token budget, 94% smaller on a real `cargo test` run with the failure intact | `Rust` |
| [skill-lint](https://github.com/Urthella/skill-lint) | Linter and GitHub Action for Agent Skills (`SKILL.md`): spec rules, broken links, nested references | `TypeScript` · `GitHub Actions` |
| [nix-devshells](https://github.com/Urthella/nix-devshells) | Flake templates for Rust, Go, Node/TS, Python and Solidity dev shells, smoke-tested in CI | `Nix` |
| [dotfiles-nix](https://github.com/Urthella/dotfiles-nix) | My whole shell and editor setup as a home-manager flake for NixOS-WSL | `Nix` · `home-manager` |

---

### 🚀 Featured projects

<table>
<tr>
<td width="50%" valign="top">

#### [💸 costsight](https://github.com/Urthella/costsight)
**Cloud cost anomaly detection** on AWS CUR data.
Three detectors run in parallel (**STL · Isolation Forest · Z-Score**), with severity-banded alerts and a Streamlit dashboard.

Benchmarked across **25 random seeds**: STL wins overall (F1 ≈ 0.76), Z-Score is a perfect point-spike detector, Isolation Forest sits in between.

`Python` · `scikit-learn` · `Streamlit` · `pandas` · `pytest` · `CI`

</td>
<td width="50%" valign="top">

#### [📊 algorithm-test-sim](https://github.com/Urthella/algorithm-test-sim)
**Sorting algorithm benchmarking suite:** Quick / Heap / Shell / Merge / Radix tested on Random, Partially Sorted, and Reverse Sorted data across sizes from 1K to 500K.

Spring Boot REST API + React/Vite UI for interactive comparison, with line / bar / radar charts and CSV/JSON export.

`Java 17` · `Spring Boot` · `Maven` · `React` · `Vite` · `JUnit`

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### [🖥️ MIPS16 Pipeline Simulator](https://github.com/Urthella/MIPS16-pipeline-simulator)
**5-stage 16-bit MIPS CPU** simulator with hazard handling (data forwarding EX-EX and MEM-EX, load-use stall detection, branch flush), plus a Verilog RTL twin and live web visualization of registers, memory, and pipeline state.

`Java 17` · `Javalin` · `React` · `TypeScript` · `Verilog` · `Gradle`

</td>
<td width="50%" valign="top">

#### [🚗 used-car-platform](https://github.com/Urthella/used-car-platform)
**Used-car marketplace** with JWT auth, role-based access (admin / seller / buyer), favorites, in-app messaging, image uploads, and a full Cypress E2E suite. Helmet, rate-limiting, and CORS hardening on the API.

`Next.js 14` · `Express` · `MongoDB` · `Tailwind` · `Jest` · `Cypress`

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### [⏰ Reveil](https://github.com/Urthella/Reveil) <sup>WIP</sup>
**AI-powered habit-tracking** mobile app. Three-tier architecture: React Native (Expo) client + NestJS API + FastAPI AI engine, all backed by PostgreSQL.

`React Native` · `Expo` · `NestJS` · `FastAPI` · `PostgreSQL`

</td>
<td width="50%" valign="top">

#### [🌐 portfolio-website](https://github.com/Urthella/portfolio-website)
Personal portfolio at [utkudemirtas.tech](https://www.utkudemirtas.tech) with a **WebGL fluid background**, **bilingual TR/EN** content, an interactive terminal and command palette, a live theme lab, an auto lite mode for weaker machines, and an EmailJS contact form.

`Next.js 15` · `React 19` · `WebGL` · `Tailwind` · `Framer Motion` · `GSAP`

</td>
</tr>
</table>

---

### 🤝 Open-source collaborations

Repos I contribute to as a collaborator on [**@thefcan**](https://github.com/thefcan)'s org. My role is mainly **test suites and CI pipelines** (across Go, Python, Rust, C++ and the web stack), plus fixes along the way.

<table>
<tr>
<td width="50%" valign="top">

#### [🧠 ragdesk](https://github.com/thefcan/ragdesk)
**Multi-tenant, AI-powered knowledge SaaS.** Teams upload documents and chat with an assistant that answers **only from those documents, with citations** (RAG). Go core for tenancy/billing/metering, a FastAPI LLM + embedding pipeline, a Next.js front-end, Postgres + pgvector, and a provider-agnostic model layer, with a live demo and CI/CD/CodeQL.

`Go` · `FastAPI` · `Next.js` · `Postgres + pgvector` · `Ollama/Gemini`

<sub>My contribution: the web **Vitest** suite + CI step.</sub>

</td>
<td width="50%" valign="top">

#### [⛓️ gochain](https://github.com/thefcan/gochain)
**A blockchain written from scratch in Go:** proof of work, a signed **UTXO** transaction model, ECDSA wallets, BoltDB persistence, and TCP peer-to-peer sync. Built to a production standard: property-based and fuzz tests, a security-reviewed network layer, and static analysis.

`Go` · `Proof of Work` · `ECDSA` · `BoltDB` · `P2P`

<sub>My contribution: the `cmd` CLI test suite.</sub>

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### [🌀 k8s-resilience-harness](https://github.com/thefcan/k8s-resilience-harness)
**Kubernetes chaos / resilience harness in Go.** Inject controlled faults into a system on Kubernetes, check a **steady-state hypothesis**, measure recovery, and report a deterministic pass/fail, with an ML-based anomaly layer over accumulated runs.

`Go` · `Kubernetes` · `Chaos engineering` · `kind`

<sub>My contribution: buildinfo + k8s-client tests.</sub>

</td>
<td width="50%" valign="top">

#### [🔥 femheat](https://github.com/thefcan/femheat)
**From-scratch 2D finite-element solver** for steady-state heat conduction in modern C++17. Hand-written Galerkin assembly, a Jacobi-preconditioned CG solve (Eigen), and HDF5/XDMF output for ParaView, validated to **second-order accuracy** by the Method of Manufactured Solutions.

`C++17` · `Eigen` · `CMake` · `GoogleTest` · `FEM`

<sub>My contribution: Point/Material value-type tests.</sub>

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### [📦 gocontainer](https://github.com/thefcan/gocontainer)
**A container runtime in ~80 lines of Go:** a learning re-implementation of the core of `docker run`. Isolates a process with Linux **namespaces** (UTS, PID, mount), chroots into a root filesystem, and mounts a private `/proc`. Standard library only.

`Go` · `Linux namespaces` · `chroot`

<sub>My contribution: config helpers + tests + CI go-test.</sub>

</td>
<td width="50%" valign="top">

#### [🛍️ dolap-sale-prediction](https://github.com/thefcan/dolap-sale-prediction)
**End-to-end ML** predicting whether a second-hand fashion listing sells **within 7 days**. Covers scraping, time-aware labeling, feature engineering, model comparison, ablation analysis, and a live demo, with XGBoost on top.

`Python` · `XGBoost` · `scikit-learn` · `pandas`

<sub>My contribution: pytest suite + first CI workflow.</sub>

</td>
</tr>
</table>

<sub>Also contributing to <a href="https://github.com/thefcan/rust-url-shortener">rust-url-shortener</a> (Rust · Axum) and <a href="https://github.com/thefcan/unity-match3">unity-match3</a> (Unity · C#).</sub>

---

### 🛠️ Tech stack

<table>
<tr>
<td valign="top"><strong>Frontend</strong></td>
<td>
<img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" />
<img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" />
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
<img src="https://img.shields.io/badge/React%20Native-20232A?style=flat-square&logo=react&logoColor=61DAFB" />
<img src="https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" />
</td>
</tr>
<tr>
<td valign="top"><strong>Backend</strong></td>
<td>
<img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" />
<img src="https://img.shields.io/badge/Spring-6DB33F?style=flat-square&logo=spring&logoColor=white" />
<img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" />
<img src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white" />
<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
<img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" />
<img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" />
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
</td>
</tr>
<tr>
<td valign="top"><strong>Data &amp; Infra</strong></td>
<td>
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" />
<img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" />
<img src="https://img.shields.io/badge/Apache%20Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white" />
<img src="https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Nix-5277C3?style=flat-square&logo=nixos&logoColor=white" />
</td>
</tr>
<tr>
<td valign="top"><strong>Tools</strong></td>
<td>
<img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" />
<img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" />
<img src="https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white" />
<img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white" />
<img src="https://img.shields.io/badge/OpenTelemetry-425CC7?style=flat-square&logo=opentelemetry&logoColor=white" />
<img src="https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white" />
<img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white" />
</td>
</tr>
</table>

---

### 📊 GitHub stats

<div align="center">

<a href="https://github.com/Urthella">
  <img height="180" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Urthella&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" />
</a>

<br/>

<a href="https://github.com/Urthella">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Urthella&theme=tokyonight&hide_border=true" />
</a>

</div>

---

<div align="center">

> *"Build it. Break it. Ship it. Then learn what broke."*

</div>
