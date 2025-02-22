# NYC Airbnb Data Cleaning Project

## Overview
This project demonstrates comprehensive data cleaning techniques using the Airbnb NYC 2019 dataset. The goal is to prepare the dataset for analysis by addressing various data quality issues including missing values, duplicates, and inconsistencies.

## Dataset Description
The dataset contains Airbnb listing information for New York City in 2019 with the following features:
- `id`: Listing ID
- `name`: Name of the listing
- `host_id`: Host ID
- `host_name`: Name of the host
- `neighbourhood_group`: Borough
- `neighbourhood`: Area within borough
- `latitude`: Latitude coordinates
- `longitude`: Longitude coordinates
- `room_type`: Type of room offered
- `price`: Price per night
- `minimum_nights`: Minimum nights required
- `number_of_reviews`: Number of reviews
- `last_review`: Date of last review
- `reviews_per_month`: Average reviews per month
- `calculated_host_listings_count`: Number of listings per host
- `availability_365`: Number of days available per year

## Data Cleaning Steps

### 1. Initial Data Assessment
- Check for missing values
- Identify duplicate records
- Examine data types
- Basic statistical analysis

### 2. Handling Missing Values
- `name` (16 missing): Fill with "Unnamed Listing"
- `host_name` (21 missing): Fill with "Anonymous Host"
- `last_review` (10052 missing): Fill with None
- `reviews_per_month` (10052 missing): Fill with 0

### 3. Data Standardization
- Convert `last_review` to datetime format
- Standardize neighborhood names
- Normalize price values
- Format text fields (names, descriptions)

### 4. Data Validation
- Ensure price values are positive
- Verify coordinate ranges
- Validate minimum_nights values
- Check availability_365 range (0-365)

### 5. Outlier Detection and Treatment
- Identify price outliers using IQR method
- Check for anomalous coordinate values
- Examine extreme values in minimum_nights
- Review unusual review counts

## Installation and Usage

```bash
# Clone the repository
git clone https://github.com/yourusername/nyc_airbnb_cleaning.git

# Navigate to project directory
cd nyc_airbnb_cleaning

# Install required packages
pip install -r requirements.txt

# Run data cleaning script
python src/cleaning_functions.py
```

## Key Metrics After Cleaning
- Total records: 48,895
- Missing values addressed: 20,141
- Duplicates removed: XX
- Outliers identified: XX
- Data consistency score: XX%

## Dependencies
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgments
- Dataset source: [Airbnb NYC 2019](http://data.insideairbnb.com/)
- Inside Airbnb for the original data collection
- NYC Open Data
