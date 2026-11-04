### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Стена и башня

## Станция 4 — Две башни
1. Это дополнительное задание. Программа **go** строит стену и одну башню. А здесь башня нужна на каждом конце стены: зелёные клетки — для башен.
2. Допиши программу **над** стеной: сначала башня из трёх досок, потом Агент шагает вперёд и спускается на землю.
3. Скажи вслух, какие блоки выполнятся один раз, а какие — много раз.
4. Нажми кнопку справа от себя и запусти **go**.

#### ~ tutorialhint
После первой башни Агент наверху. На сколько ему спуститься, чтобы стена началась с земли?

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 3; index++) {
        for (let index2 = 0; index2 < 2; index2++) {
            agent.move(UP, 1)
            agent.place(DOWN)
        }
        agent.move(FORWARD, 1)
        agent.move(DOWN, 2)
    }
    for (let index3 = 0; index3 < 3; index3++) {
        agent.move(UP, 1)
        agent.place(DOWN)
    }
})
```

```ghost
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index4 = 0; index4 < 1; index4++) {
        agent.move(UP, 1)
        agent.place(DOWN)
    }
    agent.move(FORWARD, 1)
    agent.move(DOWN, 1)
})
```
