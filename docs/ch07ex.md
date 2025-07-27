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

**Solution**:

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

**Solution**: In each segment of $P$, it's flat.

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

**Solution**: Let $P = \{0, \frac{19}{20}, 1\}$,

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

**Solution**: Assume $n < 2/\epsilon$, the the size
is at most $n(n+1)/2$.

(c) To complete the argument, explain how to construct a partition $P_ϵ$ of $[0,1]$ so that $U(t,P_ϵ) < ϵ$.

**Solution**: For each of $x \in [0, 1]$ such that
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

### 7.3.4.

Let $f$ and $g$ be functions defined on (possibly diﬀerent) closed
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

Proof: The following is not correct.

Assume $f$ is defined on $[a,b]$, and $g$ is
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

**Solution**: This is not true.
Consider $f$ is the Thomae function.

$$ 
g(x) = \begin{cases}
    0 &\text{if } x = 0\\
    1 &\text{if } x > 0\\
\end{cases}
$$

Then $g ◦f$ is again the Dirichlet function.

$\square$

### 7.3.5.

Provide an example or give a reason why the request is impossible.

(a) A sequence $(f_n) → f$ pointwise, where each $f_n$ has at most a finite number
of discontinuities but $f$ is not integrable.

**Solution**:

Consider

$$ 
f_n(x) = \begin{cases}
    1 &\text{if } x = p/q, q \leq n \\
    0 &\text{otherwise}\\
\end{cases} 
$$

Then $f$ is the Dirichlet function which is not integrable.

(b) A sequence $(g_n) → g$ uniformly where each gn has at most a finite number of discontinuities and $g$ is not integrable.

**Proof**: Impossible. Each $g_n$ is integrable, and
$(g_n) → g$ uniformly. So from exercise 7.2.5, $g$ is
integrable.

(c) A sequence $(h_n) → h$ uniformly where each $h_n$ is not integrable but $h$ is integrable.

**Solution**: This is possible. Consdier

$$ 
h_n(x) = \begin{cases}
    1/n &\text{if } x \in \mathbf{Q}\\
    0 &\text{otherwise }\\
\end{cases} 
$$

$\square$

### 7.3.6.

Let $\{r_1,r_2,r_3,...\}$ be an enumeration of all the rationals in $[0,1]$, and define 

$$ 
g_n(x) = \begin{cases}
    1 &\text{if } x = r_n \\
    0 &\text{otherwise.}\\
\end{cases} 
$$

Anwser:

(a) Is $G(x) = \sum_{n = 1}^{\infty} g_n(x)$ integrable
on $[0, 1]$?

**Solution**: $G(x)$ is the Dirichlet function.
So it's not integrable.

(b) $F(x) = \sum_{n = 1}^{\infty} g_n(x)/n$
integrable on $[0, 1]$?

**Proof**: Yes. Given $\epsilon$, we can find $n$ such
that $1/n < \epsilon/2$, for $r_1,r_2,r_3,...r_n$, 
we create a segment $[r_i, r_i + 1/n^2]$. Then upper
sum of those segments will be less than $1/n < \epsilon / 2$. For the rest of them, the upper sum will
be less than $1/n \times 1 = 1/n < \epsilon / 2$.
So overall the upper sum is less than $\epsilon$.

So it's integrable and the value is 0.

$\square$

### 7.3.7.

Assume $f : [a,b] → R$ is integrable.

(a) Show that if $g$ satisfies $g(x) = f(x)$ for all but a finite number of points
in $[a,b]$, then $g$ is integrable as well.

**Proof**: Consider $h(x) = f(x) - g(x)$, then $h(x)$
is $0$ but a finite number of points. So it's integrable.

(b) Find an example to show that $g$ may fail to be integrable if it diﬀers from
$f$ at a countable number of points.

**Solution**: Consider $f = 0$ and $g$ is the Thomae
function.

$\square$

### 7.3.8.

As in Exercise 7.3.6, let $\{r_1,r_2,r_3,...\}$ be an enumeration of all the rationals in $[0,1]$,
but this time define

$$ 
h_n(x) =
\begin{cases}
    1 &\text{if } r_n < x \leq 1 \\
    0 &\text{if } 0 \leq x \leq r_n \\
\end{cases}
$$

Show $H(x) = \sum_{n = 1}^{\infty}h_n(x) / 2^n$
is integrable on $[0,1]$ even though it has discontinuities at every rational point.

**Proof**: 

Simply notice that the $H(x)$ is a monotoneous increasing function will prove it.

We can also find the partition.

Given $\epsilon$, we can find $n$ such that
$\frac{1}{2^n} < \epsilon / (2n)$.
For partition $P$ which is
$x_0 = 0, x_1,x_2,x_3,...,x_n = 1$ which is the set 
$\{0, 1, r_1,r_2,r_3,...,r_n\}$.

Between $(x_{k-1}, x_k]$, $M_k - m_k \leq \frac{1}{2^{n+1}} + \frac{1}{2^{n+2}} + \cdots < \frac{1}{2^n}$.

Also consider the interval $[x_{k-1}, x_{k-1} + \frac{1}{2^n}]$, for this interval, $m = H(x_{k-1})$,

$$ 
M < m + \frac{1}{2} + \frac{1}{2^{n+1}} + \frac{1}{2^{n+2}} + \cdots < m + \frac{1}{2} + \frac{1}{2^n}
$$ 

So

$$ 
(M - m) \Delta < (\frac{1}{2} + \frac{1}{2^n}) \frac{1}{2^n} < \frac{1}{2^n}
$$

since there are $n$ of them, then the sum
is less than $\frac{n}{2^n} < \epsilon / 2$,
for other part $[x_{k-1} + \frac{1}{2^n}, x_k]$,
then sum is less than $\epsilon / 2$.

$\square$

### 7.3.9 (Content Zero).

A set $A ⊆ [a,b]$ has content zero if for every
$ϵ > 0$ there exists a finite collection of open intervals $\{O_1,O_2,...,O_N\}$ that contain $A$
in their union and whose lengths sum to $ϵ$ or less.

Using $|O_n|$ to refer
to the length of each interval, we have

$$ 
A \subseteq \bigcup_{n=1}^{N}  O_n
\text{ and }
\sum_{n=1}^{N} |O_n| \leq \epsilon.
$$

Anwser

(a) Let $f$ be bounded on $[a,b]$.
Show that if the set of discontinuous points of
$f$ has content zero, then $f$ is integrable.

**Proof**: Assume $|f(x)| < M$, and given $\epsilon$
we can find a set of
open intervals $\{O_1,O_2,...,O_N\}$ such that

$$ 
A \subseteq \bigcup_{n=1}^{N}  O_n
\text{ and }
\sum_{n=1}^{N} |O_n| \leq \epsilon / (4M).
$$

Let $O_n = (a_n, b_n)$, let
$P = \{a_1, b_1, \cdots, a_n, b_n\}$.
In these intervals, the difference of the upper
sum and lower sum is less than
$2M \times \epsilon / (4M) = \epsilon / 2$.

In other interval, $f(x)$ is continuous, so we can find
a partition such that the upper
sum and lower sum is less than $\epsilon /2$.

$\square$

(b) Show that any finite set has content zero.

Proof: Assume there are $n$ points in $A$,
$x_1, x_2, x_3, \dots x_{n}$, let

$$ 
O_n = (x_n - \epsilon / 2n, x_n + \epsilon / 2n)
$$

$\square$

(c) Content zero sets do not have to be finite.
They do not have to be countable. Show that the Cantor set $C$ defined in Section 3.1 has content zero.

**Proof**:

Note $|C_1| = \frac{2}{3}$, we can use 2 open sets with length of $\frac{3}{8}$ to cover it.

Similarly, $|C_2|$ can be coverd by $4$ intervals of length $\frac{1}{8}$.

$|C_n|$ can be coverd by $2^n$ intervals of length
$\frac{1}{8 \times 3^{n-2}}$.

So

$$ 
\sum_{n=1}^{N} |O_n| = \frac{1}{2} \times
\left( \frac{2}{3} \right) ^{n-2}.
$$

