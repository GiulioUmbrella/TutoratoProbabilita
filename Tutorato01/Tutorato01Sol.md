---
title: Tutorato 01
author: Giulio Umbrella
header-includes: 
  - \usepackage{tikz}
---

# Calcolo combinatorio

Il calcolo combinatorio è utilizzato per effettuare **conteggio** di elementi e fornisce gli strumenti essenziali per valutare le probabilità di eventi.

Dati $n$ elementi vogliamo contare le possibili **disposizioni** oppure **combinazioni**.

- Disposizioni: **considero** l'ordine degli elementi
- Combinazioni: **non considero** l'ordine degli elementi 

## Principio del conteggio 

I principi basi del conteggio sono il principio dell'addizione e della moltiplicazione.

- Principio delle somma
- Principio della moltiplicazione

## Disposizioni

Le disposizioni tengono conto della posizioni degli elementi. Possiamo individuare due casi, con o senza ripetizioni.

### Disposizioni con ripetizioni

Nelle disposizioni con ripetizioni possiamo considerare lo stesso elemento più volte.

Ad esempio, data una cassaforte con codice a 6 cifre comprese fra 0 e 9 [0-9] il numero totale di possibile di codici $10^{6}$. Infatti, abbiamo 10 scelte per il primo valore, dieci scelte per il secondo e cosi via $10 \cdot 10 \cdot 10 \cdot 10 \cdot 10 \cdot 10$.

Un altro esempio è dato dal numero totate di sottoinsiemi di un insieme con cardinalità $n$. Per ciascun elemento possiamo fare una scelta, considerarlo oppure non considerarlo. Quindi il numero totale di scelte è $2^{n}$.

Notare che fra le diverse scelte possiamo decidere di escludere ogni elemento, ottenendo l'insieme vuoto. Quindi dato un qualsiasi insieme, il vuoto è sempre un suo sottoinsieme.

### Disposizioni senza ripetizioni

Nelle disposizioni senza ripetizione una volta che scegliamo un elemento non possiamo più utilizzarlo.

Ad esempio, in una competizione sportiva con n atleti il numero possibile di podi è dato da $n \cdot (n-1) \cdot (n-2)$. Per la prima posizione abbiamo $n$ scelte, ossia tutti gli atleti. Per la seconda posizione invece abbiamo $n-1$ scelte, perchè una volta che abbiamo scelto un atleta per il primo posto, non possiamo sceglierlo una seconda volta.

Notare che nel precedente esempio non stiamo utilizzando tutti i possibile atleti. Infatti una volta che abbiamo fatto tre scelte ci fermiamo. Se invece consideriamo tutti gli elementi stiamo eseguendo una permutazione.

## Permutazioni

Se abbiamo $n$ possibili scelte ed eseguiamo $n$ possibile scelte stiamo utilizzando tutti i possibile elementi e quindi abbaimo $n \cdot (n -1) \cdot (n-2) \cdot \ldots \cdot 2 \cdot 1$ scelte. Indichiamo questo valore con $n!$.

Nel caso degli atleti anziche considerare il numero di possibile podi, possiamo considerare il numero di possibili posizionamenti. Per semplicità ipotizziamo che tutti gli atleti facciano un punteggio diverso. In questo caso, abbiamo $n!$ possibili posizionamenti. 

**Attenzione**: a seconda dell'interpretazione che diamo al conteggio, dobbiamo utilizzare un metedo diverso. È quindi importante famigliarizzare con i concetti e capire quale formula dobbiamo utilizzare.

## Combinazioni

La principali differenze delle combinazioni è che **non** considerano l'ordine degli elementi. Quindi mentre nel caso del podio ad una competizione sportiva gli elementi $(a,b,c)$ e $(c,b,a)$ sono diversi, nelle combinazioni corrispondo allo stesso elemento.

Dobbiamo quindi utilizzare una tecnica di conteggio diversa che escluda le ripetizioni. Lo strumento che utilizziamo è il **coefficiente binomiale**.

