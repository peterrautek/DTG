---
# this file is written in YAML http://docs.ansible.com/ansible/latest/YAMLSyntax.html
# all lines with a leading sharp are comments and will not be compiled
# longer blocks of text should start with a a leading > to escape all special characters

# URL handle for generated webpage
slug:      ch01s04

# specifies layout to be used for page generation (do not modify)
layout:     card
---

## Another Word of Warning

With the previous warning in mind: we should acknowledge once more at this point that the _tangent vector_ in differential geometry is quite a bit different from what people often think of as a _vector_.
Once again - a _vector_ is an element of a _vector space_, and the vector space we are concerned with here is quite a bit different than the prime example of the Cartesian coordinate vector space.
Let's try to develop some intuition for our new 'kind of vector' here before we continue with the actual definition of the tangent vector space.

When we look at what will be called the _tangent vector_ $$X_{\gamma,p}$$, then we see by its very definition, it is nothing else than a linear map from all functions to $$\mathbb R$$.
Remember that our manifolds are constructed to be locally similar to $$\mathbb R^{dim(M)}$$, but they aren't $$\mathbb R^{dim(M)}$$. 
So the tangent vector is quite remarkable in that it takes a function (an element of $$\mathcal{C}^\infty(M)$$) and maps it to $$\mathbb R$$. 
The way it is doing this is by taking the derivative (the one we know from calculus, i.e., the one that is defined on $$\mathbb R$$) of the function at a certain point in the direction of a certain curve.

In other words: give me a curve that goes through a certain point on the manifold and I can tell you the derivative of any function in the direction of the curve at this point.
That is precisely the job that defines a tangent vector.

Although this definition might feel superficially complicated or convoluted it fulfills two very remarkable properties:
* We can use this definition on Cartesian coordinates without loosing any results we know from 'old' vector calculus in Euclidean spaces. It is kind of backward compatible.
* We can use this definition on (more general, potentially curved) smooth manifolds to denote directional derivatives.

Without this definition we would simply not know how to write down derivatives on manifolds in general. 
Also the tangent vector is not bound to a specific function. 
It's defined with respect to a point on the manifold. 
So we can (notationally) reuse it to take derivatives for all smooth functions. 

Intuitively, $$X_{\gamma,p}$$ is the _velocity_ or the _change_ along $$\gamma$$ at $$p$$. Consider the curve $$\delta(t):=\gamma(2t)$$, which is the same curve but parametrised twice as fast. 
We have, for any $$f\in \mathcal{C}^\infty(M)$$:

$$X_{\delta,p}(f) = (f\circ\delta)'(0)=2(f\circ\gamma)'(0)=2 X_{\gamma,p}(f) $$
by using the chain rule. Hence $$X_{\gamma,p}$$ scales like a velocity should.

Also note that so far we have identified what we will call a 'tangent vector', but without defining the _tangent vector space_ it is only a name. 
We will now define the tangent vector space and the cotangent vector space which will allow us to talk about tangent vectors and cotangent vectors.
