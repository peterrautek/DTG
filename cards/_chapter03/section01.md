---
# this file is written in YAML http://docs.ansible.com/ansible/latest/YAMLSyntax.html
# all lines with a leading sharp are comments and will not be compiled
# longer blocks of text should start with a a leading > to escape all special characters

# URL handle for generated webpage
slug:      ch03s01

# specifies layout to be used for page generation (do not modify)
layout:     card
---

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
