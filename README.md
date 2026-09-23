### Hi, I'm Hari

Final-year Computer Science student. I build full-stack and AI-assisted
applications, and I care most about the parts that are invisible when they
work — transactions that hold under concurrency, authentication that survives
a stolen token, schemas that don't quietly rewrite their own history.

Currently interning at **SkillForge Technologies**.

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

- CV — [Harenthira_Ravishangar_CV.pdf](https://github.com/hari20050803-beep/hari20050803-beep/blob/main/Harenthira_Ravishangar_CV.pdf)
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
