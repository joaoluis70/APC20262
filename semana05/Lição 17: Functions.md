Lição 17: Functions
#AVALIAÇÃO
//

```
var coin = createSprite(200, 10);
coin.setAnimation("coin_gold_1");
setCoin();

var bunny = createSprite(200, 350);
bunny.setAnimation("bunny1_ready_1");

var score = 0;

function draw() {

  // Muda o fundo quando chegar a 10 pontos
  if (score < 10) {
    simpleBackground();
  } else {
    sillyBackground();
  }

  if (keyDown("left")) {
    bunny.x = bunny.x - 2;
  }

  if (keyDown("right")) {
    bunny.x = bunny.x + 2;
  }

  if (coin.y > 400) {
    setCoin();
  }

  // Quando o coelho pega a moeda
  if (bunny.isTouching(coin)) {
    score = score + 1;
    setCoin();
  }

  textSize(20);
  text("Score: " + score, 10, 10, 100, 100);

  drawSprites();
}

function setCoin() {
  coin.x = randomNumber(50, 350);
  coin.y = 0;
  coin.velocityY = 3;
}

function simpleBackground() {
  background("lightblue");
  fill("green");
  rect(0, 370, 400, 30);
}

function sillyBackground() {
  background("pink");
  
  fill("yellow");
  ellipse(50, 50, 50, 50);
  
  fill("purple");
  ellipse(100, 100, 30, 30);
  
  fill("orange");
  ellipse(300, 80, 40, 40);
  
  fill("green");
  rect(0, 370, 400, 30);
  
  textSize(30);
  fill("red");
  text("10 COINS!!!", 110, 200);
}
```
