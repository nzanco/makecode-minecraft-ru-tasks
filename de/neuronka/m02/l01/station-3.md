### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Wiederholen und wie oft

## Station 3 — Der lange Stamm (Zusatzaufgabe)
1. Hier ist der Stamm länger: zehn Holzblöcke.
2. Im Wiederholen-Block stecken jetzt vier Blöcke: Der Agent zerstört einen Block, geht, zerstört den nächsten und geht wieder. In einer Runde schafft er **zwei** Holzblöcke.
3. Stell eine Zahl ein, damit der ganze Stamm verschwindet. Sag sie laut vor dem Start, dann starte **go**.

#### ~ tutorialhint
Zehn Holzblöcke, zwei pro Runde. Wie oft?

```template
player.onChat("go", function () {
    for (let index = 0; index < 1; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
})
```
