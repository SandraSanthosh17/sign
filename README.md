# Project Title
SIGN LANGUAGE RECOGNITION USINF PYTHON AND OPENCV  
There have been several advancements in technology and a lot of research has been done to help the people who are deaf and dumb. Aiding the cause, Deep learning, and computer vision can be used too to make an impact on this cause.
                                                               This can be very helpful for the deaf and dumb people in communicating with others as knowing sign language is not something that is common to all, moreover, this can be extended to creating automatic editors, where the person can easily write by just their hand gestures.
# Project Overview
In this sign language recognition project, we create a sign detector, which detects numbers from 1 to 10 that can very easily be extended to cover a vast multitude of other signs and hand gestures including the alphabets.We have developed this project using OpenCV and Keras modules of python.###
# Prerequisites
The prerequisites software & libraries for the sign language project are:

-Python (3.7.4)
-IDE (Jupyter)
-Numpy (version 1.16.5)
-cv2 (openCV) (version 3.4.2)
-Keras (version 2.3.1)
-Tensorflow (as keras uses tensorflow in backend and for image preprocessing) (version 2.0.0)
# Download Sign Language Project Code
Download the source code of sign language machine learning project: Sign Language Recognition Project
# Steps to develop sign language recognition project
This is divided into 3 parts:

1.Creating the dataset
2.Training a CNN on the captured dataset
3.Predicting the data
All of which are created as three separate .py files.
![Screenshot 2022-07-08 192300](https://user-images.githubusercontent.com/106008408/178007724-8e004639-9fb3-45b5-8a34-39a0b4c026b8.png)
1. Creating the dataset for sign language detection:
    It is fairly possible to get the dataset we need on the internet but in this project, we will be creating the dataset on our own.

We will be having a live feed from the video cam and every frame that detects a hand in the ROI (region of interest) created will be saved in a directory (here gesture directory) that contains two folders train and test, each containing 10 folders containing images captured using the create_gesture_data.py

Directory structure
![Screenshot 2022-07-08 192437](https://user-images.githubusercontent.com/106008408/178007907-5de8afd0-261b-4686-b84a-2f2534b9515c.png)
Inside of train (test has the same structure inside)
![Screenshot 2022-07-08 192512](https://user-images.githubusercontent.com/106008408/178008000-ad237e00-9df0-47ec-8588-ed4cca0b1c98.png)
![Screenshot 2022-07-08 192544](https://user-images.githubusercontent.com/106008408/178008053-0cf1ce2e-d032-41ec-a35d-52ac05eaf5ee.png)
![Screenshot 2022-07-08 192623](https://user-images.githubusercontent.com/106008408/178008127-78892d86-e5e4-4dd7-b874-254d5ecbb772.png)
![Screenshot 2022-07-08 192709](https://user-images.githubusercontent.com/106008408/178008204-8a011013-faee-4154-9821-e0ec401629a0.png)
![Screenshot 2022-07-08 193031](https://user-images.githubusercontent.com/106008408/178008284-d33b3d9f-4c04-4dc5-b3e6-6da7ee2ee6cb.png)

2.Training CNN
Now on the created data set we train a CNN.

First, we load the data using ImageDataGenerator of keras through which we can use the flow_from_directory function to load the train and test set data, and each of the names of the number folders will be the class names for the imgs loaded.
3. Predict the gesture
In this, we create a bounding box for detecting the ROI and calculate the accumulated_avg as we did in creating the dataset. This is done for identifying any foreground object.

Now we find the max contour and if contour is detected that means a hand is detected so the threshold of the ROI is treated as a test image.

We load the previously saved model using keras.models.load_model and feed the threshold image of the ROI consisting of the hand as an input to the model for prediction.
# Sign Language Recognition Output
![Screenshot 2022-07-08 193116](https://user-images.githubusercontent.com/106008408/178008467-9804cc81-bf29-4a3e-b2ad-552318984c4a.png)

# Summary
We have successfully developed sign language detection project. This is an interesting machine learning python project to gain expertise. This can be further extended for detecting the English alphabets.

