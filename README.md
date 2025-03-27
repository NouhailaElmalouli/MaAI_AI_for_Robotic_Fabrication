# **AI FOR ROBOTIC FABRICATION**


**PROJECT MEMBERS:**

- Ramy Anka <br>
- Salvador Cantuarias <br>
- Nouhaila Elmalouli <br>
- Misra Ozgok <br>
- Elena Papakosta <br>

**WHAT?**

🔍 We aim to develop a regression model that predicts the 6-joint configurations (joint coordination) of an ABB robotic arm during 3D clay printing, based on simulated toolpath data and actual printed movement data.

**WHY?**

🎯 To identify and learn the discrepancies between simulated and real joint movements, enabling more accurate motion planning, error correction, and improved robotic fabrication outcomes.

**HOW?**

🛠️ By collecting and preprocessing joint angle data from Rhino-modeled toolpaths, RoboStudio simulations, and post-printing movements, we train a regression model through polynomial or linear regression to predict joint values for given toolpath positions, enabling us to analyze, anticipate and prospectively refine robotic motion.

![Robotic Fabrication Frame 2](https://github.com/PaintDumpster/ai_for_robotic_fabrication/blob/main/Images/ai%20for%20robotic%20fabrication%20-%20Frame%202.jpg?raw=true)


**EXPECTATIONS OF CODE?**

-Load & preprocess joint data from both simulation and real-world printing accurately
-Train a regression model on the 6th joint configuration (end effector) based on toolpath input
-Evaluate and compare predicted joints with real vs simulated data using error margins
-Plot and visualize results and enable interpretation of joint movement over time
-Keep code well structured and documented for easy updates and presentation

**DATA SOURCE**

3D Printing of clay vase model and analysis

<img src="https://github.com/PaintDumpster/ai_for_robotic_fabrication/blob/main/Images/ai%20for%20robotic%20fabrication%20-%20Frame%203.jpg?raw=true" width="400" align="center"/>

![Joint Differential Marcos](https://github.com/PaintDumpster/ai_for_robotic_fabrication/blob/main/Images/plots/joint%20differential%20marcos/combined.png?raw=true)

![Joint Differential Plot](https://github.com/PaintDumpster/ai_for_robotic_fabrication/blob/main/Images/plots/joint%20differential%20yashashvy/combined.png?raw=true)



**How do we test/simulate?**

Testing and Training happens with csv files and numerical data from both:
    -The digital simulation from grasshopper
    -The documentation from the physical printing 


**RESULTS**

**Failed Training Prediction with small dataset:**

![Predicted vs Real Plot 2](https://github.com/PaintDumpster/ai_for_robotic_fabrication/blob/main/Images/plots/predvsreal_2.png?raw=true)

    - The model is not really understanding what is happening in joint 6 and instead mimics what is happening in the dataset.
    - The range for values of degrees of rotations is spanning from 0 to -40

**Successful Training Prediction with larger dataset:**

![Predicted vs Real Plot](https://github.com/PaintDumpster/ai_for_robotic_fabrication/blob/main/Images/plots/predvsreal.png?raw=true)

    -The range for values of degrees of rotations is spanning from 0 to -200, predicting an important role for the starting degree of the end effector 
    -The gap in the plot might be because it mirrored the starting point.
    -The accuracy is increased except for the starting point of the printing process which is an interesting point that it is predicting the joint's beginning action.






