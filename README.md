# Session-4 Assignment
## Problem Statement
Your new target is:
- 99.4% (this must be consistently shown in your last few epochs, and not a one-time achievement)
- Less than or equal to 15 Epochs
- Less than 10000 Parameters (additional points for doing this in less than 8000 pts)

Do this in exactly 3 steps

Each File must have "target, result, analysis" TEXT block (either at the start or the end)

Explain your 3 steps using these target, results, and analysis with links to your GitHub files (Colab files moved to GitHub). 

## Solution
### First Step
#### Target:
- Get the set-up right
- Set Transforms (with Image Normalization)
- Set Data Loader
- Set Basic Working Code
- Set Basic Training & Test Loop
- Set plotting of Train and Test Accuracy and Loss Graphs
#### Results:
- Total Parameters: 140,688
- Best Training Accuracy: 99.71%
- Best Test Accuracy: 98.77%
#### Analysis:
- Model is overfitting. It can be inferred from training accuracy that it has nearly learnt (what it can) but test accuracy is still low.
- In nearly all epochs (post first 3 epochs) training accuracy is more than testing accuracy. Model has started remembering training data and is resulting in lower test accuracy.
- Parameters in this model need to be reduced and regularized to make the model learn better.
#### Model Summary:
<img width="571" alt="Attempt_1_Summary" src="https://user-images.githubusercontent.com/118976187/213630721-b1da7341-b9eb-4561-a8c1-969e4f735651.png">

#### Model Train and Test Performance:
<img width="901" alt="Attempt_1_Performance" src="https://user-images.githubusercontent.com/118976187/213631027-798a3e87-237e-4575-b8ec-c725ced85519.png">

