# Chapter 06 Sequences and Series of Functions

## 6.2 Uniform Convergence of a Sequence of Functions

### 6.2.1.

Let

$$ 
f_n(x) = \frac{nx}{1+ nx^2}
$$

Anwser

(a) Find the pointwise limit of $(f_n)$ for all $x ∈ (0,∞)$.

Solution:

$$ 
f_n(x) = \frac{nx}{1+ nx^2} \\
= \frac{x}{1/n + x^2}
$$

So

$$ 
f(x) = \frac{1}{x}
$$

$\square$

(b) Is the convergence uniform on $(0,∞)$

**Solution**:

$$ 
\frac{nx}{1+ nx^2} - \frac{1}{x}\\
=\frac{nx^2-1-nx^2}{x + nx^3} \\
= - \frac{1}{x + nx^3}
$$

So the convergence is not uniform.

(c) Is the convergence uniform on $(0,1)$?

**Solution**: No.

(d) Is the convergence uniform on $(1,∞)$?

**Solution**: Yes.

$$ 
\left| \frac{1}{x + nx^3} \right|
< \left| \frac{1}{1 + n} \right| 
$$

$\square$

### 6.2.2.

(a) Define a sequence of functions on $\mathbf{R}$ by

$$ 
f_n(x) =
\begin{cases}
    1 &\text{if } x = 1, 1/2, 1/3, \dots, 1/n \\
    0 &\text{otherwise}\\
\end{cases} 
$$

and let $f$ be the pointwise limit of $f_n$.
Is each $f_n$ continuous at zero? Does $f_n → f$ uniformly on $\mathbf{R}$? Is $f$ continuous at zero?

**Solution**:

$$ 
f(x) =
\begin{cases}
    1 &\text{if } x = 1, 1/2, 1/3, \dots\\
    0 &\text{otherwise}\\
\end{cases} 
$$

Each $f_n$ is continuous at zero. $f_n$ does not converge to
$f$ uniformly. $f$ is not continuous at zero.

(b) Repeat this exercise using the sequence of functions

$$ 
g_n(x) =
\begin{cases}
    x &\text{if } x = 1, 1/2, 1/3, \dots, 1/n \\
    0 &\text{otherwise}\\
\end{cases} 
$$

**Solution**:

$$ 
g(x) =
\begin{cases}
    x &\text{if } x = 1, 1/2, 1/3, \dots\\
    0 &\text{otherwise}\\
\end{cases} 
$$

Each $g_n$ is continuous at zero. $g_n$ converges to
$g$ uniformly. $g$ is continuous at zero.

(c) Repeat this exercise using the sequence of functions

$$ 
h_n(x) =
\begin{cases}
    1 &\text{if } x = 1/n \\
    x &\text{if } x = 1, 1/2, 1/3, \dots, 1/(n-1) \\
    0 &\text{otherwise}\\
\end{cases} 
$$

**Solution**:

$$ 
h(x) =
\begin{cases}
    x &\text{if } x = 1, 1/2, 1/3, \dots\\
    0 &\text{otherwise}\\
\end{cases} 
$$

Each $h_n$ is continuous at zero. $h_n$ does not converge to
$h$ uniformly. $h$ is continuous at zero.

$\square$

### 6.2.3.

For each $n ∈ \mathbf{N}$ and $x ∈ [0,∞)$, let

$$
g_n(x) = \frac{x}{1 + x^n} \text{ and }
h_n(x) = 
\begin{cases}
    1  &\text{if } x \geq 1/n\\
    nx &\text{if } 0 \leq x  < 1/n\\
\end{cases} 
$$

Answer the following questions for the sequences $(g_n)$ and $(h_n)$:

(a) Find the pointwise limit on $x ∈ [0,∞)$

$$ 
g(x) =
\begin{cases}
    x &\text{if } 0 \leq x < 1 \\
    1/2 &\text{if } x = 1\\
    0 &\text{if } x > 1\\
\end{cases}
\\
h(x) =
\begin{cases}
    0 &\text{if } x = 0\\
    1 &\text{if } x > 0\\
\end{cases} 
$$

$\square$

(b) Explain how we know that the convergence cannot be uniform on $[0,∞)$.

Proof: Both $g(x)$ and $h(x)$ are not continuous in $[0, \infty)$.
So the convergence cannot be uniform.

$\square$

(c) Choose a smaller set over which the convergence is uniform
and supply an argument to show that this is indeed the case.

**Solution**: For $g_n(x)$ choose $[0, 1/2]$

$$ 
|g_n(x) - g(x)| = |\frac{x}{1 + x^n} - x| \\
= \left| \frac{-x^{n+1}}{1 + x^n} \right| \\
< |x^{n+1}| \leq \frac{1}{2^{n+1}}
$$

For $h_n(x)$, choose $[1/2, \infty)$, when $n > 2$, $h_n(x) = h(x) = 1$.

$\square$

### 6.2.4.

Review Exercise 5.2.8 which includes the definition for a
uniformly diﬀerentiable function. Use the results discussed in Section 6.2 to
show that if $f$ is uniformly diﬀerentiable, then $f'$ is continuous.

**Proof**: Given $ε > 0$ there exists a $δ > 0$ such that

$$ 
\left| 
\frac{f(x) - f(y)}{x - y}
-
f'(y)
 \right| < \epsilon
$$

$$ 
|f'(x) - f'(y) |
= \left| f'(x) - \frac{f(x) - f(y)}{x - y} +
\frac{f(x) - f(y)}{x - y} - f'(y) \right| \\
\leq
\left| f'(x) - \frac{f(x) - f(y)}{x - y} \right| +
\left| \frac{f(x) - f(y)}{x - y} - f'(y) \right| \\
< 2 \epsilon
$$

So $f'(x)$ is continuous.

$\square$

### 6.2.5.

Using the Cauchy Criterion for convergent sequences of real
numbers (Theorem 2.6.4), supply a proof for Theorem 6.2.5. (First, define a candidate for $f(x)$, and then argue that $f_n → f$ uniformly.)

Proof:

$\Rightarrow$ Since $(f_n(x)) \rightarrow f(x)$ uniformly for $x \in A$.
Then given $\epsilon$, we can find $N$, for all $n > N$ and $x \in A$, $|f_n(x) - f(x)| < \epsilon/2$. So

$$ 
\left| f_n(x) - f_m(x) \right| \\
= \left| f_n(x) - f(x) + f(x) - f_m(x) \right| \\
\leq \left| f_n(x) - f(x) \right| + \left| f(x) - f_m(x) \right| \\
< \epsilon
$$

for all $m, n > N$ and $x \in A$.

$\Leftarrow$ if given any $\epsilon$, we can find $N$, for all $m, n > N$ and $x \in A$, $|f_n(x) - f_m(x)| < \epsilon$, then
$(f_n(x))$ is a Cauchy sequence, so it must converge to some
$c_x$, then define $f(x) = c_x$.

We can find another $N_1$, for all $m, n > N_1$ and $x \in A$, $|f_n(x) - f_m(x)| < \epsilon/2$. We can show that $|f_n(x) - f(x)| < \epsilon$. This is because for any given $x \in A$, since $(f_n(x)) \rightarrow f(x)$, we can find $k$, such that $k > N_1$ and
$|f_k(x) - f(x)| < \epsilon/2$. So

$$ 
\left| f_n(x) - f(x) \right| \\
\leq \left| f_n(x) - f_k(x) \right| + \left| f_k(x) - f(x) \right| \\
< \epsilon
$$

Thus, $f_n → f$ uniformly.

$\square$

### 6.2.6.

Assume $f_n → f$ on a set $A$.

(a) If each $f_n$ is uniformly continuous, then $f$ is uniformly continuous.

**Solution**: Consider the example of 6.2.2 (ii), each $f_n$ is
uniformly continuous on $[0, 1]$, but $f$ is not a continuous
function.

Now assume $(f_n) \rightarrow f$ uniformly. We can find
$n$ such that $|f_n(x) - f(x)| < \epsilon / 3$ for $x \in A$.
For this $f_n$, since it's uniformly continuous, we can find $\delta$, if $|x - y| < \delta$, then $|f_n(x) - f_n(y)| < \epsilon / 3$. Then we have

$$ 
|f(x) - f(y)| \leq \\
|f(x) - f_n(x)| + |f_n(x) - f_n(y)| + |f_n(y) - f(y)| \lt \\
\epsilon / 3 + \epsilon / 3 + \epsilon / 3 = \epsilon
$$

So $f$ is uniformly continuous.

$\square$

(b) If each $f_n$ is bounded, then $f$ is bounded.

**Solution**: Consider $f_n = \frac{1}{1/n + x}$, $A = (0, 1]$. Then
$f(x) = \frac{1}{x}$ on $A = (0, 1]$ which is not bounded.

If $(f_n) \rightarrow f$ uniformly. We can find $n$,
$|f_n(x) - f(x) | < 1$, since $|f_n(x)| \leq M$, then
$|f(x)| \leq M + 1$.

$\square$

(c) If each $f_n$ has a finite number ofdiscontinuities, then $f$ has a finite number of discontinuities.

Proof: If the convergence is uniform, consider the following $f_n$
defined on $[0, 1]$ .

$$ 
f_n(x) =
\begin{cases}
    0 &\text{if } x \not \in \mathbf{Q}  \\
    1/p - 1/n &\text{if } x = q/p, p < n \\
    0 &\text{if } x = q/p, p \geq n      \\
\end{cases} 
$$

So we have

$$ 
f(x) =
\begin{cases}
    0 &\text{if } x \not \in \mathbf{Q}  \\
    1/p &\text{if } x = q/p \\
\end{cases} 
$$

each $f_n(x)$ has a finite number of discontinuities, but $f(x)$ is not continuous at all rational numbers.

Also note $|f_n(x) - f(x)| \leq 1/n$, so the convergence is uniform.

$\square$

(d) If each $f_n$ has fewer than $M$ discontinuities (where $M ∈ N$ is fixed), then
$f$ has fewer than M discontinuities.

**Solution**:

Consider $f_n(x) = x^n$ defined on $[0, 1]$, it has no discontinuities on $[0, 1]$. However, $f(x)$ is discontinueous at
$1$, so it has one discontinuity.

When $f_n(x) \rightarrow f(x)$ uniformly, and assume $f(x)$ has $M$ or more than $M$ discontinuities.

We first need to choose $\epsilon$. Since we can find at least
$M$ discontinuities, let

$$ 
\epsilon = \min
\left\{ 
\epsilon_1, \epsilon_2, \cdots, \epsilon_M
 \right\} 
$$

We then choose a fixed $n$ such that
$|f_n(x) - f(x) | < \epsilon / 3$ for all $x \in A$. 
Assume $c$ is continuous in $f_n(x)$
but is discontinueous in $f(x)$.

Then we can find a $\delta$ such that $x \in U_{\delta}(c)$,
$|f_n(x) - f_n(c) | < \epsilon / 3$.

Finally, since $f(x)$ is not continuous at $c$, then we can find
$x_0 \in U_{\delta}(c)$ and $|f(x) - f(c)| \geq \epsilon$.

But on the other hand,

$$ 
|f(c) - f(x_0)| \\
< |f(c) - f_n(c) | + | f_n(c) - f_n(x_0) | + | f_n(x_0) - f(x_0) | \\
< \epsilon / 3 + \epsilon / 3 + \epsilon / 3 \\
= \epsilon
$$

We have a contradiction. So $f(x)$ has fewer than M discontinuities.

Now looking back to (c), the arguments in (d) does not hold
because, we cannot find such $\epsilon$. 

$\square$

(e) If each $f_n$ has at most a countable number of discontinuities, then $f$ has
at most a countable number of discontinuities.

**Solution**:

Consider the process of constructing the Cantor set, and define

$$ 
f_n(x) =
\begin{cases}
    1 &\text{if } x \in C_n\\
    0 &\text{otherwise }\\
\end{cases} 
$$

Then

$$ 
f(x) =
\begin{cases}
    1 &\text{if } x \in C\\
    0 &\text{otherwise}\\
\end{cases} 
$$

Each $f_n$ has $2^n$ discontinuities, but $f$ is discontinueous
at all $x \in C$ which is an uncountable set.

I cannot figure out the results when the convergence is uniform.

$\square$

### 6.2.7.

Let $f$ be uniformly continuous on all of $\mathbf{R}$, and define a sequence of functions by $f_n(x) = f(x+ 1/n)$. Show that $f_n → f$ uniformly. Give an
example to show that this proposition fails if $f$ is only assumed to be continuous and not uniformly continuous on $\mathbf{R}$.

**Proof**: Since $f$ is uniformly continuous on all of $\mathbf{R}$, then given $\epsilon$, we can find $\delta$, if $|x - y| < \delta$, $|f(x) - f(y)| < \epsilon$.

So take $1/n < \delta$, we have

$$ 
|f_n(x) - f(x)| \\
= |f(x+1/n) - f(x) | < \epsilon
$$

So $f_n → f$ uniformly.

Let $f(x) = x^2$

$$ 
(x + 1/n)^2 - x^2 = \frac{2}{n}x + \frac{1}{n^2}
$$

So $f_n → f$ is not uniformly.

$\square$

### 6.2.8.

Let $(g_n)$ be a sequence of continuous functions that converges
uniformly to $g$ on a compact set $K$. If $g(x) \not = 0$ on $K$, show $(1/g_n)$ converges uniformly on $K$ to $1/g$.

Proof: since $(g_n) \rightarrow g$ uniformly, and $g_n$ is
continuous, then $g$ is a continuous function on a compact
set $K$, that means we can find $c \in K$, such that

$$ 
g(c) = \inf \left\{ |g(x)| : x \in K \right\} > 0
$$

Again, since $(g_n) \rightarrow g$ uniformly, given $\epsilon < g(c)/2$, we can find $N$, such that $n > N$, $|g_n(x) - g(x)| < \epsilon$. That is $|g_n(x)| > g(c)/2$.

So we have

$$ 
|\frac{1}{g_n(x)} - \frac{1}{g(x)}|\\
= |\frac{g(x) - g_n(x)}{g(x)g_n(x)}| < \frac{4}{g^2(c)} | g(x) - g_n(x)|
$$

So $(1/g_n)$ converges uniformly on $K$ to $1/g$.

$\square$

### 6.2.9.

Assume $(f_n)$ and $(g_n)$ are uniformly convergent sequences of
functions.

(a) Show that $(f_n +g_n)$ is a uniformly convergent sequence of functions.

**Proof**:

$$ 
\left| 
f_n(x) + g_n(x) - (f(x) + g(x))
 \right| \\
< |f_n(x) - f(x)| + |g_n(x) - g(x)| \\
< 2 \epsilon
$$

