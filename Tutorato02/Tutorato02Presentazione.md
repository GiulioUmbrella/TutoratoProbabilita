---
title: Tutorato 02
author: Giulio Umbrella
---

# Interpretazione coefficiente binomiale

Che cosa fa il coefficiente binomiale? Prendiamo come esempio un mazzo con 52 carte e consideriamo le disposizioni e le combinazioni.

## Disposizioni

\# disposizioni = $52 \star 51$

## Combinazioni 

\# combinazioni =   $\binom{52}{2} = \frac{52!}{2!(52-2)!} = \frac{52 \star 51}{2}$

# Concetti base relativi alla probabilita'

Dato uno spazio campionario, valgono le seguenti proprieta'

- $P(\Omega) = 1$
- $P(\emptyset) = 0$
- $P(A) = 1 - P(A^{c})$
- Se $A \cap B = \empty$ allora $P(A \cup B) \ = \ P(A) \ + \ P(B)$
- $P(A) = \frac{|\Omega|}{|A|}$

In particolare, vale la seguente proprieta'

- $P(A \cup B) = P(A) + P(B) - P(A \cap B)$
- Se E,$E^{c}$ formano una partizione di $\Omega$ allora $P(A) = P(A \cap E) + P(A \cap E^{c})$

# Ex 01

Sia P(A)=0.4,P(B)=0.7,P($A \cup B$)=0.9, trovare:

1. P($A \cap B$)
2. P($A^{c} \cap B$)
3. P($A \backslash B$)
4. P($A^{c} \backslash B$)
5. P($A^{c} \cup B$)
6. P($A \cap (B \cup A^{c})$)

<!-- *Suggerimento* utilizzare la rappresentazione con i diagrammi di Eulero.

**Sol**  

1. P($A \cap B$) = P($A \cup B$) - P($A$) - P($B$)
2. P($A^{c} \cap B$) = P($A \cap B$) - P($B$)
3. P($A \backslash B$) = P($A \cup B$) - P($B$)
4.  -->


# Ex 02 

Si consideri l'esperimento in cui si lancia una moneta tre volte. Calcolare la probabilita' dei seguenti eventi:

1. A = {Escano esattamente due teste}
2. B = {Non esca nessuna testa}
3. C = {Esca una sola testa}
4. D = {Escano tre teste}
5. E = {Esca almeno una testa}

# Ex 02 Spazio campionario

| Moneta 1 | Moneta 2 | Moneta 3 |
|----------|----------|----------|
|     T    |     T    |     T    |
|     T    |     T    |     C    |
|     T    |     C    |     T    |
|     T    |     C    |     C    |
|     C    |     T    |     T    |
|     C    |     T    |     C    |
|     C    |     C    |     T    |
|     C    |     C    |     C    |

<!-- **Sol**  

Per prima cosa costruiamo uno spazio campionario formato dagli esiti. Sappiamo che ognuna delle tre monete ha due possibilie esiti {T,C} e lanciamo la moneta tre volte. Quindi sappiamo che i possibili esiti dell'esperimento corrispondo al risultato dei tre lanci 

Possiamo calcoare subito la **cardinalita'** dello spazio campionario come 2x2x2 = 8 elementi.

Per costruire lo spazio campionario Possiamo quindi usare il **prodotto cartesiano** nel seguente modo {T,C} x {T,C} x {T,C}. Ciascun degli elementi della tabella corrisponde ad un **esito**. 



Gli **eventi** sono insiemi formati da esiti. Per calcolare la probabilita', contiamo la cardinalita' degli eventi e dividiamo per la cardinalita' dello spazio campionario.


1. A = {Escano esattamente due teste} = {{T,T,C},{T,C,T},{C,T,T}}

$P(A) = \frac{|A|}{|\Omega|} = \frac{3}{8}$

2. B = {PNon esca nessuna testa} = {{C,C,C}}

$P(B) = \frac{|B|}{|\Omega|} = \frac{1}{8}$

3. C = {Esca una sola testa} = {{T,C,C}, {C,T,C}, {C,C,T}}

$P(C) = \frac{|C|}{|\Omega|} = \frac{3}{8}$

4. D = {Escano tre teste} = {{T,T,T}}

$P(D) = \frac{|D|}{|\Omega|} = \frac{1}{8}$

5. E = {Esca almeno una testa}= {{T,C,C}, {C,T,C}, {C,C,T}, {T,T,C}, {T,C,T},{T,T,C},{T,T,T}}
   
$P(E) = \frac{|E|}{|\Omega|} = \frac{7}{8}$   
 -->

# Ex 02 Commento

**NB** l'evento esca almeno una testa e' l'unione di altri eventi. Quali?

