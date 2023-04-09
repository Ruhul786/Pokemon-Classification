# Pokemon-Classification
Pokemon Classification using Keras

## Problem 
# Client wants a model where it should classify the image as Pikachu, Balabasaur
# or Charmandar. These are few of the types of pokemon https://en.wikipedia.org/wiki/Pok%C3%A9mon
# This is case of multiclass classification
# The client want us to build a model so that if image is given to model, it should say that
# it is Pikachu, Balbasaur or Charmanadar


## Challanges faced

#1) Does Client has enough Dataset - No, only 4-5 images.

#2) How to get dataset
# We need atleast 400-500 images (lot of images)
# The image should also have label.
# Solution - We have written python code. Inside that we called 
# Binge API (from Microsoft) for downloading the dataset.
# the image of Pokemon has 3 types mentioned.
# This way we could download 500 images (150 - Pikachu, 150 -Balbasaur, 200 - Charmandar)

#3) Data storage 
# We have created dataset folder under mydrive
# We stored the dataset in google drive
# We can train the model in colab
# Based on Keras doc, we organized a data in such a way that training is posiible.
# Created under my drive folder datset folder, under that created 
# training_set and test_set
# Under training_set created 3 folders - pikachu, balbasaur and charmandar
# Inside these folder we hae saved the related images.
# These folder name will act as a label. eg. image inside balbasaur folder will
# have balbasaur label. Similarly this the case with other image.
# This is the way in which keras read data otherwise it will not understand which
# image will have which label.

#4) Othes issues faced

# 4.1) Resize 
# There is variation in size of images. For example resolution for some 
# images are 150*150, 200*200, 80*80, 400*350 etc.
# With different size we cannot train the model
# We have done rescaling. 


# 4.2) Depth 
# Since colored image, depth =3 (RGB Format , for black white, depth = 1)
# We have make depth 3 for all images

# 4.3) CNN model has less images in dataset
# To overcome this issue we have done data augmenatation
# for example we can generate more image from exiating image by performing 
# various activities - zoom in, zoom out, 180 degree Flip, Rotation, Shear, Crop etc.
# So with above activities we can get new images count as = 500*6 = 3000
# We will do data augmenatation for traning dataset