So $(f_n +g_n)$ is a uniformly convergent sequence of functions.

(b) Give an example to show that the product $(f_ng_n)$ may not converge uniformly.

**Solution**: Let $f_n(x) = g_n(x) = x + 1/n$,
$(f_ng_n) \rightarrow x^2$, but is not uniformly.

(c) Prove that if there exists an $M > 0$ such that $|f_n| ≤ M$ and $|g_n| ≤ M$ for
all $n ∈ N$, then $(f_ng_n)$ does converge uniformly.

**Proof**:

$$ 
|f_ng_n - fg|\\
=|f_ng_n - f g_n + f g_n - fg|\\
=|f_n - f| |g_n| + |f| |g_n - g|\\
\leq M(|fn - f| + |g_n - g|)
$$

So $(f_ng_n)$ does converge uniformly.

$\square$

### 6.2.10.

This exercise and the next explore partial converses of the
Continuous Limit Theorem (Theorem 6.2.6). Assume $f_n → f$ pointwise on $[a,b]$
and the limit function $f$ is continuous on $[a,b]$. If each $f_n$ is increasing (but not necessarily continuous), show $f_n → f$ uniformly.

Proof: Assume otherwise. Then we can find a $\epsilon$, for any
$N$, we can find $n > N$ and $x_n \in [a, b]$, such that $|f_n(x_n) - f(x_n)| \geq \epsilon$. Thus we found a sequence $(x_n)$.
Since it's bounded, we can find a subsquence $(x_n) \rightarrow c$.

On the other hand, for $c \in [a, b]$, since $f(x)$ is continuous, we can find
$[c-\delta, c+ \delta]$, such that $|f(x) - f(c)| < \epsilon$ if
$x \in [c-\delta, c+ \delta]$.

We can also find $N$, if $n > N$, $|f_n(c-\delta) - f(c-\delta)| < \epsilon$ and $|f_n(c+\delta) - f(c+\delta)| < \epsilon$.

For any $n > N$ and $x \in [c-\delta, c+ \delta]$, since $f_n$ is
increasing, we have
$|f_n(x) - f(x)| < \max (|f_n(c-\delta) - f(x)|, |f_n(c+\delta) - f(x)|)$.

$$ 
|f_n(c-\delta) - f(x)| \leq |f_n(c-\delta) - f(c-\delta)| + |f(c-\delta) - f(x)| \\
\leq |f_n(c-\delta) - f(c-\delta)| + |f(c-\delta) - f(c)| + |f(c) - f(x)| \\
< 3 \epsilon
$$

For the same reason, we have $|f_n(c+\delta) - f(x)| < 3 \epsilon$.
Thus, $|f_n(x) - f(x)| < 3 \epsilon$.

$\square$

### 6.2.11 (Dini’s Theorem).

Assume $f_n → f$ pointwise on a compact
set $K$ and assume that for each $x ∈ K$ the sequence $f_n(x)$ is increasing.
Follow these steps to show that if $f_n$ and $f$ are continuous on $K$, then the convergence is uniform.

(a) Set $g_n = f− f_n$ and translate the preceding hypothesis into statements about the sequence $(g_n)$.

New statement: $g_n → 0$ pointwise on a compact
set $K$ and assume that for each $x ∈ K$ the sequence $g_n(x)$ is
decreasing. If $g_n$ are continuous on $K$, then the convergence is uniform.

(b) Let $ϵ > 0$ be arbitrary, and define $K_n = \left\{ x ∈ K : g_n(x) ≥ ϵ \right\}$. Argue that
$K_1 ⊇ K_2 ⊇ K_3 ⊇ ···$, and use this observation to finish the argument.

Proof: If $c \in K_n$, $g_n(c) \geq \epsilon$. Since $g_n(c)$ is decreasing, then $g_n(c) \leq g_m(c), \forall m < n$. That means
$K_m \supseteq K_n$.

$K_n = g_n^{-1}([\epsilon, \infty))$, so $K_n$ is the preimage of a closed set of a continuous function. It's easy to
prove $K_n$ is also a close set. Since it's a subset of $K$, it's
also bounded. Then $K_n$ is compact.

If none of $K_n$ is empty, then according to Theorem 3.3.5 (Nested Compact Set Property), the intersection of $K_n$ is not empty.
Assume $c \in \cap K_n$, then $g_n(c) \geq \epsilon$. So $g(c) \geq \epsilon$. We have a contradiction.

This means for some $N$, as long as $n > N$, $K_n = \emptyset$, i.e. $0 < g_n(x) < \epsilon, x \in K$, i.e. the convergence is continuous.

$\square$

### 6.2.12 (Cantor Function).

Review the construction of the Cantor
set $C ⊆ [0,1]$ from Section 3.1. This exercise makes use of results and notation from this discussion.

(a) Define $f_0(x) = x$ for all $x \in [0,1]$. Now, let

$$
f_1(x) =
\begin{cases}
    (3/2)x       &\text{for } 0 \leq x \leq 1/3\\
    1/2          &\text{for } 1/3 < x < 2/3    \\
    (3/2)x - 1/2 &\text{for } 2/3 \leq x \leq 1\\
\end{cases} 
$$

Sketch $f_0$ and $f_1$ over $[0,1]$ and observe that $f_1$ is continuous, increasing,
and constant on the middle third $(1/3,2/3)= [0,1] / C_1$.

(b) Construct $f_2$ by imitating this process of flattening out the middle third
of each nonconstant segment of $f_1$ . Specifically, let

$$
f_2(x) =
\begin{cases}
    (1/2)f_1(3x) &\text{for } 0 \leq x \leq 1/3\\
    f_1(x)       &\text{for } 1/3 < x < 2/3    \\
    (1/2)f_1(3x-2) + 1/2 &\text{for } 2/3 \leq x \leq 1\\
\end{cases} 
$$

If we continue this process,show that the resulting sequence
$(f_n)$ converges uniformly on $[0,1]$.

Proof: For $f_n$, each vertical non-flat jump is $1/2^n$.
Then:
* if $x \not \in C_n$, $f_n(x) = f(x)$.
* if $x \in C_n$, $|f_n(x) - f(x)| \leq 1/2^n$.

So $(f_n)$ converges uniformly on $[0,1]$.

(c) Let $f = \lim f_n$. Prove that $f$ is a continuous, increasing function on $[0,1]$
with $f(0) = 0$ and $f(1) = 1$ that satisfies $f'(x) = 0$ for all $x$ in the open
set $[0,1]/C$. Recall that the “length” of the Cantor set $C$ is $0$. Somehow,
$f$ manages to increase from $0$ to $1$ while remaining constant on a set of “length $1$.”

Proof: Each $f_n$ is continuous and $(f_n) \rightarrow f$ uniformly, according to Theorem 6.2.6 (Continuous Limit Theorem),
$f$ is continuous. $f_n$ is increasing, so is $f$.

$f_n(0) = 0$ and $f_n(1) = 1$, so $f(0) = 0, f(1) = 1$.

If $x \in [0,1]/C$, then $f(x)$ is a constant in $U_{\delta}(x)$,
so $f'(x) = 0$.

$\square$

### 6.2.13.

Let $A= \left\{x_1,x_2,x_3,...\right\}$ be a countable set. For each $n ∈ N$, let $f_n$ be
defined on $A$ and assume there exists an $M > 0$ such that $|f_n(x)| ≤ M$ for all
$n ∈ N$ and $x ∈ A$. Follow these steps to show that there exists a subsequence
of $(f_n)$ that converges pointwise on $A$.

(a) Why does the sequence of real numbers $f_n(x_1)$ necessarily contain a convergent subsequence $(f_{n_k})$? To indicate that the subsequence of functions
$(f_{n_k})$ is generated by considering the values of the functions at $x_1$, we will use the notation $(f_{n_k}) = f_{1,k}$.

Proof: $f_n(x_1)$ is a bounded sequence, from Bolzano–Weierstrass Theorem, it must have a convergent subsequence $(f_{n_k})$.

(b) Now,explain why the sequence $f_{1,k}(x2)$ contains a convergent subsequence.

Proof: Because $f_{1,k}(x2)$ is also bounded. And use Bolzano–Weierstrass Theorem again.

(c) Carefully construct a nested family of subsequences $(f_{m,k})$, and show how this can be used to produce a single subsequence of $(f_n)$ that converges at every point of $A$.

Proof: Note that $f_{p,k} \subseteq f_{q,k}$ if $p > q$, and
$f_{p, k} (x_q)$ converges. So we can pick $f_1$ from $f_{1, k}$,
$f_2$ from $f_{2, k}$ and so on.

For any $x_n \in A$, $f_n(x_n), f_{n+1}(x_n), \dots$ converges.

$\square$

### 6.2.14.

A sequence of functions $(f_n)$ defined on a set $E ⊆ R$ is called
equicontinuous if for every $ϵ > 0$ there exists a $δ > 0$ such that $|f_n(x)−f_n(y)| < ϵ$ for all $n ∈ N$ and $|x−y| < δ$ in $E$.

(a) What is the diﬀerence between saying that a sequence of functions $(f_n)$ is
equicontinuous and just asserting that each $f_n$ in the sequence is individually uniformly continuous?

Solution: the $\delta$ might be depending on $n$ if
each $f_n$ in the sequence is individually uniformly continuous.

(b) Give a qualitative explanation for why the sequence
$g_n(x) = x^n$ is not
equicontinuous on $[0,1]$.
Is each $g_n$ uniformly continuous on $[0,1]$?

Solution: let $\epsilon = 0.1$
* when $n = 1$, $\delta = 0.1$.
* when $n = 2$, $1 - x^2 < 0.1, x < \sqrt[2]{1 - 0.1}$,  $\delta < 0.051$.
* when $n = 4$, $1 - x^4 < 0.1, x < \sqrt[4]{1 - 0.1}$,$\delta < 0.026$.
* when $n = 100$, $1 - x^{100} < 0.1, x < \sqrt[100]{1 - 0.1}$,$\delta < 0.0011$.

But each $g_n$ is indeed uniformly continuous.

### 6.2.15 (Arzela–Ascoli Theorem).

For each $n ∈ \mathbf{N}$, let $f_n$ be a
function defined on $[0,1]$. If $(f_n)$ is bounded on $[0,1]$—that is, there exists an
$M > 0$ such that $|f_n(x)| ≤ M$ for all $n ∈ \mathbf{N}$ and $x ∈ [0,1]$—and if the collection
of functions $(f_n)$ is equicontinuous (Exercise 6.2.14), follow these steps to show
that $(f_n)$ contains a uniformly convergent subsequence.

(a) Use Exercise 6.2.13 to produce a subsequence $(f_{n,k})$ that converges at every
rational point in $[0,1]$. To simplify the notation, set $g_k = f_{n,k}$. It remains
to show that $(g_k)$ converges uniformly on all of $[0,1]$.

Proof: We can just directly apply Exercise 6.2.13. $\square$

(b) Let $ϵ > 0$. By equicontinuity, there exists a $δ > 0$ such that

$$
|g_k(x) - g_k(y)| < \epsilon / 3
$$

for all $|x− y| < δ$ and $k ∈ \mathbf{N}$. Using this $δ$, let $r_1,r_2,...,r_m$ be a
finite collection of rational points with the property that the union of the neighborhoods $V_δ(r_i)$ contains $[0,1]$.
Explain why there must exist an $N ∈ \mathbf{N}$ such that

$$
|g_s(r_i) - g_t(r_i)| < \epsilon / 3
$$

for all $s,t ≥ N$ and $r_i$ in the finite subset of $[0,1]$ just described.

Why does having the set $\left\{r_1,r_2,...,r_m\right\}$ be finite matter?

**Proof**: This is because $g_k(r_i) \rightarrow g(r_i)$, according to
Cauchy criterion, we can find $N_i$ such that $s, t > N_i$

$$
|g_s(r_i) - g_t(r_i)| < \epsilon / 3
$$

Let $N = \max \left\{ r_1,r_2,...,r_m  \right\}$.

If $\left\{r_1,r_2,...,\right\}$ is infinite, $\max \left\{ r_1,r_2,... \right\}$ can be infinite. $\square$

(c) Finish the argument by showing that, for an arbitrary $x ∈ [0,1]$,

$$
|g_s(x) - g_t(x)| < \epsilon
$$

for all $s,t ≥ N$.

**Proof**:

$$ 
|g_s(x) - g_t(x)| =
|g_s(x) - g_s(r_i) + g_s(r_i) - g_t(r_i) + g_t(r_i) - g_t(x)|\\
\leq |g_s(x) - g_s(r_i)|
+ |g_s(r_i) - g_t(r_i)| + |g_t(r_i) - g_t(x)| \\
< 3 \times \epsilon / 3 = \epsilon 
$$

$\square$

## 6.3. Uniform Convergence and Diﬀerentiation

### 6.3.1.

Consider the sequence of functions defined by

$$
g_n(x) = \frac{x^n}{n}
$$

Anwser:

(a) Show $(g_n)$ converges uniformly on $[0,1]$ and find $g = \lim g_n$. Show that $g$ is diﬀerentiable and compute $g'(x)$ for all $x ∈ [0,1]$.

**Solution**: Given $x \in [0, 1]$,

$$ 
\lim_{n \to \infty} \frac{x^n}{n} = 0
$$

So $g(x) = 0$.

$$ 
|g_n(x) - g(x)| =
\left| \frac{x^n}{n} \right| < \left| 1/n \right|
$$

So $(g_n) \rightarrow g$ uniformly.

$g$ is a constant function so it's differentiable and $g'(x) = 0$.

$\square$

