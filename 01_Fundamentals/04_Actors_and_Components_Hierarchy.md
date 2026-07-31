---
title: "04 Actors & Components Hierarchy"
category: "01_Fundamentals"
type: "lesson"
tags: [ue5, 01_Fundamentals, lesson, obsidian-vault, encyclopedia]
updated: 2026-07-31
---

# 04 Actors & Components Hierarchy

> [!NOTE]
> **Category**: 01_Fundamentals | **Type**: lesson | **Status**: Complete Technical Documentation

---

## What is it?
Actors are container objects in the world, while Components (StaticMeshComponent, AudioComponent, LightComponent) define an Actors visual representation, physics, audio, and behavior.

## Why it exists
Promotes composition over inheritance. Rather than building monolithic classes, features are assembled by combining modular components.

## When to use it
Building any interactive or visual object in Unreal Engine.

## Real Game Examples
Character Actor containing SkeletalMeshComponent, CameraComponent, SpringArmComponent, and CharacterMovementComponent.

## Step-by-Step Implementation & Tutorial
1. Create a new Blueprint Class inheriting from Actor. 2. Add Root Component (e.g. SceneComponent or StaticMeshComponent). 3. Add sub-components under the Root. 4. Access components in C++ using CreateDefaultSubobject.

## Visual Explanation & Architecture
> [!TIP]
> *Visual Diagram Reference*: Blueprint graph flow, Material node layout, or Viewport hierarchy diagram.

`mermaid
graph TD
    A[Initialization / Trigger] --> B[Processing / System Evaluation]
    B --> C[Execution / Output / State Update]
`

## Best Practices
Always set a SceneComponent as Root if the Actor has no primary mesh.

## Common Mistakes & Pitfalls
Adding unnecessary components that increase tick overhead.

## Performance Considerations
Uncheck Can Ever Tick on components that do not require frame updates.

## Mini Challenge
Build a light fixture actor with Mesh, SpotLight, and Audio components.

## Quiz & Self-Check
Q: What is the base class for components that have a 3D transform? A: USceneComponent.

## Summary
Composition via components makes UE5 actors modular and maintainable.

---

## Official Epic Documentation & Community Resources
- [Unreal Engine Official Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/)
- **YouTube Creators**: Epic Games Developer Community, Mathew Wadstein, Ryan Laley, Unreal Sensei, PrismaticaDev, Smart Poly, LeafBranchGames, Virtus Learning Hub.
- **Community References**: Epic Developer Forums, Unreal Engine Subreddit (/r/unrealengine), GitHub Unreal Engine Source Repository.