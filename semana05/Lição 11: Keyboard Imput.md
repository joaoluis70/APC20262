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
\\ Tive dificuldade em enteder que era pra criar 4 cópias do inseto em animações. Quando descobri ficou fácil.
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

```javascript
var bug = createSprite(200, 200);
bug.setAnimation("fly");

function draw() {
  //Draw Background
  background("white");
  
  // Update Values
  if(keyDown("up")){
    bug.y = bug.y - 5;
    bug.setAnimation("fly_up");

  }
  if(keyDown("down")){
    bug.y = bug.y + 5;
    bug.setAnimation("fly_down");

  }
  if(keyDown("left")){
    bug.x = bug.x - 5;
    bug.setAnimation("fly_left");
  }
  if(keyDown("right")){
    bug.x = bug.x + 5;
    bug.setAnimation("fly_right");
  }

  //Draw Animations
  drawSprites();
}
```
##DESAFIO 3 

```javascript