(b) Now, show that $(g_n')$ converges on $[0,1]$.
Is the convergence uniform? Set $h = \lim g_n'$ and compare $h$ and $g'$. Are they the same?

**Solution**:

We have

$$ 
g'_n(x) = x^{n-1} \\
h(x) = \begin{cases}
    0 &\text{if } x < 1\\
    1 &\text{if } x = 1\\
\end{cases} 
$$

The converge is not uniform. $h$ and $g'(x)$ are not the same.

$\square$

### 6.3.2.

Consider the sequence of functions

$$ 
h_n(x) = \sqrt[]{x^2 + \frac{1}{n}}
$$

Answer:

(a) Compute the pointwise limit of $(h_n)$ and then prove that the convergence is uniform on $\mathbf{R}$.

**Solution**: Given $x$

$$ 
h(x) = \lim_{n \to \infty} h_n(x) = \sqrt[]{x^2} = |x|
$$

And also

$$ 
|h_n(x) - h(x)| =\\
\left| 
\frac{1/n}{\sqrt[]{x^2 + \frac{1}{n}} + |x|}
\right| <
\left| \frac{1/n}{\sqrt[]{1/n}} \right| =
\left| \frac{1}{\sqrt[]{n}} \right|
$$

So the convergence is uniform.

$\square$

(b) Note that each $h_n$ is diﬀerentiable. Show $g(x) = \lim h'_
n(x)$ exists for all $x$, and explain how we can be certain that the convergence is not uniform on any neighborhood of zero.

**Solution**:

$$ 
h_n'(x) = \left(  \sqrt[]{x^2 + \frac{1}{n}} \right) ' \\
= \frac{1}{2} \frac{1}{\sqrt[]{x^2 + \frac{1}{n}}} 2x \\
= \frac{x}{\sqrt[]{x^2 + \frac{1}{n}}}
$$

Then we have

$$ 
g(x) =
\begin{cases}
    0  &\text{if } x = 0\\
    1  &\text{if } x > 0\\
    -1 &\text{if } x < 0\\
\end{cases} 
$$

If the convergence is uniform on a neighborhood of zero,
then we must have

$$ 
h'(x) = g(x)
$$

But $h(x)$ is not differentiable at $0$. So the convergence
is not uniform.

$\square$

### 6.3.3.

Consider the sequence of functions

$$ 
f_n(x) =
\frac{x}{1 + nx^2}
$$

Answer:

(a) Find the points on $\mathbf{R}$ where each $f_n(x)$ attains its maximum and minimum value. Use this to prove $(f_n)$ converges uniformly on $\mathbf{R}$. What is the limit function?

**Solution**:

Fix $n$, and assume $x > 0$. 

$$ 
f_n(x) =
\frac{1}{\frac{1}{x} + nx} \\
= \frac{1}{(\frac{1}{\sqrt[]{x}} - \sqrt[]{nx})^2 + 2 \sqrt[]{n}} \\
\leq \frac{1}{2 \sqrt[]{n}}
$$

When $x = 1/\sqrt[]{n}$. Since $f_n(x)$ is odd function, it
attains it's minimum value at $x = -1/\sqrt[]{n}$.

The limit function is $f(x) = 0$.

$$ 
|f_n(x) - f(x)| =
\left| \frac{1}{\frac{1}{x} + nx} - 0 \right| \leq \frac{1}{2 \sqrt[]{n}}
$$

So the convergence is uniform.

(b) Let $f = \lim f_n$. Compute $f'_n(x)$ and find all the values of $x$ for which $f'(x) = \lim f'_n(x)$.

**Solution**:

$$
f_n(x) = \frac{x}{1 + nx^2} \\
f_n'(x) = \frac{
(1+nx^2) - x(2nx)
}{
(1 + nx^2)^2
} \\
= \frac{1 - nx^2}{(1 + nx^2)^2} \\
= \frac{1}{1 + nx^2} \frac{1 - nx^2}{1+nx^2}
$$

Let $g(x) = \lim_{n \to \infty} f_n'(x)$,

$$ 
g(x) =
\begin{cases}
    1 &\text{if } x \not = 0 \\
    0 &\text{if } x = 0 \\
\end{cases}
$$

So $f'(x) = g(x)$ when $x \not = 0$.

### 6.3.4.

Let

$$ 
h_n(x) = 
\frac{\sin (nx)}{\sqrt[]{n}}
$$

Show that $h_n → 0$ uniformly on $\mathbf{R}$ but that the sequence of derivatives $(h_n')$ diverges for every
$x ∈ \mathbf{R}$.

**Proof**:

$$ 
|h_n(x) - 0| \leq \frac{1}{\sqrt[]{n}}
$$

So the converge is uniform.

$$ 
h_n'(x) = \frac{n \cos (nx)}{\sqrt[]{n}} = \sqrt[]{n} \cos (nx)
$$

Since $\cos (nx)$ can be either positive or negtive, then
$h_n'(x)$ diverges for every $x \in \mathbf{R}$.

$\square$

### 6.3.5.

Let

$$ 
g_n(x) = \frac{nx + x^2}{2n}
$$

and set $g(x) = \lim g_n(x)$.
Show that $g$ is diﬀerentiable in two ways:

(a) Compute $g(x)$ by algebraically taking the limit as $n → ∞$ and then find $g'(x)$.

**Solution**:

$$ 
g(x) = \lim g_n(x) = \frac{x}{2} \\
g'(x) = \frac{1}{2}
$$

$\square$

(b) Compute $g'_n(x)$ for each $n ∈ N$ and show that the sequence of derivatives $(g'_n)$ converges uniformly on every interval $[−M,M]$.

**Solution**:

$$ 
g_n'(x) = \frac{n + 2x}{2n} = \frac{1}{2} + \frac{x}{n}
$$

We can see $\lim_{n \to \infty} g_n'(x) = \frac{1}{2}$ for $x \in \mathbf{R}$.

$$ 
|g_n'(x) - \frac{1}{2}| = |x/n| \leq M/n.
$$

So it converges uniformly on every interval $[−M,M]$.

$\square$

(c) Repeat parts (a) and (b) for the sequence
$f_n(x) = (nx^2 +1)/(2n+x)$.

**Solution**:

$$ 
f(x) = \lim_{n \to \infty} f_n(x) = \frac{x^2}{2}
$$

Then we have $f'(x) = x$.

Then we compute $f_n'(x)$.

$$ 
f_n(x) = \frac{nx^2 +1}{2n + x} \\
f_n'(x) = \frac{(2n+x)(2nx) - (nx^2+1)}{(2n+x)^2} \\
= \frac{nx^2 + 4n^2x - 1}{(2n+x)^2} \\
= \frac{nx^2 + 4n^2x - 1}{x^2 + 4nx + 4n^2}
$$

Let $h(x) = \lim_{n \to \infty} f_n'(x)$, then $h(x) = x$.

$$ 
|f_n'(x) - h(x)| =\\
\left| \frac{
(nx^2 + 4n^2x - 1) - (x^2 + 4nx + 4n^2)x
}{
x^2 + 4nx + 4n^2
} \right| = \\
\left| \frac{
3nx^2 + x^3 + 1
}{
x^2 + 4nx + 4n^2
} \right| <
\frac{3nM^2 + M^3 + 1}{(2n - M)^2}
$$

So it converges uniformly on every interval $[−M,M]$.

$\square$

### 6.3.7.

Use the Mean Value Theorem to supply a proof for Theorem 6.3.2. To get started, observe that the triangle inequality implies that, for any $x ∈ [a,b]$ and $m,n ∈ \mathbf{N}$,

$$ 
|f_n(x) - f_m(x)| \leq 
|(f_n(x) - f_m(x)) - (f_n(x_0) - f_m(x_0))|
+ |(f_n(x_0) - f_m(x_0))|
$$

**Proof**:

Fix $x$, since $f_n$ are all differentiable, from MVT,
we can find $c \in (x, x_0)$ such that

$$ 
|(f_n(x) - f_m(x)) - (f_n(x_0) - f_m(x_0))| =\\
|(f_n'(c) - f_m'(c))(x - x_0)| \\
\leq |(f_n'(c) - f_m'(c))| (b-a)
$$

Let $g(x) = \lim_{n \to \infty} f_n'(x)$, since we $(f'_n) \rightarrow g$ uniformly, we can find $N_1$, for $n, m > N_1$,
$|f_n'(x) - f_m'(x)| < \frac{\epsilon}{2 (b-a)}$.

We can also find $N_2$, for $n, m > N_2$, $|f_n(x_0) - f_m(x_0)| < \epsilon /2$.

Let $N = \max \left\{ N_1, N_2 \right\}$, then
$|f_n(x) - f_m(x)| < \epsilon$.

$\square$

## 6.4 Series of Functions

### 6.4.1.
Supply the details for the proof of the Weierstrass M-Test
(Corollary 6.4.5):

For each $n ∈ N$, let $f_n$ be a function
defined on a set $A ⊆ R$, and let $M_n > 0$ be a real
number satisfying

$$ 
|f_n(x)| \leq M_n
$$

for all $x \in A$. If $\sum_{n = 1}^{\infty}M_n$ converges,
then $\sum_{n = 1}^{\infty}f_n(x)$ converges uniformly on
$A$.

**Proof**: Given $\epsilon$, since $\sum_{n = 1}^{\infty}M_n$ converges, based on Cauchy Criterion, we can find $N$, if
$n > m > N$, then

$$ 
\left| M_{m+1} + \cdots + M_{n} \right| =\\
M_{m+1} + \cdots + M_{n} < \epsilon
$$

We also have

$$ 
\left| f_{m+1} + \cdots + f_{n} \right| \leq
\left| M_{m+1} \right| + \cdots + \left| M_{n} \right| =\\
M_{m+1} + \cdots + M_{n} < \epsilon
$$

So based on Theorem 6.4.4 (Cauchy Criterion for Uniform Convergence of Series),
$\sum_{n = 1}^{\infty}f_n(x)$ converges uniformly on
$A$.

$\square$

### 6.4.2.

Decide whether each proposition is true or false, providing a
short justification or counterexample as appropriate.

(a) If $\sum_{n = 1}^{\infty} g_n$ converges uniformly,
then $(g_n)$ converges uniformly to zero.

**Proof**: True. Based on Theorem 6.4.4 (Cauchy Criterion for Uniform Convergence of Series), we know
$\left| g_n(x) \right| < \epsilon$.

$\square$

(b) If $0 \leq f_n(x) \leq g_n(x)$ and $\sum_{n = 1}^{\infty}g_n$
converges uniformly, then $\sum_{n = 1}^{\infty}f_n(x)$ converges uniformly.

**Proof**: True, again, use Theorem 6.4.4 (Cauchy Criterion for Uniform Convergence of Series)

$$ 
\left| 
f_{m+1} (x) + \cdots + f_n(x)
 \right| =\\
f_{m+1} (x) + \cdots + f_n(x) \\
\leq 
g_{m+1} (x) + \cdots + g_n(x) \\
= | g_{m+1} (x) + \cdots + g_n(x) | < \epsilon
$$

$\square$

(c) If $\sum_{n = 1}^{\infty} f_n$ converges uniformly on $A$,
then there exist constants $M_n$ such that
$|f_n(x)| \leq M_n$ for all $x \in A$ and $\sum_{n = 1}^{\infty}M_n$ converges.

**Solution**: Let $f_1(x) = x$, for $n > 1, f_n(x) = 0$.
$\sum_{n = 1}^{\infty} f_n$ converges to $x$, but we cannot
find $M_1$ such that $|f_1(x)| \leq M_1$ for all $x \in A$.

