These are examples for the Raspberry Pi Pico development board, have VS Code support and serial output through USB. You will have to edit the include paths so they match the ones on your computer, but VS Code should warn you about it if you don't.
Also, you must have the libraries files (I2Cdev.h, I2Cdev.cpp, MPU6050.h, MPU6050.cpp, MPU6050\_6Axis\_MotionApps\_V6\_12.h, helper\_3dmath.h) inside the example folder (whichever you want to build), unless you modify the CMakeLists.txt and specify the path.

#### Instructions for building examples
1. ```cd``` to the folder of the example you want to build.
2. ```mkdir build && cd build```
3. ```cmake ..```
4. ```make```
5. Copy the uf2 file to your Pico board, using ```cp``` or the file explorer you have.
6. ```sudo minicom -D /dev/ttyACM0``` to watch the serial output. Use ```sudo```, otherwise minicom will fail to open the device and show no warnings. On Windows you can use PuTTY, choosing the COM port that was assigned (check the Device Manager) and a baudrate of 115200.