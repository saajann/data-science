# Seaborn

È una libreria python usata per la data visualization che può essere considerata una estensione di Matplotlib: possiamo fare grafici complessi che prima richiedevano più righe di codice in una sola riga. Inoltre proprio come Matplotlib, Seaborn è facilmente integrabile con Pandas.


## Distribution plots
Grafici adatti a feature NUMERICHE

### Distribution plot
Mostra la distribuzione di una variabile numerica
sns.displot(df['colonna1'])
.histplot()

### Joint plot
Compara due distribuzioni e traccia uno scatter plot
sns.jointplot(data=df, x='colonna1', y='colonna2')

### KDE plot
sns.kdeplot(df['colonna1'])

### Pair plots
Plotta le relazioni tra tutte le feature numeriche del DataFrame
sns.pairplot(df)

### Rug plots
mi sembra inutile

## Categorical plots
Grafici adatti a feature CATEGORICHE

### Bar plot
Metto in relazione la distribuzione di una feature categorica a una feature numerica
sns.barplot(data=df, x='sex', y='total_bill')

### Count plot
Come un barplot ma sulle ordinate ho la conta
sns.countplot(data=df, x='sex)

### Box plot

### Violin plot

### Strip plot

### Swarm plot 

### Palettes


## Matrix plots

### Heatmaps

### Cluster map

### Pair Grid

### Facet Grid


## Regression plots