# MCLivingEntity

## 导入相关包

It might be required for you to import the package if you encounter any issues (like casting an Array), so better be safe than sorry and add the import at the very top of the file.
```zenscript
import crafttweaker.api.entity.MCLivingEntity;
```


## Extending MCEntity

MCLivingEntity extends [MCEntity](/vanilla/api/entity/MCEntity). That means all methods available in [MCEntity](/vanilla/api/entity/MCEntity) are also available in MCLivingEntity

## 方法

:::group{name=addPotionEffect}

Return Type: boolean

```zenscript
MCLivingEntity.addPotionEffect(effectInstanceIn as MCPotionEffectInstance) as boolean
```

| 参数                     | 类型                                                                    | 描述                      |
| ---------------------- | --------------------------------------------------------------------- | ----------------------- |
| effectInstanceIn #效果实例 | [MCPotionEffectInstance](/vanilla/api/potions/MCPotionEffectInstance) | No Description Provided |


:::

:::group{name=attackEntityAsMob}

Return Type: boolean

```zenscript
MCLivingEntity.attackEntityAsMob(entityIn as MCEntity) as boolean
```

| 参数       | 类型                                       | 描述                      |
| -------- | ---------------------------------------- | ----------------------- |
| entityIn | [MCEntity](/vanilla/api/entity/MCEntity) | No Description Provided |


:::

:::group{name=attackEntityFrom}

Return Type: void

```zenscript
MCLivingEntity.attackEntityFrom(damageSource as DamageSource, amount as float) as void
```

| 参数           | 类型                                             | 描述                      |
| ------------ | ---------------------------------------------- | ----------------------- |
| damageSource | [DamageSource](/vanilla/api/util/DamageSource) | No Description Provided |
| amount       | float                                          | No Description Provided |


:::

:::group{name=canAttack}

Return Type: boolean

```zenscript
MCLivingEntity.canAttack(target as MCLivingEntity) as boolean
```

| 参数     | 类型                                                   | 描述                      |
| ------ | ---------------------------------------------------- | ----------------------- |
| target | [MCLivingEntity](/vanilla/api/entity/MCLivingEntity) | No Description Provided |


:::

:::group{name=canAttack}

Return Type: boolean

```zenscript
MCLivingEntity.canAttack(typeIn as MCEntityType) as boolean
```

