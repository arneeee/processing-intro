# classes and objects in programming

some basic reading: https://de.wikipedia.org/wiki/Klasse_(Objektorientierung)

code example: a class called **Particle** is instantiated twice

~~~~processing
Particle p1;
Particle p2;

void setup() {
  size(500, 500);
  frameRate(60);
  background(255);
  
  p1 = new Particle(250,250); // creating a object of class Particle
  p2 = new Particle(250,250); // creating another object of class Particle
} 

void draw() { 
  background(255);
  
  p1.changeColor(color(255,0,0));
  p1.moveY();
  p1.display();
  
  p2.changeColor(color(0,255,0));
  p2.moveX();
  p2.display();
  
}

class Particle {

  int x = 0;
  int y = 0;
  color clr = color(0);
  
  Particle(int x, int y) { //constructor
    this.x = x;
    this.y = y;
  }
  
  // here come the methods of the class
  void display() {
    fill(clr);
    ellipse(x,y,50,50);
  }
  
  void moveY() {
    this.y += 1 ;
  }
  
  void moveX() {
    this.x += 1 ;
  }

 void changeColor(color clr) {
    if (this.clr==color(0))
      this.clr = clr;
    else
      this.clr = color(0);
 }
}

~~~~
