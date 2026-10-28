### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Повтор в повторе

## Станция 3 — Стена и башня
1. Программа **go** строит стену со станции 2. Последняя клетка площадки — для башни, справа от неё — её колонна.
2. Допиши программу **под** внешним повтором: ещё один повтор, в котором Агент поднимается и ставит доску под собой. Так в конце стены вырастет башня.
3. Поставь в новый повтор число, чтобы башня стала такой же высоты, как её колонна. Скажи вслух, какой высоты будет стена и какой — башня.
4. Нажми кнопку справа от себя и запусти **go**.

#### ~ tutorialhint
Башня строится один раз, после стены — её повтор стоит под внешним повтором, а не внутри.

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 5; index++) {
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
    for (let index = 0; index < 5; index++) {
        for (let index2 = 0; index2 < 3; index2++) {
            agent.move(UP, 1)
            agent.place(DOWN)
        }
        agent.move(FORWARD, 1)
        agent.move(DOWN, 3)
    }
    for (let index3 = 0; index3 < 1; index3++) {
        agent.move(UP, 1)
        agent.place(DOWN)
    }
})
```
