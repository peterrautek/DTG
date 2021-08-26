---
# this file is written in YAML http://docs.ansible.com/ansible/latest/YAMLSyntax.html
# all lines with a leading sharp are comments and will not be compiled
# longer blocks of text should start with a a leading > to escape all special characters

# URL handle for generated webpage
slug:      ch01s05
toc_entry: Tangent Spaces \(T_pM\) - Notation
# specifies layout to be used for page generation (do not modify)
layout:     card
---

## Tangent Space $$T_pM$$ - Notation

Let $$M$$ be a manifold and $$p\in M$$. The _tangent space_ $$(T_pM, \oplus, \odot)$$  to $$M$$ at $$p$$ is the vector space over $$\mathbb R$$ with underlying set

$$T_pM := \{X_{\gamma,p}\mid \gamma \text{ is a smooth curve through }p\}$$

$$\text{vector addition }\oplus: T_pM\times T_pM \to T_pM$$

$$(X_{\gamma,p},X_{\delta,p}) \mapsto X_{\gamma,p}\oplus X_{\delta,p}$$

$$\text{scalar multiplication }\odot: \mathbb R\times T_pM \to T_pM$$

$$(\lambda,X_{\gamma,p}) \mapsto \lambda \odot X_{\gamma,p}$$

Addition and scalar multiplication both defined point-wise, i.e. for any $$f\in \mathcal{C}^\infty(M)$$,

$$(X_{\gamma,p}\oplus X_{\delta,p})(f) := X_{\gamma,p}(f) + X_{\delta,p}(f)$$

$$(\lambda \odot X_{\gamma,p})(f) := \lambda X_{\gamma,p}(f)$$
