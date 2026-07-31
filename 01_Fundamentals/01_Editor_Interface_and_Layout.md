---
title: "01 Editor Interface and Layout"
category: "01_Fundamentals"
type: "lesson"
tags: [ue5, editor, viewport, toolbar]
---
# 01 Editor Interface and Layout

## What is it?
The Unreal Engine 5 Editor Interface is the primary graphical user workspace where game developers assemble levels, configure actors, manage assets, and preview gameplay in real-time.

## Why it exists
It provides a unified, highly customizable environment that brings together rendering, physics, scripting, animation, and asset management into a single real-time toolchain.

## When to use it
Always. It is the core workbench for building UE5 games and applications.

## Real Game Examples
- **Fortnite**: Level assembly, world layout, real-time testing.
- **The Matrix Awakens**: Large-scale city layout and viewport management.

## Step-by-Step Implementation & Tutorial
1. **Viewport Navigation**:
   - RMB + WASD: Flythrough camera mode.
   - LMB + Drag: Orbit / Move forward and backward.
   - Alt + RMB: Smooth zoom.
2. **Transform Modes**:
   - W: Location Translate Tool.
   - E: Rotation Tool.
   - R: Scale Tool.
3. **Viewport Modes**:
   - Lit (Alt + 4): Full lighting with Lumen and reflections.
   - Unlit (Alt + 3): Flat colors, useful for geometry alignment.
   - Wireframe (Alt + 2): Polygon mesh overview.
   - Shader Complexity (Alt + 8): Shader cost diagnostic view.

## Visual Explanation Placeholder
> [!TIP]
> *Viewport Reference*: Top toolbar contains Play In Editor (PIE), Selection Modes, and Settings.

`mermaid
graph TD
    A[Main Toolbar] --> B[3D Viewport]
    B --> C[Outliner]
    B --> D[Details Panel]
    A --> E[Content Drawer]
`

## Best Practices
- Save custom window layouts for different tasks (e.g., Level Design vs Blueprint Scripting).
- Keep snapping settings active (Grid Snap, Rotation Snap, Scale Snap).

## Common Mistakes & Pitfalls
- Moving source files outside the Content Browser causing broken asset paths.

## Performance Considerations
- Reduce Viewport Scalability settings during high-density editing if GPU usage spikes.

## Mini Challenge
Customize your UE5 editor layout and save a preset named "Master Workspace".

## Quiz & Self-Check
- **Q**: What shortcut toggles between Lit and Unlit view modes?
- **A**: Alt + 4 (Lit) and Alt + 3 (Unlit).

## Summary
The UE5 Editor Interface is the command center for building games, organizing assets, and adjusting real-time rendering.

---
## Official Epic Documentation & Community Resources
- ðŸ“˜ [Unreal Engine Editor Interface Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-editor-user-interface)