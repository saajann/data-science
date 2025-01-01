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
   - **Classifier** (can also be used as a regressor)
   - Iterative splitting of data.
   - Concepts: Gini impurity, entropy.

5. **Random Forest**
   - **Classifier** (can also be used as a regressor)
   - An ensemble of decision trees.
   - Concepts: bagging, out-of-bag error.

6. **Support Vector Machines (SVM)**
   - **Classifier** (can also be used as a regressor)
   - Classification by maximizing margins.
   - Concepts: kernel trick, margin maximization.

7. **Gradient Boosting (e.g., XGBoost, LightGBM)**
   - **Classifier** (can also be used as a regressor)
   - Powerful algorithms for classification/regression.
   - Concepts: boosting, overfitting control.

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