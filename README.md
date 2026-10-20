# Energy State Classification with K-Means

# 

# This project uses K-Means clustering to group household power readings into three energy states: standby, normal use, and heavy load. It is an unsupervised learning project, so the model is never given labels and has to find the groups on its own. I built it to understand how unsupervised learning works in practice.

# 

# The dataset is simulated: 14 days of hourly readings (336 rows) with active power, voltage, and current. Each day follows a realistic cycle of standby at night, normal use during the day, and heavy load in the evening, with random noise added so the states overlap slightly.

# 

# The three features are standardized with StandardScaler, because K-Means depends on distances and voltage (around 230) would otherwise overwhelm power (around 0.2 to 5). A KMeans model with three clusters is then trained and each reading is assigned an energy state. The silhouette score is about 0.57, which shows the clusters are reasonably well separated. Cluster averages confirm the states: about 0.34 kW for standby, 1.56 kW for normal use, and 4.30 kW for heavy load. Cluster numbers are arbitrary, so the names come from interpreting these averages.

# 

# To run it, install the libraries with pip install numpy pandas matplotlib scikit-learn joblib jupyter, open unsupervised\_k\_means\_model.ipynb, and run the cells in order. The trained model and scaler are saved with joblib and must be used together, so new readings are always scaled with the same scaler used in training.

# 

# Built with Python, NumPy, Pandas, Matplotlib, scikit-learn, and Joblib.

