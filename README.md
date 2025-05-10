# OpenGK.org SIMK4x

Repository for tuning the Hyundai GK platform. Specifically the Siemens VDO 5WY ECM.

## Structure

### ADX 

TunerPro logging definitions. 

These files contain instructions on how TunerPro is supposed to connect to your ECU, and what data should it log.

Inside ADX files, you'll also find descriptions for logged variables. TunerPro logs raw data, which means
that, for example, if you record a log with `ca66xxx_version_1.0.0.ADX`, you'll still be able to later 
open it with `ca66xxx_version_2.3.4.ADX` - or the other way around.

### DBC

CAN bus signal definitions. They can be opened with software such as SavvyCAN

### XDF 

XDF files describe the contents of .bin files that you read/flash using [GKFlasher](https://github.com/Dante383/GKFlasher) or other software.


### EEPROM

Collection of firmwares (`.bin`s) for each motor and ECU version

``
XDF stays for definition of parameters inside firmware, you need to download first TunerPro, then open eeprom (*.bin) and add XDF file
ADX stays for availability of data-logging via TunerPro, you need to add it to program
EEPROM is collection of firmwares for each motor and ECU version
``