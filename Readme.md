# Character Recognition WebApp
I built a character recognition web application (currently only digits) which let's you draw a random digit on HTML canvas and let deep ConvNet predict what you have drawn. The application is hosted on Flask.

1.png            |2.png            |3.png            
:-------------------------:|:-------------------------:|:-------------------------:
![](https://bitbucket.org/ishaan2020/digitpredictor/raw/b5e7933077024f678ed395a8855e44abd43904f8/screenshots/5.png)  |  ![](https://bitbucket.org/ishaan2020/digitpredictor/raw/b5e7933077024f678ed395a8855e44abd43904f8/screenshots/2.png)  |  ![](https://bitbucket.org/ishaan2020/digitpredictor/raw/b5e7933077024f678ed395a8855e44abd43904f8/screenshots/9.png)

If you want to Explore and see the Live App: Feel free to contact me: igupta967@gmail.com.  

## Getting Started
Here I will explain how to train the model, also how to setup the app running in your own environment. Also I will try to explain basics of Convolution Neural Network.

### Prerequisites
For Package Installation and Management i used the Following Requirements.txt file in this Project.
> pip install -r requirements.txt

### Model Training
In Order to train ML Model for this project, I implemented it on CNN_model.ipynb and saved my model of highest accuracy into .h5 file.

### Running the app
For Running the App Run the app.py file from the app directory through following command:
!python app.py 

## Future Improvements

1.Similarly like this Full stack Project, The other project can be Go-Live that will recognize and predict shapes which will be drawn in a canvas by user and drawing will be predicted.
2.The adjustments will be made on the pipelines and overall architecture of the project on the given Use Case.
3. Extension of features will be made such as app will give shape names to users which needs to be drawn in canvas, then delivery of Results will be done by the App.
4.App will also detect will User draws different drawing and what that drawing represents and what should have been drawn.

## Convolutional Neural Network
Convolutional Neural Networks, like neural networks, are made up of neurons with learnable weights and biases. Each neuron receives several inputs, takes a weighted sum over them, pass it through an activation function and responds with an output. The whole network has a loss function and all the tips and tricks that we developed for neural networks still apply on Convolutional Neural Networks.

There are four layered concepts we should understand in Convolutional Neural Networks:
1. Convolution,
2. ReLu,
3. Pooling and
4. Full Connectedness (Fully Connected Layer).

**Convolution**: Convolution has the nice property of being translational invariant. Intuitively, this means that each convolution filter represents a feature of interest (e.g pixels in letters) and the Convolutional Neural Network algorithm learns which features comprise the resulting reference (i.e. alphabet).
We have 4 steps for convolution:
* Line up the feature and the image
* Multiply each image pixel by corresponding feature pixel
* Add the values and find the sum
* Divide the sum by the total number of pixels in the feature

**ReLu**: ReLU is an activation function. Rectified Linear Unit (ReLU) transform function only activates a node if the input is above a certain quantity, while the input is below zero, the output is zero, but when the input rises above a certain threshold, it has a linear relationship with the dependent variable.

**Pooling**: In this layer we shrink the image stack into a smaller size. Pooling is done after passing through the activation layer. We do this by implementing the following 4 steps:
* Pick a window size (usually 2 or 3)
* Pick a stride (usually 2)
* Walk your window across your filtered images
* From each window, take the maximum value

**Fully Connected Layer**: So to get the time-frame in one picture we can reduce the image size after passing the input through 3 layers.
We can further reduce the image to something lesser. We need to perform the 3 operations in an iteration after the first pass and so on. 
The last layers in the network are fully connected, meaning that neurons of preceding layers are connected to every neuron in subsequent layers. Also, fully connected layer is the final layer where the classification actually happens. Here we take our filtered and shrinked images and put them into one single list.

## Developer
* Ishaan Gupta More Projects:(https://github.com/igupta967937?tab=repositories)


## References
1. [Analytics Vidya Explaination](https://www.analyticsvidhya.com/)
2. [Edureka article](https://www.edureka.co/blog/convolutional-neural-network/)
