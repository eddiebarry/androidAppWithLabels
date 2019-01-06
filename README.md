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
###### Note :  Sample data has been provided already
To train the model on your own dataset, 
Create sub-folders in the data directory that only contain images from that category
After the images have been placed, navigate to the "retrain" directory from the command line and
Run the following code :-
```
chmod 700 retrain_on_data.sh
./retrain_on_data.sh
```
###### Note :  To change the default android model change the arhitecture tag in the script.sh file. For more information refer to : [Tensorflow Tutorial](https://codelabs.developers.google.com/codelabs/tensorflow-for-poets/index.html?index=..%2F..index#3)

##### Important : Copy and paste the "retrained_graph.pb" & "retrained_labels.txt" files to the convert folder.


## Convert Tensorflow graph to .lite format for use in android app
Navigate to the "convert" directory from the command line and
Run the following code :-

```
chmod 700 convert.sh
./convert.sh
```

###### Note : This conversion has been set for the mobile_net architecture. To convert for different architectures, the input output parameters need to be changed in the ./convert.sh script. For more information, refer to [Tflite Converter](https://www.tensorflow.org/lite/convert/)

##### Important : 
* Copy and paste the "optimised_graph.lite" & "retrained_labels.txt" file to the "assets" folder present in the "android_app" directory
* Rename "optimised_graph.lite" to "graph.lite" & "retrained_labels.txt" to "labels.txt";

## Build and run android app
Open the "android_app" directory as an existing project in android studio.
Build and run

### Screenshots : 

![SC1](https://github.com/eddiebarry/androidAppWithLabels/blob/master/screenshot_dent.jpeg)
![SC2](https://github.com/eddiebarry/androidAppWithLabels/blob/master/screenshot_no_damage.jpeg)
![SC3](https://github.com/eddiebarry/androidAppWithLabels/blob/master/screenshot_scratch.jpeg)
![SC4](https://github.com/eddiebarry/androidAppWithLabels/blob/master/screenshot_scratches_2.jpeg)


### Credits : 

Tutorials from ![TFLOW for poets 1](![SC1](https://github.com/eddiebarry/androidAppWithLabels/blob/master/screenshot_dent.jpeg))
Tutorials from ![TFLOW for poets 2](https://codelabs.developers.google.com/codelabs/tensorflow-for-poets/index.html?index=..%2F..index#0)








