# 🦠 COVID-19 Exploratory Data Analysis (EDA)

### 📊 Overview
This project presents an **Exploratory Data Analysis (EDA)** of the global **COVID-19 pandemic**, using daily case and death data reported by the **World Health Organization (WHO)**.  
It aims to uncover key insights such as:
- The most affected countries and regions  
- Temporal trends in cases and deaths  
- Countries with the highest fatality ratios  
- Global and regional distributions of cases and deaths  

---

### 🧩 Dataset Information
**Source:** [World Health Organization (WHO)](https://www.who.int/data)  
**Time Period:** 4 January 2020 – 3 August 2025  
**Key Columns:**
- `Date_reported` – Reporting date  
- `Country` – Country name  
- `WHO_region` – WHO region code  
- `New_cases` / `Cumulative_cases` – Daily and total confirmed cases  
- `New_deaths` / `Cumulative_deaths` – Daily and total deaths  

---

### 🧹 Data Cleaning & Preparation
- Missing values in `New_cases` and `New_deaths` were replaced with **0**.  
- Negative values (if any) were clipped to **0**.  
- Unnecessary columns (`Country_code`) were dropped.  
- Datatypes were standardized (`Date_reported` as datetime, numerical columns as int).  
- No duplicate rows were found.

---

### 📈 Key Insights
- **Total Reported Cases:** 778,555,963  
- **Total Reported Deaths:** 7,066,337  
- **Global Death Ratio:** 0.91%  
- **Highest Daily Cases:** 8,401,963 on *30 January 2022*  
- **Highest Daily Deaths:** 27,939 on *24 January 2021*  
- **Countries with No Reported Cases:** North Korea, Turkmenistan  
- **Countries with No Reported Deaths:** 13 (including DPR Korea, Holy See, and Saint Helena)  
- **Highest Death Ratio:** Yemen (18%)  

---

### 🌍 Regional Analysis (WHO)
| WHO Region | Key Insight |
|-------------|--------------|
| **EUR (Europe)** | Highest total cases (~280M) |
| **AMR (Americas)** | Highest deaths (~3M) |
| **WPR (Western Pacific)** | Significant number of cases (~200M) |
| **AFR (Africa)** | Highest death ratio among regions |
| **SEAR & EMR** | Moderate impact |

---

### 📊 Visualizations
The analysis includes:
- Line plots of global case and death trends over time  
- Bar charts of top 10 countries by cases and deaths  
- Region-wise comparisons of cases, deaths, and death ratios  
- Pie charts of regional contributions to global totals  

All visualizations were created using:
```python
import matplotlib.pyplot as plt
import seaborn as sns
from matplotlib.ticker import FuncFormatter
```

---

### 🧠 Tools & Libraries
- **Python 3.9+**
- **NumPy**
- **Pandas**
- **Matplotlib**
- **Seaborn**

---

### 🧾 Conclusion
The EDA highlights the unequal distribution of COVID-19’s impact globally.  
While some regions like Europe saw the highest infection rates, the Americas bore the greatest mortality burden. The analysis provides a data-driven understanding of how the pandemic evolved and affected different parts of the world over time.

---

### 📂 Project Structure
```
📁 COVID19-EDA
│
├── 📄 EDA Report of COVID-19.pdf        # Detailed analysis report
├── 📜 README.md                         # Project overview (this file)
├── 📊 covid_19.xlsx                     # Source dataset (not included here)
└── 🐍 covid19_analysis.ipynb            # Jupyter Notebook with full EDA
```

---

### 🚀 How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/COVID19-EDA.git
   ```
2. Navigate to the project directory:
   ```bash
   cd COVID19-EDA
   ```
3. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```
4. Run the notebook:
   ```bash
   jupyter notebook covid19_analysis.ipynb
   ```