In addition,

$$
C \subset C_n \subset \bigcup_{k=1}^{n} O_n
$$

$\square$

(d) Prove that

$$ 
h(x) =
\begin{cases}
    1 &\text{if } x \in C\\
    0 &\text{if } x \not\in C\\
\end{cases} 
$$

is integrable, and find the value of the integral.

**Proof**: if $x \not\in C$, $x$ is in an open set.
So $h(x)$ is continuous at $x$. Then we can apply (a).
So $h(x)$ is integrable. and the value is $0$.

## 7.4 Properties of the Integral

### 7.4.1.

Let $f$ be a bounded function on a set $A$, and set

$$ 
M = \sup \{f(x) : x \in A\} \\
m = \inf \{f(x) : x \in A\} \\
M' = \sup \{|f(x)| : x \in A\} \\
m' = \inf \{|f(x)| : x \in A\} \\
$$

Anwser:

(a) Show that $M - m \geq M' - m'$.

Proof:

* case 1: $M > 0, m > 0$ then $M' = M, m' = m$
* case 2: $M > 0, m = 0$ then $M' = M, m' = m$
* case 3: $M > 0, m < 0$ then $M' = M, m' > 0 > m$
* case 4: $M = 0, m = 0$ then $M' = M, m' = m$
* case 5: $M = 0, m < 0$ then $M' = -m, m' = -M$
* case 6: $M < 0, m < 0$ then $M' = -m, m' = -M$

In all 6 cases, we have $M - m \geq M' - m'$.

$\square$

(b) Show that if $f$ is integrable on the interval $[a,b]$, then $|f|$ is also integrable on this interval.

Proof: Given a partition, $P: a = x_0 < x_1 < x_2 < x_3 < \cdots < x_n = b$.

For segment $k$, the difference between upper sum
and lower sum for $f$ is

$$ 
(M_k - m_k) \Delta _k \geq (M_k' - m_k') \Delta _k
$$

So we have $U(|f|, P) - L(|f|, P) \leq U(f, P) - L(f, P) < \epsilon$.

$\square$

(c) Provide the details for the argument that in this case we have $\left| \int_{a}^{b} f \right| \leq
\int_{a}^{b} |f|$.

Proof: $|f| - f \geq 0$, so $\int_{a}^{b}(|f| - f)
\geq 0$, so $\int_{a}^{b}|f| - \int_{a}^{b} f \geq 0$,
so $\int_{a}^{b} f \leq \int_{a}^{b}|f|$.

On the other hand, $f + |f| \geq 0$, so
so $\int_{a}^{b}(f + |f|) \geq 0$,
so $\int_{a}^{b} f \geq -\int_{a}^{b}|f|$.

Together, we have
$\left| \int_{a}^{b} f \right| \leq
\int_{a}^{b} |f|$.

$\square$

### 7.4.2.

(a) Let $g(x) = x^3$, and classify each of the following as positive, negative, or zero.

(i) $\int_{0}^{-1}g + \int_{0}^{1} g$

Solution: 

$\int_{0}^{-1}g$ = $-\int_{-1}^{0}g > 0$, so overall
it's positive.

(ii) $\int_{1}^{0}g + \int_{0}^{1} g$

**Solution**:

$\int_{1}^{0}g = - \int_{0}^{1} g$, so it's 0.

(iii) $\int_{1}^{-2}g + \int_{0}^{1} g$

**Solution**:

$$ 
\int_{1}^{-2}g + \int_{0}^{1} g =
- (\int_{-2}^{1}g - \int_{0}^{1} g) = \\
- \int_{-2}^{0} g > 0
$$

$\square$

(b) Show that if $b ≤ a ≤ c$ and f is integrable on the interval $[b,c]$, then it is the case

$$ 
\int_{a}^{b} f = \int_{a}^{c} f + \int_{c}^{b} f
$$

**Proof**:

We have

$$ 
\int_{b}^{c} f = \int_{b}^{a} f + \int_{a}^{c} f
$$ 

So

$$ 
- \int_{c}^{b} f = - \int_{a}^{b} f + \int_{a}^{c} f
$$

So 

$$ 
\int_{a}^{b} f = \int_{a}^{c} f + \int_{c}^{b} f
$$

$\square$

### 7.4.3.

Decide which of the following conjectures is true and supply a short proof. For those that are not true, give a counterexample.

(a) If $|f|$ is integrable on $[a,b]$, then $f$ is also integrable on this set.

Solution: False. Consdier $f$ defined on $[0,1]$ 

$$ 
f(x) = \begin{cases}
    -1 &\text{if } x \in \mathbf{Q}\\
    1  &\text{if } x \in \mathbf{I}\\
\end{cases} 
$$

$\square$

(b) Assume $g$ is integrable and $g(x) ≥ 0$ on $[a,b]$. If $g(x) > 0$ for an infinite number of points
$x ∈ [a,b]$, then $\int_{a}^{b}f > 0$.

**Solution**: False. Consider Thomae function.

(c) If $g$ is continuous on $[a,b]$ and $g(x) ≥ 0$ with
$g(y_0) > 0$ for at least one point $y_0 ∈ [a,b]$, then $\int_{a}^{b}f > 0$.

**Proof**: Since $g$ is continuous, we can find a closed
interval $y_0 \in [c, d] \subseteq [a,b]$ such that
$f(x) > \epsilon$ for $[c, d]$. Then

$$ 
\int_{a}^{b} f = \int_{a}^{c} f +
\int_{c}^{d} f + \int_{d}^{b} f
\geq 0 + \epsilon (d-c) + 0 > 0.
$$

$\square$

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

(a) If $f$ satisfies $|f(x)| ≤ M$ on $[a,b]$, show


$$ 
\left| 
(f(x))^2 - (f(y))^2
\right|
\leq
2M \left| f(x) - f(y) \right|
$$

Proof:

$$ 
\left| 
(f(x))^2 - (f(y))^2
\right|
= \\
\left| f(x) + f(y) \right| 
\left| f(x) - f(y) \right|
\leq (|f(x)| + |f(y)|) \left| f(x) - f(y) \right| \\
\leq 2M \left| f(x) - f(y) \right|
$$

$\square$

(b) Prove that if $f$ is integrable on $[a,b]$, then so is $f^2$.

**Proof**:

Consider the partial sum $M_k - m_k$ for $f$.
For any $x, y \in [x_k, x_{k+1}]$

$$ 
(f(x) - f(y)) ^ 2 \leq
2M \left| f(x) - f(y) \right| < 2M (M_{f,k} - m_{f,k})
$$

So $U(f^2, P) - L(f^2, P) \leq 2M U(f, P) - L(f, P)$.
Then $f^2$ is also integrable.

$\square$

(c) Now show that if $f$ and $g$ are integrable, then $fg$ is integrable. (Consider $(f+g)^2$.)

**Proof**:

$$ 
fg = \frac{1}{2} ((f+g)^2 - f^2 - g^2)
$$

All functions on the right side are integrable.
The sum of them is integrable.

$\square$

### 7.4.7.

Review the discussion immediately preceding Theorem 7.4.4.

(a) Produce an example of a sequence
$(f_n) \rightarrow 0$ pointwise on [0,1] where
$\lim_{n \to \infty} \int_{0}^{1}f_n$ does not exist.

**Solution**:

Consider

$$ 
f_n(x) = \begin{cases}
    n^2 &\text{if } 0 \leq x \leq \frac{1}{n}\\
    0 &\text{if } x > \frac{1}{n^2} \\
\end{cases} 
$$

So we have

$$ 
\int_{0}^{1} f_n = n
$$

$\square$

(b) Produce an example of a sequence $g_n$ with $\int_{0}^{1}g_n \rightarrow 0$ but $g_n$ does not converge to zero for any $x \in [0,1]$.
To make it more interesting, let’s insist
that $g_n(x) ≥ 0$ for all $x$ and $n$.

**Solution**:

I borrowed the idea from exercise 6.4.2 (c)
Consdier

