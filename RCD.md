# RCD (Residual Current Device) [Difrerenciales]


## Types by protection
[RCD Classifications](https://electrical-engineering-portal.com/types-of-residual-current-devices-rcd)
* RCCB (Residual Current Circuit-Breaker):  Without overload protection
* RCBO (Residual Current Circuit-Breaker with protection against overload): With overload protection
* MRCD (Modular Residual Current Device): Have a toridal to measure Current [Link](https://www.bender.de/fileadmin/content/Products/f/e/MRCD_Fly_en.pdf)
* RCM (Residual Current Monitor): 
* CBR (Circuit Breaker incorpoorating Residual Current Proctection)
* SRCD (Socket-Outlet incorpoorating a Residual Current Device): Is a plug with RCD [Link](https://www.google.com/search?q=srcd+RCD&tbm=isch&ved=2ahUKEwiWieKKteT_AhUmsCcCHbvYAe0Q2-cCegQIABAA&oq=srcd+RCD&gs_lcp=CgNpbWcQAzoHCAAQigUQQzoFCAAQgAQ6BggAEAUQHjoGCAAQBxAeOgcIABAYEIAEUOkBWJ8HYKgJaABwAHgAgAFLiAG8AZIBATOYAQCgAQGqAQtnd3Mtd2l6LWltZ8ABAQ&sclient=img&ei=VVebZNaKD6bgnsEPu7GH6A4&bih=919&biw=958&rlz=1C1GCEA_enGB995GB995)
* PRCD (Portable Residual Current Device): Similar to the previous [Link](https://www.google.com/search?q=*+PRCD+(Portable+Residual+Current+Device)%3A+RCD&tbm=isch&ved=2ahUKEwiPy_aQteT_AhVXmicCHV__AQEQ2-cCegQIABAA&oq=*+PRCD+(Portable+Residual+Current+Device)%3A+RCD&gs_lcp=CgNpbWcQA1DSCljSCmCXGGgAcAB4AIABRIgBfZIBATKYAQCgAQGqAQtnd3Mtd2l6LWltZ8ABAQ&sclient=img&ei=YlebZI-SCte0nsEP3_6HCA&bih=919&biw=958&rlz=1C1GCEA_enGB995GB995)


## Types by Response time

|               | In x1 | In x2 | In x5 |
| ------------- | ----- | ----- | ----- |
| Generic (max) | 0.30s | 0.15s | 0.04s |
| Custom  (max) | 0.50s | 0.20s | 0.15s |
| Custom (min)  | 0.13s | 0.06s | 0.05s |

Custom allow define an hierarchy


## Types by Wave form

|  Wave form              | ICON   | AC  |  A  |  F  |  B  |
| ----------------------- | ------ | --- | --- | --- | --- |
| Senoidal                | 0.30s  | X   | X   | X   | X   |
| Pulsante                | 0.50s  | -   | X   | X   | X   |
| Pulsante Rectificada    | 0.13s  | -   | X   | X   | X   |
| Pulsante + Continua     | 0.13s  | -   | X   | X   | X   |
| High Frequency (10KHz)  | 0.13s  | -   | -   | X   | X   |
| Continua                | 0.13s  | -   | -   | -   | X   |