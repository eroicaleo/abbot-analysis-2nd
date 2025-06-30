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

## 8.3 Euler’s Sum

In Section 6.1 we saw Euler’s first and most famous derivation of the formula

$$ 
1 + \frac{1}{4} + \frac{1}{9} +
\frac{1}{16} + \frac{1}{25} + \cdots = \frac{\pi ^2}{6}
$$

At the crux of this argument are two representations for the function $sin(x)$.
The first is the standard Taylor series representation

$$ 
\tag{1}
\sin x = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!}
+ \cdots ,
$$

and the second is an infinite product representation

$$ 
\tag{2}
\sin x = x
\left( 1 - \frac{x}{\pi } \right) 
\left( 1 + \frac{x}{\pi } \right) 
\left( 1 - \frac{x}{2 \pi } \right) 
\left( 1 + \frac{x}{2 \pi } \right)
\cdots .
$$

### Wallis’s Product

### Exercise 8.3.1.

Supply the details to show that when $x = π/2$ the product
formula in (2) is equivalent to

$$ 
\tag{3}
\frac{\pi }{2}
=\lim_{n \to \infty}
\left( \frac{2 \cdot 2}{1 \cdot 3} \right) 
\left( \frac{4 \cdot 4}{3 \cdot 5} \right) 
\left( \frac{6 \cdot 6}{5 \cdot 7} \right) 
\cdots 
\left( \frac{2n \cdot 2n}{(2n - 1) \cdot (2n + 1)} \right) 
$$

**Proof**:

We plug the $\frac{\pi}{2}$ into equation (2).

$\square$

### Exercise 8.3.2.

Assume $h(x)$ and $k(x)$ have continuous derivatives on
$[a,b]$ and derive the familiar integration-by-parts
formula

$$ 
\int_{a}^{b} h(t) k'(t) dt
= h(b) k(b) - h(a) k (a)
- \int_{a}^{b} h'(t) k(t) dt .
$$

**Proof**: See exercise 7.5.6.

$\square$

### Exercise 8.3.3.

(a) Using the simple identity $\sin^n(x) = \sin^{n−1}(x)\sin(x)$ and
the previous exercise, derive the recurrence relation

$$ 
b_n = \frac{n-1}{n} b_{n-2} \text{ for all } n \geq 2
$$

**Proof**: 

$$ 
\int_{0}^{\frac{\pi}{2}}
\sin^n(x)
= 
\int_{0}^{\frac{\pi}{2}}
\sin^{n-1} (x) \sin (x)\\
= \sin^{n-1} (\frac{\pi}{2}) (-\cos (\frac{\pi}{2}))
- \sin^{n-1} (0) (-\cos (0))
- \int_{0}^{\frac{\pi}{2}} (n - 1) \sin ^{n-2} (x) \cos (x) (-\cos (x))\\
= (n - 1)\int_{0}^{\frac{\pi}{2}}
\sin ^{n-2} (x) \cos ^2 (x) \\
= (n - 1) \int_{0}^{\frac{\pi}{2}}
\sin ^{n-2} (x) - \sin ^{n} (x)
$$

So we have

$$ 
\int_{0}^{\frac{\pi}{2}}
\sin^n(x) +
(n - 1) \int_{0}^{\frac{\pi}{2}}
\sin^n(x) = (n - 1) \int_{0}^{\frac{\pi}{2}}
\sin^{n-2}(x)
$$

So,

$$ 
b_n = \frac{n-1}{n} b_{n-2} \text{ for all } n \geq 2
$$

$\square$

(b) Use this relation to generate the first three even terms and the first three odd terms of the sequence $(b_n)$.

$$ 
b_2 = \frac{1}{2} b_0 = \frac{\pi }{4}\\
b_4 = \frac{3}{4} b_2 = \frac{3 \pi }{16}\\
b_6 = \frac{5}{6} b_4 = \frac{15 \pi }{96}\\
b_3 = \frac{2}{3} b_1 = \frac{2}{3}\\
b_5 = \frac{4}{5} b_3 = \frac{8}{15}\\
b_7 = \frac{6}{7} b_4 = \frac{48}{105}\\
$$

