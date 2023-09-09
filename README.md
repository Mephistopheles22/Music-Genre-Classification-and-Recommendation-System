# Music-Genre-Classification
### Introduction
The Music Genre Classification and Recommendation System is an innovative machine-learning project aimed at classifying music genres and providing personalized song recommendations based on a user's preferences. This project leverages the power of the Support Vector Machine (SVM) algorithm for genre classification, utilizes the librosa library for feature extraction, employs the Random Forest algorithm to select important features, and recommends songs from a self-created CSV dataset.
### Project Goals
1. Music Genre Classification: The primary goal of this project is to accurately classify music tracks into predefined genres. By training an SVM(Support Vector Machines) classifier on a dataset of labeled music samples, we aim to develop a model capable of automatically categorizing songs into genres such as rock, jazz, hip-hop, classical, and more.

2. Feature Extraction: To effectively classify music genres, we will use the librosa library to extract relevant audio features from music tracks. These features may include but are not limited to tempo, spectral centroid, chroma feature, and mel-frequency cepstral coefficients (MFCCs).

3. Feature Selection: We will employ the Random Forest algorithm to identify and select the most important features for music genre classification. This step will help improve the model's accuracy by focusing on the most discriminative audio characteristics.

4. Song Recommendation: Once a user provides input regarding their musical preferences, the system will classify their favourite genre(s). Based on this classification, the system will recommend songs from a curated CSV file containing a collection of songs and their associated genres.
### Methodology
The proposed system classifies music genres using SVM and recommends songs from the same genre as the expected genre. The SVM model extracts and pre-processes audio properties from the input audio file, which are then utilised to categorise genre.
##
For training, the model uses a labelled dataset with audio attributes. The system can accurately identify the genre of a given audio input by utilising SVM's classification capabilities. This genre classification can then be used to offer songs that fit the user's favourite genre, resulting in a more personalised and engaging listening experience. This is accomplished by traversing the song dataset using the expected genre. 
##
The model takes in a .wav audio file and extracts various audio features. 
Various metadata features are extracted from the input audio file using the Librosa library. These features include onset strength, tempo, beat position, chroma feature, root mean square energy, spectral centroid, spectral bandwidth, spectral roll-off, zero-crossing rate, and Mfcc1-Mfcc20. Then random forest is used for feature selection, by comparing feature importance. These extracted features are stored in an array, which is then scaled and used by the SVM model to predict the genre.
These features are used to train the model on a labelled dataset.
##
To avoid some features from dominating others when training our distance-based SVM model, MinMaxScaler is used to perform feature scaling on the input data. The SVM model is then trained using this scaled data.
##
The SVM method would use the retrieved features to find a hyperplane in the feature space that maximises the margin between the different classes (i.e., music genres). To categorise a new audio sample, we would extract its characteristics and preprocess the data similarly to the training data. The preprocessed feature vector would then be fed into the SVM classifier, which would utilise the hyperplane learned during training to predict the genre label of the audio sample. A song's labelled genre is utilised as a crucial component in recommending other tracks in the same genre. 

### Conclusion
The Music Genre Classification and Recommendation System will enable music enthusiasts to discover new songs that align with their musical tastes. By leveraging machine learning algorithms and feature engineering techniques, this project aims to enhance the music listening experience and showcase the capabilities of data-driven music classification and recommendation systems.
