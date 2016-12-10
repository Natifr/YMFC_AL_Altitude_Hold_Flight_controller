# YMFC_AL_Altitude_Hold_Flight_controller

first make sure you know this amazing project http://www.brokking.net/ymfc-al_main.html

in this YMFC you need to connect the LED to pin 13 (or just use the LED on the arduino...)
and channel 5 in to pin 12 (channel 5 is the switch you want to use to enable the Altitude Hold)

to use this i recomend the GY-86 10DOF (it is also possible to use MPU-6050 and MS5611 in 2 diffrent chips via the I2C) 

WARNING:
this is still test mode it needs an adjustment of PID values(it hovers about 1 meter up and down ... )


first time use:
1.use it 2 meters in the air until you test it.

2.hover for 5 sec then turn it on (i limited the PID gain max to 20 to avoid extrime behave therefore the starting point must be good)

about the code:
on top of Joop's YMFC i added 2 major parts:

1. reading via LPF the MS5611.
2. PID of the input. 

