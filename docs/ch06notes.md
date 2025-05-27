# Chapter 6. Sequences and Series of Functions

## 6.1 Discussion: The Power of Power Series

* Bernoulli wanted to find the precise value of the series

$$ 
\sum_{n = 1}^{\infty} 1 + \frac{1}{4} + \frac{1}{9} +
\frac{1}{16} + \cdots 
$$

* He was wable to handle the follow 2 series

$$ 
\sum_{n = 1}^{\infty} \frac{n^2}{2^n} \text{ and }
\sum_{n = 1}^{\infty} \frac{1}{n(n+1)}
$$

* Geometric series have long been known

$$
\tag{1}
\frac{1}{1 - x} = 1 + x + x^2 + x^3 + \cdots 
$$

* Bernoulli was operating on infinite series such as the
  Geometric series with tools from the budding theory of calculus.
  E.g. take the derivative on each side of equation (1) and we
  have:

$$
\tag{2}
\frac{1}{(1-x)^2} = 0+1+2x+3x^2 +4x^3 + \cdots
$$

* Our question is this a valid formula, at least for values of $x \in (-1, 1)$.

* Substituting $−x^2$ for x in (1) gives

$$
\tag{3}
\frac{1}{1 + x^2} = 1 - x^2 + x^4 - x^6 + x^8 - \cdots
$$

* When we take antiderivatives and use the fact that

$$
(\arctan (x))' = \frac{1}{1 + x^2} \text{ and }
\arctan (0) = 0,
$$

* equation (3) becomes

$$
\tag{4}
\arctan (x) = x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7}
+ \cdots.
$$

* Plugging $x = 1$ into equation (4) yields the striking 
  relationship:

$$
\tag{5}
\frac{\pi }{4} = 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7}
+ \frac{1}{9} - \cdots 
$$

* The constant $π$, which arises from the geometry of circles, has somehow found its way into an equation involving the reciprocals of the odd integers.
    * Is this a valid formula?
    * Can we really treat the infinite series in (3) like a
      finite polynomial?
    * Plugging $x = 1$ into equations (1), (2), or (3) yields mathematical gibberish, so is it prudent to anticipate something meaningful arising from equation (4) at this
    same value?

## 6.2 Uniform Convergence of a Sequence of Functions

### Definition 6.2.1.

For each $n ∈ N$, let $f_n$ be a function defined on a set $A ⊆ R$.
The sequence $(f_n)$ of functions converges pointwise on $A$ to a function $f$ if, for
all $x ∈ A$, the sequence of real numbers $f_n(x)$ converges to $f(x)$.

### Definition 6.2.3 (Uniform Convergence).

Let $(f_n)$ be a sequence of functions defined on a set $A ⊆ R$. Then, $(f_n)$ converges uniformly on $A$ to a limit
function $f$ defined on $A$ if, for every $ϵ > 0$, there exists an $N ∈ \mathbf{N}$ such that
$|f_n(x)−f(x)| < ϵ$ whenever $n ≥ N$ and $x ∈ A$.

### Definition 6.2.1B.

Let $(f_n)$ be a sequence of functions defined on a set $A ⊆ R$. Then, $(f_n)$ converges pointwise on $A$ to a limit
function $f$ defined on $A$ if, for every $ϵ > 0$ and $x \in A$, there exists an $N ∈ \mathbf{N}$ (perhaps dependent on $x$) such that
$|f_n(x)−f(x)| < ϵ$ whenever $n ≥ N$ and $x ∈ A$.

### 6.2.5 (Cauchy Criterion for Uniform Convergence).
A sequence of functions $(f_n)$ defined on a set $A ⊆ R$ converges uniformly on $A$ if
and only if for every $ϵ > 0$ there exists an $N ∈ \mathbf{N}$ such that $|f_n(x)−f_m(x)| < ϵ$ whenever $m,n ≥ N$ and $x ∈ A$.

### 6.2.6 (Continuous Limit Theorem).

