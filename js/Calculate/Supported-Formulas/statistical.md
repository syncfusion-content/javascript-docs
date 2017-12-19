---
layout: post
title: Supported Formulas of Calculate for Syncfusion Essential JS
description: supported formulas
platform: JS
control: Calculate
documentation: ug
---

# Statistical



## AVEDEV



Returns the average of the absolute mean deviations of data points. `Avedev` is a measure of the variability in a data set.



**Syntax**



_AVEDEV(number1, number2, ...)_



**where:**



* number1, number2, ... are arguments for which you want the average of the absolute deviations. You can also use a single array or a reference to an array instead of arguments separated by commas.



**Remarks:**



* The arguments must either be numbers or names, arrays or references that contain numbers.



* If an array or reference argument contains text, logical values or empty cells, those values are ignored; however, cells with the a zero value are included.



## AVERAGE



Returns the average (arithmetic mean) of the arguments.



**Syntax**



_AVERAGE(number1, number2, ...)_ 



**where:** 

* number1, number2, ... are numeric arguments for which you want the average.



**Remarks:**



* The arguments must either be numbers or names, arrays or references that contain numbers.



* If an array or reference argument contains text, logical values, or empty cells, those values are ignored; however, cells with zero value are included.



## AVERAGEA



Calculates the average (arithmetic mean) of the values in the list of arguments. In addition to numbers and text  logical values such as True and False are also included in the calculation.



**Syntax:**



_AVERAGEA(value1, value2,...)_



**where:**



* value1, value2, ... are cells, ranges of cells, or values for which you want the average.



**Remarks:**



* The arguments must be numbers, names, arrays, or references.



* Array or reference arguments that contain text evaluate as 0 (zero). If the calculation should not include text values in the average, then use the `AVERAGE` function.



* Arguments that contain `True` evaluate as 1; arguments that contain `False` evaluate as 0 (zero).



## AVERAGEIF



The `AVERAGEIF` function returns the average of the cells in a specified range which satisfies the given criteria.



**Syntax:**



_AVERAGEIF(range, criteria, [average_range])_



**where:**



* range is the cells range to calculate the average value.



* criteria are the condition to calculate the average.



* average_range is the range optional cells range to computed average. If the average is not included, then the range is used for the average.



## AVERAGEIFS



The `AVERAGEIFS` returns the average of the cells in a specified range which satisfies the given multiple criteria.



**Syntax:**



_AVERAGEIFS(average_range, criteria_range1, criteria1, [criteria_range2, criteria2], ...)_



**where:**



* average_range is the range of cells to calculate the average.



* criteria_range1 is the first range to calculate the average.



* criteria_ is the optional cells range to evaluate the average.



* criteria1 is the first condition for the first criteria range.



* criteria2 is the optional condition for the criteria range 2.



## BINOM.DIST



The `Binom.Dist` function returns the Binomial Distribution probability for a given number of successes from a specified number of trials. 



**Syntax:**



_BINOM.DIST (trial number,sp,value, cumulative)_



**where:**



* trial number is the number of Bernoulli trials.



* sp is the probability of a success on each trial.



* value is the criterion value. 



* cumulative is a logical value that determines the form of the function.



**Remarks:**



* `#NUM!` occurs when trial number is lesser than zero, when sp and value are lesser than zero or greater than one.



* `#VALUE!` occurs when trials, sp, and value are non-numeric.



## BINOM.INV



The `Binom.Inv` function returns the smallest value for which the cumulative binomial distribution is greater than or equal to a criterion value.



**Syntax:**



_BINOM.INV(trial number,sp,value)_



**Where:**



* trial number is the number of Bernoulli trials.



* sp is the probability of a success on each trial.



* value is the criterion value.



**Remarks:**



* `#NUM!` - occurs if trial number is less than zero, if sp and value is less than zero or greater one.



* `#VALUE!` - occurs if trials, sp and value are non-numeric.



## CHIDIST



The `CHIDIST` function returns the right-tailed probability of the chi-squared distribution. 



**Syntax:**



_CHIDIST(x,degFreedom)_



**Where:**



