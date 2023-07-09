
### References7
* [Cómo Cablear un Cuadro Eléctrico de una vivienda según el reglamento electrotécnico de baja tensión](https://www.youtube.com/watch?v=DFk9neuSgxE)

## Protections
* Interruptor Control Potencia (ICP) (Optional*)
   * Prevents us from consuming more power than contracted with the electric provider
   * Is optional.  Algunos contadores telegestionados ya lo llevan integrado
   * Must be sealed and checked by electrical provider
   * Thus, must be in a separate enclosure
   
* Interruptor General Automatico (IGA) [es un magetoterminco]
   * Protect our distribution panel from overcurrents
   * Esta en la cabecera del cuadro, directamente de la derivacion individual

* Pequeno interruptor Automatico (PIA) [es un magetoterminco]  
   * Protect **one** circuit
   
* Protector contra sobretensiones (PCS) (Optional*)
   * Protect us from **External** over currenct
   * Transitorias (Rayos, Microsegundos)
      * Deriban a tierra, no hay tiempo de abrir circuito
      
      ![alt text](/Pictures/18.png)
      
      * Internally uses a Varistor: cuando el voltaje es muy alto la resistencia disminuya
      ![alt text](/Pictures/20.png)
       
   * Permanentes (>> miliseconds) IE. Rotura del neutro
   Open the circuit
    ![alt text](/Pictures/19.png)
    
   * Transitorias: " Recomendable" (IT-23 REBT)
   Endesa (NRZ103) Obligatoria
   ![alt text](/Pictures/17.png)
 
* Interruptor Differecial  (ID)

# Electrificacion

| Electrificacion  | Potencia   | IGA   | 
| ---------------- | ---------- | ----- | 
| Basica           | 5750W      | 25A   | 
| Basica           | 7360W      | 32A   |
| Elevada          | 9200W      | 40A   | 
| Elevada          | 11550W     | 50A   | 
| Elevada          | 11490W     | 63A   | 


## Electrificacion Basica Grado 1

 ![alt text](/Pictures/56.png)

| Circuit      | Use                                       | PIA     | Max Sockets  | Wire    | Socket         | Wire Cover   | Max per Socket  |
| ------------ | ----------------------------------------- | ------- | ------------ | ------- | -------------- | ------------ | --------------- |
| Circuit C1   | Iluminacion                               |  10A    | 30           | 1,5 mm2 |  Punto de luz  | 16 mm2       |   200W          |
| Circuit C2   | Toma uso general y grigorifico            |  16A    | 20           | 2,5 mm2 |  16A 2P+T      | 20 mm2       | 3.450W          |
| Circuit C3   | Cocina y horno                            |  25A    | 2            |  6  mm2 |  25A 2P+T      | 25 mm2       | 5.400W          |
| Circuit C4 * | Lavadora, Lavavajillas y termo electrico  |  20A    | 3            |  4  mm2 |  16A 2P+T      | 20 mm2       | 3.450W          |
| Circuit C5   | Tomas de corriente bano y cocina          |  16A    | 6            | 2,5 mm2 |  16A 2P+T      | 20 mm2       | 3.450W          |


### C4
Can be splitted in 3
| Circuit    |  Use               | Comment    | Comment | 
| ---------- |  ---------------- | ---------- | ------- | 
| C4.1       |  Lavadora         | 16A        | 2,5 mm2 | 
| C4.2       |  Lavavajillas     | 16A        | 2,5 mm2 | 
| C4.2       |  Termo electrico  | 16A        | 2,5 mm2 | 




# Electrificacion Elevada / Grado 2

 ![alt text](/Pictures/57.png)

| Circuit      | Use                    | PIA     |  Max Sockets  |Wire    | Socket         | Wire Cover   | Max per Socket  | Max per circuit    |
| ------------ | ---------------------- | ------- |  ------------ |------- | -------------- | ------------ | --------------- | ------------------ |
| Circuit C6   | Iluminacion            |  25A    |  N.A          |  6 mm2 |  N.A           | 25 mm2       | N.A.            | 5.750W             |
| Circuit C7   | Toma uso general       |  25A    |  N.A          |  6 mm2 |  N.A           | 25 mm2       | N.A.            | 5.750W             |
| Circuit C8   | Calefaccion            |  25A    |  N.A          |  6 mm2 |  N.A           | 25 mm2       | N.A.            | 5.750W             |
| Circuit C9   | Aire Acondicionado     |  25A    |  N.A          |  6 mm2 |  N.A.          | 25 mm2       | N.A.            | 5.750W             |
| Circuit C10  | Secadora               |  16A    |  1            |2,5 mm2 |  16A 2P+T      | 20 mm2       | 3.450W          | N.A.               |
| Circuit C11  | Automatizacion         |  10A    |  N.A          |1,5 mm2 |  N.A.          | 16 mm2       | N.A.            | 2.300W             |

* If we have more than 30 Lighta or 20 Sockets, we need use Electriccation Grado 2, Circuit  6 & 7
* If we have secadora, we need use Electriccation Grado 2
* Each 5 circuits whe need a RCD (4.1, 4.2, 4.3 are 1 circuit)

# Wires
6mm2 = 25A

# Questions

#### What is first IGA or the main RCD ?
The IGA then Main RCD

### Calculate IGA (In)
IGA (In) protect the Input and Output wire. Thus.
* I max supported by wire  >> IGA (In)
* The mm2 of IGA Input = Output (And the same for Input / Output Main RCD)



#### What must suppot more current IGA or the main RCD ?
The current is limited by the IGA
Thus the Main RCD, must support **IGA In or more**

#### How many circuist can protect a RCD ?
Max 5 Circuits (= PIA)
C4 count as 1 even if is spplited


