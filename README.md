Pyrates Final Project

Please download all the files in this directory and download the dataset from https://www.kaggle.com/grassknoted/asl-alphabet. Place the two folders inside the
input directory. Please consult the file tree .png's for further questions on the directories. 

___IF YOU WANT TO TRAIN ON YOUR COMPUTER PLEASE HAVE THE FOLLOWING PACKAGES INSTALLED___

Pytorch
Imulits – to get proper image paths
Albumentations 
cv2 – to read and preprocess images
OpenCV
Numpy
Pandas
matplotlib

___TO TRAIN RUN THE FOLLOWING FILES IN THE FOLLOWING STEPS (paranthesis describes what they do)___

preprocess.py (Read, resize (224x224 pixels) and save the images)
create_csv.py (Maps image paths to the target classes, writes data into a data frame and save as a CSV file, creates binarized labels lb.pkl)
cnn_models.py (Creates our convolutional neural network)
train.py (Train the network using a computation device (GPU or CPU), Calculate and plot epoch’s loss and accuracy)
test.py (Test static images)
cam_test.py (Test sign language recognition in Real-Time from Webcam Feed)
