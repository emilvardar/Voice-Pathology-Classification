# Voice-Pathology-Classification

In this work we used two different dataset. The first one is the Stanford dataset and the second one is the 
German dataset (as they will be called in this paper). The German dataset is mainly used for transfer learning
and the Stanford dataset is the actual goal group that we aim at.

We obtained the Stanford database, created through generous funding from The Voice Foundation’s Advancing
Scientific Voice Research Grant, from Stanford otolaryngology department for this project. This dataset
contains 296 voice samples that have been GRBAS rated by experienced voice professionals [1]. All recordings
were made in a quiet clinical environment using a head-mounted condenser microphone at a 6-centimeter
distance from the corner of the mouth and the Computerized Speech Lab (CSL) using 16-bit encryption with a
sampling rate of 48kHz [1].


As mentioned above the Stanford dataset only contains 296 different voice samples which is a small dataset
for deep learning. Therefore, we started with augmenting the audio files. To start with, we parsed, on silence,
the audio files into smaller chunks. This is accomplished in the voiceNet.ipynb file. The since the dataset
contained very few examples we also used transfer learning. We pre-trained the data on the a German dataset
that has been created for a similar reason and has similar audiofiles as we are interested. This dataset can 
be found at [2]. The pre-training is accomplished in the file 'pretraining_model'.


Finally, the model is trained on the actual dataset in the file 'voiceNet_objective' file. Other trials have been
done in the files 'other_parameters/voiceNet_different_param' and 'other_parameters/voiceNet_sota'. The only 
difference between these three files is that some of the hyperparameters are changed to see how the system behaves 
with differnet parameters. However, the accuracy varies a little between these approaches but overall the accuracy
is still quite high.

All of  the files can be downloaded and run on google Colab. Note though that the files for the stanford and German 
dataset is not uploaded on GitHub. The German dataset can be reached via [2] however, we did not publish the Stanford
dataset because we are not the owners of the files. The results can be seen on notebook.



[1] Patrick R Walden. Perceptual Voice Qualities Database (PVQD): Database Characteristics. Journal of
Voice, 2020

[2] Manfred Pützer and William Barry. Saarbruecken Voice Database. URL: http://stimmdb.coli.
uni-saarland.de/index.php4#target
