# 🏠 Apartment Rent Price Prediction using Spark MLlib

## 🎯 Objective

Implement a comprehensive data mining project using **Spark MLlib** to predict apartment rental prices. This task focuses exclusively on Spark MLlib for machine learning operations, while allowing all non-ML libraries for data manipulation and visualization.

---

## 🚀 How to Run

1. **Download and install Docker**
2. **Clone this repository**
   ```bash
   git clone <repository-url>
   cd csci316-group-assignment
   ```
3. **Build and start the containers**
   ```bash
   docker compose up --build -d
   ```
4. **Change Jupyter Token/Password**
   - Change the jupyter token/password in ./docker-compose.yml
   - Or just use the default 123456
5. **Access Jupyter**
   - Open your browser and navigate to `http://localhost:8888`
   - Run the notebook files

---

## 📋 Requirements

### 1. **Data Split Configuration**
- **Training Set:** 80% of the dataset
- **Test Set:** 20% of the dataset

### 2. **Project Structure**
The project follows these main phases:

| Phase | Description | Status |
|-------|-------------|--------|
| **(a)** | **Discover and visualize the data** | ✅ |
| **(b)** | **Prepare the data for machine learning algorithms** | ✅ |
| **(c)** | **Select and train models** | ✅ |
| **(d)** | **Fine-tune the model** | ✅ |
| **(e)** | **Evaluate the outcomes** | ✅ |

> **Note:** Steps can be performed iteratively for continuous improvement.

### 3. **Feature Engineering**
- ✅ Define **at least one new feature** using `RFormula` in step (b)
- ✅ Apply comprehensive data preprocessing techniques
- ✅ Handle missing values and outliers appropriately

### 4. **Machine Learning Models**
- ✅ Implement and compare **at least three different ML algorithms**
- ✅ Focus exclusively on algorithms available in Spark MLlib
- ✅ Include hyperparameter tuning with cross-validation

### 5. **Documentation Requirements**
- ✅ **Detailed explanations** for each step
- ✅ **Complete Python code** with comprehensive comments
- ✅ **Performance comparison** between all models
- ✅ **Comprehensive analysis** of results and insights

### 6. **Comparative Analysis**
- 📝 Brief report comparing **Spark MLlib** vs **Scikit-Learn**
- 📊 **Pros and Cons** of each framework
- 🔍 **Similarities and Differences**
- 💡 **Use case recommendations**
- 📈 **Personal insights** from assignment experience

---

## 📊 Expected Deliverables

### 📓 **Main Deliverables**
1. **Jupyter Notebook** with complete implementation
2. **Model performance metrics** and detailed comparisons
3. **Data visualizations** and actionable insights
4. **Feature engineering documentation** with rationale

### 📈 **Analysis Reports**
5. **Spark MLlib vs Scikit-Learn comparison report**
6. **Model evaluation summary**

### 🏗️ **Technical Infrastructure**
7. **Docker containerization** for reproducible environment
8. **Complete project structure** with organized code

---

## 🏆 Models Implemented

| Model | Algorithm | Performance | Status |
|-------|-----------|-------------|--------|
| **Gradient Boosted Trees** | Sequential ensemble learning | **Best R² = 0.7829** | ✅ |
| **Random Forest** | Parallel ensemble learning | R² = 0.7650 | ✅ |
| **Linear Regression** | Linear relationship modeling | R² = 0.7102 | ✅ |

---

## 📁 Project Structure

```
csci316-group-assignment/
├── build/
│   ├── Dockerfile
│   └── requirements.txt
├── data/
│   ├── apartments_for_rent_classified_100K.csv
│   └── transformed_apartment_data.parquet/
├── deliverables/
│   └── leap-csci316-task2.pdf
├── images/
│   ├── geo_map_apartment_prices.png
│   ├── top5_least_vs_most_expensive.png
│   ├── top10_states_with_the_most_listings.png
│   └── median_price_by_month_top_10_states.png
├── models/
│   ├── gbt_regressor/
│   ├── linear_regressor/
│   ├── random_forest_regressor/
│   └── scaler/
├── Leap_Assignment2_Task2.ipynb
├── docker-compose.yml
└── README.md
```

---

## 🔧 Dependencies

- **Spark MLlib** - Machine learning operations
- **PySpark** - Spark Python API
- **Pandas** - Data manipulation
- **Plotly/Matplotlib** - Data visualization
- **Jupyter** - Interactive development environment

---
