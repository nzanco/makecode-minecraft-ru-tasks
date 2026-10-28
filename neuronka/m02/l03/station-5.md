### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Повтор в повторе

## Станция 5 — Угол
1. Это дополнительное задание. Площадка из камня поворачивает за угол. Программа **go** строит первую сторону стены.
2. Допиши программу под ней: Агент один раз поворачивает, а потом строит вторую сторону такой же стеной.
3. Скажи вслух, куда должен повернуть Агент, сколько столбиков во второй стороне и какие блоки выполнятся один раз.
4. Нажми кнопку справа от себя и запусти **go**.

#### ~ tutorialhint
После первой стены Агент стоит на угловой клетке. Повернуться налево нужно один раз — между двумя стенами.

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 4; index++) {
        for (let index2 = 0; index2 < 3; index2++) {
            agent.move(UP, 1)
            agent.place(DOWN)
        }
        agent.move(FORWARD, 1)
        agent.move(DOWN, 3)
    }
})
```

```ghost
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 4; index++) {
        for (let index2 = 0; index2 < 3; index2++) {
            agent.move(UP, 1)
            agent.place(DOWN)
        }
        agent.move(FORWARD, 1)
        agent.move(DOWN, 3)
    }
    agent.turn(LEFT_TURN)
})
```
