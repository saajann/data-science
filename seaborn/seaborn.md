# Seaborn

È una libreria python usata per la data visualization che può essere considerata una estensione di Matplotlib: possiamo fare grafici complessi che prima richiedevano più righe di codice in una sola riga. Inoltre proprio come Matplotlib, Seaborn è facilmente integrabile con Pandas.


## Distribution plots
Grafici adatti a feature NUMERICHE

### Distribution plot
Mostra la distribuzione di una variabile numerica
sns.displot(df['colonna1'])

### Joint plot
Compara due distribuzioni e traccia uno scatter plot
sns.jointplot(data=df, x='colonna1', y='colonna2')

### KDE plot
sns.kdeplot(df['colonna1'])

### Pair plot
Plotta le relazioni tra tutte le feature numeriche del DataFrame
sns.pairplot(df)

### Rug plots
-

## Categorical plots
Grafici adatti a feature CATEGORICHE

### Bar plot
Metto in relazione la distribuzione di una feature categorica a una feature numerica
sns.barplot(data=df, x='sex', y='total_bill')

### Count plot
Come un barplot ma sulle ordinate ho la conta
sns.countplot(data=df, x='sex)

### Box plot
Permette di comparare variabili diverse e mostra informazioni extra come la mediana, da deviazione standard, eccetera
'hue' permette di mostrare una terza variabile (categorica e distinguibile attraverso il colore)
sns.boxplot(data=df, x='day', y='total_bill', hue='sex')

### Violin plot
da capire meglio
sns.violinplot(x='day',y='total_bill',data=tips_df, hue='sex',split=True)

### Strip plot
irrilevante

### Swarm plot 
irrilevante

## Matrix plots

### Heatmap
Mostra le correlazioni tra le variabili in modo visivo
sns.heatmap(df.corr())

### Cluster map
-

### Pair Grid
Più scatter plot messi insieme 

### Facet Grid
-

## Regression plots
-


# Priorità per EDA (Esplorazione dei Dati):
- Distribuzione: displot, pairplot, kdeplot.
- Relazioni: scatterplot, regplot, lmplot.
- Categorie: barplot, boxplot, countplot.
- Correlazioni: heatmap.