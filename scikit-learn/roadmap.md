# Roadmap Scikit-Learn

Questa roadmap ti guiderà attraverso tutti i concetti fondamentali di Scikit-Learn. Ogni giorno è progettato per costruire competenze in modo graduale e pratico.

## Giorni 1-5: Introduzione e Preprocessing dei Dati

### Giorno 1: Panoramica di Scikit-Learn

**Familiarizzati con la documentazione ufficiale.**

**Argomenti:**
- Installazione di Scikit-Learn.
- Panoramica del framework e delle API principali.

**Attività:**
- Importa Scikit-Learn e prova un semplice modello (es. LinearRegression).
- Esegui un esempio end-to-end su un dataset piccolo (es. diabetes o iris).

### Giorno 2: Preprocessing dei Dati (Parte 1)

**Argomenti:**
- Funzioni di preprocessing: scaling, encoding, imputazione.
- Strumenti principali: StandardScaler, MinMaxScaler, OneHotEncoder, SimpleImputer.

**Attività:**
- Lavora su un dataset con valori mancanti e scale diverse (es. Titanic o House Prices).
- Implementa trasformazioni usando ColumnTransformer.

### Giorno 3: Preprocessing dei Dati (Parte 2)

**Argomenti:**
- Generazione di nuove feature: PolynomialFeatures.
- Selezione delle feature: SelectKBest, RFE.

**Attività:**
- Applica metodi di selezione e creazione di feature su un dataset tabellare.

### Giorno 4: Pipeline e Workflow

**Argomenti:**
- Automatizzare il preprocessing con Pipeline e FeatureUnion.
- Salvare e caricare pipeline con joblib.

**Attività:**
- Implementa una pipeline end-to-end su un dataset (preprocessing + modello).

### Giorno 5: Revisione

**Ripassa i concetti dei giorni 1-4.**

**Attività:**
- Completa un progetto di preprocessing su un dataset reale (es. House Prices).

## Giorni 6-10: Modelli Supervisionati

### Giorno 6: Regressione Lineare

**Argomenti:**
- Modelli lineari: LinearRegression, Ridge, Lasso.
- Valutazione con metodi di cross-validation.

**Attività:**
- Implementa un modello di regressione per predire i prezzi delle case.

### Giorno 7: Regressione Avanzata

**Argomenti:**
- Modelli non lineari: DecisionTreeRegressor, RandomForestRegressor.
- Valutazione con metriche: MSE, RMSE, R2.

**Attività:**
- Confronta i risultati di diversi modelli su un dataset tabellare.

### Giorno 8: Classificazione

**Argomenti:**
- Modelli di classificazione: LogisticRegression, KNeighborsClassifier.
- Matrice di confusione e ROC curve.

**Attività:**
- Implementa un classificatore per predire la sopravvivenza sul Titanic.

### Giorno 9: Classificazione Avanzata

**Argomenti:**
- Modelli avanzati: RandomForestClassifier, GradientBoostingClassifier.
- Valutazione con metriche: precision, recall, f1-score.

**Attività:**
- Confronta i risultati di modelli avanzati su un dataset tabellare.

### Giorno 10: Revisione

**Ripassa i concetti dei giorni 6-9.**

**Attività:**
- Completa un progetto di classificazione su un dataset reale (es. Iris).

## Giorni 11-15: Modelli Non Supervisionati

### Giorno 11: Clustering

**Argomenti:**
- Algoritmi di clustering: KMeans, DBSCAN.
- Valutazione con silhouette score.

**Attività:**
- Segmenta i clienti in gruppi usando un dataset di marketing.

### Giorno 12: Riduzione della Dimensionalità

**Argomenti:**
- PCA (Principal Component Analysis).
- Visualizzazione dei dati ridotti.

**Attività:**
- Applica PCA a un dataset con molte feature (es. Wine o Digits).

### Giorno 13: Modelli di Raggruppamento

**Argomenti:**
- Modelli di raggruppamento: AgglomerativeClustering.
- Dendrogrammi per analisi gerarchica.

**Attività:**
- Analizza la gerarchia dei cluster su un dataset.

### Giorno 14: Revisione Clustering e PCA

**Ripassa i concetti dei giorni 11-13.**

**Attività:**
- Completa un progetto di clustering e riduzione dimensionalità.

### Giorno 15: Revisione Generale

**Concludi con un progetto che combina clustering, riduzione dimensionalità e visualizzazione.**

## Giorni 16-20: Ottimizzazione e Tuning

### Giorno 16: Hyperparameter Tuning

**Argomenti:**
- Ricerca grid: GridSearchCV.
- Ricerca casuale: RandomizedSearchCV.

**Attività:**
- Ottimizza i parametri di un modello (es. Random Forest).

### Giorno 17: Validazione Avanzata

**Argomenti:**
- Tecniche di validazione: k-fold, stratified k-fold.
- Valutazione su set di test.

**Attività:**
- Implementa diverse tecniche di validazione.

### Giorno 18: Tuning Avanzato

**Argomenti:**
- Bayesian Optimization (introduzione).
- Analisi dell’impatto degli hyperparameter.

**Attività:**
- Usa Optuna o skopt per ottimizzazioni avanzate.

### Giorno 19: Revisione Hyperparameter Tuning

**Ripassa i concetti dei giorni 16-18.**

**Attività:**
- Completa un progetto di tuning su un dataset reale.

### Giorno 20: Revisione Generale

**Concludi con un progetto end-to-end su un dataset complesso.**

## Giorni 21-30: Progetti Pratici

**Dedica gli ultimi 10 giorni a:**
- Completare progetti su Kaggle o dataset reali.
- Combinare tutto ciò che hai imparato (preprocessing, modelli, tuning).
- Scrivere report dettagliati e documentare i tuoi risultati.

# Risultati Attesi

- Padronanza delle funzionalità principali di Scikit-Learn.
- Competenza nell’implementazione di pipeline e modelli per problemi reali.
- Portfolio con progetti pratici ben documentati.