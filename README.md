**CNN_HANDSIGN**
CNN_HS_FK.ipynb---> Training and pre-processing of data
game.ipynb ----> python games

Technology used: Mediapipe and tensorflow

Assests is in here: https://drive.google.com/drive/folders/1Y7V2C_aw-77O0VJ_tHsTPszyUd22mchD?usp=sharing

**Overview:**
A simple game wherein user has to perform the handsign that is presented in the screen in front of a camera. 
The game uses an AI model,CNN(Convolutional Neural Network) that was trained using tensorflow to inference 
images that is cropped by mediapipe through using its own AI model to detect hands. 

Process:
1) Mediapipe inferences images captured by the camera, and with the help of mediapipe, it can detected where the
   hand is in the image and be able to crop it for ease of use for the next few parts.
2) Cropped images are then augmented through a variety of ways:
     - rotation
     - color
   In this way we are eliminating irrelevant data making inferencing of the AI model more accurate. We are only
   concern of the silhouette it produces. Colors and shadows dont matter that much.
3) with augmented done, it will now be inferenced by the trained model for determining what handsign is being presented.
4) The game will display on the screen whether the user is correct or not.

Training:
1) Mediapie made gathering of data a lot more easier and convenient through detecting which part of the picture is the hands
   and being able to crop it at certain sizes for consistency. Therefore we are eliminating irrelevant data in the picture and
   turn our focus on just the hands. In this way it makes inferencing and processing of it more efficient since less data is
   needed to be processed
2)Images collected are storred temporarily into folders.
3) A script is ran to fully automate the augmenting and storing of data to respective folders
4) it is then used to train in tensorflow.
