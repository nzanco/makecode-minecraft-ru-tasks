### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Wiederholen und wie oft

## Station 1 — Die Brücke
1. Vorne ist ein Kanal mit Wasser. Der Agent steht am Ufer und schaut auf den Kanal. Der Block ``||loops:beim Start||`` gibt dem Agenten Bretter — lass ihn so.
2. Im Programm **go** steckt der Block ``||loops:wiederholen||``. Darin sind zwei Blöcke: Der Agent geht einen Schritt vorwärts und setzt ein Brett unter sich — Richtung **nach unten**. Die Zahl im Wiederholen-Block sagt, wie oft.
3. Sag laut, wie viele Bretter liegen werden und wo der Agent stehen bleibt. Drück den grünen Knopf mit dem Dreieck, geh zurück ins Spiel, drück **T**, schreib **go** und drück **Enter**.
4. Die Brücke reicht nicht bis zum anderen Ufer. Ändere **nur die Zahl** im Wiederholen-Block, damit die Bretter über den ganzen Kanal reichen. Drück den Knopf am Start und starte **go** noch einmal.

#### ~ tutorialhint
Zähl die Wasserfelder vom Ufer bis zum Goldblock. Einmal — ein Brett.

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 2; index++) {
        agent.move(FORWARD, 1)
        agent.place(DOWN)
    }
})
```
