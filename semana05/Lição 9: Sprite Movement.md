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

# Desafio 3
