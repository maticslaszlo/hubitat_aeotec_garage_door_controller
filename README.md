# Aeotec Garage Door Controller device driver for Hubitat

Aeotec garage door controller device driver and instructions

First, you need to add this code to your apps code. After you pair your controller by Z-Wave inclusion, set type to "Aeon Garage door controller" from user section

Please, calibrate device manually:

You can also calibrate the Garage Door Controller manually using these steps, you do not have to use configuration settings to put the garage door, and may be more preferable and easier to do so manually.

Ensure that the garage door is closed, and the tilt sensor is in an CLOSED position, while the GDC shows a CLOSED status on your gateway interface.
Using the main button located at the very front of the unit (Switch Button), press and hold its button down for 10 seconds, then let go. If successful, the network LED on the back will be blinking rapidly to indicate that it is in calibration mode.
Open the garage door using the Switch Button of the GDC, or through Z-Wave commands. Let it open all the way.
Now close the garage door using the Switch Button on the GDC, or through Z-Wave commands. Let it close all the way.
Calibration is now complete.

After complete, it's recommended to send "Configure" command from device page.

Next step is setup polling:

Import Hubi-poll from https://raw.githubusercontent.com/HubitatCommunity/Hubi-Poll/master/Hubi-Poll.groovy
Add new User App Hubi-Poll
Setup Scheduled Polling Group 1
-> Select Devices to be polled: your garage door controller
-> Set polling interval (recommend to 1 second)

Assign name, set modes,etc

This is needed to keep door status up-to-date.