Let $(f_n)$ be a sequence of
functions defined on $A ⊆ R$ that converges uniformly on $A$ to a function $f$. If each $f_n$ is continuous at $c ∈ A$, then $f$ is continuous at $c$.

**Proof**: Given $\epsilon$, we can find $N$, $n > N$ and

$$ 
|f_n(x) - f(x)| < \epsilon
$$

Fix $n$, Since $f_n(x)$ is continuous at $c$, we can find
$U_{\delta}(c)$, $|f_n(x) - f_n(c)| < \epsilon / 3$.

Then

$$ 
|f(x) - f(c) | \leq \\
|f(x) - f_n(x) | + |f_n(x) - f_n(c)| + |f_n(c) - f(c)| \leq \\
\epsilon / 3 + \epsilon / 3 + \epsilon / 3 = \epsilon
$$

## 6.3. Uniform Convergence and Diﬀerentiation

### Theorem 6.3.1 (Diﬀerentiable Limit Theorem).

Let $f_n → f$ pointwise
on the closed interval $[a,b]$, and assume that each $f_n$ is diﬀerentiable. If $(f_n')$
converges uniformly on $[a,b]$ to a function $g$, then the function $f$ is diﬀerentiable and $f' = g$.

**Proof**:

Given a point $c \in [a,b]$, we want to estimate

$$ 
\left|
\frac{f(x) - f(c)}{x - c} - g(c)
\right|
$$

We can have 
$$
\tag{a}
\left|
\frac{f(x) - f(c)}{x - c} - g(c)
\right| \leq \\
\left| 
\frac{f(x) - f(c)}{x - c} - \frac{f_N(x) - f_N(c)}{x - c}
\right| +
\left| \frac{f_N(x) - f_N(c)}{x - c} - g_N(c) \right| +
\left| g_N(c) - g(c) \right| 
$$

Since $(g_n) \rightarrow g$ uniformly, we can find $N$, such that
$n \leq N, |g_n(x) - g(x)| < \epsilon / 3$. Then fix this $N$.
Sine $f_N$ is differentiable, we can find $U_{\delta}(c)$,
$x \in U_{\delta}(c)$,
$\left| \frac{f_N(x) - f_N(c)}{x - c} - g_N(c) \right| <
\epsilon / 3$.

So given this $N$ and $\delta$, let's estimate

$$ 
\left| 
\frac{f(x) - f(c)}{x - c} - \frac{f_N(x) - f_N(c)}{x - c}
\right|
$$

Consider the following and use Mean Value Theorem

$$ 
\left| 
\frac{f_m(x) - f_m(c)}{x - c} - \frac{f_n(x) - f_n(c)}{x - c}
\right| = \\
|g_m(\alpha_m) - g_n(\alpha_m)| < \epsilon / 3
$$

We have

$$ 
\lim_{m \to \infty} 
\left| 
    \frac{f_m(x) - f_m(c)}{x - c} - \frac{f_n(x) - f_n(c)}{x - c}
\right| =
\lim_{m \to \infty} 
|g_m(\alpha_m) - g_n(\alpha_m)| = |g(\alpha) - g_n(\alpha)|
\leq \epsilon / 3 \\
\lim_{m \to \infty} 
\left| 
    \frac{f_m(x) - f_m(c)}{x - c} - \frac{f_n(x) - f_n(c)}{x - c}
\right| =
\left| 
    \frac{f(x) - f(c)}{x - c} - \frac{f_n(x) - f_n(c)}{x - c}
\right| 
$$

In summary, $(a) < \epsilon$.

$\square$

### Theorem 6.3.2.

Let $(f_n)$ be a sequence of diﬀerentiable functions defined on
the closed interval $[a,b]$, and assume $(f'_n)$ converges uniformly on $[a,b]$. If there exists a point $x_0 ∈ [a,b]$ where $f_n(x_0)$ is convergent, then $(f_n)$ converges uniformly on $[a,b]$.

Proof. Exercise 6.3.7.

## 6.5 Power Series

### Lemma 6.5.3 (Abel’s Lemma).

Review exercise 2.7.13 (Abel’s Test) Abel’s Test for convergence states that if the series $\sum_{n = 1}^{\infty}x_n$ converges, and if $(y_k)$ is a sequence satisfying

$$ 
y_1 \geq y_2 \geq y_3 \geq \cdots \geq 0,
$$

then the series $\sum_{k = 1}^{\infty}x_k y_k$ converges.

(a) Use Exercise 2.7.12 to show that

$$ 
\sum_{k = 1}^{n} x_k y_k = s_n y_{n+1} +
\sum_{k = 1}^{n} s_k (y_k - y_{k+1})
$$

where $s_n = x_1 + x_2 + x_3 + \cdots + x_n$.

**Proof**: Note

$$ 
\sum_{k = 1}^{n} s_k (y_k - y_{k+1}) =
(s_1 y_1 - s_1 y_2) + (s_2 y_2 - s_2 y_3) + \cdots +
(s_n y_n - s_n y_{n+1}) = \\
s_1 y_1 + (s_2 - s_1) y_2 + (s_3 - s_2) y_3 + \cdots +
(s_n - s_{n-1}) y_n - s_n y_{n+1} = \\
x_1 y_1 + x_2 y_2 + \cdots + x_n y_n - s_n y_{n+1}
$$

This proves the claim.

(b) Use the Comparison Test to argue that $\sum_{k = 1}^{\infty}s_k (y_k - y_{k+1})$  converges absolutely, and show how this
leads directly to a proof of Abel’s Test.

Proof: $s_k$ is bounded, so assume $|s_k| < M$.

$$ 
\sum_{k = 1}^{n} |s_k (y_k - y_{k+1})| <
\sum_{k = 1}^{n} M (y_k - y_{k+1}) < M y_1
$$

So $\sum_{k = 1}^{\infty}s_k (y_k - y_{k+1})$  converges absolutely.

Also note $(y_n) \rightarrow y$ for some $y \geq 0$, so
$\lim_{n \to \infty} s_n y_{n+1}$ converges.
Thus $\sum_{k = 1}^{\infty}x_k y_k$ converges.

$\square$

**(Abel’s Lemma)** Let $b_n$ satisfy $b_1 \geq  b_2 \geq  b_3 \geq  \cdots \geq  0$, and let $\sum_{n = 1}^{\infty}a_n$
be a series for which the partial sums are bounded. In other words,
assume there exists $A > 0$ such that

$$ 
\left| a_1 + a_2 + a_3 + \cdots + a_n \right| \leq A
$$

for all $n \in \mathbf{N}$, then, for all $n \in \mathbf{N}$

$$ 
\left| a_1b_1 + a_2b_2 + a_3b_3 + \cdots + a_nb_n \right|
\leq A b_1
$$

Let $s_n = a_1 + a_2 + a_3 + \cdots + a_n$,

$$ 
\left| \sum_{k = 1}^{n} a_k b_k \right|  = \\
\left| s_n b_{n+1} +
\sum_{k = 1}^{n} s_k (b_k - b_{k+1}) \right| \leq \\
\left| s_n b_{n+1} \right| +
\left| \sum_{k = 1}^{n} s_k (b_k - b_{k+1}) \right| \leq \\
A b_{n+1} + \sum_{k = 1}^{n} A (b_k - b_{k+1}) = A b_1
$$

$\square$

### 6.5.4 (Abel’s Theorem).

Let $g(x) = \sum_{n = 0}^{\infty} a_n x^n$ be a power series
that converges at the point $x = R > 0$, Then the series
converges uniformly on the interval $[0,R]$.
A similar result holds if the series converges at $x =−R$.

**Proof**: Let $c_n = a_n R^n$, $|c_1 + c_2 + c_3 + \cdots + c_n| \leq C$. Let $b_n = \left( \frac{x}{R} \right)^n$,
so $b_1 \geq  b_2 \geq  b_3 \geq  \cdots \geq 0$.

Since $\sum_{n = 1}^{\infty}c_n$ converges, we can find $N$,
for $n > m > N$,

$$
\left| c_{m+1} + \cdots + c_n \right| < \epsilon
$$

Then for other $0 \leq x < R$,

$$ 
\left| g_{m+1}(x) + \cdots + g_n(x) \right| =\\
\left| c_{m+1}b_{m+1} + \cdots + c_n b_n \right| \leq
\epsilon b_{m+1} < \epsilon
$$

So $g(x)$ converges uniformly on the interval $[0,R]$.

$\square$

### Theorem 6.5.5.

If a power series converges pointwise on the set $A ⊆ R$, then
it converges uniformly on any compact set $K ⊆ A$.

Proof: Since $K$ is compact, we can find $K \subseteq [a, b]$,
and $a, b \in K$. Assume $a < 0 < b$, the based on 6.5.4 (Abel’s Theorem), this power series converges on $[a, 0]$ and $[0, b]$, 
so converges on $[a, b] \supseteq K$.

$\square$

### Theorem 6.5.6.

If $\sum_{n = 0}^{\infty}a_n x^n$ converges for all $x ∈ (−R,R)$,
then the diﬀerentiated series $\sum_{n = 1}^{\infty}na_n x^{n-1}$ converges at each $x ∈ (−R,R)$ as well. Consequently, the convergence is uniform on compact sets contained in $(−R,R)$.

(a) If $s$ satisfies $0 < s < 1$, show $ns^{n−1}$ is bounded for
all $n ≥ 1$.

**Proof**: 

We compare $ns^{n-1}$ and $(n+1)s^n$ and we have $ns^{n-1} > (n+1)s^n$, when $\frac{n}{n+1} > s$. So $ns^{n-1}$ is bounded.

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

## 6.6. Taylor Series

### Theorem 6.6.2 (Taylor’s Formula).

Let

$$
\tag{3}
f(x) = a_0 + a_1 x^1 + a_2 x^2 + a_3 x^3 + \cdots + a_n x^n + \cdots
$$

be defined on some nontrivial interval centered at zero. Then,

$$ 
a_n = \frac{f^{(n)}(0)}{n!}.
$$

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

### Theorem 6.6.3 (Lagrange’s Remainder Theorem).

Let $f$ be diﬀerentiable $N +1$ times on $(−R,R)$, define
$a_n = f^{(n)}(0)/n!$  for $n = 0, 1, \dots, N,$ and let

$$ 
S_N(x) = a_0 + a_1 x + a_2 x^2 + \cdots + a_N x^N
$$

Given $x \not = 0$ in $(−R,R)$, there exists a point $c$ satisfying
$|c| < |x|$ where the error function $E_N(x) = f(x) - S_N(x)$
satisfies

$$ 
E_N(x) = \frac{
  f^{(N+1)}(c)
}{(N+1)!} x^{N+1}
$$

Proof: Note that

$$ 
E_N(0) = f(0) - S_N(0) = f(0) - f(0) = 0 \\
E_N'(0) = f'(0) - S_N'(0) = f'(0) - a_1 = f'(0) - f'(0) = 0 \\
E_N^{(2)}(0) = f''(0) - S_N''(0) =
f''(0) - 2 a_2 = f''(0) - 2 f''(0)/2 = 0 \\
\cdots \\
E_N^{(N)}(0) = f^{(N)}(0) - S_N^{(N)}(0) =
f^{(N)}(0) - (N!) a_N = f^{(N)}(0) - (N!) f^{(N)}(0)/(N!) = 0 \\
$$

So we can use Generalized Mean Value Theorem (Theorem 5.3.5)

$$ 
\frac{
E_N(x) - 0
}{
x^{N+1} - 0
} =
\frac{
E_N^{(1)}(x_1)
}{
(N+1)x_1^N
} =
\frac{
E_N^{(2)}(x_2)
}{
(N+1)Nx_2^{N-1}
} = \cdots =
\frac{
E_N^{(N+1)}(x_{N+1})
}{
(N+1)!
}
$$

So we have

$$ 
E_N(x) = \frac{
f^{(N+1)}(c)
}{
(N+1)!
} x^{N+1}
$$

$\square$
