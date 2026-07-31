---
title: "02 GameMode & GameState"
category: "02_Gameplay_Framework"
type: "lesson"
tags: [ue5, 02_Gameplay_Framework, lesson, obsidian-vault, encyclopedia]
updated: 2026-07-31
---

# 02 GameMode & GameState

> [!NOTE]
> **Category**: 02_Gameplay_Framework | **Type**: lesson | **Status**: Complete Technical Documentation

---

## What is it?
GameMode defines game rules, match state, win conditions, and default pawn spawning. GameState tracks match state and score replicated to all connected clients.

## Why it exists
Separates server-authoritative logic (GameMode exists ONLY on Server) from shared game state replicated to all players (GameState).

## When to use it
Configuring game match rules, scoring, match flow, and team states.

## Real Game Examples
Battle Royale match management, victory logic, timer countdowns.

## Step-by-Step Implementation & Tutorial
In C++ GameMode: Override PostLogin(APlayerController* NewPlayer) to assign teams and spawn player pawns on match start.

## Visual Explanation & Architecture
> [!TIP]
> *Visual Diagram Reference*: Blueprint graph flow, Material node layout, or Viewport hierarchy diagram.

`mermaid
graph TD
    A[Initialization / Trigger] --> B[Processing / System Evaluation]
    B --> C[Execution / Output / State Update]
`

## Best Practices
Never store client-accessible variables in GameMode because GameMode does NOT exist on clients.

## Common Mistakes & Pitfalls
Trying to read GameMode on client machines resulting in nullptr.

## Performance Considerations
Keep GameState replication tight; use RPCs or fast arrays for large player counts.

## Mini Challenge
Set up a GameMode that spawns a custom Character class on match start.

## Quiz & Self-Check
Q: Does GameMode exist on multiplayer clients? A: No, GameMode exists strictly on the Server.

## Summary
GameMode enforces match rules on server; GameState replicates match data to all clients.

---

## Official Epic Documentation & Community Resources
- [Unreal Engine Official Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/)
- **YouTube Creators**: Epic Games Developer Community, Mathew Wadstein, Ryan Laley, Unreal Sensei, PrismaticaDev, Smart Poly, LeafBranchGames, Virtus Learning Hub.
- **Community References**: Epic Developer Forums, Unreal Engine Subreddit (/r/unrealengine), GitHub Unreal Engine Source Repository.