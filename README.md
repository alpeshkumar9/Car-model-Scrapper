# Car-model-Scrapper
<h2>Regression Models Analysis on Scrapped Car Models data</h2>

An overview of the underlying research done for the various system components is provided in this section. As a result, it also provides a background on how the project evolved leading up to the system's creation.

<h3>General Idea</h3>
The main idea behind this project was to experiment with the car’s sales data and car’s specification data for predicting the future car sales based on various car’s features. The scrapping of the data from various online resources is done using a python library called “Beautifulsoup”[2]. Once all the car’s specification has been scrapped and collected in a csv file, it is merged with the sales data based on car make and model. After that various regression models are analysed and compared on the final dataset. For improving the performance of the models, techniques like Data Pre-processing, Feature Scaling and Principal Component Analysis (PCA) will be performed on the dataset. The model which shows the best prediction is chosen to predict future sales of the car.

<h3>Libraries Used</h3>
<ul>
  <li>Pandas</li>
  <li>Scikit-learn</li>
  <li>Matplotlib</li>
  <li>Seaborn</li>
  <li>Plotly</li>
  <li>Beautiful Soup</li>
 </ul>

<h3>Models Analysis Performed</h3>
<ol>
  <li>Principal Component Analysis (PCA)</li>
  <li>
    Regression Analysis
    <ul>
      <li>Linear Regression</li>
      <li>Polynomial Regression</li>
      <li>Ridge Regression</li>
      <li>Lasso Regression</li>
      <li>Random Forest Regression</li>
     </ul>
  </li>
</ol>

<h3>ComputationalExperiments</h3>
Objectives
This experiment aims to scrap the data from online resources, pre-process the scrapped data and use the final dataset to analyse & compare various regression models according to the performance criteria [2.5]. Furthermore, in this experiment, I will also highlight the prediction results of various regression models visually to find the best model which can be selected for future predictions on unknown test data.
