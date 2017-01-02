# 01-intro

## getting started

### basic structure of a processing sketch

~~~~processing
int p = 0;

void setup() { // this function is only called once at the start
  size(500, 500);   // provides a window of the size 500 x 500
  frameRate(60);    // 24 frames per second
  //smooth
} 

void draw() { // this function is called continually
  
    ellipse(250, 250, 50, 50); // a circle is drawn at 250,250 (center of window), radius: 50

}
// the circle will stand still - it is continuously reprinted at the same position
~~~~

### interaction - binding mouse coords

~~~~processing
int p = 0;

void setup() {
  size(500, 500);
  frameRate(60);
  //smooth
} 

void draw() { 
    //background(0);
    ellipse(mouseX, mouseY, 50, 50);
}
~~~~

### auto-motive

~~~~processing
int p = 0; // counter 

void setup() {
  size(500, 500);
  frameRate(60);
} 

void draw() { 
    //background(0);
    ellipse(250, 0+p, 50, 50);
    p = p + 1;
}
~~~~

### some colors

~~~~processing
int p = 0;

void setup() {
  size(500, 500);
  frameRate(24);
} 

void draw() { 
  background(255);
  fill(255,0.5*p); // red,green,blue: running from 0 - 255; binding fill color to counter variable
  ellipse(250, 0+p, 50, 50); 
  p = p + 1;
}
~~~~

### manifold with for loops

~~~~processing
int p = 0;

void setup() {
  size(500, 500);
  frameRate(24);
} 

void draw() { 
  //background(255);
  noStroke();
  for (int i = 0; i < 5; i++) {
    fill(255 - (0.5 * p), 50 * i, 0.5 * p);
    ellipse(95 + i * 70, 0+p, 50, 50);
  }
  p = p + 1;  
}
~~~~

### randomized

~~~~processing
int p = 0;

void setup() {
  size(500, 500);
  frameRate(60);
  background(255);
} 

void draw() { 
  //background(255);
  noStroke();  
  fill(random(255), random(255), random(255));
  ellipse(random(500), random(500), 10, 10);
}
~~~~

### now get creative and combine!

some more elements:

~~~~processing
line(x1,y1,x2,y2); //line

rect(x,y,width,height); //rectangle

 if (mousePressed) {
    fill(0.5 * mouseX, 0.5 * mouseY, 150);
    ellipse(mouseX, mouseY, 40, 40);
 }

~~~~
