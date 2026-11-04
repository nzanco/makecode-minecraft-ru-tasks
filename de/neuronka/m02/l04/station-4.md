### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Mauer und Turm

## Station 4 — Zwei Türme
1. Das ist eine Zusatzaufgabe. Das Programm **go** baut eine Mauer und einen Turm. Hier braucht es an jedem Ende der Mauer einen Turm: Die grünen Felder sind für die Türme.
2. Schreib das Programm **über** der Mauer weiter: zuerst ein Turm aus drei Brettern, dann geht der Agent einen Schritt vorwärts und steigt auf den Boden hinunter.
3. Sag laut, welche Blöcke einmal laufen und welche viele Male.
4. Drück den Knopf rechts von dir und starte **go**.

#### ~ tutorialhint
Nach dem ersten Turm ist der Agent oben. Wie weit muss er hinunter, damit die Mauer am Boden beginnt?

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 3; index++) {
        for (let index2 = 0; index2 < 2; index2++) {
            agent.move(UP, 1)
            agent.place(DOWN)
        }
        agent.move(FORWARD, 1)
        agent.move(DOWN, 2)
    }
    for (let index3 = 0; index3 < 3; index3++) {
        agent.move(UP, 1)
        agent.place(DOWN)
    }
})
```

```ghost
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index4 = 0; index4 < 1; index4++) {
        agent.move(UP, 1)
        agent.place(DOWN)
    }
    agent.move(FORWARD, 1)
    agent.move(DOWN, 1)
})
```
