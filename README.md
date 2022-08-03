# Recommendation System

This project is about building a recommendation system for spotify.

The task here is to predict the number of times a user will listen to an Artist.

The dataset given have the following features: UserID, artistID and weight (number of times the user have listened to the artist).

Another dataset given have the following features: userID and friendID (A user and his friend because it likely they listen to the same artist).

Then lastly the test set, it have two features (userID and artistID).

The logic applied here is to count the number of friends each user has, then an assumption is made that user with a lot of friends will influence their friends to listen to the same artist.

Also, the artist popularity matters, then to know an artist's popularity we can check the number of times an artist have been listened to by counting his appearance in the dataset.

These results were accumalated to dataframes for both the train set and test set.

Since we have quite a good amount of data, boxplots were made to check for outliers. The result is shown below.

![image](https://user-images.githubusercontent.com/104036386/182572932-8efd49c7-8442-4cf9-b718-4e3926317960.png)

The next thing done is to remove the outliers and the result is also shown below.

![image](https://user-images.githubusercontent.com/104036386/182573172-2fd9828d-afe1-4128-b09a-153125205ce3.png)

There isn't much difference, but this new plot is better than the previous one.

## Correlation
Looking at the correlation, there isn't much correlation between the weight and other features.The correlation matrix is shown below.

![image](https://user-images.githubusercontent.com/104036386/182573408-58c4b97b-e183-4089-833e-d7923ef6f737.png)

The data were scaled using sklearn standardscaler.

## Modeling.

The evaluation metric used in this case is mean absolute error and mean squared error.
The following model were used: Linear Regression, Decision Tree Regressor and Random Forest Regressor.

Out of the 3 models, the model with the least mean absolute error and mean squared error is Random Forest Regressor.

It is used as the final model for predicting the number of times a user will listen to an artist.
