# **AIRBNB DATA ANALYSIS**

![](https://github.com/aayushmanmukherjee/Airbnb_Data_Analysis_EDA/blob/main/images/airbnb.jpeg)

## **Overview**

Exploratory Data Analysis (EDA) on New York Airbnb data to uncover trends and patterns in rental listings.

## **Tools Used**
- Python
- Jupyter notebook
- Pandas
- Matplotlib
- Seaborn

## **Objectives**

- Analyze room types, prices, and availability across different neighborhoods.
- Understand listing patterns.
- Detect potential outliers in prices.
- Provide recommendations for guests and hosts based on insights.

## **Dataset**

The dataset contains 20,765 entries and 22 features, including:

- id: Unique identifier for each listing
- name: Title of the Airbnb listing
- host_name: Name of the host
- neighborhood_group: Group (borough) where the listing is located
- latitude/longitude: Geolocation of listings
- price: Nightly rental price
- room_type: Type of accommodation (e.g., entire home, private room)
- number_of_reviews: Total reviews for the listing
- availability_365: Number of available days in the year
- rating - Average rating out of 5 for the listings

## Steps and Workflow

### 1. Data Cleaning
- Dealing with null values in the dataset
- Dealing with duplicate rows in the dataset
- Removing price column outliers (>$1000)
- Cleaning rating column

### 2. EDA (Exploratory Data Analysis)

1. Price distribution:

![](https://github.com/aayushmanmukherjee/Airbnb_Data_Analysis_EDA/blob/main/images/price_dist.png)

   - Majority of the listings were priced between $50 - $200.

2. 365 days availability distribution:

![](https://github.com/aayushmanmukherjee/Airbnb_Data_Analysis_EDA/blob/main/images/365_days_dist.png)

   - We can see maximum listings are available for 365 days of the year.

3. Average price in each neighbourhood groups:

   - Neighbourhood group: Bronx, average price: $107.05
   - Neighbourhood group: Brooklyn, average price: $153.24
   - Neighbourhood group: Manhattan, average price: $193.29
   - Neighbourhood group: Queens, average price: $120.89
   - Neighbourhood group: Staten Island, average price: $115.74

4. Average price per bed in each neighbourhood groups:

   - Neighbourhood group: Bronx, average price: $73.74
   - Neighbourhood group: Brooklyn, average price: $98.84
   - Neighbourhood group: Manhattan, average price: $133.76
   - Neighbourhood group: Queens, average price: $76.10
   - Neighbourhood group: Staten Island, average price: $67.27

5. Price dependency on neighbourhood and room type:

![](https://github.com/aayushmanmukherjee/Airbnb_Data_Analysis_EDA/blob/main/images/price_neighbour_room.png)

   - Manhattan is the most expensive
   - Entire home/apartment is consistently the costliest room type
   - Bronx and Staten Island are comparatively cheaper

6. Relation between Price and Popularity score:

![](https://github.com/aayushmanmukherjee/Airbnb_Data_Analysis_EDA/blob/main/images/price_popularity.png)

   - Higher popularity score does not necessarily mean higher price.
   - Majority of listings have popularity scores below 2000.
   - Expensive listings (above 500) appear mostly at lower popularity levels.

7. Geographical Distribution of Airbnb Listing for each room type

![](https://github.com/aayushmanmukherjee/Airbnb_Data_Analysis_EDA/blob/main/images/geographical_distribution.png)

   - Manhattan has the highest listing density, followed by Brooklyn
   - Entire home/apartment dominates
   - Queens and Bronx have fewer listings
   - Hotel and shared rooms are rare

8. Price–Demand–Quality relationships

![](https://github.com/aayushmanmukherjee/Airbnb_Data_Analysis_EDA/blob/main/images/cluster.png)

   - Rating has a weak positive correlation with popularity and reviews
   - Price, minimum nights, and availability show almost no correlation with other variables

## Key Findings and Insights

- Price Trends:

    - Manhattan has the most expensive listings, followed by Brooklyn.
    - Entire homes/apartments cost significantly more than private or shared rooms.

- Room Type Distribution:

    - Entire homes/apartments are the most common, but private rooms offer budget-friendly options.

- Outliers in Price:

    - Few listings priced at $10,000+ were detected, indicating the need to filter such extreme values.

- Availability Patterns:

    - Listings with high availability tend to have lower prices and more reviews, likely due to better guest experience.

## Future work

- Use machine learning to predict prices based on room type and location.
- Perform sentiment analysis on reviews to better understand guest experiences.
- Create an interactive dashboard using business intelligence tools.

## Conclusion
This project offers valuable insights into the New York Airbnb market, helping both guests and hosts make informed decisions. By using EDA techniques, we identified key trends and developed actionable recommendations. Future improvements can involve advanced analytics and predictive modeling to further enhance the findings.

## How to Clone This Project

1. Run the following code in your computer's command line interface:
   ```bash
   git clone https://github.com/aayushmanmukherjee/Airbnb_Data_Analysis_EDA.git
   ```
2. Create a virtual environment in the project's folder and install the required libraries:
   - For Mac/Linux
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   pip install numpy pandas matplotlib seaborn plotly scipy
   ```
   - For Windows
   ```bash
   python3 -m venv .venv
   .venv\Scripts\activate
   pip install numpy pandas matplotlib seaborn plotly scipy
   ```
   
3. Run the **Jupyter notebook** or **Python script**:
  
- [Dataset link](https://github.com/aayushmanmukherjee/Airbnb_Data_Analysis_EDA/blob/main/datasets.csv)  
- [EDA jupyter notebook link](https://github.com/aayushmanmukherjee/Airbnb_Data_Analysis_EDA/blob/main/eda.ipynb)  
