# Image Captioning
Image captioning is describing an image fed to the model. The task of object detection has been studied for a long time but recently the task of image captioning is coming into light. 

## Dataset
The dataset used is flickr8k. You can request the data [here](https://illinois.edu/fb/sec/1713398). An email for the links 
of the data to be downloaded will be mailed to your id. Extract the images in Flickr8K_Data and the text data in Flickr8K_Text.

## Requirements
1. Tensorflow
2. Keras
3. Numpy
4. h5py
5. Pandas
6. Pillow
7. Pyttsx

## Steps to execute
1. After extracting the data, execute the preprocess_data.py file by locating the file directory and execute "python preprocess_data.py". This file adds "start " and " end" token to the training and testing text data. On execution the file creates new txt files in Flickr8K_Text folder.

2. Execute the encode_image.py file by typing "python encode_image.py" in the terminal window of the file directory. This creates image_encodings.p which generates image encodings by feeding the image to VGG16 model. In case the weights are not directly available in your temp directory, the weights will be downloaded first.

3. Execute the train.py file in terminal window as "python train.py (int)". Replace "(int)" by any integer value. The variable will denote the number of epochs for which the model will be trained. The models will be saved in the Output folder in this directory. 

4. After training execute "python test.py image" for generating a caption of an image. Pass the extension of the image along with the name of the image file for example, "python test.py beach.jpg". The image file must be present in the test folder.

NOTE - You can skip the training part by directly downloading the weights and model file and placing them in the Output folder since the training part wil take a lot of time if working on a non-GPU system. A GTX 1050 Ti with 4 gigs of RAM takes around 10-15 minutes for one epoch.


