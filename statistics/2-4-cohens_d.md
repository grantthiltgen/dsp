[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)




*Exercise 4   Using the variable totalwgt_lb, investigate whether first babies are lighter or heavier than others. Compute Cohen’s d to quantify the difference between the groups. How does it compare to the difference in pregnancy length? *

Using the variable totalwgt_lb, investigate whether first babies are lighter or heavier than others.

Compute Cohen’s effect size to quantify the difference between the groups. How does it compare to the difference in pregnancy length?

firsts.totalwgt_lb.mean(), others.totalwgt_lb.mean()

firsts.totalwgt_lb.mean() - others.totalwgt_lb.mean()

-0.12476118453549034

Cohendwgt = CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)

Cohendwgt 

-0.088672927072602

The Cohen's d shows the the difference in means of weights of first born babies and other babies is small, showing that it is around 0.08 standard deviations. While that is larger than the length of pregnancy, it is still very small, although the negative value indicates that first babies are slightly smaller in weight than others.
