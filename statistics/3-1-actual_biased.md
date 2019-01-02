[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>>>
(I referenced https://github.com/zurda/thinkStats2/blob/master/chap03ex01.ipynb for assistance)

    import thinkstats2
    import thinkplot

    resp = ReadFemResp()

    resp.numkdhh.value_counts()

    kids_under18 = thinkstats2.Pmf(resp.numkdhh)
    kids_under18.Prob(0)

show the pmf
    thinkplot.Hist(kids_under18, label='numkdhh')
    thinkplot.Show()

Compute the biased distribution we would see if we surveyed the children and asked them how many children under 18 (including themselves) are in their household.

    def BiasPmf(pmf, label=''):

        new_pmf = pmf.Copy(label=label)

        for x, p in pmf.Items():
            new_pmf.Mult(x, x)

        new_pmf.Normalize()
        return new_pmf

    biased_pmf = BiasPmf(kids_under18, label='biased')
    thinkplot.Hist(biased_pmf, label='biased')
    thinkplot.Show()

Display actual and biased on same chart
    thinkplot.PrePlot(2)
    thinkplot.Pmfs([kids_under18, biased_pmf])
    thinkplot.Show(xlabel='Number of', ylabel='PMF')

Compute means
    kids_under18.Mean()
    biased_pmf.Mean()