$$ 
f_1(x) = 1 \\
f_2(x) = \begin{cases}
    1 &\text{if } x < \frac{1}{2}\\
    0 &\text{if } x \geq \frac{1}{2}\\
\end{cases} \\
f_3(x) = \begin{cases}
    0 &\text{if } x < \frac{1}{2}\\
    1 &\text{if } x \geq \frac{1}{2}\\
\end{cases} \\
f_4(x) = \begin{cases}
    1 &\text{if } \frac{0}{4} < x < \frac{1}{4}\\
    0 &\text{otherwise} \\
\end{cases} \\
f_5(x) = \begin{cases}
    1 &\text{if } \frac{1}{4} < x < \frac{2}{4}\\
    0 &\text{otherwise} \\
\end{cases} \\
f_6(x) = \begin{cases}
    1 &\text{if } \frac{2}{4} < x < \frac{3}{4}\\
    0 &\text{otherwise} \\
\end{cases} \\
f_7(x) = \begin{cases}
    1 &\text{if } \frac{3}{4} < x < \frac{4}{4}\\
    0 &\text{otherwise} \\
\end{cases} \\
\cdots 
$$

$\square$

### 7.4.8.

For each $n \in \mathbf{N}$, let

$$ 
h_n(x) = \begin{cases}
    1/2^n &\text{if } 1/2^n < x \leq 1\\
    0 &\text{if } 0 \leq x \leq 1/2^n\\
\end{cases} 
$$

And set $H(x) = \sum_{n = 1}^{\infty} h_n(x)$.
Show $H$ is integrable and compute $\int_{0}^{1} H$.

**Solution**: Because each $h_n(x)$ is increasing, $H(x)$ is also
increasing. $H(x)$ is bounded since $H(x) \leq 1$.
So $H$ is integrable.

Consider

$$ 
H_k(x) = \sum_{n = 1}^{k} h_n(x)
$$

Note that $H_k(x)$ converges uniformly to $H(x)$ and

$$ 
\int_{0}^{1} H_k(x) = \frac{1}{2} (1 - \frac{1}{2})
+ \frac{1}{4} (1 - \frac{1}{4}) + \cdots +
\frac{1}{2^k} (1 - \frac{1}{2^k}) \\
= \sum_{n = 1}^{k} \frac{1}{2^k} - \sum_{n = 1}^{k} \frac{1}{2^{2k}}
$$

So $\lim_{n \to \infty} H_k(x) = 1 - \frac{1/4}{1 - 1/4} = 2/3$.

$\square$

### 7.4.9.

Let $g_n$ and $g$ be uniformly bounded on $[0,1]$, meaning that
there exists a single $M > 0$ satisfying
$|g(x)| ≤ M$ and $|g_n(x)| ≤ M$ for all $n ∈ \mathbf{N}$ and $x ∈ [0,1]$.

Assume $g_n → g$ pointwise on $[0,1]$ and uniformly on any set of
the form $[0,α]$, where $0 < α < 1$.

If all the functions are integrable, show that

$$ 
\lim_{n \to \infty} \int_{0}^{1} g_n
= \int_{0}^{1} g
$$

**Proof**:

Given $\epsilon$, we want to find $N$ such that
if $n > N$ then

$$ 
\left| \int_{0}^{1} g_n - \int_{0}^{1} g \right| 
< \epsilon
$$

Since $g_n$ and $g$ be uniformly bounded on $[0,1]$,
we can have a $M$.

Given this $M$, we can find $\alpha$, such that
$(1 - \alpha ) M < \epsilon / 3$.

Then

$$ 
\left| \int_{0}^{1} g_n - \int_{0}^{1} g \right|
< \left| \int_{0}^{1} g_n - \int_{0}^{\alpha} g_n \right| +
\left| \int_{0}^{\alpha} g_n - \int_{0}^{\alpha} g \right| +
\left| \int_{0}^{1} g_n - \int_{0}^{\alpha} g_n \right| \\
= \left| \int_{\alpha}^{1} g_n \right| +
\left| \int_{0}^{\alpha} g_n - \int_{0}^{\alpha} g \right| + \left| \int_{\alpha}^{1} g \right| \\
\int_{\alpha}^{1} |g_n| +
\left| \int_{0}^{\alpha} g_n - \int_{0}^{\alpha} g \right| +
\int_{\alpha}^{1} |g| \leq
(1 - \alpha ) M +
\left| \int_{0}^{\alpha} g_n - \int_{0}^{\alpha} g \right| + (1 - \alpha ) M \\
2 / 3 \epsilon +
\left| \int_{0}^{\alpha} g_n - \int_{0}^{\alpha} g \right|
$$

Since $g_n → g$ uniformly on any set of
the form $[0,α]$, we can find $N$ such that
if $n > N$ then

$$ 
\left| \int_{0}^{\alpha} g_n - \int_{0}^{\alpha} g \right| < \epsilon / 3
$$

So

$$ 
\left| \int_{0}^{1} g_n - \int_{0}^{1} g \right|
< \epsilon 
$$

$\square$

### 7.4.10.

Assume $g$ is integrable on $[0,1]$ and continuous at $0$. Show

$$ 
\lim_{n \to \infty}
\int_{0}^{1} g(x^n) dx = g(0)
$$

**Proof**: We want to find $N$ such that
if $n > N$ then

$$ 
\left| \int_{0}^{1} g(x^n) dx - g(0) \right|
< \epsilon
$$

We use the technique in theorem 7.5.1

$$ 
\left| \int_{0}^{1} g(x^n) dx - g(0) \right|
= \\
\left| \int_{0}^{1} g(x^n) dx - 
\int_{0}^{1} g(0) dx \right| =
\left| 
\int_{0}^{1} (g(x^n) - g(0))dx
\right|
$$

Since $g$ is integrable, $g$ is bounded, i.e.
$\left| g(x) \right| \leq M$. 
Then we can find $c \in [0, 1]$, such that
$2M(1-c) < \epsilon /2$.

Fix this $c$. Next, since $g$ is continuous at $0$,
we can find $U_{\delta}(0)$ such that
$x \in U_{\delta}(0)$, $|g(x) - g(0)| < \epsilon / 2$.

Then we can find $N$ such that if $n > N, x \in [0,c]$, $x^n \in U_{\delta}(0)$.

So 

$$ 
\left| 
\int_{0}^{1} (g(x^n) - g(0))dx
\right| \leq
\int_{0}^{1}
\left| g(x^n) - g(0) \right| dx \\
= \int_{0}^{c} \left| g(x^n) - g(0) \right| dx
+ \int_{c}^{1} \left| g(x^n) - g(0) \right| dx \\
< \epsilon / 2 c + 2M(1-c)
< \epsilon / 2 + \epsilon / 2= \epsilon
$$

$\square$

### 7.4.11.

Review the original definition of integrability in Section 7.2,
and in particular the definition of the upper integral $U(f)$. One reasonable sug-
gestion might be to bypass the complications introduced in Definition 7.2.7 and
simply define the integral to be the value of $U(f)$. Then every bounded function
is integrable! Although tempting, proceeding in this way has some significant
drawbacks. Show by example that several of the properties in Theorem 7.4.2 no
longer hold if we replace our current definition of integrability with the proposal
that $\int_{a}^{b} f= U(f)$ for every bounded function $f$.

**Solution**:

(i) Let $f(x)$ is Thomae function and $g(x)$ be
the negative Thomae function.

$$ 
U(f) = 1, U(g) = 0
$$

So $U(f) + U(g) = 1$, but $U(f+g) = 0$.

$\square$

I think (ii), (iii), (iv), (v) holds.

$\square$

## 7.5 The Fundamental Theorem of Calculus

### 7.5.1.

(a) Let $f(x) = |x|$ and define $F(x) = \int_{-1}^{x} f$.
Find a piecewise algebraic formula for $F(x)$ 
for $F(x)$ for all $x$. Where is $F$ continuous?
Where is $F$ diﬀerentiable? Where does $F'(x) = f(x)$?

**Solution**:

$$ 
F(x) = \begin{cases}
    -\frac{1}{2} x^2 + \frac{1}{2} &\text{if } -1 \leq x \leq 0 \\
    \frac{1}{2} x^2 + \frac{1}{2} &\text{if } x > 0 \\
