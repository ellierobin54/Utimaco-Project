# Utimaco - Improving Analytics Capabiliies
### Data X @ UC Berkeley - Fall 2020
### By Jae-Hee (Robin) Yoo, Lawrence Chang, Michael Deal, Anh-Tu Lu

This project was created in UC Berkeley's Data X (IND ENG 135) class for Utimaco in Fall 2020. The project showcases different time series forecasting models utilized on sample time series CPU utilization data. The program was developed with Python and its functionalities include gathering and cleaning data, training 4 different time series models on the sample data, and testing for errors in each model.

## Set Up

This project was developed using Python 3.5.2, Jupyter Notebook, and Google Colab. The packages utilized: numpy, pandas, matplotlib, sklearn, tensorflow, keras, fbprophet, pmdarima. Open the file 'Utimaco_Project.ipynb' to read and run each individual cell to compile and run the code.

## Data

The original sample dataset is ```machine_usage``` from:<br/>
https://github.com/alibaba/clusterdata/blob/master/cluster-trace-v2018/trace_2018.md. 
  
It has three variables: <br/>
  ```Timestamp```: Time in second <br/>
  ``` CPU % ``` : CPU in percentage<br/>
  ```Memory %```: Memory in percentage<br/>
  
We cleaned the data by removing the NA's and converting the Timestamp values to a datetime object. Due to its large size, we divided the sample data into 6 different sets (```data1```,```data2```,```data3```,```data4```,```data5```,```data6```). We then visualized each of the sets.

## Models

The models that we used were:
  1. *Triple Exponential Smoothing (Holt-Winter)*
  2. *SARIMA*
  3. *FB Prophet*
  4. *Long Short-Term Memory (LSTM) Recurrent Neural Network (RNN)*

For each of the 6 example dataset, we trained the model on 75% of the sets while the remaining 25% were used at test sets. We then calculated the root mean squared error (RMSE) on each of the results to see which model performs the best statistically. From our work, we found that the **LSTM** had the best performance in terms of achieving the smallest errors. 

## Product Implementation

To implement these models onto the u.trust360 platform, we recommend first generating a dataset of CPU usage from product usage. Then the team should upload the datasets onto the notebook provided and run the code provided to train and test the models. There might be adjustments needed to the models' parameters to fit the new sample data. 

## Next Steps

To implement the capacity function, create a cumulative function to add together the actual and predicted CPU usage outcomes. The program can notify the user of potential capacity when the cumulative data reaches 80%, 90%, or full capacity of HSM product. 

## News Release

You can view our sample press release here: <br/>
https://docs.google.com/document/d/12tpC1TapOLkOcyqBimZ5ln_Ju6pc-LKszKoEqjk-XqE/edit?usp=sharing

## Authorship

This project was made by 4 UC Berkeley seniors:

  - Jae-Hee (Robin) Yoo: ellierobin54@berkeley.edu 
  
  - Anh-Tu Lu: anhtulu@berkeley.edu 
  
  - Lawrence Chang: lchang23@berkeley.edu
  
  - Michael Deal: michaelpdeal@berkeley.edu
  
Please contact us for any questions or informations.



