# Car-model-Scrapper
<h2>Regression Models Analysis on Scrapped Car Models data</h2>

An overview of the underlying research done for the various system components is provided in this section. As a result, it also provides a background on how the project evolved leading up to the system's creation.

<h3>General Idea</h3>
The main idea behind this project was to experiment with the car’s sales data and car’s specification data for predicting the future car sales based on various car’s features. The scrapping of the data from various online resources is done using a python library called <b>“Beautifulsoup”$\color{DodgerBlue}{\textrm{“Beautifulsoup”}}$</b>. Once all the car’s specification has been scrapped and collected in a csv file, it is merged with the sales data based on car make and model. After that various regression models are analysed and compared on the final dataset. For improving the performance of the models, techniques like Data Pre-processing, Feature Scaling and Principal Component Analysis (PCA) will be performed on the dataset. The model which shows the best prediction is chosen to predict future sales of the car.

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
Objectives: 
This experiment aims to scrap the data from online resources, pre-process the scrapped data and use the final dataset to analyse & compare various regression models according to the performance criteria [2.5]. Furthermore, in this experiment, I will also highlight the prediction results of various regression models visually to find the best model which can be selected for future predictions on unknown test data.

<h3>Models Analysis</h3>
<ol>
  <li>Splitting the dataset: Using the train_test_slit function in sklearn to split the pre-processes dataset, generated in section 3.4, into a training set and test set. Training set will be used to train the model and a Test set to evaluate the model.
26
I have set test_size = 0.3, so 1/3 of the data will be used as Test set. I have also set the random_state parameter to one. This requests a random sampling of the data but ensures we can always get the same random sampling if we rerun the experiment. When I tweak the model, it ensures that any changes are due to the tweaking, and not to the random sampling being different. To verify, I looked at the samples produced and confirmed the randomness of the selection.
</li>
  <li>Train the Model: Now, it was time to train some prediction models using the split dataset. I studied a wide range of regression machine learning algorithms for this project, but I have selected only Linear Regression, Ridge Regression, Lasso and Random Forest for analysis purpose.
• I created an object for each of the regression model using the sklearn functions in python.
• The regressor is trained using 𝑥𝑡𝑟𝑎𝑖𝑛 data. This is also known as fitting. I passed the feature matrix and
corresponding response vector.
    </li>
  <li>
    Evaluate performance criteria of models: Now, here I evaluated the models using the performance criteria, mentioned in Section 2, by comparing actual output and predicted output. As I was analysing more than one model so I created a common function 𝑚𝑜𝑑𝑒𝑙_𝑝𝑒𝑟𝑓𝑜𝑟𝑚𝑎𝑛𝑐𝑒() to use it for all the models.
  </li>
</ol>

<h3>Results</h3>
In this analysis, I used four regression algorithms and considered key factors related with each of the technique. The analysis provides evidence that:

<ul>
  <li>In basic model analysis, all other models performed better than random forest. As I mentioned earlier, if two models have similar performance then one should favour the model that is simpler and/or easier to grasp because the simpler model is easier for others to understand so.</li>
  <li>Feature selection gave poor performance and did not provide any improvement over basic model analysis.</li>
  <li>Using PCA as the dimensionality reduction technique provided the best result for all the models compared to basic model analysis. Also, Machine learning pipelining helped in automating the iterative process of scaling, applying PCA and building estimators and thus reducing the overall computation time.</li>
 </ul>
     
<h3>Conclusions</h3>
Regression analysis is a robust and practical statistical technique with numerous applications in research. Researchers can use it to explain, forecast, estimate, and draw reasonable conclusions about the connected factors in respect to any researched phenomenon. When scientists want to look at how certain factors relate to one another, regression also enables controlling one or more variables. Regression analysis should be planned and carried out with the type, number, and sample size of dependent and independent variables all taken into account. With a limited sample size, choosing the incorrect regression analysis method could lead to incorrect conclusions regarding the phenomenon being examined.

During this research study, I have analysed and compared various regression-based models considering all these important factors. The data for this project was scraped from various online websites using Beautifulsoup python library. The scrapped dataset was merged with car’s sales dataset and was refined using various python libraries to make it suitable for model analysis. As a result, the final dataset contains 43047 rows and 21 attributes. To test the result, linear regression, ridge regression, lasso and random forest regression was performed on the processed dataset.

The same processed dataset was used to assess the models. The criteria for comparing the results were the MSE, RMSE, MAE and R-squared. In all the type of analysis, there was tie between linear and ridge regression, however, based on MAE value overall Ridge regression produced the best results and whose R2 value was only 0.92 in basic and feature scale model analysis and increased to 0.98 when PCA was performed on the data. As a result, I came to the conclusion that Ridge regression can be used to create the sales evaluation model.

This project work can be used to improve future work by fine tuning each model parameter. Better data engineering can be used for building better training data. These models can also be used in real-life practical applications.
