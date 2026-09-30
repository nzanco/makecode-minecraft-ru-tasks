### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Агент ставит и ломает блоки

## Дыра в стене
1. Теперь Агент на второй дорожке. В стене впереди дыра между двумя золотыми блоками.
2. Собери программу **go**: подведи Агента к дыре и поставь блок ``||agent:агент: разместить||`` вперёд.
3. Скажи вслух, на какую клетку встанет доска. Запусти **go**.

#### ~ tutorialhint
Агент ставит доску в клетку прямо перед собой. Остановись на клетку раньше дыры.

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
})
```

```ghost
player.onChat("go", function () {
    agent.move(FORWARD, 1)
    agent.destroy(FORWARD)
    agent.place(FORWARD)
})
```
