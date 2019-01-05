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

##### Note :  To change the default android model change the arhitecture tag in the script.sh file. For more information refer to : [Tensorflow Tutorial](https://codelabs.developers.google.com/codelabs/tensorflow-for-poets/index.html?index=..%2F..index#3)

### Important : copy and paste the "retrained_graph.pb" & "retrained_labels.txt" files to the convert folder in the root directory.



