# Electrical Tasks week 2
**Task 3: Brushless Motor**  
(https://www.tinkercad.com/things/kS2jfWCs63d)

**1. Make an account in TinkerCAD for Arduino simulations: https://www.tinkercad.com/**

  1) Click Sign Up on the Tinkercad homepage.
  2) Choose your country from the drop-down list.
  3) Enter your birthday. 
  4) Click the Next button.
  5) Add your email address and a password, accept the Tinkercad terms of service, and click Create Account.
  
  
**2. Building the Brushless Motor circuit:**
Based on the complete circuit we know that it consists of a diode, transistor npn and resistor:

![image](https://user-images.githubusercontent.com/108147030/180010805-28d15157-e48a-49e2-a031-1925beb46a0c.png)

  1) Click on create new Circuit.
  2) From the search tool, get: Breadboard (small), Arduino uno r3, DC motor (Brushless motor), 330 ohm resistor, Diode, and transistor npn.
  3) Connect a wire from the GND (ground) and 5v from the arduino to the breadboard. 
  4) Connect a wire from 5v from the breadbord to the diode and connect it to terminal 2 in the dc motor.
  5) Connect a wire from the collector in the npn to the diode and terminal 1 of dc motor.
  6) connect the resistor from the base of the npn together to the breadboard and with pin 11 in the arduino.
  7) Connect the emitter to the ground.
  6) You can use the following code to run the simulation.

```ruby
void setup()
{
  pinMode(11, OUTPUT);
}

void loop()
{
  analogWrite(11,128);
}
  ```
  
![image](https://user-images.githubusercontent.com/108147030/180015531-4026b490-5d56-4138-82cb-196ce402c1cf.png)

7) Click on start Simulation.



