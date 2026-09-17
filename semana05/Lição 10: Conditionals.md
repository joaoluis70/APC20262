Lição 10: Conditionals

## Avaliação
// As atividades anteriores tornaram esses exercício mais fácil.
```javascript
var backdrop = createSprite(200,200);
backdrop.setAnimation("sci_fi");
var dinosaur = createSprite(200, 350);
dinosaur.scale = 0.2;
dinosaur.setAnimation("tyrannosaurus");

function draw() {
  //move the dinosaur up
  dinosaur.y = dinosaur.y - 5;

  //if it gets to the sky, turn it into a pterodactyl
  if (dinosaur.y < 100) {
    dinosaur.setAnimation("pterodactyl");
  }

  //draw everything
  drawSprites();
}
```
## Desafio
# Desafio 1

```javascript
var balloon = createSprite(200, 200);
balloon.setAnimation("balloon");
balloon.scale = 0.1;

var pop = createSprite(200, 200);
pop.setAnimation("pop");
pop.visible = false;

function draw() {
  background("white");

  balloon.scale = balloon.scale + 0.001;

  if (balloon.scale >= 0.5) {
    balloon.visible = false;
    pop.visible = true;
  }

  drawSprites();
}
```
# Desafio 2
```javascript
var balloon = createSprite(200, 200);
balloon.setAnimation("beachball_1");
balloon.scale = 0.1;

var pop = createSprite(200, 200);
pop.setAnimation("animation_1");
pop.visible = false;

function draw() {
  background("white");
 
  balloon.scale = balloon.scale + 0.001;
 
  if (balloon.scale >= 0.5) {
    balloon.visible = false;
    pop.visible = true;
  }
 
  drawSprites();
}
```