\end{cases} 
$$

$F(x)$ is continuous for $[-1, +\infty )$. It is differentiable
on this interval. Also $F'(x) = f(x)$.

(b) Repeat part (a) for the function

$$ 
f(x) = \begin{cases}
    1 &\text{if } x < 0\\
    2 &\text{if } x \geq 0\\
\end{cases} 
$$

**Solution**:

$$ 
F(x) =
\begin{cases}
    x &\text{if } -1 \leq x \leq 0\\
    2x &\text{if } x > 0\\
\end{cases} 
$$

$F(x)$ is continuous for $[-1, +\infty )$. It's not differentiable
at $0$. Also $F'(x) = f(x)$ when $x \not = 0$.

$\square$

### 7.5.2.

Decide whether each statement is true or false, providing a
short justification for each conclusion.

(a) If $g= h'$ for some $h$ on $[a,b]$, then $g$ is continuous on $[a,b]$.

**Solution**:

Consider

$$ 
h(x) = \begin{cases}
    0 &\text{if } x = 0\\
    x^{1.5}\sin \frac{1}{x} &\text{if } 0 < x \leq 1\\
\end{cases} 
$$

$$
g(0) = \lim_{x \to 0} 
\frac{x^a \sin (1/x)}{x}
= \lim_{x \to 0}  x^{a-1} \sin (1/x) = 0 \\
g(c) = ac^{a-1} \sin(1/c) - c^{a-2} \cos (1/c)
$$

$g$ is not continuous at $0$.

(b) If $g$ is continuous on $[a,b]$, then $g= h'$ for some $h$
on $[a,b]$.

**Proof**: This is true.

$g$ is continuous, so it's integrable. Then consider
$G(x) = \int_{a}^{x} g(x)$. Since $g$ is continuous,
$G'(x) = g(x)$.

$\square$

(c) If $H(x) = \int_{a}^{x} h$ is diﬀerentiable at $c ∈ [a,b]$, then $h$ is continuous at $c$.

**Solution**: false.

Consider $h(x)$ defined on $[0,2]$.

$$ 
h(x) = \begin{cases}
    0 &\text{if } x \not = 1\\
    1 &\text{if } x = 1\\
\end{cases}
$$

Then $H(x) = 0$ is differentiable at $c = 0$, but $h(x)$ is
not continuous at $0$.

$\square$

### 7.5.3.

The hypothesis in Theorem 7.5.1 (i) that $F'(x) = f(x)$ for all
$x ∈ [a,b]$ is slightly stronger than it needs to be. Carefully read the proof and
state exactly what needs to be assumed with regard to the relationship between
$f$ and $F$ for the proof to be valid.

**Solution**: $F'(x) = f(x)$ for all $(a, b)$ is enough.

$\square$

### 7.5.4.

Show that if $f : [a,b] → \mathbf{R}$ is continuous and
$\int_{a}^{x} f = 0$ for all
$x ∈ [a,b]$, then $f(x) = 0$ everywhere on $[a,b]$. Provide an example to show that
this conclusion does not follow if f is not continuous.

**Proof**: For theorem 7.5.1, $f$ is integrable and continuous,
then $F(x) = \int_{a}^{x}f$ and $F'(x) = f(x)$.
Since $F(x) = 0$, so $F'(x) = 0$ for $x \in [a, b]$, then
$f(x) = 0$ for $x \in [a, b]$.

$\square$

### 7.5.5.

The Fundamental Theorem of Calculus can be used to supply
a shorter argument for Theorem 6.3.1 under the additional assumption that the sequence of derivatives is continuous

Assume $f_n → f$ pointwise and $f'_n → g$ uniformly on $[a,b]$. Assuming each $f'_n$ is continuous, we can apply Theorem 7.5.1 (i) to get

$$ 
\int_{a}^{x} f_n' = f_n(x) - f_n(a)
$$

for all $x ∈ [a,b]$. Show that $g(x) = f'(x)$.

**Proof**:

Since $f'_n → g$ and $f'_n$ is continuous, then $g$ is continuous.
So $g$ is integrable. Furthermore

$$ 
\int_{a}^{x} g(x) = \lim_{n \to \infty}
\int_{a}^{x} f_n'(x)
$$

On the left side

$$ 
G(x) = \int_{a}^{x} g(x) \text{ and }
G'(x) = g(x)
$$

On the right side

$$ 
\lim_{n \to \infty}
\int_{a}^{x} f_n'(x) = \lim_{n \to \infty} f_n(x) - f_n(a)\\
 = f(x) - f(a)
$$

So $G(x) = f(x) - f(a)$, so $g(x) = f'(x)$.

$\square$

### 7.5.6 (Integration-by-parts).

(a) Assume $h(x)$ and $k(x)$ have continuous derivatives on
$[a,b]$ and derive the familiar integration-by-parts
formula

$$ 
\int_{a}^{b} h(t) k'(t) dt
= h(b) k(b) - h(a) k (a)
- \int_{a}^{b} h'(t) k(t) dt .
$$

Proof:

Since $h(x)$ and $k(x)$ have continuous derivatives on
$[a,b]$, so does $h(x)k(x)$. And its derivative at
$t \in [a, b]$  is

$$ 
h(t)k'(t) + h'(t)k(t)
$$

In addition, since $h(x), k(x), h'(x), k'(x)$ are all
continuous, then $h(t)k'(t), h'(t)k(t)$ are both
integrable. 

So we can directly apply Theorem 7.5.1 to get

$$
\int_{a}^{b} (h(t)k'(t) + h'(t)k(t)) dt
=
h(b) k(b) - h(a) k (a)
$$

Using theorem 7.4.2 (i) and rearrange it, we can prove it.

(b) Explain how the result in Exercise 7.4.6 can be used to slightly weaken the hypothesis in part (a).

Solution: exercise 7.4.6 states it is true that the product of integrable functions is integrable.

So we just need to assume $h'(x), k'(x)$ are both integrable.
Then the argument in (a) still holds.

$\square$

### 7.5.7.

Use part (ii) of Theorem 7.5.1 to construct another proof of
part (i) of Theorem 7.5.1 under the stronger hypothesis that
$f$ is continuous.
(To get started, set $G(x) = \int_{a}^{x}f$.)

Proof: $f$ is continuous, then $G'(x) = f(x)$.
If $F'(x) = f(x)$, then $(F(x) - G(x))' = 0$ for $x \in [a, b]$.
That means $F(x) = G(x) + C$.

$F(b) - F(a) = G(b) - G(a) = \int_{a}^{b}f(x) - \int_{a}^{a}f(x)$.

$\square$

### 7.5.8 (Natural Logarithm and Euler’s Constant).

Let

$$ 
L(x) = \int_{1}^{x} \frac{1}{t} dt
$$

where we consider only $x > 0$.

(a) What is $L(1)$?
Explain why $L$ is diﬀerentiable and find $L'(x)$.

**Solution**: $L(1) = 0$. This is because $\frac{1}{t}$ is
continuous.

$\square$

(b) Show that $L(xy) = L(x)+L(y)$. (Think of $y$ as a constant and diﬀerentiate $g(x) = L(xy).$)

**Proof**:

$$ 
L(xy) = \int_{1}^{xy} \frac{1}{t} dt \\
L'(xy) = yL'(xy) = y \frac{1}{xy} = \frac{1}{x} = L'(x)
$$

So $L(xy) = L(x) + C$ and plug $x = 1$, so $L(y) = C$.
So $L(xy) = L(x) + L(y)$.

$\square$

(c) Show $L(x/y) = L(x)−L(y)$.

Proof:

$$ 
L'(1/x) = x \cdot (- \frac{1}{x^2}) = - \frac{1}{x} = -L'(x) \\
L(x) + L(1/x) = C
$$

plug $x = 1$, so $C = L(1) + L(1) = 0$.
So $L(1/x) = -L(x)$.

Then with (b), we proved.

(d) Let

$$ 
\gamma _n = (1 + \frac{1}{2} + \frac{1}{3} +
\cdots + \frac{1}{n}) - L(n)
$$

