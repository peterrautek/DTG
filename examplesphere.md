---
layout: default
---

Examples are important to see the abstract math constructs in action. 
Here, we will look at the sphere - a simple, yet useful example. 
We will look at the [abstract mathematical objects that we introduced for smooth manifolds](./index.html).
define chart maps (an atlas in fact), derive the inverse chart maps, chart transition maps, 
coordinate transformation maps, define an embedding 
in $$\mathbb R^3$$, and show illustrations of functions on the manifold (i.e., elements of $$\mathcal{C}^\infty(\mathbb S^2)$$) and vector fields on the sphere.

Remember, the purpose of defining an atlas of the sphere is to have local (1-1) mappings from the manifold $$\mathbb S^2$$ to $$\mathbb R$$.
We need these mappings to (for instance) calculate directional derivatives on the manifold. 


## An Atlas of the 2-Sphere
Let $$\mathbb S^2$$ be a (real and smooth) manifold with an atlas $$\mathcal{A}$$ defined as:
$$\mathcal{A} := \{ (L, w), (U, x), (V, y) \}$$
where $$(U, x), (V, y), (L, w)$$ are the charts of the sphere defined such that 
$$w^1$$ will be what is commonly referred to as the longitude, 
$$w^2$$ will be what is commonly referred to as the latitude.
$$x$$ as well as $$y$$ will be orthographic projections of the northern and southern hemisphere onto the $$\mathbb R^2$$ plane respectively.

## Chart Transition Maps
We define the chart transition map $$w\circ x^{-1}: x(L\cap U) \to w(L\cap U)$$ component-wise:

$$x^1\circ w^{-1}(lon, lat) \mapsto \cos(lat) \sin(lon) $$

$$x^2\circ w^{-1}(lon, lat) \mapsto -\cos(lat) \cos(lon) $$

and its inverse map:

$$w^1\circ x^{-1}(u,v) \mapsto \arctan_2(v,-u)$$

$$w^2\circ x^{-1}(u,v) \mapsto \arcsin(\sqrt{1-(u^2+v^2)})$$

We define $$w\circ y^{-1}: y(L\cap V) \to w(L\cap V)$$:

$$y^1\circ w^{-1}(lon, lat) \mapsto \cos(lat) \sin(lon) $$
$$y^2\circ w^{-1}(lon, lat) \mapsto \cos(lat) \cos(lon) $$

and its inverse map:

$$w^1\circ y^{-1}(u,v) \mapsto \arctan_2(v,u)$$

$$w^2\circ y^{-1}(u,v) \mapsto \arcsin(-\sqrt{1-(u^2+v^2)})$$

For the inverse chart transition maps we use the [$$\arctan_2(x,y)$$](https://en.wikipedia.org/wiki/Atan2) function which avoids the problem of the common $$\arctan(\frac{x}{y})$$ function 
that looses the information of the independent signs of its arguments $$x$$ and $$y$$.

Take note (once more) that the chart transition maps as well as their inverses, are maps from a subset of $$\mathbb R^2$$ to a subset of $$\mathbb R^2$$.
They transform the co-ordinates induced by one chart to the co-ordinates of another chart.

## Change of Components of Chart-Induced Basis of $$T_pM$$
To change from components $$\dot{\gamma}^{j}_{y}$$ of a tangent vector given in the chart (V,y)-induced basis, 
to components of the same tangent vector in the chart (L,w)-induced basis, we need to first derive the objects
$$(\frac{\partial w^i}{\partial y^j})_p$$ 

The change of components of the tangent vector is then given as:

$$\dot{\gamma}^{i}_{w} = \sum_{j=1..2} \dot{\gamma}^{j}_{y} (\frac{\partial w^i}{\partial y^j})_p $$

We first compute the four partial derivatives $$(\frac{\partial w^1}{\partial y^1})_p$$, $$(\frac{\partial w^1}{\partial y^2})_p$$, $$(\frac{\partial w^2}{\partial y^1})_p$$, $$(\frac{\partial w^2}{\partial y^2})_p$$ via their definition:

$$(\frac{\partial w^i}{\partial y^j})_p = \partial_i (w^i \circ y^{-1})(y(p))$$ 

* * *

We will use the chart transition maps that are given above and will need the partial derivatives of 
$$\arcsin(-\sqrt{1-(u^2+v^2)})$$ and $$\arctan_2(v,u)$$. Let's get them out of the way first:

$$\frac{\partial}{\partial u}(\arcsin(-\sqrt{1-(u^2+v^2)}))(u,v) = \frac{u}{\sqrt{-(u^2+v^2-1)(u^2+v^2)}}$$ 

$$\frac{\partial}{\partial v}(\arcsin(-\sqrt{1-(u^2+v^2)}))(u,v) = \frac{v}{\sqrt{-(u^2+v^2-1)(u^2+v^2)}}$$ 

$$\frac{\partial}{\partial u} (\arctan_2)(v,u) = \frac{\partial}{\partial u}(\arctan)(\frac{v}{u}) = \frac{-v}{u^2+v^2} $$

$$\frac{\partial}{\partial v} (\arctan_2)(v,u) = \frac{\partial}{\partial u}(\arctan)(\frac{v}{u}) = \frac{u}{u^2+v^2} $$

* * *

We will use them and the chart transition maps to compute the $$(\frac{\partial w^i}{\partial y^j})_p$$:

$$(\frac{\partial w^1}{\partial y^1})_p = $$
$$ \partial_1(w^1 \circ y^{-1})(y(p)) = $$ 
$$ \partial_1(arctan_2(u,v))(y(p)) = $$
$$\frac{-u}{u^2+v^2}$$ 

$$(\frac{\partial w^1}{\partial y^2})_p = $$
$$ \partial_2(w^1 \circ y^{-1})(y(p)) = $$ 
$$ \partial_2(arctan_2(u,v))(y(p)) = $$
$$\frac{v}{u^2+v^2}$$ 

$$(\frac{\partial w^2}{\partial y^1})_p = $$
$$ \partial_1(w^2 \circ y^{-1})(y(p)) = $$ 
$$ \partial_1(arcsin(-\sqrt{1-(u^2+v^2)}))(y(p)) = $$
$$\frac{u}{\sqrt{-(u^2+v^2-1)(u^2+v^2)})}$$ 

$$(\frac{\partial w^2}{\partial y^2})_p = $$
$$ \partial_2(w^2 \circ y^{-1})(y(p)) = $$ 
$$ \partial_2(arcsin(-\sqrt{1-(u^2+v^2)}))(y(p)) = $$
$$\frac{v}{\sqrt{-(u^2+v^2-1)(u^2+v^2)})}$$ 

* * *

With these objects it is straight forward to convert components of a tangent vector in the chart (V,y)-induced basis, 
to components of the same tangent vector in the chart (L,w)-induced basis. 

Analogously we need to derive the transformation objects for each pair of overlapping charts.

* * *
If you are familiar with the [Jacobian matrix from vector calculus](https://en.wikipedia.org/wiki/Jacobian_matrix_and_determinant), 
you might have recognized what we were doing here. 
