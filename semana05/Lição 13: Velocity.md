Lição 13: Velocity

#AVALIAÇÃO
//Os exercicios anteriores à avaliação deixaram a realização mais simples.
```
var fish = createSprite(200, 200);
fish.setAnimation("fishR");
fish.velocityX = 4;

function draw() {
  background("blue");

  if (keyWentDown("right")) {
    fish.velocityX = 4;
    fish.setAnimation("fishR");
  }

  if (fish.x > 400) {
    fish.velocityX = -4;
    fish.setAnimation("fishL");
  }

  if (fish.x < 0) {
    fish.velocityX = 0;
    fish.setAnimation("fishL");
  }
```

##DESAFIO
//Os exercicios anteriores ao desafio deixaram a realização mais simples.
#DESAFIO 1
```
var alien = createSprite(50,200);
alien.setAnimation("alien");
alien.velocityX = 0;
alien.velocityY = -5;

function draw() {
  if (alien.y < 50) {
    alien.velocityY = 0;
    alien.velocityX = 5;
  }

  if (alien.x > 350) {
    alien.velocityX = 0;
    alien.velocityY = 5;
  }

  if (alien.y > 350) {
    alien.velocityY = 0;
    alien.velocityX = -5;
  }

  if (alien.x < 50) {
    alien.velocityX = 0;
    alien.velocityY = -5;
  }
  
  drawSprites();
}

var space = createSprite(200, 200);
space.setAnimation("space");

var flag1 = createSprite(50, 50);
flag1.setAnimation("yellow_flag");

var flag2 = createSprite(350, 50);
flag2.setAnimation("yellow_flag");

var flag3 = createSprite(350, 350);
flag3.setAnimation("yellow_flag");

var flag4 = createSprite(50, 350);
flag4.setAnimation("yellow_flag");

alien.depth = 7;
```

#DESAFIO 2
```
var space = createSprite(200, 200);
space.setAnimation("space");

var ship = createSprite(50, 200);
ship.setAnimation("alien");
ship.velocityX = 3;
ship.velocityY = 0;

function draw() {
  background("black");

  if (ship.x > 350) {
    ship.velocityX = 0;
    ship.velocityY = 3;
  }

  if (ship.y > 350) {
    ship.velocityY = 0;
    ship.velocityX = -3;
  }

  if (ship.x < 50) {
    ship.velocityX = 0;
    ship.velocityY = -3;
  }

  if (ship.y < 50) {
    ship.velocityY = 0;
    ship.velocityX = 3;
  }

  drawSprites();
}
```
  drawSprites();
}
