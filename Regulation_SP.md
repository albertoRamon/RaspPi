*

# Electrificacion Basica
* Max 5.75kW or 25A monofasic

### Protections
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

### Circuits

| Circuit      | Use                                       | PIA     | Wire    | Socket         | Wire    |
| ------------ | ----------------------------------------- | ------- | ------- | -------------- | ------- |
| Circuit C1   | Iluminacion                               |  10A    | 1,5 mm2 |  Punto de luz  | 16 mm2  |
| Circuit C2   | Uso general y grigorifico                 |  16A    | 2,5 mm2 |  16A 2P+T      | 20 mm2  |
| Circuit C3   | Cocina y horno                            |  25A    |  6  mm2 |  25A 2P+T      | 25 mm2  |
| Circuit C4 * | Lavadora, Lavavajillas y termo electrico  |  20A    |  4  mm2 |  16A 2P+T      | 20 mm2  |
| Circuit C5   | Tomas de corriente bano y cocina          |  16A    | 2,5 mm2 |  16A 2P+T      | 20 mm2  |


### C4
Can be splitted in 3
| C4               | Comment    | Comment | 
| ---------------- | ---------- | ------- | 
| Lavadora         | 16A        | 2,5 mm2 | 
| Lavavajillas     | 16A        | 2,5 mm2 | 
| Termo electrico  | 16A        | 2,5 mm2 | 




# Electrificacion Grado 2
| Circuit      | Use                    | PIA     | Wire    | Socket         | Wire    | Max per Socket  | Max per circuit    |
| ------------ | ---------------------- | ------- | ------- | -------------- | ------- | --------------- | ------------------ |
| Circuit C8   | Calefaccion            |  25A    |   6 mm2 |  N.A           | 25 mm2  | N.A.            | 5.750W             |
| Circuit C9   | Aire Acondicionado     |  25A    |   6 mm2 |  N.A.          | 25 mm2  | N.A.            | 5.750W             |
| Circuit C10  | Secadora               |  16A    | 2,5 mm2 |  16A 2P+T      | 20 mm2  | 3.450W          | N.A.               |
| Circuit C11  | Automatizacion         |  10A    | 1,5 mm2 |  N.A.          | 16 mm2  | N.A.            | 2.300W             |

# Questions

#### What is first IGA or the main RCD ?

#### What must suppot more current IGA or the main RCD ?

#### How many circuist can protect a RCD ?
Max 5 Circuits (= PIA)
C4 count as 1 even if is spplited
