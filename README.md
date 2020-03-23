# Covid-19 Data experiments
## Fitting the data to sigmoid and d-sigmoid curves

I got bored and curious this weekend and decided to take a look at some data from the virus spread.  I found this great data set from [Johns Hopkins CSSE](https://github.com/CSSEGISandData/COVID-19).  Tis data is updated daily.

I graphed a few things and decided to work on fitting data to a sigmoid since this should characterize the infected population over time.  I created a modified sigmoid with three paprameters:

1.	scale - so that the top of the sigmoid is different from one.
2. 	offset - to move the inflection point of the sigmoid to a value other than zero.
3. b - a smoothing factor for flattening or steepening the transition curve of the sigmoid.

I haven't tried any learning yet, but just using the modified sigmoid and its derivative we can see some interesting results.  

The next step is to try to learn the parameters.  since this data will be updated daily, we should be able to learn these results for all the collected data and refine them as time goes on.

