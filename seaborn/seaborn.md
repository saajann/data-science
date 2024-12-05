# Seaborn
È una libreria Python usata per la data visualization che può essere considerata una estensione di Matplotlib: possiamo fare grafici complessi che prima richiedevano più righe di codice in una sola riga. Inoltre, proprio come Matplotlib, Seaborn è facilmente integrabile con Pandas.

## Distribution plots
Grafici adatti a feature **numeriche**

### Distribution plot
Mostra la distribuzione di una variabile numerica:
```python
sns.displot(df['colonna1'])
```

### Joint plot
Compara due distribuzioni e traccia uno scatter plot:
```python
sns.jointplot(data=df, x='colonna1', y='colonna2')
```

### KDE plot
Mostra la stima della densità del kernel:
```python
sns.kdeplot(df['colonna1'])
```

### Pair plot
Plotta le relazioni tra tutte le feature numeriche del DataFrame:
```python
sns.pairplot(df)
```

## Categorical plots
Grafici adatti a feature **categoriche**

### Bar plot
Mette in relazione la distribuzione di una feature categorica a una feature numerica:
```python
sns.barplot(data=df, x='sex', y='total_bill')
```

### Count plot
Come un bar plot ma sulle ordinate ho la conta:
```python
sns.countplot(data=df, x='sex')
```

### Box plot
Permette di comparare variabili diverse e mostra informazioni extra come la mediana, la deviazione standard, eccetera. 'hue' permette di mostrare una terza variabile (categorica e distinguibile attraverso il colore):
```python
sns.boxplot(data=df, x='day', y='total_bill', hue='sex')
```

## Matrix plots

### Heatmap
Mostra le correlazioni tra le variabili in modo visivo:
```python
sns.heatmap(df.corr(), annot=True)
```

## Relational plots
Grafici che mostrano relazioni tra variabili

### Scatter plot
Mostra la relazione tra due variabili numeriche:
```python
sns.scatterplot(data=df, x='colonna1', y='colonna2')
```

### Line plot
Mostra la relazione tra due variabili numeriche con una linea:
```python
sns.lineplot(data=df, x='colonna1', y='colonna2')
```