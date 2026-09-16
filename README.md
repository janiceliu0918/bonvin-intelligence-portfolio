# Bonvin Intelligence Platform — Public Portfolio

A public case study of an internal business intelligence and applied-AI platform built for a Canadian wine & spirits importer/distributor.

The production repository remains private. This portfolio focuses on **product thinking, architecture, business workflows, data engineering, and controlled AI access** without publishing credentials or secrets.

## What I built

The platform brings together product search, pricing and margin logic, inventory, purchase orders, reporting, cross-market comparison, and an authenticated AI assistant.

**Stack:** React · FastAPI · Python · SQL · Supabase/PostgreSQL · AWS · GitHub Actions · Playwright · LLM Tool Calling · MCP / RAG

## Product walkthrough

1. **BC Product Search** — unified commercial lookup.
2. **Alberta Product Search** — parallel cross-market search.
3. **Price Compare** — side-by-side commercial comparison.
4. **Pricing & Margin Calculator** — reusable business rules instead of repeated spreadsheet work.
5. **Inventory** — structured operational lookup.
6. **Reports & Downloads** — validated reporting artifacts.
7. **PO Margin Dashboard** — PO status plus commercial analysis.
8. **Ask Bonvin AI** — grounded answers through approved business tools.
9. **Secure Workspace** — authenticated internal access.

## Architecture

```text
External business / regulatory sources
                |
                v
      Scheduled ingestion
   Playwright + GitHub Actions
                |
                v
       Validation / staging
                |
                v
      Supabase / PostgreSQL
        /       |        \
       /        |         \
      v         v          v
 FastAPI     MCP tools   Reporting
 services    (read-only)  workflows
      \         |          /
       \        |         /
        +--------+--------+
                 |
                 v
          React workspace
                 |
        +--------+--------+
        |                 |
        v                 v
 Business users      Ask Bonvin AI
```

## Engineering decisions

- Keep reusable business/query logic outside prompts.
- Use controlled, read-oriented AI tools rather than arbitrary database access.
- Validate and reconcile ingestion so stale or incomplete source data fails visibly.
- Migrate progressively from validated pricing/Streamlit workflows to React + FastAPI.
- Document architecture, testing, deployment, and handoff for maintainability.

## Public site

The repository includes an `index.html` portfolio landing page intended for GitHub Pages. Full-size product screenshots are presented individually rather than compressed into a collage.

**Role:** Intelligence Coordinator / internal product builder  
**Focus:** Business systems · analytics engineering · applied AI · workflow automation
