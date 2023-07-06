# Analyzing Factors Affecting Home Ownership Prices in King County 
# Overview 
By leveraging data analysis techniques, my project aims to revolutionize the homeownership experience for our stakeholders. Through strategic insights and recommendations, I strive to empower homeowners and real estate investors with the knowledge and tools necessary to make informed decisions, maximize returns on investments, and unlock the full potential of their real estate assets. My ultimate goal is to establish Microsoft as a leader in the real estate industry by delivering innovative solutions and setting new standards in the realm of homeownership and property investment.
# Business Problem
The aim of this project is to analyze the relationship between home ownership prices and various factors that can influence those prices in King County. By leveraging the King County House Sales dataset, we seek to provide valuable insights to homeowners and real estate investors. The primary goal is to conduct predictive analysis and identify key factors that impact home prices. This analysis will help stakeholders make informed decisions regarding potential upgrades and improvements to maximize the value of their properties.
# Stakeholder and Key Business Questions
1) How can we optimize the homeownership experience for our stakeholders by identifying key factors that contribute to property value appreciation and market demand?
2) What are the most attractive neighborhoods or locations for real estate investment, based on market trends, amenities, and potential for future growth?
3) How can we enhance the efficiency and effectiveness of the property purchasing process for homeowners, providing them with a seamless and streamlined experience?
# Data Understanding 
The dataset was obtained from Kings County housing dataset contained in the CSV file kc_house_data.csv.                                                           
The file contains information on 21597 housing units. The data is organized into a table with several columns containing different information about the houses.

The following are the columns contained in the dataset along with their descriptions:
id - Unique identifier for a house                                                                                                                                 
date - Date house was sold                                                                                                                                        
price - Sale price (prediction target)                                                                                                                             
bedrooms - Number of bedrooms                                                                                                                                      
bathrooms - Number of bathrooms                                                                                                                                    
sqft_living - Square footage of living space in the home                                                                                                           
sqft_lot - Square footage of the lot                                                                                                                              
floors - Number of floors (levels) in house                                                                                                                        
waterfront - Whether the house is on a waterfront                                                                                                                 
view - Quality of view from house                                                                                                                                 
condition - How good the overall condition of the house is. Related to maintenance of house.                                                                       
See the https://info.kingcounty.gov/assessor/esales/Glossary.aspx?type=r#g Website for further explanation of each condition code                                   
grade - Overall grade of the house. Related to the construction and design of the house.                                                                           
See the https://info.kingcounty.gov/assessor/esales/Glossary.aspx?type=r#g Website for further explanation of each building grade code                              
sqft_above - Square footage of house apart from basement                                                                                                           
sqft_basement - Square footage of the basement                                                                                                                    
yr_built - Year when house was built                                                                                                                              
yr_renovated - Year when house was renovated                                                                                                                      
zipcode - ZIP Code used by the United States Postal Service                                                                                                        
lat - Latitude coordinate                                                                                                                                          
long - Longitude coordinate                                                                                                                                         
sqft_living15 - The square footage of interior housing living space for the nearest 15 neighbors                                                                  
sqft_lot15 - The square footage of the land lots of the nearest 15 neighbors                                                                                       
# Modeling
I developed a linear regression model to predict house values based on the features. The dependent variable in the linear model was price of the house and the independent variables were bedrooms, bathrooms, sqft_living, sqft_lot, floors, condition, age in year, is_renovated and grade. Several features were dropped in the statistical analysis ie date, view, sqft_basement, sqft_above, waterfront, zipcode, lat, long, sqft_living15, sqft_lot15, id. In my opinion the locations where single family homes are to be developed have already been purchased, so the features pertaining to location were not used in this analysis, they included zipcode, lat, long, waterfront, and view. Identity features were deemed irrelevant to the analysis (date, id) and to avoid multicollinearity similar columns were dropped.
# Results
![ModelThreeFittedValues](https://github.com/Wendy0001/EndofP2/assets/132939772/c59a399e-30fd-40ea-9264-29b36f63db2a)
After conducting several iterations, the final linear regression model was obtained by performing a logarithmic transformation on the dependent variable, price. This transformation was applied to align the dataset with the assumptions of linearity. The model achieved an R-squared value of 63.5%, indicating that 63.5% of the variance in the price of the house can be explained by the linear regression model. Furthermore, the model exhibited an error of USD 260,920 when predicting house prices.
![output](https://github.com/Wendy0001/EndofP2/assets/132939772/a81aefa7-6053-41fe-b0d5-07388c873944)
![outp![output2](https://github.com/Wendy0001/EndofP2/assets/132939772/6bcaa960-14cd-4281-9bb8-35136e00e04c)
![output2](https://github.com/Wendy0001/EndofP2/assets/132939772/55b66011-3263-4249-b009-ca7fcb7fdab8)




