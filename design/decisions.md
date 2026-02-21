# Design Decision Log

Decisions are logged as they are made in ADR (Architecture Decision Record) style. Each entry captures context, options considered, and rationale. Entries are append-only — if a decision is reversed, add a new entry that supersedes the original.

## Template

```markdown
## NNN — Title

**Status**: Proposed | Accepted | Superseded by NNN

**Context**: What situation or question prompted this decision?

**Options Considered**:
1. Option A — brief description and trade-offs
2. Option B — brief description and trade-offs

**Decision**: Which option was chosen and why.

**Consequences**: What changes as a result? Any new constraints, follow-up work, or risks?
```

---

<!-- Below is an example entry. Replace or delete it when you log your first real decision. -->

## 001 — Roofing Material

**Status**: Accepted

**Context**: The shed roof needs to be lightweight for flat-pack shipping but durable enough for year-round outdoor exposure. The design must keep total panel weight under 40 lbs for two-person handling.

**Options Considered**:
1. **Corrugated metal panels** — lightweight (~1.5 lb/sq ft), durable, simple overlap joints. Higher cost. Industrial appearance.
2. **Asphalt shingles** — low cost, familiar installation. Requires plywood decking (adds weight), not ideal for flat-pack (flexible, messy cuts).
3. **Polycarbonate panels** — very lightweight, lets in light. Less durable long-term, can yellow with UV exposure.

**Decision**: Corrugated metal panels. They meet the weight constraint without requiring decking, ship flat, and have a 25+ year lifespan. The cost premium is acceptable given the durability and simpler assembly (screw-down vs. nailing shingles over decking).

**Consequences**:
- Roof panels are self-supporting over 24" rafter spacing — no plywood decking needed
- Need rubber-washer screws to prevent leaks at fastener points
- Industrial appearance may not suit all settings — can be mitigated with color choice
