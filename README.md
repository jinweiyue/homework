float c1=100;
float c2=100;
void setup() {
  frameRate(10);
  size(1000, 1000);
  background(255);
}
void draw() {
  //fill(0,100);
  //rect(0,0,width,height);
  for (int i=0; i<=3; i+=1) { 
      //fill(random(0, 255),random(0, 255),random(0, 255));
      //ellipse(width/2, height, c1, c2);
      c1=random(0,1000);
      c2=c1;
      if (c1>=800){
        fill(random(0, 255),random(0, 255),random(0, 255));
        rect(random(0, 1000),random(0, 1000),random(0, 1000),random(0, 1000));
        fill(random(0, 255),random(0, 255),random(0, 255));
        triangle(random(0, 1000),random(0, 1000),random(0, 1000),random(0, 1000),random(0, 1000),random(0, 1000));
      }
      fill(random(0, 255),random(0, 255),random(0, 255));
      ellipse(width/2,height/2, c1, c2);
      noStroke();
      int x=0;
      int y=0;
      while(x+100<=width){
        fill(random(0, 255),random(0, 255),random(0, 255),50);
        rect(x,y,100,100);
        noStroke();
        y=0;
        while(y+100<=width){
          fill(random(0, 255),random(0, 255),random(0, 255),50);
          rect(x,y,100,100);
          noStroke();
          y+=100;
        }
        x+=100;
      }
      //ellipse(mouseX,mouseY, c1, c2);
  }
}
