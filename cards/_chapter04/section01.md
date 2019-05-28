---
# this file is written in YAML http://docs.ansible.com/ansible/latest/YAMLSyntax.html
# all lines with a leading sharp are comments and will not be compiled
# longer blocks of text should start with a a leading > to escape all special characters

# URL handle for generated webpage
slug:      ch04s01

# specifies layout to be used for page generation (do not modify)
layout:     card


further:
 - item:
   type: video
   title: differential geometry schuller 01
   url: https://youtube.com
 - item2:
   type: video
   title: orf
   url: https://orf.at
---

## Why didn't we need a cotangent space in Euclidean geometry?
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


## The Meaning of the Co-Vector Basis
https://www.youtube.com/watch?v=CliW7kSxxWU&feature=youtu.be  


## Tensor Spaces
todo

## The Metric Tensor
TODO

## Intrinsic vs. Extrinsic
When reading differential geometry literature a lot of discussion is about the words intrinsic vs. extrinsic. Not only is the discussion confusing, even worse, the mathematical notation for intrinsic and extrinsic objects is often used as if they were interchangeable. For instance the symbols used for a tangent vector basis are often the same regardless of the basis vectors being intrinsic or extrinsic. While this approach emphasises that fundamentally they do describe the same object, it becomes very hard to see which vectors 'live' on the manifold (intrinsic) and which vectors 'live' in the ambient space.

There's nothing one can do to clear up this confusion in literature. In this primer we exclusively will use the intrinsic viewpoint. If we need to make an exception we will clearly state that an object is 'living' in the ambient space and will try to use a different mathematical symbol for these objects.

## Interlude VII - All these concepts at just one point - Really?
todo

## Bundles and Fields
todo
 

