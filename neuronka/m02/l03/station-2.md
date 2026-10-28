### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Повтор в повторе

## Станция 2 — Стена
1. Программа **go** строит один столбик из трёх досок, а потом Агент шагает вперёд и спускается на землю. Запусти её и посмотри, где окажется Агент.
2. Стена — это столбик, повторённый много раз. Возьми ещё один блок ``||loops:повторить||`` и положи в него **всю** программу: повтор столбика и оба блока шага.
3. Поставь во внешний повтор число, чтобы стена заняла всю площадку из камня. Скажи вслух, какой длины и какой высоты будет стена.
4. Нажми кнопку справа от себя и запусти **go**.

#### ~ tutorialhint
Один раз внешнего повтора — один столбик. Сколько клеток на площадке, столько столбиков.

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 3; index++) {
        agent.move(UP, 1)
        agent.place(DOWN)
    }
    agent.move(FORWARD, 1)
    agent.move(DOWN, 3)
})
```

```ghost
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 1; index++) {
        for (let index2 = 0; index2 < 3; index2++) {
            agent.move(UP, 1)
            agent.place(DOWN)
        }
        agent.move(FORWARD, 1)
        agent.move(DOWN, 3)
    }
})
```
