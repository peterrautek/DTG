---
layout: default
---
## Prelude

[Differential Geometry](https://en.wikipedia.org/wiki/Differential_geometry) studies problems in geometry by applying concepts from calculus, linear algebra, and topology. 
It is often used to describe phenomena of change studied in Physics. 

The pivotal concept that underlies the theory of differential geometry is the differential structure that is given by tangent vector spaces. 
Abstractly speaking we want to understand the change of some phenomenon occurring on a manifold, and this change is mathematically modeled using tangent vector spaces. 

To define the notion of tangent vector spaces (and all concepts that are based on them, like cotangent vector spaces, tensor spaces, etc.) on a manifold we first need to have the notion of smooth functions and curves, as well as tangent vectors on smooth manifolds. 
We assume the basic notions of vector spaces (from [Linear Algebra](https://en.wikipedia.org/wiki/Linear_algebra)) and manifolds (from [Topology](https://en.wikipedia.org/wiki/Topological_manifold)) and will not further review them for the purpose of this brief overview. 

## Smooth Functions and Curves on Manifolds

Let $$M$$ be a (real and smooth) manifold. We define an infinite-dimensional vector space over $$\mathbb R$$ with the underlying set of all smooth functions $$\mathcal{C}^\infty(M)$$

$$\mathcal{C}^\infty(M) := \{f: M \to \mathbb R \mid f\text{ is smooth}\} $$

and with point-wise defined operations, (i.e. for any $$p\in M$$, and any $$\lambda \in \mathbb R$$):

$$(f+g)(p) := f(p)+g(p)$$

$$(\lambda f)(p) := \lambda f(p)$$

We define a _smooth curve_ on $$M$$ as a smooth map $$\gamma: \mathbb R \to M$$, where $$\mathbb R$$ is understood as a $$1$$-dimensional manifold.

This definition also applies to smooth maps $$I\to M$$ for an open interval $$I\subseteq \mathbb R$$.

## Interlude I - A Word of Warning

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

## Tangent Vectors 

Let $$\gamma:\mathbb R\to M$$ be a smooth curve through $$p\in M$$ such that $$\gamma(\lambda_0)=p$$. 
The _directional derivative operator_ at $$p$$ along $$\gamma$$ is the linear map

$$X_{\gamma,p}: \mathcal{C}^\infty(M) \xrightarrow{\sim} \mathbb R$$

$$f \mapsto (f\circ\gamma)'(\lambda_0)$$

where $$\mathbb R$$ is understood as a $$1$$-dimensional vector space over the field $$\mathbb R$$ and $$f\circ\gamma$$ is the point-wise function composition $$f$$ after $$\gamma$$.

Note that $$f\circ\gamma$$ is a map $$\mathbb R\to\mathbb R$$.
Hence we can calculate the 'usual' derivative and evaluate it at $$\lambda_0$$.

$$(f\circ\gamma)'(\lambda_0) = f'(\gamma(\lambda_0))$$

In differential geometry, $$X_{\gamma,p}$$ is called the _tangent vector_ to the curve $$\gamma$$ at the point $$p\in M$$. 

## Interlude II - The Reminder

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

## Tangent Space $$T_pM$$

Let $$M$$ be a manifold and $$p\in M$$. The _tangent space_ $$(T_pM, \oplus, \odot)$$  to $$M$$ at $$p$$ is the vector space over $$\mathbb R$$ with underlying set

$$T_pM := \{X_{\gamma,p}\mid \gamma \text{ is a smooth curve through }p\}$$

$$\text{vector addition }\oplus: T_pM\times T_pM \to T_pM$$

$$(X_{\gamma,p},X_{\delta,p}) \mapsto X_{\gamma,p}\oplus X_{\delta,p}$$

$$\text{scalar multiplication }\odot: \mathbb R\times T_pM \to T_pM$$

$$(\lambda,X_{\gamma,p}) \mapsto \lambda \odot X_{\gamma,p}$$

Addition and scalar multiplication both defined point-wise, i.e. for any $$f\in \mathcal{C}^\infty(M)$$,

$$(X_{\gamma,p}\oplus X_{\delta,p})(f) := X_{\gamma,p}(f) + X_{\delta,p}(f)$$

$$(\lambda \odot X_{\gamma,p})(f) := \lambda X_{\gamma,p}(f)$$

## Interlude III - Are co-ordinates good or bad?
So far we haven't said much about co-ordinates, because we kept concepts mathematical. 
Once you want to start computing anything on a manifold you will need to understand the relation between co-ordinates, charts, and manifolds.

The charts are the objects that will allow us to compute something on a manifold. 
From the charts we get co-ordinates, and a basis for the tangent vector spaces. 
They allow us to use real numbers for our computations.
Consequently for the practitioner the charts are very important objects. 

For the mathematician and the theoretical physicist who derive facts about manifolds in general, 
the charts are the evil objects that need to be avoided as much as possible. 
The reason being that showing something in a chart-free (i.e., co-ordinate-free) way means that we can avoid 
to write it down for every possible co-ordinate system. 
It simply works for any co-ordinate system.

## Charts and Co-ordinates

Let $$M$$ be a $$d$$-dimensional manifold. 
A pair $$(U,x)$$ where $$U$$ is an open set in the topological manifold and 
$$x: U \to x(U) \subseteq \mathbb R^d$$ is a homeomorphism (has a continuous inverse), is said to be a _chart_ of the manifold.

The _component functions_ of $$x: U\to x(U)$$ are the maps:

$$x^i : U  \to \mathbb R$$

$$p \mapsto \text{proj}_i(x(p))$$

for $$1\leq i\leq d$$, where $$\text{proj}_i(x(p))$$ is the $$i$$-th component of $$x(p)\in \mathbb R^d$$. 
The $$x^i(p)$$ are called the _co-ordinates_ of the point $$p\in U$$ with respect to the chart $$(U,x)$$.


### Atlas

An _atlas_ of a manifold $$M$$ is a collection $$\mathscr{A}:=\{(U_\alpha,x_\alpha)\mid \alpha \in \mathcal{A}\}$$ of charts such that:

$$\bigcup_{\alpha \in \mathcal{A}}U_\alpha = M. $$


### Chart Transition Maps

Two charts $$(U,x)$$ and $$(V,y)$$ are said to be $$\mathcal{C}^0$$_-compatible_ if 
either $$U \cap V = \emptyset$$ or the map:
$$
y\circ x^{-1}: x(U\cap V) \to y(U\cap V)
$$
is continuous.


Note that $$y\circ x^{-1}$$ is a map from a subset of $$\mathbb R^d$$ to a subset of $$\mathbb R^d$$.


[//]: # & U\cap V \se M \ar[ldd,"x"'] \ar[rdd,"y"]&\\
[//]: # &&&\\
[//]: # x(U\cap V) \se \R^d \ar[rr,"y\circ x^{-1}"']& & y(U\cap V)\se \R^d
[//]: # \end{tikzcd}


Since the maps $$x$$ and $$y$$ are homeomorphisms, the composition map $$y \circ x^{-1}$$ is also a homeomorphism 
and hence continuous. 
Therefore, any two charts on a topological manifold are $$\mathcal{C}^0$$-compatible. 

The map $$y\circ x^{-1}$$ (and its inverse $$x\circ y^{-1}$$) is called the _chart transition map_.

## Interlude IV - Multiple Charts Constitute a Manifold

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

### Chart-Induced Basis of $$T_pM$$ 

If $$(U,x)$$ is a chart on $$M$$, then the co-ordinate maps 
$$x^a: U \to x(U) \subseteq \mathbb R$$ are smooth functions on $$U$$. 

Since we are only dealing with finite dimensional manifolds, 
we can always construct a chart-induced basis of $$T_pM$$ as a set (of cardinality $$dim M$$):

$$\{(\frac{\partial}{\partial{x}^{a}})_{p} \mid 1\leq a \leq \dim M\}$$

The $$(\frac{\partial}{\partial{x}^{a}})_{p}$$ are elements of $$T_pM$$, 
hence special tangent vectors ($$X_{\gamma_{(a)},p}$$) that are defined for a specific chart at $$p$$, 
by defining the curves $$\gamma_{(a)}$$ in a chart dependent way:

$$\gamma_{(a)}(0) := p$$

$$\gamma_{(a)}(t) := x^{-1} \circ (0,..,0,t,0,..,0)_{a}$$

where the $$(0,..,0,t,0,..,0)_{a}$$ is an element of $$\mathbb R^d$$, that has the $$t$$ in the $$a$$-th position.

The basis vectors (being elements of $$T_pM$$) provide linear mappings:

$$X_{\gamma,p}: \mathcal{C}^\infty(M) \xrightarrow{\sim} \mathbb R$$

Since it can be shown that they form a basis for our vector space $$T_pM$$ it is sufficient to use 
linear combinations of them to act on arbitrary functions of $$\mathcal{C}^\infty(M)$$. 
In other words: for a given chart (induced basis), all possible tangent vectors (elements of $$T_pM$$), 
can be written as linear combinations of the basis vectors. 

## Interlude V - The Symbol $$\partial$$ Looks like a Partial Derivative - Is It?
The above definitions are fundamentally different from what you might be familiar with, 
from vector calculus in Euclidean spaces. 
In $$d$$-dimensional Euclidean space we have a set of coordinate functions that are valid for all of $$\mathbb R^d$$, 
which gives us $$d$$ many $$d$$-dimensional basis vectors. 
For our smooth manifold we define the basis of the tangent vector space for a specific point $$p$$ and a given chart. 

Also it is worth noting here that 
$$(\frac{\partial}{\partial{x}^{a}})_{p}$$ is to be read as a symbol denoting one specific element of the tangent vector space at $$p$$. 
Specifically for this element we:
* know how to construct it from the given co-ordinate map $$x^a$$ and
* intend to use it as a basis vector of $$TpM$$

The symbol resembles the partial derivative symbol and in fact for the manifold $$\mathbb R^d$$, 
with the identity chart map, the basis vectors of $$TpM$$ behave consistently with the partial derivative. 
Both (the partial derivative and the tangent space vector) take a function and produce the same real number.
So the notation $$(\frac{\partial}{\partial{x}^{a}})_{p}$$ was clearly chosen to resemble the partial derivative, 
but it is important to understand that the partial derivative is only defined on $$\mathbb R^d$$, 
while our tangent vectors will allow us to compute directional derivatives on smooth manifolds.

## Change of Components of Chart-Induced Basis of $$T_pM$$
To change from components $$\dot{\gamma}^{j}_{x}$$ of a tangent vector given in the chart (U,x)-induced basis, 
to components of a tangent vector in the chart (V,y)-induced basis, we need to first derive the objects
$$(\frac{\partial y^i}{\partial x^j})_p$$ 

The change of components of the tangent vector is then given as:

$$\dot{\gamma}^{i}_{y} = \sum_{j=1..dim M} \dot{\gamma}^{j}_{x} (\frac{\partial y^i}{\partial x^j})_p $$

which is commonly written in $$\sum$$instein notation as 

$$\dot{\gamma}^{i}_{y} = \dot{\gamma}^{j}_{x} (\frac{\partial y^i}{\partial x^j})_p $$




## Gradient and Gradient Operator
The gradient of a function in $$\mathcal{C}^\infty(M)$$ is a special case of the derivative. 
Let's first define the gradient and the related gradient operator, which we will use to construct the Cotangent Space.

Let $$M$$ be a manifold and let $$f: M \to \mathbb R$$ be smooth. The _gradient_ of $$f$$ at $$p\in M$$ is the covector (an element of the Cotangent space at $$p$$)

$$d_pf: T_pM \xrightarrow{\sim} T_{f(p)} \mathbb R \cong_\mathrm{vec} \mathbb R $$

$$X \mapsto d_pf(X) := X(f) $$

In fact, we can define the _gradient operator_ at $$p\in M$$ as the $$\mathbb R$$-linear map 

$$d_p : \mathcal{C}^\infty(U) \xrightarrow{\sim} T^*_pM$$

$$f \mapsto d_pf$$

with $$p\in U\subseteq M$$.


## Cotangent Space $$T^*_pM$$ and its Chart Induced Basis

Let $$M$$ be a manifold and $$p\in M$$ a point on the manifold and let $$T_pM$$ denote the tangent space at $$p$$. 
The _cotangent space_ to $$M$$ at $$p$$ is defined as the vector space dual:

$$\rm T^*_pM := (T_pM)^* = Hom(T_pM, \mathbb R)$$

which is the set of all linear maps from elements of the _tangent vector space_ $$T_pM$$ to $$\mathbb R$$.

* * *

Let $$(U,x)$$ be a chart on $$M$$, with $$p\in U$$. 

We can apply the gradient operator $$d_p$$ (with $$p\in U$$) 
to each of the basis vectors of $$\{(\frac{\partial}{\partial{x}^{a}})_{p}\}$$ to obtain $$(\dim M)$$-many elements of $$T^*_p M$$.

The set $$\{d_px^a\mid 1\leq a \leq \dim M\}$$ can be shown to form a basis of $$T^*_p M$$.

If $$\{(\frac{\partial}{\partial{x}^{a}})_{p}\}$$ is the basis of $$T_pM$$ induced by a chart $$(U,x)$$, then the dual basis is denoted as $$\{({\rm d} x^a)_p\}$$
and by definition (of the dual) we have

$$({\rm d}x^a)_p \left( \left( \frac{\partial}{\partial{x}^{b}} \right)_{p} \right) = \delta^a_b$$

## Interlude VI - Why didn't we need a cotangent space in Euclidean geometry?
todo



## Derivative and Push-Forward
We have already seen a special case of the derivative - the gradient.
Now we will define the general derivative which is also called the push-forward.

Let $$M$$ and $$N$$ be manifolds and let $$\phi: M \to N$$ be smooth. 

The _differential_ or _derivative_ of $$\phi$$ at $$p\in M$$ is the linear map

$$ d_p \phi : T_pM \xrightarrow{\sim} T_{\phi(p)}N $$ 

$$ X \mapsto d_p\phi(X) $$

where $$d_p\phi(X)$$ is the tangent vector to $$N$$ at $$\phi(p)$$

$$d_p \phi(X):  \mathcal{C}^\infty(N) \xrightarrow{\sim} \rm \mathbb R $$

$$ g \mapsto (d_p\phi(X))(g):=X(g\circ \phi) $$

todo...



## Tensor Spaces
todo

## Embedding and Immersion
A smooth manifold can be embedded or immersed in $$\rm \mathbb R^d$$, for some $$d\in \mathbb N$$. 

A smooth map $$\phi: M \to N$$ is an _immersion_ of $$M$$ into $$N$$ if the derivative is injective, for all $$p\in M$$. 

$$\rm d_p\phi \equiv (\phi_*)_p : T_pM\xrightarrow{\sim}T_{\phi(p)}N$$

The manifold $$M$$ is said to be an _immersed submanifold_ of $$N$$.

A smooth map $$\phi: M \to N$$ is said to be a _smooth embedding_ of $$M$$ into $$N$$ if
* $$\phi: M\to N$$ is an immersion
* $$M \cong_{\mathrm{top}}\phi(M)\subseteq N$$, 

where $$\phi(M)$$ carries the subset topology inherited from $$N$$.

The manifold $$M$$ is an _embedded submanifold_ of $$N$$.

## Interlude VII - All these concepts at just one point - Really?
todo

## Bundles and Fields
todo

***
# Other Topics on This Website
[An example of a Sphere with specific Charts](./examplesphere.html).

# Differential Geometry Resources
[Frederic Schuller's Youtube Lectures: Geometric Anatomy of Theoretical Physics](https://www.youtube.com/playlist?list=PLPH7f_7ZlzxTi6kS4vCmv4ZKm9u8g5yic)

[Lecture Notes in PDF format by Simon Rea: Geometric Anatomy of Theoretical Physics](https://drive.google.com/file/d/1nchF1fRGSY3R3rP1QmjUg7fe28tAS428/view)

# Other Stuff
[All different kinds of useful Mathjax and Markdown Syntax used to create this page](./mathjax-and-markdown.html).