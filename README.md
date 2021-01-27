# IoT-based-Animal-Helath-monitoring
Livestock health management is essential for developing countries in general and especially as its food security highly depends on livestock production. 
According to UNDP in Ethiopia, Ethiopia has the largest livestock population in Africa. However, the death of livestock is happening in enormous numbers 
even though it decreases over time. To minimize this high death rate, a more advanced livestock health monitoring system is required. Automated IoT-based
monitoring systems have been proposed by many researchers. A wearable hardware device that is placed at the neck or ear of the animal and tracks the health
status by reading (sensing) the animal’s body temperature, ruminating rate, geo-location, and movement data. It will then send this information to a cloud 
server through a WiFi module, where the data will be processed using machine learning, which will then observe and classify the activities of the animal. 
The end-user will be able to observe and analyze the data for further evaluation. 

This method will contribute to maintaining sustainable food production and supply in rural and urban areas in the country, as it will help to monitor the 
welfare of the livestock. Since the time of civilization and the domestication of animals, livestock has provided crucial contributions to the wellbeing 
of human beings in social and economic terms. 


#Two steps of the project

1. Data collection is the process of gathering relevant information on targeted variables in an established system, which then enables one to answer relevant 
questions and evaluate outcomes. The ‘data’ we are referring to in this particular project is the health parameters of the livestock, such as the body 
temperature, and neck movement. These analog data need to be collected and converted to digital data in order to be processed in the proposed system. 
We will be able to collect these data through a sensor called MPU 6050. This sensor contains three sensors which are: a gyroscope, used to measure angular 
acceleration; an accelerometer, used to measure linear acceleration; and a temperature sensor. The gyroscope and accelerometer will collect data of the 
livestock such as whether the animal is sleeping or standing, whereas the temperature sensor will collect the temperature data of the animal. 
The MPU 6050 sensor contains predefined registers (temporary storage area) that contain addresses, so we will have to initialize the sensor 
by setting these registers.


2. Data Transmission
The collected data is then transferred to Pic18F45k22 microcontroller through an I2C connection using jumper wires, which IS also connected to 
a WiFi adapter called ESP8266 through the USART connection. Then finally the data is transmitted to the server using the WiFi module. 

A microcontroller is a small computer on a single integrated circuit chip that contains one or more CPUs along with memory and programmable input/output peripherals.
The microcontroller that we chose in this particular project is the Pic18F45k22 microcontroller, which is easy-to-program. The microcontroller will receive the sensor 
data through an I2C connection, which is a serial communication protocol where data is transferred bit by bit along a single wire (the SDA data line). The microcontroller 
will then transmit the sensor data to the server using a WiFi module. We have used USART (Universal Synchronous and Asynchronous Receiver-Transmitter) as a way to 
connect the microcontroller to the WiFi module. USART is a microcontroller peripheral that converts incoming and outgoing bytes of data into a serial bitstream. 
We have chosen the ESP8266 WiFi module as it is low in cost, and easily accessible. The ESP8266 will then send the data to the server using the AT command on the 
microcontroller.
