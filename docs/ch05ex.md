# Chapter 05 The Derivative

## 5.2 Derivatives and the Intermediate Value Property

### 5.2.1.
Supply proofs for parts (i) and (ii) of Theorem 5.2.4.

(i) $(f+g)'(c)=f'(c)+g'(c)$

Proof:

$$
(f+g)'(c) = \lim_{x \to c}
\frac{
    (f(x)+g(x)) - (f(c)+g(c))
}{
    x - c
} \\
= \lim_{x \to c} \frac{
    (f(x)-f(c)) + (g(x)-g(c))
}{
    x - c
} \\
= \lim_{x \to c} \frac{ (f(x)-f(c)) }{ x - c } +
\frac{ (g(x)-g(c)) }{ x - c } \\
= \lim_{x \to c} \frac{ (f(x)-f(c)) }{ x - c } +
\lim_{x \to c} \frac{ (g(x)-g(c)) }{ x - c } \\
= f'(c) + g'(c)
$$
$\square$

(ii) $(kf)'(c) = kf'(c), \text{ for all } k ∈ R$

Proof:

$$ 
(kf)′(c) = \lim_{x \to c} \frac{
    kf(x) - kf(c)
}{
    x - c
} = \lim_{x \to c} k \cdot \frac{
    f(x) - f(c)
}{x - c}\\
= k \cdot \lim_{x \to c} \frac{
    f(x) - f(c)
}{x - c} = k \cdot f'(c)
$$
$\square$

### 5.2.2.

Exactly one of the following requests is impossible. Decide which it is, and provide examples for the other three. In each case, let’s assume the functions are defined on all of $\mathbf{R}$.

(a) Functions $f$ and $g$ not differentiable at zero but where $fg$ is differentiable at zero.

Solution: Consider $f = g = \left| x \right|$.

(b) A function $f$ not differentiable at zero and a function $g$ differentiable at zero where $fg$ is differentiable at zero.

Solution: Consider $f = \left| x \right|$, and $g = 0$.

(c) A function $f$ not differentiable at zero and a function $g$ differentiable at zero where $f + g$ is differentiable at zero.

Solution: this is not possible. $f = (f+g) - g$.

(d) A function $f$ differentiable at zero but not differentiable at any other point.

Solution: Consider a modified version of modified Dirichlet function.

$$ 
f(x) = \begin{cases}
    x^2 & x \in \mathbf{Q}\\
    0   & x \in \mathbf{I}\\
\end{cases} 
$$
$\square$

### 5.2.3.

(a) Use Definition 5.2.1 to produce the proper formula for
the derivative of h(x) = 1/x.

Proof:

$$ 
h'(c) = \lim_{x \to c} \frac{
    1/x - 1/c
}{x - c}\\
= \lim_{x \to c} -\frac{1}{xc}\\
= -\frac{1}{c^2}
$$

So $h'(x) = -\frac{1}{x^2}$.

$\square$

(b) Combine the result in part (a) with the Chain Rule
(Theorem 5.2.5) to
supply a proof for part (iv) of Theorem 5.2.4.

Proof: the part (iv) of Theorem 5.2.4 is this:

$$ 
(f /g)' (c) = \frac{
    g(c)f'(c)−f(c)g'(c) 
}{[g(c)]^2}, \text{ provided that }g(c) \neq 0
$$

Here is the proof:

$$ 
(f /g)(c) = f(c) \cdot \frac{1}{g(c)}
$$

So

$$ 
(f /g)'(c) = f'(c) \cdot \frac{1}{g(c)} + f(c) (\frac{1}{g(c)})'\\
= f'(c) \cdot \frac{1}{g(c)} -
f(c) (\frac{1}{[g(c)]^2})g'(c)\\
= \frac{
    g(c)f'(c)−f(c)g'(c) 
}{[g(c)]^2}
$$
$\square$

(c) Supply a direct proof of Theorem 5.2.4 (iv) by 
algebraically manipulating the difference quotient for
$(f/g)$ in a style similar to the proof of Theorem 5.2.4 (iii).

Proof:

$$ 
(f /g)(c) = \frac{f(c) }{g(c)}
$$

So

$$ 
(f /g)'(c) = \lim_{x \to c}
\frac{
    \frac{f(x) }{g(x)} - \frac{f(c) }{g(c)}
}{
    x - c
}\\
= \lim_{x \to c}
\frac{
    \frac{f(x)g(c) - g(x)f(c) }{g(x)g(c)}
}{
    x - c
}\\
= \lim_{x \to c} \frac{1}{g(x)g(c)} \cdot
\lim_{x \to c} \frac{
    (f(x) - f(c))g(c) - (g(x) - g(c))f(c)
}{
    x - c
}\\
= \frac{
    g(c)f'(c)−f(c)g'(c) 
}{[g(c)]^2}
$$

