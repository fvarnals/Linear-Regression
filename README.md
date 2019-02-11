# Machine Learning-Linear Regression Exercise

#### <em>Implement linear regression with one variable to predict profits for a food truck. Given data of profits for each food truck and the population of the city they are in, we seek to predict whether a new city will return a good profit, based on its population.

<strong>[ex1data1.txt](https://github.com/fvarnals/Linear-Regression/blob/master/ex1data1.txt) contains our dataset, where the first column gives the population of a city and the second column gives the profit of a food truck in that city. A negative value for profit indicates a loss.

1) <strong>[plotData.m](https://github.com/fvarnals/Linear-Regression/blob/master/plotData.m) - Plot the data in our dataset:</strong><br>
<code>figure; % open a new figure window</code><br>
<code>plot(x,y,'rx','MarkerSize',10); %Plot the data</code><br>
<code>ylabel('Profit in $10,000s'); %Set the y-axis label</code><br>
<code>xlabel('Population of City in 10,000s'); %Set the x-axis label</code><br>
<img src="https://github.com/fvarnals/Linear-Regression/blob/master/Figure1.png" width=500 >

2) <strong>[computeCost.m](https://github.com/fvarnals/Linear-Regression/blob/master/computeCost.m) - Compute the cost of our linear regression model:</strong><br>

- We seek to calculate the cost (accuracy) of out model using the mean squared error, using the following function:<br>
<img src="https://github.com/fvarnals/Linear-Regression/blob/master/cost_function.png" width=300 >

- Where the hypothesis is given by the linear model:<br>
<img src="https://github.com/fvarnals/Linear-Regression/blob/master/hypothesis.png" width=300 ><br>

- Using the values of population size in 10,000s (<code>X</code>), and profit in $10,000s (<code>y</code>), we calculate the <code>cost</code> using initial theta values of <code>-1</code> and <code>2</code>.

3) <strong>[gradientDescent.m.m](https://github.com/fvarnals/Linear-Regression/blob/master/gradientDescent.m) - Function to run gradient descent:</strong><br>

- Having computed the cost function, we can now run gradient descent to find the Theta values which minimise the cost/error of our function, thereby giving better accuracy for out predictions of profit for a given population size.

- We calculate the <code>errors_vector</code> which gives us the error for each prediciton, i.e. for each datapoint we calculate the difference between predicted and actual profit:<br> 
<code>h = X * theta; %predicted profit</code><br>
<code>errors_vector = h - y;</code><br>

- We then use this to calculate the gradient of the cost with respect to our Theta values:<br>
<code>(X' * errors_vector)</code><br>

- And repeatedly take small steps in that direction, using the learning rate <code>alpha</code> to insure we do not overshoot and miss the minimum; moving down the gradient, to find the values of theta which give the minimum cost:<br>
<code>for iter = 1:num_iters</code><br>
<code>h = X * theta; %predicted profit</code><br>
<code>errors_vector = h - y;</code><br>
<code>theta_change = alpha * (1/m) * (X' * errors_vector); </code><br>
<code>theta = theta - theta_change;</code><br>


<em>computeCostMulti.m</em> - Cost function for multiple variables

<em>gradientDescentMulti.m</em> - Gradient descent for multiple variables

<em>featureNormalize.m</em> - Function to normalize features

<em>normalEqn.m</em> - Function to compute the normal equations

