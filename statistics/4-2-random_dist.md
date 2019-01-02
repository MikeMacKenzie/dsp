[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> 
    import numpy as np
    import thinkstats2
    import thinkplot

    rand_nums = np.random.random(1000)

    pmf = thinkstats2.Pmf(rand_nums)
    thinkplot.Pmf(pmf, linewidth=0.1)
    thinkplot.Config(xlabel='Random number', ylabel='PMF')


    cdf = thinkstats2.Cdf(rand_nums)
    thinkplot.Cdf(cdf)
    thinkplot.Config(xlabel='Random number', ylabel='CDF')

 The distribution is uniform but the pmf is hard to interpret
 Becausse there are a relatively large number of unique values.
 Each of the 1000 numbers is presumably different and therefore has an equal liklihood. This is displayed nicely in the cmf plot.
