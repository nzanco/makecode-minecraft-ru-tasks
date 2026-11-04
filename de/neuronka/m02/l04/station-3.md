### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Mauer und Turm

## Station 3 — Mauer mit Treppe
1. Das ist eine Zusatzaufgabe. Das Programm **go** soll eine Mauer bauen, 5 lang und 2 hoch — wie der Pfosten links.
2. Starte **go** so, wie es ist, und schau, was herauskommt.
3. Sag laut, was herauskommen sollte und was herausgekommen ist. Finde den Block an der falschen Stelle und verschieb ihn.
4. Drück den Knopf rechts von dir und starte **go** noch einmal.

#### ~ tutorialhint
Braucht es den Schritt vorwärts nach jeder Säule oder nach jedem Brett?

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 5; index++) {
        for (let index2 = 0; index2 < 2; index2++) {
            agent.move(UP, 1)
            agent.place(DOWN)
            agent.move(FORWARD, 1)
        }
        agent.move(DOWN, 2)
    }
})
```

```ghost
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 5; index++) {
        for (let index2 = 0; index2 < 2; index2++) {
            agent.move(UP, 1)
            agent.place(DOWN)
        }
        agent.move(FORWARD, 1)
        agent.move(DOWN, 2)
    }
})
```
