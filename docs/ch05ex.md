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

Proof: This proof is not correrct. I think I miss this part.
* I want to prove $f(x)$ is uniformly differentiable around
$0$, i.e. given $\epsilon$ we can find $U_{\delta}(0)$ such that
$\left| \frac{f(x+h) - f(x)}{h} - f'(x) \right| < \epsilon, \forall
x \in U_{\delta}(0)$.
 
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

### 5.2.10.

Recall that a function $f : (a, b) → R$ is increasing on $(a, b) \text{ if } f (x) ≤ f (y)$ whenever $x < y$ in $(a, b)$. A familiar mantra from calculus is that a differentiable function is increasing if its derivative is positive, but this statement requires some sharpening in order to be completely accurate.

Show that the function

$$ 
f(x) =
\begin{cases}
    0.5x + x^2 \sin (1/x) &\text{if } x \not = 0\\
    0 &\text{if } x = 0\\
\end{cases}
$$

is differentiable on $\mathbf{R}$ and satisfies $g'(0) > 0$. Now, prove that $g$ is not increasing over any open interval containing $0$.

Proof: from 5.2.9 (b), we have

$$
f'(x) =
\begin{cases}
    0.5 + 2 x \sin(1/x) - \cos (1/x) &\text{if }  x \not = 0\\
    0.5 &\text{if } x = 0\\
\end{cases}
$$

So $g'(0) = 0.5 > 0$. Consider $x = \frac{1}{n \pi}$, $g'(x) < 0$. So $g(x - h) > g(x)$ for small $h$.

### 5.2.11.

Assume that $g$ is differentiable on $[a, b]$ and satisfies $g'(a) < 0 < g'(b)$.

(a) Show that there exists a point $x ∈ (a, b)$ where $g(a) > g(x)$, and a point $y ∈ (a, b)$ where $g(y) < g(b)$.

Proof: See my proof of Theorem 5.2.7.

(b) Now complete the proof of Darboux’s Theorem started earlier.

Proof: See my proof of Theorem 5.2.7.

### 5.2.12 (Inverse functions).

If $f : [a, b] → \mathbf{R}$ is one-to-one, then there exists an inverse function $f^{−1}$ defined on the range of $f$ given by $f^{−1}(y) = x$ where $y = f(x)$.
In Exercise 4.5.8 we saw that if f is continuous on $[a,b]$, then $f^{−1}$ is continuous on its domain. Let’s add the assumption that $f$ is differentiable on $[a,b]$
with $f'(x) \not = 0$ for all $x ∈ [a,b]$. Show $f^{−1}$ is differentiable with

$$ 
(f^{-1})'(y) = \frac{1}{f'(x)} \text{ where } y = f(x).
$$

Proof: Let $f^{-1} = g$, and assume $f(x_0) = y_0$ and
$g(y_0) = x_0$. We want to prove $g'(y_0) = 1 / f'(x_0)$,
i.e. 

$$ 
1/f'(y_0) = \lim_{y \to y_0}
\frac{g(y) - g(y_0)}{y - y_0} 
$$

First we show give $\delta$, we can find $\zeta$, if
$y \in V_{\zeta}(y_0)$, then $x \in V_{\delta }(x_0)$. We can refer to Exercise 4.5.8 to show $f$ and
$g$ is monotone function first.
We can prove this directly. Given sequence $(y_n) \rightarrow y_0$, and $g(y_n) = x_n \not \in V_{\delta }(x_0)$, since $(x_n)$ is bounded, we can
find subsequence that converges to $x_1 \not = x_0$.
Since $f$ is continuous, $f(x_1) = y_0$, $f$ is
not 1 to 1, we have a contradiction.

Next, given $\epsilon$, we show we can find $\delta$, such that,
$x \in U_{\delta}(x_0)$,

