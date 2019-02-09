# mcpypi API

## Переменные и аргументы

Все методы и функции записаны в виде:\
`function(arguments) => return_value:type`

`x, y, z` - целочисленные координаты.\
`xf, yf, zf` - координаты.\
`id` - идентификатор блока (целое число,  0 - 400+).\
`blockData` - модификатор блока,  например цвет блока шерсти (0 - 15).
`Block` - объект блока.

## Методы объекта Minecraft

`spawnEntity(type, x, y, z, tags) => id:int` - Создание сущности.

`removeEntity(id)` - Удаление сущности.

`getBlock(x, y, z) => id:int` - Получить идентификатор блока по координате.

`getBlockWithData(x, y, z) => Block` - Получить объект блока.

`getBlockWithNBT(x, y, z) => Block | (Block,  nbt)` - Получить блок и тег. Для того,  чтобы это сработало,  нужно вызвать команду `Minecraft.setting("include_nbt_with_data", 1)`.

`getBlocks(x0, y0, z0, x1, y1, z1) => [id:int]` - Get a cuboid of blocks. Packed with a y-loop,  x-loop,  z-loop,  in this order.

`getBlocksWithData(x0, y0, z0, x1, y1, z1) => [Block(id:int,  meta:int)]` - Взять куб блоков-объектов.

`getBlocksWithNBT(x0, y0, z0, x1, y1, z1) => [Block(id,  meta,  nbt)]` - Взять куб блоков-объектов с тегами.

`setBlock(x, y, z, id, [blockData])` - Установить блок по идентификатору.

`setBlockWithNBT(x, y, z, id, blockData, nbt)` - Установить блок с тегом.

`setBlocks(x0, y0, z0, x1, y1, z1, id, [blockData])` - Установить куб из блоков по идентификатору.

`setBlocksWithNBT(x0, y0, z0, x1, y1, z1, id, blockData, nbt)` - Установить куб из блоков с тегами.

`getHeight(x, z) => int` - Получить высоту мира по координате (относительно уровня моря).

`getPlayerId() => id:int` - Взять идентификатор текущего пользователя

`getPlayerEntityIds() => [id:int]` - Взять идентификаторы всех подключенных пользователей.

`saveCheckpoint()` - Сохранить текущее состояние мира.

`restoreCheckpoint()` - Восстановить состояние мира к сохраненному.

`postToChat(message)` - Вывести сообщение в чат.
