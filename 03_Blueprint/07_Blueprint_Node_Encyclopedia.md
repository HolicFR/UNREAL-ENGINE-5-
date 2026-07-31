---
title: "07 Master Blueprint Node Encyclopedia"
category: "03_Blueprint"
type: "encyclopedia"
tags: [ue5, blueprint, nodes, encyclopedia]
---
# Master Blueprint Node Encyclopedia

## 1. Branch
- **Exec In**: Exec line.
- **Condition**: Boolean input.
- **Outputs**: True Exec, False Exec.
- **Usage**: Evaluates conditions to branch execution flow.

## 2. Sequence
- **Exec In**: Exec line.
- **Outputs**: Then 0, Then 1, Then 2...
- **Usage**: Executes code blocks sequentially in the same frame.

## 3. ForEachLoop
- **Exec In**: Exec line.
- **Array**: Target Array.
- **Outputs**: Loop Body Exec, Array Element, Array Index, Completed Exec.
- **Usage**: Iterates through every element in an array.

## 4. LineTraceByChannel
- **Inputs**: Start (Vector), End (Vector), Trace Channel, Drivers/Params.
- **Outputs**: Out Hit (HitResult Struct), Return Value (Boolean).
- **Usage**: Casts a ray through world space to detect collisions and surfaces.

## 5. Lerp (Linear Interpolate)
- **Inputs**: A (Float/Vector), B (Float/Vector), Alpha (Float 0-1).
- **Outputs**: Result.
- **Usage**: Smoothly transitions values between point A and B based on Alpha weight.