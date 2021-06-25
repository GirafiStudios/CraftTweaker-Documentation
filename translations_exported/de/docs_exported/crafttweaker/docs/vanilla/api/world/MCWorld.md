# MCWorld

Worlds represent a dimension within the game. They are used to interact with the blocks, mobs, and other variables within that dimension.

## Diese Klasse importieren

It might be required for you to import the package if you encounter any issues (like casting an Array), so better be safe than sorry and add the import at the very top of the file.
```zenscript
import crafttweaker.api.world.MCWorld;
```


## Implemented Interfaces
MCWorld implements the following interfaces. That means all methods defined in these interfaces are also available in MCWorld

- AutoCloseable

## Casters

| Result type                                       | Is Implicit |
| ------------------------------------------------- | ----------- |
| [MCServerWorld](/vanilla/api/world/MCServerWorld) | false       |

## Methoden

:::group{name=addEntity}

add an entity to the world, return if the entity is added successfully.

Return Type: boolean

```zenscript
MCWorld.addEntity(entity as MCEntity) as boolean
```

| Parameter | Type                                     | Beschreibung            |
| --------- | ---------------------------------------- | ----------------------- |
| entity    | [MCEntity](/vanilla/api/entity/MCEntity) | No Description Provided |


:::

:::group{name=asServerWorld}

Return Type: [MCServerWorld](/vanilla/api/world/MCServerWorld)

```zenscript
// MCWorld.asServerWorld() as MCServerWorld

world.asServerWorld();
```

:::

:::group{name=destroyBlock}

Destroys a block within the world.

Return Type: boolean

```zenscript
// MCWorld.destroyBlock(pos as BlockPos, doDrops as boolean) as boolean

world.destroyBlock(new BlockPos(0, 1, 2), true);
```

| Parameter | Type                                   | Beschreibung                                         |
| --------- | -------------------------------------- | ---------------------------------------------------- |
| pos       | [BlockPos](/vanilla/api/util/BlockPos) | The position of the block.                           |
| doDrops   | boolean                                | Whether or not the block drops itself and it's loot. |


:::

:::group{name=destroyBlock}

Destroys a block within the world.

Return Type: boolean

```zenscript
// MCWorld.destroyBlock(pos as BlockPos, doDrops as boolean, breaker as MCEntity) as boolean

world.destroyBlock(new BlockPos(0, 1, 2), true, player);
```

| Parameter | Type                                     | Beschreibung                                         |
| --------- | ---------------------------------------- | ---------------------------------------------------- |
| pos       | [BlockPos](/vanilla/api/util/BlockPos)   | The position of the block.                           |
| doDrops   | boolean                                  | Whether or not the block drops itself and it's loot. |
| breaker   | [MCEntity](/vanilla/api/entity/MCEntity) | The entity to break the block.                       |


:::

:::group{name=getBiome}

Gets the biome at a given position.

Return Type: [MCBiome](/vanilla/api/world/MCBiome)

```zenscript
// MCWorld.getBiome(pos as BlockPos) as MCBiome

world.getBiome(new BlockPos(0, 1, 2));
```

| Parameter | Type                                   | Beschreibung             |
| --------- | -------------------------------------- | ------------------------ |
| pos       | [BlockPos](/vanilla/api/util/BlockPos) | The position to look up. |


:::

:::group{name=getBlockState}

Gets the block state at a given position.

Return Type: [MCBlockState](/vanilla/api/block/MCBlockState)

```zenscript
// MCWorld.getBlockState(pos as BlockPos) as MCBlockState

world.getBlockState(new BlockPos(0, 1, 2));
```

| Parameter | Type                                   | Beschreibung             |
| --------- | -------------------------------------- | ------------------------ |
| pos       | [BlockPos](/vanilla/api/util/BlockPos) | The position to look up. |


:::

:::group{name=getEntitiesInArea}

Gets all entities in given area, but the arguments are block poses. If `pos2` is omitted, it will use `pos1.add(1, 1, 1)`

Return Type: stdlib.List&lt;[MCEntity](/vanilla/api/entity/MCEntity)&gt;

