# Tasmota_UBX_GPS
Backup of all files for my Tasmota-GPS-Project. This is a playground project, but it would be possible to finish this driver to merge it.
  
  
  
## GPS-driver for the Ublox-series 6-8  
Driver is tested on a NEO-6m and a Beitian-220. Series 7 should work too. This adds only about 6kb to the program size, because the efficient UBX-protocol is used. These modules are quite cheap, starting at about 3.50€ for the NEO-6m.

## Features:  
- get position and time data
- sets system time automatically and Settings.latitude and Settings.longitude via command  
- can log postion data with timestamp to flash with a small memory footprint of only 12 Bytes per record
- constructs a GPX-file for download of this data  
- 
  
   
   
## Usage:  
The serial pins are hardcoded (default 4,5 -> D2,D1), no further installation steps needed. To get more debug information compile it with option "DEBUG_TASMOTA_SENSOR".
