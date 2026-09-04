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

Fullstack developer building production-style applications end-to-end on the .NET + Angular stack — from API and database design through to the client — with a strong interest in system architecture.

- 🎓 Going through a fullstack curriculum: C# 14 / .NET 10, TypeScript, Git, ASP.NET Core 10, EF Core 10 + PostgreSQL, Angular 22
- 🏗️ **TMS (Training Management System)** — ASP.NET Core 10 API (Clean Architecture, CQRS/MediatR, SignalR) + a zoneless Angular 22 client (signals, NgRx SignalStore, a `@defer`-loaded analytics dashboard)
- 💊 **PMAFS (Pharmacy Medicine Availability Finding System)** — a location-aware pharmacy stock finder for Addis Ababa, built alongside the curriculum on the same module structure. Still splitting PMFApi out of its old single-project layout into Clean Architecture (Domain/Application/Infrastructure/Api), same move TMS made earlier — once that's done, next up is wiring Pmf-Clients-2 (the Angular frontend) to it
- 📍 Addis Ababa, Ethiopia
- ⚡ **TMS now:** Module 12, Session 2 — frontend testing. Vitest for components/stores, HTTP boundary specs, Playwright E2E with shared login state, plus a new `MaxEnrollmentsPerStudent` rule
- ⚡ **PMAFS now:** splitting PMFApi into Clean Architecture. Pmf-Clients-2 is queued up next once that's done

---

## 🚀 Featured Projects

<details open>
<summary><b>🎓 Training Management System (TMS)</b> — click to collapse</summary>
<br/>

Course enrollment platform for a fictional training institution (CTBE).

| Layer | Highlights |
|---|---|
| **API** | ASP.NET Core 10, EF Core 10, PostgreSQL — Clean Architecture, CQRS/MediatR, versioned endpoints, ProblemDetails |
| **Real-time** | SignalR hubs for enrollment/transcript/grade updates, async request-reply for longer jobs |
| **Client** | Angular 22, zoneless, signals, NgRx SignalStore — instructor dashboard, live SignalR sync |
| **Auth & Security** | JWT with refresh rotation, resource-based policies, route guards, rate limiting, security headers |
| **Testing** *(in progress)* | Vitest for components/stores, Playwright E2E, shared login state across a setup project |

**Repos:**
[![TmsApi](https://img.shields.io/badge/TmsApi-181717?style=flat-square&logo=github)](https://github.com/kaluabiyu-wq/TmsApi)
[![tms-clients2](https://img.shields.io/badge/tms--clients2-181717?style=flat-square&logo=github)](https://github.com/kaluabiyu-wq/tms-clients2)
[![TmsCore](https://img.shields.io/badge/TmsCore-181717?style=flat-square&logo=github)](https://github.com/kaluabiyu-wq/TmsCore)
[![tms-client](https://img.shields.io/badge/tms--client-181717?style=flat-square&logo=github)](https://github.com/kaluabiyu-wq/tms-client)

</details>

<details>
<summary><b>💊 PMAFS — Pharmacy Medicine Availability Finding System</b> — click to expand</summary>
<br/>

A pharmacy network API for Addis Ababa — which pharmacies carry which medicines, at what price, and how trustworthy that stock info is. Two pieces: **PMFCore**, where I prototype the domain rules on their own, and **PMFApi**, the real ASP.NET Core Web API with a TypeScript client on top. PMFApi is still mid-split on the `Pmf-Split-in-CleanArchitecture` branch, moving into four layered projects (Domain/Application/Infrastructure/Api). Once that lands, the next stop is Pmf-Clients-2 — bringing the Angular frontend up to speed with the new API shape.

| Layer | Highlights |
|---|---|
| **Domain (PMFCore)** | `PharmacyRank` score (stock freshness + recency → 1–4 tier), validation baked into the models, async batched lookups |
| **API (PMFApi)** *(in progress)* | EF Core + PostgreSQL, versioned CRUD across Pharmacies, Medicines, Inventory, Locations, Users. Mid-split into 4-project Clean Architecture |
| **Data & Auditing** | Every inventory price change logged via `InventoryHistory`. `Location` records carry subcity, woreda, lat/long for proximity search |
| **Auth** | Custom header-based `PharmacyAuthHandler`, four roles: Patient, Pharmacy Staff, Pharmacy Admin, System Admin |
| **Client (Pmf-Client)** *(next up)* | TypeScript 7.0, discriminated unions with the Temporal API, Angular reactive forms — Pmf-Clients-2 rebuild queued after the API split |

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
Just wrapped Module 12, Session 2 — frontend testing. Building on M11's JWT/policy work: Vitest specs for signal-input components and NgRx SignalStores, HTTP boundary specs, and a Playwright E2E suite with shared login state — a happy-path admin-approve flow and a forced-500 spec to check the error banner. Also added a MaxEnrollmentsPerStudent rule, test-first.
</details>

<details>
<summary><b>Am I open to collaborating or job opportunities?</b></summary>
<br/>
Yes — especially fullstack roles in .NET and Angular. Email or LinkedIn above works.
</details>

<details>
<summary><b>What's the tech stack behind TMS, in one line?</b></summary>
<br/>
ASP.NET Core 10 (Clean Architecture, CQRS/MediatR, SignalR) talking to a zoneless Angular 22 client (signals, NgRx SignalStore), backed by Vitest + Playwright.
</details>

<details>
<summary><b>How can you support this profile?</b></summary>
<br/>
Starring the repos above helps the most — it's the strongest signal for both GitHub's discovery and anyone evaluating the work. A follow keeps you posted as new modules ship.
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
Job offers, collaboration, anything that needs a real reply.
<br/>
<a href="mailto:kaluabiyu@gmail.com">kaluabiyu@gmail.com</a>
</td>
<td align="center" width="33%">

**💼 LinkedIn**
<br/>
Professional networking and recruiter outreach.
<br/>
<a href="https://linkedin.com/in/kalu-abiyu">/in/kalu-abiyu</a>
</td>
<td align="center" width="33%">

**📸 Instagram**
<br/>
A casual hello, or what I'm up to outside of code.
<br/>
<a href="https://instagram.com/Kalu_abi77">@Kalu_abi77</a>
</td>
</tr>
</table>

---
