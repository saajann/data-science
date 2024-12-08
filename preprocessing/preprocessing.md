# Pulizia dei dati

## Gestione dei Valori Mancanti

### Imputazione
Sostituisci i valori mancanti con la media, la mediana o la moda.

```python
import pandas as pd
from sklearn.impute import SimpleImputer

# DataFrame di esempio
df = pd.DataFrame({'A': [1, 2, None, 4], 'B': [None, 2, 3, 4]})

# Imputer per la media
imputer = SimpleImputer(strategy='mean')
df_imputed = pd.DataFrame(imputer.fit_transform(df), columns=df.columns)
print(df_imputed)
```

### Rimozione
Rimuovi righe o colonne con valori mancanti.

```python
# Rimuovi righe con valori mancanti
df_dropped_rows = df.dropna()
print(df_dropped_rows)

# Rimuovi colonne con valori mancanti
df_dropped_columns = df.dropna(axis=1)
print(df_dropped_columns)
```

## Rimozione dei Duplicati
Identifica e rimuovi righe duplicate nel dataset.

```python
# DataFrame di esempio con duplicati
df = pd.DataFrame({'A': [1, 2, 2, 4], 'B': [1, 2, 2, 4]})

# Rimuovi duplicati
df_no_duplicates = df.drop_duplicates()
print(df_no_duplicates)
```

## Correzione degli Errori nei Dati
Correggi valori fuori scala o errati.

```python
# DataFrame di esempio con valori errati
df = pd.DataFrame({'A': [1, 2, -999, 4], 'B': [1, 2, 3, 4000]})

# Sostituisci valori errati
df_corrected = df.replace([-999, 4000], [None, None])
print(df_corrected)
```

# Gestione delle Variabili Categoriali

## One-Hot Encoding
Usa per variabili nominali senza ordine.

```python
# DataFrame di esempio con variabile categoriale
df = pd.DataFrame({'Categoria': ['A', 'B', 'A', 'C']})

# One-Hot Encoding
df_encoded = pd.get_dummies(df, columns=['Categoria'])
print(df_encoded)
```

## Label Encoding
Usa per variabili ordinali con ordine.

```python
from sklearn.preprocessing import LabelEncoder

# DataFrame di esempio con variabile ordinale
df = pd.DataFrame({'Variabile': ['Basso', 'Medio', 'Alto', 'Medio']})

# Label Encoding
label_encoder = LabelEncoder()
df['Variabile_Encoded'] = label_encoder.fit_transform(df['Variabile'])
print(df)
```

# Gestione delle Variabili Numeriche

## Scaling/Normalizzazione

### Standardizzazione (Z-score)
Trasforma i dati per avere media 0 e deviazione standard 1.
Utilizza quando i dati seguono una distribuzione normale o quando l'algoritmo è sensibile alla distanza tra i punti (come SVM, KNN, regressione lineare). È meno sensibile agli outlier rispetto alla normalizzazione.

```python
from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()
df_standardized = pd.DataFrame(scaler.fit_transform(df), columns=df.columns)
df = scaler.fit_transform(df)
print(df_standardized)
```

### Normalizzazione (Min-Max)
Scala i dati a un intervallo specifico (ad es., 0-1).
Utilizza quando vuoi ridurre i dati a un intervallo specifico (di solito [0, 1]). È preferibile quando usi algoritmi come le reti neurali o quando hai variabili con un intervallo definito. Tuttavia, fai attenzione agli outlier.

```python
from sklearn.preprocessing import MinMaxScaler

# Normalizzazione
scaler = MinMaxScaler()
df_normalized = pd.DataFrame(scaler.fit_transform(df), columns=df.columns)
print(df_normalized)
```

## Gestione degli Outlier

### Trimming
Rimuovi gli outlier.

```python
# DataFrame di esempio
df = pd.DataFrame({'A': [1, 2, 3, 100], 'B': [2, 3, 4, 200]})

# Rimuovi outlier
df_trimmed = df[(df['A'] < 10) & (df['B'] < 10)]
print(df_trimmed)
```

### Winsorizzazione
Limita gli outlier a un valore massimo/minimo.

```python
import numpy as np

# Winsorizzazione
df_winsorized = df.copy()
df_winsorized['A'] = np.where(df['A'] > 10, 10, df['A'])
df_winsorized['B'] = np.where(df['B'] > 10, 10, df['B'])
print(df_winsorized)
```

# Gestione delle Variabili Temporali (se presenti)
Estrai caratteristiche temporali come anno, mese, giorno della settimana, ecc.

```python
# DataFrame di esempio con datetime
df = pd.DataFrame({'Data': pd.to_datetime(['2021-01-01', '2021-02-01', '2021-03-01'])})

# Estrai caratteristiche temporali
df['Anno'] = df['Data'].dt.year
df['Mese'] = df['Data'].dt.month
df['GiornoDellaSettimana'] = df['Data'].dt.dayofweek
print(df)
```

