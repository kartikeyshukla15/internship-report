<a id="readme-top"></a>

# 💼 Pocket - Linked Accounts Management – DMP 2026 Internship Progress Report

![Internship](https://img.shields.io/badge/Internship-Mifos%20Initiative-blueviolet?style=for-the-badge)
![Duration](https://img.shields.io/badge/Duration-11%20Weeks-brightgreen?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow?style=for-the-badge)
![PRs Opened](https://img.shields.io/badge/PRs%20Opened-✔️%2011-informational?style=for-the-badge)
![Tech](https://img.shields.io/badge/Tech-Kotlin%20Multiplatform%20%7C%20Compose%20Multiplatform-orange?style=for-the-badge)

---

## 🔗 Quick Links

[![GitHub](https://img.shields.io/static/v1?style=for-the-badge&label=&message=GITHUB&color=24292e&labelColor=374151&logo=github&logoColor=white)](https://github.com/Kartikey15dem)
[![Jira](https://img.shields.io/static/v1?style=for-the-badge&label=&message=Jira&color=24292e&labelColor=374151&logo=jira&logoColor=white)](https://mifosforge.jira.com/jira/polaris/projects/MR/ideas/view/b6010bc1-0ff8-4d81-ac5c-45402016cbfd?selectedIssue=MR-16&issueViewSection=overview)
[![LinkedIn](https://img.shields.io/static/v1?style=for-the-badge&label=&message=LINKEDIN&color=0A66C2&labelColor=374151&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kartikey-shukla-655565198/)

## 📌 Description

**Pocket - Linked Accounts Management** ([Issue #1997](https://github.com/openMF/mifos-pay/issues/1997), JIRA [MR-16](https://mifosforge.jira.com/jira/polaris/projects/MR/ideas/view/b6010bc1-0ff8-4d81-ac5c-45402016cbfd?selectedIssue=MR-16&issueViewSection=overview)) is a feature developed as part of the Mifos Initiative internship project to help users organize and manage their linked financial accounts in a unified Pocket experience across **Mifos Mobile** and **Mifos Pay**.

The implementation includes a **Pocket Dashboard screen** that provides a consolidated view of linked accounts, displays aggregated balances, and groups savings, loan, and share accounts. It also includes a **Manage Pocket screen** that allows users to link and delink accounts through dedicated account-selection flows, tabs, and search functionality.

The feature includes a complete **Pocket data and repository layer** with caching and offline fallback handling, along with conflict-resolution logic between locally cached and remotely fetched Pocket data. The Pocket implementation was developed across both **mifos-mobile** and **mifos-pay** Kotlin Multiplatform codebases.

Additional functionality includes the **Smart Pocket Suggestion** feature, which prioritizes Pocket-related accounts during transactions and prompts users to add an account to their Pocket when appropriate.

To ensure reliability, the project also includes **Pocket feature tests** covering the repository, ViewModels, Pocket Dashboard screen, and Manage Pocket screen.

The feature is implemented using **Kotlin Multiplatform** and **Compose Multiplatform**, with the work covering the data layer, Pocket Dashboard, Manage Pocket, smart account suggestions, caching, offline handling, and automated tests across both applications.

---

<a id="tech-stack"></a>

## 🛠️ Tech Stack

| **Category**              | **Technology / Framework**             | **Purpose** |
|----------------------------|-----------------------------------------|-------------|
| **Language**               | Kotlin (Multiplatform)                  | Shared business logic across Android, iOS, Desktop |
| **UI Framework**           | Compose Multiplatform, Jetpack Compose  | Declarative UI for all platforms |
| **Architecture**           | MVI (Model-View-Intent)                 | Unidirectional state management with clear separation of concerns |
| **Networking**             | Ktor + Ktorfit                          | Type-safe HTTP client for the Pocket API |
| **Asynchronous Handling**  | Kotlin Coroutines + Flows               | Structured concurrency and reactive streams |
| **Local Persistence**      | Room (Multiplatform)                    | Offline fallback / caching for linked pocket accounts |
| **Testing**                | Kotlin Test, Compose Multiplatform Testing | Unit tests for repositories, ViewModels, and screens |
| **Backend**                | Apache Fineract – Pocket API            | Link/delink and retrieve linked pocket accounts |
| **Project Management**     | Jira + GitHub                           | Issue tracking, sprint planning, progress tracking |
---

<div align="right">

[![Back To Top](https://img.shields.io/badge/Back%20To%20Top-Blue?style=flat)](#readme-top)

</div>

<a id="goals--mid-point-milestone"></a>

## 🎯 Goals & Mid-Point Milestone

**Goals**

1. **View Pocket Dashboard** – See all linked accounts with aggregated balance.

2. **Link Accounts** – Add savings/loan/share accounts to the pocket.

3. **Delink Accounts** – Remove accounts from the pocket.

4. **Access Account Details** – Quick navigation to individual account details.

**Goals Achieved by Mid-Point Milestone:** Goal 1 (View Pocket Dashboard) fully delivered, with significant progress on Goals 2 (Link Accounts) and 3 (Delink Accounts).

---

<div align="right">

[![Back To Top](https://img.shields.io/badge/Back%20To%20Top-Blue?style=flat)](#readme-top)

</div>

<a id="weekly-progress"></a>

## 📅 Weekly Progress

| Week | Dates | Focus Area | Key Deliverables | PRs Opened |
|------|--------|------------|-------------------|------------|
| [1](#week-1-10th-june--13th-june) | 10–13 Jun | Design | Pocket Dashboard & Manage Pocket mockups | 0 |
| [2](#week-2-15th-june--20th-june) | 15–20 Jun | Data Layer (mifos-mobile) | Pocket Service/Repository, caching, balance aggregation | 1 |
| [3](#week-3-22nd-june--27th-june) | 22–27 Jun | Dashboard UI (mifos-mobile) | Pocket Dashboard screen with grouped account sections | 1 |
| [4](#week-4-29th-june--4th-july) | 29 Jun–4 Jul | Offline Support & Manage Pocket | Room-based offline fallback, build fixes, Manage Pocket architecture | 2 |
| [5](#week-5-6th-july--11th-july) | 6–11 Jul | Manage Pocket (mifos-mobile) | Link/Delink bottom sheets with tabs & search | 1 |
| [6](#week-6-13th-july--18th-july) | 13–18 Jul | Data Layer & Dashboard (mifos-pay) | Ported Pocket repository & dashboard screen to mifos-pay | 2 |
| [7](#week-7-20th-july--25th-july) | 20–25 Jul | Manage Pocket (mifos-pay) | Link/Delink bottom sheets for mifos-pay | 1 |
| [8](#week-8-27th-july--1st-aug) | 27 Jul–1 Aug | Conflict Resolution & Suggestions | Offline/API conflict handling, pocket account suggestion flow | 2 |
| [9](#week-9-3rd-aug--8th-aug) | 3–8 Aug | Testing (mifos-pay) | Repository, ViewModel & screen tests | 1 |
| [10](#week-10-10th-aug--15th-aug) | 10–15 Aug | Testing & Suggestions (mifos-mobile) | Repository/ViewModel/screen tests, pocket account suggestion | 2 |
| [11](#week-11-17th-aug--22nd-aug) | 17–22 Aug | Store Integration (mifos-pay) | Adopted intelligent caching via store integration | 1 |
---

<div align="right">

[![Back To Top](https://img.shields.io/badge/Back%20To%20Top-Blue?style=flat)](#readme-top)

</div>

## 📂 Detailed Weekly Progress

<a id="week-1-10th-june--13th-june"></a>

<details>
<summary>📌 Week 1 (10th – 13th June)</summary>

**Summary**

- Designed the mock UIs and design layouts for the **Pocket Dashboard** screen and **Manage Pocket** screen for the mifos-mobile app.

</details>

---

<a id="week-2-15th-june--20th-june"></a>

<details>
<summary>📌 Week 2 (15th – 20th June)</summary>

**Summary**

- Created the Pocket Service and Pocket Repository to handle essential data layers.

- Implemented the caching mechanism for linked pocket accounts within the repository layer.

- Resolved data processing details to successfully fetch and calculate balances for each distinct account type.

**Pull Requests**

- (mifos-mobile) [#3144](https://github.com/openMF/mifos-mobile/pull/3144) – feat: network layer (pocket repository)

</details>

---

<a id="week-3-22nd-june--27th-june"></a>

<details>
<summary>📌 Week 3 (22nd – 27th June)</summary>

**Summary**

- Implemented the complete Pocket Dashboard screen UI.

- Formatted the interface to display aggregated balances at the top.

- Categorized and grouped active accounts into loan, savings, and share sections.

**Pull Requests**

- (mifos-mobile) [#3145](https://github.com/openMF/mifos-mobile/pull/3145) – feat: pocket dashboard screen

</details>

---

<a id="week-4-29th-june--4th-july"></a>

<details>
<summary>📌 Week 4 (29th June – 4th July)</summary>

**Summary**

- Implemented an offline fallback framework using Room for the pocket repository, due to non-functional remote endpoints.

- Debugged and resolved build execution check failures on the pocket repository pull request.

- Initiated layout foundations and architecture setup for the Manage Pocket screen.

**Pull Requests**

- (mifos-mobile) [#3144](https://github.com/openMF/mifos-mobile/pull/3144) – feat: network layer (pocket repository)

- (mifos-mobile) [#3146](https://github.com/openMF/mifos-mobile/pull/3146) – feat: manage pocket

</details>

---

<a id="week-5-6th-july--11th-july"></a>

<details>
<summary>📌 Week 5 (6th – 11th July)</summary>

**Summary**

- Finalized the complete implementation and state flow of the Manage Pocket screen.

- Developed the Link Account bottom sheet UI, separating available accounts into dedicated tabs for loan, share, and savings, along with a real-time search utility.

- Built the Delink Account bottom sheet interaction to safely remove linked accounts.

**Pull Requests**

- (mifos-mobile) [#3146](https://github.com/openMF/mifos-mobile/pull/3146) – feat: manage pocket

</details>

---

<a id="week-6-13th-july--18th-july"></a>

<details>
<summary>📌 Week 6 (13th – 18th July)</summary>

**Summary**

- Ported the Pocket Service and Pocket Repository to **mifos-pay**, handling essential data layers and caching for linked pocket accounts.

- Ported the complete Pocket Dashboard screen UI to mifos-pay, with aggregated balances and grouped loan/savings/share sections.

**Pull Requests**

- (mifos-pay) [#2054](https://github.com/openMF/mifos-pay/pull/2054) – feat: network layer (pocket repository)

- (mifos-pay) [#2056](https://github.com/openMF/mifos-pay/pull/2056) – feat: pocket dashboard screen

</details>

---

<a id="week-7-20th-july--25th-july"></a>

<details>
<summary>📌 Week 7 (20th – 25th July)</summary>

**Summary**

- Finalized the complete implementation and state flow of the Manage Pocket screen in mifos-pay.

- Developed the Link Account bottom sheet UI with dedicated tabs for loan, share, and savings, plus a real-time search utility.

- Built the Delink Account bottom sheet interaction.

**Pull Requests**

- (mifos-pay) [#2057](https://github.com/openMF/mifos-pay/pull/2057) – feat: manage pocket

</details>

---

<a id="week-8-27th-july--1st-aug"></a>

<details>
<summary>📌 Week 8 (27th July – 1st Aug)</summary>

**Summary**

- Implemented conflict resolution strategies for the Pocket Repository to avoid ambiguity between the offline fallback and the pocket APIs, in both mifos-pay and mifos-mobile.

- Implemented the pocket account suggestion feature in mifos-pay — pocket accounts are suggested as a priority for any transaction, with a dialog prompting the user to add the selected account to their pocket if it isn't already linked.

**Pull Requests**

- (mifos-pay) [#2060](https://github.com/openMF/mifos-pay/pull/2060) – feat: pocket account suggestion

- (mifos-mobile) [#3152](https://github.com/openMF/mifos-mobile/pull/3152) – feat: conflict resolution for pocket repository

</details>

---

<a id="week-9-3rd-aug--8th-aug"></a>

<details>
<summary>📌 Week 9 (3rd – 8th Aug)</summary>

**Summary**

- Spent significant time learning how to write tests for screens, ViewModels, and repositories in Compose Multiplatform.

- Wrote tests for `PocketRepository`, `PocketDashboardViewModel`, `ManagePocketViewModel`, `PocketDashboardScreen`, and `ManagePocketScreen` in Mifos Pay.

**Pull Requests**

- (mifos-pay) [#2063](https://github.com/openMF/mifos-pay/pull/2063) – feat: pocket feature tests

</details>

---

<a id="week-10-10th-aug--15th-aug"></a>

<details>
<summary>📌 Week 10 (10th – 15th Aug)</summary>

**Summary**

- Wrote tests for `PocketRepository`, `PocketDashboardViewModel`, `ManagePocketViewModel`, `PocketDashboardScreen`, and `ManagePocketScreen` in Mifos Mobile.

- Implemented the pocket account suggestion feature for Mifos Mobile.

**Pull Requests**

- (mifos-mobile) [#3153](https://github.com/openMF/mifos-mobile/pull/3153) – feat: pocket feature tests

- (mifos-mobile) [#3154](https://github.com/openMF/mifos-mobile/pull/3154) – feat: pocket account suggestion

</details>

---

<a id="week-11-17th-aug--22nd-aug"></a>

<details>
<summary>📌 Week 11 (17th – 22nd Aug)</summary>

**Summary**

- Understood how store integration works for a feature.

- Adopted the pocket feature to leverage the store's intelligent caching layer.

**Pull Requests**

- (mifos-pay) [#2065](https://github.com/openMF/mifos-pay/pull/2065) – feat: pocket store adoption

</details>

<div align="right">

[![Back To Top](https://img.shields.io/badge/Back%20To%20Top-Blue?style=flat)](#readme-top)

</div>

<a id="key-learnings"></a>

## 📖 Key Learnings

- Building an end-to-end feature (data layer → UI → tests) across **two separate KMP codebases** (mifos-mobile and mifos-pay) from a single shared design.

- Designing an **offline-first repository layer** with Room as a fallback when remote endpoints are unavailable, and resolving conflicts between cached and live data.

- Structuring **Compose Multiplatform bottom sheets** with tabbed navigation and real-time search for account linking/delinking flows.

- Writing **unit tests for repositories, ViewModels, and Compose screens** in a Kotlin Multiplatform project.

- Implementing **context-aware account suggestions** that surface pocket accounts as transaction priorities.

- Adopting a **store-based caching layer** to make the Pocket feature's data access more intelligent and consistent across sessions.

---

<div align="right">

[![Back To Top](https://img.shields.io/badge/Back%20To%20Top-Blue?style=flat)](#readme-top)

</div>

<p align="center">

  <em>📌 This is a <strong>living blog</strong> – progress updates are continuously added.

  Click on the ▸ arrow buttons above to view weekly details.</em>

</p>
