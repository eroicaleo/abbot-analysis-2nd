# Chapter 08 Additional Topics

## 8.1 The Generalized Riemann Integral

### Exercise 8.1.1

Let $(P,{c_k})$ be an arbitrary tagged partition of $[a,b]$ that
is $δ$-fine, and let $P' = P ∪ P_ϵ$.

(a) Explain why both the Riemann sum $R(f,P)$ and $\int_{a}^{b}f$
fall between $L(f,P)$ and $U(f,P)$.

**Proof**: Since $\int_{a}^{b}f$ is an upper bound of $L(f,P)$
and a lower bound of $U(f,P)$, so $\int_{a}^{b}f$
fall between $L(f,P)$ and $U(f,P)$.

Since $m_k \leq c_k \leq M_k$, $R(f,P)$ also
fall between $L(f,P)$ and $U(f,P)$.

$\square$

(b) Explain why $U(f,P')−L(f,P') < ϵ/3$.

**Proof**:

Since $P' = P ∪ P_ϵ$, we have

$$ 
L(f, P_ϵ) \leq L(f, P') \leq U(f, P') \leq  U(f, P_ϵ)
$$

$\square$

### 8.1.2.

Explain why $U(f,P)−U(f,P') ≥ 0$.

**Proof**: See previous exercise.

### 8.1.3.

(a) In terms of $n$, what is the largest number of terms of the
form $M_k(x_k - x_{k-1})$ that could appear in one of $U(f,P)$ or $U(f,P')$ but not the other?

Solution: Note that $P \subseteq P' = P \cup P_{\epsilon }$, and
since $P_{\epsilon}$ has $n$ segments, so $P'$ has at most $n$ points more than $P$.

If these $n$ points fall into $n$ different
segments of $P$, then we can achive the
largest number of terms of the
form $M_k(x_k - x_{k-1})$ that appears in one of $U(f,P)$ or $U(f,P')$ but not the other, which is $3n$.

(b) Finish the proof in this direction by arguing that

$$ 
U(f, P) - U(f, P') < \epsilon / 3.
$$

Proof: Now we can bound

$$ 
U(f, P) - U(f, P') < 3n \cdot M \cdot \frac{\epsilon}{9nM}
= \epsilon / 3
$$

Combine the previous exercises, we have

$$ 
R(f, P), \int_{a}^{b}f \leq U(f, P) < U(f, P') + \epsilon / 3 \\
R(f, P), \int_{a}^{b}f \geq L(f, P) > L(f, P') - \epsilon / 3
$$

So $\left| R(f, P) - \int_{a}^{b} f \right| < \epsilon$.

$\square$

### 8.1.4.

(a) Show that if $f$ is continuous, then it is possible to pick tags
$\{c_k\}^n_{k=1}$
so that $R(f,P) = U(f,P)$.

**Proof**: Since $f$ is continuous, for each segment
$[x_{k-1}, x_k]$, because of extreme value theorem, it is possible to find $c_k$ such that
$f(x_k) = M_k$.
Pick those $c_k$, we have $R(f,P) = U(f,P)$.

(b) If $f$ is not continuous, it may not be possible to find tags for which $R(f,P) = U(f,P)$.
Show, however, that given an arbitrary $ϵ > 0$, it
is possible to pick tags for $P$ so that

$$ 
U(f,P) - R(f,P) < \epsilon.
$$

The analogous statement holds for lower sums.

**Proof**: For each segment $[x_{k-1}, x_k]$, $M_k$ is the
supremum of $f(x)$ for $x \in [x_{k-1}, x_k]$. So we can find
$c_k$ such that $M_k - c_k < \epsilon / (b-a)$.

Pick those $c_k$, we have $U(f,P) - R(f,P) < \epsilon$.

$\square$

### 8.1.5.

Use the results of the previous exercise to finish the proof of Theorem 8.1.2.

**Proof**: Given $\epsilon$, we can find partition $\delta$,
such that any $\delta$-fine tagged partition $|R(f, P) - A| < \epsilon /4$.
 $P$, such
that $U(f,P) - R_1(f,P) < \epsilon / 4$. Similarly,
$R_2(f,P) - L(f,P) < \epsilon / 4$.

Let $P_{\epsilon} = P_1 \cup P_2$, so

$$ 
U(f, P) - L (f, P)
= U(f, P) - R_1(f,P) + R_1(f,P) - A + A - R_2(f,P) + R_2(f,P) - L (f, P) \\
< \epsilon / 4 + \epsilon / 4 + \epsilon / 4 + \epsilon / 4
< \epsilon
$$

$\square$

**Gauges and δ(x)-fine Partitions**

### Definition 8.1.3.

A function $δ : [a,b] → \mathbf{R}$ is called a gauge on $[a,b]$ if $δ(x) > 0$ for all $x ∈ [a,b]$.

### Definition 8.1.4.

Given a particular gauge $δ(x)$, a tagged partition
$(P, {c_k}_{k=1}^n)$ is $\delta(x)$-fine if every subinterval
$[x_{k−1},x_k]$ satisfies $x_k - x_{k−1} < \delta(c_k)$.

In other words, each subinterval $[x_{k−1},x_k]$ has width less 
than $\delta(c_k)$.

### 8.1.6.

Consider the interval [0,1].

(a) If $\delta(x) = 1/9$, find a $\delta(x)$-fine tagged partition of $[0,1]$. Does the choice of tags matter in this case?

**Solution**:

Let $P = \{0, 0.1, 0.2, \cdots, 0.9, 1.0\}$.
The choice of tags does not matter.

$\square$

(b) Let

$$ 
\delta (x) = \begin{cases}
    1/4 &\text{if } x = 0\\
    x/3 &\text{if } 0 < x \leq 1\\
\end{cases} 
$$

Construct a $δ(x)$-fine tagged partition of $[0,1]$.

**Solution**:

Let $x_0 = 0, x_1 = 1, c_1 = 0$.

$\square$

### Theorem 8.1.5.

Given a gauge $δ(x)$ on an interval $[a,b]$, there exists a tagged
partition $(P,\{c_k\}^n_{k=1})$ that is $δ(x)$-fine.

**Proof**. Let $I_0 = [a,b]$. It may be possible to find a tag such that the trivial partition
$P= \{a,b\}$ works.

Specifically, if $b−a < δ(x)$ for some $x ∈ [a,b]$, then
we can set $c_1$ equal to such an $x$ and notice that
$(P,{c_1})$ is $δ(x)$-fine. If no
such $x$ exists, then bisect $[a,b]$ into two equal halves.

### Exercise 8.1.7.

Finish the proof of Theorem 8.1.5.

**Proof**: Assume otherwise, then this process continuous
indefinitely, then we get a nested intervals.
Because of NIP, we can find $c$ in all these intervals.
That means $\delta (c) \geq b_n - a_n$ for all $n$.
But
$\lim_{n \to \infty} b_n - a_n =
\lim_{n \to \infty}\frac{b-a}{2^n} = 0
$
So we have a contradiction.

$\square$

### Definition 8.1.6.

A function $f$ on $[a,b]$ has generalized Riemann integral $A$
if, for every $ϵ > 0$, there exists a gauge $δ(x)$ on $[a,b]$ such that for each tagged partition $(P,\{c_k\}^n_{k=1})$ that is
$δ(x)$-fine, it is true that

$$ 
|R(f,P)−A| < ϵ
$$

In this case, we write $A = \int_{a}^{b}f$.

### Theorem 8.1.7.

If a function has a generalized Riemann integral, then the
value of the integral is unique.

### Exercise 8.1.8.

Finish the argument.

**Proof**: Assume that a function $f$ has generalized Riemann 
integral $A1$ and that
it also has generalized Riemann integral $A2$.
We must prove $A1 = A2$.

Since $f$ is generalized Riemann integrable, given $\epsilon$, we
can find $\delta_1(x)$, such that if a tagged partition $P_1$ is 
$\delta_1(x)$-fine, then $|R(f, P_1) - A_1| < \epsilon$.

Similarly, we can find $\delta_2(x)$, such that if a tagged partition $P_2$ is 
$\delta_2(x)$-fine, then $|R(f, P_2) - A_2| < \epsilon$.

Now we can define $\delta (x) = \min \{\delta_1(x), \delta_2(x)\}$.
From Theorem 8.1.5, we can find a tagged partition $(P,\{c_k\}^n_{k=1})$ that is $\delta(x)$-fine.

If $(P,\{c_k\}^n_{k=1})$ is $\delta(x)$-fine, it has to be
$\delta_1(x)$-fine. This is because

$$ 
x_k - x_{k-1} < \delta (c_k) \leq \delta_1(c_k)
$$

So $|R(f, P) - A_1| < \epsilon$.

For the same reason, $(P,\{c_k\}^n_{k=1})$ is $\delta(x)$-fine, it has to be $\delta_2(x)$-fine, and $|R(f, P) - A_2| < \epsilon$.

Since

$$ 
|A_1 - A_2| < |R(f, P) - A_1| + |R(f, P) - A_2| < \epsilon /2
$$

And $\epsilon$ can be arbitrary, so $A_1 = A_2$.

$\square$

### Exercise 8.1.9

Explain why every function that is Riemann-integrable
with $\int_{a}^{b}f = A$ must also have generalized Riemann
integral $A$.

**Proof**: If $f$ is Riemann-integrable, then for any
$\epsilon$, we can find $\delta$, any tagged partition $P$ is $\delta$-fine
then $|R(f, P) - A| \leq \epsilon$.

Let this $\delta(x) = \delta$ be the gauge, we can see
$f$ is generalized Riemann integrable.

$\square$

### Theorem 8.1.8.

Dirichlet’s function $g(x)$ is generalized Riemann-integrable on
$[0,1]$ with $\int_{0}^{1} g = 0$.

**Proof**: Let ϵ > 0. By Definition 8.1.6, we must construct a 
gauge $δ(x)$ on [0,1] such that whenever
$(P,\{c_k\}^n_{k=1})$ is $\delta(x)$-fine tagged partition, it 
follows that

$$ 
0 \leq \sum_{k=1}^{n} g(c_k)(x_k - x_{k-1}) < \epsilon
$$

The gauge represents a restriction on the size of
$Δx_k = x_k−x_{k−1}$ in the sense that $Δx_k < δ(c_k)$.

The Riemann sum consists of products of the form $g(c_k)Δx_k$.
Thus, for irrational tags, there is nothing to worry about because 
$g(c_k) = 0$ in this case. Our task is to make sure that any time 
a tag $c_k$ is rational, it comes from a suitably thin subinterval.

Let $\{r_1,r_2,r_3,...\}$ be an enumeration of the countable set of rational numbers contained in $[0,1]$.
For each $r_k$, set $δ(r_k) = ϵ/2^{k+1}$. For x irrational, set
$δ(x) = 1$.

### Exercise 8.1.10.

Show that if $(P,\{c_k\}^n_{k=1})$ is a $δ(x)$-fine tagged partition, then $R(g,P) < ϵ$.

**Proof**:

If $c_k$ is irrational, then $g(c_k)Δx_k = 0$.
Otherwise, $g(c_k)Δx_k < δ(r_k) = ϵ/2^{k+1}$.
So $\sum_{k=1}^{n} g(c_k)(x_k - x_{k-1}) < \epsilon$.

$\square$

### Theorem 8.1.9.

Assume $F : [a,b] → \mathbf{R}$ is diﬀerentiable at each point in $[a,b]$, and set $f(x) = F'(x)$. Then, $f$ has the generalized Riemann integral

$$ 
\int_{a}^{b} f = F(b) - F(a)
$$

Proof. Let $P= {x_0,x_1,x_2,...,x_n}$ be a partition of $[a,b]$. Both this proof and
the proof of Theorem 7.5.1 make use of the following fact.

### Exercise 8.1.11.

Show that

$$ 
F(b) - F(a) = \sum_{k=1}^{n} [F(x_k) - F(x_{k-1})]
$$

**Proof**: It is obvious. $\square$

If $\{c_k\}^n_{k=1}$ is a set of tags for $P$, then we can estimate the diﬀerence between
the Riemann sum $R(f,P)$ and $F(b)−F(a)$ by

$$ 
|F(b) - F(a) - R(f, P)| =
\left| 
\sum_{k = 1}^{n} [F(x_k) - F(x_{k-1}) - f(c_k)(x_k - x_{k-1})]
\right| \\
\leq
\sum_{k = 1}^{n} |F(x_k) - F(x_{k-1}) - f(c_k)(x_k - x_{k-1})|
$$

Let $ϵ > 0$. To prove the theorem, we must construct a gauge $δ(c)$
such that

$$ 
|F(b) - F(a) - R(f, P)| < ϵ
$$

for all $(P,{c_k})$ that are $δ(c)$-fine. (Using the variable $c$ in the gauge function is more convenient than $x$ in this case.)

### Exercise 8.1.12.

For each $c ∈ [a,b]$, explain why there exists a $δ(c) > 0$
(a $δ > 0$ depending on $c$) such that

$$ 
\left| 
\frac{F(x) - F(c)}{x - c} - f(c)
\right|
< \epsilon
$$

for all $0 < |x-c| < \delta (c)$.

**Proof**:

Since $F(x)$ is differential at $c$, that means

$$ 
\lim_{x \to c} \frac{F(x) - F(c)}{x - c} = f(c)
$$

i.e. given $\epsilon$, for $c$, we can find a $\delta (c)$, as
long as $0 < |x-c| < \delta (c)$,

$$ 
\left| 
\frac{F(x) - F(c)}{x - c} - f(c)
\right|
< \epsilon
$$

$\square$

### Exercise 8.1.13.

(a) For a particular $c_k ∈ [x_{k−1},x_k]$ of $P$, show that

$$ 
|F(x_k)−F(c_k)−f(c_k)(x_k−c_k)| < ϵ(x_k−c_k)
$$

and

$$ 
|F(c_k)−F(x_{k−1})−f(c_k)(c_k−x_{k−1})| < ϵ(c_k−x_{k−1}).
$$

**Proof**: Since $0 < x_k - c_k < \delta (c_k)$, then

$$
\left| 
\frac{F(x_k) - F(c_k)}{x_k - c_k} - f(c_k)
\right| < \epsilon
$$

i.e.

$$ 
|F(x_k)−F(c_k)−f(c_k)(x_k−c_k)| < ϵ(x_k−c_k)
$$

The other part is the same.

$\square$

(b) Now, argue that

$$ 
|F(x_k)−F(x_{k−1})−f(c_k)(x_k−x_{k−1})| < ϵ(x_k−x_{k−1})
$$

and use this fact to complete the proof of the theorem.

**Proof**:

$$ 
|F(x_k)−F(x_{k−1})−f(c_k)(x_k−x_{k−1})| =\\
\left| 
F(x_k)−F(c_k)−f(c_k)(x_k−c_k) +
F(c_k)−F(x_{k−1})−f(c_k)(c_k−x_{k−1})
\right| \\
\leq
|F(x_k)−F(c_k)−f(c_k)(x_k−c_k)| + |F(x_k)−F(c_k)−f(c_k)(x_k−c_k)| \\
\leq
ϵ(x_k−c_k) + ϵ(c_k−x_{k−1})\\
= ϵ(x_k−x_{k−1})
$$

Then we have

$$ 
|F(b) - F(a) - R(f, P)| \\
\leq
\sum_{k = 1}^{n} |F(x_k) - F(x_{k-1}) - f(c_k)(x_k - x_{k-1})|
\\
\leq
\sum_{k = 1}^{n} ϵ(x_k−x_{k−1}) \\
= \epsilon
$$

Then we proved Theorem 8.1.9.

$\square$

If we consider the function

$$ 
F(x) =
\begin{cases}
    x^{3/2} \sin (1/x) &\text{if } x \not = 0\\
    0 &\text{if } x = 0\\
\end{cases} 
$$

then it is not too diﬃcult to show that $F$ is diﬀerentiable everywhere, including $x = 0$, with

$$ 
F'(x) =
\begin{cases}
    (3/2) \sqrt[]{x} \sin (1/x) - (1/\sqrt[]{x}) \cos (1/x) &\text{if } x \not = 0\\
    0 &\text{if } x = 0\\
\end{cases} 
$$

What is notable here is that the derivative is unbounded near the origin.
The theory of the ordinary Riemann integral begins with the assumption that we only consider bounded functions on closed intervals, but there is no such restriction for the generalized Riemann integral.
Theorem 8.1.9 proves that $F'$ has a generalized integral.

Now, *improper* Riemann integrals have been created to extend Riemann integration to some unbounded functions, but it is another
interesting fact about the generalized Riemann integral that any function having an improper integral must already be integrable in the sense described in Definition 8.1.6.

### Theorem 8.1.10 (Change-of-variable Formula).

Let $g : [a,b] → \mathbf{R}$ be
diﬀerentiable at each point of $[a,b]$, and assume $F$ is diﬀerentiable on the set $g([a,b])$.
If $f(x) = F'(x)$ for all $x ∈ g([a,b])$, then

$$ 
\int_{a}^{b} (f◦g)·g' =
\int_{g(a)}^{g(b)} f.
$$

**Proof**. The hypothesis of the theorem guarantees that the function $(F ◦g)(x)$
is diﬀerentiable for all $x ∈ [a,b]$.

### Exercise 8.1.14.

(a) Why are we sure that $f$ and $(F◦g)'$ have generalized
Riemann integrals?

**Proof**: This is because $F$ is diﬀerentiable and
$f(x) = F'(x)$. Since $g$ is also differentialble, then
$F◦g$ is differentialble. And $(F◦g)'$ is its derivative.

$\square$

(b) Use Theorem 8.1.9 to finish the proof.

**Proof**:

On the left side

$$ 
(F◦g)' = (f◦g) \cdot g'
$$

So

$$ 
\int_{a}^{b} (f◦g)·g' = F(g(b)) - F(g(a))
$$

On the right side

$$ 
\int_{g(a)}^{g(b)} f = F(g(b)) - F(g(a))
$$

$\square$
