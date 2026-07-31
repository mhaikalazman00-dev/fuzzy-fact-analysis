# Strategic Growth Opportunities: A Diagnostic Analysis of Maven Fuzzy Factory’s E-Commerce Performance (2012–2015)
Analyzing 3 years of sales records with 30k+ orders and 470k+ sessions to identify growth opportunities for an e-commerce business.

## 📖 Table of Contents
- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Data Source](#data-source)
- [Tools & Technologies](#tools--technologies)
- [Methodology](#methodology)
- [Key Findings & Insights](#key-findings--insights)
- [Visualization Gallery](#visualization-gallery)
- [How to Reproduce](#how-to-reproduce)
- [Conclusion & Next Steps](#conclusion--next-steps)
- [Contact](#contact)

---

## 📌 Overview
This project analyzes a database entailing order records, session metadata, and website analytics to optimize revenue acquisition. The goal is to find room for optimization based on trends and make actionable insights that can help stakeholders make data-driven decisions regarding their future strategies.

## 🎯 Problem Statement
The core challenge addressed in this analysis is:
> Maven Fuzzy Factory is scaling its e-commerce operations and recognizes the need to better understand its business landscape. With transactional and site traffic data spanning 2012–2015, the company seeks to conduct an exploratory diagnostic analysis to uncover patterns, trends, and potential opportunities.

**Objectives:**
- Explore revenue and traffic trends to identify patterns and anomalies in the data.
- Generate hypotheses for deeper investigation or future analysis.
- Provide recommendations to improve sales.

## 📂 Data Source
The dataset used for this analysis was obtained from [Maven Analytics](https://mavenanalytics.io/).
- **Date Range:** March 19th 2012 to March 19th 2015
- **Record Count:**
   - orders_df: 32313
   - order_items_df: 40025
   - sessions_df: 472871
   - pageviews_df: 1188124
 
- **Columns:** [Number] features (e.g., `customer_id`, `transaction_date`, `revenue`, `region`)
  - orders_df: 8 features: `order_id`, `created_at`, `website_session_id`, `user_id`, `primary_product_id`, `items_purchased`, `price_usd`, `cogs_usd`
  - order_items_df: 7 features: `order_item_id`, `created_at_id`, `order_id`, `product_id`, `is_primary_item`, `price_usd`, `cogs_usd`
  - sessions_df: 9 features: `website_session_id`, `created_at`, `user_id`, `is_repeat_session`, `utm_source`, `utm_campaign`, `utm_content`, `device_type`, `http_referrer`
  - pageviews_df: 4 features: `website_pageview_id`, `created_at`, `website_session_id`, `pageview_url`

*Note: The raw data has been cleaned and pre-processed. See the [Methodology](#methodology) section for details.*

## 🛠 Tools & Technologies
- **Data Extraction/Storage:** Python | Pandas
- **Data Cleaning:** Python | Pandas | Numpy
- **Exploratory Data Analysis (EDA):** Jupyter Notebooks / Kaggle Notebooks
- **Visualization & Dashboarding:** Matplotlib | Seaborn | Plotly

## 🔍 Methodology
This analysis followed a standard data analytics pipeline:

1. **Data Extraction & Loading:** Data was downloaded from Maven Analytics website and loaded into Kaggle.
2. **Data Cleaning:**
   - The dataset has no need for extensive cleaning as the integrity and usability is proper.
   - Standardized date formats for all `created_at` columns.
3. **Exploratory Data Analysis (EDA):**
   - Used line charts to identify trends in revenue, conversions, and traffic.
   - Used Sankey diagram to identify traffic paths/customer journey.
   - Used `pd.DataFrame.groupby()` to aggregate data and understand trends.
   - Used stacked area charts to compare product sales and traffic by channel over time.
4. **Feature Engineering:**
   - Created new metrics such as:
     - conversion rates
     - end-of-week sales aggregation
     - journey map label
     - QoQ growth
6. **Visualization:** Built charts and visuals to highlight key trends (refer to gallery).

## 💡 Key Findings & Insights
Based on the analysis, the following insights were discovered:

- **Insight 1:** Weekend-Weekday Traffic Gap – Maven Fuzzy Factory has significantly lesser traffic during weekends compared to weekdays, while maintaining similar conversion rates. This leads to weekly sales dips and signals lost opportunities for the business. While QoQ shows steady growth throughout the 3-year period, the gap between weekend sales and weekday sales are widening. Optimizing weekend traffic to scale with weekday sales  by even 10% has the potential to increase yearly revenue by over USD13k.
- **Insight 2:** Consolidated Products Portfolio – Maven Fuzzy Factory's product line are consolidated into 2; collectibles and commemorative plushies. 3 of the products have similar price band. The similarities will be appeal to narrower segments when the business could offer more segmentation to cater to customers' interests.
- **Insight 3:** Constrained Product Visibility – Despite the consolidated product portfolios, `The Original Mr. Fuzzy` is the most popular item, accounting for more than half of the sales. This raises a concern that other products are overshadowed by the `The Original Mr. Fuzzy`.
- **Insight 4:** Lack of Seasonality – On top of the visibility concerns and consolidated products portfolio, there is a concern for future losses in the next seasonal cycle. Analysis shows that `The Original Mr. Fuzzy`'s sales drops by almost half on Valentine's day, while `The Forever Love Bear` sales spikes by three times their typical sales. Currently, `The Original Mr. Fuzzy`'s losses are covered by `The Forever Love Bear`'s sales, but the coverage are decreasing due to `The Forever Love Bear`'s sales are unable to scale with `The Original Mr. Fuzzy`.


## 📊 Visualization Gallery
*Below are key screenshots from the analysis. Click to view the interactive dashboard.*

![Sankey Diagram](path/to/newplot (1).png)
*Figure 1: Overview of sales performance by region.*

![Trend Analysis](path/to/screenshot2.png)
*Figure 2: Monthly revenue trend showing a 15% increase in Q3.*

> **View Live Dashboard:** [Insert Link to Tableau Public/Power BI Service/Streamlit App]

## 🚀 How to Reproduce
To run this project locally:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/[project-name].git
   cd [project-name]
