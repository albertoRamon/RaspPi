
[NPN And PNP Proximity Sensors](https://www.omch.co/npn-and-pnp-proximity-sensors/)
[What is the difference between PNP and NPN when describing 3 wire connection of a sensor?](https://www.se.com/us/en/faqs/FA142566/)

## 3 Wire
| **N**PN                                                                    | **P**NP                                                                    |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| Switched **N**egative                                                      | Switched **P**ositive                                                      |
| ![alt text](/Pictures/68.png)                                              | ![alt text](/Pictures/67.png)                                              |
| <p> When the sensor is activated, <p> provide low output (Ground)          | <p> When the sensor is activated, <p> provide High output (+24)            |
| Called "Sinking"                                                           | Called Sourcing                                                            |
| Load is always connected to Postive (+24v)                                 | Load is always connected to Ground                                         |




* Brown: +V
* Black: output
* Blue: GND


* NPN are faster than PNP 
* PNP are recomended for PLC because avoid false-positive (if the wire is sort circuit)


## 4 Wire
The 3 wire PNP / NPN, the black can be NO or NC, you need check the instructions
The 4 Wire, include NO and NC, thus there are 2 output signals: Black and White