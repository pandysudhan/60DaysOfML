# 60DaysOfML

For the last couple of months I have been reading about materials in Machine learning. While learning, I found it hard to track my progress and notes in one place. So, to be consistent and make my work public, any new topic or old topic that I revise any day for the next 60 days, I will document it in this repo. 

For this project, I am following Deep Learning Specialization Course on Coursera by Andrew Ng.
Any code related to this project will be under code folder.

Machine Learning Roadmap
|Resources|Status|
|----|---|
|https://www.coursera.org/specializations/machine-learning-introduction| ✔|
|https://www.coursera.org/specializations/deep-learning| 🔄 |

---

### Day 1
Deep learning Specialization Course 1: 
Neural Networks

Basic introduction to neural network. As the computational power and size of data grew, it helped the growth of neural network. Traditional ML techniques efficiency usually stopped getting better after certain size of dataset.

There was a question, **does neural network needs many features**?  
=> More features works better if the features are not engineered from existing. Or else, neural network can itself find the hidden relation, we dont need to explicitly feature engineer like for traditional approaches.

## Day 2
In the course, I learned about gradient descent and back propagation again. One topic that made me confused during my first course was why gradient is the direction of steepest ascent. We use this concept in gradient descent and it works, but I wasn't able to find a explanation. [This video](https://www.youtube.com/watch?v=TEB2z7ZlRAw&pp=ygUgZ3JhZGllbnQgZGVzY2VudCBzdGVlcGVzdCBhc2NlbnQ%3D) from Khan academy made the concept clear for me. I am revising the topic today.   
  
Wrote this blog on the topic today in substack.  
[Why is gradient the direction of steepest ascent?](https://pandysudhan.substack.com/p/why-is-gradient-vector-the-direction)


## Day 3
1. I implemented single neuron logistic regression from scratch. It was Course 1 Week 2 programming assignment. The code is available [here](https://github.com/pandysudhan/60DaysOfML/blob/main/code/Logistic_Regression_with_a_Neural_Network_mindset.ipynb)

2. Learned about vectorization with numpy.
    - numpy.dot()
    - numpy.multiply()
    - numpy broadcasting

Need to look: np.matmul() vs np.dot(), both do similar matrix multiplication that I know as of yet. But there is some difference in higher dimension.

## Day 4
Today was very interesting. I implemented the one hidden layer from scratch with complete forward and backward propagation.
The code is available [here](https://github.com/pandysudhan/60DaysOfML/blob/main/code/Planar_data_classification_with_one_hidden_layer.ipynb)  

**Gradient descent** has become one of my favorite topics now.

<img width="723" alt="Screenshot 2024-03-02 at 9 43 53 PM" src="https://github.com/pandysudhan/60DaysOfML/assets/83126616/92781458-e5e2-46eb-9797-5c1d1d22a342">


## Day 5
The neural network is getting interesting day by day. Today, I implemented a 'L' layered neural network as the final submission for the first course in Deep learning specialization.

The flow of the functions for forward and back propagation, I used in the implementation is:  

[Implemetation code](https://github.com/pandysudhan/60DaysOfML/blob/main/code/Logistic_Regression_with_a_Neural_Network_mindset.ipynb)  
[Application](https://github.com/pandysudhan/60DaysOfML/blob/main/code/Deep%20Neural%20Network%20-%20Application.ipynb)  

<img width="528" alt="Screenshot 2024-03-08 at 10 15 37 AM" src="https://github.com/pandysudhan/60DaysOfML/assets/83126616/3d01b13f-893a-41ce-8b6c-abbaea2de344">

<img width="542" alt="Screenshot 2024-03-08 at 1 33 33 PM" src="https://github.com/pandysudhan/60DaysOfML/assets/83126616/bce6ae3e-3bbb-4a15-9489-c5f35d77c982">


## Day 6
Convolutional Neural Network
I started the new course in the deep learning specialization: CNN.
Concept:
Take a 2D/ 3D array (filter) and convolve it around the given dataset. Usually the dataset will be represented as 2d/ 3d array like for images.
A particular filter is used for particular feature extraction from given large feature set, and when multiple filters is used, we get data for specific feature at specific part of the original dataset. For example the presence/absence of a white line in a image.  

**Convolve**: The operation is simply a slice of original dataset of same size as filter and taken element wise product i.e the weighted values. This is repeated to all the remaining data, using same filter.

These filters need not be defined before hand, and it is what the model is supposed to learn.

CNN solves a major problem for large features dataset like images, the need to have many parameters. Using CNN, same set of parameters could be reused at multiple places. For example, as above, the filter used for presence of white line is used at all the parts of image, and thus we have the positions of all the white lines in an image.

## Day 7

When we perform convolution in a dataset, the output activation array size is smaller than input. The reason being, convolution will stop when the remaining data is smaller than the filter size. Like, if filter size is 3x3, and we are at 2nd last column, the operation cannot be perfomed and hence the last two operations (slice starting at last two columns) are skipped. 
To solve this, use a simple padding around the dataset, so that, when the columns are skipped, the padding would be skipped rather than the actual important values.


Output activation sizes after a convolution layer:  

P = padding,  
s = stride,  
f = filter size  
<img width="605" alt="Screenshot 2024-03-17 at 10 38 02 PM" src="https://github.com/pandysudhan/60DaysOfML/assets/83126616/ccb66114-a64e-4a0f-9ea5-a6cf40709cba">

Pooling: 
Usually required to decrease the dimension of the dataset/activations. Max/ avg pooling is done, so that rather than the exact location of a feature, a large area of where the occurence of that feature is likely, is taken as the activations. This way if the feature is translated just a little, it will have similar result. So, for identifying a left ear for a animal, as long as it is in the upper left area of a straight face, we will have a good result, rather than requiring exact position.


I implemented the forward propagation of CNN model(Week 1 Lab). The code can be found [here](https://github.com/pandysudhan/60DaysOfML/blob/main/code/Convolution_model_Step_by_Step_v1.ipynb).   

