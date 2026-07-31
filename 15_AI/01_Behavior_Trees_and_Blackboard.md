---
title: "01 Behavior Trees & Blackboard"
category: "15_AI"
type: "lesson"
tags: [ue5, 15_AI, lesson, obsidian-vault, encyclopedia]
updated: 2026-07-31
---

# 01 Behavior Trees & Blackboard

> [!NOTE]
> **Category**: 15_AI | **Type**: lesson | **Status**: Complete Technical Documentation

---

## What is it?
Behavior Trees (BT) dictate AI decision-making flow using Composites (Selector, Sequence), Tasks, Decorators, and Services. Blackboard acts as the AIs memory bank storing target actors, locations, and states.

## Why it exists
Provides a visual, hierarchical architecture for autonomous NPC logic.

## When to use it
Building enemy patrol, combat, search, and companion AI.

## Real Game Examples
Guard patrol AI searching for sound sources or chasing seen players.

## Step-by-Step Implementation & Tutorial
1. Create Blackboard asset BB_Enemy with keys: TargetActor (Object), PatrolLocation (Vector). 2. Create Behavior Tree BT_Enemy assigned to BB_Enemy. 3. Add Selector root -> Sequence (Patrol) -> Task MoveTo -> Task Wait. 4. Run BT from AIController using RunBehaviorTree(BT_Enemy).

## Visual Explanation & Architecture
> [!TIP]
> *Visual Diagram Reference*: Blueprint graph flow, Material node layout, or Viewport hierarchy diagram.

`mermaid
graph TD
    A[Initialization / Trigger] --> B[Processing / System Evaluation]
    B --> C[Execution / Output / State Update]
`

## Best Practices
Keep BT tasks modular and small (e.g. BTTask_FindRandomLocation).

## Common Mistakes & Pitfalls
Executing heavy code inside BT Service tick.

## Performance Considerations
Behavior Trees are lightweight and scale to hundreds of concurrent agents.

## Mini Challenge
Create a guard AI that patrols random points until player is seen via AIPerception.

## Quiz & Self-Check
Q: What is the purpose of the Blackboard in UE5 AI? A: It acts as the memory storage for data keys used by the Behavior Tree.

## Summary
Behavior Trees execute hierarchical decision trees while Blackboard holds state memory.

---

## Official Epic Documentation & Community Resources
- [Unreal Engine Official Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/)
- **YouTube Creators**: Epic Games Developer Community, Mathew Wadstein, Ryan Laley, Unreal Sensei, PrismaticaDev, Smart Poly, LeafBranchGames, Virtus Learning Hub.
- **Community References**: Epic Developer Forums, Unreal Engine Subreddit (/r/unrealengine), GitHub Unreal Engine Source Repository.