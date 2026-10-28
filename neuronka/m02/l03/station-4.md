### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Повтор в повторе

## Станция 4 — Стена выше
1. Это дополнительное задание. Программа **go** — стена и башня со станции 3. Колонна у начала стены здесь выше на один камень.
2. Сделай стену на одну доску выше, а башню оставь такой же. Для этого поменяй **два** числа.
3. Скажи вслух, какие два числа ты меняешь и почему их два.
4. Нажми кнопку справа от себя и запусти **go**.

#### ~ tutorialhint
Высоту стены держат два числа: сколько досок в столбике и на сколько Агент спускается после него.

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
    for (let index3 = 0; index3 < 5; index3++) {
        agent.move(UP, 1)
        agent.place(DOWN)
    }
})
```
