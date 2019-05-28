---
# this file is written in YAML http://docs.ansible.com/ansible/latest/YAMLSyntax.html
# all lines with a leading sharp are comments and will not be compiled
# longer blocks of text should start with a a leading > to escape all special characters

# URL handle for generated webpage
slug:      ch01s02

# specifies layout to be used for page generation (do not modify)
layout:     card
---


## A Word of Warning

So far we have not mathematically introduced anything that is surprising or complicated. If you had troubles following so far it's best to go back and review the underlying concepts.

However, _Tangent Vectors_, which come next, are the building block for many advanced concepts and it is important to understand them thoroughly. 
Also this is a good point to become aware that for many people there is a mismatch between the intuition for tangent vectors and the mathematical formulation. 
It is very important to appreciate the rigorous mathematical definition and to understand why it is not defined more closely to what people often think of.
The confusion probably stems from the early exposure of many students to vector calculus, where vectors are elements of a Euclidean space. 
Physics makes heavy use of vector calculus for the same reason as it makes use of differential geometry: The need to understand and describe _change_.
However, the problem that arises with vector calculus is that it describes _change_ from an exterior view of space. 
This exterior view comes very natural to many students and is adopted early on. 
The intrinsic view where we describe _change_ on spaces that aren't Euclidean, but can be curved, is less intuitive and somehow feels less natural. 
In fact we use manifolds which describe curved spaces as locally 'flat' spaces. It is obvious that 'flat' is the less complicated case and probably therefore feels more intuitive.
However, Physics needs to deal with all kinds of spaces and therefore we need to choose between the higher complexity but more general notion of curved spaces (the intrinsic view), or with many more higher dimensional flat spaces (the exterior view).

The problem that arises for many students in the understanding of differential geometry is the misunderstanding of what a _vector_ is.
It is worth noting here that as such the term _vector_ doesn't make much sense and the only thing that can safely be said about a _vector_ is that it is the element of a _vector space_.
Often _vector space_ is understood intuitively with the image of the very specific case of Euclidean space modeled with the Cartesian real coordinate space $$\mathbb R^n$$. 
Every student is familiar with this concept and with vector space addition and scalar multiplication. While this intuitive image serves very well for many problems, it is important to understand that it is only a very special case of a vector space.
When we talk about _tangent vectors_ in differential geometry this simplified image of a 'vector' (the element of a Cartesian coordinate space) gets in our way to understand the more general concepts.

The reader should keep this warning in mind when trying to understand the (at first sight unintuitive) definition of the tangent vector space of a smooth manifold.
