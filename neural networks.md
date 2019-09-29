---
layout: page
title: Neural Networks
---

<h2><u>Northwest Advanced Programming Workshop Project</u></h2>

In the summer of 2019, I participated in the Northwest Advanced Programming Workshop at Portland State University. I worked in a team with Emily Beecher, Griffin Walraven, and Allie Surprise to create a handwriting analyzer using neural networks. Our goal as a group was to create software that could take two images of handwriting, analyze them using neural networks, and then come to a prediction whether the two samples were written by the same person. 

<h3>View and test out our project!</h3>

All the code our group wrote for the camp is currently <a href = "https://github.com/patrickhuang112/HandwritingClassifier">hosted on GitHub</a> Instructions on how to run the GUI, handwriting classifier, and other features are described in detail on the README. Go check it out!


<h3>A little history of what I did</h3>
<h4>The first two networks:</h4>
Griffin Walraven and I worked on the neural network components of the project. We first created a simple neural network for the project. The network would resize all data into 32x32 sized images and flatten them into 1x1024 image. The flattened image would be fed into an input layer with 1024 neurons and go through two hidden layers with 512 and 256 neurons respectively before being output into a final layer with two different possible results: 'true' or 'false'. The main problem with the simple neural network was that it overfitted according to the training data. It was highly effective at predicting true vs false using different samples from the training set. However, testing the simple neural network using samples written by team members exposed the overfitting tendency of the network.

This neural network was eventually replaced by a convolutional neural network. We sought to implemenet a convolutional network to increase the reliability and accuracy of the network. The advatage of a convolutional network is that it would analyze sections of the input data instead of individual pixels, granting a stronger ability in recognizing patterns within images. The convolutional network was successful in lessening the overfitting from the simple network. However, it was still prone to inaccurate results as a result from overfitting and reliance on the training data.

<h4>The final network:</h4>
The final network we decided upon was a siamese neural network. A siemese network differs from most because it starts out as two seperate but identical networks with two seperate input layers and they merge before the output layer. This is great for comparison tasks such as facial recognition and also useful for one shot learning. This network coupled with a change in our dataset resulted in a model with 84% test accuracy and no overfitting! This network was also the best on user submitted images.

<h4>Other Features</h4>
The team created a website and a graphical user interface (GUI) to allow users to test out the neural network in a simple way. Both the website and the GUI has a "predict" tab where users can test out the neural network. Users upload two different images of handwritten words or letters and then click the "Submit" button. When using the website, the two images will be combined and will redisplay on the website with a "true" or "false" prediction along with a prediction certainty percentage. When using the GUI, the user will also have to submit images using the same process. However, the new combined image will display in a new window along with the prediction results.

The team also implemented the pytesseract library which allows analysis of words within images. Within the website and GUI, a user is able to upload an image with handwritten or typed words and the Graphology APE will analyze the image and return with the words it reads in the image. There is also a word find feature where instead of returning all words found within an image, GAPE will return the number of instances of a specific user-defined word.