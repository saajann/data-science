# Introduction to Statistical Learning
Playlist Youtube basata sul libro

### 1.1

Introduzione alla statistica (che sta alla base del machine learning) e delle sue applicazioni nel mondo.

La prima cosa che si deve fare quando si inizia a lavorare con un nuovo dataset è analizzare i dati attraverso i grafici, per capire bene le correlazioni tra i dati. 

Alcuni esempi di problemi statistici:
- prevedere se una persona avrà un infarto;
- classificare una mail come spam;
- riconoscere numeri / lettere scritte a mano;
- capire quali sono i fattori che influenzano gli stipendi.

### 1.2

The supervised learning problem
- X -> features
- Y -> outcome
- regression problem -> Y è quantitativa
- classification problem -> Y è qualitativa

The unsupervised learning problem
- X -> features
- no Y, no outcome, unlabeled data
- raggruppare gli oggetti (clustering per esempio)
- difficile capire come stai performando

Statistical Learning vs Machine Learning

### 2.1

#### Introduzione a modelli di Regressione

feature = input = predictor

Un modello può essere scritto come: 
Y = f(X) + €

La funzione di regressione (lineare) f(x)

f(x) = f(x1,x2,x3) = f(Y|X1=x1,X2=x2,X3=x3)

Possiamo avere un errore riducibili e uno irriducibile. Il nostro obiettivo è minimizzare l'errore riducibile

Per stimare f posso guardare i punti 'vicini' alla mia X

## 2.2

La dimensione dei dati gioca un ruolo fondamentale

Modello lineare

Tradeoffs:
- Prediction Accuracy vs interpretabilità
- Good fit vs undefit / overfit
- Poche feature vs tante feature

## 2.3

### Model Selection

- Mean Squared Error (MSE) -> sul Test data

### Bias-Variance Tradeoff

Il tradeoff bias-varianza è un concetto fondamentale in machine learning e statistica. Esso descrive il compromesso tra due tipi di errori che un modello può fare:

- **Bias**: errore dovuto a ipotesi troppo semplici nel modello. Un alto bias può portare a underfitting, dove il modello non cattura la complessità dei dati.
- **Varianza**: errore dovuto a ipotesi troppo complesse nel modello. Un'alta varianza può portare a overfitting, dove il modello si adatta troppo ai dati di training e non generalizza bene ai nuovi dati.

L'obiettivo è trovare un equilibrio tra bias e varianza per minimizzare l'errore totale.

## 2.4

### Classification 

La Y è qualitativa (email spam o no).

Per capire l'errore, semplicemente considero il numero di risposte sbagliate sul totale. 

Regressione logistica 

K-nearest neightbors -> k è il parametro di fine tuning. Circa un terzo dei problemi di classificazione può essere risolto con questo modello. Da tenere conto che questo modello può essere usato anche per problemi di regressione. 

## 3.1

### Simple Linear Regression

- Modello semplice ma efficace. 
- Esempio pubblicità - vendite
- Intervalli di confidenza