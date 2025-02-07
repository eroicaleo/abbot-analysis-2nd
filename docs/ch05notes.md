# Chapter 05 The Derivative

## 5.2 Derivatives and the Intermediate Value Property

***Definition 5.2.1 (Differentiability).***
Let $g : A → \mathbf{R}$ be a function defined on an interval $A$. Given $c ∈ A$, the derivative of $g$ at $c$ is defined by

$$ 
g'(c) = \lim_{x \to c}  \frac{
    g(x) − g(c)
}{
    x−c
}
$$

Provided this limit exists.
In this case we say $g$ is differentiable at $c$.
If $g$ exists for all points $c ∈ A$, we say that $g$ is differentiable on $A$.

***Theorem 5.2.3.*** If $g : A → \mathbf{R}$ is differentiable at a point $c ∈ A$, then $g$ is continuous at $c$ as well.

Proof: Assume $g'(c) = d$, that means given $\epsilon$, we can find $\delta$, if $x \in U_{\delta}(c)$, then $\left| \frac{g(x) - g(c)}{x - c} \right| < \epsilon$. let $\delta' = \min \{1, \delta\}$. Then if $x \in U_{\delta'}(c)$,

$$ 
\left| g(x) - g(c) \right| <
\left| \frac{g(x) - g(c)}{x - c} \right| <
\epsilon
$$

So $g$ is continuous at $c$ as well.
$\square$

***Theorem 5.2.5 (Chain Rule).***
Let $f : A → R$ and $g : B → R$ satisfy $f(A) ⊆ B$
so that the composition $g ◦ f$ is defined. If $f$
is differentiable at $c∈A$ and if $g$ is differentiable
at $f(c)∈B$,then $g◦f$ is differentiable at $c$
with $(g ◦ f)'(c) = g'(f(c)) · f'(c)$.

Proof: 

$$ 
(g ◦ f)'(c) = \lim_{x \to c}
\frac{(g ◦ f)(x)- (g ◦ f)(c)}{x - c} \\
= \lim_{x \to c} \frac{g(f(x))- g(f(c))}{f(x) - f(c)}
\cdot \frac{f(x) - f(c)}{x - c} \\
$$

Let

$$ 
d(y) = \frac{g(y) - g(f(c))}{y - f(c)}
$$

Define $d(y) = g'(f(c))$. So $d$ is continuous at $f(c)$.
So we have $g(y) - g(f(c)) = d(y)(y - c)$, $\forall y \in B$.

So we have $g(f(t)) - g(f(c)) = d(f(t))(f(t) - c)$,
$\forall t \in A$ 

So

$$ 
\frac{g(f(t))- g(f(c))}{t - c}\\
= \frac{d(f(t))(f(t) - c)}{t - c}\\
= d(f(t))\frac{(f(t) - c)}{t - c}
$$

Because $f(t)$ is continuous at $c$, $d(y)$ is continuous
at $f(c)$, so $d(f(t))$ is continuous at $t$ based on Theorem 4.3.9.
$\frac{(f(t) - c)}{t - c}$ is also continuous at $t$.
With Corollary 4.2.4 (Algebraic Limit Theorem for Functional Limits).

$$ 
\lim_{t \to c} d(f(t))\frac{(f(t) - c)}{t - c} \\
= \lim_{t \to c}d(f(t)) \cdot \lim_{t \to c} \frac{(f(t) - c)}{t - c}\\
= g'(f(c)) \cdot f'(c)
$$
$\square$

### Darboux’s Theorem

***Theorem 5.2.6 (Interior Extremum Theorem).***
Let $f$ be differentiable on an open interval $(a, b)$.
If $f$ attains a maximum value at some point $c ∈ (a, b)$
(i.e., $f(c) ≥ f(x)$ for all $x ∈ (a,b)$), then
$f'(c) = 0$. The same is true if $f(c)$ is a minimum value.

Proof:

$$
\lim_{x \to c}
\frac{f(x) - f(c)}{x - c} =
\lim_{x \to c^+}
\frac{f(x) - f(c)}{x - c} \le 0 \\
\lim_{x \to c}
\frac{f(x) - f(c)}{x - c} =
\lim_{x \to c^-}
\frac{f(x) - f(c)}{x - c} \ge 0 \\
$$

So $f'(c) = 0$.
$\square$

***Theorem 5.2.7 (Darboux's Theorem).***
If $f$ is differentiable on an interval
$[a,b]$, and if $\alpha$ satisfies $f'(a) < \alpha < f'(b)$
(or $f'(a) > \alpha > f'(b)$), then there exists a point
$c ∈ (a, b)$ where $f'(c) = \alpha$.

Proof: Consider $g(x) = f(x) - \alpha x$.

$$ 
g'(a) = f'(a) - \alpha < 0
\text{ and }
g'(b) = f'(b) - \alpha > 0
$$

* If $g(a) >= g(b)$, since $g'(b) > 0$, then exists $\delta$,
  such that if $x \in (b-\delta , b)$, $g(x) < g(b)$. Then
  $g$ attains a minimum value at some point $c ∈ (a, b)$.
  So $g'(c) = 0$ and $f'(c) = \alpha$.
* If $g(a) < g(b)$, since $g'(a) < 0$, then exists $\delta$,
  such that if $x \in (a, a+\delta)$, $g(x) < g(a)$. Then
  $g$ attains a minimum value at some point $c ∈ (a, b)$.
  So $g'(c) = 0$ and $f'(c) = \alpha$.

$\square$
