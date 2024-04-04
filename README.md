#  RC Car Project

This project is an Arduino-based remote-controlled (RC) car that can be controlled using a two-channel remote controller. The car is capable of moving forward, backward, turning left, and turning right based on the signals received from the remote controller.

## Hardware Components

- Arduino board (Arduino Uno)
- Two motor drivers (L298N)
- Two DC motors
- Two-channel remote controller and receiver
- Battery pack for powering the Arduino and motors
- Chassis, wheels, and other mechanical components for the car

## Software Requirements

- Arduino IDE

## Pin Connections

- Receiver signal pins:
 - Channel 1 (`ch1_pin`): Digital pin 3 (PWM)
 - Channel 2 (`ch2_pin`): Digital pin 5 (PWM)

- Right motor driver pins:
 - Enable pin (`R_EN_right`): Digital pin 2
 - Enable pin (`L_EN_right`): Digital pin 4
 - PWM pin (`R_PWM_right`): Digital pin 6 (PWM)
 - PWM pin (`L_PWM_right`): Digital pin 9 (PWM)

- Left motor driver pins:
 - Enable pin (`R_EN_left`): Digital pin 7
 - Enable pin (`L_EN_left`): Digital pin 8
 - PWM pin (`R_PWM_left`): Digital pin 10 (PWM)
 - PWM pin (`L_PWM_left`): Digital pin 11 (PWM)

## Receiver Signal Thresholds

The code uses threshold values to determine the forward and backward movement of the car based on the receiver signals. These values may need to be updated based on your specific remote controller.

- Forward movement:
 - Start value (`Ch1Ch2_start_Fwd`): 1530
 - End value (`Ch1Ch2_End_Fwd`): 1980

- Backward movement:
 - Start value (`Ch1Ch2_start_Bac`): 1460
 - End value (`Ch1Ch2_End_Bac`): 960

## How to Use

1. Connect the hardware components according to the pin connections mentioned above.
2. Upload the Arduino sketch to the Arduino board using the Arduino IDE.
3. Power on the remote controller and the RC car.
4. Use the remote controller to control the car's movement:
  - Move both sticks forward to move the car forward.
  - Move both sticks backward to move the car backward.
  - Move the right stick forward and the left stick backward to turn the car right.
  - Move the left stick forward and the right stick backward to turn the car left.
  - Release both sticks to stop the car.


