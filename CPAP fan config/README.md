
Klipper config for CPAP directly to BTT Octopus pro

Should also work with Mellow Super 8 on any of the 3 pin headers 

```
[fan] #        CPAP print Cooling Fan\
pin: PG15 # for ocotopus pro Endstop 7 header
max_power: 1 # adjust below 1 if you would like the max speed to be slower
off_below: 0.2 # minimum speed where the fan starts spinning - on octopus pro this is correct - will be lower maybe 0 on mellow Super 8 because of different GPIO pullup and protection resistors
cycle_time: .0005 # = 2khz - CPAP fan driver recommended range is 2-50khz
```

![Model preview](https://github.com/clowrey/x5sa_pro_klipper/blob/main/CPAP%20fan%20config/CPAP%20driver%20pin%20location%20(Large).jpg)
![Model preview](https://github.com/clowrey/x5sa_pro_klipper/blob/main/CPAP%20fan%20config/CPAP%20driver%20to%20BTT%20octopus%20pro%20(Large).jpg)
