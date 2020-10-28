# factorial experiment

* why ANOVA, what problems it tries to address?
The purpose of ANOVA analysis is to understand ratio of variance from treatment and error, and thus to check whether a good proportion of variance can be attributed to treatment, rather than random error.

ANOVA compares the variance from different sources, and so it evaluates impacts from different factors

before introducing ANOVA, we can compare mean of two datasets (from two treatment, maybe) using t-statistics, but we lack the ability to compare more levels in more complex set up. And so ANOVA is introduced for this problem.

* 2^K, for example, is a very special form of factorial design, as each factor has only 2 levels - low and high

* Q: for 2^k factorial design, how many treatments are there?
2^K

* Q: for 2^3 factorial design with 2 replicates, how many DF are there in total, for model, and for errors?
total: 2^3 * 2 -1 = 15
model (if look for full model): main (1+1+1) + interaction (1+1+1 + 1) = 7
error: 15 - 7 = 8

* Q: what is main effect and how to measure main effects?
main effect is the effect of one factor on dependent variable, averaged over all levels of other factors.
main effect of factor A:
(effect of A at level B1 + effect of A at level B2 + ... effect of A at level Bn) / N

* Q: what are SS/SST/SSE about?
SST: sum of squared differences between all dependent variables and its grand mean
SSR: sum of squared differences between treatment mean and grand mean.
```
if three treatment A, B and C, each treatment has 10 replicates:
then
SST = ( (mean A - grand mean)^2 + (mean B - grand mean)^2 + (mean C - grand mean)^2 ) 10 (replicates)
or
SST = VAR.S(A:C) * 2 (df: 3-1) * 10 (replicates)

sample variance = variance / (n-1)
```

SSE: sum of squared differences between dependent variables and treatment mean.

* Q: why in the ANOVA F-test, we put MST in the nominator and MSE in the denominator, even sometimes the MST is smaller? does it matter???

* What confounding in 2k factorial design


* why we use blocking:
to reduce the uncontrollable variation from experiment units
i.e. different batch of materials, experiment machines, plant field, day or time of experiment, etc.

to properly use blocking, we need to allocate different treatment across blockings/nuisance factors, and so the difference/variance due to different blockings might be separated out from analysis
