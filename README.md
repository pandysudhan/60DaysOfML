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



