# State change detections using the accelerometers with inbuilt filters at IOT platform
Manoranjan Kumar (makuaa@lnu.se),
PhD student

In this IOT (Internet of things) course I decided to study its concept hence performing a small project in the frame of its end-to-end implementations. I choose to use accelerometers hence programming in microcontroller to detect the acceleration changes using filters to avoid noise detections or smoothing of dataset. Further I also like to visualize those changes to the IOT platforms. I am hoping this should not take more than 8 weeks of time for such investigations and implementations.

Contents
1.	Objective	
2.	Material	
3.	Environmental setup	
4.	Putting everything together	
5.	Platforms and infrastructure	
6.	The code	
7.	The physical network layer	
8.	The Visualization and user interface	
9.	Finalizing the design	
10.	References	

# 1.	Objective

Accelerometer is an important sensor in identifying the state of machines or equipment’s which includes changes in motions. This is also used widely into different domain such as automotive, house safety and health fitness etc. This can capture and identify the states of any equipment’s it is attached depending upon the definitions of state detections. In this project I tried to investigate how I can capture the states changes of the accelerometers depending upon the changes it is experiencing.  The detection of states also depends on what kind of filters are applied into the accelerometers original data. Filters are necessary to avoid the noises, smoothing or detecting a particular state of the systems. Hence by doing this project it will enables to deploy filter algorithms and detecting the states due to changes of accelerations. Once the states are detected further insights can be known of the attached equipment’s related to different controls if any.
# 2.	Material
The following type of materials are brought to perform this project from different places as shown below in Table 1. 

Table 1. List of materials in doing this project
|  Material 	            |  Purchased Place 	  |  Cost |   Unit|  Specifications 	                                                |
|---	|---	|---	|---	|---	|
|Expansion Board 3.0	    | https://pycom.io/	  |  18	  | Pound | USB and LiPo battery powered	                                    |
|  LoPy4 - With Headers  	| https://pycom.io/ 	|  39 	|  Pound|  With network protocol such as Bluetooth, Wi-Fi, LoRa and Sigfox 	|
|  Custome Tax 	          | https://pycom.io/   |  428 	|  SEK 	|   	                                                              |
|  shipping cost from UK 	| https://pycom.io/   |   25	|  Pound|   	                                                              |
|  ADXL345 from adafruit 	|  electrokit.se 	    |  166 	|  SEK 	| I2C and SPI interfaces, 3.3v, sensitivity of +/- 2G to +/- 16G  	|
|  PCboard	              |  electrokit.se 	    |  0 	  |  SEK 	| 	                                                                |
|  USB cable 	            |  electrokit.se 	    |  0 	  |  SEK 	| micro-B of length 1.8m  	                                        |
|  Jumpers 	              |  amazon.se 	        |  80 	|  SEK 	|  	                                                                |
|  LoRa anteena 	        |  Kjell & company 	  |  100 	|  SEK 	| 824-960 Mhz (GSM, LoRa etc), 1710-2200 MHz GSM. 	                |

Further the design of the project is shown below in Figure 1 with the details of materials.
![figure1](https://raw.githubusercontent.com/manoranjan9991/4DV119-IOT/main/NewFolder/fig1.png) 
      Figure 1. The materials used in designing this project.
# 3.	Environmental setup

To setup the lopy4.0 the software for e.g. node.js and Atom [1] are installed into the windows environments. Once these programs were installed the lopy4.0 is detected by the atom who gave the specification of the lopy4.0 as shown below Figure 2 .

![figure2](https://raw.githubusercontent.com/manoranjan9991/4DV119-IOT/main/NewFolder/fig2.png) 

     Figure 2. The Lopy4.0 configurations into Atom.
It was not needed to flash the latest firmware but still steps are taken to reflash the latest firmware. The flash has been performed by installing ParticleCLISetup.exe files using the instruction from [2]. Once the lopy4.0 is configured to the system further it is registered to the pybytes [3] for setting up the wi-Fi connections and LoRa for data transfer. This is done under my device sections to the pybytes GUI as shown below in Figure 3.

![figure3](https://raw.githubusercontent.com/manoranjan9991/4DV119-IOT/main/NewFolder/fig3.png)
Figure 3. The registration of pycom and setting up the GUI.