$$ 
\left| 
\frac{x - x_0}{f(x) - f(x_0)}
-
\frac{1}{f'(x_0)}
\right| < \epsilon
$$
$\square$

## 5.3 The Mean Value Theorems

### 5.3.1.

Recall from Exercise 4.4.9 that a function $f : A → \mathbf{R}$ is Lipschitz on $A$ if there exists an $M > 0$ such that

$$ 
\left| 
\frac{f(x) - f(y)}{x-y}
\right| \leq M
$$

for all $x \leq y$ in $A$.

(a) show $f$ is differentiable on a closed interval
$[a, b]$ and if $f'$ is continuous on $[a, b]$, then
$f$ is Lipschitz on $[a, b]$.

Proof: Since $f'(x)$ is continuous on $[a, b]$,
based on Extreme Value Theorem, let $f'(c) = M$ is the maximum of $|f'(x)|$.

Then apply the Mean Value Theorem, we have

$$ 
\left| 
\frac{f(x) - f(y)}{x-y}
\right| = |f'(c)| \leq M
$$

$\square$

(b) Review the definition of a contractive function in Exercise 4.3.11. If we add the assumption that $|f'(x)| < 1$ on $[a,b]$, does it follow that $f$ is contractive on this set?

Proof: Since $f'(x)$ is continuous on $[a, b]$,
we have $f'(c) = M < 1$, then $f$ is contractive on this set.

Furthermore, we can even remove the assumption that
$f'(x)$ is continuous. Assume given any $n$, we
can find 

### 5.3.2.

Let $f$ be differentiable on an interval $A$. If $f'(x) \not = 0$ on $A$, show that $f$ is one-to-one on $A$. Provide an example to show that the converse statement need not be true.

Proof: If $f(a) = f(b)$, then we can find $c \in (a,b)$ such that

$$ 
0 = \frac{
f(b) - f(a)
}{
b - a
} = f'(c)
$$

then we have a contradiction, so $f$ is one-to-one on
$A$.

A example is $f(x) = \cos x, x \in [0, \pi]$.
We have $f'(0) = f'(\pi) = 0$. But $f$ is still
one-to-one on $A$.

### 5.3.3.

Let $h$ be a differentiable function defined on the interval $[0, 3]$, and assume that $h(0) = 1, h(1) = 2$, and $h(3) = 2$.

(a) Argue that there exists a point $d ∈ [0, 3]$
where $h(d) = d$.

Proof: let $f(x) = h(x) - x$, $f$ is continuous 
function on $[0, 3]$. $f(1) = -1 < 0$ and $f(3) = 1 > 0$, according to Intermediate Value Property, we
can find $d \in (1, 3)$ such that $f(d) = 0$, so
$h(d) = d$.

(b) Argue that at some point $c$ we have $h'(c) = 1/3$

Proof: Based on Mean Value theorem, we can find $c$
such that

$$ 
h'(c) = \frac{h(3) - h(0)}{3 - 0} = \frac{1}{3}
$$

$\square$

(c) Argue that $h'(x) = 1/4$ at some point in the domain.

Proof: Let $g(x) = h(x) - h(x - 1), x \in [1, 3]$.
We don't know what $h(2)$.
* $h(2) > 2$, then $g(3) = h(3) - h(2) < 0$.  
* $h(2) = 2$, then $g(2) = h(2) - h(1) = 0$.  
* $h(2) < 2$, then $g(2) = h(2) - h(1) < 0$.

Whatever the case, we can find some $d$ such that
$g(1) = 1, g(d) \leq 0$. Since $g(x)$ is continuous,
we can find $g(c) = 1/4$.

Then

$$ 
g'(e) = \frac{h(c) - h(c-1)}{1} = \frac{1}{4} 
$$

$\square$

### 5.3.4.

Let $f$ be differentiable on an interval $A$ containing zero, and
assume $(x_n)$ is a sequence in $A$ with $(x_n) → 0$ and $x_n  \not = 0$.

(a) If $f(x_n)=0$ for all $n∈N$,show $f(0)=0$ and $f'(0)=0$.

Proof: Since $f(x)$ is continuous, we have
$\lim_{x_n \to 0} f(x_n) = f(0)$, so $f(0) = 0$.

We also have

$$ 
f'(0) = \lim_{x_n \to 0} 
\frac{f(x_n) - f(0)}{x_n - 0}
= 0
$$

$\square$

(b) Add the assumption that $f$ is twice-differentiable at zero and show that
$f''(0)=0$ as well.

Proof:

For $x_n$, according to mean value theorem, we can
find $y_n \in (0, x_n)$, such that

$$ 
0 = \frac{f(x_n) - f(0)}{x_n - 0} = f'(y_n)
$$

As a result, we can find $(y_n) \rightarrow 0$ such
that $f'(y_n) = 0$. So we use (a) and we can conclude
$f''(0) = 0$ as well.

### 5.3.5.

(a) Supply the details for the proof of Cauchy’s Generalized Mean Value Theorem (Theorem 5.3.5).

Proof: Let

$$ 
h(x) = (f(b) - f(a))g(x) - (g(b) - g(a))f(x)
$$

Then

$$ 
h(b) = (f(b) - f(a))g(b) - (g(b) - g(a))f(b)\\
=f(b)g(a) - f(a)g(b)\\
$$
and
$$
h(a) = (f(b) - f(a))g(a) - (g(b) - g(a))f(a) \\
=
$$

So $h(a) = h(b)$, so we can find $c$,
such that $h'(c) = 0$, i.e.

$$ 
h'(c) = (f(b) - f(a))g'(c) - (g(b) - g(a))f'(c) = 0
$$

Then

$$ 
\frac{f(b) - f(a)}{g(b)-g(a)} =
\frac{f'(c)}{g'(c)}
$$

$\square$

(b) Give a graphical interpretation of the Generalized Mean Value Theorem analogous to the one given for the Mean Value Theorem at the beginning of Section 5.3. (Consider $f$ and $g$ as parametric equations for a curve.)

Solution: Consdier a curve $(g(x), f(x))$. At
a point $c$, the derivative is

$$ 
\lim_{x \to c}
\frac{f(x) - f(c)}{g(x) - g(c)}
= \lim_{x \to \infty} 
\frac{
\frac{f(x) - f(c)}{x-c}
}{
\frac{g(x) - g(c)}{x-c}
} =
\frac{f'(c)}{g'(c)}
$$
$\square$

### 5.3.6.

(a) Let $g : [0,a] → \mathbf{R}$ be differentiable, $g(0) = 0$, and $|g'(x)| ≤ M$ for all $x ∈ [0,a]$. Show $|g(x)| ≤ Mx$ for all $x ∈ [0,a]$.

Proof: When $x = 0$, $g(0) = 0 \le M \cdot 0$.

When $x \not = 0$, from Mean value theorem

$$ 
\left|
\frac{g(x)-g(0)}{x-0}
\right| = |g'(c)| \le M 
$$

So

$$ 
|g(x)| \le Mx
$$ 

$\square$

(b) Let $h : [0, a] → \mathbf{R}$ be twice differentiable, $h'(0) = h(0) = 0$ and $|h''(x)| ≤ M$ for all $x ∈ [0,a]$. Show $|h(x)| ≤ Mx^2/2$ for all $x ∈ [0,a]$.

Proof: This time we need to use Generalized Mean
Value Theorem. Let $f(x) = Mx^2/2$ 

From (a) we know $|h'(x)| \le Mx$.

$$ 
\left|\frac{h(x)}{f(x)}\right| = 
\left|
\frac{
h(x) - h(0)
}{
f(x) - f(0)
}
\right| 
=
\left|
\frac{
    h'(c)
}{f'(c)}
\right| \le
\left| 
\frac{Mx}{Mx}
\right| = 1
$$

So $|h(x)| \leq f(x) = Mx^2/2$

$\square$

(c) Conjecture and prove an analogous result for a function that is differentiable three times on $[0, a]$.

Solution: the conjecture should be like this:

Let $h : [0, a] → \mathbf{R}$ be three times differentiable, $h''(0) = h'(0) = h(0) = 0$ and $|h'''(x)| ≤ M$ for all $x ∈ [0,a]$. Show $|h(x)| ≤ Mx^3/6$ for all $x ∈ [0,a]$.

Proof: We already know $|h'(x)| \leq Mx^2/2$.
And let $f(x) = Mx^3/6$.

$$ 
\left|\frac{h(x)}{f(x)}\right| = 
\left|
\frac{
h(x) - h(0)
}{
f(x) - f(0)
}
\right| 
=
\left|
\frac{
    h'(c)
}{f'(c)}
\right| \le
\left| 
\frac{Mx^2/2}{Mx^2/2}
\right| = 1
$$

So $|h(x)| \leq f(x) = Mx^3/6$.

$\square$

### 5.3.7.

A fixed point of a function $f$ is a value $x$ where $f(x) = x$. Show that if $f$ is differentiable on an interval with $f'(x) \not = 1$, then $f$ can have at most one fixed point.

Proof: If $f(x) = x, f(y) = y, x \not = y$.
Then

$$ 
\frac{f(x) - f(y)}{x - y} =
\frac{x - y}{x - y} = 1 
$$

We have a contradiction.

$\square$

### 5.3.8.

Assume $f$ is continuous on an interval containing zero and differentiable for all $x \not = 0$. If $\lim_{x \to 0} f'(x) = L$, show $f'(0)$ exists and equals $L$.

Proof:

$$ 
f'(0) = \lim_{x \to 0}
\frac{f(x)-f(0)}{x - 0} \\
= \lim_{x \to 0} \frac{f'(c)}{g'(c)}\\
= L
$$

### 5.3.9.

Assume $f$ and $g$ are as described in Theorem 5.3.6, but now
add the assumption that $f$ and $g$ are differentiable at $a$, and $f'$ and $g'$ are continuous at $a$ with $g'(a)\not = 0$. Find a short proof for the $0/0$ case of L’Hospital’s Rule under this stronger hypothesis.

Proof:

$$ 
\lim_{x \to a}
\frac{f(x)}{g(x)}\\
= \lim_{x \to a}
\frac{f(x)-f(a)}{g(x)-g(a)}\\
= \lim_{x \to a}
\frac{\frac{f(x)-f(a)}{x-a}}
{\frac{g(x)-g(a)}{x-a}}\\
= \frac{
\lim_{x \to a} \frac{f(x)-f(a)}{x-a}   
}{
\lim_{x \to a} \frac{g(x)-g(a)}{x-a}
}\\
=\frac{f'(a)}{g'(a)}
$$

### 5.3.10.

Let $f(x) = x \sin(1/x^4) e^{−1/x^2}$ and $g(x) = e^{−1/x^2}$. Using the familiar properties of these 
functions, compute the limit as $x$ approaches zero of $f(x), g(x), f(x)/g(x), f'(x)/g'(x)$.

Solution: Let $h(x) = x \sin(1/x^4)$. For $x \not = 0$, we have

$$ 
h'(x) =
\sin (1/x^4) + x \cos (1/x^4) \cdot (-4)\cdot 1/x^5
= \sin (1/x^4) - 4 /x^{4} \cos (1/x^4)
\\
g'(x) = -2 x^{-3} e^{−1/x^2}
$$

$$ 
\lim_{x \to 0} f(x) = 0\\
\lim_{x \to 0} g(x) = 0\\
\lim_{x \to 0} f(x)/g(x) =
\lim_{x \to 0} h(x) = 0\\
$$

See the [stackexchange](https://math.stackexchange.com/questions/2055368/counterexample-to-lhopitals-rule-as-an-exercise-in-understanding-analysis) discussion.

$\square$

### 5.3.11.

(a) Use the Generalized Mean Value Theorem to furnish a proof of the $0/0$ case of L’Hospital’s Rule (Theorem 5.3.6).

Proof:

$$ 
\frac{f(x)}{g(x)} =
\frac{f(x) - f(0)}{g(x) - g(0)}
= \frac{f'(c_x)}{g'(c_x)}
$$

Given $\epsilon > 0$, we can find $\delta$,
if $x \in V_{\delta}(0)$,

$$ 
\left| 
\frac{f'(x)}{g'(x)} - L
 \right| < \epsilon
$$

So we have

$$ 
\lim_{x \to a}
\frac{f(x)}{g(x)} = L
$$

$\square$

(b) If we keep the first part of the hypothesis of Theorem 5.3.6 the same but
we assume that

$$ 
\lim_{x \to a}
\frac{f'(x)}{g'(x)} = \infty
$$

does it necessarily follow that

$$ 
\lim_{x \to a}
\frac{f(x)}{g(x)} = \infty
$$

Proof:

$$ 
\frac{f(x)}{g(x)} =
\frac{f(x) - f(0)}{g(x) - g(0)}
\\
= \frac{f'(c)}{g'(c)}, c \in (0, x) 
$$

Since $\lim_{x \to a} \frac{f'(x)}{g'(x)} = \infty$,
then give $N$, we can find $V_{\delta}(a)$, if $x \in V_{\delta}(a)$, $\lim_{x \to a} \frac{f'(x)}{g'(x)} > N$, so $\frac{f(x)}{g(x)} > N$.

That means 

$$ 
\lim_{x \to a}
\frac{f(x)}{g(x)} = \infty
$$

### 5.3.12.

If $f$ is twice differentiable on an open interval containing $a$ and $f''$ is continuous at $a$, show

$$ 
\lim_{h \to 0}
\frac{
f(a+h) - 2 f(a) + f(a-h)
}{
h^2
} = f''(a)
$$

Proof: Let $g(h) = f(a+h) - 2 f(a) + f(a-h)$,
then $g(0) = 0$,

$$
\lim_{h \to 0}
\frac{
g'(h)
}{2h}
= \lim_{h \to 0}
\frac{
f'(a+h) - f'(a-h)
}{2h} = f''(a)
$$

Another approach:



$\square$

