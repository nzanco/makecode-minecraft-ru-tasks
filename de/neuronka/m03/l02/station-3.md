### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Von mir aus ~

## Station 3 — Ein Programm
1. Stell dich auf den Goldblock **X 50, Y 4, Z 10**. Der rote Block: **X 54, Y 4, Z 12**. Ändere zwei Zahlen mit ~ und starte **go**.
2. Jetzt die beiden anderen Goldblöcke: **X 50, Y 4, Z 18** und **X 58, Y 4, Z 18**. Beim ersten liegen zwei blaue Blöcke: **X 53, Z 22** und **X 55, Z 19**. Beim zweiten zwei lilafarbene: **X 61, Z 22** und **X 60, Z 23**.
3. Finde die Zahlen mit ~, die vom ersten Goldblock auf einen blauen und vom zweiten auf einen lilafarbenen Block führen — dieselben Zahlen für beide.
4. Starte **go** von einem Goldblock aus und dann, ohne etwas zu ändern, vom anderen.

#### ~ tutorialhint
Zähle für jeden farbigen Block: Um wie viel ist X größer, um wie viel Z als beim Goldblock? Welches Zahlenpaar kommt bei beiden vor?

```template
player.onChat("go", function () {
    agent.teleport(pos(1, 0, 1), SOUTH)
})
```

```ghost
player.onChat("go", function () {
    agent.teleport(pos(0, 0, 0), SOUTH)
})
```
