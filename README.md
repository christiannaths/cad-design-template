# CAD Design Template

A project template for AI-assisted CAD and design work using **Claude Code** + **Blender** + **Bonsai BIM**.

Claude Code connects to Blender through an MCP (Model Context Protocol) server, giving it the ability to view, create, and modify IFC building models directly. The `design/` directory provides a structured framework for requirements, decisions, and specifications — giving Claude (and you) a shared source of truth for the project.

## Prerequisites

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) — Anthropic's CLI for Claude
- [Blender](https://www.blender.org/) (4.x+)
- [Bonsai BIM](https://bonsaibim.org/) — Blender add-on for IFC/BIM modeling
- [uv](https://docs.astral.sh/uv/) — Python package manager (used to run the MCP server)

## Setup

1. **Create a new repo from this template** (or clone it directly)

2. **Clone the Bonsai MCP server** into the project:
   ```sh
   git clone https://github.com/JotaDeRodriguez/Bonsai_mcp blender/Bonsai_mcp
   ```

3. **Start Blender and enable Bonsai**:
   - Open Blender
   - Go to Edit > Preferences > Add-ons, enable the Bonsai add-on
   - In the Bonsai panel, start the MCP server

4. **Run Claude Code** in the project root:
   ```sh
   claude
   ```
   The Bonsai MCP tools should be available automatically — Claude can view and modify the Blender scene.

## Project structure

```
├── CLAUDE.md              # AI assistant instructions
├── .mcp.json              # MCP server configuration
├── blender/
│   ├── Bonsai_mcp/        # Cloned MCP server (gitignored)
│   └── scripts/           # Project-specific Blender scripts
├── design/
│   ├── README.md          # Design framework documentation
│   ├── requirements.md    # Project requirements / design brief
│   ├── decisions.md       # Decision log (ADR style)
│   ├── specifications.md  # Precise values, materials, tolerances
│   └── references/        # Datasheets, photos, research notes
└── exports/               # IFC exports, drawings, budgets
```

## Design framework

See [`design/README.md`](design/README.md) for documentation on the design framework — how requirements, decisions, and specifications relate to each other and how to use them effectively.