This is a boring example, a more interested example is presented
[here](https://solverer.com/library/stephen_abbott/understanding_analysis/exercise_6-4-2).

It constructs $M_n$ like this:

$$ 
M_1 = 1 \\
M_2 = M_3 = 1/2 \\
M_4 = M_5 = M_6 = M_7 = 1/4 \\
\cdots
$$

Then $\sum_{n = 1}^{\infty}M_n$ does not converge.

### 6.4.3.

(a) Show that

$$ 
g(x) = \sum_{n = 0}^{\infty}
\frac{\cos (2^nx)}{2^n}
$$

is continuous on all of $\mathbf{R}$.

**Proof**: Given any $[-M, M]$, apply Theorem 6.4.4 (Cauchy Criterion for Uniform Convergence of Series),

$$ 
\left| g_{m+1} + \cdots + g_{n} \right| \leq
\frac{1}{2^{m+1}} + \cdots + \frac{1}{2^n} \\
< \frac{1}{2^m}
$$

$\square$

(b) The function $g$ was cited in Section 5.4 as an example of a continuous
nowhere diﬀerentiable function. What happens if we try to use Theorem
6.4.3 to explore whether $g$ is diﬀerentiable?

**Solution**: Let

$$ 
h_n(x) = g_n'(x) = - \sin (2^n x).
$$

We can see $\sum_{n = 1}^{\infty} h_n(x)$ is not uniformly converging.

Because $|h_n(1/2^{n+1}\pi)| = \sin (\pi / 2) = 1$.
Then apply Theorem 6.4.4 (Cauchy Criterion for Uniform Convergence of Series), we prove this.

So we cannot use Theorem 6.4.3 to explore whether $g$ is diﬀerentiable.

$\square$

### 6.4.4.

Define

$$ 
g(x) = \sum_{n = 1}^{\infty}
\frac{x^{2n}}{1 + x^{2n}}
$$

Find the values of $x$ where the series converges and show that we get a continuous function on this set.

**Solution**: Let

$$ 
g_n(x) = \frac{x^{2n}}{1 + x^{2n}}
$$

When $|x| \geq 1$, $g_n(x) \geq \frac{1}{2}$, so $g(x)$ does
not converge.

When $|x| < 1$, $g_n(x) < x^{2n}$. Then given $x$,

$$ 
\left| g_{m+1} + \cdots + g_{n} \right| < \\
x^{2(m+1)} + x^{2n} = \\
\frac{x^{2(m+1)} - x^{2(n+1)}}{1 - x^2} < \\
\frac{x^{2(m+1)}}{1 - x^2} \rightarrow 0
$$

For any $|x| < 1$, we can get $|x| < M < 1$. Then we have

$$ 
\frac{x^{2(m+1)}}{1 - x^2} \leq \frac{M^{2(m+1)}}{1-M^2}
$$

So $g(x)$ converges uniformly on $[-M, M]$. $g(x)$ is continuous
at $x$.

$\square$

### 6.4.5.

(a) Prove that

$$ 
h(x) = \sum_{n = 1}^{\infty} \frac{x^n}{n^2}
$$

is continuous on $[-1, 1]$.

**Proof**: $\left| \frac{x^n}{n^2} \right| \leq \frac{1}{n^2}$
and $\sum_{n = 1}^{\infty} \frac{1}{n^2}$ converges.
So based on Corollary 6.4.5 (Weierstrass M-Test), $h(x)$ converges
uniformly. So $h(x)$ is continuous.

$\square$

(b) The series

$$ 
h(x) = \sum_{n = 1}^{\infty} \frac{x^n}{n}
$$

converges for every $x$ in the half-open interval $[−1,1)$ but does not converge when $x = 1$. For a fixed $x_0 ∈ (−1,1)$, explain how we can still use the Weierstrass M-Test to
prove that $f$ is continuous at $x_0$.

**Proof**:

Given $x_0 \in (-1, 1)$, we can find $0 < M < 1$ such that
$x_0 \in [-M, M]$, we prove $h(x)$ converges uniformly on
this interval.

$$ 
|h_n(x)| = |\frac{x^n}{n}| \leq |x|^n \leq M^n
$$

And $\sum_{n = 1}^{\infty} M^n = \frac{M}{1 - M}$.
So $h(x)$ converges uniformly on $[-M, M]$. Then $h(x)$ is
continuous at $x_0$.

### 6.4.6.

Let

$$ 
f(x) = \frac{1}{x} - \frac{1}{x + 1} + \frac{1}{x + 2}
- \frac{1}{x + 3} + \frac{1}{x + 4} - \cdots
$$

Show $f$ is defined for all $x > 0$. Is $f$ continuous on
$(0, +\infty)$? How about diﬀerentiable?

**Proof**:

Let

$$
f_1(x) = \frac{1}{x} - \frac{1}{x + 1} \\
f_2(x) = \frac{1}{x + 2} - \frac{1}{x + 3} \\
f_3(x) = \frac{1}{x + 4} - \frac{1}{x + 5} \\
\cdots \\
f_n(x) = \frac{1}{x + 2n - 2} - \frac{1}{x + 2n - 1} \\
\cdots \\
$$

Given $x$, $\sum_{i = 0}^{n} f_i(x)$ is increasing, and we have

$$ 
\sum_{i = 0}^{n} f_i(x) <
\sum_{i = 0}^{n} \frac{1}{x + i - 1} - \frac{1}{x + i}\\
< \frac{1}{x} - \frac{1}{x + n} < \frac{1}{x}
$$

So it's upper bounded. So $f(x)$ converges.

Then let's check

$$ 
|f_{m+1}(x) + \cdots + f_n(x)| \\
= 
\sum_{i = m+1}^{n}\frac{1}{x + 2i - 2} - \frac{1}{x + 2i - 1} \\
< \sum_{i = m+1}^{n} \frac{1}{x + i - 1} - \frac{1}{x + i} \\
= \frac{1}{x + m} - \frac{1}{x + n} < \frac{1}{m}
$$

That means $\sum_{n = 0}^{\infty} f_n(x)$ converges uniformly
from Theorem 6.4.4. So $f(x)$ is continuous.

Now, let's examine the if it's differentiable.

$$ 
f_n'(x) =
\frac{1}{(x+2n-1)^2} - \frac{1}{(x + 2n - 2)^2}
$$

Then we have

$$ 
|\sum_{i = m+1}^{n} f_i'(x)| \\
= \left| \sum_{i = m+1}^{n} \frac{1}{(x+2i-2)^2} - \frac{1}{(x + 2i - 1)^2} \right| \\
< \left| \sum_{i = m+1}^{n} \frac{1}{(x+2i-2)^2} + \frac{1}{(x + 2i - 1)^2} \right| \\
< \left| \sum_{i = m+1}^{n} \frac{1}{x + 2i - 2} - \frac{1}{x + 2i} \right| \\
= \left| \frac{1}{x + 2m} - \frac{1}{x + 2n} \right| \\
< \frac{1}{2m}
$$

That means $\sum_{n = 0}^{\infty} f_n'(x)$ converges uniformly
from Theorem 6.4.4. So $f(x)$ is differentiable.

$\square$

### 6.4.7.

Let

$$ 
f(x) = \sum_{k = 1}^{\infty } \frac{\sin (kx)}{k^3} 
$$

Anwser:

(a) Show that $f(x)$ is diﬀerentiable and that the
derivative $f'(x)$ is continuous.

**Proof**: We have

$$ 
f_k(x) = \frac{\sin (kx)}{k^3} \\
f_k'(x) = \frac{\cos (kx)}{k^2}
$$

Then we have $|f_k'(x)| \leq \frac{1}{k^2}$, and
$\sum_{k = 1}^{\infty} \frac{1}{k^2}$ converges. So
based on Corollary 6.4.5, $\sum_{k = 1}^{\infty} f_k'(x) \rightarrow g(x)$ converges uniformly. That means $f$ is differentiable, and $f'(x) = g(x)$.
Each $\sum_{k = 1}^{n} f_k'(x)$ is continuous, so $g(x)$ is
also continuous.

$\square$

(b) Can we determine if f is twice-diﬀerentiable?

**Solution**: Consider

$$ 
g_k(x) = -f_k''(x) = \frac{\sin (kx)}{k}
$$

Consider $x = \pi / 2$

$$ 
\sum_{n = 1}^{\infty}
\frac{\sin (n \frac{pi}{2})}{n} \\
= 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \cdots
$$

I cannot evne figure out if
$\sum_{n = 1}^{\infty} g_k(x)$ converges. 

$\square$

### 6.4.8.

Consider the function

$$ 
f(x) = \sum_{k = 1}^{\infty } \frac{\sin (x/k)}{k} 
$$

Where is $f$ defined? Continuous? Diﬀerentiable? Twice-diﬀerentiable?

**Solution**:

We will need this fact: $\sin x \leq x$ for $x \geq 0$.
Let $g(x) = x - \sin x$, $g'(x) = 1 - \cos x \geq 0$.
Therefore, $g(x) - g(0) = g(x) = g'(c)x \geq 0$.
So $x \geq \sin x$.

Let $f_n(x) = \frac{\sin (x/k)}{k}$. Given $x$, consider

$$ 
|f_{m+1}(x) + \cdots + f_n(x)| \leq \\
|f_{m+1}(x)| + \cdots + |f_n(x)| \leq \\
\frac{|x|}{(m+1)^2} + \cdots \frac{|x|}{n^2} < \\
\frac{|x|}{m} - \frac{|x|}{n} < \frac{|x|}{m}
$$

So $\sum_{n = 1}^{\infty}f_n(x)$ converges for all $x \in \mathbf{R}$.
So $f(x)$ is defined for $x \in \mathbf{R}$.

Let

$$ 
g_n(x) = f_n'(x) = \frac{\cos (x/n)}{n^2} \\
$$

Then we have

$$ 
|g_{m+1}(x) + \cdots + g_n(x)| \leq \\
|g_{m+1}(x)| + \cdots + |g_n(x)| \leq \\
\frac{1}{(m+1)^2} + \cdots \frac{1}{n^2} < \\
\frac{1}{m} - \frac{1}{n} < \frac{1}{m}
$$

That means $\sum_{n = 1}^{\infty} g_n(x) \rightarrow g(x)$
uniformly. We also know $\sum_{n = 1}^{\infty}f_n(x)$ converges for all $x \in \mathbf{R}$. Then $f$ is differentiable,
and $f' = g$.

Since it's differentiable, it has to be continuous.

Let

$$ 
h_n(x) = g_n'(x) = -\frac{\sin (x/n)}{n^3}
$$

Since $|h_n(x)| < \frac{1}{n^2}$ and $\sum_{n = 1}^{\infty}\frac{1}{n^2}$ converges, then $\sum_{n = 1}^{\infty}h_n(x)$ converges uniformly. 

Also since $\sum_{n = 1}^{\infty}g_n(0)$ converges, then we know
$g(x)$ is differentiable and $g'(x) = h(x)$. So $f$ is Twice-diﬀerentiable everywhere.

$\square$

### 6.4.9.

Let

$$ 
h(x) = \sum_{n = 1}^{\infty}
\frac{1}{x^2 + n^2}
$$

Answer:

(a) Show that $h$ is a continuous function defined on all of $\mathbf{R}$.

**Proof**: let

$$ 
h_n(x) = \frac{1}{x^2 + n^2}
$$

Then $h_n(x)$ is continuous. Also $h_n(x) \leq \frac{1}{n^2}$,
and we know $\sum_{n = 1}^{\infty} \frac{1}{n^2}$ converges.

So $h$ converges uniformly on $\mathbf{R}$. Based on Theorem 6.4.2, $h$ is continuous on $\mathbf{R}$.

$\square$

(b) Is $h$ diﬀerentiable? If so, is the derivative function $h'$ continuous?

**Proof**: Let

$$ 
g_n(x) = -h_n'(x) = \frac{2x}{(x^2 + n^2)^2}
$$

If we plot the $g_n(x)$, we can see $g_n(x)$ reaches its
maximum value some where. We want to find this maximum value.
So we get derivative of $g_n(x)$.

$$ 
g_n'(x) = \frac{2(x^2 + n^2)^2 - 2x2(x^2+n^2)2x}{(x^2 + n^2)^2}\\
= \frac{(2x^4 + 4x^2n^2+2n^4) - (8x^4+8x^2n^2)}{(x^2 + n^2)^2}\\
= \frac{-6x^4 - 4x^2n^2 + 2n^4}{(x^2 + n^2)^2}
$$

If we set $g_n'(x) = 0$, we have $x^2 = \frac{1}{3}n^2$.
And then

$$ 
\sup g_n(x) = g_n(\sqrt[]{1/3}n) \\
= \frac{\frac{2}{\sqrt[]{3}}n}{\frac{16}{9}n^4} < \frac{1}{n^3}
$$

Then we can see $\sum_{n = 1}^{\infty}g_n'(x)$ converges
uniformly. So $h$ is differentiable and since each $g_n(x)$ is
continuous, $h'$ is continuous.

$\square$

### 6.4.10.

Let $\{r_1,r_2,r_3,...\}$ be an enumeration of the set of
rational numbers. For each $r_n ∈ \mathbf{Q}$, define

$$ 
u_n(x) =
\begin{cases}
    1/2^n &\text{for } x > r_n   \\
    0     &\text{for } x \leq r_n\\
\end{cases}
$$

Now let $h(x) = \sum_{n = 1}^{\infty}u_n(x)$.
Prove that $h$ is a monotone function defined on
all of $\mathbf{R}$ that is continuous at every irrational point.

Proof: First $u_n(x) \leq 1/2^n$, based on Corollary 6.4.5 (Weierstrass M-Test), $\sum_{n = 1}^{\infty}u_n(x)$ converges
to $h(x)$ uniformly. So $h(x)$ is well-defined.

Assume $x < y$, then $u_n(x) < u_n(y)$ for all $n$.
Thus $h(x) \leq h(y)$.

Given $x \not \in \mathbf{Q}$, and $\epsilon > 0$.
We want to find $\delta$, if $|x - y| < \delta$, then
$|h(y) - h(x)| < \epsilon$.

Let $h_n(x) = \sum_{k = 1}^{n}u_n(x)$. We can find $N$, such that $|h_n(x) - h(x)| < \epsilon / 2$
for $n > N$.

Pick any $n > N$. Since $x$ is
an irrational number, we can find $U_{\delta}(x)$, such that
$r_1, r_2, \cdots, r_n \notin U_{\delta}(x)$.

Let $y \in U_{\delta}(x)$, note $u_k(x) = u_k(y)$ for
all $k \leq n$. 

$$ 
h_n(x) - h_n(y) =
\sum_{k = 1}^{n} u_k(x) - u_k(y) = 0
$$

Finally we have

$$ 
|h(x) - h(y)| =
|h(x) - h_n(x)| + |h_n(x) - h_n(y)| + |h_n(y) - h(y)| <
\epsilon / 2 + 0 + \epsilon / 2 = \epsilon
$$

So $h(x)$ is continuous at every irrational point.

$\square$

## 6.5. Power Series

### 6.5.1

Consider the function $g$ defined by the power series

$$ 
g(x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4}
$$

Anwser:

(a) Is $g$ defined on $(−1,1)$? Is it continuous on this set?
Is $g$ defined on $(−1,1]$? Is it continuous on this set?
What happens on $[−1,1]$? Can
the power series for $g(x)$ possibly converge for any
other points $|x| > 1$?

Solution: Given any $|x| < 1$, $g(x)$ converges absolutely.
In addition $g(x)$ converges when $x = 1$.

$$ 
g(x) = 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \cdots
$$

converges. Given any $n, m$,

$$ 
\left| 
x_{m+1} + \cdots + x_n
 \right| < |x_{m+1}| = \frac{1}{m + 1}
$$

On the other hand $g(-1)$ does not converge.

For any $|x| > 1$, $|\frac{x^n}{n}|$ is not bounded.
So $g(x)$ does not converge for $|x| > 1$.

$\square$

(b) For what values of $x$ is $g'(x)$ defined? Find a formula for g'.

**Solution**:

$$ 
\frac{g(1) - g(x)}{1 - x} =\\
1 - \frac{1 + x}{2} + \frac{1 + x + x^2}{3}
- \frac{1 + x + x^2 + x^3}{4} + \cdots
$$

So I think $g(x)$ does not exists.

So $g'(x)$ is defined on $(-1, 1)$.

$\square$

### 6.5.2

Find suitable coeﬃcients $(a_n)$ so that the resulting power
series $\sum_{n = 0}^{\infty}a_n x^n$ has the given
properties, or explain why such a request is impossible

(a) Converges for every value of $x ∈ R$.

**Solution**: Let $a_n = 0$ for all $n$.

$\square$

(b) Diverges for every value of $x ∈ R$.

**Solution**: It converges at 0.

$\square$

(c) Converges absolutely for all $x ∈ [−1,1]$ and diverges oﬀ of this set.

**Solution**: Consider

$$ 
\sum_{n = 1}^{\infty} \frac{x^n}{n^2}
$$

Because $\lim_{n \to \infty} \frac{x^n}{n^2} = \infty$ so it is
not bounded.

$\square$

(d) Converges conditionally at $x =−1$ and converges absolutely
at $x = 1$.

**Proof**: This is not impossible. Because
$|a_n(-1)^n| = |a_n (1)^n|$.

$\square$

(e) Converges conditionally at both $x =−1$ and $x = 1$.

**Solution**: Consider

$$ 
\sum_{n = 0}^{\infty} a_n x^n = 1 - \frac{x^2}{2} + \frac{x^4}{4}
-\frac{x^6}{6} + \cdots 
$$

When $x =−1$ and $x = 1$, the power series becomes

$$ 
1 - \frac{1}{2} + \frac{1}{4} -\frac{1}{6} + \cdots
$$

Using Cauchy Criterion, we can see it converges.
But is is not absolute converging, because

$$ 
1 + \frac{1}{2} + \frac{1}{4} + \frac{1}{6} + \cdots
$$

does not converge.

$\square$

### 6.5.3

Use the Weierstrass M-Test to prove Theorem 6.5.2.

Theorem 6.5.2 states If a power series $\sum_{n = 0}^{\infty}a_nx^n$ converges absolutely at a point
$x_0$, then it converges uniformly on the closed interval $[−c,c]$, where $c = |x_0|$.

**Proof**: Let $M_n = |a_nc^n|$, and $\sum M_n$ converges.

For $x \in [-c, c]$, $|a_nx^n| < |a_nc^n|$. So
it converges uniformly on the closed interval $[−c,c]$.

$\square$

### 6.5.4 (Term-by-term Antidiﬀerentiation).

Assume $f(x) = \sum_{n = 0}^{\infty}a_{n} x^{n}$ converges on
$(-R, R)$.

(a) Show

$$ 
F(x) = \sum_{n = 0}^{\infty}\frac{a_{n}}{n+1} x^{n+1}
$$

is defined on $(-R, R)$ and satisfies $F'(x) = f(x)$.

Proof: Given $x \in (-R, R)$, $\sum_{n = 0}^{\infty}a_{n} x^{n}$
converges absolutely. We can find $n$ such that $n+1 > x$.
So

$$ 
\left| \frac{a_n}{n+1} x^{n+1} \right| =
\left| \frac{x}{n+1} a_{n}x^n\right| <
\left| a_{n} x^n \right|
$$

So $F(x)$ is defined on $(-R, R)$.

Given $c \in (-R, R)$, $f(c)$ converges. From Abel's theorem,
$f(x)$ converges uniformly on $[0,c]$.
From Theorem 6.3.1, $F(x)$ is differentiable on $[0, c]$ and
$F'(x) = f(x)$.

$\square$

(b) Antiderivatives are not unique. If $g$ is an arbitrary
function satisfying $g'(x) = f(x)$ on $(-R, R)$.
Find a power series representation for $g$.

**Proof**: Consider $h(x) = g(x) - F(x)$.

See the exercise 6.5.8, we can prove $g(x) = F(x) + c$.

$\square$

### 6.5.5.

(a) If $s$ satisfies $0 < s < 1$, show $ns^{n−1}$ is bounded for
all $n ≥ 1$.

**Proof**: 

We compare $ns^{n-1}$ and $(n+1)s^n$ and we have $ns^{n-1} > (n+1)s^n$, when $\frac{n}{n+1} > s$. So $ns^{n-1}$ is bounded.

$\square$

(b) Given an arbitrary $x ∈ (−R,R)$, pick $t$ to satisfy $|x| < t < R$. Use this start to construct a proof for Theorem 6.5.6.

**Proof**:

Consider

$$ 
\sum_{n = 1}^{\infty} n a_n x^{n-1} =
\sum_{n = 1}^{\infty}
n \left( \frac{x}{t} \right) ^ {n-1} a_n t^{n-1}
$$

Since $t < R$, then $\sum_{n = 1}^{\infty} a_n t^{n-1}$ converges
absolutely. Let $|n \left( \frac{x}{t} \right) ^ {n-1}| \leq M$,

$$
\left| 
(m+1) \left( \frac{x}{t} \right) ^ {m} a_{m+1} t^{m} + \cdots +
n \left( \frac{x}{t} \right) ^ {n-1} a_n t^{n-1}
\right|
< \\ 
\left| 
(m+1) \left( \frac{x}{t} \right) ^ {m} a_{m+1} t^{m}
\right| + \cdots +
\left| 
n \left( \frac{x}{t} \right) ^ {n-1} a_n t^{n-1}
\right|
< \\
M (|a_{m+1} t^{m}| + \cdots + |a_n t^{n-1}|) < \epsilon
$$

So $\sum_{n = 1}^{\infty}na_n x^{n-1}$ converges at each
$x ∈ (−R,R)$ as well.

$\square$

### 6.5.6.

Previous work on geometric series (Example 2.7.5) justifies
the formula

$$ 
\frac{1}{1 - x} =
1 + x + x^2 + x^3 + x^4 + \cdots , \text{ for all } |x| < 1.
$$

Find the following 2 sums:

(a) $\sum_{n = 1}^{\infty} n/2^n$

**Solution**: we take derivative on the right side

$$ 
1 + 2x + 3x^2 + \cdots =\\
(1 + x + x^2 + x^3 + \cdots ) + \sum_{n = 1}^{\infty} n/2^n
$$

So

$$ 
\sum_{n = 1}^{\infty} n/2^n = \frac{1}{(1-x)^2} - \frac{1}{1-x}\\
=\frac{x}{(1-x)^2} = 2
$$

$\square$

(b) $\sum_{n = 1}^{\infty} n^2/2^n$

**Solution**: Consider

$$ 
\sum_{n = 1}^{\infty} (nx^n)' =
\sum_{n = 1}^{\infty} n^2 x^{n-1} = \\
1 + \sum_{n = 1}^{\infty} (n+1)^2x^n = \\
1 + \sum_{n = 1}^{\infty} n^2 x^n + 2 \sum_{n = 1}^{\infty} nx^n
+ \sum_{n = 1}^{\infty}x^n
$$

So

$$ 
\frac{(1-x)^2 +2 x (1-x)}{(1-x)^4} =\\
\frac{1+x}{(1-x)^3} =\\
1 + S + \frac{2x}{(1-x)^2} + \frac{x}{1 - x}\\
S = 12 - 1 - 4 - 1 = 6
$$

$\square$


### 6.5.7.

Let $\sum_{n = 1}^{\infty} a_nx_n$ be a power series with
$a_n  \not = 0$, and assume

$$ 
L = \lim_{n \to \infty} 
\left| \frac{a_{n+1}}{a_n} \right|
$$

exists.

(a) Show that if $L \not = 0$, then the series converges for
all $x$ in $(-1/L, 1/L)$.
(The advice in Exercise 2.7.9 may be helpful.)

**Proof**: fix $x \in (-1/L, 1/L)$, we can find $\epsilon, r > 0$ such that
$0 \leq |x| < r < \frac{1}{L + \epsilon}$.

So when $n$ is large enough, we have

$$ 
|x| < r  < \frac{1}{L + \epsilon} < \left| \frac{a_n}{a_{n+1}} \right| \leq 1/L \\
|a_{n+1} x^{n+1}| = |\frac{a_{n+1}}{a_{n}} x | | a_n x^n | \\
< r (L +\epsilon) |a_n x^n|
$$

And note $r (L + \epsilon ) < 1$, so the series converges at $x$.

$\square$

(b) Show that if $L = 0$, then the series converges for all
$x ∈ \mathbf{R}$.

**Proof**: Given any $x \in \mathbf{R}$, we can find $|x| < M$.
When $n$ is large enough, $\left| \frac{a_{n+1}}{a_n} \right| < \frac{1}{2M}$. So

$$ 
|a_{n+1} x^{n+1}| = |\frac{a_{n+1}}{a_{n}} x | | a_n x^n |\\
< \frac{1}{2} |a_{n} x|
$$

the series converges for all $x ∈ \mathbf{R}$.

$\square$

(c) Show that (a) and (b) continue to hold if $L$ is replaced by the limit

$$ 
L' = \lim_{n \to \infty} s_n \text{ when }
s_n = \sup \left\{
\left| 
    \frac{a_{k+1}}{a_k}
\right| : k \geq n
\right\}.
$$

**Proof**: if $L' = 0$, then $L = 0$, it becomes (b).
If $L' > 0$, let $L_n = \left| \frac{a_{n+1}}{a_n} \right|$ 

fix $x \in (-1/L', 1/L')$, we can find $N, r > 0$
such that $0 \leq |x| < r < \frac{1}{L'_N} \leq \frac{1}{L}$.

So, for $n > N$,

$$ 
|a_{n+1} x^{n+1}| = |\frac{a_{n+1}}{a_{n}} x | | a_n x^n | \\
< r L_N |a_n x^n|
$$

And note $r L_N < 1$, so the series converges at $x$.

$\square$

### 6.5.8.

(a) Show that power series representations are unique.
If we have

$$ 
\sum_{n = 0}^{\infty} a_n x^n = 
\sum_{n = 0}^{\infty} b_n x^n
$$

for all $x$ in an interval $(−R,R)$, prove that $a_n = b_n$ for
all $n = 0,1,2, \cdots$

**Proof**: Set $x = 0$, then we have $a_0 = b_0$.
Consider

$$ 
f(x) = \sum_{n = 0}^{\infty} (a_n - b_n) x^n
$$

$f(x)$ converges to $0$ in the interval $(−R,R)$.
From Theorem 6.5.7, $f$ is infinitely diﬀerentiable on $(−R,R)$.
Also note $f^{(n)}(x) = 0$.

On the other hand

$$ 
f^{(n)}(0) = a_n - b_n 
$$

So $a_n = b_n$ for all $n = 0,1,2, \cdots$.

(b) Let $f(x) = \sum_{n = 0}^{\infty}a_nx^n$, converge on $(−R,R)$, and assume $f'(x) = f(x)$ for all $x ∈ (−R,R)$ and $f(0) = 1$. Deduce the values of $a_n$.

**Solution**: $a_0 = f(0) = 1$.

$$ 
f'(x) = \sum_{n = 1}^{\infty} na_n x^{n-1}
$$

Based on (a), we have

$$ 
na_n = a_{n-1}
$$

$\square$

### 6.5.9.

Review the definitions and results from Section 2.8 concerning
products of series and Cauchy products in particular.
At the end of Section 2.9, we mentioned the following result:
If $\sum_{}^{}a_n$ and $\sum_{}^{}b_n$ converge conditionally
to $A$ and $B$ respectively, then it is possible for the Cauchy product,

$$ 
\sum_{}^{}d_n \text{ where } d_n = a_0 b_n + a_1 b_{n-1} +
\cdots + a_n b_0,
$$

to diverge. However, if $\sum_{}^{}d_n$ does converge, then
it must converge to $AB$. To prove this, set

$$ 
f(x) = \sum a_n x^n, 
g(x) = \sum b_n x^n,
\text{ and }
h(x) = \sum d_n x^n
$$

Use Abel’s Theorem and the result in Exercise 2.8.7 to establish this result.

**Proof**: Let $x_m = \frac{m}{m+1}$, since $f(1), g(1)$ 
converges.
$\sum a_n x^n_m$ and $\sum b_n x^n_m$ converges absolutely.
From Exercise 2.8.7, we have $f(x_m)g(x_m) = h(x_m)$.

Since $f(1), g(1), h(1)$ converges, these 3 functions are
continuous at $1$.

Then we have

$$ 
AB = f(1)g(1) = \lim_{m \to \infty} f(x_m)g(x_m) =
\lim_{m \to \infty} h(x_m) = h(1) = \sum d_n
$$

$\square$

### 6.5.10
Let $g(x) = \sum_{n = 0}^{\infty}b_nx^n$ converge on $(−R,R)$, and assume $(x_n) \rightarrow 0$ with $x_n \not = 0$. If $g(x_n) = 0$ for all $n ∈ \mathbf{N}$, show that $g(x)$ must be
identically zero on all of $(−R,R)$.

**Proof**: $g(x)$ is continuous, so $g(0)$ = 0, that means $b_0 = 0$.
Compare to exercise 5.3.4 and with Mean value theorem, we know
we can find $(y_n) \rightarrow 0$ such that $g'(y_n) = 0$.
So $g'(0) = 0$, that means $b_1$.

For the same reason, $b_2 = b_3 = \cdots = 0$.

$\square$

### 6.5.11

A series $\sum_{n = 0}^{\infty}a_n$ is said to be Abel-summable
to $L$ if the power series

$$ 
f(x) = \sum_{n = 0}^{\infty}a_n x^n
$$

converges for all $x \in [0, 1)$ and $L = \lim_{x \to 1^{-1}} f(x)$.

(a) Show that any series that converges to a limit $L$ is also Abel-summable to $L$.

**Proof**: $\sum_{n = 0}^{\infty}a_n = L$, then we can directly
apply Abel's theorem, $f(x)$ is continuous at $1$, and
$L = \lim_{x \to 1^{-1}} f(x)$.

$\square$

(b) Show that $\sum_{n = 0}^{\infty} (-1)^n$ is Abel-summable and find the sum.

**Proof**: Let

$$ 
f(x) = \sum_{n = 0}^{\infty} (-x)^n
$$

$f(x)$ converges for all $x \in [0, 1)$ and it converges to

$$ 
\frac{1}{1 + x}
$$

So the Abel sum is $1/2$.

$\square$

## 6.6. Taylor Series

### 6.6.1.

The derivation in Example 6.6.1 shows the Taylor series for
$\arctan(x)$ is valid for all $x ∈ (−1,1)$. Notice, however,
that the series also
converges when $x = 1$. Assuming that $\arctan(x)$ is continuous, explain why the value of the series at $x = 1$ must necessarily
be $\arctan(1)$. What interesting identity do we get in this
case?

Proof: When $x \in (-1, 1)$, $1 - x^2 + x^4 - x^6 + x^8 - \cdots$
converges to $\frac{1}{1 + x^2}$. Then based on Exercise 6.5.4 (Term-by-term Antidiﬀerentiation).

$$
F(x) = x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7} + \cdots
$$

is defined on $(-1, 1)$ and $F'(x) = \frac{1}{1 + x^2}$.

So $F(x) = c + \arctan x$ for some $c$. Then since $F(0) = 0$
we have $c = 0$. So $F(x) = \arctan x, x \in (-1, 1)$.

Since $F(x)$ converges, then based on Abel's theorem,
$F(x)$ is uniformly converging on $[0, 1]$, then $F(x)$ is
continuous at $1$. Since we assume $\arctan (x)$ is also
continuous, we have

$$ 
F(1) = \lim_{x \to 1} F(x) = \lim_{x \to 1} \arctan (x) = 
\arctan (1) = \frac{\pi }{4}
$$

So the interesting part is $F(x)$ is defined at $1$, but
$f(x)$ is not. 

$\square$

### 6.6.2.

Starting from one of the previously generated series in this
section, use manipulations similar to those in Example 6.6.1 to find Taylor
series representations for each of the following functions. For precisely what
values of x is each series representation valid?

(a) $x \cos(x^2)$

**Solution**: We stard from $\sin x$

$$ 
\sin x = x - \frac{x^3}{3!}  + \frac{x^5}{5!} - \frac{x^7}{7!}
$$

First we get derivative on both side

$$ 
\cos x = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!}
+ \cdots
$$

