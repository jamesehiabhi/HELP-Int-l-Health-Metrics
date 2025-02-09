# HELP-Int'l-Health-Metrics
## An Extensive Data-Driven Exploration of Socio-Economic and Health Indicators

<img src="https://github.com/jamesehiabhi/HELP-Int-l-Health-Metrics/blob/main/Displays/Cover.png" alt="Displays" width="800" height="400"/>

### ⛑️INTRODUCTION
In the realm of global development, understanding the socio-economic and health indicators of countries is crucial for policymakers, researchers, and stakeholders. This report presents an in-depth analysis of socio-economic indicators across 167 countries using machine learning techniques. The study leverages K-Means clustering to segment countries into meaningful groups based on economic and social well-being metrics. Through data-driven insights, stakeholders at **HELP International** can better allocate resources, prioritize aid, and formulate policies for global development.

### ⛑️DATA OVERVIEW
The dataset includes key socio-economic factors such as:
- **Child Mortality Rate** (per 1,000 births)
- **Life Expectancy** (years)
- **Income per Capita** (USD)
- **GDP per Capita** (USD)
- **Health Expenditure** (% of GDP)
- **Fertility Rate** (births per woman)
- **Inflation Rate** (% per year)
- **Exports & Imports** (% of GDP)

### ⛑️PROBLEM STATEMENT
- **HELP has recently been collecting data relevant to its problem statement.**
- **The Board has decided to leverage insights from this data to identify nations that embody the problems we are trying to address.**
- **For this cycle, with donations amounting to $30M, the stakeholders want us to analyze the data and provide them with a group of countries that are at the epicenter of the issues we are addressing.**
- **Additionally, the benefactors want countries with low GDP output and lower life expectancy to be prioritized when distributing aid.**

### ⛑️DATA PREPROCESSING AND ANALYSIS
The dataset was meticulously pre-processed to ensure accuracy and reliability. Key steps included:
- **Loading the Dataset:** The dataset was loaded using the Pandas library, ensuring seamless data manipulation and analysis.
- **Exploratory Data Analysis (EDA):** Initial exploration involved examining the first few rows, checking for missing values, and generating summary statistics. The dataset was found to be complete, with no missing values.
- **Data Distribution:** Analysis of child mortality, exports, health expenditure, imports, income, inflation, life expectancy, total fertility, and GDP.
- **Visualization:** Heatmaps and descriptive statistics were employed to visualize data distributions and identify correlations between variables.
- **Algorithm:** K-means clustering to determine optimal clusters.

### ⛑️DATA INSIGHTS 
**1. Child Mortality (child_mort):**
  - Right-skewed distribution.
  - Most countries have low child mortality rates (below 50).
  - Some countries exceed 100, indicating disparities in health outcomes.

**2. Exports (exports):**
- Right-skewed distribution.
- Most countries have moderate export percentages (below 75%).
- Some countries exceed 100%, showing reliance on trade.

**3. Health (health):**
- Right-skewed distribution.
- Most countries spend 4-8% of GDP on health.
- Some countries spend up to 16%, indicating differences in healthcare investments.

**4. Imports (imports):**
- Slightly right-skewed distribution.
- Similar pattern to exports.

**5. Income (income):**
- Heavily right-skewed distribution.
- Most countries earn below $40,000.
- A few wealthy countries show large disparities.

**6. Inflation (inflation):**
- Right-skewed distribution.
- Most inflation rates are below 20%.
- Some countries face hyperinflation (up to 100%).

**7. Life Expectancy (life_expec):**
- Left-skewed distribution.
- Most countries have high life expectancy (60-80 years).
- A few countries face severe health challenges.

**8. Total Fertility Rate (total_fer):**
- Right-skewed distribution.
- Most fertility rates are between 2-4 children.
- Some countries have rates over 5.

**9. GDP per capita (gdpp):**
- Highly right-skewed distribution.
- Most countries have low GDP per capita.
- A few countries are extremely wealthy.

<img src="https://github.com/jamesehiabhi/HELP-Int-l-Health-Metrics/blob/main/Displays/Data%20insight.png" alt="Displays" width="900" height="400"/>

### ⛑️KEY FINDINGS
**1. Child Mortality: A Stark Divide**
- **Range:** 2.6 (lowest) to 208 (highest deaths per 1,000 live births).
- **Outliers:** Countries like Angola (child_mort = 119) and Afghanistan (child_mort = 90.2) face acute challenges.
- **Implication:** High child mortality correlates with low GDP and healthcare spending, signalling an urgent need for targeted interventions.

