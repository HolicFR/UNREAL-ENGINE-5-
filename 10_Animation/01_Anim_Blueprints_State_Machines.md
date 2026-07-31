---
title: "01 Anim Blueprints & State Machines"
category: "10_Animation"
type: "lesson"
tags: [ue5, 10_Animation, lesson, obsidian-vault, encyclopedia]
updated: 2026-07-31
---

# 01 Anim Blueprints & State Machines

> [!NOTE]
> **Category**: 10_Animation | **Type**: lesson | **Status**: Complete Technical Documentation

---

## What is it?
Animation Blueprints (AnimBP) evaluate character pose graphs using Event Graphs (reading speeds/states) and Anim Graphs (State Machines, Blend Spaces).

## Why it exists
Drives character animation transitions dynamically based on speed, direction, jumping, falling, and combat states.

## When to use it
Controlling character skeletal mesh animations during gameplay.

## Real Game Examples
Locomotion transitions: Idle -> Walk -> Run -> Jump -> Fall -> Land.

## Step-by-Step Implementation & Tutorial
1. Create AnimBP targeting Character Skeleton. 2. Event Graph: Read TryGetPawnOwner -> Get Velocity -> Calculate Speed. 3. AnimGraph: Add State Machine node -> Output to Final Pose. 4. In State Machine: Create states (Idle, Run, Jump) and draw transitions with boolean rules.

## Visual Explanation & Architecture
> [!TIP]
> *Visual Diagram Reference*: Blueprint graph flow, Material node layout, or Viewport hierarchy diagram.

`mermaid
graph TD
    A[Initialization / Trigger] --> B[Processing / System Evaluation]
    B --> C[Execution / Output / State Update]
`

## Best Practices
Use Fast Path in AnimBP (avoid complex Blueprint node logic inside AnimGraph execution).

## Common Mistakes & Pitfalls
Casting and searching for components inside AnimGraph instead of caching variables in Event Graph.

## Performance Considerations
AnimBP Fast Path optimizes pose evaluations natively in C++.

## Mini Challenge
Build a State Machine handling Idle, Walk, Run, and Jump states.

## Quiz & Self-Check
Q: Where should variable reading take place in an AnimBP? A: In the Event Graph (BlueprintThreadSafeUpdateAnimation).

## Summary
AnimBP and State Machines evaluate skeletal poses continuously during gameplay.

---

## Official Epic Documentation & Community Resources
- [Unreal Engine Official Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/)
- **YouTube Creators**: Epic Games Developer Community, Mathew Wadstein, Ryan Laley, Unreal Sensei, PrismaticaDev, Smart Poly, LeafBranchGames, Virtus Learning Hub.
- **Community References**: Epic Developer Forums, Unreal Engine Subreddit (/r/unrealengine), GitHub Unreal Engine Source Repository.