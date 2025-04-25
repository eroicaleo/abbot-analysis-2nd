# Chapter 06 Sequences and Series of Functions

## 6.2 Uniform Convergence of a Sequence of Functions

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
