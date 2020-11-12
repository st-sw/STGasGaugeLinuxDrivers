# ST Gas Gauge Linux Drivers (old version)
STC311x Fuel Gauge / Gas Gauge / Battery monitoring

Driver for Linux Kernel 2.6 (with Platform Data) <br />
__Warning__: Not compatible with Device Tree (DT) <br />

* __New version here:__   <br />
https://github.com/st-sw/STC3117_LinuxDriver  <br />

This repository contains the Linux drivers for STC3117 battery monitoring IC from STMicroelectronics.


---------------------------------
Linux driver standard behavior:
---------------------------------

- Probe function is called by Android kernel start-up
- Probe function uses the predefined battery parameters declared in platform data file
- All software internal compensation and features are configurable from the platform data structure
- Work function is called automatically by the internal driver scheduler
	* The scheduler delay can be updated accordingly to the application needs
	* Typical delay value 5 to 30 seconds
- The battery information are reported in the standard power_supply structure

