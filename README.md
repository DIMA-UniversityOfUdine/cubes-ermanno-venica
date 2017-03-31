# Primo progetto Grafica 3D Interattiva
![screenshot](/screenshot/4.JPG)
![screenshot](/screenshot/17.JPG)
##Concept##
L'idea iniziale è quella di far muovere dei cubi, disposti in una fila verticale, a destra e sinistra, con moto armonico, con diversi periodi.
Successivamente è stata ampliata modificando anche le caratteristiche di scala e colore secondo la stessa logica.
##Risultato##
Un gruppo di cubi, disposti sul piano xy, si muove di moto armonico lungo la direzione z con periodo diverso in base alla posizione.
Ciò è stato realizzato inserendo le mesh in un array bidimensionale e usando la somma degli indici per definire il periodo:
factor = Math.sin(time * (i+j-31.5) / (5000));
Il colore viene definito singolarmente sui tre canali R, G e B (con valore compreso fra 0 e 1) rispettivamente in base agli indici i, j e i+j, 
questo genera tutte le possibili combinazioni di colore durante l'esecuzione del codice.
##Difficoltà##
I punti che hanno richiesto più tempo sono stati la creazione di un array a due dimensioni e l'assegnazione dei colori.
##Video##
Il video presenta prima le singole caratteristiche animate (canale R, canale G, canale B ecc.) e la loro composizione parziale fino ad ottenere 
il risultato completo, per poi mostrarlo da più angolazioni e con movimento di camera.
##Annotazioni##
Nel codice sono lasciate commentate le parti che permettono il movimento automatico di camera attorno al cento degli assi.
La telecamera può essere posizionata in qualsiasi punto durante l'esecuzione, ma i più interessanti sono lungo i vettori (0, 0, 1), (0, 0, -1) e (-1, 1, 0).
