# Common Nighthawk Call Recognizer and Distance Estimator Usage Readme

This recognizer is designed to detect Common Nighthawk (*Chordeiles minor*) calls in audio recordings.  In addition this notebook includes a model to estimate the distance of the Common Nighthawk from the ARU based on the volume of the call.  The recognizer output is a sigmoidal score for Common Nighthawk presence and the relative decibel level for each ~0.064 second detection window of a recording.  The distance estimate produces an estimate of distance from the ARU with upper and lower bounds of a 95% confidence interval.

## Running the models
Recordings must be run through the Common Nighthawk detection model by running the scripts in the "CommonNighthawk_Recognizer_Processing" Jupyter notebook either locally or via Google Colab.  The repository can be cloned to a local machine in order to run the recognizer via Jupyter Notebooks, or to Google Drive where the recognizer can be run in the Google Colab environment.  To run the notebook on Google Colab you will need to have a Google account and have the audio recordings that you wish to process stored in your Google Drive.  If your recordings are stored locally on your machine or a portable hard drive you will need to run the code locally on your machine within a python environment that runs Jupyter Notebooks.

### Running the model locally
If you wish to run the model on your local machine you can clone the repository to your machine, or you can download all three parts of the model ('coni-model.index', 'coni-model.meta', and 'coni-model.data-00000-of-00001') and the notebook ('CommonNighthawk_Recognizer_Processing.ipynb') to the same folder on your local drive and run the notebook in a local python environment of your choice.  You'll need to have the model files and notebook in the same folder that you will set to be your working directory, though the recordings can be located elsewhere on your machine.

### Running the model on Google Colab 
If you want to run the model using Google Colab rather than a python environment on your own computer then you can open the notebook directly in Colab from the Github repository and then clone the repository to your Google Drive via the steps in the notebook.  Follow the steps for linking your Google Drive account and the audio recording files stored there to the scripts in the code to make them accessible to the model running in the notebook.

---
The Common Nighthawk recognizer was developed using the Tensorflow package in python by Chris Scott in collaboration with Elly Knight, and was updated by Kevin Kelly.

The distance estimate model was developed by Dan Yip and Elly Knight.