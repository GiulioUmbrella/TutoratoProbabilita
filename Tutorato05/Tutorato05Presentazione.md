---
title: Tutorato 05
author: Giulio Umbrella
---

# Argomenti di oggi

1. Indipendenza
2. Esercizi

# Pillole di git

Come copio il repository il locale?

https://github.com/GiulioUmbrella/TutoratoProbabilita

# Pillole di git

`git clone https://github.com/GiulioUmbrella/TutoratoProbabilita`

# Indipendenza 

## Esempio 01

Data una moneta regolare, calcolare la probabilita' che esca testa sapendo che la massa del Sole e' 2×$10^{30}$ kg. 

## Esempio 02

Data una moneta regolare, calcolare la probabilita' che esca testa sapendo che esce croce.
  
\vspace{1in}

**Domanda**: qual'e' la differenza fra i due esempi?


# Indipendenza - Definizione

Due eventi sono **indipendenti** se la pro

## Due diverse definizioni 

$P(A|B) = P(A)$
$P(A \cap B) = P(A) \star P(B)$

# Independenza - 3 Eventi

Se abbiamo piu' tre eventi dobbiamo controllare piu' condizioni

- $P(A,B)=P(A) \star P(B)$
- $P(A,C)=P(A) \star P(C)$
- $P(B,C)=P(B) \star P(C)$
- $P(A,B,C)=P(A) \star P(B) \star P(B)$
  

# Indipendenza vs Disgiunti 

- Sono due concetti diversi!

- Se A e B sono indipendenti, A non da nessuna informazioni su B

- Se A e B sono disgiunti **non** possono verificarsi assiemi. Questo fornisce un'informazione!

# Esercizio Foglio 02 09

Sia $\Omega=\{0,1\}^{3}$ e P una misura di probabilta' **uniforme** su $\Omega$ con

- $A=\{w\in\Omega \ : \ w_{3}=0\}$ 
- $B=\{w\in\Omega \ : \ w_{1}=0\}$ 
- $C=\{000,010,100,101\}$ 

# Esercizio Foglio 02 09 Sol

|$w_{1}$|$w_{2}$|$w_{3}$|   |   |   |
|-------|-------|-------|---|---|---|
|   1   |   1   |   1   |   | B |   |
|   1   |   1   |   0   | A | B |   |
|   1   |   0   |   1   |   | B | C |
|   1   |   0   |   0   | A | B | C |
|   0   |   1   |   1   |   |   |   |
|   0   |   1   |   0   | A |   | C |
|   0   |   0   |   1   |   |   |   |
|   0   |   0   |   0   | A |   | C |

# Esercizio Foglio 02 07

Sia di un esempio di spazio di probabilita' ad eventi $A_{1}$, $A_{2}$ e B tali che:

- P(B) > 0 
- P($A_{1}$}|B) > P($A_{1}$})
- P($A_{2}$}|B) < P($A_{2}$})

# Esercizio Ross 27 

Supponiamo  sono due fabbriche - A e B - producono forni. I forni della fabbrica A hanno un difetto con probabilita' 0.05, mentre i forni prodotti da B hanno un difetto con probabilita' 0.01.  

Compriamo due forni, entrambi dalla stessa fabbrica

Se uno dei due forni e' difettato, qual'e' la probabilita' che anche il secondo forno sia difettato?

# Esercizio Ross 29

Chiedete al vostro vicino di inaffiare le piante mentre siete in vacanza. Senza acqua, la pianta muore con probabilita' 0.8, con acqua muore con probabilita' 0.15. Il vicino si ricorda di innaffiare con probabilta' del 0.9

1. Qual e' la probabilita' che la pianta sia viva?
2. Se la pianta e' morta, qual e' la probabilita' che il vicino non l'abbia inaffiata? Perche' in questo caso non siamo arrabbiati col vicino?
3. Supponiamo che la pianta sia un cactus e che la probabilita' che la pianta muoia senza acqua e' 0.05, mentre con acqua e' 0.01. Come cambiamo le probabilita' calcolate prima? Che cosa pensiamo del vicino adesso? 

# Esercizio Ross 29 commento

P(M|A) e P(M|NA) sommmate non fanno 1. Perche'?

# Esercizio Ross 31

Nella citta' di Springfield su un totale di 1000 persone, 600 sono iscritte al partito repubblicano mentre 400 a quello democratico.  

Alle elezione locali in cui partecipano tutti, 60 repubblicani votano democratico mentre 50 democratici votano repubblicano.  

Prendiamo un iscritto a caso al partito repubblicano qual e' la probabilita' che abbiamo votato democratico?

# Esercizio Ross 34

Il franking e’ una tecnica per estrarre petrolio dal sottosuolo. Per cercare gli appezzamenti migliori, viene controllata la densità del suolo. Tuttavia il test non e’ perfetto. Se il suolo non e’ denso il terreno contiene petrolio con probabilità’ del 0.135, mentre aumenta al 0.268 se il terreno contiene petrolio

Un petroliere esperto e’ convito che un certo appezzamento contenga petrolio con probabilità 0.7, calcolare la probabilità’ che   

1. il terrono sia denso
2. il test non e’ denso

Ripeti il ​​precedente, questa volta assumendo che il petroliere stimi che l’appezzamento contenga petrolio con probabilità’ del 0.3

# Esercizio Ross 34 Interpretazione

## Che dati abbiamo

- P(Petrolio|Suolo Denso) = 0.135
- P(Petrolio|Suolo Molle) = 0.268


## Cosa ci chiede l'esercizio

- P(Suolo Denso| Petrolio)
- P(Suolo Molle| Petrolio)


