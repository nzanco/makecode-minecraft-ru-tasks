### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Wiederholung in der Wiederholung

## Station 3 — Mauer und Turm
1. Das Programm **go** baut die Mauer von Station 2. Das letzte Feld des Bauplatzes ist für den Turm, rechts davon steht sein Pfosten.
2. Schreib **unter** die äußere Wiederholung weiter: noch eine Wiederholung, in der der Agent nach oben steigt und ein Brett unter sich legt. So wächst am Ende der Mauer ein Turm.
3. Stell die Zahl der neuen Wiederholung so ein, dass der Turm so hoch wird wie sein Pfosten. Sag laut, wie hoch die Mauer und wie hoch der Turm wird.
4. Drück den Knopf rechts von dir und starte **go**.

#### ~ tutorialhint
Der Turm wird einmal gebaut, nach der Mauer — seine Wiederholung steht unter der äußeren Wiederholung, nicht darin.

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 5; index++) {
        for (let index2 = 0; index2 < 3; index2++) {
            agent.move(UP, 1)
            agent.place(DOWN)
        }
        agent.move(FORWARD, 1)
        agent.move(DOWN, 3)
    }
})
```

```ghost
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 5; index++) {
        for (let index2 = 0; index2 < 3; index2++) {
            agent.move(UP, 1)
            agent.place(DOWN)
        }
        agent.move(FORWARD, 1)
        agent.move(DOWN, 3)
    }
    for (let index3 = 0; index3 < 1; index3++) {
        agent.move(UP, 1)
        agent.place(DOWN)
    }
})
```
