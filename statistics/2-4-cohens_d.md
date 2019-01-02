[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>>> 
 To compute Cohen's d I used the existing thinkstats Summarize function.
 I replaced "prglngth" with "totalwgt_lb"

    def Summarize2(live, firsts, others):
        """Print various summary statistics."""

        mean = live.totalwgt_lb.mean()
        var = live.totalwgt_lb.var()
        std = live.totalwgt_lb.std()

        print('Live mean', mean)
        print('Live variance', var)
        print('Live std', std)

        mean1 = firsts.totalwgt_lb.mean()
        mean2 = others.totalwgt_lb.mean()

        var1 = firsts.totalwgt_lb.var()
        var2 = others.totalwgt_lb.var()

        print('Mean')
        print('First babies', mean1)
        print('Others', mean2)

        print('Variance')
        print('First babies', var1)
        print('Others', var2)

        #print('Difference in weeks', mean1 - mean2)
        #print('Difference in hours', (mean1 - mean2) * 7 * 24)

        #print('Difference relative to 39 weeks', (mean1 - mean2) / 39 * 100)

        d = thinkstats2.CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)
        print('Cohen d', d)

    Summarize2(live, firsts, others)

First babies were approximately 0.12 lbs. lighter than non-first babies (Cohen's d = .09).
First babies were longer than non-first babies but this effect (d = .03) was weaker than the weight effect (d = .09) and in the opposite direction.
