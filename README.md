# Life Cycle Assessment (LCA) - Random Forest Regression Analysis
This project utilizes a Random Forest Regressor to predict the Global Warming Potential (GWP), measured in kg CO2 eq, of various beverage containers based on their life cycle data.

## 📊 Project Overview

The analysis explores how different materials, manufacturing processes, and transportation factors contribute to the environmental impact of packaging. The model identifies key variables that drive carbon emissions throughout the entire life cycle of a product.

### Key Features of the Analysis:

* **Data Preprocessing:** Handled categorical variables using **One-Hot Encoding** (for nominal columns) and **Target Encoding** (for the high-cardinality "Manufacturing process" column).
* **Model:** Random Forest Regressor with 100 trees and a max depth of 10.
* **Evaluation:** Performance is measured using R-squared (R²), Root Mean Squared Error (RMSE), and Mean Absolute Error (MAE).
* **Insights:** Feature importance ranking to identify the primary drivers of GWP.

## 📈 Dataset Summary

* **Samples:** 54
* **Features:** 13 (raw) → 32 (after encoding)
* **Target Variable:** GWP (kg CO2 eq)

| Feature Category | Examples |
| :--- | :--- |
| **Material Info** | Bottle Material, Cap Material, Filled Material, Label |
| **Logistics** | Transport Mode, Transport Distance, No. of uses, Mass |
| **Production** | Manufacturing Process, Electricity Mix, Electricity Value |
| **End of Life** | EOL Scenario, EOL Percentage |

## 🚀 Final Results

The model demonstrated strong predictive performance on the test set:

* **R² Score:** 0.8847
* **RMSE:** 13.1459 kg CO2 eq
* **MAE:** 7.0454 kg CO2 eq

## 🏆 Top Contributors to GWP

According to the model's **Feature Importance**, the most significant drivers of emissions are:

1.  **Manufacturing Process** (0.8265)
2.  **EOL Scenario: Landfilling** (0.0266)
3.  **Label Type: Paper** (0.0210)
4.  **No of uses** (0.0199)
5.  **Cap Material: Aluminium** (0.0193)