$\square$

### 5.2.4.

Follow these steps to provide a slightly modified proof of the Chain Rule.

(a) Show that a function $h:A→\mathbf{R}$ is differentiable
at $a∈A$ if and only if there exists a function
$l : A → \mathbf{R}$ which is continuous at $a$
and satisfies

$$ 
h(x) − h(a) = l(x)(x − a) \text{ for all } x ∈ A.
$$

Proof:

$\Rightarrow$ Assume $h$ is differentiable at $a$, let

$$ 
l(x) = \begin{cases}
    \frac{ h(x) - h(a) }{x - a} &\text{if } x \not = a\\
    h'(a) &\text{if } x = a\\
\end{cases} 
$$

Then we have

$$ 
\lim_{x \to a} l(x) = \lim_{x \to a} 
\frac{ h(x) - h(a) }{x - a} = h'(a) = l(a)
$$

So $l(x)$ is continuous at $a$.

* When $x = a$, $h(a) - h(a) = 0 = l(a)(a-a)$.
* When $x \not = a$,
$l(x)(x-a)=\frac{ h(x) - h(a) }{x - a}(x-a)=h(x)-h(a)$.

$\Leftarrow$ If there exists a function
$l : A → \mathbf{R}$ which is continuous at $a$
and satisfies

$$ 
h(x) − h(a) = l(x)(x − a) \text{ for all } x ∈ A.
$$

Then

$$ 
\lim_{x \to a} 
\frac{ h(x) - h(a) }{x - a} = 
\lim_{x \to a} l(x) = l(a)
$$

So $h$ is differentiable at $a∈A$. $\square$

(b) Use this criterion for differentiability (in both directions) to prove Theorem 5.2.5.

Proof: $g$ is differentiable at $f(c)$, we can find a function $l$ such that $g(f(x)) - g(f(c)) = l(f(x))(f(x) - f(c)) = l(f(x))m(x)(x - c)$ where

$$ 
l(y) = \begin{cases}
    \frac{ g(y) - g(f(c)) }{y - f(c)} &\text{if } y \not = f(c)\\
    g'(f(c)) &\text{if } y = f(c)\\
\end{cases} \\
m(x) = \begin{cases}
    \frac{ f(x) - f(c) }{x - c} &\text{if } x \not = c\\
    f'(c) &\text{if } x = c\\
\end{cases} 
$$

So we have

$$ 
\lim_{x \to c} l(f(x))m(x) =\\
\lim_{x \to c} l(f(x)) \lim_{x \to c} m(x) =\\
l(f(c))m(c) = g'(f(c))f'(c)
$$
$\square$

### 5.2.5.

Let

$$ 
f(x) = \begin{cases}
    x^a &\text{if } x > 0\\
    0   &\text{if } x \le 0\\
\end{cases} 
$$

For which values of $a$ is $f$ continuous at zero?

Solution:

* For $a > 0$, $\lim_{x \to 0} f(x) = 0$, so $f$ is continuous at zero.
* For $a = 0$, $\lim_{x \to 0} f(x) = 1$, so $f$ is not continuous at zero.
* For $a < 0$, $\lim_{x \to 0} f(x) = +\infty$, so $f$ is not continuous at zero.

(b) For which values of $a$ is $f$ differentiable at zero? In this case, is the derivative function continuous?

Solution:

$$ 
\lim_{x \to 0^+} \frac{x^a - 0}{x - 0} = x^{a - 1} \\
\lim_{x \to 0^-} \frac{0 - 0}{x - 0} = 0 \\
$$

So
* For $a > 1$, $\lim_{x \to 0} x^{a-1} = 0$, so $f$ is differentiable at zero. Further more, the derivative function
is also continuous.
* For $a <= 1$, $\lim_{x \to 0} x^{a-1} \not = 0$, so $f$ is not differentiable at zero.

(c) For which values of $a$ is $f$ twice-differentiable?

Solution: we can use the same analysis and see $a > 2$, then
$f$ is twice-differentiable.

### 5.2.6.
Let $g$ be defined on an interval $A$, and let $c ∈ A$.

(a) Explain why $g'(c)$ in Definition 5.2.1 could have
been given by

$$ 
g'(c) = \lim_{h \to 0} 
\frac{g(c+h) - g(c)}{h}
$$

Proof: the Definition 5.2.1 is