| 参数     | 类型                                                         | 描述                      |
| ------ | ---------------------------------------------------------- | ----------------------- |
| typeIn | [MCEntityType #MC实体类型](/vanilla/api/entities/MCEntityType) | No Description Provided |


:::

:::group{name=canBeRiddenInWater}

Return Type: boolean

```zenscript
MCLivingEntity.canBeRiddenInWater() as boolean
myMCLivingEntity.canBeRiddenInWater();
```

:::

:::group{name=canBreatheUnderwater}

Return Type: boolean

```zenscript
MCLivingEntity.canBreatheUnderwater() as boolean
myMCLivingEntity.canBreatheUnderwater();
```

:::

:::group{name=canEquip}

Return Type: boolean

```zenscript
MCLivingEntity.canEquip(item as MCItemDefinition) as boolean
```

| 参数   | 类型                                                     | 描述                      |
| ---- | ------------------------------------------------------ | ----------------------- |
| item | [MCItemDefinition](/vanilla/api/item/MCItemDefinition) | No Description Provided |


:::

:::group{name=clearActivePotions}

Return Type: boolean

```zenscript
MCLivingEntity.clearActivePotions() as boolean
myMCLivingEntity.clearActivePotions();
```

:::

:::group{name=getAIMoveSpeed}

Return Type: float

```zenscript
MCLivingEntity.getAIMoveSpeed() as float
myMCLivingEntity.getAIMoveSpeed();
```

:::

:::group{name=getActivePotionEffect}

Return Type: [MCPotionEffectInstance](/vanilla/api/potions/MCPotionEffectInstance)

```zenscript
MCLivingEntity.getActivePotionEffect(potionIn as MCPotionEffect) as MCPotionEffectInstance
```

| 参数       | 类型                                                    | 描述                      |
| -------- | ----------------------------------------------------- | ----------------------- |
| potionIn | [MCPotionEffect](/vanilla/api/potions/MCPotionEffect) | No Description Provided |


:::

:::group{name=getActivePotionEffects}

Return Type: Collection&lt;[MCPotionEffectInstance](/vanilla/api/potions/MCPotionEffectInstance)&gt;

```zenscript
MCLivingEntity.getActivePotionEffects() as Collection<MCPotionEffectInstance>
myMCLivingEntity.getActivePotionEffects();
```

:::

:::group{name=getActivePotionMap}

Return Type: [MCPotionEffectInstance](/vanilla/api/potions/MCPotionEffectInstance)[[MCPotionEffect](/vanilla/api/potions/MCPotionEffect)]

```zenscript
MCLivingEntity.getActivePotionMap() as MCPotionEffectInstance[MCPotionEffect]
myMCLivingEntity.getActivePotionMap();
```

:::

:::group{name=getArmorCoverPercentage}

Return Type: float

```zenscript
MCLivingEntity.getArmorCoverPercentage() as float
myMCLivingEntity.getArmorCoverPercentage();
```

:::

:::group{name=getArmorInventoryList}

Return Type: stdlib.Iterable&lt;[ItemStack](/vanilla/api/item/ItemStack)&gt;

```zenscript
MCLivingEntity.getArmorInventoryList() as stdlib.Iterable<ItemStack>
myMCLivingEntity.getArmorInventoryList();
```

:::

:::group{name=getArrowCountInEntity}

Return Type: int

```zenscript
MCLivingEntity.getArrowCountInEntity() as int
myMCLivingEntity.getArrowCountInEntity();
```

:::

:::group{name=getAttackingEntity}

Return Type: [MCLivingEntity](/vanilla/api/entity/MCLivingEntity)

```zenscript
MCLivingEntity.getAttackingEntity() as MCLivingEntity
myMCLivingEntity.getAttackingEntity();
```

:::

:::group{name=getBeeStingCount}

Return Type: int

```zenscript
MCLivingEntity.getBeeStingCount() as int
myMCLivingEntity.getBeeStingCount();
```

:::

:::group{name=getHealth}

Return Type: float

```zenscript
MCLivingEntity.getHealth() as float
myMCLivingEntity.getHealth();
```

:::

:::group{name=getHeldItemMainhand}

Return Type: [ItemStack](/vanilla/api/item/ItemStack)

```zenscript
MCLivingEntity.getHeldItemMainhand() as ItemStack
myMCLivingEntity.getHeldItemMainhand();
```

:::

:::group{name=getHeldItemOffhand}

Return Type: [ItemStack](/vanilla/api/item/ItemStack)

```zenscript
MCLivingEntity.getHeldItemOffhand() as ItemStack
myMCLivingEntity.getHeldItemOffhand();
```

:::

:::group{name=getIdleTime}

Return Type: int

```zenscript
MCLivingEntity.getIdleTime() as int
myMCLivingEntity.getIdleTime();
```

:::

:::group{name=getItemStackFromSlot}

Gets the ItemStack in the specific slot.

Return Type: [IItemStack](/vanilla/api/items/IItemStack)

```zenscript
MCLivingEntity.getItemStackFromSlot(slot as MCEquipmentSlotType) as IItemStack
```

| 参数   | 类型                                                           | 描述                      |
| ---- | ------------------------------------------------------------ | ----------------------- |
| slot | [MCEquipmentSlotType](/vanilla/api/util/MCEquipmentSlotType) | No Description Provided |


:::

:::group{name=getLastAttackedEntity}

Return Type: [MCLivingEntity](/vanilla/api/entity/MCLivingEntity)

```zenscript
MCLivingEntity.getLastAttackedEntity() as MCLivingEntity
myMCLivingEntity.getLastAttackedEntity();
```

:::

:::group{name=getLastAttackedEntityTime}

Return Type: int

```zenscript
MCLivingEntity.getLastAttackedEntityTime() as int
myMCLivingEntity.getLastAttackedEntityTime();
```

:::

:::group{name=getMaxHealth}

Return Type: float

```zenscript
MCLivingEntity.getMaxHealth() as float
myMCLivingEntity.getMaxHealth();
```

:::

:::group{name=getRevengeTarget}

Return Type: [MCLivingEntity](/vanilla/api/entity/MCLivingEntity)

```zenscript
MCLivingEntity.getRevengeTarget() as MCLivingEntity
myMCLivingEntity.getRevengeTarget();
```

:::

:::group{name=getRevengeTimer}

Return Type: int

```zenscript
MCLivingEntity.getRevengeTimer() as int
myMCLivingEntity.getRevengeTimer();
```

:::

:::group{name=getShouldBeDead}

Return Type: boolean

```zenscript
MCLivingEntity.getShouldBeDead() as boolean
myMCLivingEntity.getShouldBeDead();
```

:::

:::group{name=getTotalArmorValue}

Return Type: int

```zenscript
MCLivingEntity.getTotalArmorValue() as int
myMCLivingEntity.getTotalArmorValue();
```

:::

:::group{name=heal}

Return Type: void

```zenscript
MCLivingEntity.heal(healAmount as float) as void
```

| 参数         | 类型    | 描述                      |
| ---------- | ----- | ----------------------- |
| healAmount | float | No Description Provided |


:::

:::group{name=isAlive}

Return Type: boolean

```zenscript
MCLivingEntity.isAlive() as boolean
myMCLivingEntity.isAlive();
```

:::

:::group{name=isChild}

Return Type: boolean

```zenscript
MCLivingEntity.isChild() as boolean
myMCLivingEntity.isChild();
```

:::

:::group{name=isEntityUndead}

Return Type: boolean

```zenscript
MCLivingEntity.isEntityUndead() as boolean
myMCLivingEntity.isEntityUndead();
```

:::

:::group{name=isOnLadder}

Return Type: boolean

```zenscript
MCLivingEntity.isOnLadder() as boolean
myMCLivingEntity.isOnLadder();
```

:::

:::group{name=isPotionActive}

Return Type: boolean

```zenscript
MCLivingEntity.isPotionActive(potionIn as MCPotionEffect) as boolean
```

| 参数       | 类型                                                    | 描述                      |
| -------- | ----------------------------------------------------- | ----------------------- |
| potionIn | [MCPotionEffect](/vanilla/api/potions/MCPotionEffect) | No Description Provided |


:::

:::group{name=isPotionApplicable}

Return Type: boolean

```zenscript
MCLivingEntity.isPotionApplicable(potioneffectIn as MCPotionEffectInstance) as boolean
```

| 参数             | 类型                                                                    | 描述                      |
| -------------- | --------------------------------------------------------------------- | ----------------------- |
| potioneffectIn | [MCPotionEffectInstance](/vanilla/api/potions/MCPotionEffectInstance) | No Description Provided |


:::

:::group{name=isWaterSensitive}

Return Type: boolean

```zenscript
MCLivingEntity.isWaterSensitive() as boolean
myMCLivingEntity.isWaterSensitive();
```

:::

:::group{name=removeActivePotionEffect}

Return Type: [MCPotionEffectInstance](/vanilla/api/potions/MCPotionEffectInstance)

```zenscript
MCLivingEntity.removeActivePotionEffect(potioneffectin as MCPotionEffect) as MCPotionEffectInstance
```

| 参数             | 类型                                                    | 描述                      |
| -------------- | ----------------------------------------------------- | ----------------------- |
| potioneffectin | [MCPotionEffect](/vanilla/api/potions/MCPotionEffect) | No Description Provided |


:::

:::group{name=removePotionEffect}

Return Type: boolean

```zenscript
MCLivingEntity.removePotionEffect(effectIn as MCPotionEffect) as boolean
```

| 参数       | 类型                                                    | 描述                      |
| -------- | ----------------------------------------------------- | ----------------------- |
| effectIn | [MCPotionEffect](/vanilla/api/potions/MCPotionEffect) | No Description Provided |


:::

:::group{name=setAIMoveSpeed}

Return Type: void

```zenscript
MCLivingEntity.setAIMoveSpeed(speedIn as float) as void
```

| 参数      | 类型    | 描述                      |
| ------- | ----- | ----------------------- |
| speedIn | float | No Description Provided |


:::

:::group{name=setArrowCountInEntity}

Return Type: void

```zenscript
MCLivingEntity.setArrowCountInEntity(count as int) as void
```

| 参数    | 类型  | 描述                      |
| ----- | --- | ----------------------- |
| count | int | No Description Provided |


:::

:::group{name=setBeeStingCount}

Return Type: void

```zenscript
MCLivingEntity.setBeeStingCount(p_226300_1_ as int) as void
```

| 参数            | 类型  | 描述                      |
| ------------- | --- | ----------------------- |
| p_226300_1_ | int | No Description Provided |


:::

:::group{name=setHealth}

Return Type: void

```zenscript
MCLivingEntity.setHealth(health as float) as void
```

| 参数     | 类型    | 描述                      |
| ------ | ----- | ----------------------- |
| health | float | No Description Provided |


:::

:::group{name=setIdleTime}

Return Type: void

```zenscript
MCLivingEntity.setIdleTime(idleTimeIn as int) as void
```

| 参数         | 类型  | 描述                      |
| ---------- | --- | ----------------------- |
| idleTimeIn | int | No Description Provided |


:::

:::group{name=setItemStackToSlot}

Sets a copied given itemStack to the slot

Return Type: void

```zenscript
MCLivingEntity.setItemStackToSlot(slot as MCEquipmentSlotType, itemStack as IItemStack) as void
```

| 参数   | 类型                                                           | 描述                      |
| ---- | ------------------------------------------------------------ | ----------------------- |
| slot | [MCEquipmentSlotType](/vanilla/api/util/MCEquipmentSlotType) | No Description Provided |
| 物品应用 | [IItemStack](/vanilla/api/items/IItemStack)                  | No Description Provided |


:::

:::group{name=setLastAttackedEntity}

Return Type: void

```zenscript
MCLivingEntity.setLastAttackedEntity(entityIn as MCEntity) as void
```

| 参数       | 类型                                       | 描述                      |
| -------- | ---------------------------------------- | ----------------------- |
| entityIn | [MCEntity](/vanilla/api/entity/MCEntity) | No Description Provided |


:::

:::group{name=setRevengeTarget}

Return Type: void

```zenscript
MCLivingEntity.setRevengeTarget(livingBase as MCLivingEntity) as void
```

| 参数         | 类型                                                   | 描述                      |
| ---------- | ---------------------------------------------------- | ----------------------- |
| livingBase | [MCLivingEntity](/vanilla/api/entity/MCLivingEntity) | No Description Provided |


:::


