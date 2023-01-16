
**Klipper config for CPAP directly to BTT Octopus pro**

It should work on any of the 3 pin headers because they all use the same basic output schematic. 

The stock 3 pin 2.54mm pitch connector that goes from CPAP driver PCB to the variable resistor is actually the same 3 pin connector used on these MB! So you just have to move the pins around with small flat head screwdriver.. 

*Mellow Super 8 section below these pictures*

```yaml
[fan] #        CPAP print Cooling Fan\
pin: PG15 # for ocotopus pro Endstop 7 header
max_power: 1 # adjust below 1 if you would like the max speed to be slower
off_below: 0.2 # minimum speed where the fan starts spinning - on octopus pro this is correct - will be lower maybe 0 on mellow Super 8 because of different GPIO pullup and protection resistors
cycle_time: .0005 # = 2khz - CPAP fan driver recommended range is 2-50khz
```

![Model preview](https://github.com/clowrey/x5sa_pro_klipper/blob/main/CPAP%20fan%20config/CPAP%20driver%20pin%20location%20(Large).jpg)
![Model preview](https://github.com/clowrey/x5sa_pro_klipper/blob/main/CPAP%20fan%20config/CPAP%20driver%20to%20BTT%20octopus%20pro%20(Large).jpg)
![Model preview](https://github.com/clowrey/x5sa_pro_klipper/blob/main/CPAP%20fan%20config/Octopus%20pro%20recommended%20pins.jpg)
![Model preview](https://github.com/clowrey/x5sa_pro_klipper/blob/main/CPAP%20fan%20config/Octopus%20pro%20PCB%20GPIO%20pin%20names.jpg)

**Mellow Super 8 CPAP Config**

For the Mellow Super 8 the output schematic is quite different - with a 1k series resistor on almost all of the output pins, this in combination with the 10k pullup allows for the lowest voltage to be 0.3v - which is still below the turn on voltage of the CPAP fan driver I believe. 

The green circled HV in pin is the best one to use as it has no pullup. The other ones in yellow have 10k pullups so would be the second choice and should still work fine. 

here is a klipper example using the HV IN header:

```yaml
[fan] #        CPAP print Cooling Fan\
pin: PF3 # for mellow super 8 HI IN header
max_power: 1 # adjust below 1 if you would like the max speed to be slower
off_below: 0.2 # minimum speed where the fan starts spinning - on octopus pro this is correct - 
# will be lower maybe 0 on mellow Super 8 on pins with 10k pullup because of different GPIO pullup and protection resistors
# on HVin pin PF3 it will probably be 0.2 because of no pullup
cycle_time: .0005 # = 2khz - CPAP fan driver recommended range is 2-50khz
```

![Model preview](https://github.com/clowrey/x5sa_pro_klipper/blob/main/CPAP%20fan%20config/Super%208%20recommended%20pins.jpg)
![Model preview](https://github.com/clowrey/x5sa_pro_klipper/blob/main/CPAP%20fan%20config/Super%208%20PCB%20underside%20GPIO%20names.jpg)