$\square$

(c) Write a general expression for $b_{2n}$ and $b_{2n+1}$

$$
b_{2n} = \frac{\pi}{2} \cdot \frac{1}{2}
\cdot \frac{3}{4}
\cdot \frac{5}{6} \cdots
\cdot \frac{2n-1}{2n}
$$

and 

$$ 
b_{2n+1} = 1
\cdot \frac{2}{3}
\cdot \frac{4}{5}
\cdot \frac{6}{7}
\cdots
\cdot \frac{2n}{2n+1}
$$

### Exercise 8.3.4.

Show

$$ 
\lim_{n \to \infty} \frac{b_{2n}}{b_{2n+1}} = 1
$$

and use this fact to finish the proof of Wallis’s product formula in (3).

**Proof**:

Because $b_{2n} \geq b_{2n+1} \geq b_{2n+2}$, so

$$ 
1 \leq \frac{b_{2n}}{b_{2n+1}} \leq \frac{b_{2n}}{b_{2n+2}}
= \frac{2n+2}{2n+1}
$$

So

$$ 
\lim_{n \to \infty} \frac{b_{2n}}{b_{2n+1}}
\leq 
\lim_{n \to \infty} \frac{2n+2}{2n+1} = 1
\\
\lim_{n \to \infty} \frac{b_{2n}}{b_{2n+1}}
\geq
\lim_{n \to \infty} 1 = 1
$$

Then it's easy to see product formula in (3) holds.

$\square$

### Exercise 8.3.5.

Derive the following alternative form of Wallis’s product formula:

$$ 
\sqrt[]{\pi} =
\lim_{n \to \infty}
\frac{
2^{2n} (n!)^2
}{
(2n)! \sqrt[]{n}
}
$$

**Proof**:

We know

$$ 
\frac{\pi }{2}
=\lim_{n \to \infty}
\left( \frac{2 \cdot 2}{1 \cdot 3} \right) 
\left( \frac{4 \cdot 4}{3 \cdot 5} \right) 
\left( \frac{6 \cdot 6}{5 \cdot 7} \right) 
\cdots 
\left( \frac{2n \cdot 2n}{(2n - 1) \cdot (2n + 1)} \right) \\
= \frac{
(2^{2n} (n!)^2)^2
}{
(2n!)^2 (2n+1)
}
$$

So

$$ 
\pi = \lim_{n \to \infty} 
\frac{
(2^{2n} (n!)^2)^2 2
}{
(2n!)^2 (2n+1)
}
$$

So

$$ 
\sqrt[]{\pi} =
\lim_{n \to \infty}
\frac{
2^{2n} (n!)^2
}{
(2n)! \sqrt[]{n}
}
$$

$\square$

### Taylor Series

### Exercise 8.3.6.

Show that $1/\sqrt[]{1−x}$ has Taylor expansion
$\sum_{n=0}^{∞} c_nx_n$, where $c_0 = 1$ and

$$ 
c_n = \frac{
(2n)!
}{2^{2n}(n!)^2}
= \frac{
1 \cdot 3 \cdot 5 \cdots (2n - 1)
}{
2 \cdot 4 \cdot 6 \cdots 2n
}
$$

for $n \geq 1$.

**Solution**:

$$ 
f'(0) = \frac{1}{2} (1 - x)^{-3/2} = \frac{1}{2} \\
f''(0) = \frac{3}{4} (1-x)^{-5/2} = \frac{3}{4} \\
\cdots \\
f^{(n)}(0) = \frac{1 \cdot 3 \cdots(2n-1)}{2^n}
$$

Then

$$ 
c_n = \frac{f^{(n)}(0)}{n!} =
\frac{
1 \cdot 3 \cdot 5 \cdots (2n - 1)
}{
2 \cdot 4 \cdot 6 \cdots 2n
}
$$

$\square$

### Exercise 8.3.7.

Show that $\lim c_n = 0$ but $\sum_{n=0}^{∞} c_n$ diverges.

