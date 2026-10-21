### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Внутри и снаружи

## Станция 4 — Две полосы
1. Перед Агентом две полосы по пять камней. Первая — прямо впереди. Вторая — справа от неё и на клетку ближе.
2. Программа **go** убирает первую полосу. Запусти её и посмотри, где остановился Агент.
3. Допиши программу **под** повтором: Агент один раз разворачивается ко второй полосе, а потом второй повтор убирает её.
4. Нажми кнопку у старта. Скажи, какие блоки выполнятся один раз, и запусти **go**.

#### ~ tutorialhint
Разворот нужен один раз — между двумя повторами, не внутри: повернуться вправо, шаг, повернуться вправо.

```template
player.onChat("go", function () {
    for (let index = 0; index < 5; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
})
```

```ghost
player.onChat("go", function () {
    for (let index = 0; index < 4; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 1)
})
```
