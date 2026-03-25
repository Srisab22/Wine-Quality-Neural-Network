Wine Quality Prediction using Neural Networks from Scratch 
 Artificial Neural Network & Deep LearningThis repository contains a complete implementation of a multi-layer perceptron (Neural Network) built using only NumPy and Pandas. The project demonstrates the manual implementation of forward propagation, backpropagation, and gradient descent to predict wine quality based on chemical properties.
📌 Project Overview
The objective is to analyze the Wine Quality Dataset and build a predictive model. Unlike using high-level frameworks like TensorFlow or PyTorch, this project focuses on the underlying mathematics of neural networks, including:Manual weight initialization and matrix operations.Implementation of ReLU and Sigmoid activation functions.Calculation of gradients using the Chain Rule.Feature engineering through correlation analysis.
📊 Dataset Description
The dataset used is WineQT.csv, which consists of 1,143 wine samples.Input Features: 11 chemical attributes (Fixed acidity, Volatile acidity, Alcohol, Sulphates, etc.)Target Variable: quality (Categorical score, normalized for the network).
🛠️ Technical Implementation1. 
Exploratory Data Analysis (EDA)Data Cleaning: Removed irrelevant columns like Id.Feature Selection: Calculated the correlation matrix and selected features with a Pearson correlation coefficient $> 0.1$ against the target variable to reduce noise and improve model efficiency.Normalization: Applied StandardScaler to ensure all features contribute equally to the weight updates.2. Neural Network ArchitectureThe model is a Deep Neural Network with the following structure:Input Layer: 8 nodes (based on selected features).Hidden Layer 1: 16 nodes with ReLU activation.Hidden Layer 2: 8 nodes with ReLU activation.Output Layer: 1 node with Sigmoid activation (predicting normalized quality).3. Training ProcessLoss Function: Mean Squared Error (MSE).Optimization: Gradient Descent with a learning rate of $0.01$.Epochs: 500 iterations to minimize the loss.
🚀 How to Run the CodeClone the Repository:Bashgit clone https://github.com/YOUR_GITHUB_USERNAME/Wine-Quality-Neural-Network.git
Install Dependencies:Bashpip install numpy pandas matplotlib seaborn scikit-learn
Run the Notebook:Open WineQT_EDA.ipynb in Jupyter Notebook or VS Code and run all cells.
📉 Results & Visualization
The project generates two key plots:Training Loss Curve: Visualizes how the MSE decreases as the backpropagation algorithm updates the weights over 500 epochs.Actual vs. Predicted Plot: A scatter plot comparing the model's predictions on the test set against the ground truth labels.
📂 File Structure
WineQT.csv - The raw dataset.WineQT_EDA.ipynb - The primary source code for EDA and the Neural Network.README.md - Project documentation.
