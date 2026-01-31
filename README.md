
## 📋 Project Overview

This project focuses on predicting Customer Satisfaction (CSAT) scores using Deep Learning Artificial Neural Networks (ANN) in the context of e-commerce. The model analyzes customer interactions and feedback to forecast CSAT scores, providing actionable insights for service improvement and enhanced customer retention.

### 🎯 Business Context
Customer satisfaction in the e-commerce sector is a pivotal metric that influences loyalty, repeat business, and word-of-mouth marketing. This project enables real-time CSAT prediction, offering a granular view of service performance and identifying areas for immediate improvement.

## 📊 Dataset Information

### Source
The dataset captures customer satisfaction scores for a one-month period at **Shopzilla** (pseudonym), an e-commerce platform.

### Dataset Characteristics
- **Total Records**: 85,907 customer interactions
- **Features**: 20 comprehensive attributes
- **Target Variable**: CSAT Score (1-5 scale)
- **Data Period**: One month of customer service interactions

### Key Features
| Feature | Description |
|---------|-------------|
| `channel_name` | Customer service channel (Inbound, Outcall, Email) |
| `category` | Interaction category (12 unique categories) |
| `Sub-category` | Detailed interaction sub-category (57 unique values) |
| `Customer Remarks` | Customer feedback text |
| `Order_id` | Associated order identifier |
| `order_date_time` | Order timestamp |
| `Issue_reported at` | Issue reporting timestamp |
| `issue_responded` | Issue response timestamp |
| `Survey_response_Date` | Customer survey date |
| `Customer_City` | Customer location (1,782 unique cities) |
| `Product_category` | Product classification (9 categories) |
| `Item_price` | Product price (₹0 - ₹164,999) |
| `connected_handling_time` | Interaction duration |
| `Agent_name` | Customer service agent |
| `Supervisor` | Agent supervisor |
| `Manager` | Team manager |
| `Tenure Bucket` | Agent experience level |
| `Agent Shift` | Agent working shift |
| **`CSAT Score`** | **Target variable (1-5 satisfaction rating)** |

## 🏗️ Model Architecture

### Neural Network Design
- **Framework**: TensorFlow/Keras
- **Architecture**: Sequential Artificial Neural Network
- **Hidden Layers**: 5 layers with 128 neurons each
- **Activation Function**: LeakyReLU for hidden layers
- **Output Layer**: Softmax (6 classes for CSAT scores 0-5)
- **Total Parameters**: 67,846 trainable parameters

### Model Configuration
```python
Model Architecture:
├── Flatten Layer (Input: 7 features)
├── Dense Layer (128 neurons) + LeakyReLU
├── Dense Layer (128 neurons) + LeakyReLU  
├── Dense Layer (128 neurons) + LeakyReLU
├── Dense Layer (128 neurons) + LeakyReLU
├── Dense Layer (128 neurons) + LeakyReLU
└── Output Layer (6 neurons) + Softmax
```

### Training Configuration
- **Optimizer**: Adagrad
- **Loss Function**: Sparse Categorical Crossentropy
- **Epochs**: 25
- **Train-Test Split**: 80-20

## 📈 Model Performance

### Accuracy Metrics
| Metric | Score |
|--------|-------|
| **Training Accuracy** | 69.5% |
| **Validation Accuracy** | 69.5% |
| **Test Accuracy** | 69.1% |

### Key Performance Insights
- ✅ **Consistent Performance**: No significant overfitting observed
- ✅ **Stable Training**: Minimal variance between training and validation accuracy
- ⚠️ **Moderate Accuracy**: 69.1% test accuracy indicates room for improvement
- 📊 **Balanced Results**: Model shows consistent performance across all datasets

## 🛠️ Technical Implementation

### Data Preprocessing
1. **Missing Data Handling**: Comprehensive null value treatment
2. **Feature Engineering**: 
   - Datetime conversion for temporal features
   - Categorical encoding for text variables
   - Numerical feature scaling using StandardScaler
3. **Feature Selection**: Removal of non-predictive features (Unique ID, Customer Remarks, Order ID)

### Technologies Used
- **Python 3.x**
- **TensorFlow 2.x** - Deep learning framework
- **Keras** - High-level neural network API
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Scikit-learn** - Machine learning utilities
- **Matplotlib/Seaborn** - Data visualization
- **Gradio** - Interactive model interface

## 🚀 Getting Started

### Prerequisites
```bash
pip install tensorflow pandas numpy scikit-learn matplotlib seaborn gradio
```

### Usage
1. **Clone the repository**
   ```bash
   git clone https://github.com/sharath199324/DeepCSAT--E-Commerce-Customer-Satisfaction-Score-Prediction-main.git
   cd CSAT-ANN-Project
   ```

2. **Run the Jupyter Notebook**
   ```bash
   jupyter notebook CSAT_ANN.ipynb
   ```

3. **Or open in Google Colab**
   - Click the "Open in Colab" badge above
   - Run all cells sequentially

## 📊 Key Findings

### Data Insights
- **Channel Distribution**: Balanced representation across Inbound, Outcall, and Email channels
- **Missing Data**: Significant null values in item price (79.98%) and handling time (99.72%)
- **CSAT Distribution**: Scores range from 1-5 with varying frequency distributions
- **Temporal Patterns**: One-month data span with comprehensive timestamp coverage

### Model Insights
- **Feature Importance**: Channel type, tenure bucket, and item price show strong predictive power
- **Performance Stability**: Consistent accuracy across training, validation, and test sets
- **Improvement Opportunities**: Enhanced feature engineering could boost performance

## 🔮 Future Enhancements

### Model Improvements
- [ ] **Advanced Architectures**: Experiment with LSTM/GRU for temporal patterns
- [ ] **Feature Engineering**: Create interaction features and temporal aggregations
- [ ] **Hyperparameter Tuning**: Optimize learning rate, batch size, and architecture
- [ ] **Ensemble Methods**: Combine multiple models for improved accuracy

### Data Enhancements
- [ ] **Text Analysis**: Implement NLP on customer remarks
- [ ] **Time Series Features**: Extract seasonal and trend components
- [ ] **External Data**: Incorporate market and economic indicators

### Deployment
- [ ] **Real-time Prediction API**: Flask/FastAPI implementation
- [ ] **Model Monitoring**: Performance tracking and drift detection
- [ ] **A/B Testing Framework**: Compare model versions in production

## 📄 Project Structure
```
CSAT-ANN-Project/
├── CSAT_ANN.ipynb          # Main analysis notebook
├── README.md               # Project documentation
├── data/                   # Dataset files (if applicable)
├── models/                 # Saved model files
└── requirements.txt        # Python dependencies
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.


