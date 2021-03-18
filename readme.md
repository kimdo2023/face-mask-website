# Face Mask Detection
Upload an image or video to detect whether you or someone else is wearing a face mask!

## Description
The Face Mask Detection where it uses facial and object recognition to accurately distinguish those with or without masks. The user would upload an image and the program would analyze it and output whether or not they're wearing a mask. This project is needed to prevent higher risk of spreading the coronavirus and to enforce those who don't follow proper guidelines to wear a mask.

![Thumbnail](/blog/header.jpg)

## Creator
Hello! My name is Kim, a sophomore studying Computer Science at the University of Southern California. I have many interests but currently, I want to explore more in the field of robotics, artificial intelligence, and front-end development. Outside of coding, I love to do digital design, gaming, hanging out with friends, and streaming on [twitch](https://www.twitch.tv/akzelea)! I also have a personal website [here](http://kimhoangdo.com/) if you would like to know more about me.

### Why I Created this Project
I created this project because I wanted to address the problem with people not following the guidelines for wearing face-masks during a global pandemic. It saddens me to see those not putting on masks when needed in public because it causes a higher risk of spreading the virus even more. Thus, I created this project to encourage and enforce people to wear one.

Another reason why I created this project is because like most college students, we want to be able to attend in-person classes as soon as possible and the only way we can go back to our college campuses is for the number of COVID cases to die down. Therefore, I felt that like a project like this can simulate technology that can benefit those who are trying to prevent the virus from spreading as much as possible.

## Project Features
* Python
* Microsoft Azure Functions
* Deep Learning
* Machine Learning
* Google Collaborate
* Front-End
  * HTML
  * CSS
  * Javascript
  * Bootstrap
* Tensorflow API
  *  Keras
  *  OpenCV

## Diagram of Project
![Diagram](/blog/diagram.png)

## Facial and Object Recognition
We need to create the code for the program that reads an image pixel by pixel and uses facial and object recognition to output a frame and percentage on the face in order to detect whether or not the person is wearing a face mask.

I did this part of the project in an environment called google colaboratory. It's a colab, similiar to Jupyter Notebook that allows anyone to write and execute python code through the browser, and is especially well suited to machine learning, data analysis and much more. I also created a repository in github entirely for my code so I can clone it every time I enter back to my colab file.

First, we have to import many different libraries in order for this to work and the ones we need are shown below.

We're using a very basic and simple face detector called the [Haar Cascade](https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_objdetect/py_face_detection/py_face_detection.html) due to my first time playing around with face detection.The Haar Cascade algorithm is a machine learning object detection algorithm which is used to identify objects in an image or video. Instead of creating and training the model from scratch, we use the “haarcascade_frontalface_alt2.xml” to detect faces. It's one of the oldest face detector file applications and it detects the face in a matter of few seconds using machine learning. It's not the best in accuracy but it's one of the fastest. Once the face is detected, then we will use this model file from Keras Tensorflow called mask_recog.h5 to detect masks.

Once we have everything set up, we start the code. First, we need to convert the file into a grayscale image or video and then use our Haar Cascade to detect the faces in the image. However, my code can currently only detect one face at a time. It will output an error if there is more than one face or more than one output (ex. detects one person wearing a mask and one not wearing a mask). 
## Azure Function App

## Front-End Development
