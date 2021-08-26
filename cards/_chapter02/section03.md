---
# this file is written in YAML http://docs.ansible.com/ansible/latest/YAMLSyntax.html
# all lines with a leading sharp are comments and will not be compiled
# longer blocks of text should start with a a leading > to escape all special characters

# URL handle for generated webpage
slug:      ch01s03
toc_entry: Tangent Vectors - Notation
# specifies layout to be used for page generation (do not modify)
layout:     card
---


## Tangent Vectors - Notation

Let $$\gamma:\mathbb R\to M$$ be a smooth curve through $$p\in M$$ such that $$\gamma(\lambda_0)=p$$. 
The _directional derivative operator_ at $$p$$ along $$\gamma$$ is the linear map

$$X_{\gamma,p}: \mathcal{C}^\infty(M) \xrightarrow{\sim} \mathbb R$$

$$f \mapsto (f\circ\gamma)'(\lambda_0)$$

where $$\mathbb R$$ is understood as a $$1$$-dimensional vector space over the field $$\mathbb R$$ and $$f\circ\gamma$$ is the point-wise function composition $$f$$ after $$\gamma$$.

Note that $$f\circ\gamma$$ is a map $$\mathbb R\to\mathbb R$$.
Hence we can calculate the 'usual' derivative and evaluate it at $$\lambda_0$$.

$$(f\circ\gamma)'(\lambda_0) = f'(\gamma(\lambda_0))$$

In differential geometry, $$X_{\gamma,p}$$ is called the _tangent vector_ to the curve $$\gamma$$ at the point $$p\in M$$. 
