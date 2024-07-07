## AR Models
Auto Regressive (AR) Models predict the future value of a time series based on its own past values.
An AR model is typically written as:

$$
y_t = c + \phi_1 y_{t-1} + \phi_2 y_{t-2} + \ldots + \phi_p y_{t-p} + \epsilon_t
$$

where \( \phi_1, \phi_2, \ldots, \phi_p \) are the model coefficients.

The model coefficients, \( \phi_1, \phi_2, \ldots, \phi_p \), are estimated using a variety of methods, such as least squares estimation.

## MA Models
Moving Average (MA) Models predict the future value of a time series based on past forecast errors. An MA model is typically written as:

$$
y_t = \mu + \epsilon_t + \theta_1 \epsilon_{t-1} + \theta_2 \epsilon_{t-2} + \ldots + \theta_q \epsilon_{t-q}
$$

where \( \theta_1, \theta_2, \ldots, \theta_q \) are the model coefficients, \( \mu \) is the mean of the series, and \( \epsilon_t \) is the error term.

The model coefficients, \( \theta_1, \theta_2, \ldots, \theta_q \), are estimated by minimizing the sum of the squares of the errors (SSE).

## ARMA Models
Auto Regressive Moving Average (ARMA) Models combine both AR and MA models. An ARMA model is typically written as:

$$
y_t = c + \phi_1 y_{t-1} + \phi_2 y_{t-2} + \ldots + \phi_p y_{t-p} + \epsilon_t + \theta_1 \epsilon_{t-1} + \theta_2 \epsilon_{t-2} + \ldots + \theta_q \epsilon_{t-q}
$$

where \( \phi_1, \phi_2, \ldots, \phi_p \) are the AR coefficients, \( \theta_1, \theta_2, \ldots, \theta_q \) are the MA coefficients, \( c \) is a constant, and \( \epsilon_t \) is the error term.

The ARMA model captures both the linear dependencies in the time series data (via AR terms) and the dependencies between an observation and a residual from a moving average model applied to lagged observations (via MA terms).


## ARIMA Models
Auto Regressive Integrated Moving Average (ARIMA) Models extend ARMA models to account for non-stationarity in the time series. An ARIMA model is typically written as:

$$
y_t = c + \phi_1 y_{t-1} + \phi_2 y_{t-2} + \ldots + \phi_p y_{t-p} + \epsilon_t + \theta_1 \epsilon_{t-1} + \theta_2 \epsilon_{t-2} + \ldots + \theta_q \epsilon_{t-q} + d
$$

where \( d \) represents the number of differencing required to make the time series stationary.

## SARIMA Models
Seasonal Auto Regressive Integrated Moving Average (SARIMA) Models extend ARIMA models to account for seasonality in the time series. A SARIMA model is typically written as:

$$
SARIMA(p, d, q)(P, D, Q)_m
$$

where:
- \( p, d, q \) are the non-seasonal parameters.
- \( P, D, Q \) are the seasonal parameters.
- \( m \) is the number of periods in each season.
- AR(p): Autoregressive component of order p
- MA(q): Moving average component of order q
- I(d): Integrated component of order d
- Seasonal AR(P): Seasonal autoregressive component of order P
- MA(Q): Seasonal moving average component of order Q
- Seasonal I(D): Seasonal integrated component of order D

## When to use what 
  1. 
