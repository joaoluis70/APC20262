Lição 14: Collision Detection

#AVALIAÇÃO
//A avaliação foi bem tranquila.
```
// create the sprites
var horse = createSprite(200, 150);
horse.setAnimation("horse");

var rainbow = createSprite(0, 400);
rainbow.setAnimation("rainbow");
rainbow.velocityY = -5;
rainbow.velocityX = 5;
rainbow.rotateToDirection = true;

function draw() {
  // draw the background
  background("skyblue");

  // change the horse to a unicorn when the rainbow touches it
  if (rainbow.isTouching(horse)) {
    horse.setAnimation("unicorn");
  }

  drawSprites();
}
```
#DESAFIO
//Não tive dificuldades para fazer os desafios.
##DESAFIO 1
```
var roller = createSprite(200, 200);
roller.scale = 2;
roller.setAnimation("roller_1");

// Use .setCollider() with all 6 parameters.
roller.setCollider("rectangle", 0, 0, 50, 100, 45);

roller.debug = true;
drawSprites();
```

##DESAFIO 2
```
var points = 0;
var coin = createSprite(200, 100);
coin.setAnimation("coin");

var ghost = createSprite(200, 300);
ghost.setAnimation("ghost");

function draw() {
  if (ghost.isTouching(coin)) {
    points = points + 1;
    coin.x = randomNumber(50, 350);
    coin.y = randomNumber(50, 350);
  }
 
  background("lightblue");
  text("Points: " + points, 25, 25);
 
  if(keyDown("up")) {
    ghost.y = ghost.y - 5;
  }
 
  if(keyDown("down")) {
    ghost.y = ghost.y + 5;
  }
 
  if(keyDown("left")) {
    ghost.x = ghost.x - 5;
  }
 
  if(keyDown("right")) {
    ghost.x = ghost.x + 5;
  }
 
  drawSprites();
}
```

##DESAFIO 3

```
// GAME SETUP

// Create the sprites
var frog = createSprite(100, 300);
frog.setAnimation("frog");

var fly = createSprite(450, 150);
fly.setAnimation("fly");

var mushroom = createSprite(450, 300);
mushroom.setAnimation("mushroom");

// set velocity for the obstacle and the target
fly.velocityX = -5;
mushroom.velocityX = -5;

// create the variables
var score = 0;
var health = 100;

function draw() {

  // BACKGROUND
  background("skyblue");

  // ground
  fill("green");
  rect(0, 350, 400, 50);

  // SPRITE INTERACTIONS

  // if the player touches the obstacle
  // the health goes down, and the obstacle turns
  if (frog.isTouching(mushroom)) {
    health = health - 1;
    mushroom.rotation = mushroom.rotation + 5;
  }

  // if the frog touches the fly
  // the score goes up, the fly resets
  if (frog.isTouching(fly)) {
    score = score + 1;
    fly.x = 450;
    fly.y = randomNumber(100, 250);
  }

  // JUMPING

  // if the player has reached the ground
  // stop moving down
  if (frog.y >= 300) {
    frog.y = 300;
    frog.velocityY = 0;
  }

  // if the player presses the up arrow
  // start moving up
  if (keyDown("up") && frog.y >= 300) {
    frog.velocityY = -10;
  }

  // if the player reaches the top of the jump
  // start moving down
  if (frog.y < 150) {
    frog.velocityY = 5;
  }

  // LOOPING

  // if the obstacle has gone off the left hand side
  // move it to the right hand side
  if (mushroom.x < -50) {
    mushroom.x = 450;
  }

  // if the target has gone off the left hand side
  // move it to the right hand side
  if (fly.x < -50) {
    fly.x = 450;
    fly.y = randomNumber(100, 250);
  }

  // DRAW SPRITES
  drawSprites();

  // SCOREBOARD
  fill("black");
  textSize(20);
  text("Score:", 25, 30);
  text(score, 90, 30);

  text("Health:", 280, 30);
  text(health, 350, 30);

  // GAME OVER
  if (health <= 0) {
    background("black");
    fill("green");
    textSize(50);
    text("Game Over!", 40, 200);
  }
}
```
