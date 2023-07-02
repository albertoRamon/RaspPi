*

# Electrificacion Basica
* Max 5.75kW or 25A monofasic

### Protections
* Interruptor Control Potencia (ICP)
   * Prevents us from consuming more power than contracted with the electric provider
   * Is optional.  Algunos contadores telegestionados ya lo llevan integrado
   * Must be sealed and checked by electrical provider
   * Thus, must be in a separate enclosure
   
* Interruptor General Automatico (IGA) [es un magetoterminco]
   * Protect our distribution panel from overcurrents
   * Esta en la cabecera del cuadro, directamente de la derivacion individual

* Interruptor General Automatico (PIA) [es un magetoterminco]  
   * Protect one circuit
   
* Protector contra sobretensiones (PCS)
   * Protect our from **External** over currenct
   * Transitorias (Rayos, Microsegundos)
      * Deriban a tierra, no hay tiempo de abrir circuito
        ![alt text](/Pictures/18.png)
	  * Internally uses a Varistor: cuando el voltaje es muy alto la resistencia disminuya
	    ![alt text](/Pictures/20.png)
	  
   * Permanentes (> miliseconds) IE. Rotura del neutro
   Open the circuit
    ![alt text](/Pictures/19.png)
	
   * Transitorias: Recomendable* (IT-23 REBT)
   Endesa (NRZ103) Obligatoria
   ![alt text](/Pictures/17.png)

### Circuits

| Circuit      | Use                                       | Comment | Comment |
| ------------ | ----------------------------------------- | ------- | ------- |
| Circuit C1   | Iluminacion                               |         |         |
| Circuit C2   | Uso general y grigorifico                 |         |         |
| Circuit C3   | Cocina y horno                            |         |         |
| Circuit C4 * | Lavadora, Lavavajillas y termo electrico  |         |         |
| Circuit C5   | Tomas de corriente bano y cocina          |         |         |


### C4
Can be splitted in 3
* Lavadora
* Lavavajillas
* Termo electrico