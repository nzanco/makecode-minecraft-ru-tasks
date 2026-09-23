### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Дерево на следах

## Шаг 1
1. В синем блоке ``||player:при команде чата||`` стоит слово **go**. Не меняй его.
2. Упавшее дерево загородило следы. Пусть Агент уберёт его блоками ``||agent:агент: уничтожить||`` и ``||agent:агент: собрать все||``.
3. Нажми зелёную кнопку с треугольником.
4. Вернись в игру, нажми **T**, напиши **go** и нажми **Enter**.

#### ~ tutorialhint
Уничтожить можно только то, что прямо перед Агентом. Подведи его к дереву.


```ghost
player.onChat("go", function () {
    for (let index = 0; index < 4; index++) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.destroy(FORWARD)
        agent.collectAll()
    }
})
```
