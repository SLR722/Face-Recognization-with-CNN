# Face-Recognization-with-CNN

The project has two modules.

The first module is face detection model. The input of this module is a normal image of people and the output of this module is the faces detected in the image. This module can extract the main features for face recognization and remove other features which may disturb face recognization. I used dlib packet based on HOG to implement this module.

The second module is face recognization module. I used transfer learning technology based on VGGFace which is a 16 layers pre-trained convolutional neural network from Visual Geometry Group. I downloaded the dataset from Georgia Tech face database (http://www.anefian.com/research/face_reco.htm), which contains 750 images of 50 people. All people in the database are represented by 15 color JPEG images with cluttered background taken at resolution 640x480 pixels. The average size of the faces in these images is 150x150 pixels. The pictures show frontal and/or tilted faces with different facial expressions, lighting conditions and scale. Additionally, I added another 15 images of one of my classmates to see if I could recognize her face using our model. Then I used 14 images of one people for training and 1 image of one people for testing. So I totally had 714 images for training and 51 images of testing. Based on the output, I finally got validation accuracy = 94.12%. I think the limited amount of training data restricts the model performance.

For more details about the code , you could turn to the face-detection.ipynb and final_project.ipynb.

If you want to run this project on your own PC, you should

-Download the dataset_fetching.ipynb and final_project.ipynb.

-Run dataset_fetching.ipynb to get the dataset from dropbox. After this step, you will have a train folder and a test folder in your current path.

-Run final_project.ipynb to get the output of our project. This step could cost about 20min because of the large amount of data.

If you want to regonize your own face, you should

-Download the dataset_fetching.ipynb, face-detection.ipynb and final_project.ipynb.

-Run dataset_fetching.ipynb to get the dataset from dropbox. After this step, you will have a train folder and a test folder in your current path.

-Extract your face in your photo using face-detection.ipynb and put the face images in the train folder and leave one for validation.

-Modify the last layer of deep learning network to the classes you want to classify.

-Run final_project.ipynb to train the model and use validation image to enjoy the magic of machine learning!!!

