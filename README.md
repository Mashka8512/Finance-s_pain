# Finance-s_pain
This is some simple code, which processes the time series of quotes and marke prediction of trend.
The main idea - convert time series to independent elements. At first, we need to smooth out a time series and split 
into sample elements. And after, we will predict trend with help KNN algorithm.

The main class name: Learner. 

Options:
 - k_neighbors - parameter of KNN algorithm, amount of nearest neighbors.
 - rolling_mean_window - smoothing ratio of real time series.
 - min_size - minimum of the element in sample.
 - eps  - limit for 'plato' state.
 - metrics:
  -'euclidean'
 Now there is only euclidean metrics. But in future, several other metrics will be added.

Thera are next functions:
* prepare_data(X) - where X is pandas.table object.
It convert time serie to independent elements. Return data, target (list object).
* fit_predict(X_train, y_train, X_test) - where all parametrs are numpy array.
Because KNN algorithm does not require, we can do predict at once. Return numpy array of predicted values.
* KNN_cross_validation(X, y) - where X, y - numpy array or list of prepared data and target.
Return (amount of right predicts) / (size of y).

