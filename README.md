# TEMP-Air: Welcome soundscape

Here you will find the instructions to replicate the system used at TEMP-Air 2017 at Te Uru Art Gallery in Titirangi (Auckland, New Zealand)

## TEMP
For more information about the TEMP project, check the website:
http://www.tempauckland.org.nz/

## TEMP-Air
As part of the TEMP project, the Air component consists of a mixed-reality experience at Te Uru Art Gallery (http://www.teuru.org.nz/) around making the invisible in our air visible.

More details can be found on the project's website: https://www.otukapua.nz/

# System
The system consists of a motion sensor, speakers and a Raspberry Pi (https://www.raspberrypi.org/). When someone starts to make their way to the main exhibition area, the motion sensor sends a signal to the Raspberry Pi which then plays the welcome sound. Once the sound has finished, the Raspberry Pi waits until the next activation of the motion sensor to start playing the sound again. The sound is not interrumpted if more "motion events" are identified.

## Requirements
1. PIR sensor (https://nicegear.co.nz/sensors/dfrobot-pir-motion-sensor/)
2. Raspberry Pi (https://nicegear.co.nz/raspberry-pi/raspberry-pi-3/). Any version will work but the sound is better with a RPi2 or above.
3. Linux image for the hardware you have. The guide here was tested with Raspbian Jessie but you can try other flavours. (https://www.raspberrypi.org/downloads/)
4. Speakers (https://www.pbtech.co.nz/product/SPKLOG2453263/Logitech-Z200-Speaker---Black)

## Setup
1. Prepare the SDcard for the Raspberry Pi. The Fedora Arm Installer is a great tool! (https://fedoraproject.org/wiki/Architectures/ARM/F25/Installation#Fedora_Arm_Installer) or you can go "manual" and follow the steps here: https://www.raspberrypi.org/documentation/installation/installing-images/README.md
2. Install this repository
3. Setup a cron job for the main script so that it runs at boot. See `cron-job-sample.txt`
3. Wire the trigger pin of the motion sensor to one of the GPIO pins
4. Plug the speakers and test the script and the sound volume.
4. Deploy!

# License
This repository is license under the GPLv3 which can be summarised as:

>You may copy, distribute and modify the software as long as you track changes/dates in source files. Any modifications to or software including (via compiler) GPL-licensed code must also be made available under the GPL along with build & install instructions.

The full text of the license is in `LICENSE`
