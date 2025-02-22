# Heart Disease Prediction with Deep Learning  

This project uses a deep learning model to predict the likelihood of heart disease in individuals based on various health-related features. The target variable indicates whether a person has heart disease (`1`) or not (`0`).  

## Dataset  
The dataset is stored in a CSV file named `heart.csv` and contains the following information:  
- Features: Various health-related attributes (e.g., cholesterol levels, blood pressure, age).  
- Target: The `HeartDisease` column, where `1` indicates the presence of heart disease and `0` indicates its absence.  

## Project Workflow  

### 1. Data Loading and Exploration  
- The dataset is loaded using `pandas` and explored with `.head()`, `.info()`, and `.describe()` methods.  
- The dataset's features and target are separated for preprocessing and modeling.  

### 2. Data Preprocessing  
- **Label Encoding**: Non-numeric features are encoded using `LabelEncoder`.  
- **Train-Test Split**: The dataset is split into training and testing sets (80%-20%).  
- **Normalization**: Features are scaled to a range of `[0, 1]` using `MinMaxScaler`.  

### 3. Model Architecture  
The model is implemented using TensorFlow and Keras:  
- Input Layer: 11 features.  
- Hidden Layers:  
  - Four dense layers with 128 neurons each and ReLU activation.  
  - Dropout layers to prevent overfitting (20%, 50%, and 30%).  
- Output Layer:  
  - A single neuron with a sigmoid activation function for binary classification.  

### 4. Model Compilation and Training  
- **Optimizer**: Adam  
- **Loss Function**: Binary Crossentropy  
- **Metric**: Accuracy  
- The model is trained for 100 epochs with a batch size of 128.  

### 5. Results and Visualization  
The training and validation accuracy and loss are visualized using `matplotlib` to evaluate the model's performance.  
