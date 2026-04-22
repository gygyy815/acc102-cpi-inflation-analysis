这是根据你的CPI通胀分析项目和ACC102课程要求定制的**完整README.md文件**。你只需要将方括号 `[]` 中的内容替换为你的实际信息即可。

```markdown
# US CPI Inflation Trend Analysis (2010-2023)

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![XJTLU](https://img.shields.io/badge/XJTLU-ACC102-red)](https://www.xjtlu.edu.cn)

**Demo Video**: [Insert your Mediasite or YouTube link here]

---

## 1. Problem & User

**Problem**: Understanding inflation trends is crucial for economic decision-making, yet raw CPI data is often presented in complex tables. It is difficult for general audiences to quickly grasp long-term trends and identify periods of significant economic change, such as the post-pandemic inflation surge.

**User/Audience**: This project is designed for **Economics students, early-career financial analysts, and general news readers** who want a quick, visual, and data-driven overview of US inflation over the last decade without needing to access specialized economic databases or software.

---

## 2. Data

- **Source**: U.S. Bureau of Labor Statistics (BLS) - Consumer Price Index for All Urban Consumers (CPI-U)
- **File**: `cpiai.csv`
- **Access Date**: **April 22, 2026**
- **Key Fields**:
    - `Date`: Monthly observation (YYYY-MM-DD)
    - `Index`: CPI Index value (1982-1984 = 100)
    - `Inflation`: Month-over-month inflation rate (%)

---

## 3. Methods & Technical Steps

The analysis is performed entirely in Python using a Jupyter Notebook (`analysis.ipynb`). The core workflow includes:

1. **Import Libraries**: Load `pandas`, `matplotlib`, and `seaborn` for data manipulation and visualization
2. **Data Ingestion & Cleaning**: Load CSV data using `pandas`. Convert the 'Date' column to `datetime` format for time-series analysis
3. **Filtering**: Extract the 'Year' from the date and filter the dataset to focus on the period **2010–2023**
4. **Time-Series Visualization**: Use `matplotlib` and `seaborn` to plot monthly inflation rates, highlighting periods of volatility
5. **Aggregation**: Group data by year to calculate the **average annual inflation rate**
6. **Comparative Analysis**: Generate a bar chart comparing annual inflation performance across the 14-year period
7. **Summary Statistics**: Calculate and display maximum, minimum, and peak inflation years

---

## 4. Key Findings

- **Post-Pandemic Surge**: The analysis clearly visualizes a sharp inflation spike beginning in 2021, peaking at **1.37% monthly** in the dataset
- **Peak Inflation Year**: **2021** was identified as the year with the highest average annual inflation rate within the 2010-2023 window
- **Deflationary Period**: The dataset recorded a minimum monthly inflation rate of **-0.67%** (deflation) during the observed period
- **Pre-Pandemic Stability**: Inflation remained relatively stable from 2010-2019 (mostly between 0.0% and 0.5% monthly), making the 2020-2023 period a significant outlier
- **Visual Storytelling**: The combination of time-series and bar charts effectively communicates both short-term volatility and long-term trends to a general audience

---

## 5. How to Run

To reproduce this analysis locally:

1. **Clone the repository**:
   ```bash
   git clone [your-repo-url]
   cd [repo-name]
   ```

2. **Install dependencies**:
   Ensure you have Python 3.8 or higher installed, then run:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Notebook**:
   Launch Jupyter Lab or Jupyter Notebook:
   ```bash
   jupyter notebook analysis.ipynb
   ```
   Alternatively, you can run it in VS Code with the Jupyter extension.

4. **Expected Output**:
   - Two visualizations will display: a monthly inflation trend line chart and an annual average bar chart
   - Summary statistics will print to the console
   - Charts are automatically saved to the `figures/` folder as PNG files

---

## 6. Repository Structure

```
[repo-name]/
├── README.md                # Project documentation (you are here)
├── analysis.ipynb           # Main Jupyter Notebook with code & visualizations
├── cpiai.csv                # Source dataset (CPI data from BLS)
├── requirements.txt         # Python library dependencies
└── figures/                 # Exported chart images
    ├── monthly_inflation_trend.png
    └── annual_inflation_bar.png
    └── annual_inflation_bar_hue.png
```

---

## 7. Limitations & Next Steps

**Limitations**:
- The analysis uses **Month-over-Month** inflation rather than the more commonly reported **Year-over-Year** rate, which may understate long-term cumulative price changes
- The dataset does not break down inflation by category (e.g., Food, Energy, Shelter), limiting sector-specific insights
- The analysis is descriptive rather than predictive; it does not forecast future inflation trends

**Future Improvements**:
- Implement a function to automatically calculate Year-over-Year inflation for more standard economic reporting
- Deploy the visualization as an interactive **Streamlit** dashboard (Track 4) allowing users to select custom date ranges and compare different time periods
- Incorporate additional economic indicators (e.g., unemployment rate, GDP growth) for richer contextual analysis

---

## 8. Reflection & AI Disclosure

*This section provides a brief summary. For the full 500-800 word reflection and detailed AI disclosure, please refer to the separate reflection document submitted on LMO.*

This project was developed as part of the ACC102 Mini Assignment (Track 2). The primary challenge was ensuring the data path was relative to allow for cross-platform reproducibility. I learned the importance of structuring data transformation steps clearly in the notebook to tell a coherent data story. The project strengthened my understanding of time-series data manipulation in pandas and effective visualization design for non-technical audiences.

**AI Disclosure Summary**:

| Item | Details |
|------|---------|
| **Tool** | DeepSeek |
| **Model/Version** | DeepSeek-V3 |
| **Access Date** | April 15-22, 2026 |
| **Purpose** | Assisted with formatting the README.md structure, generating code comments, and debugging the `pd.to_datetime` syntax in the data cleaning step |
| **Human Verification** | All AI-generated content was manually reviewed, tested, and validated by the author. The final code and documentation reflect my own understanding and decisions |

---

## 9. Acknowledgements

- Data provided by the **U.S. Bureau of Labor Statistics (BLS)**
- This project was completed as part of **ACC102: Introduction to Data Analytics** at **Xi'an Jiaotong-Liverpool University (XJTLU)**
```

---

## 使用前检查清单

在提交前，请确认以下内容已替换：

| 位置 | 需要替换的内容 | 示例 |
|------|---------------|------|
| 第1行（徽章下方） | `[Insert your Mediasite or YouTube link here]` | `https://youtu.be/abc123xyz` |
| 第2节（Data） | `[Insert Date]` | `April 22, 2026` |
| 第5节（How to Run） | `[your-repo-url]` | `https://github.com/zhangsan/acc102-cpi-project.git` |
| 第5节（How to Run） | `[repo-name]` | `acc102-cpi-project` |
| 第6节（Repository Structure） | `[repo-name]` | `acc102-cpi-project` |
| 第8节（AI Disclosure） | 根据实际使用的AI工具调整 | DeepSeek / ChatGPT / Copilot |
