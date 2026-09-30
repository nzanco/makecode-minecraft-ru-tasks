### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1

# Der Agent setzt und baut Blöcke ab

## Die große Wand
1. Vor dem Agenten steht eine Wand aus Brettern: fünf Felder breit und zwei Felder hoch. Sie hat **zwei Lücken** und **drei rote Blöcke**.
2. Unten, von links nach rechts: Brett, Lücke, roter Block, Brett, Brett. Oben: roter Block, Brett, Brett, Lücke, roter Block.
3. Fülle beide Lücken mit Brettern und ersetze jeden roten Block durch ein Brett. Der Agent steht ein Feld vor der Wand. Für die obere Reihe bewegt er sich einen Block nach oben.
4. Baue das Programm **go** mit Bewegungen, Drehungen, ``||agent:Agent, zerstöre||`` und ``||agent:Agent, platziere||``. Nenne vor dem Start die fünf Felder, die sich ändern.

#### ~ tutorialhint
Zerstöre einen roten Block zuerst und setze dann ein Brett an dieselbe Stelle. Fülle eine Lücke nur mit einem Brett. Für die obere Reihe bewege den Agenten nach oben.

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
})
```

```ghost
player.onChat("go", function () {
    agent.move(FORWARD, 3)
    agent.turn(LEFT_TURN)
    agent.move(UP, 1)
    agent.destroy(FORWARD)
    agent.place(FORWARD)
})
```
