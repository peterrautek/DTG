---
# this file is written in YAML http://docs.ansible.com/ansible/latest/YAMLSyntax.html
# all lines with a leading sharp are comments and will not be compiled
# longer blocks of text should start with a a leading > to escape all special characters

# URL handle for generated webpage
slug:      ch01s02

# specifies layout to be used for page generation (do not modify)
layout:     card
---


## A New Animal in the Zoo

So far these animals should all look quite familiar. However, the next animal in the zoo might be a little more surprising. The name of the animal should sound familiar but when we inspect it more closely it has a few surprising properties. The animal is called a tangent vector. A tangent vector lives at the tangent space - a space at a specific point of a manifold. The space is defined by means of all possible tangents to all possible curves through that point. The surprising thing might be that a tangent vector is not the same as a tangent. It is not a geometrical object but a function - a linear map - that eats a continuous function and produces a real number. A specific tangent vector animal lives at a certain point and has the curve built into it. When we give it a continuous function it will produce a number by calculating the derivative of the function along the curve. I would argue that this is a weird animal - and that it only lives through the virtue of a specific point on a specific manifold and a specific curve through that point. But we are not here to judge animals - we are here to get to get to know the zoo!

The species of tangent vectors is particularly interesting and we should have a closer look at it. We depart from our perspective as a zoologist and take the role of a functional biologist. How does the tangent vector work, specifically how does it digest a continuous function and turn it into a real number. The organ that is responsible for this function is the differential structure. The differential structure takes a point on a manifold, a curve that goes through it, and a continuous function. It combines them in such a way that the number it returns is the derivative of the function at the given point along the given curve. 

If we look at it mathematically the differential structure borrows its functionality from elementary calculus - remember - we can do that because locally we can treat the manifold as a flat space. 