* X is the value at which the chi-square distribution is to be evaluated (must be ≥ 0).



* degFreedom is the number of degrees of freedom.



**Remarks:**



* `#NUM!` - occurs if the  x is negative or degFreedom argument is invalid.



## CONFIDENCE.NORM



The `Confidence.Norm` function uses [Normal Distribution](http://en.wikipedia.org/wiki/Normal_distribution) to calculate a confidence value that can be used to construct the confidence interval for a population mean, for a supplied probability, and sample size.



**Syntax:**



_CONFIDENCE.NORM(alpha,stdev,size)_



**where:**



* alpha is the significance level.



* stdev is the population standard deviation for the data range.



* size is the sample size. 



**Remarks:**



* `#VALUE!` occurs when any argument is non-numeric.



* `#NUM!` occurs when alpha and stdev is lesser than or equal to zero or when alpha is greater than or equal to zero.



* `#DIV/0!` occurs when the size is equal to one.



##  CHISQ.INV



The `Chisq.Inv` function returns the inverse of the left-tailed probability of the chi-squared distribution.



**Syntax:**



_CHISQ.INV(probability,degFreedom)_



**where:**



* probability is a probability of chi-squared distribution.



* deg_freedom is the number of degrees of freedom.



**Remarks:**



* `#NUM!` occurs when probability is lesser than zero, when probability is greater than 1, and degFreedom is lesser than 1.



* `#VALUE!` occurs when probability or degFreedom is non-numeric.



## CHISQ.INV.RT



The `Chisq.Inv.Rt` function calculates the inverse of the right-tailed probability of the [chi-square distribution](http://en.wikipedia.org/wiki/Chi-square_distribution).



**Syntax:**



_CHISQ.INV.RT(probability, degFreedom)_



**where:**



* probability is a probability of chi-squared distribution.



* degFreedom is the number of degrees of freedom.



**Remarks:**



* `#NUM!` occurs when probability is lesser than zero, when probability is greater than 1, and when degFreedom is lesser than 1.



* `#VALUE!` occurs when probability or degFreedom is non-numeric. 



## CHISQ.DIST.RT



The `Chisq.Dist.Rt` function calculates the right-tailed probability of the [chi-square distribution](http://en.wikipedia.org/wiki/Chi-square_distribution).



**Syntax:**



_CHISQ.DIST.RT(x,degFreedom)_ 



**where:**



* x is the value that evaluates the function.



* degFreedom is the number of degrees of freedom.



**Remarks:**



* `#VALUE!` occurs when either argument is non-numeric.



* `#VALUE!` occurs when any argument is non-numeric.



* `#NUM!` occurs when f degFreedom < 1 or degFreedom >10^10.



## CHISQ.DIST



The `Chisq.Dist` function calculates the Probability Density Function or the Cumulative Distribution Function for the chi-square distribution.



**Syntax:**



_CHISQ.DIST(x,degFreedom,cumulative)_ 



**where:**



* x is the value that evaluates the function.



* degFreedom is the number of degrees of freedom.



* cumulative is a logical value that determines the form of the function.



**Remarks:**



* `#VALUE!` - occurs if any argument is non-numeric.



* `#NUM!` - occurs if x is negative and if f degFreedom < 1 or degFreedom >10^10.



## CORREL



The `Correl` function returns the correlation coefficient of the array1 and array2 cell ranges.



**Syntax:**



_CORREL(array1, array2)_



**where:**



* array1 is a cell range of values.



* array2 is the second cell range of values.



**Remarks:**



* array1 and array2 must have the same number of data points.



## COUNT



The `Count` counts the number of items in a list that contains numbers.



**Syntax:**



_COUNT(value1, value2,...)_



**where:**



value1, value2, ... are arguments that can contain or refer to a variety of different types of data, but only numbers are counted.



**Remarks:**



* Arguments that are numbers, dates or text representations of numbers are counted; arguments that are error values or text that cannot be translated into numbers are ignored.



* If an argument is an array or reference, only numbers in that array or reference are counted. Empty cells, logical values, text or error values in the array or reference are ignored.



## COUNTA



The `CountA` counts the number of cells that are not empty.



**Syntax:**



_COUNTA(value1, value2,...)_



**where:**



* value1, value2, ... are arguments representing the values you want to count. In this case, a value is any type of information, excluding empty cells.



## COUNTBlank



The `CountBlank` counts empty cells in a specified range of cells.



**Syntax:**



_COUNTBLANK(range)_



**where:**



range is the range from which you want to count the blank cells.



**Remarks:**



* Cells with formulas that return "" (empty text) are also counted. Cells with zero values are not counted.



## COUNTIF



Returns the number of cells (of a supplied range), that satisfy a given criteria.



**Syntax:**



_COUNTIF (range, criteria)_



**where:**



* range is the range of cells to count.



* criteria is the criteria that controls which cells should be counted.



## DEVSQ



The `DevSQ` returns the sum of squares of deviations of data points from their sample mean.



**Syntax:**



_DEVSQ(number1, number2,...)_



**where:**



* number1, number2, ... are arguments for which, you want to calculate the sum of squared deviations. You can also use a single array or a reference to an array instead of arguments separated by commas.



**Remarks:**



* The arguments must be numbers or names, arrays or references that contain numbers.



## EXPON.DIST



The `Expon.Dist` function calculates the value of the probability density function or the cumulative distribution function for the **Exponential Distribution**.



**Syntax:**



_EXPON.DIST(x,y,cumulative)_



**where:**



* x is the value that evaluates the function.



* y is the parameter value.



* cumulative is a logical value for given function.



**Remarks:**



* `#NUM!` occurs when x is lesser than zero and y is equal to or lesser than zero. 



* `#VALUE!` occurs when x or y is non-numeric.



## F.DIST 



The `F.Dist` function calculates the Probability Density Function or the Cumulative Distribution Function for the **F Distribution**.



**Syntax:**



_F.DIST(x,degFreedom1,degFreedom2,cumulative)_ 



**where:**



* x is the value that evaluates the function.



* degFreedom1 is the numerator degree of freedom.



* degFreedom1 is the denominator degree of freedom. 



* cumulative is a logical value that determines the form of the function.



**Remarks:**



* `#VALUE!` occurs when any argument is non-numeric.



* `#NUM!` occurs when x is negative, when degFreedom1< 1 and when degFreedom1< 1



## F.DIST.RT



The `F.Dist.Rt` function calculates the F Probability Distribution that measures the degree of diversity between two data sets.



**Syntax:**



_F.DIST.RT(x, degFreedom1, degFreedom2)_ 



**where:**



* x is the value that evaluates the function.



* degFreedom1 is the numerator degree of freedom.



* DegFreedom2 is the denominator degree of freedom. 



**Remarks:**



* `#VALUE!` occurs when any argument is non-numeric.



* `#NUM!` occurs when x is negative, when degFreedom1< 1 and  when degFreedom2< 1.



## F.INV.RT



The `F.INV.RT` function calculates the inverse of the Cumulative F Distribution for a supplied probability.



**Syntax:**



_F.INV.RT(probability,degFreedom1,degFreedom2)_



**where:**



* probability is a probability that corresponds to the normal distribution.



* degFreedom1 is the numerator degrees of freedom.



* degFreedom2 is the denominator degrees of freedom.



**Remarks:**



* `#NUM!` occurs when probability is equal to or lesser than zero and when probability is equal to or greater than one.



* `#VALUE!` occurs when probability or degFreedom1 or degFreedom2 is non-numeric.



## FISHER



The `Fisher` returns the Fisher transformation at x. This transformation produces a function that is normally distributed rather than skewed.



**Syntax:**



_FISHER(x)_ 



**where:**



* x is a numeric value for which you want the transformation.



**Remarks:**



* X must be > -1 and < 1.



## FISHERInv



The `FisherInv` returns the inverse of the Fisher transformation. If y = FISHER(x), then FISHERINV(y) = x.



**Syntax:**



_FISHERINV(y)_



**where:**



* y is the value for which you want to perform the inverse of the transformation.



## FORECAST



The `Forecast` calculates a future value by using existing values in a linear regression. The predicted value is a y-value for a given x-value.



**Syntax:**



_FORECAST(x, known_ys, known_xs)_



**where:**



* x is the data point for which you want to predict a value.



* known_ys is the dependent array or range of data.



* known_xs is the independent array or range of data.



## F.DIST.RT



The `F.DIST.RT` function calculates the F Probability Distribution, which measures the degree of diversity between two data sets.



**Syntax:**



_F.DIST.RT(x, degFreedom1, degFreedom2)_



**where:**

* x is the value that evaluates the function.



* degFreedom1 is the numerator degrees of freedom.



* DegFreedom2 is the denominator degrees of freedom.



**Remarks:**



* `#VALUE!` occurs if any argument is non-numeric.



* `#NUM!` occurs if x is negative, if degFreedom1< 1 and  if degFreedom2< 1



## GEOMEAN



The `Geomean` returns the geometric mean of an array or range of positive data.



**Syntax:**



_GEOMEAN(number1, number2,...)_



**where:**



* number1, number2, ... are arguments for which you want to calculate the mean.



**Remarks:**



* The arguments must be either numbers or names, arrays or references that contain numbers.



* All values must be positive.



## HARMEAN



The `Harmean` returns the harmonic mean of a data set. The harmonic mean is the reciprocal of the arithmetic mean of reciprocals.



**Syntax:**



_HARMEAN(number1, number2,...)_



**where:**



* number1, number2, ... are arguments for which you want to calculate the mean.



**Remarks:**



* The arguments must be either numbers or names, arrays or references that contain numbers.



* All data values must be positive.



## INTERCEPT



The `Intercept` calculates the point at which, the least squares fit line will intersect the y-axis.



**Syntax:**



_INTERCEPT(known_y's, known_x's)_



**where:**



* known_y's is the dependent set of observations or data.



* known_x's is the independent set of observations or data.



## LARGE



The `Large` returns the k-th largest value in a data set.



**Syntax:**



_LARGE(array, k)_



**where:**



* array is the array or range of data for which, you want to determine the k-th largest value.



* k is the position (from the largest) in the array or cell range of data to return.



**Remarks:**



* If n is the number of data points in a range, then LARGE(array,1) returns the largest value, and `LARGE(array,n)` returns the smallest value.



## MAX



The `Max` returns the largest value in a set of values.



**Syntax:**



_MAX(number1, number2, ...)_



**where:**



* number1, number2, ... are numbers for which you want to find the maximum value.



## MAXA



The `Maxa` returns the largest value in a list of arguments. Text and logical values such as True and False are compared as well as numbers.



**Syntax:**



_MAXA(value1, value2, ...)_



**where:**



* value1, value2, ... are values for which you want to find the largest value.



**Remarks:**



* You can specify arguments that are numbers, empty cells, logical values or text representations of numbers. Arguments that are error values cause errors. If the calculation does not include text or logical values, use the MAX worksheet function instead.



* If an argument is an array or reference, only values in that array or reference are used. Empty cells and text values in the array or reference are ignored.



* Arguments that contain True evaluate as 1; arguments that contain text or False evaluate as 0 (zero).



* If the arguments contain no values, MAXA returns 0 (zero).



## MEDIAN



The `Median` returns the median of the given numbers. The median is the number in the middle of a set of numbers; that is, half the numbers have values that are greater than the median and half have values that are less.



**Syntax:**



_MEDIAN(number1, number2, ...)_



**where:**



* number1, number2, ... are numbers for which you want the median.



**Remarks:**



* If there is an even number of numbers in the set, then MEDIAN calculates the average of the two numbers in the middle.



## MIN



The `Min` returns the smallest number in a set of values.



**Syntax:**



_MIN(number1, number2, ...)_



**where:** 



* number1, number2, ... are numbers for which you want to find the minimum value.



**Remarks:**



* If an argument is an array or reference, only numbers in that array or reference are used. Empty cells, logical values or text in the array or reference are ignored. If logical values and text should not be ignored, use MINA.



## MINA



The `Mina` returns the smallest value in the list of arguments. Text and logical values such as True and False are compared as well as numbers.



**Syntax:**



_MINA(value1, value2, ...)_



**where:**



* value1, value2, ... are values for which, you want to find the smallest value.



**Remarks:**



* Arguments that contain True evaluate as 1; arguments that contain text or False evaluate as 0 (zero).



## NORM.DIST



The `NORM.DIST` function calculates the normal distribution for a supplied value of x, and a supplied distribution mean & standard deviation.



**Syntax:**



_NORM.DIST(x,mean,stdev,cumulative)_



**where:**



* x is the value for which you want the distribution.



* mean is the arithmetic mean of the distribution.



* stdev is the standard deviation of the distribution.



* cumulative is a logical value for given function.



**Remarks:**



* `#VALUE!` occurs if mean or stdev is non-numeric.



* `#NUM!` occurs if stdev is equal to or less than zero.



## NORMDIST



Returns the normal cumulative distribution



**Syntax:**



_NORMDIST(x,mean,standard_dev,cumulative)_



**where:**



* x is the value for which you want the distribution.



* mean is the arithmetic mean of the distribution.



* standard_dev is the standard deviation of the distribution.



* cumulative is a logical value that determines the form of the function. If cumulative is TRUE, NORMDIST returns the cumulative distribution function; if FALSE, it returns the probability mass function.



**Remarks:**



* `#VALUE!` Occurs when mean or standard_dev is non-numeric.



* `#NUM!` Occurs when standard_dev ≤ 0.



* If mean = 0, standard_dev = 1, and cumulative = TRUE, NORMDIST returns the standard normal distribution, NORMSDIST.



## NORMSDIST



Returns the standard normal cumulative distribution.



**Syntax:**



_NORMSDIST(z)_



**where:**



* z is the value for which you want the distribution.



**Remarks:**



* `#VALUE!` Occurs when z is non-numeric.



## GAMMA.INV



The `Gamma.Inv` function returns the inverse of the Gamma Distribution.



**Syntax:**



_GAMMA.INV(x,y,z,cumulative)_



**where:**



* x is the value that evaluates the function.



* y is a distribution parameter.



* z is a distribution parameter.



* cumulative is a logical value that indicates which form of the exponential function to provide.



**Remarks:**



* `#NUM!` occurs when x is lesser than zero, when z is equal to or lesser than zero and occurs when alpha is equal to or lesser than zero. 



* `#VALUE!` occurs when x or y or z is non-numeric.



## GAMMALN.PRECISE



The `Gammaln.Precise` function returns the natural logarithm of the Gamma Distribution.



**Syntax:**



_GAMMALN.PRECISE(x)_ 



**where:**



* x is the positive numeric value that evaluates the function. 



**Remarks:**



* `#NUM!` occurs when x is lesser than zero.



* `#VALUE!` occurs when x is non-numeric.



## LOGNORM.DIST



The `Lognorm.Dist` function calculates the Log-Normal Probability Density Function or the Cumulative Log-Normal Distribution Function for a supplied value of x.



**Syntax:**



_LOGNORM.DIST(x,mean,stdev,cumulative)_



**where:**



* x is the value that evaluates the function.



* mean is the mean value of ln(x).



* stdev is the standard deviation of ln(x).



* cumulative is a logical value that determines the form of the function. 



**Remarks:**



* `#VALUE!` occurs when any argument is non-numeric.



* `#NUM!` occurs when x ≤ 0 or if stdev ≤ 0.



## LOGNORM.INV



The `Lognorm.Inv` function calculates the inverse of the Cumulative Log-Normal Distribution Function of x for a supplied probability.



**Syntax:**



_LOGNORM.INV(probability, mean, stdev)_



**where:**



* probability is a probability that corresponds to the lognormal distribution.



* mean is the arithmetic mean of In(x).



* stdev is the standard deviation of ln(x).



**Remarks:**



* `#VALUE!` occurs when any argument is non-numeric.



* `#NUM!` occurs when probability <= 0 or probability >= 1 and if Stdev<=0.





## NORM.S.DIST



The `Norm.S.Dist` function returns the standard normal distribution.



**Syntax:**



_NORM.S.DIST(val, cumulative)_



**where:**



* val is the value for which you want the distribution.



* cumulative is a logical value that determines the form of the function.



## NORM.S.INV



The `Norm.S.Inv` function returns the inverse of the standard normal cumulative distribution.



**Syntax:**



_NORM.S.INV(probability)_



**where:**



* probability is a probability that corresponds to the normal distribution.



## NEGBINOM.DIST



The `Negbinom.Dist` function calculates the probability mass function or the cumulative distribution function for the `Negative Binomial Distribution`.



**Syntax:**



_NEGBINOM.DIST(F_number,S_number,S_probability,cumulative)_



**where:**



* F_number is the number of failures.



* S_number is the threshold number of successes.



* S_probability is the probability of a success.



* cumulative is a logical value that determines the form of the function.



## PERCENTILE.EXC



The `Percentile.Exc` function returns the k-th percentile of values in a range, where k is in the range of 0 to 1 exclusively.



**Syntax:**



_PERCENTILE.EXC(array, k)_



**where:**



* array is the range of data that defines relative standing.



* k is the percentile value in the range of 0 to 1.



**Remarks:**



* `#NUM!` occurs when k is equal to or lesser than zero, when k is equal to or greater than 1, and when the array is empty.



* `#VALUE!` occurs when k is non-numeric.



## PERCENTILE.INC



The `Percentile.Inc` function returns the k-th percentile of values in a range, where k is in the range 0 to 1.



**Syntax:**



_PERCENTILE.INC (array,k)_



**where:**



* array is the range of data that defines relative standing.



* k is the percentile value in the range 0 to 1.



**Remarks:**



* `#NUM!` occurs when k is equal to or lesser than zero, when k is equal to or greater than 1, and when the array is empty.



* `#VALUE!` occurs when k is a non-numeric.



## PERMUTATIONA



The `PermutationA` function returns the number of permutations for a given number of objects (with repetitions) that can be selected from the total number of objects.



**Syntax:**



_PERMUTATIONA(number, number-chosen)_



**where:**



* number is an integer that describes the total number of objects.



* number-chosen is an integer that describes the number of objects in each permutation.



**Remarks:**



* `#VALUE!` occurs when numeric arguments use data types that are non-numeric.



* `#NUM!` occurs when numeric arguments have values that are not valid.



## POISSON.DIST



The `Poisson.Dist` function calculates the Poisson Probability Mass Function or the Cumulative Poisson Probability Function for a supplied set of parameters.



**Syntax:**



_POISSON.DIST(x,mean,cumulative)_



**where:**



* x is the number of events.



* mean is the expected numeric value.



* cumulative is a logical value that determines the form of the probability distribution returned.



**Remarks:**



* `#VALUE!` occurs when x is not an integer.



* `#NUM!` occurs when x or mean is non-numeric and s when x < 0.



## PERMUT



The `Permut` returns the number of permutations for a given number of objects that can be selected from a number of objects.



**Syntax:**



_PERMUT(number, number_chosen)_



**where:**



* number is an integer that describes the number of objects.



* number_chosen is an integer that describes the number of objects in each permutation.



**Remarks:**



•Number must be > 0 and  number_chosen must be >= 0.



•Number must be >= number_chosen.



## RANK.EQ



The `Rank.Eq` function returns the statistical rank of a given value within a supplied array of values.



**Syntax:**



_RANK.EQ(number, ref)_



**where:**



* number is the value for which you want to find the rank.



* ref is an array of values containing the supplied number.



## RSQ



The `RSQ` returns the square of the Pearson product moment correlation coefficient through data points in known_y's and known_x's.



**Syntax:**



_RSQ(known_y's, known_x's)_



**where:**



* known_y's is an array or range of data points.



* known_x's is an array or range of data points.



## SMALL



The `Small` returns the k-th smallest value in a data set.



**Syntax:**



_SMALL(array, k)_



**where:**



* array is an array or range of numerical data for which you want to determine the k-th smallest value.



* k is the position (from the smallest) in the array or range of data to return.



## STANDARDIZE



The `Standardize` returns a normalized value from a distribution characterized by mean and standard_dev.



**Syntax:**



_Standardize(x, mean, standard_dev))



**where:**



* x is the value that you want to normalize.



* mean is the arithmetic mean of the distribution.



* standard_dev is the standard deviation of the distribution.



**Remarks:**



* standard_dev must be > 0.



## STDEV



Returns the standard deviation of a supplied set of values (which represent a sample of a population).



**Syntax:**



_STDEV(number1,[number2],...)_



**where:**



* number1 is the first number argument corresponding to a sample of a population.



* number2… is the number arguments 2 to 255 corresponding to a sample of a population. You can also use a single array or a reference to an array instead of arguments separated by commas.



## STDEVA



Estimates standard deviation based on a sample. The standard deviation is a measure of how widely values are dispersed from the average value (the mean). Text and logical values such as True and False are also included in the calculation.



**Syntax:**



_STDEVA(value1, value2 , ...)_



**where:**



* value1, value2, ... are values corresponding to a sample of a population. You can also use a single array or a reference to an array instead of arguments separated by commas.



**Remarks:**



* Arguments that contain True evaluate as 1; arguments that contain text or False evaluate as 0 (zero).



## STDEVPA



Calculates the standard deviation based on the entire population given as arguments, including text and logical values.



**Syntax:**



_STDEVPA(value1, value2, ...)_



**where:**



* value1, value2, ... are values corresponding to a population. You can also use a single array or a reference to an array instead of arguments separated by commas.



**Remarks:**



* Arguments that contain True evaluate as 1; arguments that contain text or False evaluate as 0 (zero).



## STDEV.P



The `STDEV.P` function calculates the standard deviation of a supplied set of values.



**Syntax:**



_STDEV.P(number1,[number2],...])_



**where:**



* number1 is the first number argument corresponding to a population.



* number2 ... are the arguments 2 to 254 corresponding to a population.



**Remarks:**



* Arguments can either be numbers or names, arrays, or references that contain numbers.



* The standard deviation is calculated by using the **n** method.



* Arguments that are error values or text that cannot be translated into numbers cause errors.



## STDEV.S



The `STDEV.S` function calculates the sample standard deviation of a supplied set of values.



**Syntax:**



_STDEV.S(number1,[number2],...])_



