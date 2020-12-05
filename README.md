# UCB_COVID_Prediction_Model
# Final Project
# FINAL PROJECT: SEGMENT_1: PRESENTAION
             

## Selected Topic:                                        
In this project, we present **the prediction model for various COVID-19 and non-Covid medical conditions from frontal chest X-ray of the patients**. The need to streamline patient management for both COVID-19 and non-Covid conditions has become more pressing than ever. Chest X-rays provide a non-invasive (potentially bedside) tool to monitor the progression of the disease. Such a tool can gauge severity of the lung infections for these diseases that can be used for escalation or de-escalation of care as well as monitoring treatment efficacy, especially in the ICU. 
 
## Reason why selected topic:                   
As the world grapples with multiple medical conditions, especially COVID-19, every ounce of technological innovation and ingenuity harnessed to fight this pandemic and other infections brings us one step closer to overcoming it. Artificial intelligence and machine learning are playing a key role in better understanding and addressing, especially the COVID-19 crisis. Machine learning technology enables computers to mimic human intelligence and ingest large volumes of data to quickly identify patterns and insights.
In the fight against these critical medical conditions, organizations have been quick to apply their machine learning expertise in several areas: scaling customer communications, understanding how they spread, and speeding up research and treatment. In this scenario, it is both relevant and useful to understand chest X-ray images to understand and develop an AI-based approach to predict and understand both COVID-19 and non Covid-19 diseases.
 
## Description of the source of data:
* This is a labelled datset of 5000 frontal chest X-ray images of COVID and non-COVID cases of Atelectasis, Cardiomegaly, Consolidation, Edema, Enlarged Cardiomediastinum, Fracture, Lung Lesion, Lung Opacity, Pleural, Pneumonia and Pneumothorax. 
* The 2 sources used to create this data set are:
Covid-Chestxray-Dataset, for COVID-19 X-ray samples
	(https://github.com/ieee8023/covid-chestxray-dataset)
ChexPert Dataset, for Non-COVID samples
	(https://stanfordmlgroup.github.io/competitions/chexpert)
* These COVID-19 samples from Covid-Chestxray-Dataset are extracted from several publications. Only the posterior-anterior images have been used for the dataset. Also, the X-ray images of COVID-19 samples have been verified by board-certified radiologist for the credibility of dataset.
* It has been tried to uniformly sample images from ChexPert for Non-COVID samples.
 
 
## Question we hope to be answered through data:	
Using input of chest X-ray images of both Covid and several Non-COVID cases, we intend to predict if the patient has that particular COVID or Non-COVID (Atelectasis, Cardiomegaly, Consolidation, Edema, Enlarged Cardiomediastinum, Fracture, Lung Lesion, Lung Opacity, Pleural, Pneumonia and Pneumothorax or no finding at all) medical condition or not.
This would give physicians an edge and allow them to act with more confidence while they wait for the analysis of a radiologist by having a digital second opinion confirm their assessment of a patient's condition. Also, these tools can provide quantitative scores to consider and use in studies.
 
## Tasks and Technologies used:
* STEP1: Data cleaning and analysis:
The images in the dataset are already augmented using the Augmentator Python library. We will use different methods form the imblearn python library to balance the dataset, including SMOTE, Cluster Centroid and SMOTEEN. 

* STEP2: Database Storage
Images would be stored in AWS S3 and the labels for the same in AWS RDB with PostgreSQL flavour. We will integrate Flask to display the data.
 
* STEP3: Applying Machine Learning Model
We'll be using the Tensorflow ML library to create a Multi-Class CNN classifier of different respiratory syndromes. We will try different pretrained models including VGG, ResNet and AlexNet and add layers at the end to adjust for our needs.
 
* STEP4_Dashboard: Tableau for visualization
In addition to using a Flask template, we will integrate Tableau for a fully functioning and interactive dashboard. It will be published on the public tableau server.
 

