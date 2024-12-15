# Flood Prediction and Alert System
A machine learning project designed to predict and alert about potential flood risks using historical and real-time data, all housed within a single Jupyter notebook.
![image](https://github.com/user-attachments/assets/68118a1a-c647-4e13-81b3-bda6835b2b47)

## Overview
The Flood Prediction and Alert System is a machine learning project that forecasts potential flood events and issues timely alerts to minimize risks and damages. The system leverages historical and real-time hydrological, meteorological, and geographical data to predict flood probabilities and provide actionable insights.

## Features
- **Data Preprocessing**: Handling missing data, outliers, and data scaling.
- **Feature Engineering**: Extraction of datetime features to enhance predictive capabilities.
- **Machine Learning Models**: Implement supervised learning techniques for flood prediction, including Logistic Regression, SVC, and Random Forest.
- **Alert System**: Automated generation of alerts based on prediction results integrated into the model.
- **Data Visualization**: Graphical representations of trends, patterns, and predictions within the context of flood risk.

## Project Structure
```plaintext
Flood-Prediction-Alert-System/
├── data/
│   ├── raw/                # Raw datasets
│   ├── processed/          # Cleaned and preprocessed data
├── notebooks/
│   ├── exploratory.ipynb   # Exploratory data analysis
│   ├── model_training.ipynb # Model training and evaluation
├── src/
│   ├── preprocessing.py    # Data preprocessing scripts
│   ├── model.py            # Model training and prediction scripts
│   ├── alert_system.py     # Alert generation logic
├── tests/
│   ├── test_preprocessing.py # Unit tests for preprocessing
│   ├── test_model.py        # Unit tests for the model
├── reports/
│   ├── results.pdf          # Final report of the project
├── README.md                # Project documentation
├── requirements.txt         # Python dependencies
├── .gitignore               # Ignored files and folders
└── LICENSE                  # Project license
```

## Dataset
This project uses the following data sources:
1. **Historical Flood Data**: Details of past flood events.
2. **Hydrological Data**: River levels, flow rates, etc.
3. **Meteorological Data**: Rainfall, temperature, and humidity levels.
4. **Geographical Data**: Elevation and land-use patterns.

## Installation
### Prerequisites
- **Python 3.8+**
- **Git**

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Flood-Prediction-Alert-System.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Flood-Prediction-Alert-System
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
The entire workflow—from data loading and preprocessing to model training, evaluation, and alert system implementation—is integrated into a single Jupyter notebook. This notebook provides a step-by-step guide to each phase of the project:
1. **First**, I loaded and examined the dataset, exploring its structure and missing values.
2. **Next**, I cleaned and preprocessed the data, handling missing values and scaling features.
3. **Feature Engineering** included extracting datetime features to help model the relationship between weather patterns and flood occurrences.
4. **Model Training** involved using various classifiers (Logistic Regression, SVC, Random Forest) and evaluating them to find the best performing model.
5. **Alert System Integration**: Implemented an email alert system to notify users of high flood risks based on model predictions.

Here are the main commands you can run directly from the Jupyter notebook:
1. **Preprocess the data**:
   ```python
   !python src/preprocessing.py
   ```
2. **Train the model**:
   ```python
   !python src/model.py
   ```
3. **Run the alert system**:
   ```python
   !python src/alert_system.py
   ```

## Workflow
All data processing, model training, and alert system scripts are integrated into one Jupyter notebook, providing a streamlined workflow from data ingestion to prediction. This approach facilitated the seamless integration of various preprocessing techniques and machine learning models, ensuring robust flood prediction capabilities.

## Results
The system achieved an **accuracy of 85%** using a Random Forest model on the test dataset. Predictions were validated using k-fold cross-validation and confusion matrix analysis.

## Feature Engineering
Key features like `datetime` were extracted to enhance predictive capabilities. The correlation matrix was used to avoid multicollinearity and understand which weather factors are most closely linked to flooding. The data was also encoded and scaled to facilitate model training.

## Data Visualization
- **Correlation Heatmap**: Visualized relationships between weather factors to identify significant features affecting flood risk.
- **Trend Analysis**: Visualized trends in wind speed, temperature, humidity, and sea level pressure during flood events across different months and years.

## Categorical Encoding
Weather types (`preciptype`) were encoded using `LabelEncoder` to turn categorical data into numeric values suitable for model training.

## Feature Scaling
StandardScaler was used to scale relevant features like temperature, humidity, wind speed, and sea level pressure to a standard range. This step is crucial for training effective machine learning models.

## Model Training and Evaluation
- **Logistic Regression**: Used to set a baseline model performance.
- **SVC (Support Vector Classifier)**: Implemented to evaluate performance on linear separation of flood risk data.
- **Random Forest**: Chosen as the best performing model due to its ability to handle complex interactions between features and its robust performance in classifying flood risks.

## Future Predictions
The model was validated using future weather forecasts for Lagos, predicting high-risk flood dates. The next flooding days in Lagos are expected to be the 11th of July, 2024, based on the model’s prediction. This makes the model particularly useful for early warning systems.

## Building and Embedding a Flood Alert System
The alert system was integrated into the prediction model to automatically send email alerts based on flood risk predictions. Using Python’s `smtplib`, email alerts can be sent to multiple recipients with customized messages when flood risk thresholds are met.

### Alert System Setup
- **SMTP Server**: Configured to use Gmail for sending alerts.
- **Email Functionality**: Sent real-time alerts with weather details and flood probabilities, ensuring timely response from relevant stakeholders.

## Contribution
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Submit a pull request with a detailed description of your changes.

## License
This project is licensed under the [MIT License](LICENSE).

## Author
**Regina Rukeme Agaren**  
Connect with me on [LinkedIn](https://www.linkedin.com/in/regina-rukeme-agaren/) and explore more projects on [GitHub](https://github.com/BendelHybrid/).