Then we replace $x$ with $x^2$ and multiply by $x$,

$$ 
x \cos x^2 = x - \frac{x^5}{2!} + \frac{x^9}{4!} - \frac{x^{13}}{6!}
$$

The Lagrange Remainder of it is

$$ 
\frac{f^{(N+1)}(c) x^{N+1}}{(N+1)!}
$$

We can compute $f^{(n)}$ 

$$ 
f'(x) = \cos x^2 - 2 x^2 \sin x^2 \\
f''(x) = 2x \cos x^2 - 4x \sin x^2 -4x^3 \cos x^2 \\
f^{(n)} = 2^nx^{n+1} + \delta
$$

The Taylor series converges for $\mathbf{R}$.

(b) $x/(1+4x^2)^2$

**Solution**: We start with

$$ 
\frac{1}{1-x} = 1 + x + x^2 + x^3 + \cdots
$$

Replace $x$ with $-4x^2$

$$ 
\frac{1}{1 + 4x^2} = 
1 - 4x^2 + 4^2x^4 - 4^3x^{6} + \cdots
$$

Then we take derivative on both sides

$$ 
-\frac{8x}{(1 + 4x^2)^2} = 0 - 2 \cdot 4 x + 4 \cdot 4^2x^3
- 6 \cdot 4^3 x^5 + \cdots \\
x/(1+4x^2)^2 = x - 2 \cdot 4 x^3 + 3 \cdot 4^2 x^5 + \cdots
= \sum_{n = 0}^{\infty} (-1)^n (n+1) 2^{2n} x^{2n+1}
$$