```zenscript
// MCWorld.getEntitiesInArea(pos1 as BlockPos, pos2 as BlockPos) as stdlib.List<MCEntity>

world.getEntitiesInArea(new BlockPos(0, 1, 2), new BlockPos(3, 4, 5));
```

| Parameter | Type                                   | Beschreibung            | Optional | DefaultValue |
| --------- | -------------------------------------- | ----------------------- | -------- | ------------ |
| pos1      | [BlockPos](/vanilla/api/util/BlockPos) | No Description Provided | false    |              |
| pos2      | [BlockPos](/vanilla/api/util/BlockPos) | No Description Provided | true     |              |


:::

:::group{name=getEntitiesInArea}

Gets all entities in given area.

Return Type: stdlib.List&lt;[MCEntity](/vanilla/api/entity/MCEntity)&gt;

```zenscript
// MCWorld.getEntitiesInArea(x1 as double, y1 as double, z1 as double, x2 as double, y2 as double, z2 as double) as stdlib.List<MCEntity>

world.getEntitiesInArea(1.0, 1.0, 1.0, 11.4, 11.4, 11.4);
```

| Parameter | Type   | Beschreibung            |
| --------- | ------ | ----------------------- |
| x1        | double | No Description Provided |
| y1        | double | No Description Provided |
| z1        | double | No Description Provided |
| x2        | double | No Description Provided |
| y2        | double | No Description Provided |
| z2        | double | No Description Provided |


:::

:::group{name=getEntitiesInAreaExcluding}



Return Type: stdlib.List&lt;[MCEntity](/vanilla/api/entity/MCEntity)&gt;

```zenscript
// MCWorld.getEntitiesInAreaExcluding(excludingEntity as MCEntity?, predicate as Predicate<MCEntity>, pos1 as BlockPos, pos2 as BlockPos) as stdlib.List<MCEntity>

world.getEntitiesInAreaExcluding(entity, (entityIn) => entityIn.isInWater(), new BlockPos(0, 1, 2), new BlockPos(3, 4, 5));
```

| Parameter       | Type                                                                  | Beschreibung            | Optional | DefaultValue |
| --------------- | --------------------------------------------------------------------- | ----------------------- | -------- | ------------ |
| excludingEntity | [MCEntity](/vanilla/api/entity/MCEntity)?                             | No Description Provided | false    |              |
| predicate       | Predicate&lt;[MCEntity](/vanilla/api/entity/MCEntity)&gt; | No Description Provided | false    |              |
| pos1            | [BlockPos](/vanilla/api/util/BlockPos)                                | No Description Provided | false    |              |
| pos2            | [BlockPos](/vanilla/api/util/BlockPos)                                | No Description Provided | true     |              |


:::

:::group{name=getEntitiesInAreaExcluding}

Gets all entities in given area, excluding the one passed into it.

Return Type: stdlib.List&lt;[MCEntity](/vanilla/api/entity/MCEntity)&gt;

```zenscript
// MCWorld.getEntitiesInAreaExcluding(excludingEntity as MCEntity?, x1 as double, y1 as double, z1 as double, x2 as double, y2 as double, z2 as double, predicate as Predicate<MCEntity>) as stdlib.List<MCEntity>

world.getEntitiesInAreaExcluding(entity, 1.0, 1.0, 1.0, 11.4, 11.4, 11.4, (entityIn) => entityIn.isInWater());
```

| Parameter       | Type                                                                  | Beschreibung            |
| --------------- | --------------------------------------------------------------------- | ----------------------- |
| excludingEntity | [MCEntity](/vanilla/api/entity/MCEntity)?                             | No Description Provided |
| x1              | double                                                                | No Description Provided |
| y1              | double                                                                | No Description Provided |
| z1              | double                                                                | No Description Provided |
| x2              | double                                                                | No Description Provided |
| y2              | double                                                                | No Description Provided |
| z2              | double                                                                | No Description Provided |
| predicate       | Predicate&lt;[MCEntity](/vanilla/api/entity/MCEntity)&gt; | the entity filter       |


:::

:::group{name=getRedstonePower}

Gets the redstone signal strength available to a position from a given direction.

Return Type: int

```zenscript
// MCWorld.getRedstonePower(pos as BlockPos, direction as Direction) as int

world.getRedstonePower(new BlockPos(0, 1, 2), <direction:north>);
```

