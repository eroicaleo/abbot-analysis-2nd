# Chapter 07 The Riemann Integral

## 7.2 The Definition of the Riemann Integral

### 7.2.1.

Let $f$ be abounded function on $[a,b]$, and let $P$ be an arbitrary
partition of $[a,b]$. First, explain why $U(f) ≥ L(f,P)$. Now, prove Lemma 7.2.6.

Proof: Given any partition $P'$,

$$
U(f, P') \geq U(f, P \cup P')
\geq L(f, P \cup P') \geq L(f, P)
$$

That means $L(f,P)$ is a lower bound of
$\{U(f,P) : P \in \mathbb{P}\}$.

So $U(f) \geq L(f,P)$.

This means $U(f)$ is also an upper bound of
$\{L(f,P) : P \in \mathbb{P}\}$.

So $U(f) \geq L(f)$.

$\square$

### 7.2.2.

Consider $f(x) = 1/x$ over the interval $[1,4]$. Let $P$ be the
partition consisting of the points $\{1,3/2,2,4\}$.

(a) Compute $L(f,P)$, $U(f,P)$, and $U(f,P)−L(f,P)$.

**Solutions**:

$L(f, P) = \frac{3}{2} \cdot \frac{1}{2} + \frac{1}{2} \cdot \frac{1}{2} + \frac{1}{4} \cdot 2 = \frac{3}{2}$

$$ 
U(f, P) = 1 \cdot \frac{1}{2} + \frac{3}{2} \cdot \frac{1}{2}
+ \frac{1}{2} \cdot 2 = \frac{9}{4}
$$

The difference is $\frac{3}{4}$.

### 7.2.3 (Sequential Criterion for Integrability).

(a) Prove that
a bounded function $f$ is integrable on $[a,b]$ if and only if there exists a
sequence of partitions $(P_n)^{\infty}_{n=1}$ satisfying

$$ 
\lim_{n \to \infty} [U(f, P_n) - L(f, P_n)] = 0,
$$

and in this case $\int_{a}^{b}f = \lim_{n \to \infty} U(f, P_n) = \lim_{n \to \infty}  L(f, P_n)$.

**Proof**: $\Rightarrow$
given $1/n$, we can find $P_n$, such that

$$ 
0 < U(f, P_n) - L(f, P_n) < \frac{1}{n}
$$

Then we have

$$ 
\lim_{n \to \infty} [U(f, P_n) - L(f, P_n)] = 0.
$$

$\Leftarrow$

$U(f) \leq U(f, P_n)$ and $L(F) \geq L(f, P_n)$,
so $U(f) - L(f) \leq U(f, P_n) - L(f, P_n)$.

Since $\lim_{n \to \infty} [U(f, P_n) - L(f, P_n)] = 0$
then $U(f) - L(f) \leq 0$.

On the other hand, exercise 7.2.1 proves $U(f) - L(f) \geq 0$. So $U(f) = L(f)$. So $f$ is integrable.

$\square$

### 7.2.4.

Let $g$ be bounded on $[a,b]$ and assume there exists a partition $P$ with $L(g,P) = U(g,P)$. Describe g. Is it integrable? If so, what is the value of $\int_{a}^{b}g$?

**Solutions**: In each segment of $P$, it's flat.

$\square$

### 7.2.5.

Assume that, for each $n$, $f_n$ is an integrable function on $[a,b]$.

If $(f_n) → f$ uniformly on $[a,b]$, prove that $f$ is also integrable on this set. (We
will see that this conclusion does not necessarily follow if the convergence is pointwise.)

**Proof**: Given $\epsilon$, we can find $N$ such that
$n > N$, $|f_n(x) - f(x)| < \frac{\epsilon}{2(b-a)}$.

Fix this $n$, we can find a partition such that 
$U(f_n, P) - L(f_n, P) < \epsilon / 2$

$$
U(f_n, P) - L(f_n, P) = \sum_{k = 1}^{n}
(M_{n, k} - m_{n, k}) \Delta x_{n, k} \geq
\sum_{k = 1}^{n} (M)
$$

### 7.2.6.

A tagged partition $(P,{c_k})$ is one where in addition to a partition $P$ we choose a sampling point $c_k$ in each of the subintervals $[x_{k−1},x_k]$.
The corresponding Riemann sum,

$$ 
R(f, P) = \sum_{k = 1}^{n}
f(c_k) \Delta x_k,
$$

is discussed in Section 7.1, where the following definition is alluded to.

Riemann’s Original Definition of the Integral: A bounded function f is
integrable on $[a,b]$ with $\int_{a}^{b} f = A$,
if for all $ϵ > 0$ there exists a $δ > 0$ such that
for any tagged partition $(P,{c_k})$ satisfying
$\Delta x_k < \delta$ for all $k$, it follows that

$$ 
\left| R(f, P) - A \right| < \epsilon
$$

Show that if $f$ satisfies Riemann’s definition above, then $f$ is integrable in the
sense of Definition 7.2.7. (The full equivalence of these two characterizations of
integrability is proved in Section 8.1.)

**Proof**:

$$
M_k - m_k < f(c_{M, k}) + \frac{\epsilon}{4(b-a)} -
(f(c_{m, k}) - \frac{\epsilon}{4(b-a)})
= f(c_{M, k}) - f(c_{m, k}) + \frac{\epsilon}{2(b-a)}
$$

So

$$ 
\sum_{k=1}^{n} (M_k - m_k) \Delta x_k \\
< \sum_{k=1}^{n} (f(c_{M, k}) - f(c_{m, k}) + \frac{\epsilon}{2(b-a)}) \Delta x_k \\
= R_1(f, P) - R_2(f, P) + \epsilon / 2 \\
< \epsilon / 2 + \epsilon / 2 = \epsilon.
$$

$\square$

## 7.3 Integrating Functions with Discontinuities

### 7.3.1.

Consider the function

$$ 
h(x) = \begin{cases}
    1 &\text{for } 0 \leq x < 1\\
    2 &\text{for } x = 1\\
\end{cases} 
$$

over the interval $[0,1]$

(a) show that $L(f,P) =1$ for every partition $P$ of
$[0,1]$.

Proof: Assume $P$ is $0 = x_0 < x_1 < x_2 < \cdots x_{n-1} < x_n = 1$. In the first $n-1$ segments, $h(x)$ is constant $1$, so the $m_k = 1$. In the nth segment,
the $m_n$ is still $1$. So $L(f, P) = 1$.

(b) Construct a partition $P$ for which $U(f,P) < 1+1/10$.

**Solutions**: Let $P = \{0, \frac{19}{20}, 1\}$,

$$ 
U(f, P) = \frac{19}{20} + \frac{1}{10} < 1 + \frac{1}{10}
$$.

(c) Given $ϵ > 0$, construct a partition $P_ϵ$ for which $U(f,P_ϵ) < 1+ϵ$.

**Proof**: Let $P = \{0, 1 - \frac{\epsilon}{2}, 1\}$.

$$ 
U(f, P) = 1 - \frac{\epsilon}{2} + \epsilon = 1 + \frac{\epsilon}{2}.
$$

### 7.3.2.

Recall that Thomae’s function

$$ 
t(x) =
\begin{cases}
    1 &\text{if } x = 0\\
    1/n &\text{if } x = m/n \\
    0 &\text{if } x \not\in \mathbf{Q} \\
\end{cases} 
$$

has a countable set of discontinuities occurring at precisely every rational number.
Follow these steps to prove t(x) is integrable on
$[0,1]$ with $\int_{0}^{1} t = 0$.

(a) First argue that $L(t,P) = 0$ for any partition $P$ of $[0,1]$.

**Proof**: Given any partition $0 = x_0 < x_1 < x_2 < \cdots x_{n-1} < x_n = 1$. For any segment, the
$m_k$ is always $0$. So $L(f,P) = 0$.

(b) Let $ϵ > 0$, and consider the set of points
$D_{ϵ/2} = \{x ∈ [0,1] : t(x) ≥ ϵ/2\}$.
How big is $D_{ϵ/2}$?

**Solutions**: Assume $n < 2/\epsilon$, the the size
is at most $n(n+1)/2$.

(c) To complete the argument, explain how to construct a partition $P_ϵ$ of $[0,1]$ so that $U(t,P_ϵ) < ϵ$.

**Solutions**: For each of $x \in [0, 1]$ such that
$t(x) > \epsilon /2$, we make it a partition $[x, x + \frac{\epsilon}{n(n+1)}]$. So the upper sum is less than
$\frac{\epsilon}{n(n+1)}$. Since there are only
$n(n+1)/2$ of them, then total upper sum is
$\epsilon / 2$. For other segments, each upper sum
is $\epsilon / 2 \Delta x_k$, so the total upper
sum is less than $\epsilon / 2$. Then the total sum
is $\epsilon$.

$\square$

### 7.3.3.

Let

$$ 
f(x) = \begin{cases}
    1 &\text{if } x = 1/n \text{ for some } n \in N\\
    0 &\text{otherwise }\\
\end{cases}
$$

Show that $f$ is integrable on $[0,1]$ and compute
$\int_{0}^{1}f$.

**Proof**: Let

$$
P_n = \{
0, \frac{1}{n}, \frac{1}{n} + \frac{1}{n^2},
\frac{1}{n-1}, \frac{1}{n-1} + \frac{1}{n^2},
\frac{1}{n-2}, \frac{1}{n-2} + \frac{1}{n^2},
\}
$$

So

$$
U(f, P_n) = \frac{1}{n} + \frac{1}{n^2} \times (n-1) \\
< \frac{2}{n} \rightarrow 0
$$

So $\int_{0}^{1} f = 0$.

$\square$

###

7.3.4. Let $f$ and $g$ be functions defined on (possibly diﬀerent) closed
intervals, and assume the range of $f$ is contained in the domain of $g$ so that the
composition $g ◦f$ is properly defined.

(a) Show, by example, that it is not the case that if
$f$ and $g$ are integrable, then $g ◦f$ is integrable.

Solution: We use the example in the previous 2
exercises. Consider $f(x)$ is the Thomae function,
and $g(x)$ is the function in exercise 7.3.3.
Then $g◦f$ is the Dirichlet function, which is not
differentiable.

(b) If $f$ is increasing and $g$ is integrable, then $g ◦f$ is integrable.

Proof: Assume $f$ is defined on $[a,b]$, and $g$ is
defined on $[c,d]$, and $[f(a), f(b)] \subseteq [c, d]$. Since $g$ is integrable, and given $\epsilon$.
We can find a $P = \{x_0, x_1, \cdots, x_n\}$ for $[c,d]$ such that
$U(g,P) - L(g,P) < \epsilon.$

Assume $x_{k-1} \leq f(a) < x_k$ for some $k$. And let
$c$ be the supremum of

$$ 
S_k = \{x : f(x) \leq x_k\}
$$

If $f(c) \leq x_k$, then
$(M_{g ◦f, [a,c]} - m_{g ◦f, [a,c]}) (c-a) \leq (M_k - m_k)\Delta _k$.

If $f(c) > x_k$, then assume $f(c) \in (x_{l-1}, x_l]$
for some $l > k$. Then we can divide $[a,c]$ into
$[a,d]$ and $[d,c]$ so that

$$ 
(M_{g ◦f, [a,d]} - m_{g ◦f, [a,d]}) (d-a) +
(M_{g ◦f, [d,c]} - m_{g ◦f, [d,c]}) (c-d) \leq \\
(M_k - m_k)\Delta _k +
(M_{g, [x_{l-1}, f(c)]} - m_{g, [x_{l-1}, f(c)]})(f(c) - x_{l-1})
$$

In this way, we can construct a partition of $[a,b]$
such that

$U(g ◦f,P') - L(g ◦f,P') < \epsilon.$

$\square$

(c) If $f$ is integrable and $g$ is increasing, then $g ◦f$ is integrable.

**Solutions**: This is not true.
Consider $f$ is the Thomae function.

$$ 
g(x) = \begin{cases}
    0 &\text{if } x = 0\\
    1 &\text{if } x > 0\\
\end{cases}
$$

Then $g ◦f$ is again the Dirichlet function.

$\square$

## 7.4 Properties of the Integral

### 7.4.4.

Show that if $f(x) > 0$ for all $x ∈ [a,b]$ and $f$ is integrable, then $\int_{a}^{b} f > 0$.

**Proof**: No idea for now. Seems like we need to use
section 7.5.

### 7.4.5.

Let $f$ and $g$ be integrable functions on $[a,b]$.

(a) Show that if $P$ is any partition of $[a,b]$, then

$$
U(f+g, P) \leq U(f, P) + U(g, P)
$$

Provide a specific example where the inequality is strict. What does the corresponding inequality for lower sums look like?

**Proof**: For any segment $[x_k, x_{k+1}]$, assume
$M_{f+g, k}$ is the supremum of $f+g$ on this segment.
For any $c \in [x_k, x_{k+1}]$, $(f+g)(c) = f(c) + g(c)\leq M_{f,k} + M_{g, k}$. So $M_{f+g, k} \leq M_{f,k} + M_{g, k}$.

Therefore $U(f+g, P) \leq U(f, P) + U(g, P)$.

Let $f(x) = x, g(x) = -x, [a,b] = [0,1], P = \{0, 1\}$.

So $f+g = 0$, $U(f+g, P) = 0$.
On the other hand, $U(f,P) = 1, U(g,P) = 0$, so
$U(f+g, P) = U(f,P) + U(g,P)$.

The lower sums look like

$$
L(f+g, P) \geq L(f, P) + L(g, P)
$$

$\square$

(b) Review the proof of Theorem 7.4.2 (ii), and provide an argument for part (i) of this theorem.

**Proof**: Since $f, g$ are all integrable,
we can find $P_{f, n}, Q_{g, n}$, such that

$$ 
\lim_{n \to \infty} U(f, P_{f, n}) - L(f, P_{f, n}) = 0 \\
\lim_{n \to \infty} U(g, P_{g, n}) - L(g, P_{g, n}) = 0 \\
$$

Then let $P_n = P_{f, n} \cup P_{g, n}$, then

$$ 
\lim_{n \to \infty} U(f, P_{n}) - L(f, P_{n}) = 0 \\
\lim_{n \to \infty} U(g, P_{n}) - L(g, P_{n}) = 0 \\
$$

Adding them together

$$ 
\lim_{n \to \infty}
(U(f, P_{n}) + U(g, P_{n})) -
(L(f, P_{n}) + L(g, P_{n})) = 0
$$

Furthermore, We apply (a), then we know

$$ 
\lim_{n \to \infty}
U(f+g, P_n) -
L(f+g, P_n) \leq 0
$$

On the other hand, $U(f+g, P_n) - L(f+g, P_n) \geq 0$.
So

$$ 
\lim_{n \to \infty}
U(f+g, P_n) -
L(f+g, P_n) = 0
$$

So $f+g$ is integrable. Since $U(f+g, P) \leq U(f, P) + U(g, P)$, then $U(f+g) \leq U(f) + U(g)$.
Similarly, $L(f+g) \geq  L(f) + L(g)$.

So $\int_{a}^{b} (f+g) = \int_{a}^{b}f + \int_{a}^{b} g$.

$\square$

### 7.4.6.

Although not part of Theorem 7.4.2, it is true that the product of integrable functions is integrable. Provide the details for each step in the following proof of this fact:

