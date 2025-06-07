# 🧠Problem Statement:  

The goal of this project is to build a binary classification model that can distinguish between normal and abnormal vertebral column conditions using six biomechanical features extracted from medical imaging data. This is achieved using the K-Nearest Neighbors (KNN) algorithm with various distance metrics and voting strategies. The classifier aims to assist in preliminary medical diagnoses based on non-invasive biomechanical measurements.

# 📂 Dataset:
**Source:** Vertebral Column Data Set from https://archive.ics.uci.edu/ml/datasets/Vertebral+Column.  

**Attributes:** Pelvic incidence, Pelvic tilt, Lumbar lordosis angle, Sacral slope, Pelvic radius, Degree of spondylolisthesis.    

**Labels:** Class 0 -> Normal (NO), Class 1 -> Abnormal (AB), includes Disk Hernia (DH) and Spondylolisthesis (SL).  

# 🔍 Project Highlights:
**Exploratory Data Analysis:** Scatter plots and boxplots to visualize feature distributions by class.  

**Train/Test Split:** 70 samples from Class 0 and 140 from Class 1 for training; remainder used for testing.  

**KNN Implementation:** Evaluation with various k values using confusion matrix, precision, recall, F1-score.  

**Learning Curves:** Studied generalization vs training size.  

**Distance Metric Comparisons:** Euclidean, Manhattan (Minkowski with p=1), Chebyshev, Mahalanobis.  

**Weighted KNN:** Implemented inverse-distance weighted voting.  

# 🔍 Key Results and Insights
**1) Optimal k Selection (Euclidean Distance):**  

🔥 Best performing k = 4  

**Confusion Matrix & Metrics (k = 4):**  

✅ True Positive Rate (Recall): 0.9857  
✅ True Negative Rate: 0.8333  
✅ Precision: 0.9324  
✅ F1 Score: 0.9583  

**2. Performance Across Distance Metrics (Unweighted KNN) with different values of k**  

Minkowski with log-scaled p provides flexible control and performed best in this dataset with **test error of 0.06** at optimal **k-value = 1**  

**3. Weighted KNN Results**  

Euclidean performed best with **test error of 0.10** at optimal **k-value = 6**  

Weighted KNN stabilizes performance across high k values but doesn’t outperform the best unweighted setup.  

# Learning curve  


