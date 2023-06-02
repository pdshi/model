# MoveMate's Machine Learning MODEL
* Consist of {Workout Planner, Activity Recognition Model}

## 1. Workout Planner
* Consist of {Capability Classifier Model (CCM), Schedule Generator (SG)} 
* Posits a workout schedule for 1 month
* The output is determined by the data inputted by the user, currently ['Gender', 'Height', 'Weight'] for CCM and ['Availability/Week'] for SG other head are not yet included

Flow of Process
![asac](https://github.com/pdshi/model/assets/94330691/c5bab383-7917-4bdf-b340-764825e5e9a6)


### 1a. Capability Classifier Model (CCM)
* Posits a percentage of capability 0 to 100% 
* Later used to calculate the ideal reps in a particular workout

Dataset
https://www.kaggle.com/datasets/yersever/500-person-gender-height-weight-bodymassindex

A Visual

![datset characteristic](https://github.com/pdshi/model/assets/94330691/75c7e119-e183-41dc-864b-6a3f8bb93863)
![F to M status proportion](https://github.com/pdshi/model/assets/94330691/8d2c1a89-93c8-4b19-a88c-e5e9d7f8255f)

500 data in total


The Model

![model-ccm](https://github.com/pdshi/model/assets/94330691/3fb89c82-ea6d-4ee0-8b12-c5160f6e921a)


Train Result

![train result](https://github.com/pdshi/model/assets/94330691/0e55d00d-0ae2-47dd-a130-c4e28605efea)


Output

![sasaa](https://github.com/pdshi/model/assets/94330691/8620681b-7bf1-4fdb-a891-23aa38a37813)

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

Output

![dsdsds](https://github.com/pdshi/model/assets/94330691/45f32679-d482-4b14-b9c2-b398161adaa1)







