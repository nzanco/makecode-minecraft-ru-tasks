### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Auf den Spuren der Schildkröten

## Schritt 1
1. Im blauen Block ``||player:bei Chat-Befehl||`` steht das Wort **go**. Lass es so.
2. Schau, wohin der Agent schaut und wohin die Spuren gehen.
3. Bau im blauen Block den Weg aus ``||agent:Agent, bewege dich||`` und ``||agent:Agent, drehe dich nach||``.
4. Sag laut, wo der Agent stehen bleibt und wohin er dann schaut.
5. Drück den grünen Knopf mit dem Dreieck.
6. Geh zurück ins Spiel, drück **T**, schreib **go** und drück **Enter**.

Die Spuren biegen auf den bunten Platten ab. Geh sie Stück für Stück: Der Agent fängt dort an, wo er stehen geblieben ist, und schaut in dieselbe Richtung.

#### ~ tutorialhint
Steht der Agent falsch? Bau das Programm nicht neu. Ändere nur die Zahl oder die Drehrichtung.


```template
player.onChat("go", function () {
})
```

```ghost
player.onChat("go", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
```
