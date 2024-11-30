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
Imposta il tipo di marker nei grafici.
```python
plt.plot(x, y, marker='o')
```

### ms (markersize)
Imposta la dimensione dei marker.
```python
plt.plot(x, y, marker='o', ms=10)
```

### mec (markeredgecolor)
Imposta il colore del bordo dei marker.
```python
plt.plot(x, y, marker='o', mec='r')
```

### mfc (markerfacecolor)
Imposta il colore interno dei marker.
```python
plt.plot(x, y, marker='o', mfc='b')
```

### linestyle
Imposta lo stile della linea.
```python
plt.plot(x, y, linestyle='--')
```

### color
Imposta il colore della linea.
```python
plt.plot(x, y, color='g')
```

### linewidth
Imposta lo spessore della linea.
```python
plt.plot(x, y, linewidth=2)
```

### multiple lines (two plots)
Tracciare più linee in un singolo grafico.
```python
plt.plot(x1, y1, label='Line 1')
plt.plot(x2, y2, label='Line 2')
plt.legend()
```

### xlabel
Imposta l'etichetta dell'asse x.
```python
plt.xlabel('X Axis Label')
```

### ylabel
Imposta l'etichetta dell'asse y.
```python
plt.ylabel('Y Axis Label')
```

### title
Imposta il titolo del grafico.
```python
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
```

#### title
Imposta il titolo del subplot.
```python
plt.subplot(2, 1, 1)
plt.plot(x, y)
plt.title('Subplot Title')
```

#### subtitle
Imposta il sottotitolo del subplot.
```python
plt.suptitle('Main Title')
```

### scatter plot
Crea un grafico a dispersione.
```python
plt.scatter(x, y)
```

#### colors
Imposta i colori dei punti.
```python
plt.scatter(x, y, c='r')
```

#### cmap
Imposta una mappa di colori.
```python
plt.scatter(x, y, c=z, cmap='viridis')
```

#### colorbar
Aggiunge una barra dei colori.
```python
plt.colorbar()
```

#### size
Imposta la dimensione dei punti.
```python
plt.scatter(x, y, s=100)
```

#### alpha
Imposta la trasparenza dei punti.
```python
plt.scatter(x, y, alpha=0.5)
```

### bar plots
Crea un grafico a barre.
```python
plt.bar(x, height)
```

### barh
Crea un grafico a barre orizzontali.
```python
plt.barh(x, width)
```

#### color
Imposta il colore delle barre.
```python
plt.bar(x, height, color='b')
```

#### width
Imposta la larghezza delle barre.
```python
plt.bar(x, height, width=0.5)
```

#### height
Imposta l'altezza delle barre.
```python
plt.barh(x, height)
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