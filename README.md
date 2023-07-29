# Electrical-Fault-detection-and-classification
Evaluation of SVM and Logistic Rregression for detection and classification of Electrical-Fault-detection-and-classification



## Data 
Taken from --> https://www.kaggle.com/datasets/esathyaprakash/electrical-fault-detection-and-classification
Taken from -->https://www.kaggle.com/code/manishabenschop/electrical-fault-analysis

They have modeled a power system in MATLAB to simulate fault analysis. The power system consists of 4 generators of 11 × 10^3 V, each pair located at each end of the transmission line. Transformers are present in between to simulate and study the various faults at the midpoint of the transmission line.

![Capture](https://github.com/keonij1/Electrical-Fault-detection-and-classification/assets/10182525/4cdf0eac-0fea-4a27-bf55-109bb3959367)

They simulate the circuit under normal conditions as well as under various fault conditions. We then collect and save the measured Line Voltages and Line Currents at the output side of the power system. They collected nearly 12000 data points, and then the data is labeled.


So we have two files(datasets) here namely classData.csv and detect_dataset_csv:
- detect_dataset_csv  is for train the model to detect any type of Fault and
- classData.csv  is for Classification of Shunt Fault



###detect_dataset_csv 

![Capture](https://github.com/keonij1/Electrical-Fault-detection-and-classification/assets/10182525/b2a9f5f0-0235-481e-b469-c88174812c7d)



###classData.csv

![Capture1](https://github.com/keonij1/Electrical-Fault-detection-and-classification/assets/10182525/bc351db9-96f1-4985-b066-aed3429b8d41)

This file classData.csv contains the dataset to classify the types of fault.

A,B,C are the 3-phases of the electrical system. Most of the Electricity transmission happens via 3-phase system,
and hence Ia represents the current(I) in phase A, Va represents the Voltage(V) in phase A and so on for Phase A and B.

Inputs - [Ia,Ib,Ic,Va,Vb,Vc]
Outputs - [G C B A]

Examples :
[0 0 0 0] - No Fault
[1 0 0 1] - LG fault (Between Phase A and Gnd)
[0 0 1 1] - LL fault (Between Phase A and Phase B)
[1 0 1 1] - LLG Fault (Between Phases A,B and ground)
[0 1 1 1] - LLL Fault(Between all three phases)
[1 1 1 1] - LLLG fault( Three phase symmetrical fault)

## Models

## Results
