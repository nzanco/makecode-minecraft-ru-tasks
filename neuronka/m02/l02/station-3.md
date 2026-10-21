### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Внутри и снаружи

## Станция 3 — Зигзаг
1. Камни лежат ступеньками: вперёд и вправо, вперёд и вправо. Всего восемь камней.
2. Программа **go** написана на одну ступеньку: сломать, шагнуть, повернуться вправо, сломать, шагнуть, повернуться влево. Запусти **go** — уберутся два камня.
3. Возьми блок ``||loops:повторить||`` и положи в него **все шесть** блоков. Оба поворота должны быть внутри: Агент поворачивает на каждой ступеньке. Поставь число, чтобы ушли все восемь камней.
4. Нажми кнопку у старта. Скажи число до запуска и запусти **go**.

#### ~ tutorialhint
Одна ступенька — два камня. Восемь камней — сколько ступенек?

```template
player.onChat("go", function () {
    agent.destroy(FORWARD)
    agent.move(FORWARD, 1)
    agent.turn(RIGHT_TURN)
    agent.destroy(FORWARD)
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
```

```ghost
player.onChat("go", function () {
    for (let index = 0; index < 4; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
        agent.turn(RIGHT_TURN)
    }
})
```
