[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> resp = nsfg.ReadFemResp()  
pmf = thinkstats2.Pmf(resp.numkdhh, label='numkdhh')  
thinkplot.Pmf(pmf)  
thinkplot.Config(xlabel='Number of Children', ylabel='PMF')  

>> biased_pmf = pmf.Copy()  
for x, p in pmf.Items():  
    biased_pmf.Mult(x, x)  

>> thinkplot.PrePlot(2)  
thinkplot.Pmfs([pmf, biased_pmf])  
thinkplot.Config(xlabel='Number of children', ylabel='PMF')  

pmf.Mean()  

biased_pmf.Mean()  

The means are:  
actual = 1.024205155043831  
biased = 2.461860525971477  

