---
title: "01 UObject & AActor Architecture"
category: "02_Gameplay_Framework"
type: "lesson"
tags: [ue5, uobject, aactor, architecture]
---
# 01 UObject & AActor Architecture

## What is it?
UObject is the base class for all Unreal Engine object types offering garbage collection, reflection, serialization, and network replication. AActor inherits from UObject and is the base class for any object that can be spawned into a level world.

## Why it exists
Separates pure data/logic objects (UObject) from objects that possess 3D transform and can exist in a game world (AActor).

## Step-by-Step Implementation & Tutorial
`cpp
// C++ AActor Spawn Example
FActorSpawnParameters SpawnParams;
SpawnParams.Owner = ThisActor;
APawn* NewPawn = GetWorld()->SpawnActor<APawn>(PawnClass, SpawnLocation, SpawnRotation, SpawnParams);
`

`mermaid
graph TD
    UObject --> AActor
    AActor --> APawn
    APawn --> ACharacter
    AActor --> AInfo
    AInfo --> AGameModeBase
`

## Performance Considerations
Actors carry network overhead and transform hierarchy; use UObject or lightweight structs for pure data tasks.