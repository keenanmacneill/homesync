# **HomeSync**  
*A modular full‑stack household life‑management platform.*

## **✨ Features** (Coming Soon)

### **Unified Household Operations**
HomeSync consolidates multiple life‑management domains into one platform:

- **Credit Card Benefits** — Track credit card benefits, usage, reset cycles, and expiring credits.  
- **Chores** — Recurring tasks, assignments, completion history, and supply notes.  
- **Movies** — Shared watchlist with ratings, platform tags, and watched status.  
- **Workouts** — Log exercises, sets, reps, RPE, PRs, routines, deload logic, and progress photos.  
- **Lawn Care** — Mowing, fertilizing, herbicide logs, weather‑based mowing windows, and lawn photos.  
- **Car Maintenance** — Vehicles, mileage‑based tasks, due dates, and manufacturer schedule ingestion.  
- **Cat Care** — Feeding, litter, meds, vet visits, weight tracking, photos, and supply inventory.

## **🤖 AI‑Powered Enhancements** (Coming Soon)

HomeSync includes an integrated AI assistant for:

- Smart recommendations (chores, workouts, lawn care, car maintenance).  
- Credit card category optimization (“Which card should I use for this purchase?”).  
- Auto‑generated schedules and reminders.  
- Document ingestion (PDFs, screenshots) to populate maintenance schedules, workout templates, etc.  
- Purchase suggestions with links.

## **📄 Document Ingestion** (Coming Soon)

A Python microservice parses:

- Car maintenance schedules  
- Workout templates  
- Lawn care product instructions  
- Vet documents  

Extracted data becomes structured entries in the database.

## **🧱 Architecture** (Coming Soon)

### **Tech Stack**
**Frontend:** React, TypeScript, React Router, React Query, MUI  
**Backend:** Node.js, Express, TypeScript, Python ingestion service  
**Database:** PostgreSQL (Raspberry Pi or cloud)  
**Infra:** Docker Compose (dev), containerized deployment (Render/Fly.io/EC2)  
**Auth:** JWT (access + refresh), password‑based login  
**Storage:** S3‑compatible bucket for photos & uploads  

## **🏛️ Architectural Style** (Coming Soon)

HomeSync is a **modular monolith** with:

- A shared core (auth, users, households, notifications, AI, ingestion).  
- Independent domain modules:
  - Credit Cards  
  - Chores  
  - Movies  
  - Workouts  
  - Lawn Care  
  - Car Maintenance  
  - Cat Care  
  - Media  

Each module follows consistent patterns for controllers, services, repositories, and SQL migrations.

## **🗄️ Database Overview** (Coming Soon)

Each module includes its own tables. Examples:

### **Credit Cards**
- `cards`  
- `card_benefits`  
- `benefit_usage`  

### **Chores**
- `chores`  
- `chore_assignments`  
- `chore_history`  

### **Workouts**
- `workouts`  
- `workout_sets`  
- `workout_photos`  

### **Lawn Care**
- `lawn_profiles`  
- `lawn_events`  
- `lawn_weather_cache`  

### **Car Maintenance**
- `vehicles`  
- `vehicle_maintenance`  
- `vehicle_docs`  

### **Cat Care**
- `cats`  
- `cat_events`  
- `cat_supplies`  
- `cat_photos`  

## **🧭 API Structure** (Coming Soon)

Base URL: `/api/v1`

Example modules:

### **Auth**
- `POST /auth/register`  
- `POST /auth/login`  
- `POST /auth/refresh`  

### **Chores**
- `GET /chores`  
- `POST /chores`  
- `POST /chores/:id/complete`  

### **Credit Cards**
- `GET /cards`  
- `POST /cards/:id/benefits`  
- `POST /benefits/:id/usage`  

### **AI**
- `POST /ai/chat`  
- `POST /ai/recommendations`  

### **Document Ingestion**
- `POST /ingest/upload`  
- `GET /ingest/:id`  

## **📱 Frontend Structure** (Coming Soon)

### **Global Layout**
- Top nav: household name, user menu  
- Side nav: Dashboard, Cards, Chores, Movies, Workouts, Lawn, Vehicles, Cats  
- AI assistant panel  

### **Dashboard Highlights** (Coming Soon)
- Upcoming chores  
- Expiring card benefits  
- Car maintenance due  
- Lawn events  
- Cat tasks  
- Workout stats  
- AI suggestions  
- Recent photos  

## **🔐 Non‑Functional Requirements** (Coming Soon)

- Secure JWT auth  
- Hashed passwords  
- Role‑based household permissions  
- React Query caching  
- Graceful error handling  
- Mobile‑friendly UI  
- Extensible module pattern  

## **🚀 Development Roadmap**

### **Phase 1 — Foundation**
- Repo structure  
- Auth + households  
- PostgreSQL + migrations  
- Layout + navigation  
- Media upload service  
- Basic AI assistant  

### **Phase 2 — Core Modules**
- Chores  
- Credit cards  
- Car maintenance  
- Document ingestion (car schedules)  

### **Phase 3 — Supporting Modules**
- Movies  
- Workouts (deload logic)  
- Lawn care (weather logic)  
- Cat care (supplies + weight tracking)  

### **Phase 4 — Polish**
- Dashboard  
- Notifications  
- Demo user + seed data  
- Screenshots + demo video  
- AI recommendations across modules  

## **📦 Installation & Setup**

```bash
git clone https://github.com/yourusername/homesync
cd homesync
docker compose up --build
```

Frontend: http://localhost:3000  
Backend: http://localhost:4000  

## **📸 Screenshots** (Coming Soon)

- Dashboard  
- Credit card tracker  
- Chores  
- Workouts  
- Lawn care  
- Car maintenance  
- Cat care  
