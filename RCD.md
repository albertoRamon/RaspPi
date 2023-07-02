# RCD (Residual Current Device) /  Differential Circuit Breaker


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


## Types by Response time

|               | In x1 | In x2 | In x5 |
| ------------- | ----- | ----- | ----- |
| Generic (max) | 0.30s | 0.15s | 0.04s |
| Custom  (max) | 0.50s | 0.20s | 0.15s |
| Custom  (min) | 0.13s | 0.06s | 0.05s |

Custom allow define an hierarchy (Selectivity)


## Types by Wave form

|  Wave form              | ICON                           | AC                              |  A                              |  F                                                            |  B                                                                                          |    Activation Trigger      |
| ----------------------- | ------------------------------ | ------------------------------- | ------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | -------- |
| ICON  RCD               | N.A                            | ![alt text](/Pictures/01.png)   | ![alt text](/Pictures/02.png)   | <p> ![alt text](/Pictures/02.png) <p> ![alt text](/Pictures/04.png)   | <p> ![alt text](/Pictures/02.png) <p> ![alt text](/Pictures/04.png)  <p>  ![alt text](/Pictures/03.png)  | N.A. |
| Sinusoidal AC  50Hz     | ![alt text](/Pictures/0A.png)  | X                               | X                               | X                                                             | X                                                                                           | 0.5 - 1 IΔn             |
| Pulsating  50Hz         | ![alt text](/Pictures/0B.png)  | -                               | X                               | X                                                             | X                                                                                           | 0.35 -1.4 IΔn                          |
| Pulsating Rectificada   | ![alt text](/Pictures/0C.png)  | -                               | X                               | X                                                             | X                                                                                           | <p> 0.25 - 1.4 In (90º)  <p>0.11 - 1.4 In (135º)     |
| Pulsating + DC          | ![alt text](/Pictures/0D.png)  | -                               | X                               | X                                                             | X                                                                                           | <p> 1.4In + 6mA (Type A) <p> 1.4In + 10mA (Type F) <p> 1.4In + 0.4In (Type B)        |
| High Frequency (1KHz)   | ![alt text](/Pictures/0E.png)  | -                               | -                               | X                                                             | X                                                                                           | 0.5 - 1.4 In             |
| DC                      | ![alt text](/Pictures/0F.png)  | -                               | -                               | -                                                             | X                                                                                           | 0.5 - 2 In             |


* For AC 50 Hz, if IΔn is 30 mA, the trigger must be done between 15-30mA
* For pulse AC,  Type AC won't be activated
* For Pulsante + DC: Type A, must allow (before Trigger) 1.4 IΔn (AC component) + 6mA (DC component)
* For > 50Hz, only  type F & B can protect
* For DC, only Type B can protect


|  Type    | ICON                                                                                                     |  Comments                                                                                            |   Examples |
| -------- | -------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | -------------------------------------------------------------- | 
| AC       | ![alt text](/Pictures/01.png)                                                                            | <p> General type:  <p> Equipment resistive / capacitive / inductive <p> without electronic component | Electric Showers / Oven / hub / **Tugsten** Light      |
| A        | ![alt text](/Pictures/02.png)                                                                            | <p> Pulsating are generated by  diode bridge rectifier <p> Pulsating can have a DC of max 6mA <p>  ![alt text](/Pictures/09.png) <p> Electronic Components  | Inverters, Leds, PowerSupply Class II, **Induction** Hobs, Electric Vehicle      |
| F        | <p> ![alt text](/Pictures/02.png) <p> ![alt text](/Pictures/04.png)                                      | <p> Frequency Controlled / Variable speed driver                                           |  Air Acconditioner / Washing machines & dishwasher / Tumble Driers   |
| B        | <p> ![alt text](/Pictures/02.png) <p> ![alt text](/Pictures/04.png)  <p>  ![alt text](/Pictures/03.png)  | <p> For single and 3 Phase equipment                                                      | Inverter , UPS, photovoltaic system, Lifts, escalator, welding equipment     |


## Type F / SI : High immunization / Superimmunized
* Must be tested as Type A
* Other Icons:

|  ICON                           | ICON                            |
| ------------------------------- | ------------------------------- |  
| ![alt text](/Pictures/08.png)   | ![alt text](/Pictures/08.png)   |

## Type S (Time - Delayed)


## Selectivity (Discrimination)
* Important when we have 'n' RCD in Series (RCD Chained)
*
* Simbol: ![alt text](/Pictures/06.png)

## How this work
![alt text](/Pictures/05.png)