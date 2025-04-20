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

## 5.3 The Mean Value Theorems

* The ease of the proof, however, is misleading,
as it is built on top of some hard-fought accomplishments from the study of limits and continuity.
* The Mean Value Theorem is the cornerstone of the proof for almost every major theorem pertaining to differentiation.
    * We will use it to prove L’Hospital’s rules regarding limits of quotients of differentiable functions.
    * A rigorous analysis of how infinite series of functions behave when differentiated requires the Mean Value Theorem (Theorem 6.4.3)
    * It is the crucial step in the proof of the Fundamental Theorem of Calculus (Theorem 7.5.1)
    * It is also the fundamental concept underlying Lagrange’s Remainder Theorem (Theorem 6.6.3) which approximates the error between a Taylor polynomial and the function that generates it.

### Theorem 5.3.1 (Rolle’s Theorem).

Let $f : [a, b] → \mathbf{R}$ be continuous on $[a, b]$ and differentiable on $(a,b)$. If $f(a) = f(b)$, then there exists a point $c ∈ (a,b)$ where $f'(c) = 0$.

Sketch of Proof: $f$ is a continuous, so it attains
its maximum or minimum value at some point $c ∈ (a,b)$. Then $f'(c) = 0$ from
the Interior Extremum Theorem (Theorem 5.2.6).

### Theorem 5.3.2 (Mean Value Theorem).

If $f : [a, b] → \mathbf{R}$ is continuous on
$[a, b]$ and differentiable on $(a, b)$, then there exists a point $c ∈ (a, b)$ where

$$ 
f'(c)=
\frac{f(b)-f(a)}{b-a}
$$

Sketch of Proof: Let

$$ 
g(x) = \frac{f(b)-f(a)}{b-a} (x-a) - f(x)
$$

Then $g(a) = -f(a)$, $g(b) = -f(a)$. Then we can
apply Rolle theorem:

$$ 
g'(c) = \frac{f(b)-f(a)}{b-a} - f'(c) = 0
$$

So

$$ 
f'(c)=
\frac{f(b)-f(a)}{b-a}
$$

### Theorem 5.3.5 (Generalized Mean Value Theorem). 

If $f$ and $g$ are continuous on the closed interval $[a, b]$ and differentiable on the open interval
$(a, b)$, then there exists a point $c ∈ (a, b)$ where

$$ 
[f (b) − f (a)]g' (c) = [g(b) − g(a)]f' (c)
$$

If $g'$ is never zero on $(a, b)$, then the conclusion can be stated as

$$ 
\frac{f(b) - f(a)}{g(b)-g(a)} =
\frac{f'(c)}{g'(c)}
$$

Proof: See exercise 5.3.5.

$\square$

### Theorem 5.3.6 (L’Hospital’s Rule: 0/0 case).

Let $f$ and $g$ be continuous on an interval containing $a$, and assume $f$ and $g$ are differentiable on this interval with the possible exception of the point $a$. If $f(a) = g(a) = 0$ and $g'(x) \not =0$ for all $x \not =a$, then

$$ 
\lim_{x \to a} 
\frac{f'(x)}{g'(x)} = L \text{ implies }
\lim_{x \to a} 
\frac{f(x)}{g(x)} = L
$$

Proof: See Exercise 5.3.11.

### Theorem 5.3.8 (L’Hospital’s Rule: $∞/∞$ case).

Assume $f$ and $g$ are differentiable on $(a, b)$ and that $g'(x) \not = 0$ for all $x ∈ (a, b)$. If $\lim_{x→a} g(x) = ∞$ (or $−∞$), then

$$ 
\lim_{x \to a} 
\frac{f'(x)}{g'(x)} = L \text{ implies }
\lim_{x \to a} 
\frac{f(x)}{g(x)} = L
$$

Proof: We can find $\delta_1$ such that

$$
\left| 
\frac{f'(x)}{g'(x)} - L
\right| < \epsilon /2
$$

Let $t = a + \delta_1$, for any $x \in (a, t)$, we
have

$$ 
L - \epsilon / 2 <
\frac{ f(x) - f(t) }{g(x) - g(t)}
< L + \epsilon / 2
$$

We times $1 - \frac{g(t)}{g(x)}$ and get

$$ 
(1 - \frac{g(t)}{g(x)})(L - \epsilon / 2) <
(1 - \frac{g(t)}{g(x)})(\frac{ f(x) - f(t) }{g(x) - g(t)})
< (1 - \frac{g(t)}{g(x)})(L + \epsilon / 2) \\
L - \epsilon / 2 - \frac{
L g(t) - \epsilon / 2 g(t) - f(t)
}{g(x)}
< \frac{g(x)}{f(x)} <
L + \epsilon / 2 + \frac{
-L g(t) - \epsilon / 2 g(t) + f(t)
}{g(x)}
$$

As long as $x$ is close to $a$ enough,

$$ 
L - \epsilon <
\frac{ f(x) }{g(x)}
< L + \epsilon
$$ 

So

$$ 
\lim_{x \to a} 
\frac{f(x)}{g(x)} = L
$$

$\square$
