---
title: "01 PBR Workflow (Base Color, Roughness, Metallic)"
category: "05_Materials"
type: "lesson"
tags: [ue5, 05_Materials, lesson, obsidian-vault, encyclopedia]
updated: 2026-07-31
---

# 01 PBR Workflow (Base Color, Roughness, Metallic)

> [!NOTE]
> **Category**: 05_Materials | **Type**: lesson | **Status**: Complete Technical Documentation

---

## What is it?
Physically Based Rendering (PBR) models light interaction with surfaces using realistic physical inputs: Base Color, Metallic, Specular, Roughness, Normal, and Ambient Occlusion.

## Why it exists
Ensures materials look consistent and accurate under any lighting condition or environment.

## When to use it
Authoring any 3D asset material in Unreal Engine 5.

## Real Game Examples
Realistic metals, rusted iron, wet stone, polished wood in AAA games.

## Step-by-Step Implementation & Tutorial
1. Open Material Editor. 2. Connect Texture Sample (RGB) to Base Color. 3. Connect Packed ORM Texture: R -> Ambient Occlusion, G -> Roughness, B -> Metallic. 4. Connect Normal Map to Normal input.

## Visual Explanation & Architecture
> [!TIP]
> *Visual Diagram Reference*: Blueprint graph flow, Material node layout, or Viewport hierarchy diagram.

`mermaid
graph TD
    A[Initialization / Trigger] --> B[Processing / System Evaluation]
    B --> C[Execution / Output / State Update]
`

## Best Practices
Keep Roughness values between 0.05 and 0.95; non-metals have 0.0 Metallic.

## Common Mistakes & Pitfalls
Setting Metallic to intermediate values like 0.5 for non-metallic surfaces.

## Performance Considerations
Pack Occlusion, Roughness, and Metallic into a single ORM texture (RGB) to save texture samplers.

## Mini Challenge
Create a wet mud material that blends Roughness dynamically using a Scalar Parameter.

## Quiz & Self-Check
Q: What value should Metallic be for plastic or wood? A: 0.0.

## Summary
PBR standardizes surface shading across Base Color, Roughness, Metallic, and Normal inputs.

---

## Official Epic Documentation & Community Resources
- [Unreal Engine Official Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/)
- **YouTube Creators**: Epic Games Developer Community, Mathew Wadstein, Ryan Laley, Unreal Sensei, PrismaticaDev, Smart Poly, LeafBranchGames, Virtus Learning Hub.
- **Community References**: Epic Developer Forums, Unreal Engine Subreddit (/r/unrealengine), GitHub Unreal Engine Source Repository.