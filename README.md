## Deep Learning - Sequence Model Application

This repository contains my implementation of the use case of Sequence Models, which I learnt while taking an online course on Deep Learning and Neural Networks.

# Trigger word detection

Trigger word detection is the technology that allows devices like Amazon Alexa, Google Home, Apple Siri to wake up upon hearing a certain word. In this project we use the trigger word as "activate" to be detected in any recorded audio in .wav format. The recorded audio is first converted into its sprectrogram, a time-frequency plot extracted using Fourier Transform over the time series audio file. Fourier Transform applied frequency window on each of the time frame and converts it into Frequency signal. We need the Spectrogram in order to be able to do the analysis on the numbers easily. 
Sequential Model consisting of Gated Recurrent Unit is then trained on those spectrogram values of the Overlayed audio files. (Instead of taking a complete 1 single audio of noise and trigger word, we create the file by overlaying separately recorded Trigger words, non- trigger words onto the background (our case 10 ms). 
The model is implemented on Keras, I have used Google Colab for training and implementing the model alone, while the other preprocessing step is done on my local machine. 
Once the model is validated, it is tested on my_rec file.

The data folder is quite huge and thus is available in the **release** section as an easily downloadable zip file.
