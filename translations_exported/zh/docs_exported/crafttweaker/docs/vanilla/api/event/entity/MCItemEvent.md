# MCItemEvent

The event is not cancelable.

The event does not have a result.

## 导入相关包

It might be required for you to import the package if you encounter any issues (like casting an Array), so better be safe than sorry and add the import at the very top of the file.
```zenscript
import crafttweaker.api.event.entity.MCItemEvent;
```


## Extending MCEntityEvent

MCItemEvent extends [MCEntityEvent](/vanilla/api/event/entity/MCEntityEvent). That means all methods available in [MCEntityEvent](/vanilla/api/event/entity/MCEntityEvent) are also available in MCItemEvent

## 参数

| 名称         | 类型                                               | 可获得  | 可设置   |
| ---------- | ------------------------------------------------ | ---- | ----- |
| entityItem | [MCItemEntity](/vanilla/api/entity/MCItemEntity) | true | false |

