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

Consdier the process of constructing the Cantor set, and define

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