Dati $n$ atleti, vogliamo considerare il modo di creare squadre composte da 3 elementi. Quindi se considero le squadra $(a,b,c)$ e $(c,b,a)$ sono uguali. Il numero totale di squadre di 3 atleti è:

$C(n,3) =  \binom{n}{3} = \frac{n!}{3!(n-3)!}$

Possiamo usare i metodi di conteggio con i principi iniziale. Ad esempio, dato un mazzo di 52 carte, quanti sono i modi di avere due carte pari e due parte dispari? 

Possiamo contare i due blocchi separatamente. Dato che 26 carte sono pari e 26 sono dispari, sappiamo che ci sono $\binom{26}{2}$ per scegliere le carte pari e altrettanti modi per quelle dispari. Quindi in totale abbiamo $\binom{26}{2} \cdot \binom{26}{2}$ scelte.

## Esercizi

**Ex 1**

Dato un mazzo di 52 carte:

1. Quante mani di 5 carte possono essere formate?

Per rispondere a questa domanda possiamo usare il coefficiente binomiale: $\binom{52}{5} = \frac{52!}{5!(52-5)!}$

2. Quanti possibili modi ci sono di avere carte dello stesso seme?

Dato che ci sono 4 semi, per ciascun tipo di seme abbiamo $\frac{52}{4} = 13$ carte. Quindi per ciascun seme abbiamo in totale $\binom{13}{5}$ possibili combinazioni. Dato che le scelte sono fra loro indipendenti possiamo sommare le diverse combinazioni e quindi il numero totale è $4 \cdot \binom{13}{5}$

3. Quante possibili mani con 3 ma non 4 assi ci sono?

Possiamo spezzare questo esercizio in due fasi diverse:
- Scelta degli assi
- Scelta delle due rimanenti carte.

Dati 4 assi sappiamo che ci sono $\binom{4}{3}$ modi di scegliere gli assi. A questo punto dobbiamo scegliere altre due carte dal resto del mazzo composto da 48 carte, 52 - 4 assi. Le restanti carte possono essere scelte in $\binom{48}{2}$ modi diversi. Dato che le scelte avvengono in modo indipendente, possiamo moltiplicare i due valori:

$\binom{4}{3} \ast \binom{48}{2}$

**Ex 2** 

Un comitato di $k$ persone deve essere scelto da un insieme composto da 7 uomini e 4 donne. Quandi modi di formare il comitato ci sono se:

1. Il comitato deve consistere di 3 donne e 2 uomini

Possiamo scegliere le donne in $\binom{7}{3}$ modi diversi; allo stesso modo possiamo scegliere gli uomini in $\binom{4}{3}$ modi diversi. Dato che le due scelte sono indipendenti abbiamo in totale $\binom{7}{3} \cdot \binom{4}{3}$ 

2. Il comitato è formato da un numero positivo di persone, ma deve avere lo stesso numero di uomini e di donne.

Dato che il numero di uomini è inferiore al numero di donne, so che il comitato può avere al massimo 8 elementi. Quindi procedo alla somma dei singoli casi:

$\binom{7}{1} \cdot \binom{4}{1} + \binom{7}{2} \cdot \binom{4}{2} + \binom{7}{3} \cdot \binom{4}{3} + \binom{7}{4} \cdot \binom{4}{4}$

Quindi dato il numero di uomini e donne uso il coefficiente binonimale per calcolare il rispettivo numero di scelte e poi moltiplico i due valori. Infatti le due scelte corrispondono a fasi diverse. Infine sommo i valori cosi ottenuti dato che corrispondono a casi mutualmente esclusivi.

3. Il comitato è formato da 4 persone e almeno una è il Signor Rossi (non presente fra la scelta iniziale degli uomini).

Il Signor Rossi è presente, questo vuol dire che abbiamo solo 3 scelte per il comitato. Dato che non abbiamo altre restrizioni, possiamo contare in totale $7 + 3 = 10$ persone. Quindi in totale si sono $\binom{10}{3}$ possibili scelte.

4. Il comitato è formato da 4 persone e almeno due devo essere donne.

