# ObjectOrientationIntroduction

## What is Object Orientation

## Arduino and Breadboard Setup

## The Domain

Lights
  * basic light
  * blinking light
  * light switch - that can switch both of the above lights on
  
## Breadboard setup

## Javascript Objects

Object literals
Javascript don't have classes
Simulate classes using functions

### Function scope

### 'this' in Javascript

###Inheritence

We will use constructor stealing

```javascript 
var Vehicle = function(regNo){
  var speed = 0;
  
  this.regNo = regNo;
  
  this.accelerate = function(){
    speed += 10;
  };
  
  this.currentSpeed = function(){
    return speed;
  };
}

var Golf = function(regNo){
  Vehicle.call(this, regNo);
};


var golf1 = new Golf('CY 670 234');
console.log(golf1.regNo);

golf1.accelerate();
golf1.accelerate();
golf1.accelerate();

// print 30
console.log(golf1.currentSpeed());


```

### Composition

Create an object that reference other objects
