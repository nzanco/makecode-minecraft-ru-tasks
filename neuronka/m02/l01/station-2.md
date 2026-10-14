### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Повтор и сколько раз

## Станция 2 — Ствол
1. Перед Агентом лежит ствол дерева: восемь брёвен в ряд.
2. Программа **go** ломает бревно и делает шаг — и так два раза. Скажи вслух, сколько брёвен она сломает. Запусти **go** и проверь.
3. Чтобы убрать весь ствол, ту же пару блоков пришлось бы написать восемь раз. Возьми блок ``||loops:повторить||``, вложи в него одну пару — ``||agent:агент: уничтожить||`` и ``||agent:агент: переместиться||`` — и поставь нужное число. Лишние блоки убери.
4. Нажми кнопку у старта. Скажи, где остановится Агент, и запусти **go**.

#### ~ tutorialhint
Одно бревно — один раз. Сколько брёвен, столько раз.

```template
player.onChat("go", function () {
    agent.destroy(FORWARD)
    agent.move(FORWARD, 1)
    agent.destroy(FORWARD)
    agent.move(FORWARD, 1)
})
```

```ghost
player.onChat("go", function () {
    for (let index = 0; index < 4; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
})
```