Dato che devo avere almeno due donne, so che i seguenti comitati soddisfano la condizione:
- 2 donne e 2 uomini
- 3 donne e 1 uomo
- 4 donne

I quattro casi sono disgiunti, quindi posso sommare il numero di combinazioni:  

$\binom{7}{2} \cdot \binom{4}{2} + \binom{7}{3} \cdot \binom{4}{1} + \binom{7}{4} \cdot \binom{4}{0}$

# Operazioni insiemistiche 

<!-- DEFINIZIONI PER TIKZ -->
\def\firstcircle{(0,0) circle (1.5cm)}
\def\secondcircle{(0:2cm) circle (1.5cm)}

\colorlet{circle edge}{blue!50}
\colorlet{circle area}{blue!20}

\tikzset{filled/.style={fill=circle area, draw=circle edge, thick},
    outline/.style={draw=circle edge, thick}}

Ripassiamo gli insiemi e le principale operazioni.

## Proprietà insiemi

1. Definizione
2. Sottoinsieme
3. Uguaglianza fra insiemi
4. Insieme universo
5. Cardinalità
6. Prodotto cartesiano

Un **insieme** è un raggruppamento di **oggetti** elementari. Possiamo dare diverse rappresentazioni, sia testuali che grafiche.

Per elencazione $A = \{1,2,3,4,5,6\}$

Oppure per caratteristica $A = \{x | \textrm{x è un intero compreso fra 1 e 6}\}$

Dato un insieme $A$, possiamo definire un suo **sottoinsieme** $B$ se ogni elemento di $B$ è un elemento di $A$.

${ B \subseteq A  \iff \forall x \in A  x \in B }$

Dati due insiemi $A$ e $B$ possiamo stabilire se sono **uguali** verificando se sono uno sottoinsieme dell'altro. 

In altre parole, se $A$ è un sottoinsieme di $B$ e $B$ a sua volta è un sottoinsieme di $A$, allora i due insieme sono uguali.

**Domanda**: perchè in un insieme non ci sono elementi ripetuti? 

La **cardinalità** di un insieme è un intero che rappresenta il numero di elementi 
dell'insieme. L'insieme $A$ contiene 6 elementi quindi $\left|A\right| = 6$.

Possiamo definire il **prodotto cartesiano** fra due insieme $A \times B$ come insieme delle coppie che otteniamo prendendo un elemento da $A$ e un elemento da $B$. Il risultato è un insieme i cui elementi sono **coppie**.

Possiamo moltiplicare fra loro più di due insiemi $A \times B \times C$ e ottenere un insiemi formato da **terne** e cosi via.

$A = {1,2}$ e $B = {3,4}$ allora $A \times B = \{(1,3),(1,4),(2,3),(2,4)\}$.

## Operazioni elementari su insiemi

Per i seguenti esempi, ipotizziamo di avere un insieme $E$ che chiamiamo universo e due sue sottoinsiemi $A$ e $B$. Possiamo definire le seguenti operazioni su insiemi: 

1. Complementare
2. Unione
3. Intersezione
4. Differenza
5. Differenza simmetrica

Dato un insieme $A$ il suo **complementare**, indicato con $A^{c}$ oppure $\overline{A}$, è un insieme i cui elementi **non** appartengono ad $A$.

$A^{c} =\{ x \in E | x \notin A \}$

Dati due insieme $A$ e $B$, definiamo l'**unione** come un insieme i cui elementi appartengono ad $A$ oppure a $B$.

<!-- % Set A or B -->
\begin{tikzpicture}
    \draw[filled] \firstcircle node {$A$}
                  \secondcircle node {$B$};
    \node[anchor=south] at (current bounding box.north) {$A \cup B$};
\end{tikzpicture}

In termini logici, stiamo eseguendo un OR inclusivo tra i due insiemi.

$A \cup B = \{w \in E | w \in A o w \in B \}$  


Dati due insiemi $A$ e $B$, definiamo l'**intersezione** come un insieme i cui elementi appartengono ad $A$ e a $B$.

