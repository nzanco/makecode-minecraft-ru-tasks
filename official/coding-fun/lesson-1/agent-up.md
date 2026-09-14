### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Агент поднимается к золотой плите

## Шаг 1
1. Измени программу **go** так, чтобы Агент встал на золотую плиту.
2. В блоке ``||agent:агент: переместиться||`` можно выбрать направление **вверх**.
3. Нажми зелёную кнопку с треугольником.
4. Вернись в игру, нажми **T**, напиши **go** и нажми **Enter**.


```ghost
player.onChat("go", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
```
