### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Повтор и сколько раз

## Станция 3 — Длинный ствол (дополнительно)
1. Здесь ствол длиннее: десять брёвен.
2. Внутри повтора теперь четыре блока: Агент ломает бревно, шагает, ломает следующее и снова шагает. За один раз он убирает **два** бревна.
3. Поставь в повтор такое число, чтобы ствол исчез целиком. Скажи его вслух до запуска, потом запусти **go**.

#### ~ tutorialhint
Десять брёвен, по два за раз. Сколько раз нужно?

```template
player.onChat("go", function () {
    for (let index = 0; index < 1; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
})
```
