# Feature Engineering
L'obiettivo della feature engineering è rendere i dati più utili per il modello di machine learning, creando, trasformando e selezionando le colonne più importanti.

## Principali tecniche

### 1. Creazione di nuove feature
Combinare, trasformare o aggregare le variabili esistenti per creare nuove informazioni utili per il modello.
```python
df['BMI'] = df['weight'] / (df['height'] ** 2)
```

### 2. Trasformazioni logiche
Applicare trasformazioni matematiche per rendere le feature più utili. Ad esempio, per gestire gli outlier, si può applicare una trasformazione logaritmica.
```python
df['log_feature'] = np.log(df['feature'] + 1)
```

### 3. Binning
Raggruppare valori continui in intervalli o categorie.
```python
df['age_group'] = pd.cut(df['age'], bins=[0, 18, 40, 100], labels=['Young', 'Adult', 'Senior'])
```

### 4. Creazione di variabili categoriali

#### One-Hot Encoding
Creare una colonna per ogni categoria possibile, con valori 0 o 1. Adatto per variabili senza ordine, come "sesso" o "paese".
```python
df = pd.get_dummies(df, columns=['gender', 'country'])
```

#### Label Encoding
Assegnare un numero intero a ciascuna categoria. Utile per variabili con un ordine implicito, come "basso", "medio", "alto".
```python
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
df['income_level'] = le.fit_transform(df['income_level'])
```

### 5. Feature Selection
Identificare e rimuovere le feature meno rilevanti quando si hanno troppe feature.

#### Correlazione
Rimuovere le feature fortemente correlate tra loro per ridurre la ridondanza. Se due variabili hanno una correlazione molto alta (ad esempio, > 0.9), considerare di rimuoverne una.
```python
corr_matrix = df.corr()
```

#### Metodi automatici di selezione
Utilizzare strumenti come SelectKBest di scikit-learn per selezionare le migliori feature in base a un punteggio statistico.s
```python
from sklearn.feature_selection import SelectKBest, f_classif
selector = SelectKBest(f_classif, k=5)  # Seleziona le 5 migliori feature
df_selected = selector.fit_transform(df.drop('target', axis=1), df['target'])
```