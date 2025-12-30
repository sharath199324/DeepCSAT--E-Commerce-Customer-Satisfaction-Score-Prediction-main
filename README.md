# Customer Satisfaction (CSAT) Prediction using Artificial Neural Networks

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Hritikrai55/CSAT-ANN-Project/blob/main/CSAT_ANN.ipynb)

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

