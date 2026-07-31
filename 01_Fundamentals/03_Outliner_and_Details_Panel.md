---
title: "03 Outliner & Details Panel"
category: "01_Fundamentals"
type: "lesson"
tags: [ue5, 01_Fundamentals, lesson, obsidian-vault, encyclopedia]
updated: 2026-07-31
---

# 03 Outliner & Details Panel

> [!NOTE]
> **Category**: 01_Fundamentals | **Type**: lesson | **Status**: Complete Technical Documentation

---

## What is it?
The Outliner lists every Actor in the current level world, while the Details Panel displays and edits components, properties, and transform data for selected Actors.

## Why it exists
Provides direct control over world hierarchy, actor attachment, component properties, and editor metadata.

## When to use it
Whenever placing, searching, attaching, or tweaking properties of placed actors in a level.

## Real Game Examples
Organizing thousands of level props in Fortnite; tweaking light parameters in real-time.

## Step-by-Step Implementation & Tutorial
1. Use search bar in Outliner to filter by Actor Class or Name. 2. Create Folders in Outliner to group related props. 3. In Details Panel, lock properties or search by property name. 4. Edit Component hierarchy by dragging child components onto parent components.

## Visual Explanation & Architecture
> [!TIP]
> *Visual Diagram Reference*: Blueprint graph flow, Material node layout, or Viewport hierarchy diagram.

`mermaid
graph TD
    A[Initialization / Trigger] --> B[Processing / System Evaluation]
    B --> C[Execution / Output / State Update]
`

## Best Practices
Folder organization in Outliner is critical for team collaboration.

## Common Mistakes & Pitfalls
Leaving thousands of un-grouped actors in the Outliner root.

## Performance Considerations
Selecting huge numbers of actors simultaneously causes minor UI hitches.

## Mini Challenge
Organize a level with 50 props into 5 clean Outliner folders.

## Quiz & Self-Check
Q: How do you attach one component to another in the Details Panel? A: Drag the child component onto the desired parent component in the Component Hierarchy view.

## Summary
Outliner manages world hierarchy; Details Panel edits object properties.

---

## Official Epic Documentation & Community Resources
- [Unreal Engine Official Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/)
- **YouTube Creators**: Epic Games Developer Community, Mathew Wadstein, Ryan Laley, Unreal Sensei, PrismaticaDev, Smart Poly, LeafBranchGames, Virtus Learning Hub.
- **Community References**: Epic Developer Forums, Unreal Engine Subreddit (/r/unrealengine), GitHub Unreal Engine Source Repository.