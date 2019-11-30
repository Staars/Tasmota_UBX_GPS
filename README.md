# Tasmota_UBX_GPS
Backup of all files for my Tasmota-GPS-Project. This is a playground project, but it would be possible to finish this driver to merge it.
  
  
  
## GPS-driver for the Ublox-series 6-8  
Driver is tested on a NEO-6m and a Beitian-220. Series 7 should work too. This adds only about 6kb to the program size, because the efficient UBX-protocol is used. These modules are quite cheap, starting at about 3.50€ for the NEO-6m.

## Features:  
- get position and time data
- sets system time automatically and Settings.latitude and Settings.longitude via command  
- can log postion data with timestamp to flash with a small memory footprint of only 12 Bytes per record
- constructs a GPX-file for download of this data  
- Web-UI 
- simplified NTP-server
- command interface
  
   
   
## Usage:  
The serial pins are hardcoded (default 4,5 -> D2,D1), no further installation steps needed. To get more debug information compile it with option "DEBUG_TASMOTA_SENSOR". 
  
  
Commands:  
  
+ sensor92 0  
  write to all available sectors, then restart and overwrite the older ones
  
+ sensor92 1  
  write to all available sectors, then restart and overwrite the older ones
  
+ sensor92 2  
  filter out horizontal drift noise
  
+ sensor92 3  
  turn off noise filter
  
+ sensor92 4  
  start recording, new data will be appended
  
+ sensor92 5  
  start new recording, old data will lost
  
+ sensor92 6  
  stop recording, download link will be visible in Web-UI
  
+ sensor92 7  
  send mqtt on new postion + TELE -> consider to set TELE to a very high value
  
+ sensor92 8  
  only TELE message
  
+ sensor92 9  
  start NTP-server
  
+ sensor92 10  
  deactivate NTP-server
  
+ sensor92 11  
  force update of Tasmota-system-UTC with every new GPS-time-message
  
+ sensor92 12  
  do not update of Tasmota-system-UTC with every new GPS-time-message
  
+ sensor92 13  
  set latitude and longitude in settings  
  
  
  
## Rules examples for SSD1306 32x128


