# ELEGOO Relay Module


* [Description](https://www.elegoo.com/products/elegoo-8-channel-relay-module-kit)
* [User Manual](/pdfs/ELEGOO_Relay/8 CHANNEL 5V 10A RELAY MODULE.pdf)
* [Electric Schema PDF](/pdfs/ELEGOO_Relay/8 Channel DC 5V Relay Module with Optocoupler Schematic diagram.pdf)
Datasheet:
* [Resources](https://www.elegoo.com/blogs/arduino-projects/elegoo-dc-5v-relay-module-tutorial)
* [Relay Datasheet SRD-05VDC](/pdfs/ELEGOO_Relay/SRD-05VDC-SL-C.pdf)
* [Fast switching Diode 1N4148](/pdfs/ELEGOO_Relay/1n4148.pdf)
* [Transistor S8050](/pdfs/ELEGOO_Relay/1n4148.pdf)
* [Opto PC817c 0241](/pdfs/ELEGOO_Relay/73758.pdf)



### Pros:
* 10A on 220V
* Optocoupler (low current digital input and shield) (See )
* The relay has 5 contacts (NOpen and NClose)
* Independent Vcc (JD-Vcc) for Electronic + Relay (See )

### Cons:
* I'm not sure if the current consumption in the datasheet is corret (See )
* There is not a resistence for Flyback diode
* In the public schematic diadram there are resistor of 102 and 511 Ohm, but on the PCB al are 102 (1K on [SMD Calculator](https://www.hobby-hour.com/electronics/smdcalc.php) )

### Relay + Fast Diode: Flyback Diode
[Reference](https://resources.altium.com/p/using-flyback-diodes-relays-prevents-electrical-noise-your-circuits)
[Wikipedia](https://en.wikipedia.org/wiki/Flyback_diode)
[Video](https://www.youtube.com/watch?v=yGem7tLQcFE)

![Picture](/images/01.png)
When the siwtch is closed,the current start to grow up slowly thus the inductor create a voltage opposite to the source
With the time, the current will grow-up until I=V/R and the voltage opposite will be 0

![Picture](/images/02.png)
When the switch is oppened suddenly, the current go down too fast, creating a high voltage to try the compensate the intensity

TIP: In some references, the put a resistor in serie with the inductor


### Calculate Iin
![Picture](/images/03.png)
Is important know the current demanded to Raspberry PI

Vcc=3.3/ 5.0
Vopto (Vf Forward voltage)=1.2
Vled= 1.8  (measured with multimeter)
R1=102 OHM

Volts in R1 = 3.3 - (1.2+1.8)=0.3
I3.3 = 0.3 / 1K = **0.3 ma (3.3v)**
I5.0 = 2 / 1K = 2 ma (5.0v)

### Calculate I JD-VCC
JD-VCC is used to give power to the opto + relay
Check that is 5 V, **NO 3.3**

Cirtcuit opto: 
* JD-VCC = 5v
* Vce Opto= 0.1
* R9=511
* Vbe = 1.2 Max

Volts in R9 = 5v - (0.1 + 1.2 ) = 3.7v
I opto = 3.7 / 511 = **7.24 mA**


Circuit Relay: 
* Type used "SRD-05VDC-SL-C" thus, Coil Sensitivity L=0.36W (high sensitivity)
* Coil Voltage = 5 V, thus nominal current **71.4 mA**

I JD-VCC (3.3) per relay = 0.3 + 7.24 + 71.4 = **78.9 mA**
I JD-VCC (5.0) per relay = 2 + 7.24 + 71.4 = 80.6 mA

I JD-VCC (3.3) total =  92.34 mA * 8 = **631 mA**


In the relay data-sheet the put 480mA:
![Picture](/images/04.png)




