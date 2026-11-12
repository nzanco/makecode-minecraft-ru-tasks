### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Где я? X, Y, Z

## Показ учителя
1. Показ к слайду: три блока — зелёный, красный и синий. Программа телепортирует в ``||positions:мир 94 4 20||``.
2. Ученик называет блок до запуска. Запусти **go**.

```template
player.onChat("go", function () {
    player.teleport(world(94, 4, 20))
})
```
