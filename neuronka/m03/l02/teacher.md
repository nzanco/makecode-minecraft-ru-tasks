### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Относительно меня ~

## Показ учителя
1. Золотые блоки: X 90, Z 10 и X 94, Z 17. Программа **go** не меняется.
2. Запусти **go** с первого, со второго, потом снова с первого, лицом на север.

```template
player.onChat("go", function () {
    agent.teleport(pos(3, 0, 0), SOUTH)
})
```

```ghost
player.onChat("go", function () {
    agent.teleport(pos(3, 0, 0), SOUTH)
})
```
