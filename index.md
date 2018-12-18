---
layout: default
---
## Prelude

[Differential Geometry](https://en.wikipedia.org/wiki/Differential_geometry) studies problems in geometry by applying concepts from calculus, linear algebra, and topology. 
It is often used to describe phenomena of change studied in Physics. 

The pivotal concept that underlies the theory of differential geometry is the differential structure that is given by tangent vector spaces. 
Abstractly speaking we want to understand the change of some phenomenon occurring on a manifold, and this change is mathematically modeled using tangent vector spaces. 

To define the notion of tangent vector spaces (and all concepts that are based on them, like cotangent vector spaces, tensor spaces, etc.) on a manifold we first need to have the notion of smooth functions and curves on manifolds. 
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
However, Physics needs to deal all kinds of spaces and therefore we need to choose between the higher complexity but more general notion of curved spaces (the intrinsic view), or with many more higher dimensional flat spaces (the exterior view).

The problem that arises for many students in the understanding of differential geometry is the misunderstanding of what a _vector_ is.
It is worth noting here that as such the term _vector_ doesn't make much sense and the only thing that can savely be said about a _vector_ is that it is the element of a _vector space_.
Often _vector space_ is understood intuitively with the image of the very specific case of Euclidean space modeled with the Cartesian real coordinate space $$\mathbb R^n$$. 
Every student is familiar with this concept and with vector space addition and scalar multiplication. While this intuitive image serves very well for many problems, it is important to understant that it is only a very special case of vector space.
When we talk about _tangent vectors_ in differential geometry this simplified image of a 'vector' (the element of a Cartesian coordinate space) gets in our way to understand the more general concepts.

The reader should keep this warning in mind when trying to understand the (at first sight unintuitive) definition of the tangent vector space of a smooth manifold.

## Tangent Vectors 

Let $$\gamma:\mathbb R\to M$$ be a smooth curve through $$p\in M$$ such that $$\gamma(0)=p$$. 
The _directional derivative operator_ at $$p$$ along $$\gamma$$ is the linear map

$$X_{\gamma,p}: \mathcal{C}^\infty(M) \xrightarrow{\sim} \mathbb R$$

$$f \mapsto (f\circ\gamma)'(0)$$

where $$\mathbb R$$ is understood as a $$1$$-dimensional vector space over the field $$\mathbb R$$.

Note that $$f\circ\gamma$$ is a map $$\mathbb R\to\mathbb R$$, hence we can calculate the 'usual' derivative and evaluate it at $$0$$.

In differential geometry, $$X_{\gamma,p}$$ is called the _tangent vector_ to the curve $$\gamma$$ at the point $$p\in M$$. 

## Interlude II - The Reminder

With the previous warning in mind: we should acknowledge once more at this point that the _tangent vector_ in differential geometry is quite a bit different from what people often think of as a _vector_.
Once again - a _vector_ is an element of a _vector space_, and the vector space we are concerned with here is quite a bit different than the prime example of the Cartesian coordinate vector space.
Let's try to develop some intuition for our new 'kind of vector' here before we continue with the actual definition of the tangent vector space.

When we look at what will be called the _tangent vector_ $$X_{\gamma,p}$$, than we see by its very definition, it is nothing else than a linear map from all functions to $$\mathbb R$$.
Remember that our manifolds are constructed to be locally similar to $$\mathbb R^{dim(M)}$$, but they aren't $$\mathbb R^{dim(M)}$$. 
So the tangent vector is quite remarkable in that it takes a function (an element of \mathcal{C}^\infty(M)) and maps it to $$\mathbb R$$. 
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

## Tangent Space and Cotangent Space

Let $$M$$ be a manifold and $$p\in M$$. The _tangent space_ $$(T_pM, \oplus, \odot)$$  to $$M$$ at $$p$$ is the vector space over $$\mathbb R$$ with underlying set

$$T_pM := \{X_{\gamma,p}\mid \gamma \text{ is a smooth curve through }p\}$$

$$\text{vector addition }\oplus: T_pM\times T_pM \to T_pM$$

$$(X_{\gamma,p},X_{\delta,p}) \mapsto X_{\gamma,p}\oplus X_{\delta,p}$$

$$\text{scalar multiplication }\odot: \mathbb R\times T_pM \to T_pM$$

$$(\lambda,X_{\gamma,p}) \mapsto \lambda \odot X_{\gamma,p}$$

Addition and scalar multiplication both defined pointwise, i.e. for any $$f\in \mathcal{C}^\infty(M)$$,

$$(X_{\gamma,p}\oplus X_{\delta,p})(f) := X_{\gamma,p}(f) + X_{\delta,p}(f)$$

$$(\lambda \odot X_{\gamma,p})(f) := \lambda X_{\gamma,p}(f)$$

* * *

Let $$M$$ be a manifold and $$p\in M$$ a point on the manifold and let $$T_pM$$ denote the tangent space at $$p$$. 
The _cotangent space_ to $$M$$ at $$p$$ is defined as the vector space dual:

$$\rm T^*_pM := (T_pM)^* = Hom(T_pM, \mathbb R)$$

which is the set of all linear maps from elements of the _tangent vector space_ $$T_pM$$ to $$\mathbb R$$.


## Charts and Co-ordinates
So far we haven't said much about co-ordinates, because we kept concepts rather high-level. Once you start computing anything on manifolds you will need to understand the relation between co-ordinates, charts, and manifolds.


Let $$M$$ be a $$d$$-dimensional manifold. 
A pair $$(U,x)$$ where $$U$$ is an open set in the topological manifold and $$x: U \to x(U) \subseteq \mathbb R^d$$ is a homeomorphism (has a continous inverse), is said to be a _chart_ of the manifold.

The _component functions_ of $$x: U\to x(U)$$ are the maps:

$$x^i : U  \to \mathbb R$$

$$p \mapsto \text{proj}_i(x(p))$$

for $$1\leq i\leq d$$, where $$\text{proj}_i(x(p))$$ is the $$i$$-th component of $$x(p)\in \mathbb R^d$$. 
The $$x^i(p)$$ are called the _co-ordinates_ of the point $$p\in U$$ with respect to the chart $$(U,x)$$.

TODO: co-ordinates are invertible functions mapping points of the manifold to $$\mathbb R$$.

An _atlas_ of a manifold $$M$$ is a collection $$\mathscr{A}:=\{(U_\alpha,x_\alpha)\mid \alpha \in \mathcal{A}\}$$ of charts such that:

$$\bigcup_{\alpha \in \mathcal{A}}U_\alpha = M. $$


## TODO 

If $$\{(\frac{\partial}{\partial{x}^{a}})_{p}\}$$ is the basis of $$T_pM$$ induced by a chart $$(U,x)$$, then the dual basis is denoted as $$\{({\rm d} x^a)_p\}$$
and by definition (of the dual) we have

$$({\rm d}x^a)_p \left( \left( \frac{\partial}{\partial{x}^{b}} \right)_{p} \right) = \delta^a_b$$

## Interlude III - Why didn't we need a cotangent space in Euclidean geometry?
todo

## Gradient
The gradient of a function in $$\mathcal{C}^\infty(M)$$ is a special case of the derivative. Let's first define the gradient and afterwards the general derivative which is also called the push-forward.

Let $$M$$ be a manifold and let $$f: M \to \mathbb R$$ be smooth. The _gradient_ of $$f$$ at $$p\in M$$ is the covector (an element of the Cotangent space at $$p$$)

$$d_pf: T_pM \xrightarrow{\sim} T_{f(p)} \mathbb R \cong_\mathrm{vec} \mathbb R $$

$$X \mapsto d_pf(X) := X(f) $$

In fact, we can define the _gradient operator_ at $$p\in M$$ as the $$\mathbb R$$-linear map 

$$d_p : \mathcal{C}^\infty(U) \xrightarrow{\sim} T^*_pM $$

$$f \mapsto d_pf$$

with $$p\in U\subseteq M$$.



## Derivative and Push-Forward
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

## Bundles and Fields
todo

***



# Differential Geometry Resources
[Frederic Schuller's Youtube Lectures: Geometric Anatomy of Theoretical Physics](https://www.youtube.com/playlist?list=PLPH7f_7ZlzxTi6kS4vCmv4ZKm9u8g5yic)

[Lecture Notes in PDF format by Simon Rea: Geometric Anatomy of Theoretical Physics](https://drive.google.com/file/d/1nchF1fRGSY3R3rP1QmjUg7fe28tAS428/view)

# Other Stuff
[All different kinds of useful Mathjax and Markdown Syntax used to create this page](./mathjax-and-markdown.html).