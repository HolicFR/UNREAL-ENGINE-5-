---
title: "01 Replication, RPCs & Network Roles"
category: "17_Multiplayer"
type: "lesson"
tags: [ue5, 17_Multiplayer, lesson, obsidian-vault, encyclopedia]
updated: 2026-07-31
---

# 01 Replication, RPCs & Network Roles

> [!NOTE]
> **Category**: 17_Multiplayer | **Type**: lesson | **Status**: Complete Technical Documentation

---

## What is it?
Unreal Engine multiplayer uses an authoritative Server-Client model. Variables replicate Server -> Client (Replicated / ReplicatedUsing). RPCs (Remote Procedure Calls) send function execution calls between Client and Server.

## Why it exists
Guarantees server authority, anti-cheat validation, and network state synchronization.

## When to use it
Building multiplayer games.

## Real Game Examples
Health replication, weapon firing RPCs, player movement prediction.

## Step-by-Step Implementation & Tutorial
In C++: Mark variables UPROPERTY(ReplicatedUsing=OnRep_Health) and declare UFUNCTION(Server, Reliable) for server RPCs.

## Visual Explanation & Architecture
> [!TIP]
> *Visual Diagram Reference*: Blueprint graph flow, Material node layout, or Viewport hierarchy diagram.

`mermaid
graph TD
    A[Initialization / Trigger] --> B[Processing / System Evaluation]
    B --> C[Execution / Output / State Update]
`

## Best Practices
All gameplay-critical decisions (taking damage, buying items) MUST occur on Server.

## Common Mistakes & Pitfalls
Executing damage calculations on client machines.

## Performance Considerations
Use Unreliable RPCs for frequent cosmetic inputs; Reliable for critical state changes.

## Mini Challenge
Implement a replicated Health variable with an OnRep notify updating player UI.

## Quiz & Self-Check
Q: Can a Client directly replicate a variable value to the Server? A: No, variable replication is strictly Server -> Client.

## Summary
Server authority controls game state; RPCs and replication sync data across clients.

---

## Official Epic Documentation & Community Resources
- [Unreal Engine Official Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/)
- **YouTube Creators**: Epic Games Developer Community, Mathew Wadstein, Ryan Laley, Unreal Sensei, PrismaticaDev, Smart Poly, LeafBranchGames, Virtus Learning Hub.
- **Community References**: Epic Developer Forums, Unreal Engine Subreddit (/r/unrealengine), GitHub Unreal Engine Source Repository.