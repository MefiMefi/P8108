# P8108 Lecture 1

## Logistic

- instructor: Q. Helen Li

## Evaluation 

Clean Concise Clear



_____

## Survival Data

- Survival data
  - Lifetime/failure time data
- Examples
  - Randomization to death
  - beginning of treatment to disease progression 
  - Mileage from the inital use to the first out of order

- combination of
  - compelete data
    - Time
      - Cont. R.V.s
      - Discrete time variable

## Time

- $T_L$: Starting point
- $T_R$: Ending point
- Relative Time $T$:
  - $T_L = 0,T_R = T$
- Time scale
- More on the incompelete data
  - events can occur before $T_L$ or after $T_R$
- More about event
  - need clear definition
  - In clinical trials: event adjustification committtee to confirm the event

## Distribution of the Survival Data

- survival time
  - discrete
  - continuous
    - $Exp$
    - piesewise exponential
    - Weibull
    - Gamma
    - Log-logistic
    - lognormal

### Discrete survival time

- Truly discrete
- survival time can only be observed by intervals
  - Cancer study: feasibility concern 
  - invasive procedure:biopsy, bone marrow
  - inconvenient to patient 

## Censoring

- Survival time ${T_L,T_R}$ contains missing parts
  - Either of one is not observed
  - Relative time $T\ge0$ can be unknown
- Right Censoring
  - Type-I
  - Type-II
  - randome censoring
  - independent censoring vs. informative censoring
- Left Censoring
- Inteval Censoring

### Right Censoring

- Type-I Censoring
  - Fixed censoring at time $t$
  - $X_i$ - event time
  - $T_i$ - observed time
  - $c$ - fixed censoring time
  - $\Delta_i$ - $\mathbb I(X_i\le c)$ - event censoring, not going to observe the event in the end of the study
  - $i = 1,\dots,n$ - subjects
  - $T_i = \min(X_i,c)$
- Type-II Censoring
  - Stop observation after $r/n$ events are observed
  - $T_i = X_{(i)}\quad if \quad c\le r$
- Random Censoring
  - Censor every one after last patient follow-up end
- Independent Censoring
  - $X\perp C$
- Dependent Censoring
  - Accrual Distribution: 
    - accrual is a rate: how fast you recruit patients
      - for example, if I want to recruit 400 patiens in 12 months (1 year), $A\sim Unif(0,1)$, $A = 1/2$ means I need to recruit 
    - **Accrual time or accrual period** is recruitment period during which subjects are being enrolled (recruited) into a study.
    - impact how long the trial would last, how long the patient will be followed
    - competing trials
- Noninformative Censoring
- Informative Censoring
  - competing risk
  - Dropout due to

### Other Type of Censoring

- Left Censoring
  - event occur before the assessment time
  - left truncation
- Interval Censoring
  - before current assesment time and after previous assessment

## Clinical Trial Basics

- studies to evaluate therapeutic efficacy and safety
  - Randomized
  - Controlled : placebo effect
  - Blinded
  - **to minimize bias**
- select a awell defined patient population
- Define endpoints
  - efficacy
  - safety
- Powered with adequate sample size
- Treatment
- Data collection
- Statistical analyses to evaluate the treatment effect in

---

## Case studies

Time to event

---

## Statistical Inference

### estimation 

- Questions
  1. How long a subject can live
  2. what is the survival rate at certain time $t$ 
  3. event rates
  4. median survival time
- Tools
  - Point estimate
  - variance/standard error
  - confidence interval, confidence band

### testing

- Questions
  - is the treatment prolonging life?
  - which treatment has better survival function
- Tools
  - 1-sample 2-samples
  - Hypothesis
  - Signigicance level and power -> sample size
  - Test statistics
  - P-value 

---

## Discrete Survival Function

- events occur at discrete time values $t_1<t_2<\cdots$
  $$
  f(t_i) = \Pr(T = t_i),i = 1,2,\dots
  $$

- cumulative distribution function

  
  $$
  \Pr(T\le t_k) = \sum\limits_{i=1}^{k}f(t_i)
  $$

- Survival Function
  $$
  S(t) = 1-\Pr(T\le t)
  $$
  

## Homework

