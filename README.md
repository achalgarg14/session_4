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

### Second Step
#### Target:
- Reducing number of parameters to reach closer to 10k
- Add batch wise normalization for increasing model efficiency
- Introduce Dropouts to avoid overfitting
- Add GAP layer
#### Results:
- Total Parameters: 11,944
- Best Training Accuracy: 99.31%
- Best Test Accuracy: 99.45%
#### Analysis:
- Model learned well and can do better if pushed to more epochs. But with current limitations we can not go beyond 15 epochs.
- Batch Normalization has helped the model in learning even with reduced parameters.
- DropOut made the model resilient.
- Consistently Test Accuracy is higher than Train Accuracy, so model is not overfitting
- GAP layer (size of 4) has not reduced accuracy
- Last few epochs does not have consistent accuracy above 99.4%
#### Model Summary:
<img width="598" alt="Attempt_2_Summary" src="https://user-images.githubusercontent.com/118976187/213638217-bd09eacb-1ed0-4dea-8e17-49977fa92c04.png">

#### Model Train and Test Performance:
<img width="901" alt="Attempt_2_Performance" src="https://user-images.githubusercontent.com/118976187/213638294-6829af6d-be1e-4b48-b2d2-030702edccac.png">

### Third Step
#### Target:
- Lower number of parameters (Meet our target of <=10000 Parameters)
- Add Transformations to make model invariant to brightness and rotation
- Use Step Learning to stablize results

#### Results:
- Total Parameters: 9,752
- Best Training Accuracy: 99.34%
- Best Test Accuracy: 99.53%

#### Analysis:
- Model was able to achieve it's target of 99.40% accuracy at 7th epoch and remained more than 99.40% after that.
- Adding transformations like Random Rotation & Color Jitter helped the model to learn better and become more resilient.
- Step Learning with higher starting learning rate of and decent step size helped the model in learning fast and stabilizing accuracy in later stages.
#### Model Summary:
<img width="570" alt="Attempt_3_Summary" src="https://user-images.githubusercontent.com/118976187/213648095-1efa5e9c-f857-4ca9-81c4-66af202449f8.png">

#### Model Train and Test Performance:
<img width="911" alt="Attempt_3_Performance" src="https://user-images.githubusercontent.com/118976187/213668194-7560af64-c1d2-4f94-bf85-e1fd9441abef.png">