## The difference between Lie-, Covariant-, and Exterior-Derivative
TODO: rewrite paragraph from Wikipedia (https://en.wikipedia.org/wiki/Lie_derivative):

## The Co-variant Derivative
A geometrically intuitive and very general explanation of the co-variant derivative can be simply given as: 
The co-variant derivative evaluates the directional derivative of a tensor in any direction at a point on a smooth manifold. This explanation is geometrically intuitive because humans usually have an easy time imagining a direction on a manifold and we also have an intuitive understanding of the directional derivative, as the thing that describes the rate of change of something.
The above explanation is very general, firstly, because it specifies the 'something' that changes in a given direction as (nothing less than) a tensor. A tensor is a very general concept that includes scalars, vectors, co-vectors and products of them. Secondly, the generality of the co-variant derivative stems from its definition on (nothing less than) a smooth manifold. Again a smooth manifold is a very general concept that includes high dimensional curved spaces, but also more familiar special cases like the 3D Euclidean space.
This generality of the co-variant derivative means that the mathematical definition is immensely valuable since it encompasses all kinds of special cases of directional derivatives. Simple cases like the directional derivative of a vector field in Euclidean space are equally well described as more complicated cases as directional derivatives of tensor fields on smooth manifolds in general.
So instead of learning many different specializations of directional derivatives that are only valid for certain cases - we shall learn 'the one' directional derivative that rules them all.

## The Lie-Derivative 
Another kind of directional derivative that 'lives' on a smooth manifold is the Lie derivative.
TODO

## Relation between Co-variant Derivative and Lie Derivative
Note that the antisymmetrized covariant derivative ∇uv − ∇vu, and the Lie derivative Luv differ by the torsion of the connection, so that if a connection is torsion free, then its antisymmetrization is the Lie derivative.  
TODO


## Jacobian Sidenote:

By far the most accesible geometrical interpretation of the Jacobian matrix that I've come across is given in this video: https://www.youtube.com/watch?v=kYB8IZa5AuE&list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab&index=3

If you need to brush up your linear algebra and want to develop some immensely helpful geometric intuition for matrices and vectors it pays off watching the whole series on linear algebra.
In just over 2.5h you can binge learn the essence of geometrical understanding of linear algebra. Something that otherwise you could spend month trying to wrap your head around.
https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab



## Nabla and all Kinds of Directional Derivatives

The Nabla operator is so important that it is hardly impossible to overstate its importance. It is the operator that generalizes directional derivatives of different kinds on manifolds. Directional derivatives are the objects that allow us to talk about rates of change and arguably this is a large portion of what physics (or if you want to get philosophical - the world as it is perceived by us) is about. 

It is also interesting that Nabla isn't just another symbol borrowed from the greek alphabet, but a symbol that was invented by [...] TODO. 
"physical mathematics is very largely the mathematics of ∇"


Nabla is arguably a confusing object. It has many meanings and takes different forms and shapes and therefore was misinterpreted in many books and publications. There is even a report [Tai 1994] of the improper uses of Nabla in the literature that lists more than 60 books on math, physics and engineering that use the operator sloppily or wrongly. The list of publications that makes improper use of the operator must go in the hundreds if not thousands.

Other concepts and operators that are related to Nabla include the gradient, divergence, curl, Laplace, the derivative, the vector differential operator, the directional derivative, the covariant derivative, connections on a manifolds, parallel transport, etc.



There are also plenty of notations for some special cases of this operator which includes...


It is obvious that Nabla is a very special and important object with lots of uses, confusions, and specializations. Specializations come in the form of either restricting it to a certain coordinate system or to certain domains.
These specializations are the source of many errors, inprecissions, and confusions. When a specialization of the Nabla operator is taken out of its context it might easily be wrongly interpreted or applied.

Here, we will try to be extra careful and define the nabla operator in an unambiguous, general sense, and enumerate the possible specializations of the operator. 

## Nabla as a Symbol
The nabla operator as a symbol has three slots, 
(\nabla_{\square}(\square))_{\square}
The first slot is open for a vector (i.e., an element of the tangent vector space T_pM at a given point p), the second slot is for the operand which needs to be a tensor field on the manifold, and the third slot is open for a point on the manifold. By filling certain slots and leaving other slots open we can get specializations of the nabla operator in very different ways and with very different meaning. 
Before we do that we will try to get a high-level understanding of the meaning of the nabla operation, i.e., the nabla operator with all three slots filled.

The meaning of the operation (\nabla_{v}(s))_{p}
is that of a directional derivative of the operand s at p, where v gives the direction. It gives at a given point p a derivative of the field s. So the result of the operation is of the same kind as the field of the operand. If the operand s is a scalar field, the result of (\nabla_{v}(s))_{p} is a scalar; if s is a vector field, the result of (\nabla_{v}(s))_{p} is a vector; ...
The operand s must be a tensor field which of course also includes scalar fields, vector fields, and co-vector fields, on the manifold. The actual derivation, i.e., the rule how to compute (\nabla_{v}(s))_{p} is not uniquely defined, but can be prescribed in different ways. This non-unique prescription is called the connection on the manifold. Once it is prescribed the connection tells us how to connect different tangent spaces with each other and we can think of it as "part of the manifold". We will look at different prescriptions (i.e., connections) later and see that some have nicer properties than others. For now we want to look a bit closer at what the symbol nabla can mean without worrying about how to compute it.

Back to the three slots of the nabla operation. Interestingly, when specializing the nabla operator, we can choose to leave any of the three slots open or unassigned. If we leave the third slot open we turn the nabla operator into an operator that is defined for vector fields on the manifold, that is evaluated at every point for the local tangent vector space. However, instead of a vector in the first slot we now need a vector field in the first slot. This is very commonly done and conveniently allows us to specify operators that operate on whole vector, and tensor fields of the manifold.

If the operand is a scalar function f \in C(\infty(M)) on the manifold and the vector is an element of the tangent vector space T_pM, the nabla operator gives us the directional derivative of the function at point p. 

If we leave the second (i.e., the operand) slot open we get the directional derivative operator \nabla_{v}(\square) that takes a function on the manifold and evaluates the directional derivative. Interestingly, we can also leave the first (i.e., the direction) slot open and write \nabla_{\square}(f), which gives us another operator. This operator is called the gradient of the function f. It takes a vector as input and gives us again the directional derivative of f at p. 

Analogously we can define different specializations of the nabla operator by reserving the second (i.e., the operand) slot for a vector. The operation then results in a vector at point p or in a vector field if we apply it to the whole manifold. By leaving the first slot open we get an operator that takes a vector as input and gives the directional derivative of the vector field in the second slot. 
By leaving the second slot open it gives the directional derivative of one vector field in the direction of another.

TODO: what are the common names for these? what is div, curl?

 
https://deepblue.lib.umich.edu/bitstream/handle/2027.42/7869/bad1475.0001.001.pdf?sequence=5&isAllowed=y  


## Directional Derivative of Tensor Fields
[Schuller WEHIWSGL-7, 556](https://youtu.be/nEaiZBbCVtI?t=556)


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

