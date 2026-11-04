### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Mauer und Turm

## Lehrerprüfung — Schichten
1. Das ist keine Schüleraufgabe. Hier prüft die Lehrkraft die Mauer aus der Prüfung am Ende der Stunde.
2. Starte **layers**: zwei Reihen aus vier Brettern, eine über der anderen.

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
