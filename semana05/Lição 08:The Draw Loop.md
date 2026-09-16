Lição 8:The Draw Loop
# Avaliação

// Tive dificuldade para adicionar o movimento ao objeto, mas revendo as outras atividades consegui fazer.

```javascript
background("skyblue");

var salt = createSprite(200, 200);
salt.setAnimation("salt");

function draw() {
  salt.rotation = 180;
  salt.x = 200;
  salt.y = randomNumber(200, 210);
  drawSprites();
}
```
# Desafio
//Tive facilidade em realizar a atividade.

## Desafio 1

```javascript
background("black");
var alien = createSprite(200, 200);
alien.setAnimation("alienBlue_duck_1");
var planet = createSprite(250, 300);
planet.scale = 0.3;
planet.setAnimation("planet11_1");
var ufo = createSprite(200, 100);
ufo.setAnimation("ufo_1");
ufo.scale = 0.2;
drawSprites();
textSize(12);
stroke("blue");
fill("yellow");
text("It´s a nice place to conquer!", 200, 160);
function draw() {
  background("black");
  alien.rotation = randomNumber(20, 100);
  alien.x = randomNumber(200, 210);
```
## Desafio 2
```javascript
background("skyblue");
var cloud = createSprite(200, 100);
cloud.setAnimation("cloud_1");
var plane1 = createSprite(200, 200);
plane1.setAnimation("planeBlue1_1");
function draw() {
  cloud.x = randomNumber(200, 203);
  cloud.scale = 0.2;
  plane1.x = randomNumber(200, 205);
  drawSprites();
}
```
