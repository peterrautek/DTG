---
# this file is written in YAML http://docs.ansible.com/ansible/latest/YAMLSyntax.html
# all lines with a leading sharp are comments and will not be compiled
# longer blocks of text should start with a a leading > to escape all special characters

# URL handle for generated webpage
slug:      ch01s01zoo
toc_entry: Smooth Functions and Curves
# specifies layout to be used for page generation (do not modify)
layout:     card
---

## Smooth Functions and Curves

The by far larger section of our zoo has a collection of animals from the family of maps. A map is a very general concept in mathematics, but they all have in common that they take something as input and give in return something as output. The input and output might be of the same species or an entirely different animal. In our zoo we are only concerned with maps that live on Riemannian manifolds. 

Let’s start by looking at one of the more familiar species, the continuous function.
A continuous function will give us a scalar number at each point on the manifold. 

We can think of the function as something that takes a point as input and gives a number as an output. The specialty of a continuous function is that when we move the input point continuously it will produce a continuous output. That is to say that we will not be able to move a point around and discover jumps in the output value of the function. Let’s have a closer look at this property: If we take two points close to each other the continuous function will give us two different values from the real numbers. These two values get closer to each other when we move the points closer. However, for two points, no matter how close, the function might always return two different values. Since these values are from the real numbers there are infinitely many other numbers between them. That does certainly look like a jump. Therefore the property continuity (the property of not having jumps) is precisely defined a little bit different: It is formulated like this: You give me a point and tell me a value that is so small that you would accept it as not being a jump (let's call this value epsilon), then I can guarantee you that by moving the second point closer, that the function will return two values which are below epsilon. We call a function continuous when it fulfills this property no matter how small your epsilon is. 

The idea of a moving point is a very powerful and important concept in geometry. More specifically we are interested in curves which are the trajectory of a continuously moving point. We can think of a curve as an animal that lives on the manifold. It takes a scalar parameter as input and produces a point. Continuously varying the parameter produces a continuous curve of points. 

Since a curve is continuous it has a tangent at every point along the curve. The tangent is a purely geometric object that has a direction. When we change the curve the tangent might point in a different direction. 
