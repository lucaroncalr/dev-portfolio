# Portfolio Project - Piano Completo

## Overview
Portfolio professionale per **Luca Ronca - AR/VR & Web Developer**. Progetto senza deadline con milestone settimanali. Obiettivo: qualità prima della velocità.

---

## Positioning & Strategia

### Primary: AR/VR Developer
- 3 app VR/AR per clienti reali (via Layout)
- Progetti personali
- Mostrare il tuo ruolo specifico anche se part di team

### Secondary: Full-Stack Web
- 1 progetto Blazor online (team)
- Nuovo cliente in arrivo: gestionale + timbratrice (CASE STUDY futuro)

### Il Differenziale
**Easter egg minigiochi nel portfolio** = mostra creatività + interattività oltre il solito

---

## Tech Stack Definitivo

| Layer | Tecnologie |
|-------|-----------|
| **Frontend** | HTML/CSS/Vanilla JS |
| **Backend** | .NET (ASP.NET Core Minimal APIs) |
| **Database** | RavenDB (containerizzato con Docker) |
| **Orchestration** | Docker Compose (locale) |
| **Hosting** | Railway (piano gratuito, con Docker) |
| **Admin** | Username/Password (easter egg nella home) |

### Database Schema
```
Collections:
- Lavori
  ├─ id
  ├─ titolo
  ├─ descrizione
  ├─ tecnologie[]
  ├─ link (se online)
  ├─ image
  └─ categoria (game/web)
  
- TechStack
  ├─ id
  ├─ nome
  ├─ categoria (language/framework/tool)
  └─ icona/colore
  
- Contatti (from form)
  ├─ id
  ├─ nome
  ├─ email
  ├─ messaggio
  └─ timestamp
```

---

## Setup & Development

### Locale (Docker)
```bash
# Avvia sia backend che RavenDB in container
docker-compose up

# Backend: http://localhost:5000
# RavenDB Studio: http://localhost:8080
```

**Flusso locale:**
- `docker-compose.yml` → Backend .NET + RavenDB
- Sviluppa e testa in container

### Deploy (Railway)
- Same Docker setup → Railway detecta `docker-compose.yml`
- Backend + RavenDB containerizzati
- Un unico push = deployment completo

---

## Struttura Progetto

```
dev-portfolio/
├─ README.md
├─ .gitignore
│
├─ frontend/
│  ├─ index.html
│  ├─ admin.html (easter egg)
│  ├─ css/
│  │  ├─ base.css
│  │  ├─ theme-gaming.css (per dopo)
│  │  └─ theme-web.css (per dopo)
│  ├─ js/
│  │  ├─ main.js
├─ docker-compose.yml (Backend .NET + RavenDB)
├─ Dockerfile (Backend .NET)
└─ .env (variabili DB, secrets
│  │  ├─ theme-switcher.js
│  │  └─ admin.js
│  └─ minigames/
│     ├─ game/
│     │  ├─ index.html
│     │  ├─ styles/
│     │  └─ scripts/
│     └─ .../ 
│
├─ backend/
│  ├─ Program.cs
│  ├─ Models/
│  │  ├─ Lavoro.cs
│  │  ├─ TechStack.cs
│  │  └─ Contatto.cs
│  ├─ Services/
│  │  ├─ LavoriService.cs
│  │  └─ TechStackService.cs
│  └─ Data/
│     └─ RavenDbContext.cs
│
└─ .env (variabili RavenDB Cloud + Railway, non committare)
```

---

## MILESTONE 1: MVP (Fine Settimana Prossima)

### Cosa Entra
- ✅ Hero impactful
- ✅ Projects grid con filtri [Tutto/Game/Web]
- ✅ Tech stack: grid di badge/icone + tooltip
- ✅ 3 minigiochi integrati (Runner + Bullet Hell + Arkanoid)
- ✅ Form contatti (invia a backend)
- ✅ Backend base (.NET API minimal)
- ✅ RavenDB connection
- ✅ Admin panel semplice (aggiungi/modifica progetti)
- ✅ 1 tema visibile (Gaming-focused)

### Cosa NON Entra
- ❌ Skill tree SVG
- ❌ Secondo tema web
- ❌ Deploy su Railway (solo test locale)
- ❌ Feature avanzate

