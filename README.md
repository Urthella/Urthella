<div align="center">

<a href="https://www.utkuwankenobi.tech">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&pause=1000&color=58A6FF&center=true&vCenter=true&width=600&lines=Hi+there%2C+I'm+Utku+%F0%9F%91%8B;Fullstack+Developer+%C2%B7+CE+Student;Building+with+React%2C+Spring%2C+and+a+bit+of+AI" alt="Typing SVG" />
</a>

<p>
  <a href="https://www.utkuwankenobi.tech"><img src="https://img.shields.io/badge/Portfolio-utkuwankenobi.tech-58A6FF?style=for-the-badge&logo=vercel&logoColor=white" /></a>
  <a href="https://linkedin.com/in/utkudemirtas"><img src="https://img.shields.io/badge/LinkedIn-Utku_Demirta%C5%9F-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="https://medium.com/@urthella1"><img src="https://img.shields.io/badge/Medium-@urthella1-12100E?style=for-the-badge&logo=medium&logoColor=white" /></a>
  <a href="mailto:utkudemirtas0@gmail.com"><img src="https://img.shields.io/badge/Email-utkudemirtas0%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
</p>

<img src="https://komarev.com/ghpvc/?username=urthella&label=Profile+views&color=58a6ff&style=flat-square" alt="Profile views" />

</div>

---

### 👨‍💻 About me

```ts
const utku = {
  role:        "Fullstack Developer · CE Student",
  location:    "Türkiye",
  currently:   ["okutgitsin.com — live vehicle-auction platform", "Reveil — AI habit-tracking app"],
  learning:    ["AI · Data Science", "Advanced React patterns"],
  collab:      ["Interactive web experiences", "Anything that ships ✨"],
  reach:       "utkudemirtas0@gmail.com",
};
```

---

### 🏆 Flagship — [okutgitsin.com](https://okutgitsin.com)

