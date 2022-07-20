# Electrical Tasks week 2
**Task 2: Stepper Motor Simulation with arduino**  
(https://www.tinkercad.com/things/81hV2UR563j)

**1. Make an account in TinkerCAD for Arduino simulations: https://www.tinkercad.com/**

  1) Click Sign Up on the Tinkercad homepage.
  2) Choose your country from the drop-down list.
  3) Enter your birthday. 
  4) Click the Next button.
  5) Add your email address and a password, accept the Tinkercad terms of service, and click Create Account.
  
  
**2. Building the Stepper Motor:**

  1) Click on create new Circuit.
  2) From the search tool, get: Breadboard (small), Arduino uno r3, 9v battery, DC Motor with Encoder (stepper motor), H-bridge Motor Driver (IC L293D).
  
  ![image](https://user-images.githubusercontent.com/108147030/179868669-b3100698-8deb-4a4d-8bd7-db676dff3820.png)

  3) Connect a wire from the IC L293D all pins 1, 8, 9, and 16 to 5v source to the breadboard.
  4) Connect a wire from the IC L293D (use only one pin 4, 5, 12, or 13) to GND (ground) to the breadboard.
  5) Connect a wire from the Motor positive (red pin in stepper motor) to +9v battery (positive).
  6) Connect a wire from the Motor negative (black pin in stepper motor) to -9v battery (negative).
  7) Connect a wire from the Motor encoder ground (green pin) to output 3 in pin 11 in IC L293D.
  8) Connect a wire from the Motor channel B (purple pin) to output 4 in pin 14 in IC L293D.
  9) Connect a wire from the Motor channel A (yellow pin) to output 2 in pin 6 in IC L293D.
  10) Connect a wire from the Motor encoder power (orange pin) to output 1 in pin 3 in IC L293D.
  11) Connect a wire from the Arduino pin 11 to input 1 in pin 2 in IC L293D.
  12) Connect a wire from the Arduino pin 10 to input 2 in pin 7 in IC L293D.
  13) Connect a wire from the Arduino pin 9 to input 3 in pin 10 in IC L293D.
  14) Connect a wire from the Arduino pin 8 to input 4 in pin 15 in IC L293D.
  
  ![image](https://user-images.githubusercontent.com/108147030/179868781-a81d2b68-bf3f-4582-82a7-25f45aee57ca.png)

  15) You can use the following arduino code to run the simulation.
  
  #include <Stepper.h>

const int stepsPerRevolution = 120;

Stepper myStepper(stepsPerRevolution, 8, 9, 10, 11);

int stepCount = 0;

void setup()
{

  Serial.begin(9600);
  
  
}

void loop()
{
 
  int sensorReading = analogRead(A0);
  
  int motorSpeed = map(sensorReading, 0, 1023, 0, 250);
  
  if (motorSpeed > 0){
    myStepper.setSpeed(motorSpeed);
    
    myStepper.step(stepsPerRevolution / 100);
    
    Serial.println(sensorReading);
  }
}
  16) Click on start Simulation.
  
