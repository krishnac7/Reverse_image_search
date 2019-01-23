# Feature Extraction and Reverse Image Search on Caltech-101 Dataset

This notebook will guide you throught the process of analysing an image dataset using a pre-trained convolution network (VGG16) and extracting feature vectors for each image

Post analysis we try to demonstrate 'reverse image search' one of the widely popular applications of image analysis. The approach we take is :

* Download [VGG16 pre-trained model](https://keras.io/applications/#vgg16) using keras

* Perform Feature Extraction :
  >Here we remove the last layer ie.,the softmax classification layer so our output model now has only 12 layers and the last layer would be fc2(Dense) a fully connected layer
  
* Get feature vectors for all the images then scale them down using [PCA](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html)

* Use cosine distance between pca features to compare the query image to 5 number of closest images and return them as thumbnails

# Adding Custom Images to the dataset:

Adding custom images is as easy as creating a folder with class name in the extracted dataset folder and adding images of that class

[Run in Colab](https://colab.research.google.com/github/krishnac7/Reverse_image_search/blob/master/ReverseImageSearch.ipynb)    {:target="_blank"}
