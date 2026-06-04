# Luca Ronca - Dev Portfolio 🚀

Professional portfolio for **Luca Ronca** - AR/VR & Full-Stack Web Developer.

> Quality over speed. A real project to be proud of.

---

## 🎯 Overview

This portfolio showcases three main aspects:

1. **AR/VR Developer** - Real client apps + personal projects
2. **Full-Stack Web** - Web applications with .NET/ASP.NET
3. **Creativity** - Interactive easter eggs to show personality and skills beyond the ordinary

---

## 🛠️ Tech Stack

| Layer | Technologies |
|-------|-----------|
| **Frontend** | HTML/CSS/Vanilla JS |
| **Backend** | .NET (ASP.NET Core Minimal APIs) |
| **Database** | RavenDB (containerized with Docker) |
| **Orchestration** | Docker Compose |
| **Hosting** | Railway |
| **Admin** | Username/Password |

---

## Getting Started

### Prerequisites
- [.NET 8.0+](https://dotnet.microsoft.com/download)
- [Docker](https://www.docker.com/products/docker-desktop) & Docker Compose

### Local Development

```bash
# Start both backend and RavenDB in containers
docker-compose up

# Backend runs on http://localhost:5000
# RavenDB Studio available at http://localhost:8080
```

Access the frontend files directly or serve them via the backend.

---

## Project Structure

```
dev-portfolio/
├─ frontend/
│  ├─ index.html (hero + projects grid + tech stack)
│  ├─ admin.html (admin panel - easter egg)
│  ├─ css/
│  │  ├─ base.css
│  │  ├─ theme-gaming.css
│  │  └─ theme-web.css
│  ├─ js/
│  │  ├─ main.js
│  │  ├─ api.js
│  │  ├─ theme-switcher.js
│  │  └─ admin.js
│  └─ minigames/
│     ├─ runner/
│     ├─ bullet-hell/
│     └─ arkanoid/
│
├─ backend/
│  ├─ Program.cs
│  ├─ Models/ (Lavoro, TechStack, Contatto)
│  ├─ Services/ (LavoriService, TechStackService)
│  ├─ Data/ (RavenDbContext)
│  └─ PortfolioBackend.csproj
│
├─ docker-compose.yml (Backend .NET + RavenDB)
├─ Dockerfile (Backend containerization)
├─ .env (secrets - not committed)
│
├─ docs/
│  └─ PORTFOLIO_PLAN.md (full plan & milestones)
│
└─ README.md
```

---

## Mini Games

Three interactive easter eggs integrated into the portfolio:

- **Runner** 
- **Bullet Hell**  
- **Arkanoid**  
- More mini games TBD

---

## Milestones

### Milestone 1: MVP ✅
- Impactful hero + projects grid with filters
- Tech stack badges + tooltips
- 3 mini games integrated
- Backend API (.NET + RavenDB)
- Working contact form
- Simple admin panel
- Gaming theme
- **Due**: End of next week

### Milestone 2: Skill Tree
- Tech stack → Skill Tree SVG
- Dynamic connections between skills
- Impactful hover effects

### Milestone 3+: Evolution
- Web theme
- Advanced admin panel
- Deploy to Railway
- Blog for case studies
- Video showcase

---

## Home
- Hero section with impactful statement
- Projects grid with filters (All/Game/Web)
- Tech stack section with badges and tooltips
- Contact form (name, email, message)
- Easter egg hints for mini games
- Theme switcher (gaming/web)
- Footer with social links

## Admin Panel 

Access `/admin.html` with fixed username/password (see `.env`).

Features:
- Add/edit projects
- Add/edit tech stack
- View received contacts

---

## Development Principles

- **Architecture before code**: Think first, code after
- **Defined MVP**: Milestone 1 is fixed, no scope creep
- **Quality over speed**: No deadline
- **Document as you develop**: Comments + README
- **Pride in the result**: Must truly represent who I am as a developer

---

## Reference

- [Full Plan](docs/PORTFOLIO_PLAN.md) - Complete milestone, timeline, and design details
- [RavenDB Docs](https://ravendb.net/docs)
- [ASP.NET Core Minimal APIs](https://learn.microsoft.com/aspnet/core/fundamentals/minimal-apis)

---

## About

**Luca Ronca**  
AR/VR Developer | Full-Stack Web Developer  
[LinkedIn](#) | [GitHub](#) | [Website](#)

---

*This is my first full case study: it shows how I think, how I code, and how I architect projects.*
