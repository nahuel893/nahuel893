<div align="center">

# Nahuel Aguirre Villafañe

**Python Developer · Backend & Data Engineering**

Salta, Argentina · Open to remote and hybrid roles

[![Email](https://img.shields.io/badge/nahuel893@hotmail.com-EA4335?style=flat-square&logo=maildotru&logoColor=white)](mailto:nahuel893@hotmail.com)
[![Open to work](https://img.shields.io/badge/Open_to_work-2ea043?style=flat-square)](mailto:nahuel893@hotmail.com)
![Location](https://img.shields.io/badge/Salta,_AR-1f1f1f?style=flat-square)

</div>

---

## About

I build backend systems and data infrastructure in Python. Three years as a data
analyst in retail and distribution taught me what the business actually needs
from a pipeline; since 2025 I've been building those systems full-time as a
developer.

My work tends to look the same regardless of the domain: an ETL that has to run
unattended at 4am, an API that another team depends on, a dimensional model that
a dashboard sits on top of. I care about the boring parts — migrations that roll
back, jobs that survive a restart, tests that fail for the right reason.

*Spanish (native) · English (professional)*

<details>
<summary><b>🇪🇸 Leer en español</b></summary>

<br>

Construyo sistemas backend e infraestructura de datos en Python. Tres años como
analista de datos en retail y distribución me enseñaron qué necesita realmente
el negocio de un pipeline; desde 2025 construyo esos sistemas full-time como
developer.

Mi trabajo se parece bastante sin importar el dominio: un ETL que tiene que
correr solo a las 4am, una API de la que depende otro equipo, un modelo
dimensional sobre el que se apoya un dashboard. Me importan las partes
aburridas — migraciones que revierten, jobs que sobreviven un reinicio, tests
que fallan por la razón correcta.

</details>

---

## Selected work

### [agents-system](https://github.com/nahuel893/agents-system) · `MIT`

Runtime platform for building and orchestrating AI agents. Agents are declared,
not coded: a role, a tool manifest and a policy — three markdown files — are
assembled by a harness into a permission-bound runtime. Generic roles live in the
platform; per-client deployments inherit, restrict or extend them without
touching core code. Ships an OpenAI-compatible endpoint so existing clients work
unchanged.

`Python 3.12` · `FastAPI` · `LangGraph` · `PostgreSQL + pgvector` · `Redis` · `Alembic`

### whatsapp-service 🔒 <sub>private</sub>

HTTP API that wraps Baileys so any application can send a WhatsApp message
without owning the Signal session. One process owns the session directory;
everything else queues. Accepted messages survive a restart (SQLite-backed
queue), every send returns a queryable job id, and delivery is paced to avoid
being flagged as a bot. Explicitly at-least-once — documented as a deliberate
trade-off, not an oversight.

`Node 24` · `Baileys` · `Express` · `node:sqlite` · `node:test` — no database or test dependencies

### medallion-etl 🔒 <sub>private · production</sub>

Production ETL for a beverage distribution company. Full Medallion architecture
— Bronze (raw), Silver (normalized), Gold (star schema) — moving Chess ERP data
into a PostgreSQL warehouse. Nine domain loaders, unified orchestrator, daily
scheduled loads, dbmate migrations. Feeds the dashboards below.

`Python` · `SQLAlchemy` · `Pydantic Settings` · `PostgreSQL` · `dbmate` · `cron`

### [chesserp-py-sdk](https://github.com/nahuel893/chesserp-py-sdk) · <sub>on PyPI</sub>

Python SDK for the ChessERP API. A base client plus nine domain services, typed
end to end with Pydantic v2. Talks to both the official REST API and the web
portal behind Spring Security, with transparent pagination and date coercion.

`Python` · `Pydantic v2` · `Requests` · `PyPI`

### [claude-dock](https://github.com/nahuel893/claude-dock)

Always-on-top desktop widget that watches Claude Code, Gemini CLI, OpenCode and
Codex sessions in real time. Live status per session, inline approval badges
driven by `PreToolUse` hooks, and a message stream.

`Electron` · `React` · `TypeScript` · `Python`

### [bank-reconciliation-arg](https://github.com/nahuel893/bank-reconciliation-arg)

Bank reconciliation ETL that reads transfer receipts sent over WhatsApp. Gemini
2.5 Flash does structured OCR on the image, the pipeline matches it against
ledger entries. Turns two to three minutes of manual entry per receipt into
seconds.

`Python` · `Flask` · `PostgreSQL` · `Google Gemini` · `Node.js`

---

### More

| Project | What it does |
|---|---|
| [excel-reporter](https://github.com/nahuel893/excel-reporter) | Modular Excel report engine over a PostgreSQL warehouse. Repository pattern, decoupled services, DB-mocked tests. |
| [fsaudit](https://github.com/nahuel893/fsaudit) | CLI that audits directory trees and reports orphans, duplicates and dead files. Metadata only — never reads contents. Read-only by design, cross-platform. |
| [sales-dashboard](https://github.com/nahuel893/sales-dashboard) | Geographic sales BI — interactive maps, temporal animation, auth with role-based access, multi-sheet Excel export. |
| [sales-forecast-ds](https://github.com/nahuel893/sales-forecast-ds) | Sales forecasting with SARIMA, Prophet and LightGBM. Lag and rolling features, experiments tracked in MLflow. |
| [steam-skins-scraper](https://github.com/nahuel893/steam-skins-scraper) | Scraper built like a service: circuit breaker, sliding-window rate limiting, connection pooling. |
| [dotfiles](https://github.com/nahuel893/dotfiles) | Hyprland, Matugen dynamic theming, AstroNvim. |

<details>
<summary><b>🇪🇸 Descripción de los proyectos en español</b></summary>

<br>

| Proyecto | Qué hace |
|---|---|
| **agents-system** | Plataforma runtime para construir y orquestar agentes de IA. Los agentes se declaran en tres archivos markdown (rol, manifiesto de tools, política) y un harness los ensambla en un runtime con permisos acotados. Los deployments por cliente heredan o restringen los roles genéricos sin tocar el core. |
| **whatsapp-service** 🔒 | API HTTP que envuelve Baileys para que cualquier app mande un WhatsApp sin ser dueña de la sesión Signal. Cola en SQLite que sobrevive reinicios, `job_id` consultable, envíos espaciados para no ser marcado como bot. At-least-once explícito y documentado. |
| **medallion-etl** 🔒 | ETL en producción para distribuidora de bebidas. Arquitectura Medallion completa (Bronze / Silver / Gold) desde Chess ERP hacia un data warehouse PostgreSQL. Nueve loaders de dominio, carga diaria automatizada, migraciones con dbmate. |
| **chesserp-py-sdk** | SDK de Python para la API de ChessERP, publicado en PyPI. Cliente base más nueve servicios de dominio, tipado con Pydantic v2, doble transporte (REST oficial y portal web) con paginación transparente. |
| **claude-dock** | Widget de escritorio always-on-top que monitorea sesiones de Claude Code, Gemini CLI, OpenCode y Codex en tiempo real, con badges de aprobación inline vía hooks `PreToolUse`. |
| **bank-reconciliation-arg** | ETL de conciliación bancaria que lee comprobantes de transferencia recibidos por WhatsApp. Gemini 2.5 Flash hace OCR estructurado y el pipeline concilia contra los asientos. De dos o tres minutos por comprobante a segundos. |
| **excel-reporter** | Motor modular de reportes Excel sobre un warehouse PostgreSQL. Repository pattern, capa de servicios desacoplada, tests con mocks de base. |
| **fsaudit** | CLI que audita árboles de directorios y reporta huérfanos, duplicados e inactivos. Solo metadata — nunca lee contenidos. Read-only por diseño y cross-platform. |
| **sales-dashboard** | BI geográfico de ventas: mapas interactivos, animación temporal, autenticación con roles y export a Excel multi-hoja. |
| **sales-forecast-ds** | Forecasting de ventas con SARIMA, Prophet y LightGBM. Features de lag y rolling, experimentos trackeados en MLflow. |
| **steam-skins-scraper** | Scraper construido como servicio: circuit breaker, rate limiting por ventana deslizante y connection pooling. |
| **dotfiles** | Hyprland, theming dinámico con Matugen, AstroNvim. |

</details>

---

## Stack

| | |
|---|---|
| **Languages** | Python · SQL · Bash · TypeScript · Lua |
| **Backend** | FastAPI · Flask · SQLAlchemy · Pydantic · Alembic |
| **Data** | PostgreSQL · pgvector · Redis · Pandas · NumPy · dbmate |
| **ML & analytics** | scikit-learn · LightGBM · Prophet · MLflow · Plotly · Jupyter |
| **AI** | LangGraph · Anthropic Claude · OpenAI · Google Gemini · Ollama |
| **Infra & tooling** | Docker · Git · GitHub Actions · Linux · pytest · Neovim |

---

<div align="center">

**Currently open to remote and hybrid opportunities**

[nahuel893@hotmail.com](mailto:nahuel893@hotmail.com)

</div>