**NB** il lancio delle monete corrisponde alla ripetizione dello stesso elemento. Quando avremo strumenti piu' sofisticati -variabili aleatorie binomiali- potremo risolvere esercizi come questo molto piu' velocemente. 

**NB** In tutte le soluzioni il denominatore ha lo stesso valore 8. Quindi possiamo dire che sta **normalizzando** ciascuna soluzione perche' abbia un valore compreso fra 0 e 1. Rivredremo questo concetto quando introdurremo la **probabilita' condizionata**.

# Ex 03

Si lanciano due dadi distinti. Calcolare le seguenti probabilita'

1. La somma dei due valori sia 5
2. Escano due 1
3. Il risultato del secondo dado e' streattamente piu' piccolo del secondo

# Ex 03 Spazio campionario

|   |   1   |   2   |   3   |   4   |   5   |   6   |
|---|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
| 1 | (1,1) | (1,2) | (1,3) | (1,4) | (1,5) | (1,6) |
| 2 | (2,1) | (2,2) | (2,3) | (2,4) | (2,5) | (2,6) |
| 3 | (3,1) | (3,2) | (3,3) | (3,4) | (3,5) | (3,6) |
| 4 | (4,1) | (4,2) | (4,3) | (4,4) | (4,5) | (4,6) |
| 5 | (5,1) | (5,2) | (5,3) | (5,4) | (5,5) | (5,6) |
| 6 | (6,1) | (6,2) | (6,3) | (6,4) | (6,5) | (6,6) |

<!-- **Sol**

La meccanica di questo esercizio e' simile alla precedente. Costruiamo uno spazio campionario e contiamo la cardinalita' degli elementi.

Gli esiti sono dati dalle coppie dei risulati di ciascun dado {1,2,3,4,5,6} x {1,2,3,4,5,6} con cui costruiamo la tabella:



Le soluzioni sono date dal cardinalita' di ciascun evento, normalizzate per la cardinalita' dello spazio campionario.

1. A1 = {{4,1},{3,2},{2,3},{1,4}}
2. A2 = {{1,1}}

3. Possiamo contare gli elementi sopra la diagonale principale; il valore e' la somma degli interi fra 1 e 5 uguale a 5*(5+1)/2 = 15. -->

# Ex 04

Si consideri il lancio di 3 dadi distinti a 6 facce. Calcolare la probabilita' che il numero 5 esca solo una volta.

# Ex 04 Spazio campionario

- Costruire lo spazio campionario e contare tutte le volte in cui il 5 appare una volta sola. 

- **Problema** spazio campionario e' dato da $6 \star 6 \star 6 = 216$ elementi

- **Soluzione** In alternativa, possiamo usare il calcolo combinatorio. 
  
# Ex 04 Calcolo combinatiroio

A = {Il numero 5 esce solo una volta} e riscriviamolo come unione di tre eventi.

A = $\{5 \ primo \ elemento\} \cup \{5 \ secondo \ elemento\} \cup  \{5 \ terzo \ elemento\}$ 



<!-- Dato che i tre insiemi sono distinti, il numero totale di scelte e' dato dalla somma delle tre cardinalita'. Adesso dobbiamo calcolare la cardinalita' dei singoli insiemi.

Nel primo insieme sappiamo che il primo numero estratto e' 5, di conseguenza abbiamo altre due posizioni da riempire con i valori {1,2,3,4,6}. Attenzione a non considerare il numero 5 una seconda volta!

La terna ha forma (5,i,j) con i,j $\in$ {1,2,3,4,6}

Quindi scegliamo uno dei valori {1,2,3,4,6} come secondo valore e infine un valore {1,2,3,4,6}. Notare che scegliere una valore non significa che dobbiamo escluderlo. Ad esempio (5,2,2) e' un valore legittimo. Quindi in totale abbiamo 5x5 = 25 scelte.

Ora dobbiamo calcolare gli altri due insiemi. Le terne hanno rispettivamente forma (i,5,j) e (i,j,5) sempre con i,j $\in$ {1,2,3,4,6}. Ma questo significa che entrambe hanno la stessa cardinalita', ossia 25. Infatti la posizione di 5 non influenze le scelte che possiamo fare.

$P(A) = \frac{|A|}{|\Omega|} = \frac{3*25}{216}$ -->

# Ex 05

Un'urna contiene 10 palline bianche, 20 palline rosse e 30 nere. Calcolare la probabilita' che venga estratta una pallina bianca oppure una pallina nera.

<!-- **Sol**

Gli eventi estrarre una pallina bianca o pallina rossa sono mutualmente esclusivi quindi calcolare la probabilita' come la somma delle probabilita' dei due casi

P(Estraggo pallina bianca o rossa) = P(Estraggo pallina bianca) + P(Estraggo pallina rossa)
 -->
# Ex 06

