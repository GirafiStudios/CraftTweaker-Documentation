# IIngredientWithAmount

Consists of an ingredient and an amount.

## Diese Klasse importieren

It might be required for you to import the package if you encounter any issues (like casting an Array), so better be safe than sorry and add the import at the very top of the file.
```zenscript
import crafttweaker.api.item.IIngredientWithAmount;
```


## Implemented Interfaces
IIngredientWithAmount implements the following interfaces. That means all methods defined in these interfaces are also available in IIngredientWithAmount

- [CommandStringDisplayable](/vanilla/api/brackets/CommandStringDisplayable)

## Properties

| Name          | Type                                          | Has Getter | Has Setter | Beschreibung                              |
| ------------- | --------------------------------------------- | ---------- | ---------- | ----------------------------------------- |
| amount        | int                                           | true       | false      | Gets the amount of Items in the ItemStack |
| commandString | string                                        | true       | false      | Returns the BEP to get this thingy        |
| ingredient    | [IIngredient](/vanilla/api/items/IIngredient) | true       | false      | The backing ingredient                    |
