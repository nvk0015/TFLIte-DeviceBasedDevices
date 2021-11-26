# TFLite-DeviceBasedDevices

# The TFLite-FashionMNIST
It is an ipython file, this programm has been developed as a reference to convert complex, heavy built TensorFlow models to a simple, less weight TFLite format to further make it feasable for interpreting on Edge devices. 
While observing this file, one can make sure that the size of trained model is drastically reduced, reducing the latency with very little model degradation. This proves that the TFLite files, which are quantized, and in flat buffer format can be further used for inferencing on Mobiles and Microcontrollers like Raspberrypi. 

# android_apps 
A sample inference on Andoid device can be made using the files in this folder. Visit this link for detailed doccumentation https://www.tensorflow.org/lite/guide/inference#android_platform
Tips:
1. Add the TensorFlow dependency to build.gradle file
2. To use the Anfroid Neural Networks API, Call the setUseNNAPI method on the interpreter and set its parameter to true.
3. The configuration of number of Threads the Interpreter uses can also be made calling the SetNumThreads method
4. For better purposes store the TFlite ML models in assets folder of the Android app

# ios_apps
Similar to mobiles running on Andoid os, the TF models can be deployed to interpret on ios platform. 
The steps involved are same, train a custom TF model, convert them to TFlite format after post training quantizations and interpret on ios devices using Swift programming language.
Tips:
1. To deploy model in ios for offline users add the model as part of app bundle
2. The images in ios memory are in CVPixel buffer format, remove the alpha channel, resize and pass the image to TFLite interpreter.
3. InterpreterOptions can be used to specidy the Thread count

# Raspberrypi
Raspberrypi can be used for both Trainign  and inference on TF models 
There are several options to install TensorFLow on the Raspberrypi based on our purpose.
1. Building TF from source
2. Installing the Tensorflow from Pypi repo#
3. Installing the TensorFlow interpreter - best for inference purposes

Example scripts to run the TFlite models in realtime on Raspberrypi are pushed to image_classification, and object_detection folder.
