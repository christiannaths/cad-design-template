# Design Framework

This directory contains the design documentation for the project. The approach is lightweight and iterative, borrowing from established frameworks — design briefs, Architecture Decision Records (ADRs), and Volere fit criteria — without the overhead of any single formal system.

## Documents

### `requirements.md` — Design Brief

Project context, goals, constraints, functional requirements, and open questions. Structured like a design brief with inspiration from Volere's "fit criteria" concept: each requirement should ideally include how you'd verify it's been met.

### `decisions.md` — Decision Log

A chronological log of design decisions in ADR (Architecture Decision Record) style. Each entry captures the context, options considered, the chosen direction, and consequences. See the template in that file.

### `specifications.md` — Specifications

Precise, measurable values that emerge as requirements solidify: dimensions, materials, tolerances, part numbers. This is what you'd hand to a fabricator or use to generate a BOM. Created when the project matures past early requirements.

### `references/` — Supporting Materials

Datasheets, photos, sketches, links, and research notes. Organize by topic or by the decision they support.

## Guidelines

- **Requirements are living** — update them as research answers open questions or constraints change.
- **Decisions are append-only** — don't edit old entries. If a decision is reversed, add a new entry that supersedes the original.
- **Move precise values to specifications** once they're locked in. Requirements describe _what_ and _why_; specifications describe the exact _how much_.
- **Keep references organized** by topic or by the decision they support.
