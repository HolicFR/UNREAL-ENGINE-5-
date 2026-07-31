---
title: "02 Content Browser & Asset Management"
category: "01_Fundamentals"
type: "lesson"
tags: [ue5, content-browser, assets, redirectors]
---
# 02 Content Browser & Asset Management

## What is it?
The Content Browser (and Content Drawer Ctrl + Space) is UE5's file management hub for importing, creating, organizing, and referencing assets.

## Why it exists
It manages UAsset files and dependencies safely within the Unreal Engine reflection and reference system.

## When to use it
For creating, importing, organizing, filtering, and renaming game assets.

## Step-by-Step Implementation & Tutorial
1. Press Ctrl + Space to toggle Content Drawer.
2. Use standard directory naming:
   - BP_ for Blueprints
   - M_ for Materials
   - MI_ for Material Instances
   - T_ for Textures
   - SM_ for Static Meshes
3. Right-click folder -> **Fix Up Redirectors in Folder** after moving or deleting assets.

## Performance Considerations
Unresolved redirectors bloat asset dependency trees and increase load times.