[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

*Exercise 1   Based on the results in this chapter, suppose you were asked to summarize what you learned about whether first babies arrive late.*

*Which summary statistics would you use if you wanted to get a story on the evening news? Which ones would you use if you wanted to reassure an anxious patient?*

I'm not sure I would use any of these statistics to get on the news as there doesn't seem to be any newsworthy results to report. To reassure a patient I would explain that the average difference is only around thirteen hours, so it's not really that much. I'd also explain that all pregenancies and women are different, so you can never really tell what will happen in your case. My sister had two children, and her first child was born two weeks earlier than her due date, and her second was born two weeks later, so there are definitely cases where the first baby is born much sooner.


*Finally, imagine that you are Cecil Adams, author of The Straight Dope (http://straightdope.com), and your job is to answer the question, “Do first babies arrive late?” Write a paragraph that uses the results in this chapter to answer the question clearly, precisely, and honestly.*

Statistically speaking, first babies do arrive later than second babies. By approximately thirteen hours on average. 




*Exercise 2   In the repository you downloaded, you should find a file named chap02ex.ipynb; open it. Some cells are already filled in, and you should execute them. Other cells give you instructions for exercises. Follow the instructions and fill in the answers.*

*A solution to this exercise is in chap02soln.ipynb*


As an exercise, plot the histogram of pregnancy lengths (column prglngth).

preglength = np.floor(live.prglngth)
histlength = thinkstats2.Hist(preglength, label='pregnancy length')
thinkplot.Hist(histlength)
thinkplot.Config(xlabel='Weeks', ylabel='Count')

Use `Largest` to display the longest pregnancy lengths.

for weeks, freq in hist.Largest(10):
    print(weeks, freq)

As an exercise, confirm that std is the square root of var:

import math
std, math.sqrt(var)

(2.702343810070593, 2.702343810070593)

Compute the Cohen effect size for the difference in pregnancy length for first babies and others.

Cohend = CohenEffectSize(firsts.prglngth, others.prglngth)
Cohend

0.028879044654449883

Using the variable totalwgt_lb, investigate whether first babies are lighter or heavier than others.

Compute Cohen’s effect size to quantify the difference between the groups. How does it compare to the difference in pregnancy length?

firsts.totalwgt_lb.mean(), others.totalwgt_lb.mean()

firsts.totalwgt_lb.mean() - others.totalwgt_lb.mean()

-0.12476118453549034

Cohendwgt = CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)

Cohendwgt 

-0.088672927072602

Make a histogram of totincr the total income for the respondent's family. To interpret the codes see the codebook.

histtotinc = thinkstats2.Hist(resp.totincr, label='Incomes')

thinkplot.Hist(histtotinc)

thinkplot.Config(xlabel='Income Level', ylabel='Count')

Make a histogram of age_r, the respondent's age at the time of interview.

histage = thinkstats2.Hist(resp.age_r, label='Age')

thinkplot.Hist(histage)

thinkplot.Config(xlabel='Age', ylabel='Count')

Make a histogram of numfmhh, the number of people in the respondent's household.

histnum = thinkstats2.Hist(resp.numfmhh, label='Number in Household')

thinkplot.Hist(histnum)

thinkplot.Config(xlabel='Number in Household', ylabel='Count')

Make a histogram of parity, the number of children borne by the respondent. How would you describe this distribution?

The distribution is skewed to the left so that the majority of the responders have few or no children and very few have more than three.

histparity = thinkstats2.Hist(resp.parity, label='Number of Children')

thinkplot.Hist(histparity)

thinkplot.Config(xlabel='Number of Children', ylabel='Count')

Use Hist.Largest to find the largest values of parity.

for parity, freq in histparity.Largest(10):

    print(parity, freq)

22 1
16 1
10 3
9 2
8 8
7 15
6 29
5 95
4 309
3 828

Let's investigate whether people with higher income have higher parity. Keep in mind that in this study, we are observing different people at different times during their lives, so this data is not the best choice for answering this question. But for now let's take it at face value.

Use totincr to select the respondents with the highest income (level 14). Plot the histogram of parity for just the high income respondents.

inc14 = resp[resp.totincr == 14]

incothers = resp[resp.totincr != 14]

​

histpar14 = thinkstats2.Hist(inc14.parity, label='Highest Income Households')

thinkplot.Hist(histpar14)

thinkplot.Config(xlabel='Number of Children', ylabel='Count')

Find the largest parities for high income respondents.

for parity, freq in histpar14.Largest():

    print(parity, freq)

8 1
7 1
5 5
4 19
3 123
2 267
1 229
0 515

Compare the mean parity for high income respondents and others.

inc14.parity.mean(), incothers.parity.mean()

inc14.parity.mean() - incothers.parity.mean()

-0.17371374470099532

Compute the Cohen effect size for this difference. How does it compare with the difference in pregnancy length for first babies and others?

DParity = CohenEffectSize(inc14.parity, incothers.parity)

DParity

-0.1251185531466061


*In the repository you downloaded, you should find a file named chap02ex.py; you can use this file as a starting place for the following exercises. My solution is in chap02soln.py.*
*Exercise 3   The mode of a distribution is the most frequent value; see http://wikipedia.org/wiki/Mode_(statistics). Write a function called Mode that takes a Hist and returns the most frequent value.*





*As a more challenging exercise, write a function called AllModes that returns a list of value-frequency pairs in descending order of frequency.*


*Exercise 4   Using the variable totalwgt_lb, investigate whether first babies are lighter or heavier than others. Compute Cohen’s d to quantify the difference between the groups. How does it compare to the difference in pregnancy length? *
