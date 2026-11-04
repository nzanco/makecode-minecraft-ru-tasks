### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Стена и башня

## Станция 1 — Мост
1. Впереди канал. Агент должен один раз повернуть влево и проложить прямой мост из пяти досок до золотого блока на том берегу. Блок ``||loops:при начале||`` даёт Агенту доски — не трогай его.
2. Запусти программу **go** как есть: нажми зелёную кнопку с треугольником, вернись в игру, нажми **T**, напиши **go** и нажми **Enter**. Посмотри, что сделал Агент.
3. Скажи вслух: что должно было получиться и что получилось? Какая это ошибка — правильная работа не столько раз или блок не на своём месте?
4. Почини программу, переставив **один** блок. Нажми кнопку справа от себя и запусти **go** ещё раз.

#### ~ tutorialhint
Сколько раз Агенту нужно повернуть? А сколько раз выполняется блок поворота?

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 5; index++) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.place(DOWN)
    }
})
```

```ghost
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    agent.turn(LEFT_TURN)
    for (let index = 0; index < 1; index++) {
        agent.move(FORWARD, 1)
        agent.place(DOWN)
    }
})
```
