# RCD (Residual Current Device) /  Differential Circuit Breaker

### References
* [Eaton - Residual Current Device](https://www.eaton.com/content/dam/eaton/products/electrical-circuit-protection/circuit-breakers/xeffect-rccb/eaton-rcd-application-guide-br019003en-en-us.pdf)

## Types by protection
[RCD Classifications](https://electrical-engineering-portal.com/types-of-residual-current-devices-rcd)
* RCCB (Residual Current Circuit-Breaker):  Without overload protection
* RCBO (Residual Current Circuit-Breaker with protection against overload): With overload protection
   * RCBO = RCCB + MCB
   * I.E [Schneider Multi9 RCBO](https://www.se.com/uk/en/product-range/1104-multi-9/12367803577-residual-current-devices-rcd/?N=1339672414) OR [CNC RCBO](https://cnc-official.com/search?type=product&options%5Bprefix%5D=last&options%5Bunavailable_products%5D=last&q=RCBO)
* MRCD (Modular Residual Current Device): Have a toridal to measure Current [Link](https://www.bender.de/fileadmin/content/Products/f/e/MRCD_Fly_en.pdf)
* RCM (Residual Current Monitor): 
* CBR (Circuit Breaker incorpoorating Residual Current Proctection)
* SRCD (Socket-Outlet incorpoorating a Residual Current Device): Is a plug with RCD [Link](https://www.google.com/search?q=srcd+RCD&tbm=isch&ved=2ahUKEwiWieKKteT_AhUmsCcCHbvYAe0Q2-cCegQIABAA&oq=srcd+RCD&gs_lcp=CgNpbWcQAzoHCAAQigUQQzoFCAAQgAQ6BggAEAUQHjoGCAAQBxAeOgcIABAYEIAEUOkBWJ8HYKgJaABwAHgAgAFLiAG8AZIBATOYAQCgAQGqAQtnd3Mtd2l6LWltZ8ABAQ&sclient=img&ei=VVebZNaKD6bgnsEPu7GH6A4&bih=919&biw=958&rlz=1C1GCEA_enGB995GB995)
* PRCD (Portable Residual Current Device): Similar to the previous [Link](https://www.google.com/search?q=*+PRCD+(Portable+Residual+Current+Device)%3A+RCD&tbm=isch&ved=2ahUKEwiPy_aQteT_AhVXmicCHV__AQEQ2-cCegQIABAA&oq=*+PRCD+(Portable+Residual+Current+Device)%3A+RCD&gs_lcp=CgNpbWcQA1DSCljSCmCXGGgAcAB4AIABRIgBfZIBATKYAQCgAQGqAQtnd3Mtd2l6LWltZ8ABAQ&sclient=img&ei=YlebZI-SCte0nsEP3_6HCA&bih=919&biw=958&rlz=1C1GCEA_enGB995GB995)
* ELCB (Earth-leakage circuit breaker): Is the old name for RCCB

|  Type      | Symbol                          |
| ---------- | ------------------------------- |
| RCCB       | ![alt text](/Pictures/30.png)   |
| RCBO       | ![alt text](/Pictures/31.png)   |


## How this work
![alt text](/Pictures/05.png)

Parameters
* IΔn = Rated Residual Operating Current
* In  = Rated current RCCB
* Ic  = Conditional short-circuit resistance 
Is the maximum I can support without damage the RCD
![alt text](/Pictures/26.png)


### Tripping Current:
|            | Action          |
| ---------- | --------------- |
| 0-0.5x IΔn | don't be trip   |
| 0.5-1x IΔn | uncertainty     |
| =>1x IΔn   | must be trip    |

### Does IΔn depend from the Voltage?
* In Europe : voltage-independent
* In America: voltage-dependent
This can be Important if the Neutral is broken (30 ppm)

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


|  Type    | ICON                                                                                                     |  Comments                                                                                                                                                        |   Examples                                                                                                                                |      Standard                          |
| -------- | -------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------- | 
| AC       | ![alt text](/Pictures/01.png)                                                                            | <p> General type:  <p> Equipment resistive / capacitive / inductive <p> without electronic component                                                             | Electric Showers <p> Oven <p>  hub <p>  **Tugsten** Light                                                                                 | <p>IEC / EN 61008 <p>IEC / EN 6100     |
| A        | ![alt text](/Pictures/02.png)                                                                            | <p> Pulsating are generated by  diode bridge rectifier <p> **Pulsating can have a DC of max 6mA** <p>  ![alt text](/Pictures/09.png) <p> Electronic Components   | Inverters <p>  Leds <p>  PowerSupply Class II <p>  **Induction** Hobs <p> Electric Vehicle (**Type 2**) [Slow]                            | <p>IEC / EN 61008 <p>IEC / EN 6100     |
| F        | <p> ![alt text](/Pictures/02.png) <p> ![alt text](/Pictures/04.png)                                      | <p> Frequency Controlled <p>  Variable speed driver                                                                                                              | Air Acconditioner <p>  Washing machines & dishwasher <p>  Tumble Driers                                                                   | <p>IEC / EN 62423                      |
| B        | <p> ![alt text](/Pictures/02.png) <p> ![alt text](/Pictures/04.png)  <p>  ![alt text](/Pictures/03.png)  | <p> For single and 3 Phase equipment                                                                                                                             | Inverter <p> UPS <p> photovoltaic system <p> Lifts <p> escalator <p> welding equipment <p> Electric Vehicle (**Type 3**) [semi - Fast]    | <p>IEC / TR 60755 <p>IEC / EN 62423    |
| Bfq      | <p> ![alt text](/Pictures/02.png) <p> ![alt text](/Pictures/04.png)  <p>  ![alt text](/Pictures/03.png)  | The vendor Eaton have a B type for max 20KHz                                                                                                                     |                                                                                                                                           | <p>IEC / EN 62423                      |
| B+       | <p> ![alt text](/Pictures/02.png) <p> ![alt text](/Pictures/29.png)  <p>  ![alt text](/Pictures/03.png)  | Is a B type for max 20KHz                                                                                                                                        |                                                                                                                                           | <p>VDE 0664-440                        |                      

## Type F / SI : High immunization / Superimmunized
* Must be tested as Type A
* Other Icons:

|  ICON                           |
| ------------------------------- |  
| ![alt text](/Pictures/08.png)   |

###  Fugas naturales / false positives  
Residual Current that always exits, even without isolation fault 

|            Pics                     |  Comments      |
| ----------------------------------- | --------------------------------------------- | 
| ![alt text](/Pictures/10.png)       | switched source from computers: <p> * These source must avoid insert noise into electric net <p> * and must be protected from electromagnetic field    |
| ![alt text](/Pictures/11.png)       | Must have capatitator filter between L and E: <p> thus, create a residual current permanent |
| ![alt text](/Pictures/12.png)       | between 0.5 - 1 mA |

### spurious trip / unwanted Tripping  [Disparo intenspestivo] / false positives 

|  The sum of all must be < 30% IΔn  in any case            |
| --------------------------------------------------------- |  
| Type F will detect random peak avoinding spurious trip    |

## Type B
* Type F: **only** 6 mA on Pulsanting DC
* Type B: Resicual Current on DC **10 mA**



## Type S (Time - Delayed) / Selectivity (Discrimination) / Vertical Selectivity / Coordination

[Video: Selectividad diferencial vertical](https://www.youtube.com/watch?v=8oNrytLkZLY)
[Circuitor: The 3 essential rules for selectivity in earth leakage protection](https://circutor.com/en/articles/the-3-essential-rules-for-selectivity-in-earth-leakage-protection/)


* Important when we have 'n' RCD in Series (RCD Chained)
* Simbol: ![alt text](/Pictures/06.png)

Conditions for full selectivity:
* Amperometric selectivity: upstream RCD must have 2x IΔn than downstream
	See [Types by Sensibility](https://github.com/albertoRamon/RaspPicoIOT/blob/main/RCD.md#types-by-sensibility-i%CE%B4n)
* Selectivity Cronometrica: upstream RCD must have a response time > downstream
	See [Types by Response time  (G vs S)](https://github.com/albertoRamon/RaspPicoIOT/blob/main/RCD.md#types-by-response-time--g-vs-s)
* Type selectivity: upstream must be the same or higer type than downstream (AC < A < F < B)
![alt text](/Pictures/21.png)

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