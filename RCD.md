# RCD (Residual Current Device) /  Differential Circuit Breaker

### References
* [Eaton - Residual Current Device](https://www.eaton.com/content/dam/eaton/products/electrical-circuit-protection/circuit-breakers/xeffect-rccb/eaton-rcd-application-guide-br019003en-en-us.pdf)
* [ABB - Protection against earth faults with Residual Current Devices](https://library.e.abb.com/public/9f0e99de3bc740288bc41ab95667f72f/RCD%20Technical%20Guide%20EN.pdf)


## Types by protection
[RCD Classifications](https://electrical-engineering-portal.com/types-of-residual-current-devices-rcd)
* RCCB (Residual Current Circuit-Breaker):  Without overload protection
* RCBO (Residual Current Circuit-Breaker with protection against overload): With overload protection
   * RCBO = RCCB + MCB
   * I.E [Schneider Multi9 RCBO](https://www.se.com/uk/en/product-range/1104-multi-9/12367803577-residual-current-devices-rcd/?N=1339672414) OR [CNC RCBO](https://cnc-official.com/search?type=product&options%5Bprefix%5D=last&options%5Bunavailable_products%5D=last&q=RCBO)
* MRCD (Modular Residual Current Device): Have a toroidal to measure Current [Link](https://www.bender.de/fileadmin/content/Products/f/e/MRCD_Fly_en.pdf)
* RCM (Residual Current Monitor): 
* CBR (Circuit Breaker incorpoorating Residual Current Proctection)
* SRCD (Socket-Outlet incorpoorating a Residual Current Device): Is a plug with RCD [Link](https://www.google.com/search?q=srcd+RCD&tbm=isch&ved=2ahUKEwiWieKKteT_AhUmsCcCHbvYAe0Q2-cCegQIABAA&oq=srcd+RCD&gs_lcp=CgNpbWcQAzoHCAAQigUQQzoFCAAQgAQ6BggAEAUQHjoGCAAQBxAeOgcIABAYEIAEUOkBWJ8HYKgJaABwAHgAgAFLiAG8AZIBATOYAQCgAQGqAQtnd3Mtd2l6LWltZ8ABAQ&sclient=img&ei=VVebZNaKD6bgnsEPu7GH6A4&bih=919&biw=958&rlz=1C1GCEA_enGB995GB995)
* PRCD (Portable Residual Current Device): Similar to the previous [Link](https://www.google.com/search?q=*+PRCD+(Portable+Residual+Current+Device)%3A+RCD&tbm=isch&ved=2ahUKEwiPy_aQteT_AhVXmicCHV__AQEQ2-cCegQIABAA&oq=*+PRCD+(Portable+Residual+Current+Device)%3A+RCD&gs_lcp=CgNpbWcQA1DSCljSCmCXGGgAcAB4AIABRIgBfZIBATKYAQCgAQGqAQtnd3Mtd2l6LWltZ8ABAQ&sclient=img&ei=YlebZI-SCte0nsEP3_6HCA&bih=919&biw=958&rlz=1C1GCEA_enGB995GB995)
* ELCB (Earth-leakage circuit breaker): Is the old name for RCCB

|  Type      | Symbol                          | Symbol                          |
| ---------- | ------------------------------- | ------------------------------- |
| RCCB       | ![alt text](/Pictures/30.png)   | ![alt text](/Pictures/45.png)   |
| RCBO       | ![alt text](/Pictures/31.png)   | ![alt text](/Pictures/46.png)   |


## How this work
![alt text](/Pictures/05.png)

Parameters
* IΔn = Rated Residual Operating Current [Corriente Nominal de disparo]
* In  = Rated current RCCB [Corriente Nominal]
* Inc  = Conditional short-circuit resistance [Corriente Nominal de Cortocicuito]
Is the maximum I can support without damage the RCD. 

![alt text](/Pictures/26.png)
* Im = Break Capacity [Capacidad Nominal de Apertura y Ruptura]

   Usually 1kA
If Current is >Im the contact can't be open

### Tripping Current:
|            | Action          |
| ---------- | --------------- |
| 0-0.5x IΔn | don't be trip   |
| 0.5-1x IΔn | uncertainty     |
| =>1x IΔn   | must be trip    |

### Does IΔn depend from the Voltage?
* In Europe : voltage-independent
* In America: voltage-dependent

This can be Important if the Neutral is broken (30 ppm):
* Voltage-independent
* Voltage-dependent


### Does the neutral be connected to de RCD?
![alt text](/Pictures/23.png)
* In the 1L + N, is clear that yes
* In the 3L + N, the same
The sum of L's + N must be 0 (or close to 0)

* What's happen if our instalation doesn't use Neutral?

![alt text](/Pictures/24.png)

To, the neutral must be connected to the imput N

* Can we use a 3L + N for a 1L + N?

![alt text](/Pictures/05.png)

Yes, only respect N ans Input output
BUT, if the RCD is digital, you will need this configuration:

![alt text](/Pictures/25.png)

* Position of the neutral, by default Right, but there are exceptions
If you put Neutral on left you can use standard Bus Bar RCD to MCB

![alt text](/Pictures/51.png)

### Types by Response time  (G vs S)
* Type G: General (= no delayed)
MIN time to Tripping = 10 ms
* Type S: Selectivity (= delayed)
MIN time to Tripping = 40 ms

|              | 1xIΔn | 2xIΔn | 5xIΔn |  500A IΔn |
| ------------ | ----- | ----- | ----- | --------- |
| Type G (max) | 0.30s | 0.15s | 0.04s | 0.04s     |
| Type G (min) | 0.01s | 0.01s | 0.01s | 0.01s     |
| Type S (max) | 0.50s | 0.20s | 0.15s | 0.15s     |
| Type S (min) | 0.13s | 0.06s | 0.05s | 0.04s     |

Why 10 ms for G is the minimum?

![alt text](/Pictures/28.png)

at 50 Hz, is half wave, thus will be a voltage through zero


| Type G  |  Type S     |
| ----------------------------- | --------------------------------- |
| ![alt text](/Pictures/15.png) | ![alt text](/Pictures/14.png)     |

![alt text](/Pictures/27.png)

### Types by Sensibility (IΔn) / Normalized values for IΔn

| Sensibility  | IΔn        |
| ------------ | ---------- |
| Very High    | 10 mA      |
| High         | 30 mA      |
| Normal       | 100-300 mA |
| Low          | 0.5 - 1 A  |

Normalized values for IΔn:
* 10 / 30 / 300 / 500 mA 
* 1 A

### Normalized values for In:
* 16 / 25 /4 A
* 63 / 80 / 100 A
for 40 °C if is more there is a table to calculate the In


### Why 30 mA?

![alt text](/Pictures/22.png)

[Reference](https://www.eaton.com/content/dam/eaton/products/electrical-circuit-protection/circuit-breakers/xeffect-rccb/eaton-rcd-application-guide-br019003en-en-us.pdf)
* AC-1 No Perception
* AC-2 Perception
* AC-3 Strong involuntary muscle contractions

## Types by Wave form

|  Wave form              | ICON                           | AC                              |  A                              |  F                                                                    |  B                                                                                                       |    Activation Trigger                                                                |
| ----------------------- | ------------------------------ | ------------------------------- | ------------------------------- | --------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| ICON  RCD               | N.A                            | ![alt text](/Pictures/01.png)   | ![alt text](/Pictures/02.png)   | <p> ![alt text](/Pictures/02.png) <p> ![alt text](/Pictures/04.png)   | <p> ![alt text](/Pictures/02.png) <p> ![alt text](/Pictures/04.png)  <p>  ![alt text](/Pictures/03.png)  | N.A.                                   |
| Sinusoidal AC  50Hz     | ![alt text](/Pictures/0A.png)  | X                               | X                               | X                                                                     | X                                                                                                        | 0.5 - 1 IΔn                            |
| Pulsating  50Hz         | ![alt text](/Pictures/0B.png)  | -                               | X                               | X                                                                     | X                                                                                                        | 0.35 -1.4 IΔn                          |
| Pulsating Rectificada   | ![alt text](/Pictures/0C.png)  | -                               | X                               | X                                                                     | X                                                                                                        | <p> 0.25 - 1.4 In (90º)  <p>0.11 - 1.4 In (135º)                                     |
| Pulsating + DC          | ![alt text](/Pictures/0D.png)  | -                               | X                               | X                                                                     | X                                                                                                        | <p> 1.4In + 6mA (Type A) <p> 1.4In + 10mA (Type F) <p> 1.4In + 0.4In (Type B)        |
| High Frequency (1KHz)   | ![alt text](/Pictures/0E.png)  | -                               | -                               | X                                                                     | X                                                                                                        | 0.5 - 1.4 In                           |
| DC                      | ![alt text](/Pictures/0F.png)  | -                               | -                               | -                                                                     | X                                                                                                        | 0.5 - 2 In                             |


* For AC 50 Hz, if IΔn is 30 mA, the trigger must be done between 15-30mA
* For pulse AC,  Type AC won't be activated
* For Pulsante + DC: Type A, must allow (before Trigger) 1.4 IΔn (AC component) + 6mA (DC component)
* For > 50Hz, only  type F & B can protect
* For DC, only Type B can protect


|  Type    | ICON                                                                                                     |  Comments                                                                                                                                                        |   Examples                                                                                                                                                         |      Standard                          |
| -------- | -------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------- | 
| AC       | ![alt text](/Pictures/01.png)                                                                            | <p> General type:  <p> Equipment resistive / capacitive / inductive <p> without electronic component                                                             | Electric Showers <p> Oven <p>  hub <p>  **Tugsten** Light                                                                                                          | <p>IEC / EN 61008 <p>IEC / EN 6100     |
| A        | ![alt text](/Pictures/02.png)                                                                            | <p> Pulsating are generated by  diode bridge rectifier <p> **Pulsating can have a DC of max 6mA** <p>  ![alt text](/Pictures/09.png) <p> Electronic Components   | Inverters <p>  Leds <p>  PowerSupply Class II <p>  **Induction** Hobs <p> Electric Vehicle (**Type 2**) [Slow]                                                     | <p>IEC / EN 61008 <p>IEC / EN 6100     |
| F        | <p> ![alt text](/Pictures/02.png) <p> ![alt text](/Pictures/04.png)                                      | <p> Frequency Controlled <p>  Variable speed driver                                                                                                              | Air Acconditioner <p>  Washing machines & dishwasher <p>  Tumble Driers  <p>  Inverter **1 phase**                                                                 | <p>IEC / EN 62423                      |
| B        | <p> ![alt text](/Pictures/02.png) <p> ![alt text](/Pictures/04.png)  <p>  ![alt text](/Pictures/03.png)  | <p> For single and 3 Phase equipment                                                                                                                             | Inverter **3 phase** <p> UPS <p> photovoltaic system <p> Lifts <p> escalator <p> welding equipment <p> Electric Vehicle (**Type 3**) [semi - Fast]                 | <p>IEC / TR 60755 <p>IEC / EN 62423    |
| Bfq      | <p> ![alt text](/Pictures/02.png) <p> ![alt text](/Pictures/04.png)  <p>  ![alt text](/Pictures/03.png)  | <p> Special version for frequency Inverters up to 20 KHz <p>Sensitivity up to 300 mA                                                                             | Frequency Inverters                                                                                                                                                | <p>IEC / EN 62423                      |
| B+       | <p> ![alt text](/Pictures/02.png) <p> ![alt text](/Pictures/29.png)  <p>  ![alt text](/Pictures/03.png)  | <p> Special version for protect against fire <p> Sensitibity up 420 mA                                                                                           |                                                                                                                                                                    | <p>VDE 0664-440                        |                      

## Type F / SI : High immunization / Superimmunized
* Must be tested as Type A
* Other Icons:

|  ICON                           |
| ------------------------------- |  
| ![alt text](/Pictures/08.png)   |

###  Fugas naturales  
Residual Current that always exits, even without isolation fault 

|            Pics                     |  Comments      |
| ----------------------------------- | --------------------------------------------- | 
| ![alt text](/Pictures/10.png)       | switched source from computers: <p> * These source must avoid insert noise into electric net <p> * and must be protected from electromagnetic field    |
| ![alt text](/Pictures/11.png)       | Must have capatitator filter between L and E: <p> thus, create a residual current permanent |
| ![alt text](/Pictures/12.png)       | between 0.5 - 1 mA |

### Spurious trip [Disparo intenspestivo] [disparos por simpatia] / false positives 
* [SE_disparos por simpatia](https://www.se.com/es/es/faqs/FAQ000225847/)  Falta !!
* [Échame un cable: ¿Qué son los disparos intempestivos de los interruptores diferenciales, y cómo podemos evitarlos?](https://blogespanol.se.com/hogares/2022/02/02/echame-un-cable-que-son-los-disparos-intempestivos-de-los-interruptores-diferenciales-y-como-podemos-evitarlos/)  falta !!

|  The sum of all must be < 30% IΔn  in any case            |
| --------------------------------------------------------- |  
| Type F will detect random peak avoinding spurious trip    |

## Type B
* Type F: **only** 6 mA on Pulsanting DC
* Type B: Resicual Current on DC **10 mA**



## Type S (Time - Delayed) / Selectivity (Discrimination) / Vertical Selectivity / Coordination

* [Video: Selectividad diferencial vertical](https://www.youtube.com/watch?v=8oNrytLkZLY)
* [Circuitor: The 3 essential rules for selectivity in earth leakage protection](https://circutor.com/en/articles/the-3-essential-rules-for-selectivity-in-earth-leakage-protection/)
* [Coordination of residual current protective devices](https://www.electrical-installation.org/enwiki/Coordination_of_residual_current_protective_devices)
* [Selectivity of Residual Current Devices (RCDs)](https://www.electrical-installation.org/enwiki/Selectivity_of_Residual_Current_Devices_(RCDs)) falta !!
* [ABB - Protection against earth faults with Residual Current Devices (Pag 63)](https://library.e.abb.com/public/9f0e99de3bc740288bc41ab95667f72f/RCD%20Technical%20Guide%20EN.pdf)

* Important when we have 'n' RCD in Series (RCD Chained)
* Simbol: ![alt text](/Pictures/06.png)

Conditions for full selectivity:
* Amperometric selectivity: upstream RCD must have 2x IΔn than downstream
	See [Types by Sensibility](https://github.com/albertoRamon/RaspPicoIOT/blob/main/RCD.md#types-by-sensibility-i%CE%B4n)
* Selectivity Cronometrica: upstream RCD must have a response time > downstream
	See [Types by Response time  (G vs S)](https://github.com/albertoRamon/RaspPicoIOT/blob/main/RCD.md#types-by-response-time--g-vs-s)
* Type selectivity: upstream must be the same or higer type than downstream (AC < A < F < B)
![alt text](/Pictures/21.png)

Conditions for partial selectivity:
* Amperometric selectivity: <the same>
The downstream RCD will be Trpped only: IΔn downstream < IΔn < 0.5 IΔn upstream

### If you have a chain of 2 RCD
1. Type G (downstream)
2. Type S (upstream)

### If you have a chain of >2 RCD, you **can't** do this: 
1. Type G (downstream)
2. Type S (upstream)
3. Type S (upstream)
Because level 2 & 3 have same response time
Solution: 
1. Type G (downstream)
2. Type S (upstream)
3. Residual current protection relay
[Schenaider RH99M](https://www.se.com/uk/en/product/56173/residual-current-protection-relay-vigirex-rh99m-30-ma-to-30-a-220-240-vac-50-60-hz-din-rail-mounting/)
[Circuitor Type B residual current protection](https://circutor.com/en/products/protection-and-control/residual-current-protection/type-b-residual-current-protection/product/P11951./)

### Σ Residual Current in downstream level
![alt text](/Pictures/16.png)
The problem in this scenario is:
* If the permanent residual current of each room is 10 mA
* them, the sum of all bottom level is 60mA
* For the upstream RCD 60 mA of permanent residual current will produce spurious trip
* The solution: RCD upstream level IΔn = 300 mA


## RCD Verifications / Measurements
* er IEC 60364-6: Verifications (2007)
* [Eaton - Residual Current Device (Pag 32)](https://www.eaton.com/content/dam/eaton/products/electrical-circuit-protection/circuit-breakers/xeffect-rccb/eaton-rcd-application-guide-br019003en-en-us.pdf)


|  Type                | Diagram                         |
| -------------------- | ------------------------------- |
| Loop Impedance       | ![alt text](/Pictures/33.png)   |
| Tripping  current    | ![alt text](/Pictures/34.png)   |

* Loop: check the trip and no trip 
* Tripping  current: meause when IΔn will be tripped


### Impedance with Earth

![alt text](/Pictures/37.png) 

Must be done after the RCD & RCD disconnected

## Incorrect Connection: Neutral  
|  Example                       | Comment                                   |
| ------------------------------ | ----------------------------------------- |
|![alt text](/Pictures/38.png)   | The feeding for L and N must be the same  |
|![alt text](/Pictures/39.png)   | The neutral cant be cros affter the RCD   |
|![alt text](/Pictures/40.png)   | The neutral cant be cros affter the RCD   |
|![alt text](/Pictures/41.png)   | 1  Neutral Block per RCD                  |


## Incorrect Connection: Feeding

* [Scheneider 1](https://www.se.com/za/en/faqs/FA401160/)
* [Scheneider 2](https://www.se.com/es/es/faqs/FA383193/)

|  * By default RCCB can be feeded from **Top ADN bottom**    | 
| ----------------------------------------------------------- |


* Some of them like Resi9 are indicate are compatible with bottom [also]
* thus are compaibles with XXX

![alt text](/Pictures/43.png) 

#### Exception: Self-Reclosing /  [Auto-rearme)
These have a sensor (wired externally or internnaly)
* [REC4-2P-40-30](https://circutor.com/en/products/protection-and-control/self-reclosing-overcurrent-and-residual-current-protection/residual-current-protection-and-self-reclosing/product/P26A21./)
* [RED: Reconectadores diferenciales](https://www.se.com/es/es/product-range/1466-red/)
* [¿Cuáles son las diferencias técnicas entre diferencial rearme automático REDs (versión Antigua vs Nueva)?](https://www.se.com/es/es/faqs/FA406632/)

![alt text](/Pictures/42.png) 

|  Circuitor                     | Schenaider                      |
| ------------------------------ | ------------------------------- |
|![alt text](/Pictures/42.png)   | ![alt text](/Pictures/44.png)   |

