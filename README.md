# An-Arduino-circuit-controlling-5-Servo-motor  
**Task 1,2.** An Arduino circuit controlling 5 Servo-motor to rotate 90° and then back to 0° via slidebutton simulated in TinkerCad (circuit and code)    
  
   **A. The code**  

```ruby
// C++ code
//
# include <Servo.h>


Servo A;
Servo B;
Servo C;
Servo D;
Servo E;

void setup()
{ 
  pinMode(13,INPUT);
   A.attach(11);
   B.attach(10);
   C.attach(9);
   D.attach(6);
   E.attach(5);
 
}

void loop()
{ 
  if (digitalRead(13)==HIGH)
  { A.write(90);
   B.write(90);
   C.write(90);
   D.write(90);
   E.write(90);}
  else
  {
   A.write(0);
   B.write(0);
   C.write(0);
   D.write(0);
   E.write(0); }
 
}

  
 

 

  ```  
  
 **B. The circuit**  
   
   
 
 ![Circuit](images/Screenshot(207).png)
 
  **C. The simulation design**  
  
   [Click here to show the project in TinkerCad](https://www.tinkercad.com/things/hg8uKSnk0X8)     
     
       ...  
       
     
**Task 3.** An Arduino circuit controlling 5 Servo-motor via potentiometer simulated in TinkerCad (circuit and code)

 **A. The code**  

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
  
 **B. The circuit**  
   
   
 
 ![Circuit](images/Screenshot(206).png)
 
  **C. The simulation design**  
  
   [Click here to show the project in TinkerCad](https://www.tinkercad.com/things/1HIFasACAva)   
     
            
                 
     
       
         

  
