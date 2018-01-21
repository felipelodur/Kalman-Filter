# Kalman-Filter
This project was initially developed as coursework for *Artificial Intelligence for Robotics* @ Georgia Tech

## What is a Kalman Filter?

It is an algorithm that uses measurements observed over time to estimate unknown variables. Kalman Filter is typically used for determining the precise location of vehicles.
<p align="center">
<img src="https://www.mathworks.com/content/dam/mathworks/videos/u/Understanding-Kalman-Filters-Part-3-Optimal-State-Estimator.mp4/_jcr_content/renditions/S2E3_Thumbnail.jpg">
</p>

Kalman Filters can be boiled down to two main steps: Update step and prediction step.


### 1) Measurement Update
In this step the system should retrieve some measurement via a sensor (e.g. GPS). 
The Algorithm considers prior knowledge of state and the noise/error the sensors may display.
These values are used to build a Gaussian distribution that implies the belief on the system location. 

### 2) Prediction
The system state may indicate that the system state should change in some way, which changes the state belief provided by the Gaussian.
This prediction also has a degree of uncertainty, which is considered to update the location belief. 
This is known as *posterior state estimate*


### Variables
The system variables are further indicated:
- x = initial state (e.g. location and velocity)
- P = initial uncertainty (how certain you are about each value of your state)
- u = external motion   (could be a effective motion or something that changes the system state)
- F = next state function (prediction based on )
- H = measurement function (sensors)
- R = measurement uncertainty (sensor error/noise) 
