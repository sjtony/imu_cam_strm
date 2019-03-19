# imu_cam_strm
Software to interface the Beaglebone Black (BBB) with the MPU-6050 3 axis accelerometer and gyro IMU. Data is collected from the IMU over I2C bus in raw quaternion format, converted to Euler angles and then sent over the network to a remote machine. Also, software is provided to stream .jpg images from the USB webcam to a remote computer. Software is based on InvenSense Motion Driver Firmware examples found on I2CDevLib and ARMmbed

## modification for beaglebone blue
* BB-blue come with built-in MPU9250
* In order to adapt to new board, minor changes are done in imu_app.c as following 
  - I2c port changed to 2
  - a few lines of ASSERT commented due to 2 port conflicting 
  - interrupt GPIO changed to 117
  - of course, IP address have to be adjust 
* The OS of my PC is Linux, to install Vpython for Linux, please follow below link
  - https://vpython.org/contents/download_linux.html  
  
