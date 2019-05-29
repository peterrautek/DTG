---
# this file is written in YAML http://docs.ansible.com/ansible/latest/YAMLSyntax.html
# all lines with a leading sharp are comments and will not be compiled
# longer blocks of text should start with a a leading > to escape all special characters

# URL handle for generated webpage
slug:      ch02s01
toc_entry: Charts, Atlas, Co-ordinates, Chart Transitions
# specifies layout to be used for page generation (do not modify)
layout:     card
---

## Co-ordinates - Good or Bad?
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