$$ 
g'(c) = \lim_{x \to c} 
\frac{g(x) - g(c)}{x - c}
$$

For any given $x$ we can find $h$ such that $x = c+h$,
so

$$ 
\frac{g(x) - g(c)}{x - c} =
\frac{g(c+h) - g(c)}{(c+h)-c} = 
\frac{g(c+h) - g(c)}{h}
$$

when $(x) \rightarrow c$, we have $(h) \rightarrow 0$.
So

$$ 
\lim_{x \to c} 
\frac{g(x) - g(c)}{x - c} =
\lim_{h \to 0} 
\frac{g(c+h) - g(c)}{h}
$$
$\square$

(b) Assume $A$ is open. If $g$ is differentiable at
$c ∈ A$, show

$$ 
g'(c) = \lim_{h \to 0}
\frac{g(c+h)-g(c-h)}{2h} 
$$

Proof: Similar to (a), we can show

$$ 
g'(c) = 
\lim_{h \to 0} 
\frac{g(c) - g(c-h)}{h}
$$

So

$$ 
2g'(c) = \lim_{h \to 0} 
\frac{g(c+h) - g(c)}{h}
+
\lim_{h \to 0} 
\frac{g(c) - g(c-h)}{h} \\
=
\lim_{h \to 0} 
\frac{(g(c+h) - g(c))+(g(c) - g(c-h))}{h}\\
=
\lim_{h \to 0} 
\frac{g(c+h) - g(c-h)}{h}
$$

$\square$

### 5.2.7.

Let

$$ 
g_a(x) =
\begin{cases}
    x^a \sin (1/x) &\text{if } x \not = 0\\
    0 &\text{if } x = 0\\
\end{cases} 
$$

Find a particular (potentially noninteger)
value for a so that 

(a) $g_a$ is differentiable on $\mathbf{R}$ but such that
$g_a$ is unbounded on $[0, 1]$.

Solution:

$$ 
g'(0) = \lim_{x \to 0} 
\frac{x^a \sin (1/x)}{x}
= \lim_{x \to 0}  x^{a-1} \sin (1/x) \\
g'(c) = ac^{a-1} \sin(1/c) - c^{a-2} \cos (1/c)
$$

Then $a = 1.5$ will be good for this case.

(b) $g_a$ is differentiable on $\mathbf{R}$ with
$g'_a$ continuous but not differentiable at zero.

$$ 
g'(x) =
\begin{cases}
    \lim_{x \to 0}  x^{a-1} \sin (1/x) &\text{if } x = 0\\
    ax^{a-1} \sin(1/x) - x^{a-2} \cos (1/x) &\text{if } x \not = 0\\
\end{cases}
$$

When $a = 2.5$,

$$ 
g_{2.5}'(x) =
\begin{cases}
    0 &\text{if } x = 0\\
    2.5x^{1.5} \sin(1/x) - x^{0.5} \cos (1/x) &\text{if } x \not = 0\\
\end{cases}
$$

So, $g_{2.5}'(x)$ is continuous at 0 because    

$$ 
\lim_{x \to 0} g_{2.5}'(x) = 0 = g_{2.5}'(0) 
$$

But

