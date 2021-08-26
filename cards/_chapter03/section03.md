---
# this file is written in YAML http://docs.ansible.com/ansible/latest/YAMLSyntax.html
# all lines with a leading sharp are comments and will not be compiled
# longer blocks of text should start with a a leading > to escape all special characters

# URL handle for generated webpage
slug:      ch02s03
toc_entry: Chart-Induced Basis of \(T_pM\) 
# specifies layout to be used for page generation (do not modify)
layout:     card
---

## Chart-Induced Basis of $$T_pM$$ 

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


### The Symbol $$\partial$$ Looks like a Partial Derivative - Is It?
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

### Change of Components of Chart-Induced Basis of $$T_pM$$
To change from components $$\dot{\gamma}^{j}_{x}$$ of a tangent vector given in the chart (U,x)-induced basis, 
to components of a tangent vector in the chart (V,y)-induced basis, we need to first derive the objects
$$(\frac{\partial y^i}{\partial x^j})_p$$ 

The change of components of the tangent vector is then given as:

$$\dot{\gamma}^{i}_{y} = \sum_{j=1..dim M} \dot{\gamma}^{j}_{x} (\frac{\partial y^i}{\partial x^j})_p $$

which is commonly written in $$\sum$$instein notation as 

$$\dot{\gamma}^{i}_{y} = \dot{\gamma}^{j}_{x} (\frac{\partial y^i}{\partial x^j})_p $$


