---
# this file is written in YAML http://docs.ansible.com/ansible/latest/YAMLSyntax.html
# all lines with a leading sharp are comments and will not be compiled
# longer blocks of text should start with a a leading > to escape all special characters

# URL handle for generated webpage
slug:      ch02s02
toc_entry: The Purpose of Defining a Manifold
# specifies layout to be used for page generation (do not modify)
layout:     card
---

## Multiple Charts Constitute a Manifold

At this point if it is not clear to the reader why we go through all the hassle of defining different charts for a manifold it is a good idea to pause and ponder.
The main motivation for having charts is that for many interesting and very common objects we cannot establish a unique coordinate system. 
To describe one mathematical object (as common as the two dimensional sphere $$S^2$$ for instance) we need multiple coordinate systems. 
In fact the meaning of the word manifold ("of many kinds") stems from this very property that it is not necessarily possible to describe the object with one kind of map.
Although, at first sight this looks like nitpicking or overcomplicated mathematical rigor, 
in practice it will quickly become clear that nothing can be computed without the notion of (multiple) charts and the respective co-ordinates.

In fact one of the most remarkable properties of differential geometry
is to derive and describe facts about manifolds without the use of specific co-ordinates, 
while providing recipes how to compute using different sets of co-ordinates.
So the higher-level mathematical concepts abstract away from a particular choice of co-ordinates, because there isn't a unique choice. Formulating all proofs and facts about a particular manifold using an arbitrary choice of coordinates would be very tedious and repetitive, so facts are described with co-ordinate independent mathematical objects as far as possible and only when it comes to computing on manifolds we resort back to a specific set of coordinates.

One thing that is quite counterintuitive for a novice reader of differential geometry is:
The chart maps at first sight appear to be the computationally useful object. 
But in fact they are merely a mathematical concept that allows us to talk about the manifold. 
The useful objects for computation are the points in $$x(U) \mathbb R^d$$ and the chart transition maps 
that map from $$x(U\cap V)$$ (a subset of $$\mathbb R^d$$) to $$y((U\cap V))$$ (another subset of $$\mathbb R^d$$).

The most important thing to understand at this point is that 
$$y\circ x^{-1}$$ 
is a map from a subset of $$\mathbb R^d$$ to a subset of $$\mathbb R^d$$.
So this map (once composed) _'avoids'_ the manifold in a certain sense, 
and hence makes it possible to compute something in co-ordinates using real numbers.

Remember, the manifold itself cannot (necessarily) be described with one set of co-ordinates, 
and in this sense it does not have (unique) co-ordinates. 
However, when we need to compute something on the manifold we need real numbers and we get them through the 
(composition of) chart maps. More so, once we define specific charts we can derive a bunch of objects (like chart induced bases) that are useful for computations.
