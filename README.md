<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:512BD4,100:DD0031&height=180&section=header&text=Kalu%20Abiyu&fontSize=48&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Fullstack%20.NET%20%2B%20Angular%20Developer&descAlignY=58&descSize=18" width="100%"/>

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=800&color=512BD4&center=true&vCenter=true&width=650&lines=Building+TMS+%E2%80%94+ASP.NET+Core+10+%2B+Angular+22;Clean+Architecture+%7C+CQRS+%2F+MediatR+%7C+SignalR;Debugging+the+Identity+handshake+%E2%80%94+M10;Designing+PMAFS+%E2%80%94+Pharmacy+Stock+Finder+for+Addis+Ababa;NgRx+SignalStore+%7C+Zoneless+Angular+%7C+Reactive+Forms;Always+learning%2C+always+shipping." alt="Typing SVG" />
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
- 💊 Designing **PMAFS (Pharmacy Medicine Availability Finding System)** — location-aware pharmacy stock platform for Addis Ababa
- 📍 Based in Addis Ababa, Ethiopia
- ⚡ Right now: on **Module 10 (full-stack auth integration)** — traced the HttpOnly `tms_auth` cookie + antiforgery (XSRF) handshake through a chain of real bugs across both repos (missing `[ApiVersion]` attribute, a route missing its literal `v`, an XSRF header-name typo, `@Service()` used instead of `@Injectable()`), confirmed the corrected flow with a diagnostic call to `AuthService.login()`, and am now building the real `LoginComponent` and `/login` route that the app is still missing

---

## 🚀 Featured Projects

<details open>
<summary><b>🎓 Training Management System (TMS)</b> — click to collapse</summary>
<br/>

Fullstack training/course enrollment platform for a fictional training institution (CTBE).

| Layer | Highlights |
|---|---|
| **API** | ASP.NET Core 10, EF Core 10, PostgreSQL — layered Clean Architecture (Domain/Application/Infrastructure/Api), CQRS with MediatR, FluentValidation, HATEOAS, versioned REST endpoints, RFC 9457 ProblemDetails |
| **Real-time** | SignalR typed hubs for enrollment/transcript notifications, async request-reply pattern for long-running work with idempotency keys |
| **Client** | Angular 22, standalone components, zoneless change detection, signals, NgRx SignalStore, reactive forms, `@defer` blocks with Angular Material — including an instructor analytics dashboard with a live Approved/Pending/Rejected chart |
| **Auth** | HttpOnly auth cookie + antiforgery (XSRF) handshake between API and client — backend flow verified end-to-end; wiring up the client-side `LoginComponent` next |

**Repos:**
[![TmsApi](https://img.shields.io/badge/TmsApi-181717?style=flat-square&logo=github)](https://github.com/kaluabiyu-wq/TmsApi)
[![tms-clients2](https://img.shields.io/badge/tms--clients2-181717?style=flat-square&logo=github)](https://github.com/kaluabiyu-wq/tms-clients2)
[![TmsCore](https://img.shields.io/badge/TmsCore-181717?style=flat-square&logo=github)](https://github.com/kaluabiyu-wq/TmsCore)
[![tms-client](https://img.shields.io/badge/tms--client-181717?style=flat-square&logo=github)](https://github.com/kaluabiyu-wq/tms-client)


</details>

<details>
<summary><b>💊 PMAFS — Pharmacy Medicine Availability Finding System</b> — click to expand</summary>
<br/>

Location-aware platform to find medicine availability across pharmacies in Addis Ababa, using sub-city/woreda location data. A parallel, independent project mirroring the TMS curriculum structure.

- Relational database design — inventory freshness, reliability scoring, location-aware search
- ASP.NET Core API scaffolding
- Service interface architecture
- A TypeScript/Node.js client exploring TypeScript 7.0, discriminated unions with the Temporal API, and Angular reactive forms

**Repos:**
[![PMFApi](https://img.shields.io/badge/PMFApi-181717?style=flat-square&logo=github)](https://github.com/kaluabiyu-wq/PMFApi)
[![PMFCore](https://img.shields.io/badge/PMFCore-181717?style=flat-square&logo=github)](https://github.com/kaluabiyu-wq/PMFCore)
[![Pmf-Client](https://img.shields.io/badge/Pmf--Client-181717?style=flat-square&logo=github)](https://github.com/kaluabiyu-wq/Pmf-Client)

</details>

---

## 🛠️ Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=cs,dotnet,postgres,angular,ts,git,html,css&theme=dark" />
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

**Frontend**
![Angular](https://img.shields.io/badge/-Angular-DD0031?style=flat&logo=angular&logoColor=white)
![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![NgRx](https://img.shields.io/badge/-NgRx%20SignalStore-BA2BD2?style=flat)
![RxJS](https://img.shields.io/badge/-RxJS-B7178C?style=flat&logo=reactivex&logoColor=white)

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
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=kaluabiyu-wq&repo=TmsApi&theme=tokyonight&hide_border=true" width="48%"/>
</a>
<a href="https://github.com/kaluabiyu-wq/tms-clients2">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=kaluabiyu-wq&repo=tms-clients2&theme=tokyonight&hide_border=true" width="48%"/>
</a>
<a href="https://github.com/kaluabiyu-wq/PMFApi">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=kaluabiyu-wq&repo=PMFApi&theme=tokyonight&hide_border=true" width="48%"/>
</a>

</div>

---

## ❓ FAQ

<details>
<summary><b>What am I currently learning?</b></summary>
<br/>
Module 10 — full-stack auth integration. I've built the HttpOnly cookie + antiforgery handshake between the ASP.NET Core API and the Angular client, tracked down the routing and configuration bugs that were breaking it (a missing API version attribute, a route missing its literal "v", an XSRF header-name typo, a wrong Angular decorator), and confirmed the corrected flow works end-to-end. Next up: the actual <code>LoginComponent</code> and <code>/login</code> route, since the app currently has no real login UI wired to it.
</details>

<details>
<summary><b>Am I open to collaborating or job opportunities?</b></summary>
<br/>
Yes — I'm particularly interested in fullstack roles working with .NET and Angular. Feel free to reach out via email or LinkedIn above.
</details>

<details>
<summary><b>What's the tech stack behind TMS, in one line?</b></summary>
<br/>
ASP.NET Core 10 API (Clean Architecture + CQRS/MediatR + SignalR) talking to an Angular 22 zoneless client (signals + NgRx SignalStore).
</details>

<details>
<summary><b>How can you support this profile?</b></summary>
<br/>
Starring the repos above is the biggest help — it's the single strongest signal for both GitHub's discovery algorithm and anyone evaluating the work. A follow keeps you posted as new modules ship.
</details>

---

## 📊 GitHub Stats

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=kaluabiyu-wq&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" width="49%"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=kaluabiyu-wq&layout=compact&theme=tokyonight&hide_border=true" width="30%"/>

<img src= "https://streak-stats.demolab.com/?user=kaluabiyu-wq&theme=tokyonight&hide_border=true" width="49%"/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=kaluabiyu-wq&theme=tokyo-night&hide_border=true" width="100%"/>

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
