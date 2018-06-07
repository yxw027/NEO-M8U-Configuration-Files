# :space_invader: NEO-M8U-Configuration :space_invader:
GNSS Configuration for the NEO-M8U Configuration via .yaml file in ROS using Kumar Robotics Ublox ROS drivers and in Windows via Ublox's U-Center. By completing this "tutorial" you should be able to perform the following:

- [ ] Configure the NEO-M8U Module to track GPS, GLONASS, and Galileo Satellites in Windows
- [ ] Poll raw NMEA 0183 data in Windows
- [ ] (Optional) Map the NMEA data to Google Earth from U-Center *KML file from "Database Export" command in U-Center*
- [ ] Configure the NEO-M8U Module to track GPS, GLONASS, and Galileo Satellites in ROS/Linux
- [ ] Poll & bag "NavSatFix" data specified by: http://docs.ros.org/api/sensor_msgs/html/msg/NavSatFix.html
- [ ] (Optional) Map the NavSatFix data to Bing Maps or others depending on API's and time availabe.

## For Configuration in Windows via U-Center:
### Installing U-Center:
Download the latest version of U-Center from Ublox's website by clicking the following link.

https://www.u-blox.com/en/product/u-center-windows

With U-Center, the NEO-M8U module can be configured three different ways, however we will only explore the SQI flash method for permanent configuration as it is the most useful given our time restraints.

  #### 1. Power & Reset Dependant
  In U-Center, configurations can be applied to the NEO-M8U module such that they retain their values for the time at which the 
  module is powered or until it is either hardware or software reset.
  
  #### 2. Batery Backed RAM (BBR)
  In U-Center, configurations can be applied to the NEO-M8U module such that they retain values independent of the status of 
  external power or any resets. The configuration parameters are retained as long as the battery supply on board is not 
  interrupted.
  
  #### 3. Serial Quad I/O (SQI) Flash
  In U-center, configurations can be applied to the NEO-M8U module such that the parameter values will always retain their 
  given values no matter the status of any power supplies or resets.

### U-Center SQI Configuration
1. Download the Configuration_Ublox_Neo_M8U.txt configuration file from my github.
2. Connect the mPCIe NEO-M8U card to the mPCIe to USB adapter and plug into your PC then open U-Center.
3. Click on the Magic Wand at the top toolbar to enable autoset for the Baud Rate. Wait for the "Connection Status" to turn green.
http://andrea-toscano.com/wp-content/uploads/2015/05/U-Center-magic-wand.png
4. On the toolbar, go to Tools -> GNSS Configuration and select the Configuration_Ublox_Neo_M8U.txt configuration file downloaded from my github. Make sure the "Store Configuration in BBR/Flash" box is checked!
5. On the toolbar, go to View -> Message View and scroll down to UBX -> CFG.
6. 


## For Configuration in Windows via ROS
