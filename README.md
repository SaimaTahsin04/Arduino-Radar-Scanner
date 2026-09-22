# Arduino Radar Scanner

## Project Overview

This project is an Arduino-based Radar Scanner that uses an HC-SR04 ultrasonic sensor and an SG90 servo motor to detect objects, measure their distance, and determine their angular position.

The ultrasonic sensor scans the surrounding area while the servo motor rotates the sensor through a 180-degree range. The measured angle and distance data are sent to a computer through serial communication and visualized using Processing.

## Objectives

* To design and implement a functional radar scanner system using basic electronic components.
* To measure object distances using an HC-SR04 ultrasonic sensor.
* To determine the angular position of detected objects using an SG90 servo motor.
* To display real-time angle and distance information.
* To demonstrate the practical application of embedded systems and sensor-based object detection.

## Components Used

| Component         | Model/Type   | Quantity |
| ----------------- | ------------ | -------: |
| Microcontroller   | Arduino UNO  |        1 |
| Ultrasonic Sensor | HC-SR04      |        1 |
| Servo Motor       | SG90         |        1 |
| Jumper Wires      | M-M, M-F     |      ~10 |
| USB Cable         | 5V USB Cable |        1 |

## Pin Configuration

### HC-SR04 Ultrasonic Sensor

| Sensor Pin | Arduino UNO | Purpose        |
| ---------- | ----------- | -------------- |
| VCC        | 5V          | Power Supply   |
| TRIG       | D10         | Trigger Signal |
| ECHO       | D11         | Echo Signal    |
| GND        | GND         | Ground         |

### SG90 Servo Motor

| Servo Wire | Arduino UNO | Purpose      |
| ---------- | ----------- | ------------ |
| Yellow     | D12         | PWM Signal   |
| Red        | 5V          | Power Supply |
| Black      | GND         | Ground       |

## Working Principle

The HC-SR04 ultrasonic sensor measures distance by sending an ultrasonic pulse and receiving its reflected echo.

The Arduino triggers the sensor using the TRIG pin. The sensor sends an ultrasonic signal, and when the signal reflects from an object, the ECHO pin receives the return signal.

The distance is calculated using:

**Distance (cm) = (Time × 0.034) / 2**

The SG90 servo motor rotates the ultrasonic sensor from approximately 15° to 165° and then back again. At each angle, the sensor measures the distance of an object.

The Arduino sends the angle and distance through the serial port in the following format:

`angle,distance.`

For example:

`45,32.`

Here, 45 represents the angle and 32 represents the measured distance in centimeters.

## Software Used

* Arduino IDE
* Processing IDE

## Arduino Program

The Arduino program controls the servo motor and ultrasonic sensor. It measures the distance and sends the angle and distance data through serial communication at 9600 baud rate.

## Processing Visualization

The Processing program receives the serial data from the Arduino and converts the angle and distance values into a radar-style graphical display.

The Processing program uses the serial port to receive data in the format:

`angle,distance.`

It then displays the scanning line, angle, distance, and detected objects on the screen.

## Circuit Diagram

Add the circuit diagram image here.

## Project Output

The system provides real-time radar visualization on the computer screen. Detected objects are displayed according to their angle and distance from the ultrasonic sensor.

Add the project output screenshot here.

## Advantages

* Low-cost project
* Simple hardware setup
* Real-time object detection
* Easy-to-understand radar visualization
* Useful for learning Arduino, sensors, servo motors, and serial communication

## Applications

* Robotics navigation
* Proximity detection
* Perimeter monitoring
* Industrial automation
* Educational projects

## Future Improvements

* Improve the radar visualization.
* Add wireless communication using ESP8266 or ESP32.
* Add additional sensors for better object detection.
* Improve object tracking and classification.

## Author

**Saima Tahsin**


## Reference

RoboZenBD — Arduino Beginner to Advanced Learning Kit
Radar Scanner – Scan Area and Show Distance on Screen

