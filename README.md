# CRNN model for music genre classification
For this project a convolutional recurrent neural network (CRNN) was used. The goal of the project was to train a model for one specific task - music genre classification.
We trained the model on the GTZAN dataset.

## Dataset 
The dataset we used is GTZAN, which contains 1000 music files, each 30 seconds long. The dataset is divided into 10 different genres, each containing 100 songs. 
The genres are - blues, classical, country, disco, jazz, rock, metal, reggae, hiphop and pop.

## Architecture
The model is made of CNN and RNN layers. < br / >
CNN layers were used for feature extraction from MEL spectograms. < br / >
The RNN layers are bidirectional LSTM layers used for temporal processing. < br / >
A self attention mechanism is also implemented for focusing on relevant audio segments. < br / >
And finally, layers for classification for 10 different genre categories.

## Training
As mentioned above, the GTZAN dataset was used for this project.
We manually divided the dataset into several parts - training, validation and testing.
For training, 70% of the dataset was used, 20% for validation and 10% for testing.
The dataset is not included in this repository, but it can be obtained here: https://www.kaggle.com/datasets/andradaolteanu/gtzan-dataset-music-genre-classification?resource=download
Make sure to delete jazz.00054.wav file, as it is corrupted and will break the training of the model.

## General information for those interested in training the model
As mentioned above, we manually divided the files, and didn't write any code to do it automatically. If you are interested in copying and training the model yourself, be sure to take that into account.
For training, files from {genre}.0000.wav to {genre}.0069.wav were used. < br / >
For validation, files from {genre}.0070.wav to {genre}.0089.wav were used. < br / >
For testing, files from {genre}.0090.wav to {genre}.0099.wav were used. < br / >
Make sure to test the model only on the testing files.

## Results
We trained the model with trimmed song duration to 15 seconds and 50 epochs. The average testing accuracy is around 60%.


## Usage
