# Analisi Esplorativa dei Dati (EDA)

1. **Importazione del Dataset**
    - Utilizza `pandas.read_csv()` o altri metodi di caricamento per importare il dataset.

2. **Ispezione Iniziale dei Dati**
    - Usa `.head()` per visualizzare le prime righe del dataset.
    - Usa `.info()` per controllare il tipo di dati e la presenza di valori mancanti.
    - Usa `.describe()` per ottenere una panoramica statistica delle colonne numeriche.

3. **Gestione dei Valori Mancanti**
    - Identifica le colonne con valori mancanti.
    - Decidi se rimuovere o imputare i valori mancanti (con media, mediana, moda).

4. **Esplorazione delle Variabili Categoriali**
    - Usa `.value_counts()` per visualizzare la distribuzione delle variabili categoriali (es. sesso, classe).
    - Considera di visualizzare queste distribuzioni con un grafico a barre.

5. **Analisi delle Correlazioni**
    - Usa `.corr()` per vedere la correlazione tra le variabili numeriche.
    - Crea una heatmap delle correlazioni per una visualizzazione più chiara.

6. **Esplorazione delle Variabili Numeriche**
    - Analizza la distribuzione delle variabili numeriche (es. età, tariffa) tramite istogrammi o boxplot.
    - Controlla la presenza di outliers.

7. **Analisi Bivariata**
    - Esplora la relazione tra variabili (es. relazione tra classe e sopravvivenza).
    - Usa scatter plot per variabili numeriche e grafici a barre per variabili categoriali.

8. **Visualizzazioni Generali**
    - Utilizza grafici di distribuzione (istogrammi, boxplot) per avere una visione complessiva dei dati.
    - Usa pairplot o violin plot per esaminare le relazioni tra variabili numeriche e categoriali.

9. **Feature Engineering**
    - Crea nuove caratteristiche, se necessario, come l'estrazione di informazioni da variabili esistenti (es. titolo da nome).
    - Codifica le variabili categoriali (es. con encoding).

10. **Rimozione o Trattamento degli Outliers**
     - Analizza se ci sono outliers significativi e valuta se rimuoverli o trattarli.
