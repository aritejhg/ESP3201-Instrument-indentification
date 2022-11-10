# ESP3201-Instrument-indentification
This repository contains the code used for downloading the OpenMIC dataset, converting the original OGG files to Log-Mel and Gammatone spectrogram, and training a simple CNN classifier on the spectrogram data using Tensorflow.

## Folders
### data pre-processing
1. data_preprocessing_logmel_studio.ipynb
    * conversion of OpenMIC OGG audio clips to Log-Mel spectrogram png files. 
    * uses the [librosa.feature.melspectrogram](https://librosa.org/doc/main/generated/librosa.feature.melspectrogram.html) function from Librosa library
2. data_preprocessing_gammatone_studio.ipynb
    * conversion of OpenMIC OGG audio clips to Gammatone spectrogram png files.
    * uses a FFT approximation of the actual Gammatone filter bank, referenced from [Gammatone Filterbank Toolkit](https://github.com/detly/gammatone) by Jason Heeris, João Felipe Santos and Kirit Thadaka
3. dataset_utils.ipynb
    * analysis of the dataset including: number of observed labels per sample, number of unobserved labels, and number of responses per sample label. 

### training
1. attention_openmic_training.ipynb
2. training_edited.ipynb
3. training_gamma_VGG11.ipynb
4. training_logmel_VGG11.ipynb
