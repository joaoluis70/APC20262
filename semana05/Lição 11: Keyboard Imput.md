Lição 11: Keyboard Imput
//O desafio foi de fácil resolução, pois as atividades anteriores ajudaram.

#DESAFIO
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



