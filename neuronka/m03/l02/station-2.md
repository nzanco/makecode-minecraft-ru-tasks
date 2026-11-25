### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Относительно меня ~

## Станция 2 — Зелёный блок
1. Встань на золотой блок: **X 30, Y 4, Z 14**. Зелёный блок: **X 35, Y 4, Z 14**.
2. Найди число, на которое отличаются X. Поменяй первое число с ~ в блоке ``||positions:~ ~ ~||``.
3. Скажи, куда попадёт Агент, и запусти **go**.

#### ~ tutorialhint
~ считает от тебя. Сколько блоков на восток от твоего X до X зелёного блока?

```template
player.onChat("go", function () {
    agent.teleport(pos(1, 0, 0), SOUTH)
})
```

```ghost
player.onChat("go", function () {
    agent.teleport(pos(0, 0, 0), SOUTH)
})
```