| Parameter | Type                                     | Beschreibung            |
| --------- | ---------------------------------------- | ----------------------- |
| pos       | [BlockPos](/vanilla/api/util/BlockPos)   | The position to check.  |
| direction | [Direction](/vanilla/api/util/Direction) | The direction to query. |


:::

:::group{name=getRedstonePowerFromNeighbors}

Gets the highest redstone signal available to a position from any of it's neighbors.

Return Type: int

```zenscript
// MCWorld.getRedstonePowerFromNeighbors(pos as BlockPos) as int

world.getRedstonePowerFromNeighbors(new BlockPos(0, 1, 2));
```

| Parameter | Type                                   | Beschreibung           |
| --------- | -------------------------------------- | ---------------------- |
| pos       | [BlockPos](/vanilla/api/util/BlockPos) | The position to check. |


:::

:::group{name=getStrongPower}

Gets the highest strong (direct) redstone signal of any neighboring block.

Return Type: int

```zenscript
// MCWorld.getStrongPower(pos as BlockPos) as int

world.getStrongPower(new BlockPos(0, 1, 2));
```

| Parameter | Type                                   | Beschreibung           |
| --------- | -------------------------------------- | ---------------------- |
| pos       | [BlockPos](/vanilla/api/util/BlockPos) | The position to check. |


:::

:::group{name=getTileData}

Gets the tile entity data for a tile entity at a given position.

Return Type: [IData](/vanilla/api/data/IData)

```zenscript
// MCWorld.getTileData(pos as BlockPos) as IData

world.getTileData(new BlockPos(0, 1, 2));
```

| Parameter | Type                                   | Beschreibung                     |
| --------- | -------------------------------------- | -------------------------------- |
| pos       | [BlockPos](/vanilla/api/util/BlockPos) | The position of the tile entity. |


:::

:::group{name=getTileEntity}

Return Type: [MCTileEntity](/vanilla/api/tileentity/MCTileEntity)?

```zenscript
MCWorld.getTileEntity(pos as BlockPos) as MCTileEntity?
```

| Parameter | Type                                   | Beschreibung            |
| --------- | -------------------------------------- | ----------------------- |
| pos       | [BlockPos](/vanilla/api/util/BlockPos) | No Description Provided |


:::

:::group{name=isAir}

Checks if the block at a given position is air.

Return Type: boolean

```zenscript
// MCWorld.isAir(pos as BlockPos) as boolean

world.isAir(new BlockPos(0, 1, 2));
```

| Parameter | Type                                   | Beschreibung             |
| --------- | -------------------------------------- | ------------------------ |
| pos       | [BlockPos](/vanilla/api/util/BlockPos) | The position to look up. |


:::

:::group{name=isBlockPowered}

Checks if a given position is receiving a redstone signal.

Return Type: boolean

```zenscript
// MCWorld.isBlockPowered(pos as BlockPos) as boolean

world.isBlockPowered(new BlockPos(0, 1, 2));
```

| Parameter | Type                                   | Beschreibung           |
| --------- | -------------------------------------- | ---------------------- |
| pos       | [BlockPos](/vanilla/api/util/BlockPos) | The position to check. |


:::

:::group{name=isLoaded}

Checks if the block at a given position is in a loaded chunk.

Return Type: boolean

```zenscript
// MCWorld.isLoaded(pos as BlockPos) as boolean

world.isLoaded(new BlockPos(0, 1, 2));
```

| Parameter | Type                                   | Beschreibung             |
| --------- | -------------------------------------- | ------------------------ |
| pos       | [BlockPos](/vanilla/api/util/BlockPos) | The position to look up. |


:::

:::group{name=isRainingAt}

Checks if it is raining at a specific position. This can never be true if the position does not have direct line of sight to the sky.

Return Type: boolean

```zenscript
// MCWorld.isRainingAt(pos as BlockPos) as boolean

world.isRainingAt(new BlockPos(0, 1, 2));
```

| Parameter | Type                                   | Beschreibung           |
| --------- | -------------------------------------- | ---------------------- |
| pos       | [BlockPos](/vanilla/api/util/BlockPos) | The position to check. |