### Timeline Milestone 1
```
Giorno 1-2: Setup progetto + Frontend structure
├─ Cartelle, file base
├─ HTML layout Milestone 1
└─ CSS base.css

Giorno 3: Backend API + Database
├─ .NET project setup
├─ RavenDB connection
└─ API endpoints (GET /projects, GET /techstack, POST /contacts)

Giorno 4-5: Frontend-Backend Integration
├─ JS per caricare dati da API
├─ Form contatti funzionante
└─ Integrazione minigiochi

Giorno 6-7: Testing + Fix
├─ Test dei flussi principali
├─ Bug fix
└─ Deploy locale (non Railway ancora)
```

---

## MILESTONE 2: Skill Tree (Settimana Dopo)

### Cosa Entra
- Converti tech stack in skill tree SVG
- Connessioni dinamiche tra skills
- Hover effects impactful
- Contextual (mostra solo skills per categoria)

---

## MILESTONE 3+: Polish & Evolution

### Opzioni Future
- Tema "web"
- Skill tree SVG con connessioni dinamiche
- Admin panel avanzato
- Deploy su Railway
- Blog per case study
- Video showcase progetti
- Altro in base a cosa emergerà

---

## Hero Section - Opzioni

### Opzione A: Full Height Focus
```
┌─────────────────────┐
│                     │
│    [CLAIM]          │
│                     │
│    [CTA Button]     │
│                     │
│ (background con     │
│  parallax leggero)  │
└─────────────────────┘
```
Semplice, diretto, professionale.

### Opzione B: Compact + Animazione
```
┌─────────────────────┐
│ Claim + CTA + Icon  │
│ (altura ridotta)    │
│ (animation entry)   │
└─────────────────────┘
```
Veloce, moderno, porta ai progetti.

### Opzione C: Interattiva (TBD)
Aspetta di capire meglio l'idea.

---

## TODO Prima di Domani

### Contenuto (30 min)
- [ ] Descrizione breve 2-3 progetti VR/AR
- [ ] Descrizione Blazor project online
- [ ] Bio personale (2-3 righe)
- [ ] Claim principale (una frase per hero)

### Design (30 min)
- [ ] Scegli Hero option (A, B, o C con descrizione)
- [ ] Disegna wireframe semplice della homepage

### Progetto (30 min)
- [ ] Decidi nome repo: `portfolio` o `lucaronca`
- [ ] Crea cartella `portfolio` locale
- [ ] Inizializza git

### Optional
- [ ] Crea repo GitHub
- [ ] Setup Railway account (se non hai già)

---

## Principi di Sviluppo

- **Architettura prima di codice**: Pensa prima, scrivi dopo
- **MVP definito**: Milestone 1 è fisso, non aggiungere scope
- **Qualità prima della velocità**: No deadline = fai le cose bene
- **Documenta mentre sviluppi**: Commenti + README
- **Orgoglio del risultato**: Deve rappresentarti davvero

---

## FAQ / Decisioni Importanti

**Q: Quando lo metto online?**
A: Fine Milestone 1 (fine settimana prossima). Su Railway + dominio.

**Q: Che dominio usi?**
A: Da decidere. Opzioni: `lucaronca.dev`, `luca.dev`, o simile.

**Q: E il vecchio portfolio repo?**
A: Rinomina in `portfolio-archived` su GitHub. Crea repo nuova `lucaronca` per il progetto.

**Q: Password admin dove la metto?**
A: Hidden easter egg nella home (cliccabile). Username/password sono fissi nel frontend (non è production, è solo showcase).

**Q: Se non finisco Milestone 1 in 7 giorni?**
A: No problem, no deadline. Ma prova a finire con quella scadenza per avere feedback.

**Q: Come uso i 3 minigiochi nel portfolio?**
A: - Runner: nella sezione "Projects" (easter egg click)
- Bullet Hell: nella sezione "Tech Stack" (easter egg click)
- Arkanoid: nel footer o landing interattiva (easter egg click)

---

## Note Finali

- Questo è **un vero progetto** di cui essere orgoglioso
- Non è "veloce", è **fatto bene**
- Le milestone sono flessibili ma aiutano a non procrastinare
- Focus: MVP online, poi evolvi incrementalmente
- **Il portfolio È il tuo primo case study**: mostra come pensi, come scrivi codice, come architetturi

---

**Prossimo step: Domani iniziamo con HTML structure.**

Good luck! 🚀
