# MNIST Digit Recognizer Kaggle Challenge

This repository contains some experiments with the MNIST dataset. The goal
of this project was to create a model, or multiple models, that would perform
'well' on [Digit Recognizer Challenge](https://www.kaggle.com/c/digit-recognizer).
After some trial and errors with different techniques (ensemble and data
augmentation), the obtained result of the best performing combination 
of techniques resulted in an accuracy of 99.585%. 

## Results:
   
Model | Kaggle<br>Accuracy 
------|-----------------
CNN\* | 0.99271
Ensemble with MLP | 0.99342
Ensemble with averaging | 0.99457
Data augmentation | 0.99571
Data augmentation + Ensemble with averaging | 0.99585

\* The exact same one used for the [Doodle Draw project](https://github.com/jurjen96/doodle-draw) 

The best performing model is able to detect 88 images more than a single CNN (with 
no data augmentation). To put it in perspective, the test data contains 28.000 images 
of which 27.796 can be detected with a relatively simple CNN model. A way more complex 
and slower approach is able to correctly predict 27.884 images. Based on the results, 
I would recommend to stick with the simple CNN if the purpose of the project is to 
create something simple and fast and use data augmentation if you want to create 
something a bit more robust.
