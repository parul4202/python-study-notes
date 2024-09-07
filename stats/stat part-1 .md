## to chech the variance 
>- ``` 
np.var(versicolor_petal_length) 

>> in terms of formula  - take the difference of each data point and substract to mean of the data points
> differences = versicolor_petal_length - np.mean(versicolor_petal_length)
> Square the differences: 
>- diff_sq = [x**2 for x in differences]
----------------------------------------------------------------------

## Covariance
>> __Covariance__ is a statistical tool used to determine the relationship between the movements of two random variables.
 > np.cov(x, y)
 >- returns a 2D array where entries [0,1] and [1,0] are the covariances. Entry [0,0] is the variance of the data in x, and entry [1,1] is the variance of the data in y.
 ----------------------------------------------------------------------

## Pearson correlation coefficient (r) 
>> is the most common way of measuring a linear correlation. It is a number between –1 and 1 that measures the strength and direction of the relationship between two variables.
> np.corrcoef(x, y)
----------------------------------------------------------------------

## Difference between covariance and Pearson correlation coefficient
>- Covariance measures the direction of the relationship, while the Pearson correlation coefficient measures the strength and direction of the relationship.
-----------------------------------------------------------------------

## statistical inference
>-  To draw probabilistic conclusions about what we might expect if we collected the same data again.To draw actionable conclusions from data.
To draw more general conclusions from relatively few data or observations.

## Generating random numbers using the np.random
>> rng.random()
>- eg = rng = np.random.default_rng(42) **always put seed number to generate the sample, also you can use the size = 5 __generated__ 5 random numbers by passing the keyword argument size=5**
 **Seed the random number generator**

than Initialize random numbers using something = np.empty(1000)
after that Generate random numbers by looping over range(1000) i.e. 

```
for i in range(1000):
    random_numbers[i] = rng.random() 
```

------------------------------------------------------------------------

## Bernoulli trial
In the theory of probability and statistics, a Bernoulli trial (or binomial trial) is a random experiment with exactly two possible outcomes, "success" and "failure", in which the probability of success is the same every time the experiment is conducted.
>> use the _rng.random() function_, which returns a random number between zero and one 
----------------------------------------------------------------------

## Probability mass function:
A PMF is defined as the set of probabilities of discrete outcomes. e.g **of a person rolling a die once. The outcomes are discrete because only certain values may be attained**

>- **Deference between pmf and cdf**
Probability mass functions (PMFs) and cumulative distribution functions (CDFs) are both related to the probabilities of random variables. PMFs assign probabilities to the possible values of a random variable, while CDFs provide a way to calculate many probabilities at once
>- PMF Calculates the probability that a discrete random variable will take a specific value. For example, a PMF can calculate the probability of there being exactly \(x\) successes from \(n\) independent trials.
>- CDF Calculates the probability that a random variable is less than or equal to a certain value. For example, a CDF can calculate the probability of there being at most \(x\) successes from \(n\) independent trials.
`````````````````````````````````````````````````````````

## The Binomial Distribution
>- The number of observations n is fixed.
>- Each observation is independent.
>- Each observation represents one of two outcomes ("success" or "failure").
>- The probability of "success" p is the same for each outcome.

```
variable = rng.binomial(n = value, p = value, size = any)
n_defaults = rng.binomial(n = 100, p = 0.05, size = 10000)

```
------------------------------------------------------------
## Poisson process
a process where certain events occur at a constant rate, but at random and independently of each other.

```
rng.poisson(10, size = 10000)

```
Then print the mean and std, and than Specify values of n and p to consider for Binomial ,p =  [20, 100, 1000], [0.5, 0.1, 0.01] 
using for loop extract the binomial sample.
------------------------------------------------

## Probability density functions
>- a function whose integral is calculated to find probabilities associated with a continuous random variable. it can see under the curve in graph. 
---------------------------------------------

## Normal Distribution 
Normal distribution, also known as the Gaussian distribution, is a probability distribution that appears as a "bell curve" when graphed. Here mean should be in the center of graph and standard deviation is a measure of how wide the peak is, or how spread out the data from the mean.
>- to draw the data we use rng.normal() which take two arguments e.g

```
samples_std1 = rng.normal(20, 1, size = 100000)

```
-------------------------------------------------

## The Exponential distribution: 
>- the waiting time between arrivals of a Poisson process are exponentially distributed. It has a single parameter, the mean waiting time. This distribution is not peaked.

```
 t1 = rng.exponential(tau1, size = size)

 ```
 -------------------------------------------------------
## Central limit theorem: 
>- which states that a sampling distribution will approach a normal distribution as the size of the sample increases.the sampling distribution became closer to the normal distribution as we took more and more sample means.
>- the central limit theorem only applies when samples are taken randomly and are independent
>- a sample size of at least 30 is required for the central limit theorem to apply.
#### Benefits of the central limit theorem
>>- The central limit theorem also comes in handy when we have a huge population and don't have the time or resources to collect data on everyone. Instead, we can collect smaller samples and create a sampling distribution to estimate summary statistics.

## experiement 
general workflow for hypothesis testing
 controlled,
 >- can be : controlled, treatment 
 >- where the treatment refers to the independent variable, and the response to the dependent variable.
## Randomization: why to use
To reduce bias, ensure groups are comparable, and increase the chances that results will be representative of the target population.
-------------------------------------

## general hypothesis testing workflow
* define population
* define the null hypothesis
* define the alterantive hypothesis
* collect the data 
* perform statistical tests on the sample data 
* draw conclusion about the population

-------------------------------------------------
## p-value
>- When drawing conclusions in hypothesis testing we use a metric called a p-value,We can visualize the p-value for our two sample mean distributions as the total area that overlaps between them
## Significance level ($\alpha$)
>- To reduce the risk of drawing a false conclusion
The overlap of distributions accounts for less than our threshold for alpha, 0.05
------------------------------------------------

## Type I/II error
We can wrongly reject our null hypothesis when it was actually true. This is known as a type one error.

## Type I/II error
We can wrongly accept our null hypothesis when it's false. This is known as a type two error.