**2. Economic Health**
- G**DP per Capita (gdpp):** Ranges from $231 to $105,000.
  - Median: $4,660 (highlighting wealth disparity).
- Income Inequality:
  - Top 25%: Earn over $22,800.
  - Bottom 25%: Earn below $3,355.

**Actionable Insight:** Economic policies must address the "missing middle" to uplift lower-income nations.

**3. Healthcare Spending**
- **Average expenditure:** 6.8% of GDP.
- **Outliers:**
  - **High:** 17.9% (likely countries with advanced healthcare systems).
  - **Low:** 1.81% (indicating underfunded systems).
- **Correlation:** Higher healthcare spending links to longer life expectancy (e.g., Antigua and Barbuda: life_expec = 76.8 vs. Afghanistan: 56.2).

**4. Correlation Analysis**
- **Positive Correlations:**
  - Total fertility and child mortality.
  - Imports and exports.
  - Income and exports.
  - GDP and income.
  - Life expectancy and GDP.
- **Negative Correlations:**
  - Income and child mortality.
  - Life expectancy and total fertility.

Generally, what this is telling us is that Higher GDP per capita is strongly correlated with higher life expectancy and lower child mortality. Increased health expenditure tends to improve life expectancy. Countries with high fertility rates exhibit higher child mortality rates.

<img src="https://github.com/jamesehiabhi/HELP-Int-l-Health-Metrics/blob/main/Displays/HeatMap.png" alt="Displays" width="700" height="300"/> 

### ⛑️MACHINE LEARNING APPROACH
- **Feature Scaling:** Standardized numerical features to improve clustering accuracy.
- **Elbow Method:** Identified the optimal number of clusters as **three (k=3).**
- **K-Means Clustering:** Segmented countries into three distinct socio-economic clusters.
  - Class 0: Requires urgent foreign aid.
  - Class 1: No foreign aid needed.
  - Class 2: Not a priority.

<img src="https://github.com/jamesehiabhi/HELP-Int-l-Health-Metrics/blob/main/Displays/Kmeans.png" alt="Displays" width="800" height="500"/>
<img src="https://github.com/jamesehiabhi/HELP-Int-l-Health-Metrics/blob/main/Displays/Class.png" alt="Displays" width="800" height="500"/>

**Key Insights from Clustering**
  
  **1.	High-Income Nations:**
  - High GDP per capita, low child mortality, and high life expectancy.
  - Strong investments in healthcare and education.
  - Includes countries like the USA, Canada, Germany, and Australia.

  **2.	Middle-Income Nations:**
  - Moderate GDP and life expectancy.
  - Mixed levels of health expenditure and economic growth.
  - Includes Brazil, India, and China.

  **3.	Low-Income Nations:**
- High child mortality and low life expectancy.
- Limited healthcare investment and low GDP.
- Includes several African and South Asian nations.

<img src="https://github.com/jamesehiabhi/HELP-Int-l-Health-Metrics/blob/main/Displays/Map.png" alt="Displays" width="900" height="300"/>

### ⛑️POLICY RECOMMENDATIONS
**1.	Healthcare Investments:** Increased funding for healthcare infrastructure in low-income nations can significantly enhance life expectancy and reduce child mortality.

**2.	Economic Growth Initiatives:** Policies that boost GDP and per capita income can directly impact overall well-being.

**3.	Targeted Aid Distribution:** Prioritizing financial and medical aid to Cluster 3 countries can drive substantial improvements in global development.

________________________________________
### ⛑️CONCLUSION
The **HELP International** Project used a K-means clustering algorithm to successfully categorize countries by foreign aid need. This data-driven approach, leveraging machine learning, reveals global socio-economic disparities and offers valuable insights for policymakers, aid organizations, and stakeholders to strategically guide global development. The analysis highlights strong correlations between economic growth, health expenditure, and key development indicators like child mortality, life expectancy, and fertility rates. Targeted interventions and strategic investments in health and economic sectors, tailored to each country cluster's specific challenges, will ensure efficient resource allocation for sustainable development and improved living conditions in vulnerable regions.🚀🚀
________________________________________

<br>

### *Kindly share your feedback and I am happy to Connect 🌟*

<img src="https://github.com/jamesehiabhi/HELP-Int-l-Health-Metrics/blob/main/Displays/My%20Card1.jpg" alt="Displays" width="600" height="150"/>

