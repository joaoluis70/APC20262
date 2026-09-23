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
}
```
