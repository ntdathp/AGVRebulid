# AGV QR Code

### This repo consists of firmware, software and hardward of my thesis about AGV QR code:
The thesis designs a solution using a QR code matrix set up to navigate and locate an AGV. The AGV will follow a trajectory defined by the user, with specified start and end points

### Hardware Design:
Develop a robot model with a downward-facing camera to observe QR codes on the ground. A Raspberry Pi is used to process images from the camera, communicate with the GUI, and control the robot's movement via UART communication with a custom-designed STM32 microcontroller circuit. This microcontroller circuit will control the PID velocity of two DC motors using a custom-designed H-bridge circuit.
Robot:

![Robot](image/Robot.png)

Self-Designed Microcontroller board:

![Self-Designed Microcontroller board](image/Board.png)

### PID Controller and Trapizoidal Velocity Profile:
Using trapezoidal velocity information and a PID velocity controller to move the vehicle within the QR code matrix.
rapizoidal Velocity Profile and PID velocity control result:

![Trapizoidal Velocity Profile](image/TVF.png)

#### Robot Moving:

![Robot_Moving](video/Robot_Moving.gif)
### GUI:
The GUI interface is programmed using Qt, communicating with the robot through the MQTT protocol. It sends the movement trajectory between two endpoints set by the user, notifies when the vehicle reaches the QR codes in the matrix, and adjusts the vehicle's speed.


![GUI](image/GUI.png)

#### Go to goal process: 
Frames from Camera             |  Image processing with Optical Flow algorithm
:-------------------------:|:-------------------------:
![calib_video.gif](video%2Fcalib_video.gif)  | ![image_processing.gif](video%2Fimage_processing.gif)

### Test environment :
The QR code matrix is arranged on the floor, and a camera positioned above looks down to observe during the movement process to evaluate the results

QR code matrix:

![Test environment](image/Test_environment.png)


### Result Video:
[![Result](https://img.youtube.com/vi/Og9lnYisi18/0.jpg)](https://www.youtube.com/watch?v=Og9lnYisi18&list=PLiomqXJMBwLjaPSaCo-AB2hMpSG3AKzQ9)

Result:

![Result](image/Result.png)