:::

:::group{name=isRemote}

Checks if the world is remote. This is always true on the rendering thread.

Return Type: boolean

```zenscript
// MCWorld.isRemote() as boolean

world.isRemote();
```

:::

:::group{name=playEvent}

Triggers a predetermined event on the client. Using this on a server or integrated server will send the event to all nearby players.

Return Type: void

```zenscript
// MCWorld.playEvent(eventId as int, pos as BlockPos, data as int) as void

world.playEvent(2005, new BlockPos(0, 1, 2), 0);
```

| Parameter | Type                                   | Beschreibung                                                                                        |
| --------- | -------------------------------------- | --------------------------------------------------------------------------------------------------- |
| eventId   | int                                    | The ID of the event to play.                                                                        |
| pos       | [BlockPos](/vanilla/api/util/BlockPos) | The position of the event.                                                                          |
| data      | int                                    | Four bytes of additional data encoded as an integer. This <br />         is generally unused. |


:::

:::group{name=playEvent}

Triggers a predetermined event on the client. Using this on a server or integrated server will send the event to all nearby players.

Return Type: void

```zenscript
// MCWorld.playEvent(excluded as MCPlayerEntity, eventId as int, pos as BlockPos, data as int) as void

world.playEvent(player, 2005, new BlockPos(0, 1, 2), 0);
```

| Parameter | Type                                                 | Beschreibung                                                                                        |
| --------- | ---------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| excluded  | [MCPlayerEntity](/vanilla/api/entity/MCPlayerEntity) | An excluded player who will not receive the event.                                                  |
| eventId   | int                                                  | The ID of the event to play.                                                                        |
| pos       | [BlockPos](/vanilla/api/util/BlockPos)               | The position of the event.                                                                          |
| data      | int                                                  | Four bytes of additional data encoded as an integer. This <br />         is generally unused. |


:::

:::group{name=setBlockState}

Sets the block and it's state at a given position.

Return Type: boolean

```zenscript
// MCWorld.setBlockState(pos as BlockPos, state as MCBlockState) as boolean

world.setBlockState(new BlockPos(0, 1, 2), <blockstate:minecraft:iron_block>);
```

| Parameter | Type                                            | Beschreibung                      |
| --------- | ----------------------------------------------- | --------------------------------- |
| pos       | [BlockPos](/vanilla/api/util/BlockPos)          | The position to set the block at. |
| state     | [MCBlockState](/vanilla/api/block/MCBlockState) | The new state of the block.       |


:::


## Properties

| Name             | Type                               | Has Getter | Has Setter | Beschreibung                                                                                                                      |
| ---------------- | ---------------------------------- | ---------- | ---------- | --------------------------------------------------------------------------------------------------------------------------------- |
| dayTime          | boolean                            | true       | false      | Checks if it is day time in the world. Different dimensions will have <br />  different logic for how this is determined.   |
| difficulty       | string                             | true       | false      | Gets the difficulty setting for the world.                                                                                        |
| difficultyLocked | boolean                            | true       | false      | Checks if the difficulty of the world has been locked.                                                                            |
| dimension        | string                             | true       | false      | Gets the registry name of the dimension this world represents.                                                                    |
| gameTime         | long                               | true       | false      | Gets the current game time in ticks.                                                                                              |
| hardcore         | boolean                            | true       | false      | Checks if hardcore mode is enabled.                                                                                               |
| nightTime        | boolean                            | true       | false      | Checks if it is night time in the world. Different dimensions will have <br />  different logic for how this is determined. |
| raining          | boolean                            | true       | false      | Checks if it is raining.                                                                                                          |
| random           | [Random](/vanilla/api/util/Random) | true       | false      | No Description Provided                                                                                                           |
| remote           | boolean                            | true       | false      | Checks if the world is remote. This is always true on the rendering <br />  thread.                                         |
| seaLevel         | int                                | true       | false      | Gets the height of the sea level.                                                                                                 |
| thundering       | boolean                            | true       | false      | Checks if there is a thunder storm.                                                                                               |
| timeOfDay        | long                               | true       | false      | Gets the current time of the day in ticks.                                                                                        |
