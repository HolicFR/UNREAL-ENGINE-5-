---
title: "02 UCLASS, USTRUCT, UPROPERTY & UFUNCTION Macros"
category: "04_CPP"
type: "lesson"
tags: [ue5, cpp, uproperty, ufunction, macros]
---
# 02 UCLASS, USTRUCT, UPROPERTY & UFUNCTION Macros

## What is it?
Unreal Engine macro system that marks C++ classes, structs, variables, and functions for UnrealHeaderTool (UHT) reflection.

## Step-by-Step Implementation & Tutorial
`cpp
UCLASS(Blueprintable, ClassGroup=(Custom), meta=(BlueprintSpawnableComponent))
class MYGAME_API UHealthComponent : public UActorComponent
{
    GENERATED_BODY()

public:
    UPROPERTY(EditAnywhere, BlueprintReadWrite, Category="Health", meta=(ClampMin="0.0"))
    float MaxHealth = 100.0f;

    UFUNCTION(BlueprintCallable, Category="Health")
    void TakeDamage(float DamageAmount);
};
`
"@

# ----------------------------------------------------
# 05 MATERIALS
# ----------------------------------------------------
Write-Note "05_Materials/00_Index.md" @"
---
title: "05 Materials Engine Hub"
type: hub
tags: [ue5, materials, hub]
---
# ðŸ“‚ 05 Materials Engine Hub

> [!IMPORTANT]
> [[TUTORIAL|Root TUTORIAL]] -> **05 Materials Engine**

- [[05_Materials/01_PBR_Workflow_Metallic_Roughness|01 PBR Workflow (Base Color, Roughness, Metallic)]]
- [[05_Materials/02_Master_Materials_and_Material_Instances|02 Master Materials & Material Instances]]
- [[05_Materials/03_UV_Coordinates_Panning_Rotation|03 UV Coordinates, Panning & Rotators]]
- [[05_Materials/04_Runtime_Virtual_Textures_RVT|04 Runtime Virtual Textures (RVT)]]
- [[05_Materials/05_Material_Node_Encyclopedia|05 Material Node Encyclopedia]]