# YMFC_AL_Altitude_Hold_Flight_controller

first make sure you know this amazing project http://www.brokking.net/ymfc-al_main.html

in this YMFC you need to connect the LED to pin 13 (or just use the LED on the arduino...)
and channel 5 in to pin 12 (channel 5 is the switch you want to use to enable the Altitude Hold)

to use this i recomend to use GY-86 10DOF (it is possible to use MPU-6050 and MS5611 in 2 diffrent chips) 

WARNING:
this is still test mode it needs an adjustment of PID values (maybe also optimizing the code a bit).
first time use:
1.use up to 2 meters until you test it (it might crash as soon as you turn the Altitude Hold on...be rady to switch back to normal mode fast)
2.hover for 5 sec then turn it on.

about the code:
on top of Joop's YMFC i added 2 major parts:
1. reading - processing - PID from pressure sensor  MS5611 
2. once you fligh over 1.85 pressure diff - it will determine the best input to use with your drone (the point where the throttle input will keep the drone stable) 
