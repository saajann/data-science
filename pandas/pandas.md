# Pandas 

Pandas è una libreria Python utilizzata per analizzare e lavorare con i dati.

## Concetti Chiave

- **Series**: Una Series è come una colonna di una tabella.
- **DataFrame**: Un DataFrame è l'intera tabella.

### Accesso ai Dati

Per ottenere una riga specifica:
```python
df.loc[n]  # Per indice
df.loc["day2"]  # Per etichetta
```

### Caricamento dei Dati

Puoi caricare file CSV (o JSON) in un DataFrame Pandas con il seguente codice:
```python
import pandas as pd
df = pd.read_csv("example.csv")
df = pd.read_json("example.json")
```

### Analisi dei Dati

Puoi visualizzare le prime righe di un DataFrame con il metodo `head()`:
```python
df.head()
```

Puoi visualizzare le ultime righe di un DataFrame con il metodo `tail()`:
```python
df.tail()
```

L'oggetto DataFrame ha un metodo chiamato `info()`, che ti dà maggiori informazioni sul set di dati.
```python
df.info()
```

## Pulizia dei Dati

La pulizia dei dati significa correggere i dati errati nel tuo set di dati.

I dati errati potrebbero essere:
- Celle vuote
- Dati nel formato sbagliato
- Dati errati
- Duplicati

### Pulizia celle vuote

#### Rimuovere Righe

Un modo per liberarsi delle celle vuote è eliminare direttamente tutte le righe che contengono celle vuote con il metodo `dropna()`
```python
cleaned = df.dropna()  # non modifica il DataFrame originale ma ritorna una nuova copia
df.dropna(inplace=True)  # modifica direttamente il DataFrame originale
```

#### Rimpiazzare valori nulli

Invece di perdere l'intera riga per una cella nulla, puoi riempire quella cella con un valore, con il metodo `fillna()`:
```python
df.fillna(130, inplace=True)  # riempie tutte le celle vuote del DataFrame
df['colonna1'].fillna(130, inplace=True)  # riempie tutte le celle vuote di una specifica colonna 
```

#### Rimpiazzare usando media, mediana o moda
- `mean()` ritorna la media
- `median()` ritorna il valore al centro una volta messi in ordine crescente i valori
- `mode()` ritorna il valore più frequente 

```python
x = df["colonna1"].mean()
x = df["colonna1"].median()
x = df["colonna1"].mode()[0]  # mode restituisce una Series con i valori più frequenti, dunque aggiungo '[0]' per prendere il primo elemento
df["colonna1"].fillna(x, inplace=True)
```

### Pulizia dati nel formato sbagliato

Hai due possibilità: o rimuovi direttamente la riga o converti la cella nel formato giusto

#### Conversione del formato
```python
df['Date'] = pd.to_datetime(df['Date'])  # in questo caso uso to_datetime ma dipende da che formato voglio
```

#### Rimuovere righe 
```python
df.dropna(subset=['colonna1'], inplace=True)  # rimuove le righe che hanno una cella vuota nella colonna specificata 
```

### Dati errati

#### Rimpiazzare manualmente la cella 
```python
df.loc[5, 'colonna1'] = 5
```

oppure posso semplicemente eliminare la riga 

```python
df.drop(5, inplace = True) # 5 è l'index della riga che voglio eliminare
```

### Dati duplicati
```python
df.drop_duplicates(inplace = True) # rimuovo le righe duplicate
```

## Correlazioni

Durante l'analisi del DataFrame possiamo usare il metodo `corr()` per vedere le correlazioni tra le varie colonne.
Il valore della correlazione tra una colonna e l'altra spazia tra -1 e 1:
- 1 significa correlazione perfetta: quando i valori della prima colonna aumentano, aumentano anche quelli della seconda.
- -1 significa correlazione perfetta ma al contrario: quando i valori della prima colonna aumentano, quelli della seconda diminuiscono.
- 0 significa che c'è bassa correlazione tra le due colonne. 
In generale, per avere una buona correlazione si deve avere un valore x < -0.6 oppure x > 0.6