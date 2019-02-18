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
Using the above defined charts we can derive the chart-induced basis of the tangent vector space $$T_pM$$ for each chart and at each point (that is in the domain of the respective chart).
These basis vectors are very handy objects and we can use them to write any tangent vector as a linear combination of them.
This is the link to vector calculus where we write the linear combination coefficients as components of a vector.
But we have to be very careful here to not forget that the components only make sense with respect to one specific basis of the tangent vector space that is only a valid basis in one specific chart.

It becomes very clear (from the restriction that the components are only valid for one chart), that the components can be transformed into other components that are valid in respect to another chart induced basis.
This change of components operation can easily be overlooked or misunderstood when we handle vectors (from vector calculus) carelessly.

So let's look at the change of components for our example of the sphere. Let's say we want to change components that are valid in the chart induced basis of the lon,lat-chart, 
to components that are valid in our other charts. 

Let's call our components of a tangent vector given in the chart (V,x)-induced basis $$\dot{\gamma}^{i}_{x}$$. 
The components of the same tangent vector in the chart (L,w)-induced basis shall be called $$\dot{\gamma}^{j}_{w}$$. 

We need to derive the objects 
$$(\frac{\partial x^i}{\partial w^j})_p$$ 
that carry all the information how to change the components.

Once we have these partial derivatives the change of components of the tangent vector is given as:

$$\dot{\gamma}^{i}_{x} = \sum_{j=1..2} \dot{\gamma}^{j}_{w} (\frac{\partial x^i}{\partial w^j})_p $$

We first compute the four partial derivatives $$(\frac{\partial x^1}{\partial w^1})_p$$, $$(\frac{\partial x^1}{\partial w^2})_p$$, $$(\frac{\partial x^2}{\partial w^1})_p$$, $$(\frac{\partial x^2}{\partial w^2})_p$$ via their definition:

$$(\frac{\partial x^i}{\partial w^j})_p = \partial_i (x^i \circ w^{-1})(w(p))$$ 

* * *
As we can see $$(x^i \circ w^{-1})(w(p))$$ are the component-wise chart transition maps from the (lon,lat) coordinates to the coordinates of the same point in the target chart.
These chart transition maps are given above. We will simply need to derive their partial derivatives and then plug them together in the right way to get a full description of how the components change.

Let's first get these partial derivatives out of the way:

$$\frac{\partial}{\partial lon}(\cos(lat)\sin(lon))(lon,lat) = \cos(lon)\cos(lat)$$ 

$$\frac{\partial}{\partial lat}(\cos(lat)\sin(lon))(lon,lat) = -\sin(lon)\sin(lat)$$ 

$$\frac{\partial}{\partial lon} (-\cos(lat)\cos(lon))(lon,lat) = \sin(lon)\cos(lat)$$

$$\frac{\partial}{\partial lat} (-\cos(lat)\cos(lon))(lon,lat) =  \cos(lon)\sin(lat)$$

* * *

We will use them and the chart transition maps to compute the $$(\frac{\partial x^i}{\partial w^j})_p$$:

$$(\frac{\partial x^1}{\partial w^1})_p = $$
$$ \partial_1(x^1 \circ w^{-1})(w(p)) = $$ 
$$ \partial_1( ... todo )(w(p)) = $$

...

* * *

With these objects it is straight forward to convert components of a tangent vector in the chart (L,w)-induced basis, 
to components of the same tangent vector in the chart (U,x)-induced basis. 

Analogously, we need to derive the transformation objects for each pair of overlapping charts.


* * *
If you are familiar with the [Jacobian matrix from vector calculus](https://en.wikipedia.org/wiki/Jacobian_matrix_and_determinant), 
you might have recognized what we were doing here. 
