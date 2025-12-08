## 🚗 Car Data Analysis & Price Dashboard

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-blue.svg">
  <img src="https://img.shields.io/badge/Pandas-2.0+-orange.svg">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-orange.svg">
  <img src="https://img.shields.io/badge/PowerBI-Dashboard-yellow.svg">
  <img src="https://img.shields.io/badge/License-MIT-green.svg">
</p>

An intelligent data analysis dashboard for automated exploratory data analysis (EDA) on used car resale data to identify key factors influencing car selling prices.

---

**Quick Navigation:** [Features](#-features) • [Installation](#-installation) • [Usage](#-usage) • [Screenshots](#-screenshots) • [Dashboard](#-dashboard) • [Key Insights](#-key-insights) • [Demo](#-demo)

---

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Analysis Highlights](#analysis-highlights)
- [Dashboard](#dashboard)
- [Key Insights](#key-insights)
- [Technologies Used](#technologies-used)
- [Authors](#authors)
- [License](#license)

---

## 🎯 Project Overview

This project performs a complete data analysis workflow on a used car dataset to:

- 🔍 **Understand** the used car market behavior
- 📊 **Identify** the most important factors affecting car prices
- 💡 **Support** better pricing, buying, and selling decisions using data-driven insights
- 🤖 **Build** a foundation for price prediction models

---

## ✨ Features

- ✅ **Complete Data Cleaning** - Handles missing values, outliers, and data quality issues
- ✅ **Feature Engineering** - Creates meaningful features like car age, brand extraction, and price per kilometer
- ✅ **Statistical Analysis** - Comprehensive univariate, bivariate, and multivariate analysis
- ✅ **Data Visualization** - Rich charts and graphs using Matplotlib and Seaborn
- ✅ **Interactive Dashboard** - Power BI dashboard for dynamic data exploration
- ✅ **Business Insights** - Actionable conclusions for pricing strategies
- ✅ **Automated Workflows** - Streamlined EDA process from data loading to insights

---

## 📊 Dataset

The dataset contains **4,345 records** with the following features:

- `name`: Car name (brand + model)
- `year`: Manufacturing year
- `selling_price`: Selling price (target variable)
- `km_driven`: Kilometers driven
- `fuel`: Fuel type (Petrol, Diesel, CNG, LPG, Electric)
- `seller_type`: Type of seller (Individual, Dealer)
- `transmission`: Transmission type (Manual, Automatic)
- `owner`: Ownership history (First Owner, Second Owner, etc.)

### Dataset Preview

<!-- Add screenshot of dataset preview here -->
![Dataset Preview](screenshots/dataset_preview.png)

---

## 📁 Project Structure

```
Final Project/
│
├── Dataset/
│   └── car_data.csv              # Original dataset
│
├── Dashboard/
│   ├── Car Dashboard.pbix        # Power BI dashboard file
│   ├── image.png                 # Dashboard screenshot 1
│   └── image2.png                # Dashboard screenshot 2
│
├── TMP_project_phase1_DS.ipynb  # Main Jupyter notebook with complete analysis
│
├── Used Car Market Analysis Presentation
│
└── README.md                      # This file
```

---

## 🚀 Installation

### Prerequisites

- Python 3.8 or higher
- Jupyter Notebook or JupyterLab
- Power BI Desktop (for dashboard)

### Required Python Libraries

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

Or install from requirements file (if available):

```bash
pip install -r requirements.txt
```

---

## 💻 Usage

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd <repository-name>
   ```

2. **Open the Jupyter Notebook**:
   ```bash
   jupyter notebook TMP_project_phase1_DS.ipynb
   ```

3. **Update the dataset path** in the notebook:
   ```python
   df = pd.read_csv("Dataset/car_data.csv")
   ```

4. **Run all cells** to execute the complete analysis

5. **Open the Power BI Dashboard**:
   - Open `Dashboard/Car Dashboard.pbix` in Power BI Desktop
   - Connect to the cleaned dataset

---

## 📸 Screenshots

### Code & Analysis

<img width="1577" height="828" alt="Screenshot 2025-12-06 092529" src="https://github.com/user-attachments/assets/a2f3af37-6cf1-47be-ab51-b5ab176f07cc" />
<img width="1780" height="837" alt="Screenshot 2025-12-06 092514" src="https://github.com/user-attachments/assets/1043b801-fe35-4eb3-9b11-c80b284bfded" />

### Key Analysis Steps

1. **Data Cleaning**:
   - Fixed spelling mistakes in categorical features
   - Handled missing values using median (numerical) and mode (categorical)
   - Removed invalid values (negative prices, unrealistic years)
   - Clipped outliers using percentile-based method

2. **Feature Engineering**:
   - Created `car_age` feature (current_year - year)
   - Extracted `brand` from car name
   - Calculated `price_per_km` (selling_price / km_driven)

3. **Statistical Analysis**:
   - Distribution analysis for all features
   - Correlation analysis between variables
   - Relationship analysis between price and other features

---

## 📊 Dashboard

### Interactive Power BI Dashboard

<img width="1736" height="713" alt="Screenshot 2025-12-06 092753" src="https://github.com/user-attachments/assets/85c71f4a-df58-4a40-b26c-b417f90a8d85" />
<img width="1727" height="705" alt="Screenshot 2025-12-06 092830" src="https://github.com/user-attachments/assets/5e94614a-f3cd-4e8c-95a5-7dd5c16c4250" />

The Power BI dashboard provides:
- Interactive filters for all features
- Price distribution visualizations
- Brand comparison charts
- Transmission and fuel type analysis
- Owner type impact on pricing

---

## 🎬 Demo

<!-- Add demo video or GIF here -->
![Project Demo](screenshots/demo.gif)

*Interactive demonstration of the analysis workflow and dashboard features.*

---

## 🔍 Key Insights

### Top 8 Findings

1. **🚗 Car Age** is the strongest factor in price determination
   - As car age increases, selling price decreases significantly

2. **🛣️ Km Driven** reflects real usage level
   - Higher mileage directly reduces selling price

3. **⚙️ Automatic Transmission** adds a fixed premium
   - Automatic cars are priced higher than manual in all scenarios

4. **⛽ Diesel** retains value longer
   - Diesel cars show slower depreciation compared to petrol

5. **👤 Number of Owners** directly reduces market value
   - More previous owners lead to clear price drops

6. **🏷️ Brand** is a powerful determinant of price
   - Some brands maintain value despite age or mileage increases

7. **📊 Strongest Market Pricing Combinations**:
   - **Highest price**: Diesel + Automatic + First Owner + Low Car Age + Low Km Driven
   - **Lowest price**: Petrol + Manual + Third Owner + Old Car + High Km Driven

8. **🧠 Most Influential Variables** (in order):
   1. Car Age
   2. Km Driven
   3. Transmission
   4. Fuel Type
   5. Owner
   6. Brand

### Business Applications

These insights can be applied to:
- ✅ Building smart pricing models
- ✅ Identifying profitable deals
- ✅ Classifying cars into Economic – Mid-range – Luxury
- ✅ Helping buyers make informed purchase decisions
- ✅ Assisting dealers in reducing losses and increasing profits

---

## 🛠️ Technologies Used

| Technology | Version | Purpose |
|------------|---------|---------|
| **Python** | 3.8+ | Programming language |
| **Pandas** | 2.0+ | Data manipulation and analysis |
| **NumPy** | 1.24+ | Numerical computations |
| **Matplotlib** | 3.7+ | Data visualization |
| **Seaborn** | 0.12+ | Statistical data visualization |
| **Jupyter Notebook** | 1.0+ | Interactive development environment |
| **Power BI** | Latest | Business intelligence and dashboard creation |

---

## 👥 Authors

<!-- Add author names here -->
- **Shahd Alhindawy** - [GitHub Profile](https://github.com/shahdelhendawy)
- **Mohamed Younis** - [GitHub Profile](https://github.com/mohamedyounis10)
- **Mariam Fouad** - [GitHub Profile](https://github.com/mariamfo2ad)

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Microsoft Student Club - KFS - Project phase 1
- Special thanks to all contributors

---

## 📧 Contact

For questions or suggestions, please open an issue or contact the authors.

---

**⭐ If you find this project helpful, please give it a star!**




