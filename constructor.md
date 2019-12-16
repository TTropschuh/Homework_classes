```javascript

// Sketch from last Week modified with a constructor

let point1 = [];
let point2 = [];
let numLines = 20;



function setup() {
  createCanvas(400, 400);

  for (let i = 0; i < numLines; i++) {

    point1[i] = new Points();
  }
}

function draw() {
  background(0);
  for (let i = 0; i < point1.length; i++) {
    point1[i].display();
  }

  noLoop();
}


function Points(){
  this.x = random(50, 350),
  this.y = random(50, 350),

    this.display = function(){
    stroke(255);
    line(this.x, this.y, this.y, this.x);

        if (this.x > width / 2) {
          ellipse(this.x, this.y, 10);
        }

        if (this.x < width / 2) {
          ellipse(this.x, this.y, 10);}
  }
}
```
