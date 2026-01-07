# 📅 Simple Bulletin Board Project Schedule & Classification

## 1. Project Overview
- **Goal**: Implement the simplest form of a bulletin board (CRUD).
- **Duration**: 3 Days (Sprint)
- **Team**:
  - **PM/Leader**: @유재석 (Overall coordination, Deployment)
  - **Frontend / Team Leader**: @박명수 (UI/UX, Client logic, Team Mgmt)
  - **Frontend**: @노홍철 (UI Components, Styling)
  - **Backend**: @정준하 (API, Database)

---

## 2. Work Breakdown Structure (WBS)

### 📌 Common / Setup (Day 1 Morning)
| ID | Task | Assignee | Description |
|----|------|----------|-------------|
| C-01| Git Repository Init | @유재석 | Initialize Git, .gitignore setup |
| C-02| Tech Stack Decision | Team | FE: React (Vite), BE: Express (Node.js), DB: PostgreSQL |
| C-03| API Specification | Team | Define API endpoints for CRUD |

### 🎨 Frontend (FE) - Frontend Team (@박명수, @노홍철)
| ID | Task | Phase | Description |
|----|------|-------|-------------|
| F-01| Project Scaffold | Day 1 | Init project (CRA/Vite), Router setup |
| F-02| UI Layout | Day 1 | Header, Footer, Main Layout |
| F-03| Post List Page | Day 2 | Fetch & Display posts (Table/Card view) |
| F-04| Post Detail Page | Day 2 | View single post content |
| F-05| Write/Edit Page | Day 2 | Forms for creating/updating posts |
| F-06| Integration | Day 3 | Connect with Real API |

### 🛠 Backend (BE) - @정준하
| ID | Task | Phase | Description |
|----|------|-------|-------------|
| B-01| Server Init | Day 1 | Server selection, Basic setup |
| B-02| DB Schema | Day 1 | Define Post table (id, title, content, author, date) |
| B-03| API Implementation | Day 2 | GET /posts, GET /posts/:id, POST /posts, PUT, DELETE |
| B-04| CORS & Error Handling| Day 2 | Allow FE connection, basic error responses |
| B-05| Testing | Day 3 | API Testing (Postman/Swagger) |

---

## 3. Daily Schedule

### 📆 Day 1: Setup & Design
- **Morning**: Kick-off, Git init, Choose Stack.
- **Afternoon**: 
  - FE: Basic Routing & Layout.
  - BE: DB Schema & Server “Hello World”.

### 📆 Day 2: Development (Core)
- **Morning**: 
  - FE: Post List UI.
  - BE: Create & Read APIs.
- **Afternoon**:
  - FE: Write/Edit UI.
  - BE: Update & Delete APIs.

### 📆 Day 3: Integration & Polish
- **Morning**:
  - Integrate FE with BE.
  - Fix CORS issues.
- **Afternoon**:
  - Final QA.
  - Readme update.
  - Deploy (Optional).
