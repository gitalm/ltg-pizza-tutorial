# Ludwig-Thoma in der Pizzeria 🍕


### ~

## {Introduction @unplugged}

![Game animation](/static/tutorials/chase-the-pizza.gif)

In diesem Tutorial lernst eine Pizza mit einer Arcade Figur, 
dem sogenannten Sprite, zu fangen. 
Das Ziel des Spieles ist es möglichst viele Pizzen 🍕 zu finden
bevor der 3s Countdown ⌛️ vorbei ist! Jedesmal, wenn du eine Pizza findest,
bekommst du einen Punkt und der Countdown beginnt erneut.

## {Step 1}

Öffne ``||scene:Szene||`` im linken Menü und ziehe den
``||scene:setze Hintergrundfarbe auf||`` Block in den ``||loops:beim Start||`` 
Block auf dem Arbeitsplatz. Klicke auf **Weiter** 
um zum nächsten Schritt des Tutorials zu kommen.

```blocks
// @highlight
scene.setBackgroundColor(0)
```

## {Step 2}

Im ``||scene:setze Hintergrundfarbe auf||`` Block, 
klicke auf das graue Oval und suche eine eigene Hintergrundfarbe aus.
Rechts unten siehst du im Simulator, wie dein Spiel 🕹️ aussieht.

![Choose background color](/static/tutorials/chase-the-pizza/background-color.jpg)

## {Step 3}

Öffne ``||sprites:Sprites||`` im linken Menü und wähle den 
ersten Block, ziehe
``||variables(sprites):setze mySprite||`` in den  
``||loops:beim Start||`` 
Block auf der Arbeitsfläche. Damit hast du einen Spieler 
``||sprites:Player||`` für dein Spiel hinzugefügt.

```blocks
let mySprite: Sprite = null
scene.setBackgroundColor(7)
// @highlight
mySprite = sprites.create(img`
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
`, SpriteKind.Player)
```

## {Step 4}

Zeichne deinen ``||sprites:Player||`` Charakter, indem du in das
graue Quadrat klickst im ``||variables(sprites):setze mySprite||`` 
Block zum Öffnen des Editors. 
Verwende die Farbenpalette um auf der Leinwand deinen Sprite zu malen. 
Klicke auf **Fertig**, wenn du Ludwig-Thoma gemalt hast.

![Image editor](/static/tutorials/chase-the-pizza/image-editor.gif)

## {Step 5}

Öffne ``||controller:Controller||`` im linken Menü und ziehe 
``||controller:bewege mySprite mit Knöpfen||`` nach den Block
``||variables(sprites):setze mySprite||``. 
Damit kannst du den  ``||sprites:Player||`` Sprite auf dem Bildschirm bewegen.
Versuche dies im Spielsimulator 🕹️.

```blocks
let mySprite: Sprite = null
scene.setBackgroundColor(7)
mySprite = sprites.create(img`
. . . . . 5 5 5 5 5 5 . . . . .
. . . 5 5 5 5 5 5 5 5 5 5 . . .
. . 5 5 5 5 5 5 5 5 5 5 5 5 . .
. 5 5 5 5 5 5 5 5 5 5 5 5 5 5 .
. 5 5 5 f f 5 5 5 5 f f 5 5 5 .
5 5 5 5 f f 5 5 5 5 f f 5 5 5 5
5 5 5 5 5 5 5 5 5 5 5 5 5 5 5 5
5 5 5 5 5 5 5 5 5 5 5 5 5 5 5 5
5 5 5 5 5 5 5 5 5 5 5 5 5 5 5 5
5 5 f 5 5 5 5 5 5 5 5 5 5 f 5 5
5 5 5 f 5 5 5 5 5 5 5 5 f 5 5 5
. 5 5 5 f 5 5 5 5 5 5 f 5 5 5 .
. 5 5 5 5 f f f f f f 5 5 5 5 .
. . 5 5 5 5 5 5 5 5 5 5 5 5 . .
. . . 5 5 5 5 5 5 5 5 5 5 . . .
. . . . . 5 5 5 5 5 5 . . . . .
`, SpriteKind.Player)
// @highlight
controller.moveSprite(mySprite)
```