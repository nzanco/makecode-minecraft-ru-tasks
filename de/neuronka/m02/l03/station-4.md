### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Wiederholung in der Wiederholung

## Station 4 — Die höhere Mauer
1. Das ist eine Zusatzaufgabe. Das Programm **go** ist Mauer und Turm von Station 3. Der Pfosten am Anfang der Mauer ist hier einen Stein höher.
2. Mach die Mauer ein Brett höher und lass den Turm, wie er ist. Dafür änderst du **zwei** Zahlen.
3. Sag laut, welche zwei Zahlen du änderst und warum es zwei sind.
4. Drück den Knopf rechts von dir und starte **go**.

#### ~ tutorialhint
Die Höhe der Mauer steckt in zwei Zahlen: wie viele Bretter in einer Säule sind und wie weit der Agent danach hinuntergeht.

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
    for (let index3 = 0; index3 < 5; index3++) {
        agent.move(UP, 1)
        agent.place(DOWN)
    }
})
```