**where:**



* number1 is the first number argument corresponding to a population.



* Number2, ... are the arguments 2 to 254 corresponding to a population.



**Remarks:**



* Arguments can either be numbers or names, arrays, or references that contain numbers.



* The standard deviation is calculated by using the **n** method.



* Arguments that are error values or text that cannot be translated into numbers cause errors.



## T.DIST



The `T.Dist` returns the Percentage Points (probability) for the Student t-distribution where a numeric value (x) is a calculated value of t for which the Percentage Points are to be computed. 



**Syntax:**



_TDIST(x,deg_freedom,tails)_



**where:**



* X is the numeric value at which to evaluate the distribution.



* Deg_freedom  is an integer indicating the number of degrees of freedom.



* Tails is the number of distribution tails to return. If Tails = 1, TDIST returns the one-tailed distribution. If Tails = 2, TDIST returns the two-tailed distribution.



**Remarks:**



* If any argument is non-numeric, TDIST returns the `#VALUE!` error value.



* If Deg_freedom < 1, TDIST returns the #NUM! error value.



* The Deg_freedom and Tails arguments are truncated to integers.



* If Tails is any value other than 1 or 2, TDIST returns the #NUM! error value.



* If x < 0, then TDIST returns the #NUM! error value.



* If Tails = 1, TDIST is calculated as TDIST = P( X>x ), where X is a random variable that follows the t-distribution. If Tails = 2, TDIST is calculated as TDIST = P(&#124;X&#124; > x) = P(X > x or X < -x).



* Since x < 0 is not allowed, to use TDIST when x < 0, note that TDIST(-x,df,1) = 1 – TDIST(x,df,1) = P(X >-x) and TDIST(-x,df,2) = TDIST(x,df,2) = P(&#124;X&#124; > x).



## T.INV



The `T.INV` returns the left-tailed inverse of the Student's t-distribution.



**Syntax:**



_T.INV(probability,deg_freedom)_



**where:**



* Probability is the probability associated with the Student's t-distribution.



* Deg_freedom is the number of degrees of freedom with which to characterize the distribution.



**Remarks:**



* If either argument is non-numeric, T.INV returns the `#VALUE!` error value.



* If probability <= 0 or if probability >1, T.INV returns the #NUM! error value.



* If deg_freedom is not an integer, it is truncated.



* If deg_freedom < 1, T.INV returns the #NUM! error value.



## TRIMMEAN



Returns the mean of the interior of a data set. `TRIMMEAN` calculates the mean taken by excluding a percentage of data points from the top and bottom tails of a data set.



**Syntax:**



_TRIMMEAN(array, percent)_



**where:**



* array is the array or range of values to trim and average.



* percent is the fractional number of data points to exclude from the calculation. For example, if percent = 0.2, 4 points are trimmed from a data set of 20 points (20 x 0.2): 2 from the top and 2 from the bottom of the set.



**Remarks:**



* Percent must be >= 0 and <= 1.



* TRIMMEAN rounds off the number of excluded data points down to the nearest multiple of 2. If percent = 0.1, 10 percent of 30 data points equals 3 points. For symmetry, TRIMMEAN excludes a single value from the top and bottom of the data set.



## VAR.P



Calculates variance based on the entire population (ignores logical values and text in the population).



**Syntax:**



_VAR.P(number1,[number2],...)_



**where:**



* Number1 is the first number argument corresponding to a population.



* Number2, ... is Optional. Number arguments 2 to 254 corresponding to a population.



**Remarks:**



* VAR.P assumes that its arguments are the entire population. If your data represents a sample of the population, then compute the variance by using VAR.S.



* Arguments can either be numbers or names, arrays, or references that contain numbers.



* Logical values, and text representations of numbers that you type directly into the list of arguments are counted.



* If an argument is an array or reference, only numbers in that array or reference are counted. Empty cells, logical values, text, or error values in the array or reference are ignored.



* Arguments that are error values or text that cannot be translated into numbers cause errors.



* If you want to include logical values and text representations of numbers in a reference as part of the calculation, use the VARPA function.



## VARPA



Calculates variance based on the entire population. In addition to numbers and text, logical values such as True and False are also included in the calculation.



**Syntax:**



_VARPA(value1, value2, ...)_



**where:**



* value1, value2, ... are arguments corresponding to a population.



**Remarks:**



* VARPA assumes that its arguments are the entire population. If your data represents a sample of the population, you must compute the variance using VARA.



* Arguments that contain True evaluate as 1; arguments that contain text or False evaluate as 0 (zero). If the calculation does not include text or logical values, use the VARP worksheet function instead.



## VARA



The `VarA` function returns the variance of a population based on a sample of numbers, text, and logical values (ie: TRUE or FALSE).



**Syntax:**



_VARA( value1, value2, ... value_n )_



**where:**



* value1, value2, ... value_n are the sample values. They can be numbers, text, and logical values. Values that are TRUE are evaluated as 1. Values that are FALSE or text values are evaluated as 0. 30 values can be entered.



## WEIBULL.DIST



The `Weibull.Dist` function returns the Weibull Distribution.



**Syntax:**



_WEIBULL.DIST(x,alpha,beta,cumulative)_



**where:**



* x is the value that evaluates the function.



* alpha is a parameter of the distribution.



* beta is a parameter of the distribution.



* cumulative determines the form of the function.



**Remarks:**



* `#NUM!` occurs when x is lesser than zero and when alpha or beta is equal to or lesser than zero.



* `#VALUE!` occurs when beta is non-numeric.



## ZTEST



`ZTest` function returns the one-tailed probability value of a z-test.



**Syntax:**



_ZTEST(a1,T_value,sigma)_ 



**where:**



* array is an array or range of data.



* T_value is the value to test..



* sigma  is the population (known) standard deviation.