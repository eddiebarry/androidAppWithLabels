# ANDROID WITH YOUR OWN LABELS

A tutorial to create an app that labels camera input according to a provided dataset

## Dependencies :
* Github
* Android Studio
* Tensorflow

To install Android Studio

[Android Studio](https://developer.android.com/studio/)


To install Tensorflow :

```
pip install tensorflow
```

To check if Tensorflow is installed type the following command

```
pip show tensorflow
```

## Train mobilenet on your own data
##### Note :  Sample data has been provided already
To train the model on your own dataset, 
Create sub-folders in the data directory that only contain images from that category
After the images have been placed, navigate to the "retrain" directory from the command line and
Run the following code :-
```
chmod 700 script.sh
./script.sh
```


