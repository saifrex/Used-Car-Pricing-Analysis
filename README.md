# WHAT DRIVES THE PRICE OF A CAR?

## OVERVIEW

In this application, you will explore a dataset from kaggle. The original dataset contained information on 3 million used cars. The provided dataset contains information on 426K cars to ensure speed of processing. Your goal is to understand what factors make a car more or less expensive. As a result of your analysis, you should provide clear recommendations to your client -- a used car dealership -- as to what consumers value in a used car.

  ### Input Dateset: https://github.com/saifrex/Used-Car-Pricing-Analysis/blob/main/data.zip

#### CRoss Industry Standard Process for Data Mining (CRISP-DM)
<img width="374" alt="crisp" src="../assets/crisp.png?raw=true">


## Deliverables
The deliverables for this analysis includes:

1. Exploratory data analysis: Use Python to analyze and visualize the data, exploring the different user car features
2. Report: Compile the findings into a brief report highlighting the key differences and correlations identified in the analysis.
3. Related code & data files: Publish relevant code in repository.

## Code: [Jupyter Car Analysis Notebook](/Car_Pricing_Analysis.ipynb)

## Data Exploration
 
#### Data Cleanup Results
- There are 426880 rows and 18 columns
- Out of the features 14 are string & 4 integer
- We have many null values across columns with size, cylinders, condition, VIN, drive, paint_color & type have significant values as null
- Year is a float.  We will convert this to integer
- VIN & Id is a unique value for each car and can therefore be dropped
- Price & Odometer columns have few values as 0

##### Original Data set - 

![Original_dataset](../assets/data_cleanup_required.png?raw=true)


##### After cleaning up and filling in other data our final data set was reduced - 

![Dataset_after_cleanup](../assets/data_cleanup_outcome.png?raw=true)


##### Used Cars Prices -
![Car_Prices_Histogram](../assets/used_car_prices.png?raw=true)

#### Models tried, evaluated, scoring, Feature Selection and Mean Squared errors summary capture
![Modeling_Residual_plot](../assets/residual_prediction_plot.png?raw=true)

![Modeling_Residual_plot_hist](../assets/residual_prediction_histogram.png?raw=true)

#### Prediction result & trend from the chosen model
![Choosen_model_prediction_vs_test_data_sample_for_the_client](../assets/model_prediction.png?raw=true)

## Conclusions

- Most single important feature that affects car price is manufactured Year. This alone contributes to over 25% to car price
- Other features that drives the car price in below order -
  - Odometer: 10%
  - model: 5%
  - cylinders: 4%
  - fuel: 3%
  - type: 1% 
  - condition: 1% 
  - drive: 1%
- More cylinder cars leads to higher prices
- Include Diesel cars in inventory
- All Wheel drive cars holds more value and priced higher

## Next Steps

 - Reduce usage of categories of 'other' or 'missing' by reclassifying them properly when possible
 - Correct bad data such as zero USD pricing or odometer readings in the billions
 - Rerun models of higher ranks
 - Attempt other type of models
 - Clearly note the rank of drive trains, number of cylinders and fuel types for their impact on price 
 - Include location data to explore how pricing vary based on state or city etc
 - Update this document as new findings are made