**Proof**: 

$$ 
c_n = \frac{
1 \cdot 3 \cdot 5 \cdots (2n - 1)
}{
2 \cdot 4 \cdot 6 \cdots 2n
}
$$

$c_n$ is a decreasing and bigger than $0$, so $c_n$ converges.
if $(c_n) \rightarrow c > 0$, then

$$ 
\lim_{n \to \infty} \frac{1}{c_n \sqrt[]{n}} \\
= \frac{1}{c} \times 0 = 0 \not = \sqrt[]{\pi}
$$

Now note

$$ 
c_n >
\frac{
1 \cdot 2 \cdot 4 \cdots (2n - 2)
}{
2 \cdot 4 \cdot 6 \cdots 2n
} = \frac{1}{2n}
$$

So we have

$$ 
\sum_{k=1}^{n} c_n > \frac{1}{2} (1 + 1/2 + 1/4 +
\cdots + 1/n)
$$

So $\sum_{n=0}^{∞} c_n$ diverges.

$\square$

The divergence of $\sum_{n=0}^{∞} c_n$ makes sense when we consider the Taylor series
for $1/$. We want to determine the values of $x$ for which

$$ 
\tag{4}
\frac{1}{\sqrt[]{1−x}} 
= \sum_{n = 1}^{\infty} c_nx^n,
$$

### Exercise 8.3.8.

Using the expression for $E_N(x)$ from Lagrange’s Remainder
Theorem, show that equation (4) is valid for all $|x| < 1/2$.
What goes wrong
when we try to use this method to prove (4) for $x ∈ (1/2,1)$?

**Solution**:

The Lagrange's Remainder is

$$ 
E_N(x) = \frac{f^{(N+1)}(c)}{(N+1)!}x^{N+1} =
\frac{1 \cdot 3 \cdots (2N+1) }{2^{N+1} (N+1)!}
\frac{x^{N+1}}{(1-c)^{N+1} \sqrt[]{1-c}}
$$

Fix $x < 1/2$, then $c < x < 1/2$. So $1 - c > x$.
$1 - c > 1/2$. So $\frac{1}{\sqrt[]{1-c}} < \frac{1}{\sqrt[]{2}}$.

$$ 
\frac{x}{1-c} < 1
$$

So $E_N(x) \rightarrow 0$.

When $x ∈ (1/2,1)$, we cannot guarantee

$$ 
\frac{x}{1-c} < 1.
$$

$\square$

### Theorem 8.3.1 (Integral Remainder Theorem).

Let $f$ be diﬀerentiable $N + 1$ times on $(−R,R)$ and assume
$f^{(N+1)}$ is continuous. Define $a_n = f^{(n)}(0)/n!$
for $n = 0,1,...,N$, and let

$$ 
S_N(x) = a_0 + a_1 x + a_2 x^2 + a_3 x^3 + \cdots + a_N x^N
$$

For all $x ∈ (−R,R)$, the error function $E_N(x) = f(x)−S_N(x)$ satisfies

$$ 
E_N(x) = \frac{1}{N!}
\int_{0}^{x} f^{(N+1)}(t) (x - t)^N dt .
$$

**Proof**. The case $x = 0$ is easy to check, so let’s take
$x \not = 0$ in $(−R,R)$ and keep
in mind that $x$ is a fixed constant in what follows. To avoid a few technical distractions, let’s just consider the case
$x > 0$.

### Exercise 8.3.9.

(a) Show

$$ 
f(x) = f(0) + \int_{0}^{x} f'(t) dt
$$

**Proof**: $f'(t)$ is differentiable, so it's continuous.
So it's integrable. From theorem 7.5.1, then

$$ 
\int_{0}^{x} f'(t) dt = f(x) - f(0)
$$

$\square$

(b) Now use a previous result from this section to show

$$ 
f(x) = f(0)+f'(0)x + \int_{0}^{x} f''(t) (x-t) dt .
$$

**Proof**:

We use integration-by-parts, and let $h(x) = f'(x), k(x) = (x-t)$ 

