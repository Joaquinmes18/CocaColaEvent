# Coca-Cola Event Intelligence 🥤📊

> **Plataforma Phygital para la Gestión, Trazabilidad en Tiempo Real y Analítica con IA para Eventos de Coca-Cola.**

---

## 📌 Documentación del Proyecto

👉 **[docs/ — Documentación funcional y técnica (fuente de verdad)](./docs/README.md)**

| Tema | Documento |
|------|-----------|
| Visión, alcance y KPIs | [docs/01-vision-y-alcance.md](./docs/01-vision-y-alcance.md) |
| Lógica de negocio (reglas `BR-xxx`, estados) | [docs/02-logica-de-negocio.md](./docs/02-logica-de-negocio.md) |
| Historias de usuario (`US-xxx`) | [docs/03-historias-de-usuario.md](./docs/03-historias-de-usuario.md) |
| Arquitectura backend NestJS por capas | [docs/04-arquitectura-backend-nestjs.md](./docs/04-arquitectura-backend-nestjs.md) |
| Arquitectura frontend React | [docs/05-arquitectura-frontend-react.md](./docs/05-arquitectura-frontend-react.md) |
| Modelo de datos (Prisma) | [docs/06-modelo-de-datos.md](./docs/06-modelo-de-datos.md) |
| Contratos de API | [docs/07-contratos-api.md](./docs/07-contratos-api.md) |
| WhatsApp e IA | [docs/08-whatsapp-e-ia.md](./docs/08-whatsapp-e-ia.md) |
| Seguridad y privacidad | [docs/09-seguridad-y-privacidad.md](./docs/09-seguridad-y-privacidad.md) |
| Analítica y Power BI | [docs/10-analitica-power-bi.md](./docs/10-analitica-power-bi.md) |
| Roadmap y backlog | [docs/11-roadmap-y-backlog.md](./docs/11-roadmap-y-backlog.md) |
| Guía de desarrollo | [docs/12-guia-de-desarrollo.md](./docs/12-guia-de-desarrollo.md) |
| Decisiones de arquitectura (ADR) | [docs/13-decisiones-de-arquitectura.md](./docs/13-decisiones-de-arquitectura.md) |

La idea original del producto se conserva en [COCA_COLA_EVENT_INTELLIGENCE.md](./COCA_COLA_EVENT_INTELLIGENCE.md). Cuando difiere de `docs/`, **prevalece `docs/`** (ver ADRs).

---

## 🚀 Stack Tecnológico

* **Frontend (Admin Dashboard + PWA Staff):** React 18 + TypeScript + Vite, React Router, TanStack Query, Tailwind CSS + shadcn/ui, `vite-plugin-pwa`, lector QR `@zxing/browser`.
* **Backend:** NestJS 11 (TypeScript) con arquitectura por capas (domain / application / infrastructure / presentation), BullMQ + Redis para colas y jobs.
* **Base de Datos:** PostgreSQL 16 + Prisma.
* **Canal Conversacional:** Meta WhatsApp Business Cloud API (Twilio como alternativa).
* **Inteligencia Artificial:** OpenAI Whisper (Speech-to-Text) + GPT-4o-mini (Structured Outputs).
* **Business Intelligence:** Vistas SQL en esquema `analytics` + Microsoft Power BI (DirectQuery / Import).
* **Monorepo:** pnpm workspaces + Turborepo (`apps/api`, `apps/web`, `packages/contracts`).

---

## 📋 Módulos Principales

1. **Onboarding & Ticket Digital (WhatsApp):** Registro conversacional sin descargar apps, consentimiento explícito y pase QR firmado.
2. **Control de Ingreso & Antifraude (PWA Staff):** Escaneo < 1 s con semáforo, check-in (con modo offline) y sampling con límite de canjes garantizado en base de datos.
3. **Audio-to-Insights (IA):** Nota de voz post-evento → transcripción + sentimiento, intención de compra y temas → cupón según política.
4. **Dashboard en vivo & Power BI:** Métricas en tiempo real (SSE) y vistas de asistencia, recurrencia, engagement, sentimiento e intención de compra.

---

## ⚡ Inicio rápido

Ver [docs/12-guia-de-desarrollo.md](./docs/12-guia-de-desarrollo.md#3-setup-local).
