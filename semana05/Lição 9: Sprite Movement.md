Lição 9: Sprite Movement
// A avaliação não apresentou dificuldades.
## Avaliação
```javascript
var orangeFish = createSprite(400, randomNumber(0, 100));
orangeFish.setAnimation("orange_fish");
var blueFish = createSprite(250, randomNumber(0, 200));
blueFish.setAnimation("blue_fish");
var greenFish = createSprite(300, randomNumber(200, 300));
greenFish.setAnimation("green_fish");

function draw() {
  // Draw Background
  background("navy");
  
  // Update Values
  orangeFish.x = orangeFish.x - 2;
  blueFish.x = blueFish.x - 5;
  greenFish.x = greenFish.x - 1;
  
  // Draw Animations
  drawSprites();
}
```

## Desafio
//
# Desafio 1
```javascript
var orangeFish = createSprite(400, randomNumber(0, 100));
orangeFish.setAnimation("orange_fish");
var blueFish = createSprite(250, randomNumber(0, 200));
blueFish.setAnimation("blue_fish");
var greenFish = createSprite(300, randomNumber(200, 300));
greenFish.setAnimation("green_fish");

function draw() {
  // Draw Background
  background("navy");
  
  // Update Values
  orangeFish.x = orangeFish.x - 2;
  blueFish.x = blueFish.x - 5;
  greenFish.x = greenFish.x - 1;
  
  orangeFish.rotation = randomNumber(0, 5);
  blueFish.rotation = randomNumber(1, 10);
  greenFish.rotation = randomNumber(2, 6);
  // Draw Animations
  drawSprites();
}
```
# Desafio 2
```javascript
var orangeFish = createSprite(400, randomNumber(0, 100));
orangeFish.setAnimation("orange_fish");
var blueFish = createSprite(250, randomNumber(0, 200));
blueFish.setAnimation("blue_fish");
var greenFish = createSprite(300, randomNumber(200, 300));
greenFish.setAnimation("green_fish");
var bubble = createSprite(200, 400);
bubble.setAnimation("bubble_1");

function draw() {
  // Draw Background
  background("navy");
  
  // Update Values
  orangeFish.x = orangeFish.x - 2;
  blueFish.x = blueFish.x - 5;
  greenFish.x = greenFish.x - 1;
  
  orangeFish.rotation = randomNumber(0, 5);
  blueFish.rotation = randomNumber(1, 10);
  greenFish.rotation = randomNumber(2, 6);
  bubble.y = bubble.y - 1;
  bubble.scale = 0.2;
  bubble.rotation = randomNumber(10, 20);
  noFill();
  stroke("blue");
  strokeWeight(1);
  ellipse(200, 200, 200, 200);
  // Draw Animations
  drawSprites();
}
```
# Desafio 3

```javascript
var alien = createSprite(200, 200);
alien.setAnimation("alienBlue_duck_1");
var planet = createSprite(250, 300);
planet.scale = 0.3;
planet.setAnimation("planet11_1");
var ufo = createSprite(200, 100);
ufo.setAnimation("ufo_1");
ufo.scale = 0.2;
function draw() {
  background("black");
  fill("yellow");
  stroke("blue");
  textSize(12);
  text("It´s a nice place to conquer!", 200, 160);
  ufo.x = ufo.x + 1;
  alien.rotation = alien.rotation + 5;
  planet.rotation = planet.rotation - 5;
  drawSprites();
}
```
