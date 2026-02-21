## When using the Blender Bonsai MCP server

- ALWAYS check the layers panel before starting to work on a task in Blender. The user may have made changes to the scene by adding, removing, or hiding layers.
- ALWAYS capture a viewport screenshot (`get_user_view`) before and after making changes to confirm the result matches intent.
- Refer to `design/` docs for project context, requirements, and prior decisions before making changes.

## Design documentation

- See `design/README.md` for the design framework and how documents relate to each other.
- When making design decisions, log them in `design/decisions.md` using the ADR template defined in that file.
- Keep `design/requirements.md` updated as requirements evolve.
- Move precise, locked-in values to `design/specifications.md`.
