---
title: "01 Ocean Mystery Game Design & Production Bible"
category: "40_Portfolio_Projects"
type: "production_bible"
tags: [ue5, gdd, ocean-mystery, portfolio, architecture]
---
# Ocean Mystery - Comprehensive Production Bible

> [!IMPORTANT]
> **Project Type**: AAA Open-World Survival Mystery
> **Target Engine**: Unreal Engine 5.5+
> **Rendering Pipeline**: Lumen, Nanite, Water System, Chaos Physics

---

## 1. Narrative & World Vision
Set in an uncharted oceanic archipelago after an apocalyptic anomaly. Players must build rafts, dive into abyssal ruins, research alien monoliths, and survive dynamic storms.

## 2. Core Gameplay Systems & Technical Architecture
1. **Buoyancy & Ocean System**:
   - Integrated UE WaterBodyOcean with Chaos Physics Buoyancy Component.
   - Gerstner wave surface sampling for custom actor physics.
2. **Crafting & Modular Raft Building**:
   - Socket-based snap building system with grid projection.
   - Resource inventory system backed by Data Tables (DT_CraftingRecipes).
3. **Oxygen & Diving Mechanics**:
   - Sub-surface swimming state Machine in Character Movement Component.
   - Depth pressure damage model calculated via World Position Z.
4. **Dynamic Atmosphere & Weather**:
   - Volumetric cloud density modulation via Curve Assets (UCurveFloat).
   - Exponential Height Fog density ramping during storm events.

## 3. Blueprint & C++ Hybrid Architecture
`mermaid
graph TD
    A[AOceanGameModeBase] --> B[APlayerController_Ocean]
    B --> C[ACharacter_Explorer]
    C --> D[UHealthComponent]
    C --> E[UOxygenComponent]
    C --> F[UInventoryComponent]
    G[WaterBodyOcean] --> C
`

## 4. Optimization & Release Roadmap
- **Nanite Culling**: Enable Nanite on all environmental rock and coral meshes.
- **RVT Layering**: Terrain texturing using Runtime Virtual Textures to minimize draw calls.
- **Save State Serialization**: Async SaveGame writing to avoid frame hitches.

---
## Summary
Ocean Mystery serves as the ultimate portfolio centerpiece demonstrating mastery over UE5 graphics, physics, C++, Blueprints, and world building.