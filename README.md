# aiml-driving-behaviour-cloning-using-cnn


## Name
Training and Driving a simulator vehicle using Image data and Convolution Neural Network.

## Getting started

Building self-driving models could require a lot of steps starting from gathering data (images, video streams, multiple sensor data from Camera
and other sensors etc). This data collection from real world physical sources could take up a lot of time and effort. 
This could also increase the time taken for testing different versions of the model.

In this sample, we build a simple Convolution Neural Network to only train on Image data and steering input from manual driving. After training this model can be tested by real time inferencing on the simulator with other tracks, parameters, etc.
We also close the loop by letting this model inference on the simulator directly, so that we can see the model driving the car.

This sample just shows the basic flow of doing this closed loop simulation pattern and lets the builders focus of whatever AWS services can be used to scale this. For eg: this sample runs on an EC2 with GPU to do all the data collection, training the model and inferencing on the simulator. In production or scaled up mode, this can be delegated to run on different services such as Amazon S3, Amazon Sagemaker, Containrized Simluator run on EKS etc.

## Dependencies to replicate the samples
The sample has 3  steps:
1. Ingestion (carla-manual-2.py)
        I have used Open source CARLA for the synthetic simulator, however you can use any simulator of your choosing. The objective is to collect Images and steering which are to be input data to the CNN.
        CARLA 0.9.13
        CARLA client (for 0.9.13) 

2. CNN Model (cnn_Track05.ipynb)
        Tensorflow2 (preferably on python 3.9)

3. Real time inferencing on simulator (cnn_control.py)
        CARLA 0.9.13
        CARLA client (for 0.9.13) 
        Tensorflow2 (preferably on python 3.9)



## License
See the LICENSE file

