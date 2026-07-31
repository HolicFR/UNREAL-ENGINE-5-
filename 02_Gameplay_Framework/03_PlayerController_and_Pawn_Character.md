---
title: "03 PlayerController, Pawn & Character"
category: "02_Gameplay_Framework"
type: "lesson"
tags: [ue5, 02_Gameplay_Framework, lesson, obsidian-vault, encyclopedia]
updated: 2026-07-31
---

# 03 PlayerController, Pawn & Character

> [!NOTE]
> **Category**: 02_Gameplay_Framework | **Type**: lesson | **Status**: Complete Technical Documentation

---

## What is it?
PlayerController is the human driver of an entity. Pawn is the physical in-world representation. Character is a specialized Pawn equipped with CharacterMovementComponent for bipedal navigation.

## Why it exists
Separates input/camera ownership (Controller) from physical body and movement (Pawn/Character).

## When to use it
Creating playable characters, vehicles, drones, or spectating cameras.

## Real Game Examples
Possessing a vehicle in GTA or Cyberpunk switching input from Character to Vehicle Pawn.

## Step-by-Step Implementation & Tutorial
In C++ Controller: Use Unpossess() then Possess(TargetPawn) to swap control between Character and Vehicle.

## Visual Explanation & Architecture
> [!TIP]
> *Visual Diagram Reference*: Blueprint graph flow, Material node layout, or Viewport hierarchy diagram.

`mermaid
graph TD
    A[Initialization / Trigger] --> B[Processing / System Evaluation]
    B --> C[Execution / Output / State Update]
`

## Best Practices
Keep UI and input bindings in PlayerController; keep movement execution in Character.

## Common Mistakes & Pitfalls
Hardcoding character logic inside PlayerController making vehicle possession difficult.

## Performance Considerations
CharacterMovementComponent handles complex network prediction automatically.

## Mini Challenge
Implement a possession system between a Human Character and a Drone Pawn.

## Quiz & Self-Check
Q: What component gives Character its built-in walking, flying, and swimming capabilities? A: UCharacterMovementComponent.

## Summary
Controller thinks; Pawn/Character exists and moves.

---

## Official Epic Documentation & Community Resources
- [Unreal Engine Official Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/)
- **YouTube Creators**: Epic Games Developer Community, Mathew Wadstein, Ryan Laley, Unreal Sensei, PrismaticaDev, Smart Poly, LeafBranchGames, Virtus Learning Hub.
- **Community References**: Epic Developer Forums, Unreal Engine Subreddit (/r/unrealengine), GitHub Unreal Engine Source Repository.