$$
-\int_{0}^{x} f'(t) dt = \int_{0}^{x} h(t) k'(t) dt
\\
=h(x)k(x) - h(0)k(0) - \int_{0}^{x} h'(t) k(t) dt \\
= -f'(0) x- \int_{0}^{x} f''(t) (x-t) dt \\
$$

So

$$ 
\int_{0}^{x} f'(t) dt = f'(0)x + \int_{0}^{x} f''(t) (x-t) dt
$$

$\square$

(c) Continue in this fashion to complete the proof of the theorem.

**Proof**:

Let $h(t) = f^{(N)}(t), k(t) = -\frac{(x-t)^{N}}{N}$.

Consider

$$ 
\int_{0}^{x} f^{(N)}(t) (x - t)^{N-1} dt
= \int_{0}^{x} h(t) k'(t) dt
= h(x)k(x) - h(0)k(0) - \int_{0}^{x} h''(t) k(t) dt \\
= \frac{1}{N} f^{(N)}(0) x^N +
\frac{1}{N} \int_{0}^{x} f^{(N+1)}(t) (x-t)^N dt
$$

So we have

$$ 
E_N(x) = \frac{1}{N!}
\int_{0}^{x} f^{(N+1)}(t) (x - t)^N dt .
$$ 

$\square$

### Exercise 8.3.10.

(a) Make a rough sketch of $1/\sqrt[]{1-x}$
and $S_2(x)$ over the interval $(−1,1)$,
and compute $E_2(x)$ for $x = 1/2,3/4$, and $8/9$.

**Solution**:

