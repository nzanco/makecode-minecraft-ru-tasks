### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Маршрут к цели

## Станция 2 — Агент заблудился
1. Агент должен поставить светокамень в нишу под золотым блоком. Блок ``||loops:при начале||`` даёт Агенту светокамни — не трогай его.
2. Программа **go** уже собрана, но в ней ошибка. Запусти её и посмотри, где остановится Агент.
3. Скажи вслух: что должно было получиться и что получилось?
4. Найди блок, из-за которого Агент пришёл не туда. Поменяй в нём одно.
5. Нажми кнопку у старта и запусти **go** снова.

#### ~ tutorialhint
Посмотри, где встал светокамень и где ниша. На сколько клеток Агент не дошёл?

```template
agent.setItem(GLOWSTONE, 64, 1)
player.onChat("go", function () {
    agent.move(FORWARD, 2)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 2)
    agent.place(FORWARD)
})
```

```ghost
player.onChat("go", function () {
    agent.move(FORWARD, 1)
    agent.turn(RIGHT_TURN)
    agent.place(FORWARD)
})
```
