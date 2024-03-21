###  DATE: 13/03/2024

###  NAME: sugavarathan.l
###  ROLL NO :212221220051
###  DEPARTMENT: information technology


# EXPERIMENT NO 05 INTERFACING ANALOG OUTPUT SERVO MOTOR WITH ARDUINO

### AIM
To interface an Analog output (servo motor) and modify the angular displacement of the servo using PWM signal .
COMPONENTS REQUIRED:
1.	Servo motor of choice (9v is preferred )
2.	1 KΩ resistor 
3.	Arduino Uno 
4.	USB Interfacing cable 
5.	Connecting wires 
6.	Servo rated power supply (dc source )


### THEORY
Servo motors and are constructed out of basic DC motors, by adding:
•	 gear reduction
•	 a position sensor for the motor shaft
•	 an electronic circuit that controls the motor's operation
Typically, a potentiometer (variable resistor) measures the position of the output shaft at all times so the controller can accurately place and maintain its setting.
Servo motors are used for angular positioning, such as in radio control airplanes.  They typically have a movement range of 180 deg but can go up to 210 deg.The output shaft of a servo does not rotate freely, but rather is made to seek a particular angular position under electronic control. 


![image](https://user-images.githubusercontent.com/36288975/163544439-1f477927-fcd4-42f0-9ce4-c863fdbf1210.png)

![WhatsApp Image 2024-03-21 at 10 13 57_581c77ed](https://github.com/suganjoker/EXPERIMENT-NO--05-INTERFACING-ANALOG-OUTPUT-SERVO-MOTOR-WITH-ARDUINO-/assets/105915942/c3845b61-fd67-40a1-b8b2-41b3b08bb371)


#### Figure-01 SERVO MOTOR SPLIT VIEW 
Control 
An external controller (such as the Arduino) tells the servo where to go with a signal know as pulse proportional modulation (PPM) or pulse code modulation (which is often confused with pulse width modulation, PWM). PWM uses 1 to 2ms out of a 20ms time period to encode its information.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/163544482-3027136f-7135-4f3d-a23f-8dc2fe04194d.png)

### Figure-02 SERVO MOTOR PINS

 ![image](https://user-images.githubusercontent.com/36288975/163544513-ca497421-e6ba-4f91-871f-5cfba77f22a8.png)


### Figure-03 SERVO MOTOR OVERVIEW 

 


 ![WhatsApp Image 2024-03-21 at 10 14 08_e312185c](https://github.com/suganjoker/EXPERIMENT-NO--05-INTERFACING-ANALOG-OUTPUT-SERVO-MOTOR-WITH-ARDUINO-/assets/105915942/cf6d9046-afcf-4a57-b908-741eec5a3e7a)






CIRCUIT DIAGRAM
 
 ![WhatsApp Image 2024-03-21 at 10 13 57_581c77ed](https://github.com/suganjoker/EXPERIMENT-NO--05-INTERFACING-ANALOG-OUTPUT-SERVO-MOTOR-WITH-ARDUINO-/assets/105915942/5beddaae-ca48-4fab-95aa-f5792ff48f59)

 ![image](https://user-images.githubusercontent.com/36288975/163544618-6eb8a7b5-7f1a-428a-8d9f-fd899b145efb.png)

### FIGURE 04 CIRCUIT DIAGRAM

### PROCEDURE:
1.	Connect the circuit as per the circuit diagram 
2.	Connect the board to your computer via the USB cable.
3.	If needed, install the drivers.
4.	Launch the Arduino IDE.
5.	Select your board (If you the board is arduino uno, select accordingly).
6.	Select your serial port, accordingly ( E.g. COM5 )
7.	Open the file of the program  and verify the error , clear if any errors that are existing 
8.	Upload the program and check for the physical working. 
9.	Ensure safety before powering up the device.


### PROGRAM :
 
#include<Servo.h>

Servo s1;

int pos=0;

void setup()
{
  s1.attach(9);
  Serial.begin(9600);
  
}

void loop()
{
  for (pos=0;pos<=180;pos+=1)
  {
    s1.write(pos);
    delay(15);
    //Serial.print("Angle=");
    Serial.println(pos);
    
  }
  for (pos=180;pos>=1;pos-=1)
  {
    s1.write(pos);
    delay(15);
    //Serial.print("Angle=");
    
    
  }
}








### RESULTS: 
Arduino uno interfacing with servo motor is learned and angular position is controlled using PWM signal.
