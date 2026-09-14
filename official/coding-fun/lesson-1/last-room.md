### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Последняя комната

## Шаг 1
В комнате две золотые плиты: одна для тебя, другая для Агента.

1. Встань на свою золотую плиту и не сходи с неё.
2. Измени программу **go** так, чтобы Агент встал на другую плиту.
3. Нажми зелёную кнопку с треугольником.
4. Нажми **T**, напиши **go** и нажми **Enter**.


```ghost
player.onChat("go", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
```
