# Pyrates Final Project

# American Sign Language Detection using PyTorch

This project will allow you to recognize American Sign Language letters from static images and real time video. American Sign Language data is obtained from Kaggle. In order to
train your model you should download it from https://www.kaggle.com/grassknoted/asl-alphabet.

Dataset consists of 26 letters from American Sign Language and space, delete and nothing classes. There is a total of 87,000 training images - 3,000 images from each class. The
image resolution is 200x200 pixels.

In order to run the program, please download all python files in this directory. Place dataset from Kaggle and python files inside the same input directory. Please consult 
to the file tree .png's for further questions on the directories. 

The model is already trained in our computer and corresponding model (model.pth), binarized labels (lb.pkl) and data file (data.csv) can be found in output file. If you want to use already trained model you can skip to Step 5.

___IF YOU WANT TO TRAIN ON YOUR COMPUTER___

1. Run preprocess_image.py to read, resize and save images.
Can be also run from the terminal python preprocess_image.py --num-images 1200
You can change the number of images that will be selected for the model by changing the last number.

2. Run create_csv.py file to convert images to map the image paths to the target classes.
First column corresponds to the image_path and second column corresponds to the label between 0-28 associated with each image.
This code will create data.csv.

3. Run cnn_models.py
Creates convolutional neural network with four 2D convolutional layers.

4. Run train.py to train the data
Train the dataset and then validate using 15% of the data. This step will give you model.pth, accuracy and loss plots.
You can run it from the terminal by python train.py --epochs 10
You can change the last number to train with less epochs. This will decrease the training time.

___IF YOU WANT TO USE ALREADY TRAINED MODEL___

5. Run test.py to test static hand images.

6. Run cam_test_original.py to test American Sign Language letter in real time.

7. Run cam_test_modified.py to test emojis (Longhorn, Thumbs Up, Thumbs Down, I Love You, OK and Peace) trained using the same dataset.

