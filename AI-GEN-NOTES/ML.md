# Machine Learning

## 1. Classification
### Definition
**Classification** is a supervised learning approach where the goal is to predict the categorical class labels of new instances based on past observations.

### Types of Classification
- **Binary Classification**: Two possible classes (e.g., spam or not spam).
- **Multiclass Classification**: More than two classes (e.g., types of animals).

### Common Algorithms
- **Logistic Regression**
- **k-Nearest Neighbors (k-NN)**
- **Decision Trees**
- **Support Vector Machines (SVM)**
- **Neural Networks**

### Example
```python
from sklearn.linear_model import LogisticRegression
model = LogisticRegression()
model.fit(X_train, y_train)
predictions = model.predict(X_test)
```

---

## 2. Decision Tree Learning
### Definition
**Decision Tree Learning** is a non-parametric supervised learning method used for classification and regression.

### Key Concepts
- **Root Node**: Represents the entire dataset.
- **Internal Nodes**: Represent features.
- **Branches**: Represent decision rules.
- **Leaf Nodes**: Represent outcomes (class labels).

### Splitting Criteria
- **Gini Index**
- **Entropy**
- **Information Gain**

### Example
```python
from sklearn.tree import DecisionTreeClassifier
model = DecisionTreeClassifier()
model.fit(X_train, y_train)
predictions = model.predict(X_test)
```

### Advantages and Disadvantages
- **Advantages**: Easy to understand, interpret, and visualize.
- **Disadvantages**: Prone to overfitting, can create complex trees that do not generalize well.

---

## 3. Artificial Neural Networks (ANN)
### Definition
**Artificial Neural Networks** are computational models inspired by the human brain, composed of interconnected units (neurons).

### Structure
- **Input Layer**: Receives the input features.
- **Hidden Layers**: Perform computations and feature transformations.
- **Output Layer**: Produces the final prediction.

### Activation Functions
- **Sigmoid**
- **ReLU (Rectified Linear Unit)**
- **Tanh**

### Example
```python
from keras.models import Sequential
from keras.layers import Dense

model = Sequential()
model.add(Dense(12, input_dim=8, activation='relu'))
model.add(Dense(8, activation='relu'))
model.add(Dense(1, activation='sigmoid'))

model.compile(loss='binary_crossentropy', optimizer='adam', metrics=['accuracy'])
model.fit(X_train, y_train, epochs=150, batch_size=10)
```

### Advantages and Disadvantages
- **Advantages**: Can model complex patterns, highly flexible.
- **Disadvantages**: Requires a lot of data and computational power, can be difficult to interpret.

---

## 4. Support Vector Machines (SVM)
### Definition
**Support Vector Machines** are supervised learning models that analyze data for classification and regression analysis.

### Key Concepts
- **Hyperplane**: A decision boundary that separates different classes.
- **Support Vectors**: Data points that are closest to the hyperplane.
- **Margin**: The distance between the hyperplane and the nearest support vectors.

### Kernel Functions
- **Linear Kernel**
- **Polynomial Kernel**
- **Radial Basis Function (RBF) Kernel**

### Example
```python
from sklearn.svm import SVC
model = SVC(kernel='linear')
model.fit(X_train, y_train)
predictions = model.predict(X_test)
```

### Advantages and Disadvantages
- **Advantages**: Effective in high-dimensional spaces, robust to overfitting.
- **Disadvantages**: Computationally intensive, less effective on large datasets with noise.

---

## 5. Bayesian Learning
### Definition
**Bayesian Learning** involves applying Bayes' theorem for probabilistic inference.

### Key Concepts
- **Bayes' Theorem**: `P(A|B) = (P(B|A) * P(A)) / P(B)`
- **Prior Probability (P(A))**: Initial probability of an event.
- **Posterior Probability (P(A|B))**: Updated probability after considering new evidence.

### Naive Bayes Classifier
Assumes independence between predictors.
```python
from sklearn.naive_bayes import GaussianNB
model = GaussianNB()
model.fit(X_train, y_train)
predictions = model.predict(X_test)
```

### Advantages and Disadvantages
- **Advantages**: Simple, fast, works well with high-dimensional data.
- **Disadvantages**: Assumes independence between features, which is rarely true in real life.

---

## 6. Clustering
### Definition
**Clustering** is an unsupervised learning technique that groups data points into clusters based on similarity.

### Types of Clustering
- **K-Means Clustering**: Partitions data into k clusters.
- **Hierarchical Clustering**: Builds a hierarchy of clusters.
- **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**: Forms clusters based on density.

### K-Means Clustering Example
```python
from sklearn.cluster import KMeans
model = KMeans(n_clusters=3)
model.fit(X)
labels = model.predict(X)
```

### Advantages and Disadvantages
- **Advantages**: Simple, easy to implement, efficient.
- **Disadvantages**: Requires the number of clusters to be specified, sensitive to initial seed.

---

## 7. Hidden Markov Models (HMM)
### Definition
**Hidden Markov Models** are statistical models that represent systems with Markov processes having hidden states.

### Key Concepts
- **States**: Hidden conditions of the system.
- **Observations**: Visible outcomes linked to hidden states.
- **Transition Probabilities**: Probability of transitioning from one state to another.
- **Emission Probabilities**: Probability of an observation being generated from a state.

### Example
```python
import numpy as np
from hmmlearn import hmm

model = hmm.GaussianHMM(n_components=3)
model.fit(X)
hidden_states = model.predict(X)
```

### Applications
- **Speech Recognition**
- **Bioinformatics**
- **Financial Modeling**

### Advantages and Disadvantages
- **Advantages**: Efficient for time-series data, handles sequences of varying lengths.
- **Disadvantages**: Requires large amounts of data, complex to implement and interpret.
