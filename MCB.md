

# MCB (Miniature Circuit Breaker)
* IEC 60898
* GB 10963
* ITC-BT-22

* PdC 4.5KA
* Omnipolares



### Properties
* In Rated current = 10A [Calibre]
* Vn Rated Voltage = 230
* XXX  = 6000A[PdC, Poder de Corte]
* YYY = A/B/C or 1/2/3[Curva de disparo]


|   ![alt text](/Pictures/62.png)                             |     ![alt text](/Pictures/63.png)                  | ![alt text](/Pictures/64.png)                                | ![alt text](/Pictures/65.png)                              | 
| ----------------------------------------------------------- | -------------------------------------------------- |  ----------------------------------------------------------- | ---------------------------------------------------------- |
| <p>C10:   <p> Curve C <p> In =10A  <p> XXX=6KA   <p> 1P+1   | <p>iC60H: <p> Curve C <p> In =10A  <p> XXX=6KA     |  <p>C32:   <p> Curve C <p> In =32A  <p> XXX=4.5KA <p> 1P+1   |  <p>B32:   <p> Curve B <p> In =32A  <p> XXX=6KA <p> 1P+1   |

## How this work
* Sort-circuit: Magnetic
* Overload: Thermic (bimetal)

###  Tripping Curve standard 
Allow define an hierarchy (Selectivity)
![alt text](/Pictures/13.png)
* Curve B: Is the standard for domestic
* Curve C
* Curve D


### Normalized values for In:
* 6 / 10/ 16 / **20** / 25 / **32** /40 / **50** / 63 / 80 / **100** / **125** A
* Industrial: 125 / 160 / 250 / 400 / 630 / 800 / 1250 A

### Breaking capacity (I)
The maximum size of short-circuit current that can be handled.
1500 A
3000 A
4500 A
6000 A
10000 A
20000 A
25000 A


# MCB + Current Protect
* [2/3 PROTECCIÓN frente a SOBRETENSIONES permanentes y transitorias combinado con IGA](https://www.youtube.com/watch?v=NPNpR61kkC4&list=PL54-5yiMdV8FYDGRnyAfPefKPnuhqPtuQ&index=24)
* [Schneider Combi SPU 1603](https://www.se.com/il/en/product/16301/combi-spu-circuit-breaker-with-integrated-overvoltage-protection-1p-+-n-25a/)

| Transitorias + Permanentes      | 
| ------------------------------- | 
| ![alt text](/Pictures/66.png)   | 


### MCB (SPU) Transitorias 
* Protect from Thunders. Thus, 
   * Microseconds
   * There is no time to break the MCB (Mechanical system), need derived to eart
      
* Internally uses a Varistor: The resistence is lower when the voltege is to high
   ![alt text](/Pictures/69.png)
   ![alt text](/Pictures/20.png)
       
### MCB (MSU) Permanentes 
* (>> miliseconds) IE. Rotura del neutro
* Break the circuit (=Open)
   ![alt text](/Pictures/18.png)
    
# MCB + Volt Portect

### MCB + Over Voltage

### MCB + Under Voltage