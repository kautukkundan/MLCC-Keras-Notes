# Binary image classification app
Can also be trained on your own dataset. 

### DATASET DOWNLOAD INSTRUCTIONS

##### 1. Download Dataset
[Click here](https://www.microsoft.com/en-us/download/confirmation.aspx?id=54765) - Link to dataset
##### 2. After Downloading 
 - Make a new folder like this ```./cat_dog_classifier/Datasets```
 - Unzip and Paste "Cat" and "Dog" folder from dataset into this folder 

### Order to be followed

1. **01_Creating_Dataset**
-- preprocesses the downloaded images, converts them to 50x50 pixel in size, converts them into array and saves them in X.pickle file for further use
-- also generates labels (0 for Dog and 1 for Cat) and stores into y.pickle file

> IMPORTANT 
> This folder already contains a compiled dataset from images, Delete the files `X.pickle` and `y.pickle` before running the `create_dataset()` function otherwise the files will be overwritten and you'll end up with double amount of training points

2. **02_ConvNet_keras**
-- Construct a CNN model, train it on the dataset
-- save the model

> IMPORTANT 
> This folder already contains a trained model on cat and dog dataset named `64x2_CNN.model`. change the name of this file if you want to train your own model.

3. **03_Using_model**
-- Use the saved model and your custom images to classify them into classes.
-- two images 'Dog.jpg' and 'Cat.jpg' has already been provided in the folder.

---

### Train the model on your own dataset
1. Download atleast 5000-7000 images of each class of objects you want to classify, Store them in 2 separate folders under the folder `Datasets`.
2. Change the Categories array in the **01_Creating_Dataset** file and run the function. Also change the name of pickle files or your data will be appended to cat and dog dataset.
3. Make changes in the **02_ConvNets_keras** file, change X and y to your labels and features, change epochs to atleast 10-15, call `model.fit`, sit back and relax while model trains.
4. After training is complete, use other images to test your model in **03_Using_model** file
5. CONGRATS! You created your own classifier