Detecting network intrusion using various machine learning algorithms. Monitor a network or system for malicious activity and protects a computer network from unauthorized access from users, including perhaps insider. The intrusion detector learning task is to build a predictive model (i.e. a classifier) capable of distinguishing between ‘bad connections’ (intrusion/attacks) and a ‘good (normal) connections’.

data set:

The dataset to be audited was provided which consists of a wide variety of intrusions simulated in a military network environment. It created an environment to acquire raw TCP/IP dump data for a network by simulating a typical US Air Force LAN. The LAN was focused like a real environment and blasted with multiple attacks. A connection is a sequence of TCP packets starting and ending at some time duration between which data flows to and from a source IP address to a target IP address under some well-defined protocol. Also, each connection is labelled as either normal or as an attack with exactly one specific attack type. Each connection record consists of about 100 bytes.
For each TCP/IP connection, 41 quantitative and qualitative features are obtained from normal and attack data (3 qualitative and 38 quantitative features) .The class variable has two categories:
• Normal
• Anomalous

the dataset in question:
(https://github.com/yousef4real/intrusion-detection-system-implemented-with-machine-learning-/files/14847214/archive.zip) [archive.zip] 


code documentation (algorithms and functionality):

Data Preparation:

The code starts with importing necessary libraries for data manipulation, visualization, and model building.
It loads training and testing data from CSV files stored in Google Drive.
Exploratory Data Analysis (EDA):

Summary statistics and information about the training dataset are displayed using info() and describe() functions.
Missing values and duplicate rows are checked and found to be absent.
Data Preprocessing:

Categorical variables in the dataset are encoded using label encoding.
The num_outbound_cmds column, which contains only zeros, is removed from both the training and testing datasets.
Selected features are scaled using StandardScaler.
Model Training and Evaluation:

The code includes the following classification models:
Logistic Regression
K-Nearest Neighbors (KNN)
Decision Tree
For each model, training and testing times are measured, and training and testing accuracy scores are computed.
Hyperparameter Optimization:

Optuna library is used for hyperparameter optimization for KNN and Decision Tree models.
Optuna's Bayesian optimization algorithm is utilized to search for the best hyperparameters.
The best hyperparameters and corresponding accuracy scores are printed for each model.
Cross-Validation:

Cross-validation is performed for each model using precision and recall as evaluation metrics.
Mean precision and recall scores, along with their standard deviations, are displayed for each model.
Model Evaluation:

Confusion matrices, classification reports, and F1 scores are calculated for each model on the testing dataset.
The performance metrics provide insights into the model's ability to correctly classify normal and anomaly instances.
Visualization:

Bar plots are generated to visualize the mean precision and recall scores for each model.
Functionality:

The code performs the following tasks:
Data loading, preprocessing, and feature engineering.
Model training, hyperparameter optimization, and evaluation.
Cross-validation and performance analysis.
It provides insights into the effectiveness of different classification algorithms for intrusion detection.
Novelty:

The code demonstrates the application of machine learning techniques, including data preprocessing, model training, and hyperparameter optimization, specifically for the task of intrusion detection.
It utilizes the Optuna library for hyperparameter tuning, which enhances the model's performance by finding optimal hyperparameters.
Cross-validation and detailed performance analysis help in understanding the strengths and weaknesses of each model.
The code showcases best practices in machine learning model development and evaluation for cybersecurity applications.
