
This is a simple game that utilizes machine learning where the user performs an alphabet hand sign based on the letter shown on the screen. This game utilizes Mediapipe for feature extraction and Tensorflow for training and inference.

**[Purpose & Goals]**
 - The purpose of this project is to create an accurate hand sign model and to be able to learn the machine learning pipeline along the way which includes data generation, data processing, and training of the model.
   
**[Technologies used]**
 - Tensorflow: Model training and inference.
 - Mediapipe: hand tracking and feature extraction.

**[Features]**
 - Real-time inference

**[Process]**
 - **Data collection**
      1) Mediapipe tracks the hand and extracts relevant features by cropping the image/frame for it only to contain the hand minimizing the data.
      2) Images are saved every certain amount of seconds allowing the user to reposition the hands in various ways.
      3) Images are compiled according to their respective letters
         
 - **Data processing**
      1) Images are augmented to grayscale lessening the data needed to be processed when training.
      2) Images are again augmented by changing their rotation, this is to create a variation of the existing dataset collected creating more dataset for the model
   
 - **Game**
      1) The user is shown a letter
      2) The user performs the hand sign of the respective letter
      3) A time limit is set
      4) Scoring is monitored.
   



      
