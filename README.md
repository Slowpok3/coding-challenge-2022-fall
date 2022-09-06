ACM Research Coding Challenge - Fall 2022

I created and trained a machine learning model to predict the prices of cars given various input features.

This was something that was completely new to me, so I had a lot of fun learning how to make these models and train them. The framework that I used to train my model is called Scikit Learn. I used their Decision Tree Regression model. I used a Regression Model primarily because it returned a continuous value, which seems reasonable as it is trying to predict the price of cars. Additionally, through some light research, I decided to use a decision tree because it can handle categorical data well. However, I still needed to process the categorical data.

When processing the data, I simply removed a lot of the columns that I felt did not really attrbute much to a car's price, such as VIN, Stock#, and Interior Color. Additionally, I removed a couple of columns which proved to be a hassle to process, such as Street Name, Seller Name, Engine. I also had to remove 2 rows because the Zipcode in those 2 rows were simply 'City'. I also had to extract the price values and remove a couple of rows that had cars with no price. After this, I looped through all of the values in the Used column and if it was 'New', I assigned it a value of 1 and if not, I assigned it a value of 0. For the rest of the categorical data, I used an Ordinal Encoder to encode them into float values. What this did was essentially assign each category a number between 1 - (number of unique categories-1). 

Lastly, I split the data into 80% training data and 20% testing data. I also split each set between features and labels. After doing this I managed to fit my model. Once my model was fitted, I ran the test data through it's predict method and I calculated the Mean Absolute Percent Error, which told me how accurate my model was. My model seems to be somewhat accurate, as it has a MAPE of 0.1277.

If I had more time on the project, I would have spent a lot more time researching on the best machine learning model given this dataset. I would have also spent a lot of time figuring out how to process the data more effectively, and process the data that I had to leave out. 
