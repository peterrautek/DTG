---
# this file is written in YAML http://docs.ansible.com/ansible/latest/YAMLSyntax.html
# all lines with a leading sharp are comments and will not be compiled
# longer blocks of text should start with a a leading > to escape all special characters

# URL handle for generated webpage
slug:      ch01s01
toc_entry: Smooth Functions and Curves on Manifolds
# specifies layout to be used for page generation (do not modify)
layout:     card
---

## Smooth Functions and Curves on Manifolds

Let $$M$$ be a (real and smooth) manifold. We define an infinite-dimensional vector space over $$\mathbb R$$ with the underlying set of all smooth functions $$\mathcal{C}^\infty(M)$$

$$\mathcal{C}^\infty(M) := \{f: M \to \mathbb R \mid f\text{ is smooth}\} $$

and with point-wise defined operations, (i.e. for any $$p\in M$$, and any $$\lambda \in \mathbb R$$):

$$(f+g)(p) := f(p)+g(p)$$

$$(\lambda f)(p) := \lambda f(p)$$

We define a _smooth curve_ on $$M$$ as a smooth map $$\gamma: \mathbb R \to M$$, where $$\mathbb R$$ is understood as a $$1$$-dimensional manifold.

This definition also applies to smooth maps $$I\to M$$ for an open interval $$I\subseteq \mathbb R$$.
