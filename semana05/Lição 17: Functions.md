Lição 17: Functions

#AVALIAÇÃO

// A atividade foi de fácil resolução.

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

#DESAFIO

//Gostei de realizar os desafios, e adicionar novas funcionalidades para o projeto foi bem intuitivo.
##DESAFIO 1
```
function draw() {
  if (World.mouseY > 200) {
    drawScene1();
  } else {
    drawScene2();
  }
}

function drawScene1() {
  background("skyblue");
 
  // Sol
  fill("yellow");
  ellipse(330, 70, 60, 60);
 
  // Chão
  fill("green");
  rect(0, 350, 400, 50);
 
  // Casa
  fill("red");
  rect(120, 230, 160, 120);
 
  // Telhado
  fill("brown");
  triangle(100, 230, 200, 150, 300, 230);
 
  // Porta
  fill("blue");
  rect(180, 280, 40, 70);
}

function drawScene2() {
  background("darkblue");
 
  // Lua
  fill("white");
  ellipse(330, 70, 60, 60);
 
  // Estrelas
  fill("yellow");
  ellipse(50, 50, 8, 8);
  ellipse(100, 100, 8, 8);
  ellipse(180, 50, 8, 8);
  ellipse(250, 120, 8, 8);
 
  // Chão
  fill("darkgreen");
  rect(0, 350, 400, 50);
 
  // Casa
  fill("purple");
  rect(120, 230, 160, 120);
 
  // Telhado
  fill("black");
  triangle(100, 230, 200, 150, 300, 230);
 
  // Porta
  fill("orange");
  rect(180, 280, 40, 70);
}
```
##DESAFIO 2
```
function draw() {
  if (World.mouseX < 200 && World.mouseY < 200) {
    drawSummerDay();
  } else if (World.mouseX > 200 && World.mouseY < 200) {
    drawSummerNight();
  } else if (World.mouseX < 200 && World.mouseY > 200) {
    drawWinterDay();
  } else {
    drawWinterNight();
  }
}

function drawSummerDay() {
  background("skyblue");

  fill("yellow");
  ellipse(330, 70, 60, 60);

  fill("green");
  rect(0, 350, 400, 50);

  fill("red");
  rect(120, 230, 160, 120);

  fill("brown");
  triangle(100, 230, 200, 150, 300, 230);

  fill("blue");
  rect(180, 280, 40, 70);
}

function drawSummerNight() {
  background("darkblue");

  fill("white");
  ellipse(330, 70, 60, 60);

  fill("yellow");
  ellipse(50, 50, 8, 8);
  ellipse(100, 100, 8, 8);
  ellipse(200, 50, 8, 8);
  ellipse(300, 120, 8, 8);

  fill("darkgreen");
  rect(0, 350, 400, 50);

  fill("purple");
  rect(120, 230, 160, 120);

  fill("black");
  triangle(100, 230, 200, 150, 300, 230);

  fill("orange");
  rect(180, 280, 40, 70);
}

function drawWinterDay() {
  background("lightgray");

  fill("yellow");
  ellipse(330, 70, 50, 50);

  fill("white");
  rect(0, 350, 400, 50);

  fill("lightblue");
  rect(120, 230, 160, 120);

  fill("white");
  triangle(100, 230, 200, 150, 300, 230);

  fill("brown");
  rect(180, 280, 40, 70);

  ellipse(50, 100, 10, 10);
  ellipse(100, 180, 10, 10);
  ellipse(300, 150, 10, 10);
  ellipse(350, 250, 10, 10);
}

function drawWinterNight() {
  background("midnightblue");

  fill("white");
  ellipse(330, 70, 60, 60);

  ellipse(50, 50, 8, 8);
  ellipse(100, 100, 8, 8);
  ellipse(200, 50, 8, 8);
  ellipse(300, 120, 8, 8);

  fill("white");
  rect(0, 350, 400, 50);

  fill("lightblue");
  rect(120, 230, 160, 120);

  fill("white");
  triangle(100, 230, 200, 150, 300, 230);

  fill("brown");
  rect(180, 280, 40, 70);
}
```
