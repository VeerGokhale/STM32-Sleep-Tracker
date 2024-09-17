# STM32-Sleep-Tracker
This project is an STM32 based sleep tracking device. The components required to utilize the code are as follows:

- STM32F103C8T6 development board 
- MAX30102 heartrate sensor and pulse oximeter, connected via the I2C1 line
- MPU6050 gyroscope and accelerometer, connected via the I2C2 line
- MicroSD card module and MicroSD card, connected via the SPI1 line
- HC-05 Bluetooth module, connected via the USART2 line

I wrote the device driver for the MPU6050 myself. For the MAX30102, the driver comes from Analog Devices, and for the MicroSD card module, the setup code comes from this video https://www.youtube.com/watch?v=spVIZO-jbxE. 

The project consists of three main components. The first is the CubeIDE code required to interface with the sensors, store the readings on the MicroSD card, and send data via bluetooth. The second is the Python code for receiving the transmitted data on an external computer. The third is the KiCad Board design for a custom STM32F103C8T6 board that compactly houses all the sensors.

Currently, I am working on testing the board and writing software to translate the raw data into valuable sleep analytics
