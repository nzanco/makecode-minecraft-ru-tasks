### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Относительно меня ~

## Станция 4 — Две команды
1. Команда **base** должна ставить Агента на алмаз **X 72, Y 4, Z 20**, с какого золотого блока её ни запусти — место всегда одно.
2. Команда **me** должна ставить Агента на два блока восточнее тебя, с какого золотого блока её ни запусти — место движется с тобой.
3. Запусти обе с первого золотого блока, потом со второго. Что не так?
4. Поменяй в командах блоки положения: где нужен ``||positions:мир||``, а где ``||positions:~ ~ ~||``? Поставь числа и запусти обе с двух золотых блоков.

#### ~ tutorialhint
Место всегда одно — нужен «мир». Место движется с тобой — нужен ~.

```template
player.onChat("base", function () {
    agent.teleport(pos(2, 0, 10), SOUTH)
})
player.onChat("me", function () {
    agent.teleport(world(72, 4, 10), SOUTH)
})
```

```ghost
player.onChat("base", function () {
    agent.teleport(world(0, 0, 0), SOUTH)
})
player.onChat("me", function () {
    agent.teleport(pos(0, 0, 0), SOUTH)
})
```
