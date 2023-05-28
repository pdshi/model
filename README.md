# MoveMate's Machine Learning MODEL
* Consist of {Workout Planner, Activity Recognition Model}

## 1. Workout Planner
* Consist of {Capability Classifier Model (CCM), Schedule Generator (SG)} 
* Posits a workout schedule for 1 month
* The output is determined by the data inputted by the user, currently ['Gender', 'Height', 'Weight'] for CCM and ['Availability/Week'] for SG other head are not yet included

Flow of Process
![AS](https://github.com/pdshi/model/assets/94330691/9558ba24-1cf1-4016-a04a-4c2c24ba86a6)

### 1a. Capability Classifier Model (CCM)
* Posits a percentage of capability 0 to 100% 
* Later used to calculate the ideal reps in a particular workout

Dataset
https://www.kaggle.com/datasets/yersever/500-person-gender-height-weight-bodymassindex

A Visual

![datset characteristic](https://github.com/pdshi/model/assets/94330691/cc5b8df8-a561-467f-b447-809fe4b460b2)
![F to M status proportion](https://github.com/pdshi/model/assets/94330691/7fd320f6-6de8-4115-ade2-588747d1e383)
500 data in total


The Model

![model-ccm](https://github.com/pdshi/model/assets/94330691/e9625f2f-dd4c-4739-a34b-c0fcad9b1b37)


Train Result

![train result](https://github.com/pdshi/model/assets/94330691/87762fc9-dfa5-4cd8-b173-4da14dd97f20)


Output

![image](https://github.com/pdshi/model/assets/94330691/f285a9d7-4ef9-400d-b148-a0bd5968e41c)

### 1b. Schedule Generator (SG)
* First posits a workout plan consist of 3 Workout: PushUp, SitUp, JumpingJack with reps determinded by scaling the floor to ceil of workout by the capability score value 
* Then posits a workout schedule in the forms of dataframe ['No WO', 'Plan', 'Date', 'WO Starts', 'WO Stops']  
* Amount of workout/week and its duration are currently determined only by ['Availability/Week'] 
* Workout plan generated every month with updated user's data

Sets Scheme: 
- Week 1: 2 Reps
- Week 2: 3 Reps
- Week 3: 3 Reps
- Week 4: 4 Reps

(ONGOING)








