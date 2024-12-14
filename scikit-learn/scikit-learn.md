# Guida Scikit-Learn

## 1. Preprocessing dei Dati

### Gestione dei dati mancanti
- **SimpleImputer**: riempie i valori mancanti.
    - Metodi: `.fit()`, `.transform()`, `.fit_transform()`.
- **KNNImputer**: imputa i valori mancanti usando k-nearest neighbors.

### Feature Scaling
- **StandardScaler**: standardizza i dati (media 0, deviazione standard 1).
- **MinMaxScaler**: normalizza i dati in un range specifico (es. [0,1]).
- **RobustScaler**: gestisce outlier.
    - Metodi: `.fit()`, `.transform()`, `.fit_transform()`.

### Encoding
- **LabelEncoder**: converte etichette categoriali in numeri.
- **OneHotEncoder**: trasforma feature categoriali in binarie.
    - Metodi: `.fit()`, `.transform()`.

### Custom Transformers
- Creare trasformazioni personalizzate (usando `TransformerMixin` e `BaseEstimator`).

## 2. Pipeline
- **Pipeline**: concatenazione di trasformazioni e modelli.
    - `Pipeline(steps=[('step_name', transformer_or_model)])`.
    - Metodi: `.fit()`, `.predict()`, `.score()`.
- **FeatureUnion**: combina trasformazioni parallele.
    - `FeatureUnion([('name1', transformer1), ('name2', transformer2)])`.

## 3. Modelli Supervisionati

### Regressione
- **LinearRegression**: regressione lineare semplice.
- **Ridge/Lasso**: regressione lineare con regolarizzazione.
- **DecisionTreeRegressor**: albero decisionale per regressione.
    - Metodi: `.fit()`, `.predict()`, `.score()`.

### Classificazione
- **LogisticRegression**: classificazione logistica.
- **KNeighborsClassifier**: k-nearest neighbors.
- **DecisionTreeClassifier**: albero decisionale per classificazione.
- **RandomForestClassifier**: ensemble di alberi decisionali.
- **SVC (Support Vector Classifier)**: classificatore a margine massimo.
    - Metodi: `.fit()`, `.predict()`, `.predict_proba()`, `.score()`.

## 4. Modelli Non Supervisionati

### Clustering
- **KMeans**: clustering non supervisionato.
- **DBSCAN**: clustering basato sulla densità.
    - Metodi: `.fit()`, `.predict()`, `.fit_predict()`.

### Riduzione della dimensionalità
- **PCA (Principal Component Analysis)**: riduzione delle dimensioni.
    - Metodi: `.fit()`, `.transform()`, `.explained_variance_ratio_()`.

## 5. Model Selection e Valutazione

### Train-Test Split
- **train_test_split**: divide i dati in training e test.
    - Metodi: Non richiede metodi (ritorna i dati divisi).

### Metriche
- Regressione: `mean_squared_error`, `r2_score`.
- Classificazione: `accuracy_score`, `confusion_matrix`, `classification_report`.

### Cross-Validation
- **cross_val_score**: valuta un modello con cross-validation.
- **GridSearchCV/RandomizedSearchCV**: ricerca degli iperparametri.

## 6. Ensemble Methods

### Bagging
- **RandomForestClassifier/Regressor**: forest di alberi decisionali.

### Boosting
- **GradientBoostingClassifier/Regressor**: boosting sui residui.
- **AdaBoostClassifier**: adattativo.

## 7. Salvare Modelli

### Joblib
- **dump**: salva un modello.
- **load**: carica un modello.
