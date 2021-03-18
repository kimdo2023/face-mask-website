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
  * JQuery
  * Bootstrap
* OpenCV
* Tensorflow API
  *  Keras

## Diagram of Project
![Diagram](/blog/diagram.png)

## Facial and Object Recognition
We need to create the code for the program that reads an image pixel by pixel and uses facial and object recognition to output a frame and percentage on the face in order to detect whether or not the person is wearing a face mask.

I did this part of the project in an environment called google colaboratory. It's a colab, similiar to Jupyter Notebook that allows anyone to write and execute python code through the browser, and is especially well suited to machine learning, data analysis and much more. I also created a repository in github entirely for my code so I can clone it every time I enter back to my colab file.

First, we have to import many different libraries in order for this to work and the ones we need are shown below.

We're using a very basic and simple face detector called the [Haar Cascade](https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_objdetect/py_face_detection/py_face_detection.html) due to my first time playing around with face detection.The Haar Cascade algorithm is a machine learning object detection algorithm which is used to identify objects in an image or video. Instead of creating and training the model from scratch, we use the “haarcascade_frontalface_alt2.xml” to detect faces. It's one of the oldest face detector file applications and it detects the face in a matter of few seconds using machine learning. It's not the best in accuracy but it's one of the fastest. Once the face is detected, then we will use this model file from Keras Tensorflow called mask_recog.h5 to detect masks.

Once we have everything set up, we start the code. First, we need to convert the file into a grayscale image or video and then use our Haar Cascade to detect the face in the image. Note, my code can currently only detect one face at a time. It will output an error if there is more than one face or more than one output (ex. detects one person wearing a mask and one not wearing a mask). Once the images and faces are identified, you send it out to the mask detector application. We basically pre-processed the image in order to meet the requirements for Haar Cascade application. Now, we send that image to a predictor file through the model_recog.h5 OpenCV file and the rest of the code is basically it creating a frame around the face of the person and outputting a percentage as well. A person wearing a mask will be labeled with a rectangular green frame with a high percentage (most likely between 95%-100%) and a person not wearing a mask will be labeled with a rectangular red frame with a low percentage (< 90%). 

Finally, we just give the program what file we want it to read and we do that by inputting it and then showing it on google colab through the imshow library. The image output  function code is very simple but the video output function is more because it needs to detect each frame and gives us a file output (due to google colab not having a live server to allow us to watch a video). Thus, there would be a generated output file for the video. Thus, our working code is created and now we need to connect it to our front-end for others to use it.

## Front-End Development
Due to time contraints, I was inspired by a particular design and used a template and modified it to my own in order to make my website application. Below is an overview of what my overall website looks like. I used HTML, CSS, Javascript, JQuery, and Bootstrap to create and modify my website. 

### Layout of Website
1. **Homepage:** Main page that demonstrates my title, logo, navigation bar, and an iconic carousel for important reminders and relevant information.
2. **Demo Page:** To demonstrate the easy and simple steps of how to upload an image or video to create an output.
3. **Upload Page:** The area where the user will upload their image and video and the output will display back with a frame and percentage that shows if the person is wearing a mask or not.
4. **About Page:** The project description, information, and future discussion are posted there.
5. **Gallery Page:** A carousel containing lots of images that I tested out to show some samples of what similar results could be produced.

### Static Web App
We had to use static web app in order to deploy our website. Here is a link to my website: https://gentle-meadow-05bb21c1e.azurestaticapps.net/

### Uploading File
We would need to create two buttons to wear we can pick or upload our chosen image or video file and then creating a submit button in order to send the data to our HTTP trigger. Once it does that, it goes through the face mask detection functions that we created and await for our JSON response to bring back the image or video with whether or not the perseon is wearing a mask.

## Azure Function App
Now we need to create a Microsoft Azure function to call the API, face detector function, and front-end image in order to read the uploaded file from the user. First, I went on my portal and created a entirely new function. Below are the settings I used but they can vary for others. 

Then, after creating the function, I went on Visual Studios and installed the necessary extensions (such as Azure Functions) and uploaded the files I wanted to put in my function. Then I deployed it from VS code to the portal and thus, it successfully connected. There were definetely errors in terms of installing the correct libraries and such but I was able to fix most of it. After it was done connecting, I used Postman to test it out as well and it worked! Now, it became the matter of trying to figure out how connect it to my front-end as well. 

##




