# Supervised Learning Algorithms

1. **Linear Regression**
   - **Regressor**
   - [Video YouTube spiegazione](https://youtu.be/CtsRRUddV2s?si=ufTa0_heV82pWy5G)
```python
from sklearn.linear_model import LinearRegression
```

2. **Logistic Regression**
   - **Classifier**
   - Per una classificazione binaria, modello adatto se hai poche feature
   - [Video YouTube spiegazione](https://youtu.be/yIYKR4sgzI8?si=5hBf0Q403QVrUFq9)
```python
from sklearn.linear_model import LogisticRegression
```

3. **k-Nearest Neighbors (k-NN)**
   - **Classifier** (può essere usato anche come Regressor)
   - Per problemi di classificazione e regressione basati sulla prossimità
   - [Video Youtube spiegazione](https://youtu.be/HVXime0nQeI?si=91PhjpdGTl0c4S7H)
```python
from sklearn.neighbors import KNeighborsClassifier
from sklearn.neighbors import KNeighborsRegressor
```

4. **Decision Trees**
   - **Classifier** (può essere usato anche come Regressor)
   - Classification Tree / Regression Tree
   - Adatto a dataset con poche feature, rischio di overfitting
   - [Video Youtube spiegazione](https://youtu.be/JcI5E2Ng6r4?si=StBDYKgwCNZYBZfY)
```python
from sklearn.tree import DecisionTreeClassifier
from sklearn.tree import DecisionTreeRegressor
```

5. **Random Forest**
   - **Classifier** (può essere usato anche come Regressor)
   - Un insieme di Decision Trees.
   - [Video Youtube spiegazione](https://youtu.be/v6VJ2RO66Ag?feature=shared)
```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.ensemble import RandomForestRegressor
```

6. **Support Vector Machines (SVM)**
   - **Classifier** (può essere usato anche come Regressor)
   - Adatti a dataset piccoli ma con tante feature
   - Adatti a classificazione binaria 
   - [Video Youtube spiegazione](https://youtu.be/_YPScrckx28?si=g28PpybyZrDoZEhs)
```python
from sklearn.svm import SVC
from sklearn.svm import SVR
```

7. **Naive Bayes**
   - **Classifier**
```python
from sklearn.naive_bayes import GaussianNB
```

8. **Gradient Boosting (e.g., XGBoost)**
   - **Classifier** (possono essere usati anche come Regressor)
   - Capacità di catturare relazioni non lineari
   - Adatto per dati strutturati

---

# Unsupervised Learning Algorithms

1. **k-Means Clustering**
   - **Unsupervised**
   - Data partitioning into clusters.
   - Concepts: centroids, optimizing \(k\).

2. **Principal Component Analysis (PCA)**
   - **Unsupervised**
   - Dimensionality reduction.
   - Concepts: eigenvalues, eigenvectors.

3. **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**
   - **Unsupervised**
   - Density-based clustering.
   - Concepts: eps (radius), minPts (minimum points).

4. **Hierarchical Clustering**
   - **Unsupervised**
   - Building a hierarchy of clusters.
   - Concepts: dendrogram, linkage methods.