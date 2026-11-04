### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Стена и башня

## Проверка учителя — слои
1. Это не задание ученика. Здесь учитель проверяет стену из проверки в конце урока.
2. Запусти **layers**: два ряда по четыре доски, один над другим.

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("layers", function () {
    for (let index = 0; index < 2; index++) {
        agent.move(UP, 1)
        for (let index2 = 0; index2 < 4; index2++) {
            agent.place(DOWN)
            agent.move(FORWARD, 1)
        }
        agent.move(BACK, 4)
    }
})
```
