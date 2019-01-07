[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> If you attempt to create a PMF for 1000 randomly generated numbers between 0 and 1, there will be far too many different potential probabilities, such that you cannot distinguish how likely certain outcomes are.  The code to create it can be found below:

>> sample = np.random.random(1000)  
pmf = thinkstats2.Pmf(sample)  
thinkplot.Pmf(pmf)  
thinkplot.Config(xlabel='Random Number', ylabel='PMF')  

>> If you create a CDF, it is much more clear that the distribution of 1000 randomly generated numbers is uniform.  The CDF has a line running diagonally from the bottom left to the top right, with the median value, 0.5, being in the middle of the line.  

>>cdf = thinkstats2.Cdf(sample)  
thinkplot.Cdf(cdf)  
thinkplot.Config(xlabel='Random Number', ylabel='PMF')  
