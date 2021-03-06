# MCFood

## Importing the class

It might be required for you to import the package if you encounter any issues (like casting an Array), so better be safe than sorry and add the import at the very top of the file.
```zenscript
import crafttweaker.api.food.MCFood;
```


## Constructors

No Description Provided
```zenscript
new MCFood(healing as int, saturation as float) as MCFood
```

| Parameter  | Type  | Description             |
| ---------- | ----- | ----------------------- |
| healing    | int   | No Description Provided |
| saturation | float | No Description Provided |



## Methods

### addEffect

Return Type: [MCFood](/vanilla/api/food/MCFood)

```zenscript
MCFood.addEffect(effect as MCPotionEffectInstance, probability as float) as MCFood
```

| Parameter   | Type                                                                  | Description             |
| ----------- | --------------------------------------------------------------------- | ----------------------- |
| effect      | [MCPotionEffectInstance](/vanilla/api/potions/MCPotionEffectInstance) | No Description Provided |
| probability | float                                                                 | No Description Provided |


### clearEffects

Return Type: void

```zenscript
MCFood.clearEffects() as void
myMCFood.clearEffects();
```

### removeEffect

Return Type: [MCFood](/vanilla/api/food/MCFood)

```zenscript
MCFood.removeEffect(effect as MCPotionEffectInstance) as MCFood
```

| Parameter | Type                                                                  | Description             |
| --------- | --------------------------------------------------------------------- | ----------------------- |
| effect    | [MCPotionEffectInstance](/vanilla/api/potions/MCPotionEffectInstance) | No Description Provided |


### setCanEatWhenFull

Return Type: [MCFood](/vanilla/api/food/MCFood)

```zenscript
MCFood.setCanEatWhenFull(canEatWhenFull as boolean) as MCFood
```

| Parameter      | Type     | Description             |
| -------------- | -------- | ----------------------- |
| canEatWhenFull | boolean型 | No Description Provided |


### setFastEating

Return Type: [MCFood](/vanilla/api/food/MCFood)

```zenscript
MCFood.setFastEating(fastEating as boolean) as MCFood
```

| Parameter  | Type     | Description             |
| ---------- | -------- | ----------------------- |
| fastEating | boolean型 | No Description Provided |


### setHealing

Return Type: [MCFood](/vanilla/api/food/MCFood)

```zenscript
MCFood.setHealing(healing as int) as MCFood
```

| Parameter | Type | Description             |
| --------- | ---- | ----------------------- |
| healing   | int  | No Description Provided |


### setMeat

Return Type: [MCFood](/vanilla/api/food/MCFood)

```zenscript
MCFood.setMeat(meat as boolean) as MCFood
```

| Parameter | Type     | Description             |
| --------- | -------- | ----------------------- |
| meat      | boolean型 | No Description Provided |


### setSaturation

Return Type: [MCFood](/vanilla/api/food/MCFood)

```zenscript
MCFood.setSaturation(saturation as float) as MCFood
```

| Parameter  | Type  | Description             |
| ---------- | ----- | ----------------------- |
| saturation | float | No Description Provided |



## Properties

| 名称             | Type     | Has Getter | Has Setter |
| -------------- | -------- | ---------- | ---------- |
| canEatWhenFull | boolean型 | true       | false      |
| healing        | int      | true       | false      |
| isFastEating   | boolean型 | true       | false      |
| meat           | boolean型 | true       | false      |
| saturation     | float    | true       | false      |

