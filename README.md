# longSlice

## Descrizione
Data una stringa formata solo da cifre, calcolare il prodotto più grande per una sua sottostringa contigua di cifre di lunghezza N (Versione Completa).
### Esempio
data in ingresso la stringa "1027839564", 

il prodotto più grande per una serie di 3 cifre è 270 (9 * 5 * 6)

e il prodotto più grande per una serie di 5 cifre è 7560 (7 * 8 * 3 * 9 * 5).


## Codice

![image](https://user-images.githubusercontent.com/127590071/235312616-7b9cb8a1-a31e-4dfc-8705-36461acf8dc2.png)

## Codice con commenti sul funzionamento

![image](https://user-images.githubusercontent.com/127590071/235312990-96bdb128-f0bf-414c-b608-4c7232608695.png)


## Descrizione codice con divisione in blocchi

* primo blocco

![image](https://user-images.githubusercontent.com/127590071/235313038-57ced551-38d0-4b51-9d68-195264bd4d29.png)
  
Il primo blocco di codice verifica se lo span è valido (cioè se non è negativo e non supera la lunghezza della stringa "digits"), altrimenti solleva un'eccezione ArgumentException con un messaggio di errore. 

* Secondo blocco

![image](https://user-images.githubusercontent.com/127590071/235313173-2aa227f1-4709-4f93-b300-d876feb7e618.png)

Il secondo blocco di codice gestisce il caso in cui lo span è 0, restituendo 1 come prodotto di default per una sequenza vuota.

* Terzo blocco

![image](https://user-images.githubusercontent.com/127590071/235313210-68986863-5755-44be-bf11-3f2494609051.png)

Il terzo blocco di codice implementa un ciclo for che scorre la stringa "digits" e,per ogni sequenza di lunghezza "span" trovata, calcola il prodotto delle cifre che la compongono. Se una cifra nella sequenza non è un carattere numerico, solleva un'eccezione ArgumentException con un messaggio di errore.
Il prodotto risultante viene confrontato con il prodotto più grande trovato finora e, se è maggiore, viene assegnato a "largestProduct".

* Quarto blocco

![image](https://user-images.githubusercontent.com/127590071/235313267-c1343dc9-478b-4dab-a10f-48e7d7f36a0f.png)

Infine, la funzione restituisce il valore di "largestProduct", che contiene il prodotto più grande trovato.
