---
title: Tutorato 01
author: Giulio Umbrella
header-includes: 
  - \usepackage{tikz}
  - \def\firstcircle{(0,0) circle (1.5cm)}
  - \def\secondcircle{(0:2cm) circle (1.5cm)}
  - \colorlet{circle edge}{blue!50}
  - \colorlet{circle area}{blue!20}
  - \tikzset{filled/.style={fill=circle area, draw=circle edge, thick},
    outline/.style={draw=circle edge, thick}}

---

# Attivita' di oggi

1. Calcolo combinatorio
2. Operazioni fra insiemi


# Calcolo Combinatorio

Il calcolo combinatorio e' utilizzato per effettuare **conteggio** di elementi e fornisce gli strumenti essenziali per valutare le probabilita' di eventi. 

Dati n elementi voglaimo contare le possibili **disposizioni** oppure **combinazioni**.

- Disposizioni: **Considero** l'ordine degli elementi
- Combinazioni: **Non considero** l'ordine degli elementi 

# Principio del conteggio 

I principi basi del conteggio sono il principio dell'addizione e della moltiplicazione.

- Principio delle somma
- Principio della moltiplicazione

# Principio della moltiplicazione

Scelte applicate in sequenza si possono **moltiplicare**

Eg: se ho 4 camice, 3 paia di pantaloni e 2 scarpe, in quanti modi mi posso vestire?

# Principio delle somma

Scelte mutualmente esclusive si **sommano**

Eg: un'agenzia turistica mi offre 4 viaggi al mare, 3 viaggi in montagna e 5 citta' d'arte. Quante scelte ho?

# I due principi si possono combinare

Il MacDonald mi offre una scelta fra 

1. Una panino a scelta fra McChicken e CheeseBurger
2. Con o senza patatine
3. Bibita a scelta fra Coca, Pepsi e Dott. Pepper

Quanti menu' posso costruire?


# Disposizioni

Le disposizioni tengono conto della posizioni degli elementi. Possiamo individuare due casi, con o senza ripetizioni.

# Disposizioni con ripetizioni** 

Nelle disposizioni con ripetizioni possiamo considerare lo stesso elemento piu' volte.

1. Numero combinazioni cassaforte
2. Numero di posssibili sottoinsiemi


# Disposizioni senza ripetizioni**

Nelle disposizioni senza ripetizione una volta che scegliamo un elemento **non** possiamo piu' utilizzarlo.

1. Numero di possibili podi in una competizione sportiva
2. Numero di possibili arrivi


# Combinazioni

- La principali differenze delle combinazioni e' che **non** considerano l'ordine degli elementi. 

- Dobbiamo quindi utilizzare una tecnica di conteggio diversa che escluda le ripetizioni. Lo strumento che utilizziamo e' il **coefficiente binomiale**.

1. Dati n atleti, qual'e' il numero di possibili squadre con tre elementi?
2. Dato un mazzo di 52 carte, quanti sono i modi di avere due carte pari e due parte dispari?  

# Esercizio 1

Dato un mazzo di 52 carte:  

1. Quante mani di 5 carte possono essere formate?

2. Quanti possibile modi ci sono di avere carte dello stesso seme?

3. Quante possibili mani con 3 ma non 4 assi ci sono?

# Esercizion 2

Un comitato di k persone deve essere scelto da un insieme composto da 7 uomini e 4 donne.  Quandi modi di formare il comitato ci sono se:

1. Il comitato deve consistere di 3 donne e 2 uomini

2. Il comitato e' formato da un numero positivo di persone, ma deve avere lo stesso numero di uomini e di donne.

3. Il comitato e' formato da 4 persone e almeno una e' il Signor Rossi (non presente fra la scelta iniziale degli uomini).

4. Il comitato e' formato da 4 persone e almeno due devo essere donne.


# Operazioni insiemistiche 1

