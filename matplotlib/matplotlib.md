# Matplotlib
Che cos'è matplotlib? È una libreria python open-source per fare grafici semplici, utili per la data visualization. 

## Importazione 
Per poter usare matplotlib con pandas, importo il modulo pyplot:
```python
import matplotlib.pyplot as plt
df.plot()
plt.show()
```

## plot()
### marker
Imposta il tipo, la dimensione, il colore del bordo e il colore interno dei marker nei grafici.
```python
plt.plot(x, y, marker='o', ms=10, mec='r', mfc='b')
```

### linestyle e color
Imposta lo stile, il colore e lo spessore della linea.
```python
plt.plot(x, y, linestyle='--', color='g', linewidth=2)
```

### multiple lines (two plots)
Tracciare più linee in un singolo grafico.
```python
plt.plot(x1, y1, label='Line 1')
plt.plot(x2, y2, label='Line 2')
plt.legend()
```

### xlabel, ylabel e title
Imposta l'etichetta degli assi e il titolo del grafico.
```python
plt.xlabel('X Axis Label')
plt.ylabel('Y Axis Label')
plt.title('Title of the Plot')
```

### grid
Aggiunge una griglia al grafico.
```python
plt.grid(True)
```

### subplot
Crea più subplot in una singola figura.
```python
plt.subplot(2, 1, 1)
plt.plot(x, y)
plt.title('Subplot 1')

plt.subplot(2, 1, 2)
plt.plot(x, y)
plt.title('Subplot 2')
plt.suptitle('Main Title')
```

### scatter plot
Crea un grafico a dispersione con colori, mappa di colori, barra dei colori, dimensione e trasparenza dei punti.
```python
plt.scatter(x, y, c=z, cmap='viridis', s=100, alpha=0.5)
plt.colorbar()
```

### bar plots
Crea un grafico a barre verticali o orizzontali con colore, larghezza e altezza delle barre.
```python
plt.bar(x, height, color='b', width=0.5)
plt.barh(x, width, color='b', height=0.5)
```

### histogram
Crea un istogramma.
```python
plt.hist(data)
```

### piechart
Crea un grafico a torta.
```python
plt.pie(sizes, labels=labels)
```