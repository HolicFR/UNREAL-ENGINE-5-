---
title: "01 Lab: Interactive Door System"
category: "39_Labs"
type: "lab"
---
# 01 Lab: Interactive Door System

## Lab Objective
Build an interactive door actor using Blueprint timeline interpolation, vector math, and Blueprint Interface inputs.

## Step-by-Step Build
1. Create BP_Door Actor with StaticMeshComponent (Frame) and StaticMeshComponent (DoorMesh).
2. Add BoxCollision for interaction detection.
3. Implement Timeline node feeding Lerp (Rotator) into SetRelativeRotation on DoorMesh.
4. Trigger rotation on player interaction keypress.