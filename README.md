# Piramide
## Cosa è piramide?
-Programma che, dati dei mattoni in ingresso, ritorna il numero dei piani creabili con tali mattoni.
-In oltre, calcola anche i mattoni che sono in eccesso rispetto ai piani creati.


### Realizzazione del programma

#### Funzione per calcolare i piani

``` C#
 public static int Piani( int mattoni )
        {
            int piani = 0;
            int mattoniUsati = 0;
            while (mattoniUsati <= mattoni){
                piani++;
                mattoniUsati += piani * piani;
            }
            return piani - 1;
        }
``` 


#### Funzione per calcolare i blocchi in eccesso
``` C#
public static int Rimanenti( int mattoni, int piani )
        {
            int mattoniUsati = 0;
            for (int i = 1; i<= piani; i++){
                mattoniUsati += i* i;
            }
            return mattoni - mattoniUsati;
        }
```
