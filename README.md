# Argon ONE (V2) Pi 4 Script for RetroPie

I've been running a retroPie install on my rPi 4 using the Argon One V2 case with ssd add on.  
I learned that Emulation Station needs to shut down gracefully in order to save some changes propperly.
I also learned about the wonderful [ES Generic shut down script](https://github.com/crcerror/ES-generic-shutdown).
So I updated the Argon One script to use the ES Shutdown script for both the shutdown and reboot commands.

**I am in no way affiliated with [Argon 40](https://www.argon40.com "https://www.argon40.com"), I only use their cases as an end user.**

You can find them here:
* Argon 40 Website: [https://www.argon40.com](https://www.argon40.com "https://www.argon40.com")
* Argon 40 Github: [https://github.com/Argon40Tech](https://github.com/Argon40Tech "https://github.com/Argon40Tech")

## How to install

### Prerequisites

* RetroPie running on an a Raspberry Pi 4
* [Argon ONE (V2) Case for Raspberry Pi 4](https://www.argon40.com/collections/raspberry-pi-cases "Argon ONE (V2) Case for Raspberry Pi 4")

### Installing

1. Open "Terminal" in Raspbian.
2. Type the three commands below, pressing enter after each, to install

   ```
   mkdir /home/pi/myRetroPieScripts && cd /home/pi/myRetroPieScripts
   ```
   ```
   wget https://raw.githubusercontent.com/crcerror/ES-generic-shutdown/master/multi_switch.sh && chmod +x multi_switch.sh
   ```
   ```
   curl https://raw.githubusercontent.com/pponce/ArgonOne-retroPie-Script/master/source/argon1.sh | bash
   ```

3. Reboot.

## Usage Instructions are the same as the original scripts from Argon40

### Argon ONE (V2) Pi 4 Power Button Functions

ARGON ONE (V2) PI 4 STATE | ACTION | FUNCTION
:------------------: | :----: | :------:
OFF | Short Press | Turn ON
ON | Long Press (>= 3 s) | Soft Shutdown and Power Cut
ON | Short Press (< 3 s) | Nothing
ON | Double Tap | Reboot
ON | Long Press (>= 5 s) | Forced Shutdown

### Argon ONE (V2) Pi 4 Fan Speed
Upon installation of the Argon ONE (V2) Pi 4 script by default, the settings of the Argon ONE (V2) Pi 4 cooling system are as follows:

CPU TEMP | FAN POWER
:------: | :-------:
55 C | 10%
60 C | 55%
65 C | 100%

However, you may change or configure the FAN to your desired settings by clicking the Argon ONE (V2) Pi 4 Config icon on your Desktop.

Or via "Terminal" by typing and following the specified format:

```
argonone-config
```

## Uninstalling Argon ONE (V2) Pi 4 Script

To uninstall the Argon ONE (V2) Pi 4 script you may do so by clicking the Argon One (V2) Pi 4 Uninstall icon on your Desktop.

You may also remove the script via "Terminal" by typing.
```
argonone-uninstall
```

Always reboot after changing any configuration or uninstallation for the revised settings to take effect.

## Acknowledgments

Thanks to [Argon 40](https://www.argon40.com "https://www.argon40.com") for building these great Raspberry Pi Cases.

crcerror for creating this great shutdown script for retroPie users [ES-generic-shutdown](https://github.com/crcerror/ES-generic-shutdown).

---