$$ 
\lim_{x \to 0}
\frac{g_{2.5}'(x)}{x} =
\frac{2.5x^{1.5} \sin(1/x) - x^{0.5} \cos (1/x)}{x}\\
= 2.5x^{0.5} \sin(1/x) - x^{-0.5} \cos (1/x) \rightarrow -\infty
$$

So $g_{2.5}'(x)$ is not differentiable at 0.

(c) $g_a$ is differentiable on $\mathbf{R}$ and
$g'_a$ is differentiable on $\mathbf{R}$ but
$g''_a$ is not continuous at zero.

When $a = 3.5$

$$ 
g_{3.5}'(x) =
\begin{cases}
    0 &\text{if } x = 0\\
    3.5x^{2.5} \sin(1/x) - x^{1.5} \cos (1/x) &\text{if } x \not = 0\\
\end{cases}\\
g_{3.5}''(x) =
\begin{cases}
    0 &\text{if } x = 0\\
    h(x) - x^{-0.5}\sin (1/x) &\text{if } x \not = 0\\
\end{cases}\\
$$

Then $\lim_{x \to 0} g_{3.5}''(x)$ does not exist.

### 5.2.8.

Review the definition of uniform continuity (Definition 4.4.4).
Given a differentiable function $f : A → \mathbf{R}$,
let’s say that $f$ is uniformly differentiable on $A$ if,
given $ε > 0$ there exists a $δ > 0$ such that

$$ 
\left| 
\frac{f(x) - f(y)}{x - y}
-
f'(y)
 \right| < \epsilon
$$

whenever $0 < |x-y| < \delta$.

(a) Is $f(x) = x^2$ uniformly differentiable on $\mathbf{R}$?
How about $g(x) = x^3$?

Solution:
$$ 
\left| 
\frac{x^2 - y^2}{x - y} - 2x
\right|
= |x - y|
$$

So $x^2$ is uniformly differentiable.

$$ 
\left| 
\frac{x^3 - y^3}{x-y} - 3y^2
 \right| =
 \left| 
    x^2 + xy + y^2 - 3y^2
  \right| =
  \left| 
    x^2+xy-2y^2
   \right|\\
   = |(x + 2y)(x - y)|
$$

So $x^3$ is not uniformly differentiable.

(b) Show that if a function is uniformly differentiable
on an interval $A$, then the derivative must be continuous
on $A$.

Proof: Assume $f$ is uniformly differentiable
on an interval $A$, then for any $\epsilon$, we can find
$\delta$ such that

$$ 
\left| 
\frac{f(x) - f(y)}{x - y}
-
f'(y)
 \right| < \epsilon / 2 \text{ and }
\left| 
\frac{f(x) - f(y)}{x - y}
-
f'(x)
 \right| < \epsilon / 2
$$

So $|f'(x) - f'(y)| < \epsilon$, then $f'(x)$ is continuous
on $A$.

(c) Is there a theorem analogous to Theorem 4.4.7 for
differentiation? Are functions that are differentiable
on a closed interval $[a, b]$ necessarily uniformly
differentiable?

Proof: Again we consider

$$ 
g_{1.5}(x) =
\begin{cases}
    x^{1.5} \sin (1/x) &\text{if } x \not = 0\\
    0 &\text{if } x = 0\\
\end{cases}
$$

and

$$ 
g'(x) =
\begin{cases}
    \lim_{x \to 0}  x^{0.5} \sin (1/x) = 0&\text{if } x = 0\\
    1.5x^{1.5-1} \sin(1/x) - x^{1.5-2} \cos (1/x) &\text{if } x \not = 0\\
\end{cases}
$$

$g'(x)$ is not continuous at 0, so $g(x)$ is not uniformly
differentiable.

### 5.2.9.

Decide whether each conjecture is true or false.
Provide an argument for those that are true and a
counterexample for each one that is false.

(a) If $f'$ exists on an interval and is not constant,
then $f$ must take on some irrational values.

Proof: True. It's theorem 5.2.7 (Darboux's Theorem).

(b) If $f'$ exists on an open interval and there is some point $c$ where $f'(c) > 0$,
then there exists a $δ$-neighborhood $V_{\delta}(c)$ around $c$ in which $f'(x) > 0$ for all $x ∈ V_δ(c)$.

Solution: False. Consider

$$ 
f(x) =
\begin{cases}
    0.5x + x^2 \sin (1/x) &\text{if } x \not = 0\\
    0 &\text{if } x = 0\\
\end{cases}
\\
f'(x) =
\begin{cases}
    0.5 + 2 x \sin(1/x) - \cos (1/x) &\text{if }  x \not = 0\\
    0.5 &\text{if } x = 0\\
\end{cases}
$$

So when $x = \frac{1}{n \pi }$, $f'(x) = -0.5 < 0$.  

$\square$

(c) If $f$ is differentiable on an interval containing zero and if $\lim_{x \to 0} f'(x) = L$, then it must be that
$L = f'(0)$.

Proof: Assume

$$ 
f'(0) = \lim_{x \to 0} \frac{f(x) - f(0)}{x} = L'
$$

And $L' \not = L$. We also have

$$ 
\left|  \frac{f(x+h) - f(x)}{h} -
\frac{f(h) - f(0)}{h} \right| \\
=\frac{x}{h} \left| 
\frac{f(x+h) - f(h)}{x} -
\frac{f(x) - f(0)}{x}
\right|\\
\leq \frac{x}{h} \left|
\frac{f(x+h) - f(h)}{x} \right| +
\left| \frac{f(x) - f(0)}{x} \right|
$$

Then as long as $x, h$ is small enough,
$\frac{f(x+h) - f(x)}{h}$ and
$\frac{f(h) - f(0)}{h}$ can be arbitrarily close.

We also have as long as $x, h$ is small enough,
$\frac{f(x+h) - f(x)}{h}$ can be arbitrarily close $L$.

As long as $x, h$ is small enough, $\frac{f(x) - f(0)}{x}$
can be arbitrarily close $L'$.

So it's impossible that $L \not = L'$.
