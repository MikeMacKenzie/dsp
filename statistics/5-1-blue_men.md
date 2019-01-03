[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>> 
    import scipy.stats

    mu = 178
    sigma = 7.7
    dist = scipy.stats.norm(loc=mu, scale=sigma)
    type(dist)

    dist.mean(), dist.std()

    dist.cdf(mu-sigma)

    low = dist.cdf(177.8)    # 5'10"
    high = dist.cdf(185.4)   # 6'1"
    in_range = high - low

34.2% of men are within the Blue Man Group range.
