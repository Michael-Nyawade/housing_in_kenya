# **KENYAN HOUSING MARKET ANALYSIS**

<img src="https://github.com/Michael-Nyawade/housing_in_kenya/assets/157029652/6721ddfd-9966-44eb-84f1-68f1ad14c447" alt="housing" width="1000" height="400">


## **Project Overview** 

The Kenyan housing market is shaped by numerous factors. Among these factors, size and location emerge as key influencers. This project aims to explore these dynamics through Exploratory Data Analysis (EDA), to uncover the relative effects of size and location on housing prices.

## **Table of Contents**

- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Skills Demonstrated](#skills-demonstrated)
- [Data Source](#data-source)
- [Tools](#tools)
- [Data Cleaning](#data-cleaning)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Results](#results)
- [Recommendations](#recommendations)
- [Limitations](#limitations)

## **Problem Statement**

The location and size of properties are two of the several factors influencing the housing market in Kenya. Knowing how these factors relate to property prices becomes essential as investors, homeowners, and policymakers attempt to navigate this complex landscape. Through exploratory data analysis (EDA), this study seeks to close this gap. 

## **Skills Demonstrated**

1. **Data Manipulation with Python Pandas:** I effectively utilized the Pandas library to clean, transform, and analyze the housing dataset. From handling missing values to aggregating data, Pandas played a pivotal role in preparing the data for exploration.
2. **Data Visualization Using Matplotlib:** I leveraged Matplotlib to create insightful visualizations. Whether plotting price distributions, or bar charts, Matplotlib allowed me to communicate trends and patterns effectively.
3. **JupyterLab for Interactive Analysis:** JupyterLab served as my interactive workspace, enabling me to combine code, visualizations, and explanatory text seamlessly.

## **Data Source**
The dataset used for this analysis is sourced from [Kaggle](https://www.kaggle.com/datasets/iamasteriix/rental-apartments-in-kenya) and is provided in CSV format. It comprises several essential columns that are crucial for investigating housing prices in Kenya:
1. **Agency:** Denotes the agency responsible for listing the property.
2. **Neighborhood:** Represents the locality or neighborhood where the property is situated, providing insights into its geographical context.
3. **Price:** Indicates the monetary value associated with the property, serving as the primary target variable for our analysis.
4. **Link:** Contains hyperlinks or references to additional information related to the properties, offering a potential avenue for further exploration.
5. sq_mtrs: Reflects the size of the property in square meters, a critical determinant of its physical dimensions and potential utility.
6. **Bedrooms:** Specifies the number of bedrooms available within the property, providing insights into its accommodation capacity.
7. **Bathrooms:** Represents the count of bathrooms within the property, offering additional information on its amenities and functionality.

   ## **Tools**

* [Python Pandas](https://pandas.pydata.org/docs/user_guide/index.html)
* [Matplotlib](https://matplotlib.org/stable/users/index.html)
* [JupyterLab](https://jupyterlab.readthedocs.io/en/latest/user/index.html)

## **Data Cleaning**

During the data cleaning process, several essential activities were performed to prepare the dataset for analysis. Here’s an overview of the steps taken:

1. **Loading the Data:** The dataset was loaded into a Pandas DataFrame from a CSV file using the ```pd.read_csv()``` function.
2. **Initial Inspection:** I examined the first few rows of the DataFrame using ```housing_dataframe.head()``` and checked the data types and missing values with ```housing_dataframe.info()```.
3. **Handling Null Values:** Null values were observed in the dataset. To address this, I dropped rows containing null values using ```housing_dataframe.dropna(inplace=True)```.
4. **Column Modifications:**
  - **Dropping Columns:** I removed the `Link` and `Agency` columns as they were not relevant to the analysis.
  - **Creating a New Column:** A new column named `Estate` was created from the `Neighborhood` column to provide insights into the geographical context.
  - **Price Conversion:** The values in the `Price` column were converted to floating point numbers, and the column was renamed to `Price_Ksh`.
  - **Size Indicator:** Due to inconsistencies, the `sq_mtrs` column was dropped, with Bedrooms serving as a reliable size indicator.

## **Exploratory Data Analysis**

In the Exploratory Data Analysis section, I embark on a comprehensive exploration of the housing dataset. Here, I delve into descriptive statistics, uncovering key insights into the distribution and relationships among variables such as house prices, size, and location. Through visually informative plots and statistical analyses, I aim to gain a deeper understanding of the underlying patterns and trends within the data.

**Key Questions Addressed:**

1. How does the average house price compare across different Estates?
2. How do the average house prices vary across different categories of bedrooms (e.g., 1 bedroom, 2 bedrooms, etc.)?
3. How do the average house prices vary across different categories of bathrooms (e.g., 1 bathroom, 2 bathrooms, etc.)?
4. What is the distribution of house prices?

**Descriptive Statistics**

I started by computing descriptive statistics for numerical values such as house prices, bedrooms, and bathrooms, providing a foundational understanding of the dataset's characteristics.

|          |Price_Ksh|Bedrooms|Bathrooms|
|----------|---------|--------|----------|
|count|1557|	1557|	1557|
|mean|98339.75|	2.60|	2.60|
|std|40175.79|	0.81|	1.00|
|min|12000.00|	0.00|	1.00|
|25%|70000.00|	2.00|	2.00|
|50%|95000.00|	3.00|	2.00|
|75%|130000.00|	3.00|	3.00|
|max|240000.00|	6.00|	6.00|

**Distribution of Key Variables**

Visualizing the distribution of house prices, bedrooms, and bathrooms using box plots, revealing insights into the spread and central tendencies of these variables. Notably, the data suggests a prevalence of relatively high-priced properties and a trend towards larger, more spacious accommodations.

![distribution of key variables](https://github.com/Michael-Nyawade/housing_in_kenya/assets/157029652/417b13a7-303a-492f-9e7d-4cea52b90a76)

**Analysis by Estate**

Further analysis by estate highlights significant variations in average house prices, indicating disparities in property values across different localities. Desirable areas such as Westlands and Thika Road command higher prices, while more affordable options are available in estates like Kasarani and Kikuyu.

![analysis by estate](https://github.com/Michael-Nyawade/housing_in_kenya/assets/157029652/b344e3f7-2b45-45c0-a290-cc25036bd2a0)

**Impact of Bedrooms and Bathrooms**

Examining the relationship between house prices and the number of bedrooms or bathrooms reveals a positive correlation, with larger properties commanding higher prices. This underscores the importance of property size and configuration in determining market value within the housing sector, aligning with principles of supply and demand.

![bathrooms and bedrooms](https://github.com/Michael-Nyawade/housing_in_kenya/assets/157029652/091b9446-4a12-4041-ae61-c5b343d24b8c)

Overall, the exploratory analysis provides valuable insights into the dynamics of the Kenyan housing market, laying the groundwork for informed decision-making.

## **Results**

The analysis of the Kenyan housing market reveals clear trends, as evidenced by the boxplots and bar graph. Approximately half of the houses in the dataset are priced above Ksh. 100,000, indicating a prevalence of higher-value properties. This suggests a market inclination towards premium properties, possibly influenced by factors such as location or size. Moreover, properties with three or more bedrooms and two or more bathrooms are prominent, indicating a preference for larger accommodations. Notably, average house prices vary significantly across different estates, with some, like Westlands and Thika Road, commanding higher prices due to desirability, while others offer more affordable options. Additionally, the positive correlation between the number of bedrooms and bathrooms and the average house price highlights the influence of property size on market value, aligning with principles of supply and demand. These insights provide valuable context for understanding housing market dynamics in Kenya, offering guidance for both buyers and sellers in making informed decisions.

## **Recommendations**

Based on the analysis, the following recommendations are proposed:

1. **Consider Estate Selection:** Buyers should prioritize properties in estates with relatively lower average prices, such as Kasarani and Kikuyu, to optimize affordability and value for money.

2. **Emphasize Property Features:** Sellers should consider property features such as  additional bedrooms and bathrooms, as these attributes are positively associated with higher prices and may attract potential buyers.

3. **Address Affordable Housing Shortage:** Policymakers and urban planners should explore initiatives aimed at addressing the shortage of affordable housing. This could include incentivizing development in areas with lower property values or implementing policies to increase the supply of affordable housing units.

Implementing these recommendations can empower stakeholders to make strategic decisions that align with their objectives and preferences within the dynamic Kenyan real estate landscape.

## **Limitations**

Despite the insights gained from the analysis, it's essential to acknowledge several limitations of the project. Firstly, the findings are based on a single dataset sourced from Kaggle, which may not fully represent the diversity and complexity of the entire Kenyan housing market. Moreover, the study focuses primarily on variables such as price, size, and location, overlooking other factors that could influence housing market dynamics, such as economic conditions or cultural preferences. Considering these limitations is crucial for interpreting the results accurately and understanding their implications effectively.
