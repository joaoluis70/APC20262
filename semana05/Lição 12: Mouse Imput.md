Lição 12: Mouse Imput

#AVALIAÇÃO
```
var backdrop = createSprite(200,200);
backdrop.setAnimation("sky");

var creature = createSprite(200,250);
creature.setAnimation("creature");
creature.scale = 0.2;

function draw() {
  
  // shake the sprite when the mouse is pressed
  if (mouseDown()) {
    creature.rotation = randomNumber(-5,5);
  }

  drawSprites();

  // display the text when the mouse is NOT pressed
  if (!mouseDown()) {
    fill("black");
    textSize(40);
    text("Press the mouse to shake the creature.", 20, 50, 360, 100);
  }
}
```
#DESAFIO

##DESAFIO 1

```
var spiral = createSprite(100,200);
spiral.setAnimation("lollipop");

var spiral2 = createSprite(300,200);
spiral2.setAnimation("lollipop2");

function draw() {
  background("pink");

  if (mouseDown()) {
    spiral.scale = spiral.scale * 1.01;
    spiral.rotation = spiral.rotation - 3;
    spiral2.scale = spiral2.scale / 1.01;
    spiral2.rotation = spiral2.rotation + 3;
  } else {
    spiral.scale = spiral.scale / 1.01;
    spiral.rotation = spiral.rotation + 3;
    spiral2.scale = spiral2.scale * 1.01;
    spiral2.rotation = spiral2.rotation - 3;
  }

  drawSprites();
}
```

##DESAFIO 2

```
var bee = createSprite(200, 200);
bee.setAnimation("bee");

function draw() {
  background("skyblue");
 
  bee.x = World.mouseX;
  bee.y = World.mouseY;
 
  drawSprites();
}
```
##DESAFIO 3
```
var bee = createSprite(200, 200);
bee.setAnimation("bee");

var bee2 = createSprite(200, 200);
bee2.setAnimation("bee");

var bee3 = createSprite(200, 200);
bee3.setAnimation("bee");

var bee4 = createSprite(200, 200);
bee4.setAnimation("bee");

function draw() {
  background("skyblue");
 
  bee.x = World.mouseX + randomNumber(-50, 50);
  bee.y = World.mouseY + randomNumber(-50, 50);

  bee2.x = World.mouseX + randomNumber(-50, 50);
  bee2.y = World.mouseY + randomNumber(-50, 50);

  bee3.x = World.mouseX + randomNumber(-50, 50);
  bee3.y = World.mouseY + randomNumber(-50, 50);

  bee4.x = World.mouseX + randomNumber(-50, 50);
  bee4.y = World.mouseY + randomNumber(-50, 50);
 
  drawSprites();
}
```

##DESAFIO 4
```
```

##DESAFIO 5
```
```
