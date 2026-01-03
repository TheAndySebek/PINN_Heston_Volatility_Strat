This project began as toy code for visualizing volatility using yfinance data. The result included multiple graphic outputs, the most "convoluted" being the volatility surface. In this README, I will detail my goals for the project; however, much is subject to change. So, progress will be gradual as I continue in my education.

Still, this hardly amounted to much of a project, and I wanted to reinvent the idea into a more rigorous research and trading product. So, I broke it down into three segments that I plan to work on over the Spring '26 semester. Segment 1 is the first Jupyter notebook included in this repo. It pulls options data from y finance and visualizes IV with respect to time, strike, etc. 

Segment 2 is where I build out a PINN governed by Dupire local volatility PDE. A Physics Informed Neural Network (PINN) is a neural net with two loss functions. One prioritizes fitting the avaliable data, and the other prioritizes conformity to the governing PDE. Of course, this is not strict enforcement, but it does penalize deviance from the underlying physics of the problem. So, while it may not be perfect, it should do a pretty good job at enforcing arbitrage-free conditions. Then, I will calibrate a Heston model to the original yfinance IV values. I can then generate plots of and compare the yfinance, PINN, and Heston volatility surfaces. 

Segment 3 will then rely on building out a trading simulation. I will flesh out the trading signals as they become more apparent, but the gist is to use the PINN as a more informed perspective on volatility. So, compared to other pricing methods, it can be reasonably assumed that the PINN will provide better volatility inputs.