Un'urna contiene 6 palline rosse e 4 bianche. Vengono estratte **successivamente** due palline. Calcolare la probabilita' che siano entrambe rosse nell'ipotesi che ci sia o non ci sia reimmissione.

# Ex 06 Spazio campionario 

- Spazio campionario con elementi (Colore prima pallina, Colore seconda pallina). 

- $\Omega$ = {{R,R},{R,B},{B,R},{B,B}}. Il testo ci chiede di calcolare la probabilita' di {R,R}.

# Ex 06 Spazio campionario 01

- Tuttavia, conviene ragionare in modo diverso, pensando alla palline come se fossero **identificabili**, ad esempio numerate. 
  
- Il risultato non viene influenzato, ma ci aiuta ad utilizzare gli strumenti del calcolo combinatorio.

- $\Omega$ = {R-01,R-02,R-03,R-04,R-05,R-06,B-07,B-08,B-09,B-10}


# Ex 06 Con reimmissione

Grazie alla numerazione delle palline, lo spazio campionario e' formato da $10 \star 10 = 100$ elementi.

 <!-- Infatti abbiamo infatti dieci scelte per la prima estrazione, e altrettante per la seconda. Notare che non stiamo considerando il colore delle palline. -->

<!-- L'evento che ci interessa e' formato da coppie di palline rosse, quindi e' del tipo A = {{R-01,R-01},{R-01,R-02},...{R-06,R-06}}. Per calcolare la probabilita', dobbiamo calcolare la sua cardinalita'. -->

<!-- Per farlo utilizziamo il calcolo combinatorio. Abbiamo infatti 6 palline rosse da cui scegliere per la prima estrazione e altrettante per la seconda. Il totale della scelte e' $6 \star 6 = 36$. -->

<!-- Possiamo verificare che in questo modo la somma di tutti i casi da 100 -->

- (R,R), 6 * 6 = 36
- (R,B), 6 * 4 = 24
- (B,R), 4 * 6 = 24
- (B,B), 4 * 4 = 16

La probabilita' e' quindi $P(A) = \frac{36}{100}$

# Ex 06 Senza reimmissione

<!-- Anche in questo caso, ragioniamo come se le palline fossero distinte. Senza la reimmissione,  -->

- Per la prima estrazione abbiamo 10 palline mentre per la seconda 9 per un totale di 10 * 9 = 90 valori.

<!-- Per contare le coppie di palline rosse consideriamo l'evento A = {{R-01,R-02},{R-01,R-03 }...,{R-06,R-05}}. Notare che stiamo escludendo le coppie con lo stesso numero.

La cardinalita' di A e' data da $6 \star 5 = 30$ scelte, 6 per la prima pallina e 5 per la seconda. 

Anche in questo caso possiamo verificare che la somma di tutti i casi e' pari alla cardinalita' di $\Omega$ -->

- (R,R), 6 * 5 = 30
- (R,B), 6 * 4 = 24
- (B,R), 4 * 6 = 24
- (B,B), 4 * 3 = 12

La probabilita' e' quindi $P(A) = \frac{30}{90}$

# Ex 06 Commento

- Possiamo formalizzare un esperimento aleatorio in diversi modi ottenendo gli stessi risultati. Conviene fermarsi a riflettere su quale sia la forma che conviene scegliere.

- I concetti di probabilita' condizionata e indipendenza saranno utili per risolvere questo tipo di esercizi. 

# Ex 07

Un'urna contiene 6 palline rosse e 4 bianche. Vengono estratte **contemporaneamente** due palline. Calcolare la probabilita' che le palline siano delle stesso colore.

# Ex 07 Sol

Anche in questo caso conviene pensare alla palline come numerate, quindi usiamo la stessa notazione R-01,R-02,R-03,R-04,R-05,R-06,B-07,B-08,B-09,B-10.

Ma differenza del precedente esercizio, prendiamo due palline alla volta. Questo significa che la cardinalita' dei possibili risultati si riduce. Infatti  prima le coppie {R-01,B-07} e {B-07, R-01} erano diverse perche' estratte in due momenti, mentre adesso corrispondono allo stesso elemento. Non esiste infatti distinzione fra prima e seconda. 

La cardinalita' dello spazio campionario e' quindi data da $\Omega = \binom{6 + 4}{2}$

L'evento di interesse puo' essere pensato come l'unione di due eventi disgiunti; infatti posso pescare due palline rosse oppure due palline bianche. Possono quindi considerare le due probabilita' in modo separato e fare la somma.

Per le palline rosse ho $\binom{6}{2}$ modi distinti di pescarle, mentre per le bianche sono $\binom{4}{2}$.

La probabilita' e' quindi $P(A) = \frac{\binom{6}{2} +\binom{4}{2} }{\binom{10}{2}}$
