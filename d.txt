
var mouse, mouseImg, stopM , startM;
var cat, catImg, stopC, startC;
var backgroundImg;

function preload() {
    //load the images here
    catImg = loadAnimation("images/cat2.png","images/cat3.png");
    mouseImg = loadAnimation("images/mouse1.png","images/mouse2.png");
    backgroundImg = loadImage("images/garden.png");

    stopM = loadAnimation("images/mouse4.png");
    stopC = loadAnimation("images/cat4.png")

    startM = loadImage("images/mouse1.png");
    startC = loadImage("images/cat1.png");
}

function setup(){
    createCanvas(1000,800);
    //create tom and jerry sprites here
    cat = createSprite(800,650,20,20);
    cat.addImage("cat",startC);
    cat.scale = 0.2;

    mouse = createSprite(100,650,20,20);
    mouse.addImage("mouse",startM);
    mouse.scale = 0.1;

}

function draw() {

    background(backgroundImg);
    //Write condition here to evalute if tom and jerry collide

    keyPressed();
    drawSprites();
}


function keyPressed(){

  //For moving and changing animation write code here
  if(keyWentDown("W")){
      cat.addAnimation("cat1",catImg);
      mouse.addAnimation("mouse1",mouseImg);
  }


}
