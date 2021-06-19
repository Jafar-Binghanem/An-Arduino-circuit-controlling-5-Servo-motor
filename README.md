# An-Arduino-circuit-controlling-5-Servo-motor
An Arduino circuit controlling 5 Servo-motor to rotate 90° simulated in TinkerCad (circuit and code)

 **1. The code**  

```ruby
// C++ code
//
# include <Servo.h>

int scale1,scale2,scale3,scale4,scale5;
int ang1,ang2,ang3,ang4,ang5;

Servo A;
Servo B;
Servo C;
Servo D;
Servo E;
void setup()
{ 
   pinMode(A0,INPUT);
   pinMode(A1,INPUT);
   pinMode(A2,INPUT);
   pinMode(A3,INPUT);
   pinMode(A4,INPUT);
   A.attach(11);
   B.attach(10);
   C.attach(9);
   D.attach(6);
   E.attach(5);
 
}

void loop()
{ 
   scale1=analogRead(A0);
   scale2=analogRead(A1);
   scale3=analogRead(A2);
   scale4=analogRead(A3);
   scale5=analogRead(A4);
   ang1=map(scale1,0,1023,0,180);
   ang2=map(scale2,0,1023,0,180);
   ang3=map(scale3,0,1023,0,180);
   ang4=map(scale4,0,1023,0,180);
   ang5=map(scale5,0,1023,0,180); 
  
   A.write(ang1);
   B.write(ang2);
   C.write(ang3);
   D.write(ang4);
   E.write(ang5);
   delay(50);
}
  ```  
  
 **2. The circuit**  
   
   
 
 ![Circuit](images/Screenshot-task1.png)
 
  **3. The simulation design**  
  
   [Click here to show the project in TinkerCad](https://www.tinkercad.com/things/1HIFasACAva)
  
