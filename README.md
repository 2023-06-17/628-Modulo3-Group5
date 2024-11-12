# Fall24-STAT628-Module3-Group5: Holiday Season Flight Prediction Project

## Authors 
- Chenghao Lou 
- Ruiyuan Ming 
- Minliang Yu 
- Shixin Zhang

(in alphabetical order) 


## Overview
This project aims to analyze historical flight and weather data to predict flight delays and cancellations during the holiday period. Additionally, we aim to provide actionable travel tips for passengers to help them avoid cancellations and improve their chances of arriving on time.



## Repository Structure
- `data/`: Contains the raw and cleaned datasets used in the analysis.
- `code/`: Includes all codes used for data cleaning, analysis, and model building.
- `plots/`: Stores plots and visualizations generated during the analysis.
- `shiny/`: The code for the Shiny app, allowing real-time body fat predictions.
  
## Additional Resources

Due to the structure of this repo and the upload limit for certain files on GitHub, some other files are stored in our shared drive, including initial weather data, flight data, some merged datasets, and lots of other helper code files. Feel free to request access to our shared drives to check out.
[https://drive.google.com/drive/folders/0AOnlxgAvrj23Uk9PVA] - main drive
[https://drive.google.com/drive/folders/0APEShnaw2EpMUk9PVA] - backup1 drive 
[https://drive.google.com/drive/folders/0AK6d3vWligJlUk9PVA] - backup2 drive


## Statistical Analysis
The prediction task was divided into two primary models: one for predicting flight cancellations (binary classification) and another for predicting arrival delay times (regression). Both models used XGBoost due to its efficiency with large datasets, ability to handle data imbalance, and support for feature importance analysis. 

For Cancellation Prediction Model: The target variable for this model was CANCELLED, where 0 represents non-canceled flights, and 1 represents canceled flights. Predictive features included various categorical variables, which were encoded, and numeric variables such as weather and time-based metrics. 

For Arrival Delay Prediction Model: The target variable was ARR_DELAY, which represents the arrival delay in minutes. This model used the same feature set as the cancellation model and aimed to predict the delay time for non-canceled flights.

## Shiny App
The repository includes a Shiny web app that allows users to input their flight date, flight number, departing airport, arrival airport, and operating flight number. User will receive real-time predictions of whether their flight is likely to be canceled, and if not, the estimated arrival time. If the user is retrieving predictions for past dates, the system will also look for historical weather and use for prediction if found. The app uses trained models for prediction. The app also shows an interactive map, great circle distance and weather information(if available). To run this shiny app, download all files in the shiny folder and type in the command line:
  ```bash
  shiny run --app-dir /path-to-your-folder
  ```

The Shiny app is also deployed to an online platform and can be accessed here:
[https://connect.posit.cloud/szhang655/content/0193176a-818a-32e5-37d9-ca920e9e3bf6]
Please note that historical weather data feature is not supported by the online version, the source for the online version is [https://github.com/szhang655/FlightSchedulePredictionShiny.git].


## Contact
If you have any questions or issues regarding the analysis or the app, feel free to contact us:

  Email: clou25@wisc.edu, rming@wisc.edu, myu259@wisc.edu, szhang655@wisc.edu

 
**Special Thanks to Professor Kang**

