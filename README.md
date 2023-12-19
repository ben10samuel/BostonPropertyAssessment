# 1.The issues

The data used in this study was collected from the City of Boston's open data hub. The dataset we used is
called "Property Assessment for year 2023". It gives property, or parcel, ownership together with value
information, which ensures fair assessment of Boston taxable and non-taxable property of all types and
classifications. Within the context of exploring property values, our investigation aims to shed light on
specific challenges and nuances embedded in the dataset.
● Do property values and areas potentially impact the overall representativeness of the dataset?
● Does value distributions indicate a concentration of higher-value properties, potentially
influencing the overall perception of property values?
● Does the dataset span a wide range of construction years, with significant peaks in certain
decades, presenting challenges in capturing historical trends and understanding their impact on
property values?

# 2. Findings

Upon careful examination of Property Assessment for year 2023, our analysis uncovers substantial patterns
and trends within the dataset.Location features (city) are crucial in determining property values, emphasizing
the importance of spatial factors in the real estate market.Strong correlations exist between property size
(living area, gross area) and various value metrics (land, building, and total values).The dataset spans a wide
range of construction years, with significant development in the 1900s and a peak in renovations during the
1980s. Year of construction/remodeling has limited correlation with property values, emphasizing the
dominance of property size and features in valuation. Skewness in value distributions suggests a
concentration of higher-value properties, contributing to a varied real estate landscape.

# 3. Discussion

The dataset analysis reveals substantial variations in property values across cities, with Readville topping the
chart at an average property value of around $5.65 million, signaling a high-end market or the presence of
outliers. Boston follows closely at approximately $3.44 million, showcasing its premium real estate status.
Histograms and correlation analyses unveil intricate patterns, demonstrating a strong positive correlation
between property size and values, while the decision tree regressor model achieves a high explanatory power
of approximately 97.62%, with a Mean Squared Error (MSE) of around $3.77 trillion on the test set. The
feature importance plot highlights the critical role of location, property size, and specific features such as air
conditioning and exterior finish in determining property values.

Furthermore, the dataset spans construction years from as early as 1700, with a mean construction year of
1926 and a significant portion of buildings erected in the 1900s. The analysis of renovation data peaks in the
1980s, with over 104,000 properties undergoing remodeling. Descriptive statistics provide insights into
property characteristics, such as average land, building, and total property values of approximately $376,586,
$1,120,689, and $1,500,262, respectively. The decision tree model, while powerful, indicates room for
improvement, particularly in addressing outliers, as evidenced by the Root Mean Squared Error (RMSE) of
approximately $81,394.79. Overall, this comprehensive analysis not only delves into the nuances of property
value determinants but also offers practical insights for stakeholders navigating the diverse and dynamic
housing market.

# APPENDIX A: METHOD

The PROPERTY ASSESSMENT FY2023 dataset, consisting of 180,623 entries, was obtained for in-depth
analysis. The dataset exhibits consistent reporting across all examined columns, providing a comprehensive
representation of property characteristics for the fiscal year 2023.
Descriptive statistics were computed to gain insights into the properties within the dataset. The average
values for land, building, and total property were found to be approximately $376,586, $1,120,689, and
$1,500,262, respectively. Notably, the dataset displays a wide range in property values, as evidenced by high
standard deviations. The average living and gross areas were observed to be 3,814 and 4,763 square feet,
respectively, with a predominant year of construction around 1928.

A significant skewness in the distribution of property values was observed, with median values for land,
building, and total property notably lower than their respective means. This skewness indicates a
concentration of higher-value properties within a subset of the dataset. Similar skewness was identified in
property sizes, emphasising a prevalence of smaller-sized properties.

The Random Forest Regression model was employed to predict property values. This ensemble learning
technique, consisting of multiple decision trees, was trained on a subset of the dataset. Hyperparameter
tuning was executed to optimise the model's performance, allowing it to capture complex relationships
within the data.

In addition to Random Forest Regression, a Gradient Boosting (GBoost) model was utilized for property
value prediction. GBoost sequentially builds decision trees to correct errors from previous iterations. The
model underwent training and fine-tuning to enhance its ability to capture intricate patterns within the
dataset.
The performance of both the Random Forest Regression and GBoost models was evaluated using standard
regression metrics, including Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared.
These metrics provided a comprehensive understanding of the models' ability to generalize to unseen data
and accurately predict property values.
