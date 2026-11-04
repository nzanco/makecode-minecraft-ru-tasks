### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Стена и башня

## Проверка учителя — канал
1. Это не задание ученика. Здесь учитель проверяет две программы из начала урока.
2. Запусти **gap**: три доски должны лечь через одну, на клетки 2, 4 и 6.
3. Нажми кнопку справа и запусти **out**: одна доска должна лечь на клетку 4.

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("gap", function () {
    for (let index = 0; index < 3; index++) {
        agent.move(FORWARD, 2)
        agent.place(DOWN)
    }
})
player.onChat("out", function () {
    for (let index = 0; index < 4; index++) {
        agent.move(FORWARD, 1)
    }
    agent.place(DOWN)
})
```