Prove that $(γ_n)$ converges. The constant $γ = \lim γ_n$ is called Euler’s constant.

**Proof**:

For $n > m$, consdier

$$ 
γ_n - γ_m = \frac{1}{m+1} + \cdots + \frac{1}{n}
- \int_{m}^{n} \frac{1}{t} dt
$$

Then note

$$ 
\int_{m}^{n} \frac{1}{t} dt \geq
\frac{1}{m+1} \cdot 1 + \cdots + \frac{1}{n} \cdot 1 \\
\int_{m}^{n} \frac{1}{t} dt \leq
\frac{1}{m} \cdot 1 + \cdots + \frac{1}{n-1} \cdot 1 \\
$$

So

$$ 
|γ_n - γ_m| \leq \frac{1}{m} - \frac{1}{n} < \frac{1}{m}
$$

So it's Cauchy sequence.

$\square$

(d) Show how consideration of the sequence $γ_{2n}−γ_n$ leads to the interesting identity

$$ 
L(2) = 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \cdots
$$

**Proof**:

$$ 
γ_{2n}−γ_n = 1 + \frac{1}{2} + \cdots + \frac{1}{2n} - L(2n)
- (1 + \frac{1}{2} + \cdots + \frac{1}{n} - L(n)) \\
= 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \cdots -
\frac{1}{2n} - L(2)
$$

Since $(γ_n)$ converges, then $\lim_{n \to \infty} γ_{2n} - γ_n = 0$,

Then we proved.

$\square$

### 7.5.9.

Given a function $f$ on $[a,b]$, define the total variation of $f$
to be

$$ 
Vf = \sup
\{
    \sum_{k = 1}^{n}
\left| f(x_k) - f(x_{k-1}) \right| 
\}
$$

where the supremum is taken over all partitions $P$ of $[a,b]$.

