# CS440-Artificial-Intelligence

## Group members
```
Group: Zhuoshu Yang, Yifan Wang, Robin Liu, Sameena Bajwa
```

## Project description
### 1. Logistic Regression & Neural Network 2. Gesture Recognition 3. Digit Classification
```
We are designing and implementing a simple neural network and train it on 3 different datasets. Our goals: 
1. Understand how neural networks work. 
2. Implement a logistic regression classifier, and a neural network classifier. 
3. Understand the role of different parameters of a neural network, such as learning rate.
4. Learn how to evaluate a classifier using metrics like classification accuracy and confusion matrices.
```
## Problem Definition
### Design a hand shape and gesture recognition system that detects at least 3 hand shapes and hand gestures. The system should be able to recognize at least 1 static hand shape and 1 dynamic hand gesture.

## Method and Implementation
### 1) Static Hand Shape Recognition:
```
The basic steps and algorithms used are as follows:

· Skin Detection: First capture frames from video stream, and for each stream we subtract out the skin color by turning skin color to white and all other colors to black using mySkinDect function.

· Threshold function: Then we apply the threshold function to turn skin frames to binary frames in order to apply findContour function.

· Find Maximum contour: Next, we use opencv library finContour function to locate the hand. There are potentially many contours in the frame and we want to find the maximum one since the hand is close to the camera.

· Count fingers: Based on the calculated distance from the defect and the center of the hand, we can count the number of fingers in the frame. Hence determine whether it is a Rock, Scissor, or Paper.
```
### 2) Dynamic Hand Gesture Recognition:
```
· Skin Detection: For the task of dynamic gesture recognition, we first find the hand by using MySkinDect, and the frame is turned to binary frame with black and white values.

· Frame to Frame Differencing: The skin frame will then be detected of whether the hand is moving by calculate the difference between each two frames. The difference is trivial if the hand is not moving.

· Motion Energy Templates: With frame to frame differencing, we can accumulate the total difference by using motion energy template. This allows us to tell which direction or orientation the hand is going, so a hand wave can be detected.
```
