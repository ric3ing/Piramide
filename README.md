# Piramide
## Cosa è piramide?
Piramide è un programma che, dati dei mattoni in input, calcola quanti piani è possibile creare con tali mattoni e quanti ne sono in eccesso.



### Realizzazione del programma
Per la realizzazione del suddetto programma, sono state utilizzate le funzioni:

* Piani (per il calcolo dei piani);
* Rimanenti (per il calcolo dei mattoni in eccesso).

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


### Funzione per calcolare i blocchi in eccesso
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


#### Consegna del problema trattato per esteso
Quando si avvia un progetto come la costruzione di una piramide, è meglio pensarci due volte.

Il tuo compito oggi è scrivere un programma che calcoli l'altezza massima di una piramide (in piani) dato un certo numero di cubi di pietra.

Ipotizzando che:

* i piani della piramide siano quadrati
* la piramide da costruire sia compatta, cioè non ci siano cavità al suo interno. 
* ogni piano è quadrato, con una lunghezza laterale inferiore di due rispetto a quella sottostante.
* il primo piano è sempre di un mattone

Esempi:

* il primo piano ha un mattone, il secondo 9 mattoni, il terzo 25 e così via
* con 1 mattone la piramide è alta 1 piano
* con 84 mattoni la piramide è alta 4 piani

Va bene se hai blocchi rimanenti, purché tu costruisca una piramide completa.

Sviluppare:

* il metodo int Piani( int mattoni ) che torna il numero di piani
* il metodo int Rimanenti( int mattoni ) che torna il numero di mattoni rimasti dopo la costruzione