<!-- % Set A and B -->
\begin{tikzpicture}
    \begin{scope}
        \clip \firstcircle;
        \fill[filled] \secondcircle;
    \end{scope}
    \draw[outline] \firstcircle node {$A$};
    \draw[outline] \secondcircle node {$B$};
    \node[anchor=south] at (current bounding box.north) {$A \cap B$};
\end{tikzpicture}

In termini logici stiamo eseguendo un AND logico fra i due insiemi.

$A \cap B = \{w \in E | w \in A e w \in B \}$  

Dati due insiemi $A$ e $B$, la differenza fra $A$ e $B$ è l'insieme i cui elementi appartengono a $A$ ma non a $B$.

<!-- % Set A but not B -->
\begin{tikzpicture}
    \begin{scope}
        \clip \firstcircle;
        \draw[filled, even odd rule] \firstcircle node {$A$}
                                     \secondcircle;
    \end{scope}
    \draw[outline] \firstcircle
                   \secondcircle node {$B$};
    \node[anchor=south] at (current bounding box.north) {$A - B$};
\end{tikzpicture}

$A \setminus B = \{w \in E | w \in A e w \notin B \}$  

**NB**: la differenza non è un'operazione simmetrica.

Dati due insiemi $A$ e $B$, la differenza simmetrica è un insieme i cui elementi appartengono ad esclusivamente a $A$ o $B$, ma non ad entrambi.

<!-- %Set A or B but not (A and B) also known a A xor B -->
\begin{tikzpicture}
    \draw[filled, even odd rule] \firstcircle node {$A$}
                                 \secondcircle node{$B$};
    \node[anchor=south] at (current bounding box.north) {$\overline{A \cap B}$};
\end{tikzpicture}

$A \triangle B = \{w \in E | w \in A e w \notin B \}$  

## Decomposizioni in unioni disgiunte

La partizione di un insieme è data da una famiglia di insieme con le seguenti proprietà:

- Gli insieme sono disgiunti
- L'unione degli elementi della famigla forma l'insieme

Nel caso del dado indichiamo $E = \{1,2,3,4,5,6\}$. Possiamo definire una partizione considerando l'insieme dei numeri pari e l'insieme dei numeri dispari.

- $P = \{2,4,6\} $
- $D = \{1,3,5\} $

È immediato vedere che i due insiemi rispecchiano la condizione di partizione. 

**NB**: questa non è l'unica partione possibile. Ad esempio, possiamo divedere nei numeri minori o maggiori di 3. 

## Decomposizione di un insieme rispetto ad una partizione

Dato un insieme e una partizione, possiamo riscrivere l'insieme come una decomposizione di unioni disgiunte. 

Possiamo definire un insieme come $A = \{1,2,3,4\}$ e considerando il fatto che contiene sia numeri pari che dispari ottenere la seguente partizione:

$A = \{ (A \cap P ) \cup ( A \cap B) \}$

Notare che le due intersezioni sono formate da insieme disgiunti che una volta unite formano.

La decomposizione rispetto alla partizione è un'operazione fondamentale, infatti vedremo più avanti che verrà utilizzata ampiamente per semplificare il calcolo della probabilità.

## Decomposizione dell'unione di due eventi

Dati due insiemi $A$ e $B$, possono riscrivere l'unione $A \cup B$ come l'unione di tre insieme disgiunti:

${ A \cup \ B = (A \setminus B) \cup (A \cap B) \cup (B \setminus A) }$

# Esercizi Aggiuntivi

## Calcolo Combinatorio

## Operazioni insiemistiche

Dati i seguenti insiemi 
- $A = \{4,5,6\}$
- $B = \{0,1,2\}$
- $C = \{1,2,3\}$
- $D = \{2,3,7,8\}$

Indicare i risultati delle seguenti operazioni

1. $A \cap B$
2. $C \cup D$
3. $C \setminus D$
4. $D \setminus C$
5. $B \cup (C \setminus B)$
6. $A x B$
7. $(A \cup D) \cap (B \cup D)$
8. $A \cup (F \cap G)$
9. $(A \cup F) \cap (A \cup G)$
10. A x A ${\setminus}$ A x {4}