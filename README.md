### Hi, I'm Hari

Final-year Computer Science student. I build full-stack and AI-assisted
applications, and I care most about the parts that are invisible when they
work — transactions that hold under concurrency, authentication that survives
a stolen token, schemas that don't quietly rewrite their own history.

Currently completing the **CodeAlpha Full Stack Development Internship**.

---

#### What I'm working on

**A transactional e-commerce store** — Node.js, Express 5, MySQL 8, vanilla JS.

The interesting part isn't the catalogue; it's the checkout. Two customers can
want the last unit at the same instant, and a naive read-then-write sells it
twice. So the order is placed inside one transaction with `SELECT … FOR UPDATE`
row locks, taken in a consistent id order to avoid deadlock, with the stock
guard repeated in the `UPDATE` as an independent second barrier.

Verified, not assumed: five simultaneous requests for one remaining unit
produce exactly one success and four rejections, with stock landing on zero.

The cart also carries no price field, so a tampered price isn't rejected —
it's impossible to send.

---

#### Tech I work with

| Area | Tools |
|---|---|
| **Mobile** | Flutter, Dart, Firebase (Auth, Firestore) |
| **Backend** | Node.js, Express, FastAPI, ASP.NET Core |
| **Frontend** | HTML5, CSS3, JavaScript (ES modules) |
| **Data** | MySQL, SQL Server, Firestore, ChromaDB |
| **AI** | Gemini API, RAG pipelines, vector search |
| **Testing** | Jest, Supertest, Postman / Newman |
| **Tooling** | Git, Docker, MySQL Workbench, R |

---

#### Selected projects

**MedLens AI** — a medical-document assistant
Flutter · FastAPI · Firebase · Gemini · ChromaDB
Retrieval-augmented generation over uploaded medical documents, so answers are
grounded in the user's own records rather than the model's recollection. Built
end to end: ingestion, chunking and embedding, retrieval, a patient dashboard,
then hardening and deployment.

**Learnova AI** — a study companion for students
Flutter · Firebase · Gemini
Eleven modules around a single dashboard, including AI-generated flashcards
with a flip-card study mode and a study roadmap that plans a syllabus into
sessions.

**CodeAlpha E-commerce Store** — full-stack storefront
Node.js · Express · MySQL · Vanilla JS
Catalogue with full-text search, persistent cart, transactional checkout,
order history and an admin dashboard. JWT auth with rotating refresh tokens,
a Content-Security-Policy with no `unsafe-inline`, and 143 tests.

**Event management platform** — ASP.NET Core, Entity Framework, SQL Server
A layered Web API with an MVC frontend, built to a specification rather than
to whatever compiled first.

---

#### A few things I've learned the hard way

- A `Content-Security-Policy` containing `unsafe-inline` protects almost
  nothing. Earning a strict one means writing the frontend without a single
  inline script or style attribute — and that is a refactor, not a header.
- Order lines must snapshot the product name and price at purchase time.
  Joining to the products table at read time silently rewrites your own order
  history the first time somebody changes a price.
- InnoDB's `FULLTEXT` index can detach itself after a `DELETE` plus an
  `AUTO_INCREMENT` reset, and it fails *silently* — no error, the index still
  listed, and every search quietly returning nothing.

---

#### Reach me

- Email — [hari2005.08.03@gmail.com](mailto:hari2005.08.03@gmail.com)
- LinkedIn — *add your profile URL here*

<!--
  Notes for you, invisible on the rendered profile:

  1. This file lives in a repo named exactly hari20050803-beep — same as your
     username. That is what makes GitHub render it on your profile page.
  2. Fill in the LinkedIn line above, and remove the email line if you would
     rather not publish it.
  3. As you publish each project, link its name to the repo, e.g.
     **[MedLens AI](https://github.com/hari20050803-beep/MedLens-AI)**
  4. Set your display name, bio and location in GitHub Settings > Profile -
     a README cannot set those.
-->
