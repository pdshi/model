# MoveMate's Workout Planner and Activity Recognition Model

## Table of Contents
- [Description](#description)
- [Architecture](#architecture)
- [Results](#results)
- [Dependencies](#dependencies)
- [File Structure](#file-structure)

## Description
Workout Planner
* Consist of {Capability Classifier Model (CCM), Schedule Generator (SG)} 
* Posits a workout schedule for 1 month
* The output is determined by the data inputted by the user, currently ['Gender', 'Height', 'Weight'] for CCM and ['Freq/Week', 'Day Start', 'WO Time'] for SG other head are not yet included

### Capability Classifier Model (CCM)
* Posits a percentage of capability 0 to 100% 
* Later used to calculate the ideal reps in a particular workout

### Schedule Generator (SG)
* First posits a workout plan consist of 3 Workout: PushUp, SitUp, JumpingJack with reps determinded by scaling the floor to ceil of workout by the capability score value 
* Then posits a workout schedule in the forms of dataframe ['exercise no.', 'plan', 'sets', 'date', 'starts', 'end']  
* Workout plan generated every month with updated user's data

Flow of Process
![asac](https://github.com/pdshi/model/assets/94330691/c5bab383-7917-4bdf-b340-764825e5e9a6)

A Visualization of The Data

![F to M status proportion](https://github.com/pdshi/model/assets/94330691/8d2c1a89-93c8-4b19-a88c-e5e9d7f8255f)

500 data in total

## Architecture
![model-ccm](https://github.com/pdshi/model/assets/94330691/3fb89c82-ea6d-4ee0-8b12-c5160f6e921a)

## Results
### Capability Classifier Model (CCM)
![train result](https://github.com/pdshi/model/assets/94330691/0e55d00d-0ae2-47dd-a130-c4e28605efea)
Output
![sasaa](https://github.com/pdshi/model/assets/94330691/8620681b-7bf1-4fdb-a891-23aa38a37813)

### Schedule Generator (SG)
Sets Scheme: 
- Week 1: 2 Reps
- Week 2: 3 Reps
- Week 3: 3 Reps
- Week 4: 4 Reps
![dsdsds](https://github.com/pdshi/model/assets/94330691/45f32679-d482-4b14-b9c2-b398161adaa1)

## Dependencies
Here are the dependencies and libraries needed to run the notebook
- Python
- TensorFlow
- Numpy
- Pandas
- Matplotlib

## File Structure
- `Workout Planner/Capability Classifier`: Directory containing the notebook and outputs for Capability Classifier.
- `Workout Planner/Schedule Generator`: Directory containing the notebook and outputs for Schedule Generator.

The dataset used for the model can be found here
https://www.kaggle.com/datasets/yersever/500-person-gender-height-weight-bodymassindex