$$ 
a_0 = 1\\
a_1 = \frac{f'(0)}{1!} = \frac{1}{2} \\
a_2 = \frac{f''(0)}{2!} = \frac{1 \cdot 3}{2 \cdot 4} \\
$$

So $S_2(x) = 1 + \frac{1}{2}x + \frac{3}{8} x^2$.

Here are the python code to plot and compute $E_2(x)$.

```python
import numpy as np
import matplotlib.pyplot as plt

# Define the range of x values, avoiding the point where the function is undefined
x = np.linspace(-1, 0.99, 400)  # 400 points between -1 and 0.99

# Compute the function values
y = 1 / np.sqrt(1 - x)
z = 1 + (1/2) * x + (3/8) * (x**2)
# Plot the function
plt.plot(x, y)
plt.plot(x, z)
plt.title('Plot of $1/\sqrt{1-x}$ and $1 + (1/2)x + (3/8)x^2$')
plt.xlabel('x')
plt.ylabel('1/sqrt(1-x)')
plt.grid(True)
plt.show()

x = np.array([1/2, 3/4, 8/9])
y = 1 / np.sqrt(1 - x)
z = 1 + (1/2) * x + (3/8) * (x**2)
e = y - z
print(e)
```

The $E_2(x)$ for $x = 1/2,3/4$, and $8/9$ are
$[0.07046356, 0.4140625, 1.25925926]$

$\square$

(b) For a general $x$ satisfying $−1 < x < 1$, show

$$ 
E_2(x) = \frac{15}{16}
\int_{0}^{x}
\left( 
\frac{x-t}{1-t}
\right) ^ 2
\frac{1}{
(1-t)^{3/2}
} dt
$$

**Proof**:

$$ 
E_2(x) =
\frac{1}{2!}
\int_{0}^{x} f^{(2+1)}(t) (x - t)^2 dt
$$

$$ 
f^{(1)}(t) = \frac{1}{2} (1-x)^{-\frac{3}{2}} \\
f^{(2)}(t) = \frac{1 \cdot 3}{2 \cdot 2} (1-x)^{-\frac{5}{2}} \\
f^{(3)}(t) = \frac{1 \cdot 3 \cdot 5}{2 \cdot 2 \cdot 2}
(1-x)^{-\frac{7}{2}} \\
$$

So we proved.

$\square$

(c) Explain why the inequality

$$ 
\left| 
\frac{x-t}{1-t}
\right| \leq |x|
$$

is valid, and use this to find an overestimate for
$|E_2(x)|$ that no longer
involves an integral. Note that this estimate will necessarily depend on $x$.
Confirm that things are going well by checking that this overestimate is
in fact larger than $|E_2(x)|$ at the three computed values from part (a).

**Proof**: 

Assume $0 \leq t \leq x < 1$. Then $xt \leq  t$,
$x - xt \geq x - t$, so $\frac{x-t}{1-t} \leq x$ 

If $-1 < x \leq t \leq 0$, then $xt \geq t$ so
$x - xt \leq x - t$, so $x \leq \frac{x-t}{1-t}$, i.e.
$-x \geq -\frac{x-t}{1-t}$

In both cases, we proved it.

$$ 
|E_2(x)| = \frac{15}{16}
\left| 
\int_{0}^{x}
\left( 
\frac{x-t}{1-t}
\right) ^ 2
\frac{1}{
(1-t)^{3/2}
} dt
\right| \\
\leq
\frac{15}{16} x^3 \frac{1}{(1-|x|)^{3/2}}
$$

For $x = 1/2,3/4$, and $8/9$ are, the errors are

$$ 
[0.3314563, 3.1640625, 17.77777778]
$$

$\square$

(d) Finally, show
$E_N(x) → 0$ as $N → ∞$ for an arbitrary $x ∈ (−1,1)$.

**Proof**:

We have

$$ 
f^{(N+1)}(t) =
\frac{1 \cdot 3 \cdots (2N+1) }{2^{N+1}}
\cdot
\frac{1}{(1-t)^{N}}
\cdot
\frac{1}{(1-t)^{3/2}}
$$

So

$$ 
E_N(x) = \frac{1}{N!}
\int_{0}^{x}
\frac{1 \cdot 3 \cdots (2N+1) }{2^{N+1}}
\cdot
\frac{1}{(1-t)^{N}}
\cdot
\frac{1}{(1-t)^{3/2}}
(x-t)^N dt \\
\leq 
C_N \cdot (2N+1)|x|^N \frac{|x|}{(1-|x|)^{3/2}}
$$

Since $C_N \rightarrow 0$ and $(2N+1)|x|^N \rightarrow 0$,
then $E_N(x)$.

$\square$

The next step is to take the term-by-term anti-derivative of
this series.
Any time we start manipulating infinite series as though they 
were finite in nature we need to pause and make sure we are on 
solid footing.

### Exercise 8.3.11.

Assuming that the derivative of $\arcsin (x)$ is indeed
$1 / \sqrt[]{1−x^2}$
supply the justification that allows us to conclude

$$
\tag{5}
\arcsin (x) =
\sum_{n = 0}^{\infty}
\frac{c_n}{2n+1} x^{2n+1} \text{ for all } |x| < 1.
$$

**Proof**: Since $\sum_{n = 0}^{\infty}c_nx^{2n}$ converges
for $|x| < 1$, and $\frac{c_n}{2n+1} x^{2n+1} < c_nx^{2n}$,
then $\sum_{n = 0}^{\infty} \frac{c_n}{2n+1} x^{2n+1}$
converges for $|x| < 1$.

Let

$$ 
f(x) =
\sum_{n = 0}^{\infty}
\frac{c_n}{2n+1} x^{2n+1}
$$

From theorem 6.5.7, $f(x)$ is differentiable and
$f'(x) = \arcsin' (x)$. So $f(x) = \arcsin (x) + C$.
Since $f(0) = \arcsin (0) = 0$, then $f(x) = \arcsin (x)$,
for $|x| < 1$.

$\square$

### Exercise 8.3.12.

Our work thus far shows that the Taylor series in (5) is valid
for all $|x| < 1$, but note that $\arcsin(x)$ is continuous for all $|x| ≤ 1$. Carefully
explain why the series in (5) converges uniformly to
$\arcsin(x)$ on the closed interval $[−1,1]$.

Proof: Consider

$$ 
f(1) =
\sum_{n = 0}^{\infty}
\frac{c_n}{2n+1}
$$

Since

$$ 
\lim_{n \to \infty} \frac{1}{c_n \sqrt[]{n}}
= \sqrt[]{\pi }
$$

Then

$$ 
\lim_{n \to \infty} c_n \sqrt[]{n}
= 1/\sqrt[]{\pi }
$$

when $n$ is large,
$c_n < \frac{1 + 1/\sqrt[]{\pi}}{\sqrt[]{n}} < \frac{2}{\sqrt[]{n}}$.

So

$$ 
\frac{c_n}{2n+1} < \frac{2}{(2n+1)\sqrt[]{n}}
\lt n^{-3/2} 
$$

So

$$ 
\sum_{n = 0}^{\infty}
\frac{c_n}{2n+1}
$$

converges. Since it's all positive, it converges absolutely.
Then (5) also converges in $-1$.

$\square$

### Summing $\sum_{n = 1}^{\infty} 1/n^2$

Every proof of Euler’s sum contains a moment of genuine
ingenuity at some point, and this is where our proof takes
an unanticipated turn.

Let’s make the substitution
$x = \sin(θ)$ in (5) where we restrict our attention
to $−π/2 ≤ θ ≤ π/2$. The result is

$$ 
\theta = \arcsin (\sin (\theta) ) =
\sum_{n = 1}^{\infty}
\frac{c_n}{2n+1} \sin ^{2n+1} (\theta )
$$

which converges uniformly on $[−π/2,π/2]$.

### Exercise 8.3.13.

(a) Show

$$ 
\int_{0}^{\pi /2} \theta d \theta 
= \sum_{n = 1}^{\infty} \frac{c_n}{2n+1} b_{2n+1}
$$

being careful to justify each step in the argument. The term
$b_{2n+1}$ refers
back to our earlier work on Wallis’s product.

**Proof**: let

$$
f_n(\theta ) =
\frac{c_n}{2n+1} \sin ^{2n+1} (\theta ) \\
f(\theta ) = \theta
$$

So $\sum_{n = 1}^{\infty}f_n(\theta ) \rightarrow f(\theta )$
uniformly, then

$$ 
\int_{0}^{\pi /2} \theta d \theta =
\sum_{n = 1}^{\infty} \int_{0}^{\pi /2} f_n(\theta)
= \sum_{n = 1}^{\infty} 
\frac{c_n}{2n+1} \int_{0}^{\pi /2} \sin ^{2n+1} (\theta ) \\
= \sum_{n = 1}^{\infty} 
\frac{c_n}{2n+1} b_{2n+1}
$$

$\square$

(b) Deduce

$$ 
\frac{\pi ^2}{8} = \sum_{n = 0}^{\infty} \frac{1}{(2n+1)^2},
$$

and use this to finish the proof that $\frac{\pi ^2}{6} = \sum_{n = 1}^{\infty} 1/n^2$.

**Proof**:

$$ 
c_n = \frac{
1 \cdot 3 \cdot 5 \cdots (2n - 1)
}{
2 \cdot 4 \cdot 6 \cdots 2n
}
$$

$$ 
b_{2n+1} = 1
\cdot \frac{2}{3}
\cdot \frac{4}{5}
\cdot \frac{6}{7}
\cdots
\cdot \frac{2n}{2n+1}
$$

So

$$ 
\frac{c_n}{2n+1} b_{2n+1} = \frac{1}{(2n+1)^2}
$$

On the left side, $\int_{0}^{\pi /2} \theta d \theta = \frac{1}{2}(\frac{\pi}{2})^2 - 0 = \frac{\pi ^2}{8}$.

So we proved the first part.

Let

$$
A = \frac{1}{1^2} + \frac{1}{2^2} + \frac{1}{3^2} + \frac{1}{4^2}
+ \cdots
$$

Then

$$ 
A = (\frac{1}{1^2} + \frac{1}{3^2} + \cdots) +
(\frac{1}{2^2} + \frac{1}{4^2} + \cdots) \\
= \frac{\pi^2}{8} +  \frac{1}{4} A
$$

So $A = \frac{\pi ^2}{6}$.

$\square$
