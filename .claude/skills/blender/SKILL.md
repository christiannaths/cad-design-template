---
name: blender
description: Use when working with Blender and the Bonsai MCP server to create, modify, or inspect IFC building elements.
user-invocable: false
---

# Blender / Bonsai MCP

## Before starting any task

ALWAYS check the layers panel before starting to work on a task in Blender, the user may have made changes to the scene by adding, removing, or hiding layers.

## IFC-first workflow

This project has an active IFC model managed by Bonsai. When creating or modifying objects in Blender:

1. **Always create objects as IFC entities** — use `bpy.ops.bim.assign_class()` or the ifcopenshell API to create properly classified IFC elements, not plain Blender mesh objects.
2. **Use the correct IFC classification** — columns are `IfcColumn`, beams/rails are `IfcBeam`, slabs are `IfcSlab`, structural framing members are `IfcMember`, and assemblies are `IfcElementAssembly`.
3. **Assign to spatial structure** — new elements must be contained within the appropriate `IfcBuildingStorey` (ie "Ground Floor").
4. **Use MCP query tools for inspection** — prefer `get_ifc_total_structure`, `list_ifc_entities`, and `get_ifc_properties` over raw Blender object inspection when checking the model.

## Bonsai Python module

The Bonsai Python module is `bonsai`, not `blenderbim`. For example:

```python
import bonsai.tool as tool
ifc_file = tool.Ifc.get()
```