- Un **insieme** e' un raggruppamento di **oggetti** elementari. Possiamo dare diverse rappresentazioni, sia testuali che grafiche.

  - Elencazione $A = \{1,2,3,4,5,6\}$
  - Caratteristica $A = \{x | \textrm{x e' un intero compreso fra 1 e 6}\}$

- Dato un insieme A, possiamo definire un suo **sottoinsieme** B se ogni elemento di B e' un elemento di A, ${ B \subseteq A  \iff \forall x \in A  x \in B }$

- Dati due insiemi A e B possiamo stabilire se sono **uguali** verificando se sono uno sottoinsieme dell'altro. 


# Operazioni insiemistiche 2


- La **cardinalita'** di un insieme e' un intero che rappresenta il numero di elementi 
dell'insieme. 

- Possiamo definire il **prodotto cartesiano** fra due insieme A x B come insieme delle coppie che otteniamo prendendo un elemento da A e un elemento da B. Il risultato e' un insieme i cui elementi sono **coppie**.

Eg A = {1,2} e B = {3,4} allora AxB = {(1,3),(1,4),(2,3),(2,4)}.


# Operazioni elementari su insiemi

Per i seguenti esempi, ipotizziamo di avere un insieme E che chiamiamo universo e due sue sottoinsiemi A e B. Possiamo definire le seguenti operazioni su insiemi: 

1. Complementare
2. Unione
3. Intersezione
4. Differenza
5. Differenza simmetrica

# Complementare

Dato un insieme A il suo **complementare**, indicato con $A^{c}$ oppure $\overline{A}$, e' un insieme i cui elementi **non** appartengono ad A.

$A^{c} =\{ x in E | x \notin A \}$

# Unione

Dati due insieme A e B, definiamo l'**unione** come un insieme i cui elementi appartengono ad A oppure a B. 

<!-- % Set A or B -->
\begin{tikzpicture}
    \draw[filled] \firstcircle node {$A$}
                  \secondcircle node {$B$};
    \node[anchor=south] at (current bounding box.north) {$A \cup B$};
\end{tikzpicture}

In termini logici, stiamo eseguendo un OR inclusivo tra i due insiemi.

$A \cup B = \{w \in E | w \in A \ o \ w \in B \}$  

# Intersezione

Dati due insieme A e B, definiamo l'**intersezione** come un insieme i cui elementi appartengono ad A e a B.  

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

$A \cap B = \{w \in E | w \in A \ e \ w \in B \}$  

# Differenza

Dati due insiemi A e B, la differenza fra A e B e' l'insieme i cui elementi appartengono a A ma non a B

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

$A \setminus B = \{w \in E | w \in A \ e \ w \notin B \}$  

**NB**: la differenza non e' un'operazione simmetrica

# Differenza simmetrica

Dati due insiemi A e B, la differenza simmetrica e' un insieme i cui elementi appartengono ad esclusivamente a A o B, ma non ad entrambi.

<!-- %Set A or B but not (A and B) also known a A xor B -->
\begin{tikzpicture}
    \draw[filled, even odd rule] \firstcircle node {$A$}
                                 \secondcircle node{$B$};
    \node[anchor=south] at (current bounding box.north) {$\overline{A \cap B}$};
\end{tikzpicture}

$A \triangle B = \{w \in E | w \in A \ e \ w \notin B \}$  


# Decomposizioni in unioni disgiunte

La partizione di un insieme e' data da una famiglia di insieme con le seguenti proprieta'

- Gli insieme sono disgiunti 
- L'unione degli elementi della famigla forma l'insieme.

Nel caso del dado indichiamo E = {1,2,3,4,5,6}. Possiamo definire una partizione considerando l'insieme dei numeri pari e l'insieme dei numeri dispari.

- $P = \{2,4,6\} $
- $D = \{1,3,5\} $

E' immediato vedere che i due insiemi rispecchiano la condizione di partizione. 

NB: questa non e' l'unica partione possibile. Ad esempio, possiamo divedere nei numeri minori o maggiori di 3. 

# Decomposizione di un insieme rispetto ad una partizione

Dato un insieme e una partizione, possiamo riscrivere l'insieme come una decomposizione di unioni disgiunte. 

Possiamo definire un insieme come $A = {1,2,3,4}$ e considerando il fatto che contiene sia numeri pari che dispari ottenere la seguente partizione:

$A = \{ (A \cap P ) \cup ( A \cap B) \}$  

Notare che le due intersezioni sono formate da insieme disgiunti che una volta unite formano.

La decomposizione rispetto alla partizione e' un'operazione fondamentale, infatti vedremo piu' avanti che verra' utilizzata ampiamente per semplificare il calcolo della probabilita'.

# Decomposizione dell'unione di due eventi

Dati due insiemi A e B, possono riscrivere l'unione $A \cup B$ come l'unione di tre insieme disgiunti:

${ A \cup \ B = (A \setminus B) \cup (A \cap B) \cup (B \setminus A) }$


