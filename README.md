# Predicting-dangerous-cognitive-state-of-pilot-using-physiological-data
Predicting dangerous cognitive state of pilot using physiological data to reduce commercial aviation fatality

This project is from the kaggle competition https://www.kaggle.com/c/reducing-commercial-aviation-fatalities to develop a model to detect troubling event from the physiological data of aircr
aft crew members. 
# Problem details
Aircraft accidents may happen from due to various reasons such as pilot errors, aircraft issues, runway deffects, etc. We are studying the "Pilot error part" as it is very important for 
the pilot to have abilities to do multi-tasking, concentration, and do pay attention to all the control tasks.
There is something called Airplane State Awareness (ASA) which is nothing but a pilot perfomance attribute. The Loss of ASA may lead to dangerous situations sometimes even to loss of controle
of the aircraft.

The given dataset is the real time physiological data of pilots who were subjected to distracting events and deviate from ASA to one of the three cognitive states.
1. Channelized Attention (CA)

Focusing only on one task without giving any attention to other task.

2. Diverted Attention (DA)

The attention is diverted by action or thought process associated with a decision.


3. Startle/Surprise (SS)

This is the response to a sudden unexpected stimulus.

More details about the dataset is [Here](https://www.kaggle.com/c/reducing-commercial-aviation-fatalities/data)

The Challenge is to predict the state of mind of the pilot in real-time using the physiological data given. There should be alert whenever any of the pilot enter into any of the 
given cognitive states.

# The Training Data
The training data consists of three experiments CA, DA, and SS. So, the output label which is named as 'event' is always one of the four  : Baseline (No event), CA, DA, or SS.

The Test data is collected from a flight simulator in which we are predicting the cognitive state of the pilot. 

The Data field has data from sensors such as EEG (From different parts of the brain such as frontal(f), temporal(t), perietal(p), etc), ECG, and Galvanic Skin Response.

# Exploratory Data Analysis

EDA is done on the data to get a deep understanding of the data. And various visualizion methods are used on each feature.

# Feature Engineering

Feature engineering is carried out on the data with the support of dedicated libraries like biosppy.
The Heartbeat information is derived from ECG samples using bisppy. The potential difference between EEG electrodes are also derived.

The frequency bands such as alpha_low, alpha_high, beta, ect are calculated from EEG.
And finally the redundant features are droped based on the correlation checkup.

# Modelling

Basic Logistic Regression model and Light GBM (Gradient Boosting Machine) are used.
Confusion matrix-based evaluation and analysis are carried out along with plotting the importance of features in Light GBM model.
The Final prediction on the test data is also done and the final result and the model perfomance evaluation matrics are also included.

--Basil K Jose
