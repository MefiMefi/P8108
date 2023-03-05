# P8108 Lecture 2

## Discrete survival time

### density function

$f(t_j) = P(T = t_j),j = 1,2,\ldots, k$

$P(T\ge t_1) = 1$

$P(T\ge t_j) = P(T>t_{j-1})$

### survival function

$S(t_j) = P(T\gt t_j) = \sum\limits_{k\ge j}^{} f(t_k)$

### harzard function

- conditional probablility of failure at $t_i$ given that the individual has survived to $t_i$
- length of the interval, longer the greater chance subjects meet events

### hazard rate

Number of events per person-time, not only the ratio of events

$S(t_j) = \prod\limits_{i:t_i\le t_j}^{}(1-h_i)$

## continuous survival time

$$
\begin{aligned}
h(t) &= \lim\limits_{\Delta t\rightarrow 0}\frac{P(t\le T\lt t+\Delta t\mid T\ge t)}{\Delta t}\\
& = \lim\limits_{\Delta t\rightarrow 0}\frac{P(t\le T\lt t+\Delta t, T\ge t)}{\Delta t P(T\ge t)}\\
& = \lim\limits_{\Delta t\rightarrow 0}\frac{P(t\le T\lt t+\Delta t)}{\Delta t}\cdot\frac{1}{P(T\ge t)}\\
& = \frac{f(t)}{S(t^-)}\\
& = -\frac{dS(t)}{dt}\cdot\frac{1}{S(t)}\\
& = -\frac{d\log S(t)}{dt}
\end{aligned}
$$



### cumulative hazard function

$H(t) = \int\limits_{0}^{t} h(x)dx = \int\limits_{0}^{t}-\frac{d\log S(x)}{dx}dx = -\log S(t)$

## Hazard function with dependent censoring

survival data $(T_i, \Delta_i)$

- $T_i = \min(X_i, C_i)$
- $\Delta_i = \mathbb I (X_i\le C_i)$
- $X_i$ event time

$$
h(t) =\lim\limits_{\Delta t\rightarrow 0}\frac{P(t\le T_i\lt t+\Delta t\mid T_i\ge t, C_i\ge t)}{\Delta t}
$$

## Mean survival

the expected survival

$E(T) = \int uf(u)du$

## Survival quantiles

- median survival time $t_m$
- $S(t_m) = P(T\gt t_m) = 0.5$
- $t_m = \inf\{t:S(t)\le 0.5 \}$

## Exponential distribution

### constant hazard rate

- $\lambda$ is the rate of event
  - $\lambda_1 = 0.5$
    - 50 deaths per 100 patient-year
    - 4.17 deaths per 100 patient-month
  - $\lambda_2 = 2$
- Hazard ratio $\lambda_1/\lambda_2$

### survival quantiles

- median survival time $\lambda = 0.5$: $S(t_m) = 0.5 = e^{-\lambda t_m}$ (Person-day): 1.38 days
- 60% survival time $\lambda = 0.005$: 102 days



## Pisewise Exponential

- the event rate can change overtime

### Pisewise Hazard Function

### Pisewise exponential - cumulative hazard function

sum of length of interval $\times$ hazard rate

- $S(t) = e^{-H(t)}$

### Pisewise exponential - PDF

<u>**NEED DERIVIATION**</u>

## Weibull Distribution

- Generalized exponential distribution
- accelerated hazard functions
- convenient to model

### Weibull

- $T\sim Weibull(\alpha,\lambda)$
  - $\alpha>0$, shape parameter
  - $\lambda >0 $, scale parameter
  - $\alpha = 1 \rightarrow T\sim Exp(\lambda)$
- $f(t) = \lambda\alpha t^{\alpha-1}e^{-\lambda t}$

### Weibull hazard function

- $\alpha > 1$ : Accelerate 

## Log-normal 

## Gamma distribution

## Log-logistic

---

# Nonparametric Estimation

half close half open

## Life table Estimate

- number of events
- number of censors
- numberi of subjects at risk
- average number of subjects at the interval: reason why have 1/2, kaplan-meier dont need this average

### survival function estimation

$\hat S(t_i) = \hat S(t_{i-1})(1-\frac{d_i}{n'_i})$ 

### pdf

### hazard function

- Number of events per person-time-units(constant rate, constant censor, constant event)
- do the deriviation
- weighted average of the hazard functions in the interval, so don't have invariant property 



