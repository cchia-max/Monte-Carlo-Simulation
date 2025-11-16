Monte Carlo Simulation

An interactive web-based Monte Carlo simulation using geometric Brownian motion to model asset price evolution and risk analysis


Overview
This project demonstrates Monte Carlo simulation techniques commonly used in quantitative finance, risk management, and statistical modeling. The simulation generates thousands of possible future scenarios based on random sampling, allowing you to visualize the distribution of outcomes and assess probabilities.


Features

Real-time Simulation: Run up to 10,000 Monte Carlo paths instantly
Interactive Parameters: Adjust initial value, expected returns, volatility, and time horizon
Visual Results: See 50 sample paths plotted on an interactive chart
Statistical Analysis: View key metrics including mean, median, standard deviation, and percentiles
Probability Assessment: Calculate the likelihood of different outcomes
Responsive Design: Works seamlessly on desktop and mobile devices


Monte Carlo simulation is a computational technique that uses random sampling to model complex systems and estimate the probability of different outcomes. It's named after the famous Monte Carlo casino in Monaco, reflecting the role of chance in the method.

Common Applications:

Finance: Portfolio optimization, option pricing, risk assessment
Engineering: Reliability analysis, design optimization
Science: Molecular modeling, climate predictions
Project Management: Schedule risk analysis, cost estimation

Technology Stack

React - Component-based UI framework
Recharts - Data visualization library
Tailwind CSS - Utility-first styling
Lucide React - Icon library


How to Use

Set Parameters:

Number of Simulations: How many random paths to generate (100-10,000)
Initial Value: Starting amount ($10-$1,000)
Mean Annual Return: Expected growth rate (-20% to +30%)
Volatility: Price variability (1% to 50%)
Time Steps: Number of trading days to simulate (50-500)


Run Simulation: Click "Run Simulation" to generate results

Analyze Results:

View statistical metrics in the results panel
Examine sample paths on the chart
Check probability of profit/loss


Experiment: Adjust parameters to see how they affect outcomes


Mathematical Model
The simulation uses Geometric Brownian Motion (GBM), the same model used in the Black-Scholes option pricing formula:
dS = μS dt + σS dW
Where:

S = asset price
μ = drift (expected return)
σ = volatility
dW = Wiener process (random walk)

The discrete implementation uses:
S(t+1) = S(t) × exp((μ - σ²/2)Δt + σ√Δt × Z)
Where Z is a random standard normal variable generated using the Box-Muller transform.


Customization

Adapt for Different Scenarios
The core simulation engine can be easily modified for:
Dice Games: Replace the GBM formula with discrete outcomes
javascriptconst outcome = Math.floor(Math.random() * 6) + 1;
Project Timelines: Use triangular or beta distributions
javascriptconst duration = triangularDistribution(min, mode, max);
Insurance Claims: Use Poisson distributions for event frequency
javascriptconst numClaims = poissonRandom(lambda);


Understanding the Results

Mean: Average final value across all simulations
Median: Middle value (50th percentile)
Standard Deviation: Measure of outcome variability
5th/95th Percentile: Range containing 90% of outcomes
Probability of Profit: Percentage of simulations ending above initial value


Acknowledgements

Monte Carlo methods pioneered by Stanisław Ulam and John von Neumann
GBM model foundational to modern quantitative finance
Inspired by financial modeling and risk analysis practices
