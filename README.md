# 🚀 DEV-CORE: Unified Operations & Financial Intelligence Suite

![Dashboard Preview](assets/dashboard_preview.png)

## 🌟 Overview

**DEV-CORE** is a high-performance, modular internal management platform designed for modern business operations. It unifies financial intelligence, client relationship management (CRM), and core administrative control into a single, cohesive ecosystem.

---

## 🛠 Modular Architecture

The system is split into three primary modules, each designed with a high-speed **FastAPI** backend and a responsive, **Vanilla JavaScript** frontend.

### 🛡 1. CORE_SYSTEM (The Hub)
The central nervous system of the platform.
- **Role**: Handles authentication, user management, and global data orchestration.
- **Tech**: FastAPI, SQLite, Caddy Reverse Proxy.
- **Entry Point**: `CORE_SYSTEM/run.sh` (Ports: 8000/3000)

### 💰 2. Finance Management (Intelligence)
A sophisticated engine for tracking the pulse of the business.
- **Role**: Real-time budget flow, transaction auditing, and financial reporting.
- **Features**: Interactive charts, income/expense tracking, and audit logs.
- **Entry Point**: `Finance/run.sh` (Ports: 8001/3001)

### 👥 3. Client Management (CRM)
Streamlined relationship tracking and project status management.
- **Role**: Centralized client database, project milestones, and interaction logs.
- **Features**: Dynamic client profiles and real-time status updates.
- **Entry Point**: `Client_manageent/run.sh` (Ports: 8000/3000 - Standalone)

---

## 🚀 Getting Started

### Prerequisites
- **Python 3.10+**: Core engine.
- **Virtualenv**: For dependency isolation.
- **Caddy**: (Optional) For production-grade domain mapping.

### Quick Start (Unified Mode)
To launch the entire suite with automated database initialization:
```bash
cd CORE_SYSTEM
chmod +x run.sh
./run.sh
```

---

## ⚙️ Tech Stack & Integration

| Layer | Technology | Purpose |
| :--- | :--- | :--- |
| **Backend** | Python / FastAPI | High-concurrency API performance |
| **Frontend** | HTML5 / CSS3 / Vanilla JS | No-build, lightning-fast UI loading |
| **Database** | SQLite / SQLAlchemy | Reliable, zero-config persistence |
| **Security** | JWT / Password Hashing | Robust user authentication |
| **Proxy** | Caddy | Production-ready SSL & Routing |

---

## 📁 Project Structure

```text
.
├── CORE_SYSTEM/          # Administrative & Authentication Hub
│   ├── api/              # Python Backend
│   └── web/              # Dashboard Frontend
├── Finance/              # Financial Analytics Module
│   ├── backend/          # Analytics Engine
│   └── frontend/         # Financial UI
└── Client_manageent/     # CRM & Relationship Module
    ├── backend/          # CRM API
    └── frontend/         # Client UI
└── assets/               # Branding & Documentation Assets
```

---

## 🔑 Default Credentials

> [!IMPORTANT]
> These are the default credentials initialized by the system. It is highly recommended to change these immediately after the first login.

| Role | Username | Password | Access Level |
| :--- | :--- | :--- | :--- |
| **System Root** | `root` | `root123` | Full Access (Global) |
| **IT Administrator** | `admin_it` | `it123` | IT & Server Management |
| **Finance Manager** | `finance_mgr` | `fin123` | Financial & Salary Records |

### Initialization
If the database is not yet initialized, run the following command to create these users:
```bash
curl -X POST http://localhost:8000/users/init-root
```

---

## 🛠 Installation & API Docs

Initial setup is handled via the `CORE_SYSTEM/api/seed.py` and `seed_real.py` scripts. Use the `/users/init-root` endpoint (automatically called by `run.sh`) to establish primary system access.

| Resource | URL |
| :--- | :--- |
| **Unified API Docs** | `http://localhost:8000/docs` |
| **Finance API Docs** | `http://localhost:8001/docs` |
| **Client Manager Docs** | `http://localhost:8000/docs` |



---

**© 2024 DEV-CORE Operations. All rights reserved.**
