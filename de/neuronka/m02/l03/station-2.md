### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Wiederholung in der Wiederholung

## Station 2 — Die Mauer
1. Das Programm **go** baut eine Säule aus drei Brettern, dann geht der Agent einen Schritt vorwärts und wieder hinunter auf den Boden. Starte es und schau, wo der Agent ankommt.
2. Eine Mauer ist eine Säule, viele Male wiederholt. Nimm noch einen Block ``||loops:wiederholen||`` und leg das **ganze** Programm hinein: die Wiederholung der Säule und beide Blöcke für den Schritt.
3. Stell die Zahl der äußeren Wiederholung so ein, dass die Mauer den ganzen Bauplatz aus Stein füllt. Sag laut, wie lang und wie hoch die Mauer wird.
4. Drück den Knopf rechts von dir und starte **go**.

#### ~ tutorialhint
Einmal die äußere Wiederholung — eine Säule. So viele Felder auf dem Bauplatz, so viele Säulen.

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 3; index++) {
        agent.move(UP, 1)
        agent.place(DOWN)
    }
    agent.move(FORWARD, 1)
    agent.move(DOWN, 3)
})
```

```ghost
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 1; index++) {
        for (let index2 = 0; index2 < 3; index2++) {
            agent.move(UP, 1)
            agent.place(DOWN)
        }
        agent.move(FORWARD, 1)
        agent.move(DOWN, 3)
    }
})
```
