# Machine Learning-Linear Regression Exercise

#### <em>Implement linear regression with one variable to predict profits for a food truck. Given data of profits for each food truck and the population of the city they are in, we seek to predict whether a new city will return a good profit, based on its population.

<strong>[ex1data1.txt](https://github.com/fvarnals/Linear-Regression/blob/master/ex1data1.txt) contains our dataset, where the first column gives the population of a city and the second column gives the profit of a food truck in that city. A negative value for profit indicates a loss.

1) <strong>[plotData.m](https://github.com/fvarnals/Linear-Regression/blob/master/plotData.m) - Plot the datain our dataset:</strong><br>
<code>figure; % open a new figure window</code><br>
<code>plot(x,y,'rx','MarkerSize',10); %Plot the data</code><br>
<code>ylabel('Profit in $10,000s'); %Set the y-axis label</code><br>
<code>xlabel('Population of City in 10,000s'); %Set the x-axis label</code><br>


<em>computeCost.m</em> - Function to compute the cost of linear regression

<em>gradientDescent.m</em> - Function to run gradient descent

<em>computeCostMulti.m</em> - Cost function for multiple variables

<em>gradientDescentMulti.m</em> - Gradient descent for multiple variables

<em>featureNormalize.m</em> - Function to normalize features

<em>normalEqn.m</em> - Function to compute the normal equations

