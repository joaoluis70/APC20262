Lição 7 - Text
# Avaliação
//A atividade foi bem intuitiva. Os exercícios anteriores contribuiram para a sua finalização.

```javascript
var grass = createSprite(200,200);
grass.setAnimation("floating_grass");

var alien = createSprite(180,100);
alien.setAnimation("alien");
alien.scale = 1.3;

var robot = createSprite(300,300);
robot.setAnimation("robot");
robot.scale = 0.2;

drawSprites();

textSize(20);
fill("black");
text("It´s a amazing robot!", 150, 30);

textSize(15);
fill("black");
text("Oh! Butterflies", 270, 200);
```

# Desafio
//A atividade foi bem intuitiva. Os exercícios anteriores contribuiram para a sua finalização.
## Desafio 1

```javascript
var sky = createSprite(200,200);
sky.setAnimation("rainbow");
drawSprites();
textSize(50);
fill("red");
text("Rainbows", 30, 50);
fill("orange");
text("in the" , 70, 100);
fill("darkblue");
text("sky...", 110, 150);
fill("green");
textSize(20);
text("Clouds are so cool!", 200, 250);
```
## Desafio 2

```javascript
fill("white");
stroke("black");
strokeWeight(3);
textSize(20);
text("Four score and seven years ago...", 30, 200);
```
##Desafio 3

```javascript
textSize(50);
fill("black");
text("Four score and seven years ago...", 30, 200, 30, 200);
```
##Desafio 4

```javascript
background("black");
var alien = createSprite(200, 200);
alien.setAnimation("alienBlue_duck_1");
var planet = createSprite(250, 300);
planet.scale = 0.3;
planet.setAnimation("planet11_1");
var ufo = createSprite(200, 100);
ufo.setAnimation("ufo_1");
ufo.scale = 0.2;
drawSprites();
textSize(12);
stroke("blue");
fill("yellow");
text("It´s a nice place to conquer!", 200, 160);
```
