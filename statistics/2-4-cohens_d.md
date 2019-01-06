[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> If we inspect the means, we'll find that first born babies are 0.125 pounds lighter on average than other babies.  The Cohen effect size for the total weight between these two groups is -0.089.  This is nearly 3 times larger than the Cohen effect size for pregnancy length, though it is still a rather small and insignifact difference.  The code used to find the value can be found below:

import math
live = preg[preg.outcome == 1]
firsts = live[live.birthord == 1]
others = live[live.birthord != 1]
diff = firsts.totalwgt_lb.mean() - others.totalwgt_lb.mean()
firsts_var = firsts.totalwgt_lb.var()
others_var = others.totalwgt_lb.var()
firsts_n = len(firsts.totalwgt_lb)
others_n = len(others.totalwgt_lb)
pooled_var = (firsts_n * firsts_var + others_n * others_var) / (firsts_n + others_n)
cohens_d = diff / math.sqrt(pooled_var)
cohens_d