> **[🔨 okut](https://github.com/Urthella/okut) — a live-streamed group vehicle-auction platform.**
> An admin opens a **live broadcast**, puts N cars up for auction, and users join with **tokens** and bid in real time.
> A Redis + **Lua** atomic bid engine handles millisecond-level bidding, **Socket.IO** broadcasts every offer, and
> **LiveKit** powers the camera/mic streams. Escrow deposit flow (HELD → REFUNDED/FORFEITED), IBAN verification,
> expert reports, a dealer dashboard, admin analytics, and Resend-powered transactional email.

`NestJS 11` · `Next.js 16` · `React 19` · `PostgreSQL + Prisma` · `Redis + Lua` · `Socket.IO` · `LiveKit` · `Turborepo` · `Deployed on Vercel`

---

### 🚀 Featured projects

<table>
<tr>
<td width="50%" valign="top">

#### [💸 costsight](https://github.com/Urthella/costsight)
**Cloud cost anomaly detection** on AWS CUR data.
Three detectors run in parallel — **STL · Isolation Forest · Z-Score** — with severity-banded alerts and a Streamlit dashboard.

Benchmarked across **25 random seeds**: STL wins overall (F1 ≈ 0.76), Z-Score is a perfect point-spike detector, Isolation Forest sits in between.

`Python` · `scikit-learn` · `Streamlit` · `pandas` · `pytest` · `CI`

</td>
<td width="50%" valign="top">

#### [📊 algortihm-test-sim](https://github.com/Urthella/algortihm-test-sim)
**Sorting algorithm benchmarking suite** — Quick / Heap / Shell / Merge / Radix tested on Random, Partially Sorted, and Reverse Sorted data across sizes from 1K to 500K.

Spring Boot REST API + React/Vite UI for interactive comparison, with line / bar / radar charts and CSV/JSON export.

`Java 17` · `Spring Boot` · `Maven` · `React` · `Vite` · `JUnit`

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### [🖥️ MIPS16 Pipeline Simulator](https://github.com/Urthella/MIPS16-pipeline-simulator)
**5-stage 16-bit MIPS CPU** simulator with hazard handling — data forwarding (EX-EX, MEM-EX), load-use stall detection, branch flush — plus a Verilog RTL twin and live web visualization of registers, memory, and pipeline state.

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
Personal portfolio with a **3D Spline robot scene** that tracks the cursor across the page, **bilingual TR/EN** content, EmailJS contact form, and Framer Motion animations.

`Next.js 15` · `React 19` · `Spline` · `shadcn/ui` · `Framer Motion`

</td>
</tr>
</table>

---

### 🤝 Open-source collaborations

Repos I contribute to as a collaborator on [**@thefcan**](https://github.com/thefcan)'s org — my role is mainly **test suites and CI pipelines** (across Go, Python, Rust, C++ and the web stack), plus fixes along the way.

<table>
<tr>
<td width="50%" valign="top">

#### [🧠 ragdesk](https://github.com/thefcan/ragdesk)
**Multi-tenant, AI-powered knowledge SaaS.** Teams upload documents and chat with an assistant that answers **only from those documents, with citations** (RAG). Go core for tenancy/billing/metering, a FastAPI LLM + embedding pipeline, a Next.js front-end, Postgres + pgvector, and a provider-agnostic model layer — with a live demo and CI/CD/CodeQL.

`Go` · `FastAPI` · `Next.js` · `Postgres + pgvector` · `Ollama/Gemini`

<sub>My contribution: the web **Vitest** suite + CI step.</sub>

</td>
<td width="50%" valign="top">

#### [⛓️ gochain](https://github.com/thefcan/gochain)
**A blockchain written from scratch in Go** — proof of work, a signed **UTXO** transaction model, ECDSA wallets, BoltDB persistence, and TCP peer-to-peer sync. Built to a production standard: property-based and fuzz tests, a security-reviewed network layer, and static analysis.

`Go` · `Proof of Work` · `ECDSA` · `BoltDB` · `P2P`

<sub>My contribution: the `cmd` CLI test suite.</sub>

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### [🌀 k8s-resilience-harness](https://github.com/thefcan/k8s-resilience-harness)
**Kubernetes chaos / resilience harness in Go.** Inject controlled faults into a system on Kubernetes, check a **steady-state hypothesis**, measure recovery, and report a deterministic pass/fail — with an ML-based anomaly layer over accumulated runs.

`Go` · `Kubernetes` · `Chaos engineering` · `kind`

<sub>My contribution: buildinfo + k8s-client tests.</sub>

</td>
<td width="50%" valign="top">

#### [🔥 femheat](https://github.com/thefcan/femheat)
**From-scratch 2D finite-element solver** for steady-state heat conduction in modern C++17. Hand-written Galerkin assembly, a Jacobi-preconditioned CG solve (Eigen), and HDF5/XDMF output for ParaView — validated to **second-order accuracy** by the Method of Manufactured Solutions.

`C++17` · `Eigen` · `CMake` · `GoogleTest` · `FEM`

<sub>My contribution: Point/Material value-type tests.</sub>

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### [📦 gocontainer](https://github.com/thefcan/gocontainer)
**A container runtime in ~80 lines of Go** — a learning re-implementation of the core of `docker run`. Isolates a process with Linux **namespaces** (UTS, PID, mount), chroots into a root filesystem, and mounts a private `/proc`. Standard library only.

`Go` · `Linux namespaces` · `chroot`

<sub>My contribution: config helpers + tests + CI go-test.</sub>

</td>
<td width="50%" valign="top">

#### [🛍️ dolap-sale-prediction](https://github.com/thefcan/dolap-sale-prediction)
**End-to-end ML** predicting whether a second-hand fashion listing sells **within 7 days**. Covers scraping, time-aware labeling, feature engineering, model comparison, ablation analysis, and a live demo — XGBoost on top.

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
<img src="https://img.shields.io/badge/Vue.js-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white" />
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
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
</td>
</tr>
<tr>
<td valign="top"><strong>Data &amp; Infra</strong></td>
<td>
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" />
<img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" />
<img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" />
<img src="https://img.shields.io/badge/Apache%20Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white" />
</td>
</tr>
<tr>
<td valign="top"><strong>Tools</strong></td>
<td>
<img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" />
<img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" />
<img src="https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white" />
<img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white" />
<img src="https://img.shields.io/badge/Arduino-00979D?style=flat-square&logo=arduino&logoColor=white" />
</td>
</tr>
</table>

---

### 📊 GitHub stats

<div align="center">

<a href="https://github.com/Urthella">
  <img height="180" src="https://github-readme-stats.vercel.app/api?username=Urthella&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true" />
  <img height="180" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Urthella&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" />
</a>

<br/>

<a href="https://github.com/Urthella">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Urthella&theme=tokyonight&hide_border=true" />
</a>

<br/><br/>

<a href="https://github.com/Urthella">
  <img src="https://github-profile-trophy.vercel.app/?username=Urthella&theme=tokyonight&no-frame=true&no-bg=true&row=1&column=7" />
</a>

</div>

---

<div align="center">

> *"Build it. Break it. Ship it. Then learn what broke."*

</div>
