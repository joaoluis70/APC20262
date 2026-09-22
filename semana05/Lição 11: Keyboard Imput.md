Lição 11: Keyboard Imput
//O desafio foi de fácil resolução, pois as atividades anteriores ajudaram.

#AVALIAÇÃO
```javascript
var backdrop = createSprite(200,200);
backdrop.setAnimation("rainbow");
var flyer = createSprite(200,200);
flyer.setAnimation("wing_bot");

function draw() {
  if (keyDown("left")) {
    flyer.x = flyer.x - 3;
  }
  if (keyDown("right")) {
    flyer.x = flyer.x + 3;
  }
  if (keyDown("up")) {
    flyer.y = flyer.y - 3;
  }
  if (keyDown("down")) {
    flyer.y = flyer.y + 3;
  }
  
  drawSprites();
}
```
#DESAFIO

##DESAFIO 1

```javascript
var clicks = 0;

function draw() {
  // add clicks when the space bar is pressed
  if (keyWentDown("space")) {
      clicks = clicks + 1;
  }
  background("white");
  textSize(50);
  text(clicks, 165, 175, 70, 50);
}
```

##DESAFIO 2