(a) If $f$ is continuously diﬀerentiable ($f'$ exists as a continuous function), use Fundamental Theorem of Calculus to show
$Vf \leq \int_{a}^{b} |f'|$.

**Proof**: $f'$ is integrable. So from theorem 7.5.1 (i), we know
$f(x_k) - f(x_{k-1}) = \int_{x_{k-1}}^{x_k} f'(x)$.

So

$$
\sum_{k = 1}^{n}
\left| f(x_k) - f(x_{k-1}) \right| =
\sum_{k = 1}^{n}
\left| \int_{x_{k-1}}^{x_k} f'(x) \right| \\
\leq \sum_{k = 1}^{n}
\int_{x_{k-1}}^{x_k} |f'(x)| \\
= \int_{a}^{b} |f'(x)|
$$

So $Vf \leq \int_{a}^{b} |f'|$

$\square$

(b) Use the Mean Value Theorem to establish the reverse inequality and conclude that $Vf = \int_{a}^{b} |f'|$.

**Proof**:

$$ 
\sum_{k = 1}^{n}
\left| f(x_k) - f(x_{k-1}) \right| =
\sum_{k = 1}^{n}
|f'(x_{k, c})(x_k - x_{k-1})| \geq L(|f|, P)
$$

So $Vf \geq L(|f|) = \int_{a}^{b} |f'(x)|$.

$\square$

### 7.5.10 (Change-of-variable Formula).

Let $g : [a,b] → \mathbf{R}$ be differentiable and assume
$g'$ is continuous.
Let $f : [c,d] → \mathbf{R}$ be continuous, and
assume that the range of $g$ is contained in $[c,d]$ so that the composition $f◦g$ is properly defined.

(a) Why are we sure $f$ is the derivative of some function? How about $(f◦g)g'$?

**Proof**: $f$ is continuous, so from Theorem 7.5.1 (ii) we know
if $F(x) = \int_{c}^{x}f(x)$, then $f(x) = F'(x)$.

So consider the composite function $F◦g$,

$$ 
(F◦g)'(x) = F'(g(x)) \cdot g'(x) = f(g(x)) \cdot g'(x)
$$

So $(f◦g)g'$ is the derivative of $F◦g$.

$\square$

(b) Prove the change-of-variable formula

$$ 
\int_{a}^{b} f(g(x)) g'(x) dx = 
\int_{g(a)}^{g(b)} f(t) dt
$$

**Proof**:

Since $f$ is continuous, then $f$ is integrable.
Furthermore $F'(x) = f(x)$. Then

$$ 
\int_{g(a)}^{g(b)} f(t) dt = F(g(b)) - F(g(a))
$$

For the left side, $f(g(x))$ is continuous and $g'(x)$ is
continuous, so $f(g(x)) g'(x)$ is integrable, and
$(F◦g)' = (f◦g)g'$. So

$$ 
\int_{a}^{b} f(g(x)) g'(x) dx = F(g(b)) - F(g(a))
$$

$\square$

### 7.5.11.

Assume $f$ is integrable on [a,b] and has a “jump discontinu-
ity” at $c ∈ (a,b)$. This means that both one-sided limits exist as $x$ approaches
$c$ from the left and from the right, but that

$$ 
\lim_{x \to c^-} f(x) \not =
\lim_{x \to c^+} f(x)
$$

(This phenomenon is discussed in more detail in Section 4.6.)

(a) Show that in this case, $F(x) = \int_{a}^{x}f(x)$ is not diﬀerentiable at $x = c$.

**Proof**: Assume

$$ 
\lim_{x \to c^-} f(x) = a < b = \lim_{x \to c^+} f(x)
$$

We following the proof of Theorem 7.5.1 (ii), assume $x < c$
and given $\epsilon$, we can find $(c-\delta, c)$
if $x \in (c-\delta, c)$, then
$$
\left| 
\frac{
F(c) - F(x)
}{c - x} - a
\right| 
= \frac{1}{c - x} |\int_{x}^{c} f(x) - a| \\
\leq \frac{1}{c - x} \int_{x}^{c} |f(x) - a|
<\epsilon 
$$

That means

$$ 
\lim_{x \to c^-}
\frac{
F(c) - F(x)
}{c - x} = a
$$

$\square$

(b) The discussionin Section 5.5 mentions the existence of a continuous monotone function that fails to be diﬀerentiable on a dense subset of R. Combine the results of part (a) with Exercise 6.4.10 to show how to construct such a function.

**Solution**: In 6.4.10, we define this function.

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

Since $h(x)$ is bounded and monotone increasing, then
it is integrable. Let

$$ 
H(x) = \int_{0}^{x} h(x)
$$

Since $h(x) \geq 0$, then $H(x)$ is monotone increasing.
From theorem 7.5.1 (ii), we know $H(x)$ is continuous.

$\lim_{x \to r_n^-} h(x)$ and $\lim_{x \to r_n^-} h(x)$
exist.

Since from any $r_n$, $\lim_{x \to r_n^-} h(x) < \lim_{x \to r_n^+} h(x)$, then based on (a), $H(x)$ is not differentiable
at all $r_n$ which is $\mathbf{Q}$, which is dense in $\mathbf{R}$.

$\square$

## 7.6 Lebesgue’s Criterion for Riemann Integrability

### Riemann-integrable Functions with Infinite Discontinuities

Recall from Section 4.1 that Thomae’s function

$$ 
t(x) = \begin{cases}
    1 &\text{if } x = 0 \\
    1/n &\text{if } x = m/n \in \mathbf{Q} \backslash \{0\} \\
    0 &\text{if } x \not\in \mathbf{Q} \\
\end{cases} 
$$

is continuous on the set of irrationals and has 
discontinuities at every rational
point. Let’s prove that Thomae’s function is 
integrable on $[0,1]$ with $\int_{0}^{1} t = 0$.

### Exercise 7.6.1.

(a) First, argue that $L(t,P) = 0$ for any partition 
$P$ of $[0,1]$.

Proof: this is because in every partition we can
find an irrational number.

(b) Consider the set of points
$D_{ϵ/2} = \{x : t(x) ≥ ϵ/2\}$. How big is $D_{ϵ/2}$.

**Solution**: Let $n$ be the biggest integer such
that $1/n \geq ϵ/2$. So the size of $D_{ϵ/2}$
is less than $\sum_{k=1}^{n}k = \frac{n(n+1)}{2}$.

$\square$

(c) To complete the argument, explain how to 
construct a partition $P_ϵ$ of $[0,1]$
so that $U(t,P_ϵ) < ϵ$.

**Proof**: We construct a partition such that
the point in $D_{ϵ/2}$ fall in an interval whose
length is less than $(ϵ/2)/(n(n+1)/2)$.

In those intervals, the partial sum is less than
$ϵ/2$. In other intervals, the partial sum is also
less than $ϵ/2$. So $U(t,P_ϵ) < ϵ$.

$\square$

### Exercise 7.6.2.

Define

$$ 
h(x) =
\begin{cases}
    1 &\text{if } x \in C\\
    0 &\text{if } x \not\in C\\
\end{cases} 
$$

Prove the following

(a) Show $h$ has discontinuities at each point of 
$C$ and is continuous at every point of the 
complement of $C$. Thus, $h$ is not continuous on an 
uncountably infinite set.

**Proof**: Assume $x \not\in C$, then assume
$x \in C_n$ but $x \not\in C_{n+1}$. Since only
open set was removed, $x$ is removed with an open
set. So $h(x)$ is continuous at $x$.

If $x \in C$, given any neighborhood of $V_{\epsilon}(x)$, we can find $n$ such that
$\frac{1}{3^n} < \epsilon$. Since the next step
will take out an open internal of
$\frac{1}{3^{n+1}}$. And this interval is
within $V_{\epsilon}(x)$, so its value is $1$.
$h(x)$ is not continuous at $x$.

$\square$

(b) Now prove that $h$ is integrable on [0,1].

**Proof**: Let $P_n$ be $C_n$.
The length of all the intervals containing $C$ is

$$ 
1 - \frac{1}{3} - \frac{2}{9} - \frac{4}{27} -
\cdots \frac{1}{3} (\frac{2}{3})^n \\
1 - \frac{1}{3} (1 + \frac{2}{3} + \cdots + (\frac{2}{3})^n) \\
1 - 3 (1 - (\frac{2}{3})^{n+1}) \\
3 \left( \frac{2}{3} \right)^{n+1}
$$

The upper sum of these intervals is
$3 \left( \frac{2}{3} \right)^{n+1}$, in other
intervals the upper sum is $0$.

So $\lim_{n \to \infty} U(h, P_n) = 0$.
so $h$ is integrable on [0,1].

$\square$

### Sets of Measure Zero

### Definition 7.6.1. Measure zero

A set $A ⊆ \mathbf{R}$ has *measure zero* if,
for all $ϵ > 0$, there exists a countable collection 
of open intervals $O_n$ with the property that $A$ 
is contained in the union of all of the intervals
$O_n$ and the sum of the lengths of all of the
intervals is less than or equal to $ϵ$.
More precisely, if $|O_n|$ refers to the length of
the interval $O_n$, then we have

$$ 
A \subseteq \bigcup_{n=1}^{\infty} O_n
\text{ and }
\sum_{n = 1}^{\infty} |O_n| \leq \epsilon
$$

### Example 7.6.2.

Consider a finite set $A= \{a_1,a_2,...,a_N\}$. To show that $A$ has measure zero, let $ϵ > 0$ be 
arbitrary. For each $1 ≤ n ≤ N$, construct the
interval

$$ 
G_n = \left( 
a_n - \frac{ϵ}{2N},
a_n + \frac{ϵ}{2N}
\right).
$$

Clearly, $A$ is contained in the union of these intervals, and

$$ 
\sum_{n = 1}^{N} |G_n| =
\sum_{n = 1}^{N} \frac{ϵ}{N} = \epsilon
$$

$\square$

### Exercise 7.6.3.

Show that any countable set has measure zero.

**Proof**: Given a countable set

$$ 
A = \{r_1, r_2, r_3, \cdots, r_n \cdots \}
$$

Consider

$$ 
G_n = \left( 
r_n - \frac{ϵ}{2^{n+1}},
r_n + \frac{ϵ}{2^{n+1}}
\right).
$$

$$ 
\sum_{n = 1}^{\infty} |G_n| =
\sum_{n = 1}^{\infty} \frac{ϵ}{2^n} = \epsilon
$$

$\square$

### Exercise 7.6.4.
Prove that the Cantor set has measure zero.

**Proof**:

$C_1$ can be coverd by 2 segments of $3/8$.
$C_2$ can be coverd by 4 segments of $1/8$.
$C_3$ can be coverd by 8 segments of $1/24$.
$C_n$ can be coverd by $\frac{3}{4} \cdot (\frac{2}{3})^{n-1}$ .
So the Cantor set has measure zero.

### Exercise 7.6.5.

Show that if two sets $A$ and $B$ each have measure 
zero, then $A∪B$ has measure zero as well. In 
addition, discuss the proof of the stronger
statement that the countable union of sets of 
measure zero also has measure zero. (This second 
statement is true, but a completely rigorous proof 
requires a result about double summations discussed 
in Section 2.8.)

**Proof**:

Let

$$ 
A = \{a_1, a_2, a_3, \cdots, a_n \cdots \}
\text{ and }
B = \{b_1, b_2, b_3, \cdots, b_n \cdots \}
$$

Let

$$ 
G_n = \left(
a_n - \frac{ϵ}{2^{n+2}},
a_n + \frac{ϵ}{2^{n+2}}
\right)
\text{ and }
H_n = \left(
b_n - \frac{ϵ}{2^{n+2}},
b_n + \frac{ϵ}{2^{n+2}}
\right).
$$

So

$$ 
\sum_{n = 1}^{\infty} |G_n| + |H_n| =
\sum_{n = 1}^{\infty}
\frac{ϵ}{2^{n+1}} + \frac{ϵ}{2^{n+1}}
=
\sum_{n = 1}^{\infty}
\frac{ϵ}{2^{n}}
= \epsilon
$$

Now consider we have $A_1, A_2, A_3, \cdots, A_n, \cdots$ countable sets. Each of them has countable
elements. We list them in double array

$$ 
\begin{matrix}
a_{11} & a_{12} & \cdots & a_{1n} & \cdots \\
a_{21} & a_{22} & \cdots & a_{2n} & \cdots \\
\vdots & \vdots & \ddots & \vdots & \cdots \\
a_{n1} & a_{n2} & \cdots & a_{nn} & \cdots \\
\vdots & \vdots & \ddots & \vdots & \cdots \\
\end{matrix}
$$

For each of them, we assign an open interval of
certain length listed as following

$$ 
\begin{matrix}
ϵ/4 & ϵ/8  & \cdots & ϵ/2^{n+1} & \cdots \\
ϵ/8 & ϵ/16 & \cdots & ϵ/2^{n+2} & \cdots \\
\vdots & \vdots & \ddots & \vdots & \cdots \\
ϵ/2^{n+1} & ϵ/2^{n+2} & \cdots & ϵ/2^{n+n} & \cdots \\
\vdots & \vdots & \ddots & \vdots & \cdots \\
\end{matrix}
$$

Then we can see

$$ 
\sum_{i = 1}^{\infty}
\sum_{j = 1}^{\infty}
|a_{ij}|
$$

converges. In fact, it converges to

$$ 
\sum_{i = 1}^{\infty}
\sum_{j = 1}^{\infty}
|a_{ij}| = ϵ
$$

Now if we have a countable of measure zero set,
each length is 

$$ 
\begin{matrix}
|O_{11}| & |O_{12}| & \cdots & |O_{1n}| & \cdots \\
|O_{21}| & |O_{22}| & \cdots & |O_{2n}| & \cdots \\
\vdots & \vdots & \ddots & \vdots & \cdots \\
|O_{n1}| & |O_{n2}| & \cdots & |O_{nn}| & \cdots \\
\vdots & \vdots & \ddots & \vdots & \cdots \\
\end{matrix}
$$

We can let 

$$ 
\sum_{j = 1}^{\infty} |O_{ij}| < \frac{\epsilon }{2^{i+1}}
$$

So

$$ 
\sum_{i = 1}^{\infty}
\sum_{j = 1}^{\infty}
|O_{ij}| < \epsilon
$$

$\square$

### α-Continuity

### Definition 7.6.3.

Let $f$ be defined on $[a,b]$, and let $α > 0$. The 
function $f$ is $α$-continuous at $x ∈ [a,b]$ if 
there exists $δ > 0$ such that for all
$y,z ∈ (x−δ,x+δ)$ it follows that $|f(y)−f(z)| < α$.

Let $f$ be a bounded function on $[a,b]$. For each
$α > 0$, define $D^α$ to be the set of points in
$[a,b]$ where the function $f$ fails to be 
$α$-continuous; that is,

$$ 
\tag{1}
D^α =
\{x \in [a,b] :
f \text{ is not } α-\text{continuous at } x.
\}
$$

### Exercise 7.6.6.

If $α < α'$, show that $D_f^{α'} ⊆ D_f^{α}$.

