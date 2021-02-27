# OpenDrone project
---

The goal is to build a complete commercial level software+hardware stack for a quadcopter from scratch with keeping minimalism in mind. The quadcopter should be very easy to fly and the user should not have any previous flying experience. The drone should be very stable and should have altitude hold.

The components used for this projects should be off-the-shelves and easy to get. The moving components to kept minimal, and easy for developer/users to look around code and understand. To begin with, Im going to just build the flight controller and use ready made components and frame.


## Hardware stack
- Pico RP2040
- MPU6050
- BMP 280
- the generic red and white F450 frame
- FlySky Controllers (Later will build a complete one from scratch)
- Simon ESCs
## Software stack
- Golang program serving the front-end over web server. Things like calibration, tuning, re-programming, GPS position, Information GUI, etc can be displayed in the browser.
- Pico C/C++ SDK for the hardware codes. Maybe someone can port a simpler version for Arduino core. Or I will simultaneously write both for arduino core and pico SDK.
- A PWA App with WebBluetooth(Wireless) or WebSerial(Wired with an external transmitter) can be built for more interesting controller.

## Things to do
Get the following things working
- RP2040 + MPU6050 (i2c)
- RP2040 + BMP280 (i2c)
- RP2040 + RF receiver (Analog Read)
- RP2040 + ESC (PWM)
- Sensor fusion (Gyro + accelerometer), complimentary and kalman filter inside the RP2040
- Build a testing jig for two single axis testing
- Write a PID controller for single axis (Just 2 motors, pivoting in the middle)
- Write a PID controller for all 4 motors
- Figure out altitude hold function with the Barometer module
- Build a PC SMPS tethering setup for the drone
- Read about batteries and figure out the charging and usage
- Build the a perfboard PCB prototype
- Design a PCB with RP2040+MPU6050+BMP280+few componets for final flight controller
