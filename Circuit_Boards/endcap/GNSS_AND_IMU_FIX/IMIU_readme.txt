Due to a design error, the IMU chip on the endcap has an undefined i2c address, so the Pi cannot talk to it. 
To enable the IMU unit, which may or not be iportant, solder a small bead to short pins 8 and 9
to each other. This fixes the i2c address. See the image IMU_pin_to_short.png to identify the correct pins.
