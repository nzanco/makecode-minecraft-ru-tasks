### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Der Agent setzt und baut Blöcke ab

## Ziegel auf dem Weg
1. Im blauen Block ``||player:bei Chat-Befehl||`` steht das Wort **go**. Lass es so. Den Block ``||loops:beim Start||`` lässt du auch so: Er gibt dem Agenten Bretter.
2. Auf dem Weg liegt ein Ziegel. Der Agent kommt nicht hindurch.
3. Bring den Agenten mit ``||agent:Agent, bewege dich||`` bis vor den Ziegel.
4. Nimm ``||agent:Agent, zerstöre||`` nach vorne: Der Agent baut den Ziegel vor sich ab.
5. Noch einmal ``||agent:Agent, bewege dich||`` – bis zur goldenen Platte.
6. Sag laut, wo der Agent stehen bleibt. Drück den grünen Knopf mit dem Dreieck, geh zurück ins Spiel, drück **T**, schreib **go** und drück **Enter**.

#### ~ tutorialhint
Der Agent bleibt vor dem Ziegel stehen? Schau, ob „zerstöre" im Programm ist und ob es dort steht, wo der Agent schon am Ziegel ist.

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
})
```

```ghost
player.onChat("go", function () {
    agent.move(FORWARD, 1)
    agent.destroy(FORWARD)
    agent.place(FORWARD)
})
```
