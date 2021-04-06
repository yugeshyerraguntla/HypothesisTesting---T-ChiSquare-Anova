# HypothesisTesting---T-ChiSquare-Anova
HypothesisTesting - T Test, ChiSquare Test, Anova(F) Test, Correlation.

1. What is hypothesis testing ?
Hypothesis testing is a statistical method that is used in making statistical decisions using experimental data. Hypothesis Testing is basically an assumption that we make about the population parameter.
_A hypothesis test evaluates two mutually exclusive statements about a population to determine which statement is best supported by the sample data._

__Null hypothesis :-__ In inferential statistics(make predictions (“inferences”) from that data.), the null hypothesis is a general statement or default position that there is no relationship between two measured phenomena, or no association among groups

__Alternative hypothesis :-__ The alternative hypothesis is the hypothesis used in hypothesis testing that is contrary to the null hypothesis.

Type I error: When we reject the null hypothesis, although that hypothesis was true. Type I error is denoted by alpha. In hypothesis testing, the normal curve that shows the critical region is called the alpha region
Type II errors: When we accept the null hypothesis but it is false. Type II errors are denoted by beta. In Hypothesis testing, the normal curve that shows the acceptance region is called the beta region.

One tailed test :- A test of a statistical hypothesis , where the region of rejection is on only one side of the sampling distribution , is called a one-tailed test.

Two-tailed test :- A two-tailed test is a statistical test in which the critical area of a distribution is two-sided and tests whether a sample is greater than or less than a certain range of values.

P-value :- The P value, or calculated probability, is the probability of finding the observed, or more extreme, results when the null hypothesis (H 0) of a study question is true — the definition of ‘extreme’ depends on how the hypothesis is being tested.

__Low P-value == Reject H0__
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

One tail test - = or !=
Two tail test - > or <

1. Hypothesis - Null Ho and Alternative H1
2. Signficance - Alpha = 0.05
3. Sample - Take a sample
4. p value
5. Decide

# Widely used hypothesis testing types:

__1. Z-Test__
- Sample is assumed to be Normally distributed.
- Calculate Z-Score using Mean and SD.
- If the test statistic is lower than the critical value, accept the hypothesis or else reject the hypothesis
- z = (x — μ) / (σ / √n)

hypothesis that the sample drawn belongs to the same population.
Null: Sample mean is same as the population mean
Alternate: Sample mean is not same as the population mean


__2. T-Test__
- Sample is Normally Distributed
- But Mean and SD are not known.
- T-test is used to compare the mean of two given samples
- There are three versions of t-test
1. Independent samples t-test which compares mean for two groups                    (stats.ttest_ind)
2. Paired sample t-test which compares means from the same group at different times (stats.ttest_rel(a=weight1,b=weight2) 
3. One sample t-test which tests the mean of a single group against a known mean.   (stats.ttest_1samp) returns ttest,p_value
                                                               
-t = (x1 — x2) / (σ / √n1 + σ / √n2)


__3. Chi-Square Test__
- Chi-square test is used to compare categorical variables (say A and B)(dataset_table = pd.crosstab(dataset['A'],dataset['B']));(val=stats.chi2_contingency(dataset_table)); 
- There are two type of chi-square test
1. Goodness of fit test, which determines if a sample matches the population.
2. A chi-square fit test for two independent variables is used to compare two variables in a contingency table to check if the data fits.
  small chi-square value means that data fits
  high chi-square value means that data doesn’t fit.
- Χ2 = Σ [ (Or,c — Er,c)2 / Er,c ]
  
hypothesis being tested for chi-square is
Null: Variable A and Variable B are independent
Alternate: Variable A and Variable B are not independent.


__4. ANOVA Test__
- also known as analysis of variance, is used to compare multiple (three or more) samples with a single test.
- There are 2 major flavors of ANOVA
1. One-way ANOVA: It is used to compare the difference between the three or more samples/groups of a single independent variable.
2. MANOVA: MANOVA allows us to test the effect of one or more independent variable on two or more dependent variables. In addition, MANOVA can also detect the difference in co-relation between dependent variables given the groups of independent variables.

-F= ((SSE1 — SSE2)/m)/ SSE2/n-k

hypothesis being tested in ANOVA is
Null: All pairs of samples are same i.e. all sample means are equal
Alternate: At least one pair of samples is significantly different

============================
One Categorical Feature - One Sample Propotion Test
Two Categorical Feature - Two Sample Propotion Test - Chi Square Test
One Continuous Feature - Z Test or T Test
Mean and Cont. Feature - T Test
Two Continuous Feature - Correlation
One Cont./Nume + Categorical(with mor than 2 categories) - ANOVA Test

https://towardsdatascience.com/statistical-tests-when-to-use-which-704557554740
