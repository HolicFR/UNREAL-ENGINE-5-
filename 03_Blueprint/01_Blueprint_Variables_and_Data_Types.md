---
title: "01 Blueprint Variables & Data Types"
category: "03_Blueprint"
type: "lesson"
tags: [ue5, 03_Blueprint, lesson, obsidian-vault, encyclopedia]
updated: 2026-07-31
---

# 01 Blueprint Variables & Data Types

> [!NOTE]
> **Category**: 03_Blueprint | **Type**: lesson | **Status**: Complete Technical Documentation

---

## What is it?
Blueprint Variables store values (Boolean, Integer, Float, Name, String, Text, Vector, Rotator, Transform, Enum, Struct, Object Reference, Soft Reference).

## Why it exists
Enables data retention, state manipulation, and communication between nodes.

## When to use it
Storing health, ammo, speed, target references, and UI labels.

## Real Game Examples
Tracking player health (Float), ammo count (Integer), and player name (Text).

## Step-by-Step Implementation & Tutorial
1. Open Blueprint -> Variables Panel -> Click + Button. 2. Name variable CurrentHealth, set type to Float. 3. Set Default Value to 100.0. 4. Drag variable into graph as Get or Set.

## Visual Explanation & Architecture
> [!TIP]
> *Visual Diagram Reference*: Blueprint graph flow, Material node layout, or Viewport hierarchy diagram.

`mermaid
graph TD
    A[Initialization / Trigger] --> B[Processing / System Evaluation]
    B --> C[Execution / Output / State Update]
`

## Best Practices
Use Text for player-facing localized UI strings; use Name for fast internal tags.

## Common Mistakes & Pitfalls
Using String for localized UI text causing translation failure.

## Performance Considerations
Use Soft Object References for large mesh assets to prevent unintended memory load.

## Mini Challenge
Create a Player Stats Struct containing Health, Shield, Name, and Inventory Array.

## Quiz & Self-Check
Q: What variable type should be used for localized UI text? A: Text.

## Summary
Variables store game state across primitive types, structs, and object references.

---

## Official Epic Documentation & Community Resources
- [Unreal Engine Official Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/)
- **YouTube Creators**: Epic Games Developer Community, Mathew Wadstein, Ryan Laley, Unreal Sensei, PrismaticaDev, Smart Poly, LeafBranchGames, Virtus Learning Hub.
- **Community References**: Epic Developer Forums, Unreal Engine Subreddit (/r/unrealengine), GitHub Unreal Engine Source Repository.