If $|x| \geq \frac{1}{2}$,

$$ 
\left| (-1)^n (n+1) 2^{2n} x^{2n+1} \right| \geq 
\left| (n+1)2^{2n} (\frac{1}{2})^{2n+1} \right| = \frac{n+1}{2}
$$

So it's not bounded. So it converges on $(-1/2, 1/2)$.

$\square$

(c) $\log(1+x^2)$

Solution:

First take derivative we get $\frac{2x}{1 + x^2}$.

$$ 
\frac{2x}{1 + x^2} = 2x(1 - x^2 + x^4 - x^6 + \cdots)
= 2x - 2x^3 + 2x^5 - 2x^7 + \cdots = g(x)
$$

Then we take antiderivatives

$$ 
\frac{x^2}{1} - \frac{x^4}{2} + \frac{x^6}{3}
- \frac{x^8}{4} + \cdots
$$

We can see this series converges on $[-1, 1]$, but
we are not sure about if it converges to $f(x)$.

We can use the same argument in the 6.6.1, $g(x)$ is defined
in $(-1, 1)$, so $G(x) = f(x)$ for $x \in (-1, 1)$. Also
$G(1)$ is defined, so $G(x)$ is continuous at $1$, also
$f(x)$ is continuous at $1$, so $G(1) = f(1)$, same thing
for $G(-1) = f(-1)$.

If We want to calculate the Lagrange Remainder, it's complex.

The first derivatives is
$$ 
f'(x) = \frac{2x}{1 + x^2}
$$

The 2nd derivative is
$$
f''(x) = \frac{- 2x^2 + 2}{(1 + x^2)^2}
$$

The 3rd derivative is

$$
f'''(x) = \frac{-4x(1+x^2)^2 - 2(1-x^2)2(1+x^2)2x}{(1 + x^2)^4} \\
= \frac{-4x(1+x^2) - 8x(1-x^2)}{(1 + x^2)^3} \\
= \frac{4x^3 - 12x}{(1 + x^2)^3} \\
$$

$$
f^{(4)}(x) = 
\frac{(12x^2-12)(1+x^2)^3 - (4x^3-12x)3(1+x^2)^22x}{(1 + x^2)^6}\\
\\
\frac{12(x^2-1)(x^2+1)-(4x^3-12x)6x}{(1+x^2)^4} \\
\frac{12(x^2-1)(x^2+1)-(4x^3-12x)6x}{(1+x^2)^4} \\
\frac{-12x^4 + 72x^2 - 12}{(1+x^2)^4} \\
$$

In genenal, assume

$$ 
f^{(n)} = \frac{f_n(x)}{(1+x^2)^n} \text{ and } \\
f_n(x) = a^{(n)}_n x^n + a^{(n)}_{n-2} x^{n-2} +
a^{(n)}_{n-4} x^{n-4} + \cdots \\
$$

We want to compute

$$ 
f_{n+1}(x) = a^{(n+1)}_{n+1} x^{n+1}
+ a^{(n+1)}_{n-1} x^{n-1} +
a^{(n+1)}_{n-3} x^{n-3} + \cdots 
$$

We have

$$ 
f_{n+1}(x) = f'_n(x) (1 + x^2) - 2nxf_n(x)
$$

So we have

$$ 
a^{(n+1)}_{n+1} = n a^{(n)}_n - 2n a^{(n)}_n = - na^{(n)}_n \\
a^{(n+1)}_{n-1} = n a^{(n)}_n + (n-2)a^{(n)}_{n-2} - 2n a^{(n)}_{n-2} = n a^{(n)}_n - (n+2) a^{(n)}_{n-2} \\
a^{(n+1)}_{n-3} = (n-2)a^{(n)}_{n-2} + (n-4)a^{(n)}_{n-4} -
2n a^{(n)}_{n-4} = (n-2)a^{(n)}_{n-2} - (n+4) a^{(n)}_{n-4} 
$$

So we cannot tell from Lagrange Remainder theorem.

$\square$

### 6.6.3.

Derive the formula for the Taylor coeﬃcients given in
Theorem 6.6.2.

Proof: First note, $a_0 = f(0) = 0 = \frac{f^{(1)}}{0!}$.

Since $\sum_{n = 0}^{\infty}a_{n} x^{n}$ converges on $(-R, R)$ to
$f(x)$, then based on Theorem 6.5.7, we have

$$ 
f'(x) = a_1 + 2 a_2 x + 3 a_3 x^2 + \cdots \\
f^{(2)}(x) = 2 a_2  + 6 a_3 x + \cdots \\
f^{(3)}(x) = 6 a_3 + (4!) a_4 x + \cdots \\
$$

Then set $x = 0$, we have

$$ 
a_1 = \frac{f^{(1)}}{1!} (0)\\
a_2 = \frac{f^{(2)}}{2!} (0)\\
a_3 = \frac{f^{(3)}}{3!} (0)\\
\cdots
$$

$\square$

### 6.6.4.

Explain how Lagrange’s Remainder Theorem can be modified
to prove

$$ 
1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} +
\frac{1}{5} - \frac{1}{6} + \cdots = \log_{} (2)
$$

**Proof**: Consider $f(x) = \log_{} (x)$.

$$ 
S_N(x) = f(1) + \frac{f'(1)}{1} (x - 1) + \frac{f''(1)}{2!}(x-1)^2
+ \cdots + \frac{f^{(N)}(x)}{N!} (x - 1)^N
$$

Let $E_N(x) = f(x) - S_N(x)$.

$$ 
E_N(1) = f(1) - S_N(1) = 0 \\
E_N^{(1)}(1) = f'(1) - f'(1) = 0 \\
\cdots \\
E_N^{(N)}(1) = f^{(N)}(1) - f^{(N)}(1) = 0 \\
$$

Then we have

$$ 
\frac{E_N(x) - E_N(1)}{(x - 1)^{N+1} - 0} =\\
\frac{E_N(x) - E_N(1)}{(x - 1)^{N+1} - 0} =\\
\frac{f^{(N+1)}(c)}{(N+1)!}(x-1)^{N+1} =\\
\pm \frac{(x-1)^{N+1}}{c^{N+1}(N+1)!}
$$

Plug $x = 2$, then note $c \in (1, 2)$ 

$$ 
E_N(2) = \frac{1}{c^{N+1} (N+1)!} \rightarrow 0
$$

$\square$

### 6.6.5.

(a) Generate the Taylor coeﬃcients for the exponential
function $f(x) = e^x$, and then prove that the corresponding Taylor series converges uniformly to $e^x$ on any interval of the form $[−R,R]$.

**Proof**:

$$ 
f^{(1)}(0) = e^0 = 1 \\
f^{(2)}(0) = e^0 = 1 \\
\cdots \\
f^{(N+1)}(0) = e^0 = 1 \\
$$

So we have

$$ 
f(x) = 1 + \frac{1}{1} x + \frac{1}{2!} x^2 + \frac{1}{3!} x^3 +
\cdots
$$

Based on theorem 6.6.3 (Lagrange’s Remainder Theorem),

$$ 
E_N(x) = \frac{f^{(N+1)}(c) x^{N+1}}{(N+1)!} 
$$

So 

$$
\left| \frac{f^{(N+1)}(c) x^{N+1}}{(N+1)!} \right| \leq
\frac{e^R R^{N+1}}{(N+1)!} \rightarrow 0
$$

So $E_N(R) \rightarrow 0$, then based on Abel's theorem,
Taylor series converges uniformly to $e^x$ on any interval of the form $[−R,R]$.

$\square$

(b) Verify the formula $f'(x) = e^x$.

**Proof**: If we take derivative item by item, we get

$$ 
f'(x) = 1 + x + \frac{1}{2!}x^2 + \frac{1}{3!}x^3 + \cdots
= f(x) = e^x
$$

$\square$

(c) Use a substitution to generate the series for $e^{−x}$, and then informally calculate $e^x \cdot e^{−x}$ by multiplying 
together the two series and collecting common powers of $x$.

Proof:

$$ 
e^{-x} = 1 - x + \frac{1}{2!}x^2 - \frac{1}{3!}x^3 + \cdots
$$

So the coeﬃcient for $x^4$ is

$$
\frac{1}{4!} - \frac{1}{3!} + \frac{1}{(2!)^2} - \frac{1}{3!}
+\frac{1}{4!} = \frac{1 - 4 + 6 - 4 + 1}{24} = 0
$$

So the coeﬃcient for $x^5$ is

$$ 
\frac{1}{5!} - \frac{1}{4!1!} + \frac{1}{3!2!} - \frac{1}{2!3!}
+ \frac{1}{1!4!} - \frac{1}{0!5!}
$$

So the coeﬃcient for $x^6$ is

$$ 
\frac{1}{6!0!} - \frac{1}{5!1!} + \frac{1}{4!2!} - \frac{1}{3!3!}
+\frac{1}{2!4!} - \frac{1}{1!5!} + \frac{1}{0!6!}
$$

To summarize, the coefficient is the following when $n$ is even

$$ 
a_n = \frac{1}{n!} ( C_n^0-C_n^{1} + ... - C_n^{n-1} + C_n^n)
$$

So positive item in the above equation is to choose even number
of elements from $n$ elements. Consider when $n$ is odd,
then the number of ways to choose even number of elements is
the same as the ways to choose odd number of elements.

Now when $n$ is even, if want to choose even number of elements,
there are 2 ways:
* Choose odd number of elements then plus the new element.
* Choose even number of elements from previous $n-1$ elements.

So the above equation is still $0$.

$\square$

### 6.6.6.

Review the proof that $g'(0) = 0$ for the function

$$ 
g(x) =
\begin{cases}
    e^{-1/x^2} &\text{for } x \not = 0 \\
    0 &\text{for } x = 0\\
\end{cases} 
$$

introduced at the end of this section.

(a) Compute $g'(x)$ for $x \not = 0$. Then use the definition of the derivative to find $g''(0)$.

**Solution**: 

$$ 
g'(x) = e^{-1/x^2} \cdot \frac{2}{x^3}
$$

Then we have

$$ 
g''(0) = \lim_{x \to 0} \frac{e^{-1/x^2} \cdot \frac{2}{x^3} - 0}
{x - 0} =\\
\lim_{x \to 0} e^{-1/x^2} \cdot \frac{2}{x^4} = \\
\lim_{x \to 0}
\frac{
1/x^4
}{
e^{1/x^2}
} =
\lim_{x \to 0} \frac{
-4/x^5
}{
e^{1/x^2} \cdot \frac{-2}{x^3}
} = \\
\lim_{x \to 0} \frac{
2/x^2
}{e^{1/x^2}} = \\
\lim_{x \to 0} \frac{
-4/x^3
}{e^{1/x^2} \cdot \frac{-2}{x^3} } = \\
\lim_{x \to 0} \frac{
2
}{e^{1/x^2}} = 0
$$

$\square$

(b) Compute $g''(x)$ and $g'''(x)$ for $x \not = 0$. Use these observations and invent whatever notation is needed to give a general description for the nth derivative $g^{(n)}(x)$
at points diﬀerent from zero.

$$ 
g'(x) = e^{-1/x^2} \cdot \frac{2}{x^3} \\
g''(x) = e^{-1/x^2} \cdot \frac{2}{x^6} - e^{-1/x^2} \frac{6}{x^4} \\
g'''(x) = e^{-1/x^2} \frac{4}{x^9} - e^{-1/x^2} \frac{12}{x^7} -
e^{-1/x^2} \frac{12}{x^7} + e^{-1/x^2} \frac{24}{x^5} =\\
e^{-1/x^2} \frac{4}{x^9} - e^{-1/x^2} \frac{24}{x^7} +
e^{-1/x^2} \frac{24}{x^5}
$$

The general description is 

$$ 
g^{(n)}(x) = e^{-1/x^2}
(
\frac{a_n}{x^{3n}} + \frac{a_{n-1}}{x^{3n-2}} + \cdots 
+ \frac{a_1}{x^{n+2}}
)
$$

$\square$

(c) Construct a general argument for why $g^{(n)}(0) = 0$ for
all $n \in \mathbf{N}$.

**Solution**: In general

$$ 
\lim_{x \to 0} \frac{1/x^n}{e^{1/x^2}} = \\
\lim_{x \to 0} \frac{n/x^{n-2}}{2e^{1/x^2}} = \\
\lim_{x \to 0} \frac{n(n-2)/x^{n-4}}{2^2e^{1/x^2}} = \\
\cdots \\
= 0
$$

$\square$

### 6.6.7.

Find an example of each of the following or explain why no
such function exists.

(a) An infinitely diﬀerentiable function $g(x)$ on all of $\mathbf{R}$ with a Taylor series that converges to
$g(x)$ only for $x ∈ (−1,1)$.

**Solution**: Consider

$$ 
\frac{1}{1 + x^2} = 1 - x^2 + x^4 - x^6 + \cdots
$$

It only converges on $(-1, 1)$.

(b) An infinitely diﬀerentiable function $h(x)$ with the same Taylor series as
$\sin(x)$ but such that $h(x) \not = \sin(x)$ for all $x \not = 0$.

**Solution**: Yes, it's possible. Consider the $g(x)$ defined
in exercise 6.6.6. And let $h(x) = \sin (x) + g(x)$.
Since $h^{(n)}(0) = \sin ^{(n)} (0) + g^{(n)} (0) = \sin ^{(n)} (0)$, but $g(x) \not = 0$ for $x \not = 0$.
So $h(x) \not = \sin (x), x \not = 0$.

(c) An infinitely diﬀerentiable function $f(x)$ on all of $\mathbf{R}$ with a Taylor series
that converges to $f(x)$ if and only if $x ≤ 0$.

**Solution**: consider

$$ 
f(x) = \begin{cases}
    g(x) &\text{if } x > 0 \\
    0    &\text{if } x \leq 0 \\
\end{cases} 
$$

Its Taylor series converges to $0$, which equals to $f(x)$ for
$x \leq 0$. But when $f(x) \not = 0$ when $x > 0$.

$\square$

### 6.6.8.

Here is a weaker form of Lagrange’s Remainder Theorem whose
proof is arguably more illuminating than the one for the stronger result.

(a) First establish a lemma: If $g$ and $h$ are diﬀerentiable on $[0,x]$ with $g(0) = h(0)$ and $g'(h) \leq h'(x)$ for all
$g(t) ≤ h(t)$ for all $t \in [0, x]$.

**Proof**:

Let

$$ 
f(x) = h(x) - g(x)
$$

Then $f(x) - f(0) = f'(c)x$, since $f'(c) = h'(c) - g'(c) \geq 0$,
$f(x) = f(0) + f'(c)x = f'(c) x \geq 0$

$\square$

(b) Let $f$, $S_N$, and $E_N$ be as Theorem 6.6.3,
and take 0 < x < R. If $\left| f^{(N+1)} (t) \right| \leq M$
for all $t \in [0, x]$, show

$$ 
|E_N(x)| \leq \frac{M x^{N+1}}{(N+1)!}
$$

**Proof**: based on (a), $E_N^{(N)}(0) = M 0 = 0$, and
$E_N^{(N+1)} = f^{(N+1)}(x)$ and 
$-M \leq f^{(N+1)}(x) \leq M$, so

$$
-Mx \leq E_N^{(N)}(x) \leq Mx \\
\text{i.e. }, |E_N^{(N)}(x)| \leq Mx
$$

Furthermore $E_N^{(N-1)}(0) = \frac{1}{2} M 0^2 = 0$,
So

$$ 
-\frac{1}{2}M x^2 \leq E_N^{(N-1)}(x) \leq \frac{1}{2} M x^2
$$

We continue this process for $N-2, N-3, \cdots, 0$, we have

$$
-\frac{1}{(N+1)!}M x^{N+1} \leq
E_N(x) \leq
\frac{1}{(N+1)!}M x^{N+1}
$$

So we proved (b).

$\square$

### 6.6.9 (Cauchy’s Remainder Theorem).

Let $f$ be diﬀerentiable
$N+1$ times on $(−R,R)$. For each $a ∈ (−R,R)$, let $S_N(x,a)$ be the partial sum
of the Taylor series for $f$ centered at $a$; in other words, define

$$ 
S_N(x, a) = \sum_{n = 0}^{N}c_{n} (x - a)^{n} \text{ where }
c_n = \frac{f^{(n)}(a)}{n!}
$$

Let $E_N(x, a) = f(x) - S_N(x, a)$. Now fix $x \not = 0$ in
$(-R, R)$ and consider $E_N(x, a)$ as a function of $a$.

(a) Find $E_N(x, x)$.

**Solution**: $E_N(x, x) = f(x) - S_N(x, x) = f(x) - f(x) = 0$.

$\square$

(b) Explain why $E_N(x,a)$ is differentiable with respect to
$a$, and show

$$ 
E_N(x, a)' = \frac{-f^{(N+1)}(a)}{N!}(x - a)^N
$$

**Proof**:

$$
E_N'(x, a) = f'(x) - S_N'(x, a) = - S_N'(x, a) \\
S_N'(x, a) = c_0' + (c_1'(c-a) - c_1) + (c_2'(c-a)^2 - 2 c_2 (c -a)) + \cdots \\
= f'(a) + (f''(a)(x-a)-f'(a)) +
(\frac{1}{2!}f'''(a)(x-a) -f''(a)(x-a)) + \cdots +
(\frac{1}{N!}f^{(N+1)}(x-a)^N - \frac{1}{(N-1)!}f^{(N)}(x-a)^{N-1}) \\
= \frac{1}{N!}f^{(N+1)}(x-a)^N \\
$$

