# BlockBuilderPillarRotatable

A special Block Builder that allows you to create blocks that can be rotated in the same way as logs can. <p> This means that it has one texture for the top and bottom and one texture for the sides. By default these sides' locations are the block's name, followed by and either `_end` or `sides`. As with most things here, sample images are generated for you by default, though.

This class was added by a mod with mod-id `contenttweaker`. 因此，如果要使用此功能，则需要安装此mod。

## 导入相关包

It might be required for you to import the package if you encounter any issues (like casting an Array), so better be safe than sorry and add the import at the very top of the file.
```zenscript
import mods.contenttweaker.block.pillar.BlockBuilderPillarRotatable;
```


## Extending BlockTypeBuilder

BlockBuilderPillarRotatable extends [BlockTypeBuilder](/mods/contenttweaker/API/block/BlockTypeBuilder). That means all methods available in [BlockTypeBuilder](/mods/contenttweaker/API/block/BlockTypeBuilder) are also available in BlockBuilderPillarRotatable

## 方法

:::group{name=build}

Instructs CoT to actually build whatever this builder is supposed to be building.

Return Type: void

```zenscript
// BlockBuilderPillarRotatable.build(resourceLocation as string) as void

new BlockBuilder().withType<BlockBuilderPillarRotatable>().build("my_awesome_block");
```

| 参数               | 类型     | 描述                                   |
| ---------------- | ------ | ------------------------------------ |
| resourceLocation | string | The resource path to give this block |


:::

:::group{name=withEndTexture}

Allows you to override the path of the texture that the end sides (top/bottom) should use. If that texture's namespace is in the namespace of CoT or any of its addons (that support it) then the image will be created by default. Uses a function that takes the block's name as input and returns the end texture for it.

Return Type: [BlockBuilderPillarRotatable](/mods/contenttweaker/API/block/pillar/BlockBuilderPillarRotatable)

```zenscript
// BlockBuilderPillarRotatable.withEndTexture(endTexture as Function<MCResourceLocation,MCResourceLocation>) as BlockBuilderPillarRotatable

new BlockBuilder().withType<BlockBuilderPillarRotatable>().withEndTexture((blockName as ResourceLocation) => new ResourceLocation(blockName.namespace, blockName.path + "_end"));
```

| 参数         | 类型                                                                                                                                                | 描述                  |
| ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------- |
| endTexture | Function&lt;[MCResourceLocation](/vanilla/api/util/MCResourceLocation),[MCResourceLocation](/vanilla/api/util/MCResourceLocation)&gt; | The function to use |


:::

:::group{name=withEndTexture}

Allows you to override the path of the texture that the end sides (top/bottom) should use. If that texture's namespace is in the namespace of CoT or any of its addons (that support it) then the image will be created by default.

Return Type: [BlockBuilderPillarRotatable](/mods/contenttweaker/API/block/pillar/BlockBuilderPillarRotatable)

```zenscript
// BlockBuilderPillarRotatable.withEndTexture(endTexture as MCResourceLocation) as BlockBuilderPillarRotatable

new BlockBuilder().withType<BlockBuilderPillarRotatable>().withEndTexture(<resource:contenttweaker:my_awesome_pillar_end>);
```

| 参数         | 类型                                                         | 描述                                        |
| ---------- | ---------------------------------------------------------- | ----------------------------------------- |
| endTexture | [MCResourceLocation](/vanilla/api/util/MCResourceLocation) | The texture to be used for the end sides. |


:::

:::group{name=withSideTexture}

Allows you to override the path of the texture that the sides (everything but top/bottom) should use. If that texture's namespace is in the namespace of CoT or any of its addons (that support it) then the image will be created by default. Uses a function that takes the block's name as input and returns the side texture for it.

Return Type: [BlockBuilderPillarRotatable](/mods/contenttweaker/API/block/pillar/BlockBuilderPillarRotatable)

```zenscript
// BlockBuilderPillarRotatable.withSideTexture(sidesTexture as Function<MCResourceLocation,MCResourceLocation>) as BlockBuilderPillarRotatable

new BlockBuilder().withType<BlockBuilderPillarRotatable>().withSideTexture((blockName as ResourceLocation) => new ResourceLocation(blockName.namespace, blockName.path + "_sides"));
```

| 参数           | 类型                                                                                                                                                | 描述                  |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------- |
| sidesTexture | Function&lt;[MCResourceLocation](/vanilla/api/util/MCResourceLocation),[MCResourceLocation](/vanilla/api/util/MCResourceLocation)&gt; | The function to use |


:::

:::group{name=withSideTexture}

Allows you to override the path of the texture that the sides (everything but top/bottom) should use. If that texture's namespace is in the namespace of CoT or any of its addons (that support it) then the image will be created by default.

Return Type: [BlockBuilderPillarRotatable](/mods/contenttweaker/API/block/pillar/BlockBuilderPillarRotatable)

```zenscript
// BlockBuilderPillarRotatable.withSideTexture(sidesTexture as MCResourceLocation) as BlockBuilderPillarRotatable

new BlockBuilder().withType<BlockBuilderPillarRotatable>().withSideTexture(<resource:contenttweaker:my_awesome_pillar_side>);
```

| 参数           | 类型                                                         | 描述                                    |
| ------------ | ---------------------------------------------------------- | ------------------------------------- |
| sidesTexture | [MCResourceLocation](/vanilla/api/util/MCResourceLocation) | The texture to be used for the sides. |


:::

