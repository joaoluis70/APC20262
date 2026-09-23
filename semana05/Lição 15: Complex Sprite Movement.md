Lição 15: Complex Sprite Movement

#Avaliação

```
var rock = createSprite(200, 350);
rock.setAnimation("rock");
rock.velocityY = -10;
rock.rotationSpeed = 2;

function draw() {
  background("skyblue");

  // update sprites
  rock.velocityY = rock.velocityY + 0.5;

  drawSprites();
}
```

##DESAFIO


#DESAFIO 1
```
var plane = createSprite(50, 350);
plane.setAnimation("plane");

var rock = createSprite(150, 350);
rock.setAnimation("rock");

var rockdown = createSprite(350, 100);
rockdown.setAnimation("rock_down");

plane.velocityY = -15;
plane.velocityX = 3;

function draw() {
  background("lightblue");
 
  plane.velocityY = plane.velocityY + 0.5;
 
  drawSprites();
}
```

#DESAFIO 2
```
var car = createSprite(200, 350);
car.setAnimation("car");

car.velocityY = -15;

function draw() {
  background("forestgreen");
  fill("gray");
  rect(150, 0, 100, 400);

  // Make the Y velocity more downward
  car.velocityY = car.velocityY + 0.5;

  // Prevent the car from moving backwards
  if (car.velocityY > 0) {
    car.velocityY = 0;
  }

  drawSprites();
```

##DESAFIO 3
```
var plane = createSprite(50, 350);
plane.setAnimation("plane");

var rock = createSprite(150, 350);
rock.setAnimation("rock");

var rock2 = createSprite(300, 350);
rock2.setAnimation("rock");

plane.velocityY = -9;
plane.velocityX = 3;

function draw() {
  background("lightblue");

  plane.velocityY = plane.velocityY + 0.5;

  if (plane.x > 120 && plane.x < 180 && plane.y > 250) {
    plane.velocityY = -9;
  }

  if (plane.x > 270 && plane.x < 330 && plane.y > 250) {
    plane.velocityY = -9;
  }

  drawSprites();
}
```
}
```