So

$$ 
S_N'(x, a) = \frac{-f^{(N+1)}(a)}{N!}(x - a)^N
$$

$\square$

(c) Show

$$ 
E_N(x) = E_N(x, 0) = \frac{f^{(N+1)}(c)}{N!}(x - c)^N x
$$

**Proof**:

First

$$ 
E_N(x, 0) = f(x) - S_N(x, 0) =
\sum_{n = 0}^{N}c_{n} (x-0)^{n} = E_N(x)
$$

$$ 
\frac{
    E_N(x, x) - E(x, 0)
}{x - 0}
= E'(x, c) = \frac{-f^{(N+1)}(c)}{N!}(x - c)^N
$$

So we have

$$ 
E_N(x, 0) = \frac{f^{(N+1)}(c)}{N!}(x - c)^N x
$$

$\square$

### 6.6.10.

Consider $f(x) = 1/ \sqrt[]{1−x}$.

Generate the Taylor series for $f$ centered at zero, and use Lagrange’s
Remainder Theorem to show the series converges to $f$ on $[0,1/2]$. (The
case $x < 1/2$ is more straightforward while $x = 1/2$ requires some extra
care.) What happens when we attempt this with $x > 1/2$?

$$ 
f'(0) = \frac{1}{2} (1 - x)^{-3/2} = \frac{1}{2} \\
f''(0) = \frac{3}{4} (1-x)^{-5/2} = \frac{3}{4} \\
\cdots \\
f^{(n)}(0) = \frac{1 \cdot 3 \cdots(2n-1)}{2^n}
(1 - x)^{-\frac{2n+1}{2}}
$$

Then the Lagrange's Remainder is

$$ 
\frac{f^{(N+1)}(c)}{(N+1)!}x^{N+1} =
\frac{1 \cdot 3 \cdots (2N+1) }{2^{N+1} (N+1)!}
\frac{x^{N+1}}{(1-c)^{N+1} \sqrt[]{1-c}}
$$

Because $c < x \leq 1/2$, then $1 - c > 1/2 \geq x$, so

$$ 
\frac{x}{1 - c} < 1
$$

Also since $c < 1/2$, then  

$$
\frac{1}{\sqrt[]{1-c}} < \frac{\sqrt[]{2}}{2}
$$

Let

$$ 
c_n =
\frac{1 \cdot 3 \cdot 5 \cdots (2n-1)}{
2 \cdot 4 \cdot 6 \cdots 2n
}
$$

From Exercise 8.3.7, $\lim_{n \to \infty} c_n = 0$.

Then the Lagrange's Remainder converges to 0.

When $x > 1/2$, we cannot establish $\frac{x}{1 - c} < 1$.
So Lagrange's Remainder theorem is not applicable in this case.

$\square$

(b) Use Cauchy’s Remainder Theorem proved in Exercise 6.6.9 to show the series representation for $f$ holds on $[0,1)$.

**Proof**: the Cauchy’s Remainder

$$ 
E_N(x) = \frac{f^{(N+1)}(c)}{N!}(x - c)^N x \\
= \frac{1 \cdot 3 \cdots (2N+1) }{2^{N+1} N!}
\frac{(x-c)^{N}x}{(1-c)^{N+1} \sqrt[]{1-c}}
$$

Given any $0 < c < x < 1$, so $x-c < 1-c$.
Furthermore since $xc < c$, so $x - xc > x - c$, so  

$$ 
\frac{x-c}{1-c} < x
$$

Also

$$ 
\frac{1}{(1-c)^{3/2}} < \frac{1}{(1-x)^{3/2}}
$$

So

$$ 
E_N(x) =
\frac{1 \cdot 3 \cdot 5 \cdots (2N+1)}{
2 \cdot 4 \cdot 6 \cdots 2N
} \cdot
\frac{(x-c)^N}{(1-c)^N}
\cdot
\frac{1}{(1-c)^{3/2}} \\
< 
\frac{1 \cdot 3 \cdot 5 \cdots (2N-1)}{
2 \cdot 4 \cdot 6 \cdots 2N
} \cdot
(2N+1) \cdot x^N
\cdot \frac{1}{(1-x)^{3/2}}
$$

Since $x < 1$ then $\lim_{n \to \infty} (2n+1) x^n = 0$,
we have

$$ 
\lim_{N \to \infty} E_N(x) = 0
$$

$\square$

## 6.7 The Weierstrass Approximation Theorem

### 6.7.1

Assuming WAT, show that if $f$ is continuous on $[a,b]$, then
there exists a sequence $(p_n)$ of polynomials such that $p_n → f$ uniformly on $[a,b]$.

**Proof**:

Given $\epsilon = \frac{1}{n}$, we can find polynomial $p_n(x)$ such that

$$ 
\left| p_n(x) - f(x) \right| < \frac{1}{n} = \epsilon
$$

So we found a sequence $(p_n)$ of polynomials such that $p_n → f$ uniformly on $[a,b]$.

$\square$

### Definition 6.7.2.

A continuous function $\phi : [a,b] → \mathbf{R}$ is polygonal if there is a partition

$$ 
a = x_0 < x_1 < x_2 < \cdots < x_{n} = b
$$

of $[a,b]$ such that $\phi$ is linear on each subinterval $[x_{i−1}, x_i]$, where $i = 1,...n$.

### Theorem 6.7.3.

Let $f : [a,b] → R$ be continuous. Given $ϵ > 0$, there exists a
polygonal function $\phi$  satisfying

$$ 
\left| f(x) - \phi (x) \right| < \epsilon 
$$

for all $x \in [a, b]$.

### Exercise 6.7.2.

Prove Theorem 6.7.3.

Proof: Since $f$ is continuous on $[a, b]$, then $f$ is uniformly
continuous on $[a,b]$, so we can find $\delta$, as long as
$\left| x - y \right| < \delta$, $\left| f(x) - f(y) \right| < \epsilon/2$.

Then we can find 

$$ 
a = x_0 < x_1 < x_2 < \cdots < x_{n} = b
$$

such that $x_{i+1} - x_i < \delta$

Assume $c \in [x_{i}, x_{i+1}]$

$$ 
\left| f(c) - \phi (c) \right| \leq 
|f(c) - f(x_i)| + |f(x_i) - \phi (x_i)| + |\phi (x_i) - \phi (c)|
\leq 
|f(c) - f(x_i)| + |f(x_i) - \phi (x_i)| + |\phi (x_i) - \phi (x_{i+1})| \\
|f(c) - f(x_i)| + 0 + |f(x_i) - f(x_{i+1})|
< \epsilon /2 + 0 + \epsilon / 2 = \epsilon 
$$

$\square$

### 6.7.3.

(a) Find the second degree polynomial $p(x) = q_0+q_1x+q_2x^2$
that interpolates the three points $(−1,1),(0,0)$, and $(1,1)$ on the graph of
$g(x) = |x|$. Sketch $g(x)$ and $p(x)$ over $[−1,1]$ on the same set of axes.

**Solution**:

$$ 
p(-1) = q_0 - q_1 + q_2 = 1 \\
p(0)  = q_0 = 0 \\
p(+1) = q_0 + q_1 + q_2 = 1 \\
$$

So $p(x) = x^2$.

(b) Find the fourth degree polynomial that interpolates
$g(x) = |x|$ at the points
$x =−1,−1/2,0,1/2$, and $1$. Add a sketch of this polynomial to
the graph from (a).

**Solution**

Let $p(x) = p_0 + p_1 x + p_2 x^2 + p_3 x^3 + p_4 x^4$,
then $p(0) = 0$, so $p_0 = 0$.

$$
-p_1 + p_2 - p_3 + p_4 = p_1 + p_2 + p_3 + p_4 = 1 \\
-8 p_1 + 4 p_2 - 2 p_3 + p_4 = 8 p_1 + 4 p_2 + 2 p_3 + p_4 = 8 \\
p_2 + p_4 = 1\\
p_1 + p_3 = 0\\
16 p_1 + 4 p_3 = 0\\
8 p_2 + 2 p_4 = 16 \\
p_1 = p3 = 0 \\
p_2 = 7 / 3 \\
p_4 = -4 / 3
$$

$\square$

### 6.7.4.

Show that $f(x) = \sqrt[]{1−x}$ has Taylor series coeﬃcients an
where $a_0 = 1$ and

$$ 
a_n =
\frac{-1 \cdot 3 \cdot 5 \cdots (2n-3) }
{2 \cdot 4 \cdot 6 \cdots 2n}
$$

**Solution**:

