# Weight Loss Simulator
## Purpose
In recent years, social pressure has led many individuals to attempt losing weight. A popular approach has been calorie reduction, which is often believed to guarantee weight loss. However, many people often fail to recognize that this weight loss is only temporary as the body adjusts its metabolic rate to compensate for the reduction in energy intake. This results in a new steady body weight being achieved without any further decrease in weight even if a the reduced caloric intake is maintained, as highlighted below.

![image](https://github.com/rmahinpei/Weight-Loss-Simulator/blob/main/Figure-1.png)

To bring awareness to this phenomena, a Python implementation of the deterministic model of weight loss proposed by Diana M. Thomas was created. The original paper presenting the model can be found [here](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2764961/) to learn more about the details of the model.

## Key Features
The Python model uses Euler's approximation technique to predict an individual's body weight over a set time period. The model allows experimentation with the following case-dependent parameters:
- Time step used in each iteration
- Subject's reduced caloric intake
- Subject's initial weight
- Subject's initial age
- Subject's gender

## How to Use
First, download WeightLoss.ipynb. Then, open the file and before running the code, adjust the case dependent constants to your desired values.
```python:
# case dependent constants used in model
I = 0.75*2677.8          # energy intake in kcal/day                  
W0 = 60                  # initial weight in kg                       
A0 = 20                  # initial age in years                       
dt = 1                   # size of time step used in each Euler iteration in days
```
Depending on the chosen gender for your subject, you may need to change the values of some of the universal constants.
```python:
# universal constants used in model
a = 293                  # male = 293     female = 248     for resting metabolic rate (RMR)    
p = 0.4330               # male = 0.4330  female = 0.4356  for RMR    
y = 5.92                 # male = 5.92    female = 5.09    for RMR  
omega = 0.56             # male = 0.56    female = 0.32    for alpha variable
```

## How To Contribute
Here are just a few ways that interested individuals can contribute to this project:
- Update the values used for the universal constants in the model
- Add new case-dependent parameters for users to change
- Make model's results more accurate by accounting for even more universal constants
- Allow the results for multiple subjects to be displayed on the same graph
