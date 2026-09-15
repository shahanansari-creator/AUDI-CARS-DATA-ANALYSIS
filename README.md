# Audi Vehicle Listings — EDA & Data Visualization

Exploratory data analysis and visualization on a dataset of Audi vehicle listings, built in Python and designed to run in Google Colab. The project cleans the data, visualizes price/mileage/year/engine trends, quantifies correlations, and flags pricing outliers to inform a future price-prediction model.

## 📁 Repository Contents

| File | Description |
|---|---|
| `cars_dataset.csv` | Raw dataset of used-vehicle listings (see note below on scope) |
| `Audi_Cars_EDA.ipynb` | Colab-ready Jupyter notebook with full EDA and visualizations, pre-executed |
| `Audi_Cars_EDA_Project_Report.md` | Written project report summarizing methodology, findings, and recommendations |

## 📊 Dataset

The dataset contains **72,435 rows** across `model`, `year`, `price`, `transmission`, `mileage`, `fuelType`, `tax`, `mpg`, `engineSize`, and `Make`. It's not Audi-only — the `Make` column spans seven brands (Audi, BMW, Ford, VW, Toyota, Skoda, Hyundai). This project filters to the **10,668 Audi listings** as its main scope, with a bonus cross-brand comparison included.

## 🚀 Running in Google Colab

1. Open `Audi_Cars_EDA.ipynb` in [Google Colab](https://colab.research.google.com/).
2. Upload `cars_dataset.csv` to the Colab session (or mount Google Drive) when prompted in the first code cell.
3. Run all cells top to bottom — no other setup required (uses `pandas`, `numpy`, `matplotlib`, `seaborn`, all pre-installed on Colab).

## 🔍 What's Inside the Notebook

- Data cleaning (whitespace stripping, null/duplicate checks)
- Univariate analysis: price, mileage, year, engine size, mpg, tax distributions
- Categorical breakdowns: model, transmission, fuel type
- Bivariate analysis: price vs. year, mileage, engine size, transmission, fuel type
- Correlation heatmap across numeric features
- IQR-based outlier detection on price
- Bonus: Audi vs. other brands in the dataset

## 📈 Key Findings

- Audi listing prices range from **£1,490 to £145,000** (mean **£22,897**, median **£20,200**), right-skewed by high-end RS/S-line and R8 listings.
- **Year** (+0.59) and **engine size** (+0.59) are the strongest positive correlates of price; **mileage** (−0.54) and **mpg** (−0.60) are the strongest negative correlates.
- **A3, Q3, A4, A1** are the highest-volume models; **R8, Q8, RS6, RS5, RS4** command the highest average prices.
- **443 listings (4.15%)** are statistical price outliers — almost entirely genuine premium/performance models, not data errors.
- Across brands, **Audi has the highest average listing price (£22,897)**, narrowly ahead of BMW (£22,733).

Full methodology, charts, and recommendations are in [`Audi_Cars_EDA_Project_Report.md`](./Audi_Cars_EDA_Project_Report.md).

## 🛠️ Tech Stack

- Python 3
- pandas, numpy
- matplotlib, seaborn
- Jupyter / Google Colab

## 📌 Next Steps

- Build a regression model to predict `price` (one-hot encode categorical fields, log-transform `price`/`mileage`, handle outliers separately for performance/flagship models).
- Extend the cross-brand comparison into a full multi-brand pricing analysis.

## 📬 Contact

Mohd Shahan Ansari — [Shahanansarimoto@gmail.com](mailto:Shahanansarimoto@gmail.com) · [LinkedIn](https://www.linkedin.com/in/mohd-shahan-ansari-100479259/) · [GitHub](https://github.com/shahanansari-creator)
