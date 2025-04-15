# Sovol_SV08

This will my log of changes to my SV08 3D printer.

04-11-25
Cut CPU fan shroud for the first step to quiet the noise.

04-12-25
CPU Fan PWM
Modified printer.cfg 
Fixed the pin to PA1 and changed the target temp to 75. At 60 it would run constantly run at just below 10% causing a high pitch noise.

[temperature_fan CPUfan] # exhaust fan
pin: PA1
kick_start_time: 0.5
max_power: 1.0
min_temp: 0
max_temp: 90
hardware_pwm: true
target_temp: 75
sensor_type: temperature_host
max_speed: 1.0
min_speed: 0
control: pid
pid_Kp: 2     
pid_Ki: .5     
pid_Kd: 0.25     
pid_deriv_time: 5.0

04-13-25
Added G-Code to my slicer to automatically turn off the LED at the end of a print.

END_PRINT
mainled_off

