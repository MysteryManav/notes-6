### Linear Regression:
- It is a statistical method used to model relationship between a single independent variable and a continuous dependent variable
- It assumes there is a linear relationship between the predictor and response, which can be described by a straight line
- It aims to estimate the parameters of this line to predict the values of the dependent variable based on the values of the independent variable
- Equation: $$Y = \beta_0 + \beta_1X + \epsilon$$ where,
	- $Y$ => Dependent Variable (Target)
	- $X$ => Independent Variable (Feature)
	- $\beta_0$ => y-intercept (Constant Term)
	- $\beta_1$ => Slope of the line (regression coefficient)
	- $\epsilon$ => Error term representing random variability in data
- Goal: To estimate the values of $\beta_0$ and $\beta_1$ that minimise the sum of squared errors between the observed and predicted values of the dependent variable
- Application: Forecasting Stock Prices, Temperature Forecasting, etc.

### Least Square Regression:
- It is a method used to estimate the parameters of a linear regression model by minimising the sum of the squared differences between the observed and predicted values of the dependent variable
- It aims to find the line that best fits the data by minimising the residual sum of squares (RSS) which represent the sum of the squared differences between actual and predicted values of the dependent variable
- Objective: Find coefficients of linear regression model that minimise the sum of squared residuals
- Residuals are difference between observed value of dependent variable and predicted values from regression model
