# MCToolType

A ToolType is used to identify what kind of blocks a tool can mine, or inversely, what kind of tool is required to mine a given block.

This class was added by a mod with mod-id `contenttweaker`. Так что если вы хотите использовать эту функцию, вам нужно установить этот мод.

## Импорт класса

It might be required for you to import the package if you encounter any issues (like casting an Array), so better be safe than sorry and add the import at the very top of the file.
```zenscript
import mods.contenttweaker.item.MCToolType;
```


## Implemented Interfaces
MCToolType implements the following interfaces. That means all methods defined in these interfaces are also available in MCToolType

- [CommandStringDisplayable](/vanilla/api/brackets/CommandStringDisplayable)
## Constructors

Constructs a ToolType object. If one with the given name already exists, they will internally point to the same toolType. Otherwise, a new one with the name is created (The same holds true for Brackets as well!)
```zenscript
new MCToolType(name as string) as MCToolType
new MCToolType("pickaxe");
```
| Параметр | Тип    | Description         |
| -------- | ------ | ------------------- |
| name     | string | The name to be used |


## Утилиты

| Тип результата | Является неявным |
| -------------- | ---------------- |
| string         | false            |

## Methods

### getName

Gets the name of this toolType. The name is what is used in the Bracket expression after the `<toolType:`

Return Type: string

```zenscript
MCToolType.getName() as string
<toolType:pickaxe>.getName();
```
### hashCode

Returns the object's hash code

Return Type: int

```zenscript
MCToolType.hashCode() as int
<toolType:pickaxe>.hashCode();
```
### toString

Get the string representation of this type. Is different from commandString!

Return Type: string

```zenscript
MCToolType.toString() as string
<toolType:pickaxe>.toString();
```

## Операторы

### EQUALS

Compares if two given MCToolType objects are equal

```zenscript
myMCToolType == o as Object
<toolType:pickaxe> == new MCToolType("pickaxe")
```



## Свойства

| Название | Тип    | Имеет Getter | Имеет Setter |
| -------- | ------ | ------------ | ------------ |
| name     | string | true         | false        |