Proof: 
This is exercise 4.6.9.
If $x \in D_f^{α'}$, then given $\delta$, we can 
find $y, z \in V_{\delta}(x)$ such that $|f(y) - f(z)| > \alpha' > \alpha$. So $x \in D_f^{α}$. Then $D_f^{α'} ⊆ D_f^{α}$.

$\square$

* Now, let

$$ 
\tag{2}
D =
\{x \in [a,b] :
f \text{ is not continuous at } x.
\}
$$

### Exercise 7.6.7.

(a) Let $α > 0$ be given. Show that if $f$ is continuous at $x$, then it is $α$-continuous at $x$ as well. Explain how it follows that $D^α ⊆ D$.

**Proof**: This is exercise 4.6.10.

If $f$ is continuous at $x$, then we can find a $U_{\delta}(x) = (x−δ, x+δ)$ such that $|y-x| < \alpha /2$ and $|z-x| < \alpha /2$. Then $|y-z| < \alpha$. So $f$ is $α$-continuous at $x$ as well.

Then given $x \in D^{α}$, $f$ has to be discontinuous at $x$, so $x \in D$. Then $D^{α} ⊆ D$.

$\square$

(b) Show that if $f$ is not continuous at $x$, then $f$ is not $α$-continuous for some $α$ > 0. Now explain why this guarantees that

$$ 
D = \bigcup_{n = 1}^{\infty} D^{\alpha_n}
$$

where $α_n = 1/n$.

**Proof**: This is exercise 4.6.11.

If $f$ is not continuous at $x$, then exists $\epsilon$, given any $\delta$, we can find $y \in U_{\delta}(x)$ such that $|f(y)-f(x)| >= \epsilon$. So $f$
is not $\epsilon$-continuous at $x$. We can find
$n$ such that $1/n < \epsilon$.

According to 4.6.9, $x \in D^{\epsilon} ⊆ D^{1/n}$.
Then it follows:

$$ 
D = \bigcup_{n = 1}^{\infty} D^{\alpha_n}
$$

$\square$

### Exercise 7.6.8.

Prove that, for a fixed $α > 0$, the set $D^α$ is closed.

**Proof**: This is exercise 4.6.8.

Let $x$ be a limit point of $D^α$. Given any $\delta$, we can find $a \in U_{\delta}(x)$ such that $a \in D^α$, since $U_{\delta}(x)$ is open, we can find
$U_{\zeta}(a) \subset U_{\delta}(x)$. Since $a \in D^α$, we can find $y, z \in U_{\zeta}(a)$ with $|f(y) − f(z)| \ge α$. Since $y, z \in U_{\delta}(x)$, $x$ is also not
$α$-continuous.

$\square$

### uniformly α-continuous

For a fixed $α > 0$, a function $f : A → \mathbf{R}$ is uniformly 
$α$-continuous on $A$ if there exists a $δ > 0$ such that 
whenever $x$ and $y$ are points in $A$ satisfying
$|x− y| < δ$, it follows that $|f(x)− f(y)| < α$. By imitating 
the proof of Theorem 4.4.7, it is completely straight forward to 
show that if $f$ is $α$-continuous at every point on some compact 
set $K$, then $f$ is uniformly $α$-continuous on $K$.

### Compactness Revisited

### Theorem 7.6.4.

Let $K ⊆ R$. The following three statements are all equivalent,
in the sense that if any one is true, then so are the two others.

(i) Every sequence contained in $K$ has a convergent subsequence that converges to a limit in $K$.

(ii) $K$ is closed and bounded.

