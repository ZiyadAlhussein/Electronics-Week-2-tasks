# Electrical Tasks week 2
**Task 1: Servo Motor Simulation with arduino**  
(https://www.tinkercad.com/things/b2JdpbFsfw2)

1- Make an account in TinkerCAD for Arduino simulations: https://www.tinkercad.com/
  i) Click Sign Up on the Tinkercad homepage.
  ii) Choose your country from the drop-down list.
  iii) Enter your birthday. 
  iV) Click the Next button.
  V) Add your email address and a password, accept the Tinkercad terms of service, and click Create Account.
  
2- Building the Servo Motor:
  i) Click on create new Circuit.
  ii) From the search tool, get: Breadboard (small), Arduino uno r3, and Micro servo.
  iii) Connect a wire from the GND (ground) of the arduino to the negative sign column in the breadboard, Connect the ground from the servo moter to the negative sign column in the breadboard.
  iv) Connect a wire to the power from the servo motor to 5V in the arduino.
  v) Connect a wire to the signal from the servo motor to pin 9 in the arduino.
  vi) You can either use the following arduino code or a block diagram to run the simulation.
  vii) Click on start Simulation.
  
// C++ code
//
#include <Servo.h>

int position = 0;

int i = 0;

Servo servo_9;

void setup()
{
  servo_9.attach(9, 500, 2500);
}

void loop()
{
  position = 0;
  for (position = 1; position <= 179; position += 1) {
    servo_9.write(position);
    delay(20); // Wait for 20 millisecond(s)
  }
  for (i = 179; i >= 1; i -= 1) {
    servo_9.write(position);
  }
}
  
  ![image](https://user-images.githubusercontent.com/108147030/179791824-f81a187b-b5d3-4e64-a53e-bab70c83a9e1.png)

