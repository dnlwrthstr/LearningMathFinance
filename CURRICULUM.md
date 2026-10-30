# Curriculum

Eleven modules, ordered so each one only needs math from the sibling repos plus earlier modules.
Status: ☐ planned · ◐ in progress · ☑ done.

**Prerequisite shorthand** (paths inside the sibling repos):

- **P:** [LearningProbability](https://github.com/dnlwrthstr/LearningProbability), `coursera/…`
- **L:** [LearningLinearAlgebra](https://github.com/dnlwrthstr/LearningLinearAlgebra), `hyperskill/…`
- **C:** [LearningCalculus](https://github.com/dnlwrthstr/LearningCalculus), `hypersklill/…`, `coursera/…` or `my_learning/…`
- **gap**: no sibling notebook yet; the module teaches the math itself or a course notebook is needed first.

---

## 00 Returns and compounding

| # | Notebook | Math link | Status |
|---|---|---|---|
| 01 | Simple vs log returns, aggregation over time and across assets | C: `02_derivaties/05_derivative_of_logarithmic_functions` | ☐ |
| 02 | Continuous compounding as a limit | C: `01_limits/00_limits_of_sequences`, `02_derivaties/06_derivative_of_exponential_functions` | ☐ |
| 03 | Time value of money: discounting, annuities, NPV, IRR (root finding) | C: Newton's method (gap) | ☐ |
| 04 | Annualizing return and volatility (√T rule and when it fails) | P: `02_discribing_distribution/05_variance` | ☐ |

## 01 Fixed income math

| # | Notebook | Math link | Status |
|---|---|---|---|
| 01 | Bond price as a function of yield | C: `02_derivaties/01_derivatives_of_polynomials` | ☐ |
| 02 | Duration = first derivative, convexity = second derivative | C: `02_derivaties/09_higher_order_derivatives` | ☐ |
| 03 | Taylor approximation of price changes | C: Taylor series (gap) | ☐ |
| 04 | Yield curves and forward rates | C: `04_integrals/00_introduction_to_integrals` | ☐ |

## 02 Describing returns

| # | Notebook | Math link | Status |
|---|---|---|---|
| 01 | Mean, median, mode of fund returns and AuM | P: `02_discribing_distribution/01_mean_expected_value`, `02_median_and_mode` | ☐ |
| 02 | Volatility and the units of risk | P: `02_discribing_distribution/05_variance`, `06_standard_deviation` | ☐ |
| 03 | Skewness, kurtosis, fat tails | P: `02_discribing_distribution/10_skewness`, `11_kurtosis` | ☐ |
| 04 | Are returns normal? QQ plots and tail checks | P: `02_discribing_distribution/16_qq_plots` | ☐ |

## 03 Covariance and two assets

| # | Notebook | Math link | Status |
|---|---|---|---|
| 01 | Variance of a sum and a difference: diversification, tracking error, hedging | P: `02_discribing_distribution/04_sum_of_expectations`, `03_…/06_covariance` | ◐ |
| 02 | Correlation and what it does not tell you | P: `03_probability_distribution_with_multiple_variables/09_correlation_coefficient` | ◐ |
| 03 | Minimum-variance hedge ratio | P: `03_…/06_covariance`, C: `02_derivaties/10_local_extrema` | ◐ |
| 04 | The two-asset frontier | P: `03_…/06_covariance`, C: `02_derivaties/10_local_extrema` | ◐ |

## 04 Portfolio mathematics

| # | Notebook | Math link | Status |
|---|---|---|---|
| 01 | Portfolio variance w′Σw | P: `03_…/08_covariance_matrix`, L: `01_vector_and_vector_spaces/010_vectors_matrices_scalars` | ◐ |
| 02 | Why Σ must be positive semi-definite | L: `05_matrix_decomposition/056_positive_definite_matrices` | ◐ |
| 03 | Global minimum-variance portfolio with Lagrange multipliers | C: Lagrange multipliers (gap) | ◐ |
| 04 | Efficient frontier, tangency portfolio, Sharpe ratio | L: `05_matrix_decomposition/051_lu_decomposition` | ◐ |
| 05 | CAPM and the security market line | modules 03–04 | ◐ |

## 05 Risk measures

| # | Notebook | Math link | Status |
|---|---|---|---|
| 01 | Value at Risk: parametric, historical, Monte Carlo | P: `02_discribing_distribution/12_quantiles`, `01_probability_distribution/10_normal_distribution` | ◐ |
| 02 | Expected shortfall (CVaR) | P: `02_discribing_distribution/03_expected_value_of_a_function`, C: `04_integrals/03_u_substitution` | ◐ |
| 03 | Drawdowns | P: `01_probability_distribution/08_cumulative_distribution_function`, `04_sampling_and_point_estimation/05_law_of_large_numbers` | ◐ |
| 04 | Risk contributions and Euler allocation | C: `coursera/02_gradients/01_partial_derivatives_part_1`, `03_gradients` | ◐ |

## 06 Estimation error

| # | Notebook | Math link | Status |
|---|---|---|---|
| 01 | How noisy is a mean return? | P: `04_sampling_and_point_estimation/02_sample_mean`, `07_central_limit_theorem_continuous` | ◐ |
| 02 | Confidence interval for a Sharpe ratio | P: `06_confidence_intervals/` | ◐ |
| 03 | Is this fund's alpha real? Testing outperformance | P: `07_hypothesis_testing/04_p_values` | ◐ |
| 04 | Means are hard, covariances are easier | P: `04_sampling_and_point_estimation/04_sample_variance` | ◐ |

## 07 Regression and factor models

| # | Notebook | Math link | Status |
|---|---|---|---|
| 01 | Beta as a regression slope | P: `05_point_estimation/04_mle_linear_regression` | ◐ |
| 02 | Least squares and the normal equations | L: `05_matrix_decomposition/0510_least squares` | ◐ |
| 03 | Multi-factor models (Fama–French style) and return attribution | L: `05_matrix_decomposition/059_psedoinverse` | ◐ |
| 04 | PCA of returns: statistical factors | L: `05_matrix_decomposition/055_spectral_decomposition`, `057_singular_value_decomposition` | ☐ |

## 08 Robust portfolio construction

| # | Notebook | Math link | Status |
|---|---|---|---|
| 01 | Why mean-variance optimization breaks (error maximization) | module 06 | ☐ |
| 02 | Covariance shrinkage (Ledoit–Wolf) | P: `05_point_estimation/05_regularization` | ☐ |
| 03 | Risk parity | module 05/04 | ☐ |
| 04 | Black–Litterman as Bayesian updating | P: `05_point_estimation/06_from_mle_to_map`, `00_introduction_to_probability/11_bayes_theorem_formula` | ☐ |

## 09 Time series and volatility

| # | Notebook | Math link | Status |
|---|---|---|---|
| 01 | Random walk and autocorrelation | gap (time series) | ☐ |
| 02 | Volatility clustering, EWMA volatility | gap | ☐ |
| 03 | GARCH(1,1) by maximum likelihood | P: `05_point_estimation/01_intro_to_maximum_likelihood` | ☐ |

## 10 Stochastic processes and pricing

| # | Notebook | Math link | Status |
|---|---|---|---|
| 01 | Binomial tree and risk-neutral pricing | P: `01_probability_distribution/03_binomial_distribution` | ☐ |
| 02 | From random walk to Brownian motion | P: `04_sampling_and_point_estimation/07_central_limit_theorem_continuous` | ☐ |
| 03 | Geometric Brownian motion and lognormal prices | P: `01_probability_distribution/10_normal_distribution` | ☐ |
| 04 | Itô's lemma, intuitively | gap (stochastic calculus) | ☐ |
| 05 | Black–Scholes and Monte Carlo pricing | modules 10/01–04 | ☐ |

---

## Math gaps to fill in the course repos

Newton's method (IRR) · Taylor series · partial derivatives and gradients in finance form ·
Lagrange multipliers · time series (stationarity, ARMA) · stochastic calculus.

## Reference curricula this plan is built from

- MIT OCW 18.S096, *Topics in Mathematics with Applications in Finance* (2013): linear algebra, probability, regression, VaR, time series, volatility, portfolio theory, factor models, stochastic processes, Itô calculus, Black–Scholes. https://ocw.mit.edu/courses/18-s096-topics-in-mathematics-with-applications-in-finance-fall-2013/
- CFA Level I, Quantitative Methods (rates and returns, TVM, statistical measures of asset returns, portfolio mathematics, simulation, estimation, hypothesis testing, regression) and Portfolio Management (risk and return I/II, risk management). https://finance.uworld.com/cfa/level-1-topics/
- EDHEC / Coursera, *Investment Management with Python and Machine Learning* specialization: portfolio construction, robust estimation, factor models, ML for asset management. https://www.classcentral.com/course/investment-management-python-machine-learning-18815