(iii) Given a collection of open intervals $\{G_λ : λ ∈ Λ\}$ that 
covers $K$ (that is, $K \subseteq \cup_{λ ∈ Λ} G_λ$
there exists a finite subcollection
$\{G_{λ_1}, G_{λ_2}, G_{λ_3}, \cdots, G_{λ_n}\}$
of the original set that also covers $K$.

### Lebesgue’s Theorem

### Theorem 7.6.5 (Lebesgue’s Theorem).

Let $f$ be a bounded function defined on the interval $[a,b]$. 
Then, $f$ is Riemann-integrable if and only if the set of
points where $f$ is not continuous has measure zero.

**Proof**. Let $M > 0$ satisfy $|f(x)| ≤ M$ for all $x ∈ [a,b]$, 
and let $D$ and $D^α$ be defined as in the preceding equations 
(1) and (2). Let’s first assume that $D$ has
measure zero and prove that our function is integrable.

$\Leftarrow$ Let $\epsilon > 0$ and set

$$ 
\alpha = \frac{\epsilon}{2(b-a)}
$$

### Exercise 7.6.9.

Show that there exists a finite collection of disjoint open
intervals ${G_1,G_2,...,G_N}$ whose union contains $D_α$ and that 
satisfies

$$ 
\sum_{n=1}^{N} |G_n| < \frac{\epsilon }{4M}
$$

**Proof**: Since $D$ is measure zero, we can find a countable
of open set $\{O_n\}$ such that $D \subseteq \cup O_n$.

Since $D^α \subseteq D$ and it's closed, so we can find
a finite number of $O_n$ such that
$D^α \subseteq \cup_{i=1}^{n} O_n$.
Then we can combine those open sets which have intersection.

$\square$

### Exercise 7.6.10.

Let $K$ be what remains of the interval $[a,b]$ after the open
intervals $G_n$ are all removed; that is,
$K = [a,b] \backslash \cup_{n=1}^N G_n$.
Argue that $f$ is uniformly $α$-continuous on $K$.

**Proof**: If $x$ is not $α$-continuous, then $x \in D^α$.
Then it's in one of $G_n$. So if $x \in K$, then
$x$ is $α$-continuous. Furthermore, $K$ is a finite union of
closed intervals, so it is uniformly $α$-continuous in each
of the intervals, then it has to be uniformly $α$-continuous.

$\square$

### Exercise 7.6.11.

Finish the proof in this direction by explaining how to
construct a partition $P_ϵ$ of $[a,b]$ such that
$U(f, P_ϵ) - L(f, P_ϵ) \leq \epsilon$.
It will be helpful to break the sum

$$ 
U(f, P_ϵ) - L(f, P_ϵ) =
\sum_{k=1}^{n} (M_k - m_k) \triangle x_k
$$

into two parts—one over those subintervals that contain points of 
$D^α$ and the other over subintervals that do not.

**Proof**: We use $G_k$ to do the partition.
In $G_k$, the partial sum is $2M \times \frac{\epsilon }{4M} = \epsilon / 2$.

In other intervals, the partial sum is less than
$α \times (b-a) = \epsilon / 2$.

In summary, the partial sum is less than $\epsilon / 2$.

$\square$

$\Rightarrow$

For the other direction, assume $f$ is Riemann-integrable. We 
must argue that the set $D$ of discontinuities of $f$ has measure 
zero.

Let $ϵ > 0$ be arbitrary, and fix $α > 0$. Because $f$ is 
Riemann-integrable, there exists a partition $P_ϵ$ of $[a,b]$ 
such that $U(f,P_ϵ)−L(f,P_ϵ) < αϵ$.

### Exercise 7.6.12.

(a) Prove that $D^α$ has measure zero. Point out that it is
possible to choose a cover for $D^α$ that consists of a finite number of open intervals.

**Proof**: We consider $P_ϵ$. For those intervals such that
$M_k - m_k \geq \alpha$, their total length should less than
$\epsilon$. Assume their total length is $\epsilon'$,
and $d = \epsilon - \epsilon'$. Assume there are only $N$ segments that satisfy $M_k - m_k \geq \alpha$.
We can use $2N$ open intervals with length $\frac{d}{4N}$.
So the total length is

$$ 
\epsilon' + 2N \cdot \frac{d}{4N} = \epsilon' + \frac{d}{2}
< \epsilon' + d = \epsilon.
$$

$\square$

(b) Show how this implies that $D$ has measure zero.

**Proof**: This is because $D$ is a countable union of
measure zero set.

$\square$

### Exercise 7.6.13.

(a) Show that if $f$ and $g$ are integrable on $[a,b]$, then so is
the product $fg$. (This result was requested in Exercise 7.4.6, 
but notice how much easier the argument is now.)

**Proof**: Consider $D_f$ and $D_g$ which are measure zero,
and $D_{fg} = D_f \cup D_g$.
So it is measure zero too.

Then $fg$ is integrable.

(b) Show that if $g$ is integrable on $[a,b]$ and $f$ is 
continuous on the range of $g$, then the composition $f◦g$ is 
integrable on $[a,b]$.

**Proof**: If $g$ is continuous at $x$, then $f◦g$ is also
continuous at $x$. So if $x \in D_{f◦g}$ then $x \in D_g$.
That is $D_{f◦g} \subseteq D_g$. Since $D_g$ is measure zero,
so is $D_{f◦g}$.

$\square$

### 7.6.14.

(a) Find $g'(0)$.

**Solution**:

$$ 
\lim_{x \to 0} \frac{
x^2 \sin \frac{1}{x} - 0
}{x - 0} = \lim_{x \to 0} x \sin \frac{1}{x} = 0
$$

$\square$

(b) Use the standard rules of diﬀerentiation to compute $g'(x)$ for $x \not = 0$.

$$ 
g'(x) = 2x \sin \frac{1}{x} - x^2 \cos \frac{1}{x} \frac{1}{x^2}\\
= 2x \sin \frac{1}{x} - \cos \frac{1}{x}
$$

$\square$

(c) Explain why, for every $δ > 0$, $g'(x)$ attains every value between $1$ and $−1$
as $x$ ranges over the set $(−δ,δ)$. Conclude that $g'$ is not continuous at $x = 0$.

**Proof:** Given $(−δ,δ)$, we can find $k$ such that

$$ 
-δ < -\frac{1}{2k \pi} < -\frac{1}{2 (k+1) \pi} < 0
< \frac{1}{2 (k+1) \pi} < \frac{1}{2k \pi} < δ
$$

Note

$$ 
g'(-\frac{1}{2k \pi}) = g'(\frac{1}{2k \pi}) = -1 \\
g'(-\frac{1}{2(k+1) \pi}) = g'(\frac{1}{2(k+1) \pi}) = 1 \\
$$

Since $g'(x)$ is continuous on $[\frac{1}{2 (k+1) \pi}, \frac{1}{2k \pi}]$, then because of the intermediate value property,
$g'(x)$ attains every value between $1$ and $−1$.

Since $g'(x) = 0$, $g'$ is not continuous at $x = 0$.

$\square$

### 7.6.15.

(a) If $c ∈ C$, what is $\lim_{n→∞} f_n(c)$?

**Solution**: In each $f_n$, $f_n(c) = 0$. So
$\lim_{n→∞} f_n(c) = 0$.

(b) Why does $\lim_{n→∞} f_n(x)$ exist for $x \not ∈ C$?

**Solution**: If $x \not \in C$, then there exists
$N$, if $n \geq N$, $x \not \in C_n$. Let $N$ be the smallest
integer such that $x \not \in C_N$.

It will be replaced by the $x^2 \sin \frac{1}{x}$ function
and won't be changed any more.

So $\lim_{n→∞} f_n(x)$ exists.

### 7.6.16.

(a) Explain why $f'(x)$ exists for all $x \not \in C$.

**Proof**: if $x \not \in C$, then we can assue it was taken
out during the interval $(a,b)$. On this interval,
it is either $g(x-a)$ or $g(-x + b)$ or in the splice part.
Wherever it is, it's differentiable.

$\square$

(b) If $c ∈ C$, argue that $|f(x)| ≤ (x− c)^2$ for all
$x ∈ [0,1]$. Show how this implies $f'(c) = 0$.

**Proof**: If $x \in C$, $f(x) = 0$. So it holds.

If $x \not \in C$, assume it is taken out with $(a, b)$.
Note that $a, b \in C$. So $(x-c)^2 \geq \max \{ (x-a)^2, (x-b)^2\}$. By our construction of $f(x)$, we know

$$ 
|f(x)|^2 \leq (x - a)^2 \text{ and } |f(x)|^2 \leq (-x + b)^2
$$

So the inequality also holds.

$$ 
\lim_{x \to c}  \left| 
\frac{f(x) - f(c)}{x - c} - 0
 \right| =\\
 \lim_{x \to c}
\left| 
\frac{f(x)}{x-c}
\right|
\leq 
\lim_{x \to c}
\left| 
\frac{(x-c)^2}{x-c}
\right| = 0
$$

So $f'(c) = 0$.

$\square$

(c) Give a careful argument for why $f'(x)$ fails to be continuous on $C$. Remember that $C$ contains many points besides the endpoints of the intervals
that make up $C1,C2,C3,...$.

**Proof**: Let $c ∈ C$. And given $U_{\delta}(c)$, it is possible
to find an open interval $(a, b) \subset U_{\delta}(c)$ and
$(a, b) \cap C = \emptyset$. Based on our construction of
$f$, $f'(x)$ can achieve any value in $[-1, 1]$ when $x \in (a, b)$. Since $f'(c) = 0$, $f'(x)$ cannot be continuous at $c$.

$\square$

### 7.6.17.

Why is $f'(x)$ Riemann-integrable on [0,1]?

**Proof**: This is because $f'(x)$ is continuous for
$x \not \in C$, and Cantor set is measure $0$.

$\square$

### 7.6.18.

Show that, under these circumstances, the sum of the lengths
of the intervals making up each $C_n$ no longer tends to zero as $n → ∞$. What is this limit?

**Proof**: The segment we take out is

$$ 
\sum_{n=1}^{\infty} 2^{n-1}
\left( \frac{1}{3^{n+1}} \right)
= \frac{1}{9} (1 + \frac{2}{3} + \frac{4}{9} + \cdots) = \frac{1}{3}
$$

$\square$

### 7.6.19.

As a final gesture, provide the example advertised in
Exercise 7.6.13 of an integrable function $f$ and a continuous function $g$ where the
composition $f ◦ g$ is properly defined but not integrable. Exercise 4.3.12 may be useful.

**Solution**: Consider $A$ is the set defined in 7.6.18,
$g$ is the function used in Exercise 4.3.12. Since $A$ is
a close set, $g$ is continuous. Let $f$ be this function
defined in $[0,1]$ :

$$ 
f(x) = \begin{cases}
    0 &\text{if } x = 0 \\
    \sin \frac{1}{x} &\text{if } x \not = 0 \\
\end{cases} 
$$

$f(x)$ is integrable because $f(x)$ is only discontinueous at $0$.

So let $h = f ◦ g$, $h(x) = 0$ if $x \in A$, because the
distance between $x$ and $A$ is $0$.

Furthermore, $h(x)$ is not continuous at $x \in A$.
Given $c \in A$ it is possible
to find an open interval $(a, b) \subset U_{\delta}(c)$ and
$(a, b) \cap C = \emptyset$, $a,b \in A$. $h(x)$ can achieve any value in $[-1, 1]$ when $x \in (a, b)$. Since $h(c) = 0$, $h(x)$ cannot be continuous at $c$.

$\square$
