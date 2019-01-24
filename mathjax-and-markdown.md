---
layout: default
---

# All Kinds of Markdown Examples 
## Header 2
### Header 3
#### Header 4
This is a normal paragraph following a header. 

## Link
[Link to another page](./another-page.html).


## Text
Text can be **bold**, _italic_, or ~~strikethrough~~.

## Equation support
$$x = {-b \pm \sqrt{b^2-4ac} \over 2a}$$

$$x = {-b \pm \sqrt{b^2-4ac} \over 2a}$$

[MathJax Syntax](http://www.onemathematicalcat.org/MathJaxDocumentation/TeXSyntax.htm)

## Diagrams
Via the [AMScd](http://www.jmilne.org/not/Mamscd.pdf) package:
$$
\require{AMScd}
\begin{CD}
K(X) @>{ch}>> H(X,\mathbb Q)\\
@VVV @VVV \\
K(Y) @>{ch}>> H(Y,\mathbb Q)
\end{CD}
$$

## Blockquote
> This is a blockquote 
>
> When something is important enough

## Code

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

```cpp
// test
int i =0;
/* just checking */
template<int n>
class A{
public:
 A var;
}
```

## Table

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

## Horizontal rule 

* * *

## Unordered list

*   Item foo
*   Item bar
*   Item baz
*   Item zip

## Ordered list

1.  Item one
1.  Item two
1.  Item three
1.  Item four

## Image

![Octocat](https://assets-cdn.github.com/images/icons/emoji/octocat.png)





[back](./)
