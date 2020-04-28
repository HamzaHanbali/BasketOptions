# BasketOptions : 'bop' function
Calculate prices of put and call options with early exercise (American-type) on a basket of stock following Geometrical Brownian motions

# Description of input parameters
bop ( InterestRate, Weights, SpotPrices, Volatilities, CorrelationMatrix, Strike, Maturity, NumberTimeSteps, Put = 0, AmericanType = 0)

InterestRate: numerical value of the interest rate.

Weights: numerical vector of length n for the weights assigns to each component in the basket.

SpotPrices: numerical vector of length n for the time-0 values of each component.

Volatilities: numerical vector of length n for the volatilities of each component.

CorrelationMatrix: correlation matrix with positive pairwise correlations, or a single number in case of equal pairwise correlations.

Strike: positive numerical value for the excercise price.

Maturity: positive numerical value for the maturity of the option.

NumberTimeSteps: for the discretization of the time grid.

Put: returns put price if Put=1, or call price if Put=0 (default).

AmericanType: includes early exercise if AmericanType=1, or the European-type price for AmericanType=0 (default).

# Example of input parameters:
InterestRate=0.1

SpotPrices=rep(100,8)

Volatilities=c(0.3,0.6,0.1,0.9,0.3,0.7,0.8,0.2)

Weights= rep(1/8,8)

CorrelationMatrix=0.5

Strike=30

Maturity=.5

NumberTimeSteps=100

Put=1

AmericanType=1

# Reference:
Hanbali, H. and Linders, D. (2019), 'American-type basket option pricing: a simple two-dimensional Partial Differential Equation', Quantitative Finance 19, pp. 1689--1704.

