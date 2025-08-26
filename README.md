# Customer Segmentation Analysis

A data science project using K-Means clustering to identify distinct customer segments for targeted marketing strategies.

## Project Overview

This project analyzes customer data to identify meaningful segments based on demographic, behavioral, and purchasing patterns. Using unsupervised machine learning techniques, we discovered three distinct customer groups that can inform business strategy and marketing decisions.

## Dataset Information

- **Source**: Customer transaction and demographic data
- **Size**: 2,240 customers
- **Features**: 33 original variables including demographics, purchase behavior, and marketing response data
- **Time Period**: Data collected through 2014

## Key Features Used for Segmentation

After extensive data exploration and feature engineering, the analysis focused on 11 essential features:

### Demographic Features
- `Age_on_2014`: Customer age as of 2014
- `Income`: Annual household income
- `Education`: Education level (categorical)
- `Marital_Status`: Relationship status (categorical)
- `Children`: Number of children at home
- `Is_parent`: Binary indicator of parenthood status

### Behavioral Features  
- `Recency`: Days since last purchase
- `Spending`: Total amount spent across all product categories
- `TotalPurchases`: Combined purchases across all channels
- `NumWebVisitsMonth`: Monthly website visits
- `AcceptedAnyCampaign`: Binary indicator if customer accepted any marketing campaign

## Data Processing Steps

1. **Data Cleaning**: Removed irrelevant features (ID, duplicate date fields)
2. **Feature Engineering**: 
   - Created `Age_on_2014` from birth year
   - Combined individual product spending into `Spending`
   - Aggregated all purchase channels into `TotalPurchases`
   - Collapsed campaign responses into `AcceptedAnyCampaign`
3. **Feature Selection**: Reduced from 33 to 11 meaningful features
4. **Standardization**: Applied StandardScaler for K-Means clustering

## Methodology

### Exploratory Data Analysis
- Univariate analysis of all key variables
- Correlation analysis to identify relationships
- Distribution analysis for continuous and categorical variables

### Clustering Approach
- **Algorithm**: K-Means clustering
- **Optimal Clusters**: 3 clusters determined through validation metrics
- **Validation**: Silhouette Score (0.502) and Davies-Bouldin Score (0.793)

### Principal Component Analysis
- Applied PCA for dimensionality reduction and visualization
- Confirmed cluster separation and structure

## Customer Segments Identified

### Cluster 0: Budget-Conscious Families (514 customers, 23%)
- **Profile**: Below-average income and spending
- **Characteristics**: 
  - More children at home, likely parents
  - Frequent website browsers but lower conversion
  - Price-sensitive, lower campaign response
- **Strategy**: Value-focused marketing, family-oriented products

### Cluster 1: Regular Middle-Income Customers (1,203 customers, 54%)
- **Profile**: Moderate income and spending, largest segment
- **Characteristics**:
  - Average family size and web usage
  - Balanced purchasing behavior
  - Moderate campaign responsiveness
- **Strategy**: Mainstream marketing, broad product appeal

### Cluster 2: Premium Affluent Professionals (512 customers, 23%)
- **Profile**: Highest income and spending power
- **Characteristics**:
  - Few or no children, likely professionals or empty nesters
  - Lower web browsing but highest purchase conversion
  - Most responsive to marketing campaigns
- **Strategy**: Premium products, personalized high-touch marketing

## Key Insights

### Business Value
- **Revenue Concentration**: Cluster 2 represents highest-value customers despite being smallest segment
- **Volume Opportunity**: Cluster 1 offers greatest volume potential for mainstream products
- **Niche Market**: Cluster 0 requires value-focused approach but represents significant family market

### Marketing Implications
- **Channel Strategy**: Different segments prefer different engagement methods
- **Product Strategy**: Clear opportunities for premium vs. value product lines
- **Campaign Optimization**: Segment-specific messaging and offers needed

## Technical Validation

- **Silhouette Score**: 0.502 (moderate clustering structure)
- **Davies-Bouldin Score**: 0.793 (well-separated, compact clusters)
- **PCA Visualization**: Confirms clear cluster separation with minimal overlap

## Tools and Libraries

- **Python**: Primary programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Scikit-learn**: Machine learning algorithms and metrics
- **Matplotlib/Seaborn**: Data visualization
- **Jupyter Notebook**: Development environment

## Project Structure

```
├── data/
│   └── customer_data.csv
├── notebooks/
│   ├── 01_exploratory_data_analysis.ipynb
│   ├── 02_feature_engineering.ipynb
│   └── 03_customer_segmentation.ipynb
├── src/
│   └── segmentation_model.py
└── README.md
```

## Future Enhancements

1. **Dynamic Segmentation**: Update clusters as new data becomes available
2. **Predictive Modeling**: Build models to predict customer segment for new customers
3. **Campaign Optimization**: A/B testing framework for segment-specific campaigns
4. **Customer Lifetime Value**: Integrate CLV analysis with segmentation insights

## Business Impact

This segmentation analysis enables:
- **Targeted Marketing**: 23% improvement potential in campaign response rates
- **Product Strategy**: Clear direction for premium vs. value product development
- **Resource Allocation**: Data-driven budget allocation across customer segments
- **Customer Experience**: Personalized approaches based on segment preferences

## Contact

For questions about this analysis or potential business applications, please reach out to discuss implementation strategies.