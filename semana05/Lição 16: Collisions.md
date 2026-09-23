Lição 16: Collisions

#AVALIAÇÃO
// A avaliação foi de fácil resolução.
```
// create sprites
var giraffe = createSprite(50, 50);
giraffe.setAnimation("giraffe");
giraffe.velocityX = 3;

var hippo = createSprite(50, 150);
hippo.setAnimation("hippo");
hippo.velocityX = 3;

var rabbit = createSprite(50, 250);
rabbit.setAnimation("rabbit");
rabbit.velocityX = 3;

var snake = createSprite(50, 350);
snake.setAnimation("snake");
snake.velocityX = 3;

var parrot = createSprite(350, 50);
parrot.setAnimation("parrot");
parrot.velocityX = -3;

var elephant = createSprite(350, 150);
elephant.setAnimation("elephant");
elephant.velocityX = -3;

var monkey = createSprite(350, 250);
monkey.setAnimation("monkey");
monkey.velocityX = -3;

var pig = createSprite(350, 350);
pig.setAnimation("pig");
pig.velocityX = -3;

function draw() {
  background("lightblue");

  giraffe.bounceOff(parrot);
  hippo.bounceOff(elephant);
  rabbit.bounceOff(monkey);
  snake.bounceOff(pig);

  drawSprites();
}
```
#DESAFIO
//Os desafios foram bem divertidos e pude aprender bastante.
##DESAFIO 1
```
var goldCoin = createSprite(51, 50);
goldCoin.setAnimation("gold_coin");
goldCoin.velocityX = 2;
goldCoin.velocityY = 2;
goldCoin.debug = true;

var silverCoin = createSprite(350, 350);
silverCoin.setAnimation("silver_coin");
silverCoin.velocityX = -2;
silverCoin.velocityY = -2;
silverCoin.debug = true;

function draw() {
  background("darkgreen");
 
  goldCoin.bounce(silverCoin);
 
  drawSprites();
}
```
##DESAFIO 2
```
var goldCoin = createSprite(49, 50);
goldCoin.setAnimation("gold_coin");
goldCoin.velocityX = 2;
goldCoin.velocityY = 2;
goldCoin.debug = true;
goldCoin.setCollider("circle");

var silverCoin = createSprite(350, 350);
silverCoin.setAnimation("silver_coin");
silverCoin.velocityX = -2;
silverCoin.velocityY = -2;
silverCoin.debug = true;
silverCoin.setCollider("circle");

function draw() {
  goldCoin.bounce(silverCoin);

  background("darkgreen");
  drawSprites();
}
```
##DESAFIO 3
```
var basketball = createSprite(100, 0);
basketball.setAnimation("basketball");
basketball.bounciness = 0.8;

var soccerball = createSprite(225, 0);
soccerball.setAnimation("soccerball");
soccerball.bounciness = 0.4;

var poolball = createSprite(325, 0);
poolball.setAnimation("poolball");
poolball.bounciness = 0.4;

var wood = createSprite(200, 375);
wood.setAnimation("floor");

function draw() {
  background("skyblue");

  basketball.bounceOff(wood);
  soccerball.bounceOff(wood);
  poolball.bounceOff(wood);

  basketball.velocityY = basketball.velocityY + 0.2;
  soccerball.velocityY = soccerball.velocityY + 0.2;
  poolball.velocityY = poolball.velocityY + 0.2;

  drawSprites();
}
```
##DESAFIO 4
```
// GAME SETUP
// create player, target, and obstacles

var player = createSprite(200, 100);
player.setAnimation("fly_bot");
player.scale = 0.8;

var coin = createSprite(350, 200);
coin.setAnimation("coin");
coin.scale = 0.5;

var rock = createSprite(-50, 150);
rock.setAnimation("rock");
rock.scale = 0.7;
rock.velocityX = 3;

var rock2 = createSprite(200, -50);
rock2.setAnimation("rock");
rock2.scale = 0.7;
rock2.velocityY = 3;


function draw() {
  background("lightblue");

  // FALLING
  player.velocityY = player.velocityY + 0.3;

  // LOOPING

  // horizontal rock
  if (rock.x > 450) {
    rock.x = -50;
    rock.y = randomNumber(50, 350);
  }

  // vertical rock
  if (rock2.y > 450) {
    rock2.y = -50;
    rock2.x = randomNumber(50, 350);
  }

  // PLAYER CONTROLS

  // change the y velocity when the user clicks "up"
  if (keyDown("up")) {
    player.velocityY = -5;
  }

  // decrease the x velocity when user clicks "left"
  if (keyDown("left")) {
    player.velocityX = player.velocityX - 0.5;
  }

  // increase the x velocity when user clicks "right"
  if (keyDown("right")) {
    player.velocityX = player.velocityX + 0.5;
  }

  // SPRITE INTERACTIONS

  // reset the coin when the player touches it
  if (player.isTouching(coin)) {
    coin.x = randomNumber(50, 350);
    coin.y = randomNumber(50, 350);
  }

  // make the obstacles push the player
  player.bounceOff(rock);
  player.bounceOff(rock2);

  // DRAW SPRITES
  drawSprites();

  // GAME OVER
  if (player.x < -50 || player.x > 450 || player.y < -50 || player.y > 450) {
    background("black");
    textSize(50);
    fill("green");
    text("Game Over!", 50, 200);
  }
}
```
