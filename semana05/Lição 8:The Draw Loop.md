#Avaliação

\\ Tive dificuldade para adicionar o movimento ao objeto, mas revendo as outras atividades consegui fazer.

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