$$ 
f'(x) = - \frac{1}{2} (1-x)^{-\frac{1}{2}} \\
f''(x) = - \frac{1 }{2^2} (1-x)^{-\frac{3}{2}} \\
f'''(x) = - \frac{1 \cdot 3 }{2^3}
(1-x)^{-\frac{5}{2}} \\
$$

So

$$ 
a_n = \frac{f^{(n)}(0)}{n!} =
-\frac{-1 \cdot 3 \cdot 5 \cdots (2n-3)}{2^n n!} (1-0)^{\frac{-(2n-1)}{2}} \\
\frac{-1 \cdot 3 \cdot 5 \cdots (2n-3) }
{2 \cdot 4 \cdot 6 \cdots 2n}
$$

$\square$

### 6.7.5.
(a) Follow the advice in Exercise 6.6.9 to prove the Cauchy
form of the remainder:

$$ 
E_N(x) = \frac{f^{(N+1)}(c)}{N!}(x - c)^N x
$$

for some $c$ between $0$ and $x$.

**Proof**: See the 6.6.9.

(b) Use this result to prove equation (1) is valid for all $x ∈ (−1,1)$.

**Proof**: 

$$ 
E_N(x) = -\frac{-1 \cdot 3 \cdot 5 \cdots (2N-1)}{2^{N+1}N!}
(1 - c)^{\frac{-(2N+1)}{2}} (x-c)^N x \\
= - \frac{1}{2} \cdot \frac{1 \cdot 3 \cdot 5 \cdots (2N-1)}
{2 \cdot 4 \cdot 6 \cdots (2N)}
\left( \frac{x - c}{1 - c} \right)^N \frac{x}{\sqrt{1 - c}}
$$

Note that $x < 1$ and $x - c < 1 - c$, so $x - c < x - xc$.
that means $\frac{x - c}{1-c} < x$, also

$$ 
\frac{x}{\sqrt[]{1-c}} < \frac{x}{\sqrt[]{1-x}}
$$

So $E_N(x) < \frac{1}{2}x^N \frac{x}{\sqrt[]{1-x}} \rightarrow 0$.

If $-1 < x < c < 0$, then

$$ 
cx > c \\
x - cx < x-c \\
0 > \frac{x-c}{1-c} > x > -1 \\
\left| \frac{x-c}{1-c} \right|  < \left| x \right|
$$

Also 

$$ 
\left| \frac{x}{\sqrt[]{1-c}} \right|  < \left| x \right| 
$$

So

$$ 
\left| E_N(x) \right|  < \frac{1}{2} |x|^N \rightarrow 0
$$

$\square$

### 6.7.6.

(a) Let

$$ 
c_n =
\frac{1 \cdot 3 \cdot 5 \cdots (2n-1)}
{2 \cdot 4 \cdot 6 \cdots 2n}
$$

for $n \geq 1$. Show $c_n < \frac{2}{\sqrt[]{2n+1}}$.

**Proof**: We use induction $c_1 = \frac{1}{2} < \frac{2}{\sqrt[]{3}}$. And assume it holds for $k = n$. When $k = n + 1$ 

$$ 
c_{n+1} =
\frac{1 \cdot 3 \cdot 5 \cdots (2n+1)}
{2 \cdot 4 \cdot 6 \cdots 2(n+1)} \\
< \frac{2}{\sqrt[]{2n+1}} \frac{2n+1}{2(n+1)} \\
= 2 \frac{\sqrt[]{2n + 1}}{2 (n + 1)} \\
$$

Because

$$ 
(2n + 1) (2n + 3) = 4n^2 + 8n + 3 < 4n^2 + 8n + 4 = (2n + 2)^2
$$

So

$$ 
2 \frac{\sqrt[]{2n + 1}}{2 (n + 1)} <\\
2 \frac{\sqrt[]{2n + 1}}{\sqrt[]{2n + 1} \sqrt[]{2n + 3}} \\
= \frac{2}{\sqrt[]{2n + 3}}
$$

So it holds for $k = n + 1$.

$\square$

(b) Use (a) to show that $\sum_{n = 0}^{\infty}a_{n}$
converges (absolutely, in fact) where an is
the sequence of Taylor coeﬃcients generated in Exercise 6.7.4.

**Proof**:

$$ 
\sum_{n = 0}^{\infty}
\left| 
\frac{-1 \cdot 3 \cdot 5 \cdots (2n-3) }
{2 \cdot 4 \cdot 6 \cdots 2n}
 \right| =\\
\sum_{n = 0}^{\infty}
\frac{1 \cdot 3 \cdot 5 \cdots (2n-1)}
{2 \cdot 4 \cdot 6 \cdots 2n}
\cdot \frac{1}{2n-1} \\
< \sum_{n = 0}^{\infty}
\frac{2}{\sqrt[]{2n+1}} \cdot \frac{1}{2n-1} \\
< \sum_{n = 0}^{\infty}
\frac{2}{(2n-1)^{\frac{3}{2}}} \\
\sum_{n = 0}^{\infty}
\frac{1}{(2n-2)^{\frac{3}{2}}}
+ \frac{1}{(2n-1)^{\frac{3}{2}}}
$$

So it converges.

(c) Carefully explain how this verifies that equation (1) holds for all $x ∈[-1, 1]$.

**Proof**: $f(x) = \sum_{n = 0}^{\infty}a_{n} x^{n}$ converges
at $[-1, 1]$, then according to Abel's Theorem, $f(x)$ is continuous on $[-1, 1]$.

Let $g(x) = \sqrt[]{1-x}$, it's also continuous on
$[-1, 1]$. Furthermore, $g(x) = f(x)$ on $(-1, 1)$.
So

$$ 
f(1) = \lim_{x \to 1} f(x) = \lim_{x \to 1} g(x) = g(1)
$$

For the same reason, $f(-1) = g(-1)$.

$\square$

### 6.7.7.

(a) Use the fact that $|a| = \sqrt[]{a^2}$ to prove that, given
$\epsilon > 0$ there exists a polynomial $q(x)$ satisfying

$$ 
\left| |x| - q(x) \right| < \epsilon
$$

for all $x \in [-1, 1]$.

**Proof**:

Let $f_m(x) = \sum_{n = 0}^{m}a_{n} x^{n}$ be the partial
sum of the Taylor series of $g(x) = \sqrt[]{1-x}$.

We have proved $f_m(x) \rightarrow g(x)$ on $[-1. 1]$.
From Abel's theorem, this converge is uniform.

So give $\epsilon$, we can find $f_N(x)$ such that

$$ 
\left| 
f_N(x) - \sqrt[]{1-x}
 \right| < \epsilon
$$

for all $x \in [-1, 1]$.

Now replace the $x$ with $1-t^2$.
Note if $t \in [-1, 1]$, then $1 - t^2 \in [0, 1]$.
Then we get

$$ 
\left| 
f_N(1-t^2) - \sqrt[]{t^2} < \epsilon
 \right| 
$$

for all $t \in [-1, 1]$. Also note that
$f_N(1-t^2)$ is a polynomial of $t$.
So we found this polynomial $q(t)$.

$\square$

(b) Generalize this conclusion to an arbitrary interval [a,b].

**Proof**:

We can find $R$ such that $[a, b] \subseteq [-R, R]$.
From (a), we can find a polynomial $q(x)$ such that

$$ 
\left| q(x) - |x| \right|  < \epsilon / R
$$

For any $t \in [-R, R]$, let $p(t) = Rq(t/R)$.

So

$$ 
\left| |t/R| - q(t/R) \right| < \epsilon/R\\
$$

So

$R \left| |t/R| - q(t/R) \right| < \epsilon / R * R = \epsilon$

So

$$ 
\left| |t| - p(t) \right|  < \epsilon
$$

For $t \in [-R, R]$.

$\square$

### 6.7.8.

(a) Fix $a ∈ [−1,1]$ and sketch

$$ 
h_a(x) = \frac{1}{2} (|x-a| + (x-a))
$$

over $[-1,1]$. Note that $h_a$ is polygonal and satisfies
$h_a(x) = 0$ for all $x ∈ [−1,a]$.

**Solution**:

$$ 
h_a(x) =
\begin{cases}
    x - a &\text{if } a \leq x \leq 1\\
    0 &\text{if } -1 \leq x < a\\
\end{cases} 
$$

The shape is like this:

```python
          /
         /
        /
 ______/
-1     a    1
```

(b) Explain why we know $h_a(x)$ can be uniformly approximated with a polynomial on $[−1,1]$.

**Proof**: We have proved that given $\epsilon$, for $|t|$, we can find a polynomial $f(t) = \sum_{n = 0}^{k}a_{n} t^{n}$ such
that

$$ 
|f(t) - |t|| < \epsilon
$$

for $t \in [-2, 2]$. If $x, a \in [-1, 1]$, then
$x - a \in [-2, 2]$. So

$$ 
|f(x - a) - |x - a| | < \epsilon
$$

For $x \in [-1, 1]$. Let $g(x) = f(x - a)$, then $g(x)$ is
a polynomial of $x$. Now let

$$ 
l(x) = \frac{1}{2} (g(x) + (x - a)) \\
|l(x) - h_a(x)| = \frac{1}{2} |(g(x) + (x - a)) - (|x-a| + (x-a))| \\
= \frac{1}{2} | g(x) - |x-a|| < \epsilon / 2
$$

for $x \in [-1, 1]$.

So $h_a(x)$ can be uniformly approximated with a polynomial
$l(x)$ on $[−1,1]$.

(c) Let $\phi$  be a polygonal function that is linear on each subinterval of the partition.

$$ 
-1 = a_0 < a_1 < a_2 < a_3 < \cdots < a_n = 1.
$$

Show there exist constants $b_0, b_1, b_2, b_3, \cdots, b_{n-1}$  so that

$$ 
\phi (x) = \phi (-1) + b_0 h_{a_0} (x) + b_1 h_{a_1} (x)
+ \cdots + b_{n-1} h_{a_{n-1}} (x)
$$

for all $x \in [-1, 1]$.

**Solution**:

We know

$$
\phi (a_1) = \phi (-1) + b_0 h_{a_0} (a_1) \\
b_0 = \frac{\phi (a_1) - \phi (a_0)}{(a_1 - a_0)}
$$

Now plug $a_2$ 

$$ 
\phi (a_2) = \phi (-1) + b_0 h_{a_0} (a_2) + b_1 h_{a_1} (a_2)\\
= \phi (a_0) +
\frac{\phi (a_1) - \phi (a_0)}{(a_1 - a_0)} (a_2 - a_0) + b_1 (a_2 - a_1) \\
= \frac{\phi (a_0) a_1 - \phi (a_0) a_0 + 
\phi (a_1) a_2 - \phi (a_0) a_2 - \phi (a_1) a_0 + \phi (a_0) a_0}{a_1 - a0} + b_1(a_2 - a_1) \\
= \frac{
\phi (a_0) (a_1 - a_2) + \phi (a_1) (a_2 - a0)
}{
a_1 - a_0
} + b_1(a_2 - a_1)\\
$$

So we can solve $b_1$. We can continue this process to solve
all $b_n$.

Let $j(x) = \phi (-1) + b_0 h_{a_0} (x) + b_1 h_{a_1} (x) + \cdots + b_{n-1} h_{a_{n-1}} (x)$.

We know $j(x)$ is piecewise linear and $j(a_i) = \phi (a_i)$.
So $j(x) = \phi (x)$.

$\square$

(d) Complete the proof of WAT for the interval $[−1,1]$, and then generalize to an arbitrary interval $[a,b]$.

Proof: Given a continuous function $f(x)$ defined on $[−1,1]$ and
$\epsilon$. Based on Theorem 6.7.3, we can find a polygonal
function $\phi (x)$ defined on $[−1,1]$, such that

$$ 
\left| f(x) - \phi (x) \right| < \epsilon / 2
$$

for $x \in [−1,1]$. Since

$$ 
\phi (x) = \phi (-1) + b_0 h_{a_0} (x) + b_1 h_{a_1} (x)
+ \cdots + b_{n-1} h_{a_{n-1}} (x)
$$

And for each $h_{a_i}(x)$ we can find a polynomial $j_i(x)$,
such that $|h_{a_i}(x) - j_i(x)| < \frac{\epsilon}{2 b_i n}$
for $x \in [−1,1]$.

Let

$$ 
J(x) = \phi (-1) + b_0 j_0 (x) + \cdots + b_{n-1} j_{n-1}(x)
$$

So

$$ 
\left| f(x) - J(x) \right| <
|f(x) - \phi (x) | + | \phi (x) - J(x) |
< \epsilon / 2 +
\left| 
\sum_{i = 0}^{n - 1} b_i (h_{a_i}(x) - j_i(x))
 \right|
< \epsilon / 2 + n \frac{\epsilon }{2n} = \epsilon
$$

To generalize to $[a, b]$, we consider the function

$$ 
H_a(x) = \frac{1}{2} (|x-a| + (x-a))
$$

defined on $[-R, R]$ and fix $a \in [-R, R]$.
Then consider

$$
\frac{1}{R}H_a(x) = \frac{1}{2}
(|x/R-a/R| + (x/R-a/R))
$$ 

Let $t = x/R, b = a/R$, we have $t, b \in [-1, 1]$, and

$$ 
H_a(x) = \frac{R}{2} (|t-b| + (t-b)) = R h_b(t)
$$

Then we can find polynomial $f(t) = \sum_{k = 0}^{n}a_{k} t^{k}$ 
such that $|f(t) - h_b(t)| < \epsilon / R$, i.e.

$$ 
R|f(t) - h_b(t)| = 
\left| 
R \sum_{k = 0}^{n}a_{k} (x/R)^{k} - R h_b(t)
 \right| \\
\left| 
= \sum_{k = 0}^{n} \frac{a_{k}}{R^{k-1}}  x^{k}
- H_a(x)
\right| < \epsilon
$$

for $x \in [-R, R]$.

Then we can use exactly the same argument for $[-1, 1]$ to
prove $[-R, R]$.

$\square$

### 6.7.9.

(a) Find a counterexample which shows that WAT is not
true if we replace the closed interval $[a,b]$ with the open interval $(a,b)$.

**Solution**:

Consider $f(x) = \frac{1}{x}$ defined on $(0, 1)$. Given
$\epsilon = 1$, and assume we can find
$g(x) = \sum_{k = 0}^{n}a_{k} x^{k}$ such that

$$ 
|f(x) - g(x)| < 1
$$

for all $x \in (0, 1)$.

Note that $\lim_{x \to 0} g(x) = a_0$. So we can find
a $U_{\delta}(0)$ such that $x \in U_{\delta}(0)$, then
$|g(x) - a_0| < \epsilon$. So $|g(x)| < a_0 + \epsilon$.

On the other hand, $\lim_{x \to 0} \frac{1}{x} = \infty$,
so $|f(x) - g(x)|$ cannot be less than 1.

$\square$

(b) What happens if we replace $[a,b]$ with the closed set
$[a,∞)$. Does the theorem still hold?

**Solution**: No it does not.
Consider $f(x) = e^x$ defined on $[0, \infty)$. Given any polynomial
$g(x) = \sum_{k = 0}^{n}a_{k} x^{k}$, then we can find
$M$ such that $|a_k| < M$.

Then we have $|g(x)| < M \sum_{k = 0}^{n} x^k < M (n+1) x^n$ for
$x \geq 1$.

But $e^x > Kx^n$ for any $K, n$ as long as $x$ is large enough.

$\square$

### 6.7.10.

Is there a countable subset of polynomials $C$ with the
property that every continuous function on $[a,b]$ can be uniformly approximated by polynomials from $C$?

**Proof**: Consider all polynomials only with rational number
coefficients. This set is countable.

Given a continuous function $f(x)$, and $\epsilon > 0$, we can find a polynomial $g(x) = \sum_{n = 0}^{k}a_{n} x^{n}$ such that
$|f(x) - g(x)| < \epsilon / 2$.

On the other hand we can find $h(x) = \sum_{n = 0}^{k}b_{n} x^{n} \in C$ and let $M = \max \left\{ 1, |b|^k, |a|^k \right\}$ 

$$ 
|g(x) - h(x)|
< \sum_{n = 0}^{k}| a_{n} - b_n| |x^{n}| \\
< M \sum_{n = 0}^{k}| a_{n} - b_n|
$$

We can select $b_n \in \mathbf{Q}$ such that $|a_n - b_n| < \epsilon /(2(k+1)M)$

So $|g(x) - h(x)| < \epsilon  / 2$.

Then $|f(x) - h(x)| < \epsilon$

$\square$

### 6.7.11

Assume that $f$ has a continuous derivative on $[a,b]$. Show
that there exists a polynomial $p(x)$ such that

$$ 
|f(x) - p(x) | < \epsilon \text{ and }
|f'(x) - p'(x) | < \epsilon
$$

**Proof**: Given $\epsilon$, from WAT, we know we can find
$q(x)$ subh that $|f'(x) - q(x)| < \frac{\epsilon}{b - a}$.

Take the antiderivative of $q(x)$ and call it $p_0(x)$, note
$p_0'(x) = q(x)$. Let $c = f(a) - p_0(a)$, and let
$p(x) = p_0(x) + c$. We have

$$ 
p'(x) = q(x) \\
p(a) = f(a)
$$

Now we can use mean value theorem and let $g(x) = f(x) - p(x)$:

$$ 
\frac{g(x) - g(a)}{x - a} = g'(c) \\
|g(x) - g(a)| = |g'(c)| \cdot (x - a) =\\
|f'(x) - q(c)| (x - a) < \frac{\epsilon}{b - a} \cdot (x - a) \\
< \epsilon
$$

So we have $|f(x) - p(x) | < \epsilon$.

$\square$
