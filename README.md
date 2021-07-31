var sea,seaImage;
var ship,shipImage
function preload(){
  sea=loadImage("sea.png");
  
  ship=loadAnimation("ship-1.png","ship-2.png");
  
 

}

function setup(){
  createCanvas(400,400);
  seaImage=createSprite(200,200)
  seaImage.addImage(sea);
  seaImage.scale=0.25;
  seaImage.velocityX=-2;
  shipImage=createSprite(90,180,150,100);
  shipImage.addAnimation("going",ship);
  shipImage.scale=0.2;
 
  
  


  
  
}

function draw() {
  background("blue");
  if(seaImage.x<0){
    seaImage.x=300
  }

 drawSprites();
}
