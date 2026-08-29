<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:512BD4,100:DD0031&height=180&section=header&text=Kalu%20Abiyu&fontSize=48&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Fullstack%20.NET%20%2B%20Angular%20Developer&descAlignY=58&descSize=18" width="100%" alt="Kalu Abiyu — Fullstack .NET + Angular Developer"/>

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=800&color=512BD4&center=true&vCenter=true&width=650&lines=Building+TMS+%E2%80%94+ASP.NET+Core+10+%2B+Angular+22;Clean+Architecture+%7C+CQRS+%2F+MediatR+%7C+SignalR;JWT+Bearer+Auth+%2B+Resource-Based+Policies+%E2%80%94+M11;Vitest+%2B+Playwright+E2E+%E2%80%94+M12;Designing+PMAFS+%E2%80%94+Pharmacy+Stock+Finder+for+Addis+Ababa;NgRx+SignalStore+%7C+Zoneless+Angular+%7C+Reactive+Forms;Always+learning%2C+always+shipping." alt="Typing SVG — Building TMS with ASP.NET Core 10 and Angular 22" />
</a>

<br/>

![Profile Views](https://komarev.com/ghpvc/?username=kaluabiyu-wq&color=512BD4&style=for-the-badge&label=PROFILE+VIEWS)
[![GitHub followers](https://img.shields.io/github/followers/kaluabiyu-wq?label=Followers&style=for-the-badge&color=DD0031)](https://github.com/kaluabiyu-wq?tab=followers)
[![Public Repos](https://img.shields.io/badge/dynamic/json?label=Repos&query=public_repos&url=https%3A%2F%2Fapi.github.com%2Fusers%2Fkaluabiyu-wq&color=512BD4&style=for-the-badge)](https://github.com/kaluabiyu-wq?tab=repositories)
![Open to Work](https://img.shields.io/badge/Open%20to%20Work-success?style=for-the-badge&logo=briefcase&logoColor=white)

</div>

---

## 👋 About Me

Fullstack developer building production-style applications end-to-end on the **.NET + Angular** stack — from API and database design through to the client — with a strong interest in system architecture.

- 🎓 Working through a structured fullstack curriculum: **C# 14 / .NET 10, TypeScript, Git, ASP.NET Core 10, EF Core 10 with PostgreSQL, Angular 22**
- 🏗️ Building **TMS (Training Management System)** — ASP.NET Core 10 API (Clean Architecture, CQRS/MediatR, SignalR) + Angular 22 zoneless client (signals, NgRx SignalStore, `@defer`-loaded analytics dashboard)
- 💊 Building **PMAFS (Pharmacy Medicine Availability Finding System)** — location-aware pharmacy stock platform for Addis Ababa, run as a parallel independent project alongside the curriculum, mirroring the same module structure (C# domain modeling, TypeScript, Git, ASP.NET Core, EF Core/PostgreSQL, REST API, hardening, Angular client). Currently mid-migration: splitting PMFApi out of its original single-project layout into a layered Clean Architecture (`PmfApi.Domain`/`PmfApi.Application`/`PmfApi.Infrastructure`/`PmfApi.Api`), matching the structure TMS moved to earlier in the curriculum
- 📍 Based in Addis Ababa, Ethiopia
- ⚡ Right now: **Module 12, Session 2 — Frontend Vitest, Playwright E2E & Business Rule Sprint.** Locking down the TMS frontend surface after M11's auth hardening: Vitest component specs for signal-input Angular components (`fixture.componentRef.setInput`, `provideRouter([])`), NgRx SignalStore integration specs, HTTP-boundary specs against `HttpTestingController`, and a Playwright E2E suite — shared-`storageState` auth reuse across a `setup` project dependency, a happy-path admin-approves-enrollment flow, and an unhappy-path spec forcing a 500 via `page.route` — plus a new `MaxEnrollmentsPerStudent` business rule driven out with a guiding test.
---

## 🚀 Featured Projects

<details open>
<summary><b>🎓 Training Management System (TMS)</b> — click to collapse</summary>
<br/>

Fullstack training/course enrollment platform for a fictional training institution (CTBE).

| Layer | Highlights |
|---|---|
| **API** | ASP.NET Core 10, EF Core 10, PostgreSQL — layered Clean Architecture (Domain/Application/Infrastructure/Api), CQRS with MediatR, FluentValidation, HATEOAS, versioned REST endpoints, RFC 9457 ProblemDetails |
| **Real-time** | SignalR typed hubs (`ITmsHubClient`) for enrollment/transcript/grade notifications, async request-reply pattern for long-running work with idempotency keys |
| **Client** | Angular 22, standalone components, zoneless change detection, signals, NgRx SignalStore, reactive forms, `@defer` blocks with Angular Material — including an instructor analytics dashboard with a live Approved/Pending/Rejected chart, defensive RxJS (`exhaustMap` rage-click guards, `takeUntilDestroyed`), and a `LiveSyncService` bridging SignalR push events into the store |
| **Auth & Security** | M10: HttpOnly auth cookie + antiforgery (XSRF) handshake. M11: JWT Bearer authentication with refresh token rotation, resource-based policy authorization (`CourseInstructorHandler`), Angular route guards + JWT interceptor, named rate-limit policies, and a security-response-headers middleware — followed by a correction pass that fixed real bugs across both the API and client branches |
| **Testing** | M12: Vitest component/store specs (signal inputs, `HttpTestingController` boundary tests) and a Playwright E2E suite covering happy-path and failure-path (forced 5xx) journeys, with shared `storageState` auth reuse across a dedicated `setup` project |

**Repos:**
[![TmsApi](https://img.shields.io/badge/TmsApi-181717?style=flat-square&logo=github)](https://github.com/kaluabiyu-wq/TmsApi)
[![tms-clients2](https://img.shields.io/badge/tms--clients2-181717?style=flat-square&logo=github)](https://github.com/kaluabiyu-wq/tms-clients2)
[![TmsCore](https://img.shields.io/badge/TmsCore-181717?style=flat-square&logo=github)](https://github.com/kaluabiyu-wq/TmsCore)
[![tms-client](https://img.shields.io/badge/tms--client-181717?style=flat-square&logo=github)](https://github.com/kaluabiyu-wq/tms-client)


</details>

<details>
<summary><b>💊 PMAFS — Pharmacy Medicine Availability Finding System</b> — click to expand</summary>
<br/>

A pharmacy-network API for Addis Ababa that tracks which pharmacies carry which medicines, at what price, and how reliable that stock information is. Built as two pieces: **PMFCore**, a small standalone project for prototyping the domain rules in isolation, and **PMFApi**, the full ASP.NET Core Web API that implements them for real, with a TypeScript/Node client on top. PMFApi is currently on its `Pmf-Split-in-CleanArchitecture` branch, mid-migration from a single-project layout into four layered projects (`PmfApi.Domain`, `PmfApi.Application`, `PmfApi.Infrastructure`, `PmfApi.Api`).

| Layer | Highlights |
|---|---|
| **Domain (PMFCore)** | Standalone prototyping project for the core rules before they hit the full API — a `PharmacyRank` scoring algorithm blending stock freshness and recency-of-update into a 1–4 reliability tier, validation baked into the models themselves (no medicine price ≤ 10, no blank names, reliability scores clamped to 1–100), plus LINQ grouping and async lookups (`Task.WhenAll`, dictionary-keyed lookups) for batched data loading |
| **API (PMFApi)** | ASP.NET Core, EF Core migrations against PostgreSQL (Npgsql) — versioned CRUD controllers for Pharmacies, Medicines, Inventory, Locations, Users, Roles, Pharmacy Schedules, and User Feedback; global exception handling via `ProblemDetails`, request logging middleware, Scalar/OpenAPI docs; currently being split into a 4-project Clean Architecture layout (`PmfApi.Domain`/`Application`/`Infrastructure`/`Api`) on the `Pmf-Split-in-CleanArchitecture` branch |
| **Data & Auditing** | Every price change on an inventory item is logged (old price, who changed it, when) via a dedicated `InventoryHistory` entity; pharmacies and users tied to a `Location` record carrying subcity, woreda, and lat/long coordinates for location-aware search |
| **Auth** | Custom header-based `PharmacyAuthHandler` authentication handler backing four roles (Patient, Pharmacy Staff, Pharmacy Admin, System Admin) |
| **Client** | TypeScript/Node client (Pmf-Client) built on TypeScript 7.0 (the Go-based compiler rewrite), using discriminated unions with the Temporal API and Angular reactive forms with `FormArray` |

**Repos:**
[![PMFApi](https://img.shields.io/badge/PMFApi-181717?style=flat-square&logo=github)](https://github.com/kaluabiyu-wq/PMFApi)
[![PMFCore](https://img.shields.io/badge/PMFCore-181717?style=flat-square&logo=github)](https://github.com/kaluabiyu-wq/PMFCore)
[![Pmf-Client](https://img.shields.io/badge/Pmf--Client-181717?style=flat-square&logo=github)](https://github.com/kaluabiyu-wq/Pmf-Client)

</details>

---

## 🛠️ Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=cs,dotnet,postgres,angular,ts,git,html,css&theme=dark" alt="Tech stack icons: C#, .NET, PostgreSQL, Angular, TypeScript, Git, HTML, CSS"/>
</p>

<details>
<summary><b>See full breakdown by category</b></summary>
<br/>

**Backend**
![C#](https://img.shields.io/badge/-C%23-239120?style=flat&logo=c-sharp&logoColor=white)
![.NET](https://img.shields.io/badge/-.NET%2010-512BD4?style=flat&logo=dotnet&logoColor=white)
![ASP.NET Core](https://img.shields.io/badge/-ASP.NET%20Core-512BD4?style=flat&logo=dotnet&logoColor=white)
![EF Core](https://img.shields.io/badge/-EF%20Core-512BD4?style=flat)
![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![SignalR](https://img.shields.io/badge/-SignalR-512BD4?style=flat)
![JWT](https://img.shields.io/badge/-JWT-000000?style=flat&logo=jsonwebtokens&logoColor=white)

**Frontend**
![Angular](https://img.shields.io/badge/-Angular-DD0031?style=flat&logo=angular&logoColor=white)
![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![NgRx](https://img.shields.io/badge/-NgRx%20SignalStore-BA2BD2?style=flat)
![RxJS](https://img.shields.io/badge/-RxJS-B7178C?style=flat&logo=reactivex&logoColor=white)

**Testing**
![Vitest](https://img.shields.io/badge/-Vitest-6E9F18?style=flat&logo=vitest&logoColor=white)
![Playwright](https://img.shields.io/badge/-Playwright-2EAD33?style=flat&logo=playwright&logoColor=white)

**Tools & Practices**
![Git](https://img.shields.io/badge/-Git-F05032?style=flat&logo=git&logoColor=white)
![Clean Architecture](https://img.shields.io/badge/-Clean%20Architecture-2E8B57?style=flat)
![CQRS](https://img.shields.io/badge/-CQRS-2E8B57?style=flat)
![MediatR](https://img.shields.io/badge/-MediatR-2E8B57?style=flat)

</details>

---

## 📌 Pinned Repos

<div align="center">

<a href="https://github.com/kaluabiyu-wq/TmsApi">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=kaluabiyu-wq&repo=TmsApi&theme=tokyonight&hide_border=true&cache_seconds=86400" width="48%" alt="TmsApi repo card"/>
</a>
<a href="https://github.com/kaluabiyu-wq/tms-clients2">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=kaluabiyu-wq&repo=tms-clients2&theme=tokyonight&hide_border=true&cache_seconds=86400" width="48%" alt="tms-clients2 repo card"/>
</a>
<a href="https://github.com/kaluabiyu-wq/PMFApi">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=kaluabiyu-wq&repo=PMFApi&theme=tokyonight&hide_border=true&cache_seconds=86400" width="48%" alt="PMFApi repo card"/>
</a>

</div>

---

## ❓ FAQ

<details>
<summary><b>What am I currently learning?</b></summary>
<br/>
Just wrapped Module 12, Session 2 — Frontend Vitest, Playwright E2E & Business Rule Sprint. Building on M11's JWT/policy auth work, I locked down the Angular frontend surface: Vitest specs for signal-input components and NgRx SignalStores, HTTP-boundary specs against HttpTestingController, and a Playwright E2E suite with shared storageState auth reuse across a dedicated setup project — covering both a happy-path admin-approve-enrollment flow and an unhappy-path spec that forces a 500 to verify the error banner. Also drove out a new MaxEnrollmentsPerStudent business rule with a guiding test.
</details>

<details>
<summary><b>Am I open to collaborating or job opportunities?</b></summary>
<br/>
Yes — I'm particularly interested in fullstack roles working with .NET and Angular. Feel free to reach out via email or LinkedIn above.
</details>

<details>
<summary><b>What's the tech stack behind TMS, in one line?</b></summary>
<br/>
ASP.NET Core 10 API (Clean Architecture + CQRS/MediatR + SignalR) talking to an Angular 22 zoneless client (signals + NgRx SignalStore), backed by a Vitest + Playwright test suite.
</details>

<details>
<summary><b>How can you support this profile?</b></summary>
<br/>
Starring the repos above is the biggest help — it's the single strongest signal for both GitHub's discovery algorithm and anyone evaluating the work. A follow keeps you posted as new modules ship.
</details>

---

## 📊 GitHub Stats

<div align="center">

<img src="https://streak-stats.demolab.com/?user=kaluabiyu-wq&theme=tokyonight&hide_border=true&disable_animations=true" width="49%" alt="Kalu's GitHub streak stats"/>

</div>

---

## 📬 Contact Me

<div align="center">

[![Email](https://img.shields.io/badge/Email-kaluabiyu%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:kaluabiyu@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-kalu--abiyu-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/kalu-abiyu)
[![Instagram](https://img.shields.io/badge/Instagram-Kalu__abi77-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/Kalu_abi77)

</div>

<table align="center">
<tr>
<td align="center" width="33%">

**📧 Email**
<br/>
for job offers, collaboration proposals, or anything that needs a real reply.
<br/>
<a href="mailto:kaluabiyu@gmail.com">kaluabiyu@gmail.com</a>
</td>
<td align="center" width="33%">

**💼 LinkedIn**
<br/>
 for professional networking and recruiter outreach.
<br/>
<a href="https://linkedin.com/in/kalu-abiyu">/in/kalu-abiyu</a>
</td>
<td align="center" width="33%">

**📸 Instagram**
<br/>
 for a more casual hello or to see what I'm up to outside of code.
<br/>
<a href="https://instagram.com/Kalu_abi77">@Kalu_abi77</a>
</td>
</tr>
</table>

---
