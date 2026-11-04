### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Стена и башня

## Станция 3 — Стена с лесенкой
1. Это дополнительное задание. Программа **go** должна построить стену длиной 5 и высотой 2 — как колонна слева.
2. Запусти **go** как есть и посмотри, что получилось.
3. Скажи вслух, что должно было получиться и что получилось. Найди блок, который стоит не на своём месте, и переставь его.
4. Нажми кнопку справа от себя и запусти **go** ещё раз.

#### ~ tutorialhint
Шаг вперёд нужен после каждого столбика или после каждой доски?

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 5; index++) {
        for (let index2 = 0; index2 < 2; index2++) {
            agent.move(UP, 1)
            agent.place(DOWN)
            agent.move(FORWARD, 1)
        }
        agent.move(DOWN, 2)
    }
})
```

```ghost
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 5; index++) {
        for (let index2 = 0; index2 < 2; index2++) {
            agent.move(UP, 1)
            agent.place(DOWN)
        }
        agent.move(FORWARD, 1)
        agent.move(DOWN, 2)
    }
})
```
