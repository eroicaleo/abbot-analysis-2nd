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

## 8.4 Inventing the Factorial Function

### Exercise 8.4.2.

Verify that the series converges absolutely for all
$x ∈ R$, that $E(x)$ is diﬀerentiable on $R$, and
$E'(x) = E(x)$.

**Proof**: Fix any $x \in \mathbf{R}$, we can find 
$N > 2x$. Let $a_n = \frac{x^n}{n!}$ and

$$
A =
\left| 
\frac{x^N}{N!}
\right| 
$$

For $n > N$, $|a_n| < \frac{A}{2^{n-N}}$. So $\sum_{k = 1}^{\infty}|a_n|$ converges absolutely. Then we can apply
Theorem 6.5.7 to know that $E(x)$ is diﬀerentiable on $R$,
and $E'(x) = E(x)$.

$\square$

### Exercise 8.4.3.

(a) Use the results of Exercise 2.8.7 and the binomial formula
to show that $E(x+y) = E(x)E(y)$ for all $x,y ∈ \mathbf{R}$.

**Proof**: Fix $x$ and $y$. Let

$$ 
a_n = \frac{x^n}{n!} \\
b_n = \frac{y^n}{n!} \\
$$

Then note

$$ 
d_k = a_{0}b_{k} + a_{1}b_{k-1} + \cdots + a_{k-1}b_{1} + a_k b_0 \\
= \frac{y^k}{0!k!} + \frac{xy^{k-1}}{1!(k-1)!} + \cdots 
+ \frac{x^{k-1}y}{(k-1)!1!} + \frac{x^k}{k!0!} \\
= \frac{(x+y)^k}{k!}
$$

Use the results of Exercise 2.8.7, $\sum_{k = 1}^{\infty}d_k$
converges and it converges $E(x)E(y)$.

On the other hand, $\sum_{k = 1}^{\infty}d_k = E(x+y)$.

So $E(x+y) = E(x)E(y)$.

$\square$

(b) Show that $E(0) = 1, E(−x) = 1/E(x)$, and $E(x) > 0$ for all $x ∈ \mathbf{R}$.

**Proof**:

$$ 
E(0) = 1 + \frac{0}{1!} + \frac{0^2}{2!} + \cdots = 1
$$

Also

$$ 
1 = E(0) = E(x + (-x)) = E(x)E(-x)
$$

So $E(-x)=1/E(x)$.

Also since if $x > 0$, then $a_n = \frac{x^n}{n!} > 0$,
then $E(x) > 0$.

$\square$

### Exercise 8.4.4.

Define $e = E(1)$. Show $E(n) = e^n$ and $E(m/n) = (\sqrt[n]{e})^m$ for all $m,n ∈ Z$.

**Proof**:

$$ 
E(n) = E(1+1+\cdots +1) = E(1)\cdot E(1) \cdots E(1)\\
= e^n
$$

We also have

$$ 
e = E(1) = E(1/n + \cdots +1/n) = E(1/n)^n
$$

So $E(1/n) = \sqrt[n]{e}$. So $E(m/n) = (\sqrt[n]{e})^n$.

$\square$

### Definition 8.4.1.

Given $f : [a,∞] → R$, we say that $\lim_{x \to \infty} f(x) = L$ if for all $ϵ > 0$, there exists $M > a$ such that whenever $x ≥ M$ it follows that

$$ 
|f(x) - L| < \epsilon
$$

### Exercise 8.4.5.

Show $\lim_{x \to \infty}  x^ne^{−x} = 0$
for all $n = 0,1,2,...$.

**Proof**:

$$
\frac{x^n}{e^x} = 
\frac{x^n}{1 + \frac{x}{1} + \frac{x^2}{2!}+ \cdots + \frac{x^{n+1}}{(n+1)!} + \cdots} \leq
\frac{(n+1)!}{x} \rightarrow 0
$$

$\square$

### Exercise 8.4.6.

(a) Explain why we know $e^x$ has an inverse function—let’s
call it $\log x$—defined on the strictly positive real numbers and satisfying

(i) $\log (e^y) = y$ for all $y \in \mathbf{R}$ and

(ii) $e^{\log x} = x$, for all $x > 0$.

(b) Prove $(\log x)' = 1/x$. (See Exercise 5.2.12.)

**Proof**:

Let $y = e^x$ 
$$ 
\log'y = \frac{1}{(e^x)'} = \frac{1}{e^x} = 1/y
$$

$\square$

(c) Fix $y > 0$ and diﬀerentiate $\log(xy)$ with respect to $x$. Conclude that

$$ 
\log_{} (xy) = \log x + \log y \text{ for all } x, y > 0.
$$

**Proof**: Also see exercise
Exercise 7.5.8 (Natural Logarithm and Euler’s Constant).

$$ 
\log_{}' (xy) = \frac{1}{xy} \cdot y = \frac{1}{x}
$$

Since $\log_{}' x = \frac{1}{x}$, so

$$ 
\log xy = \log x + C
$$

Since $\log 1 = 0$, we can plug $x = 1$ and get
$\log y = C$.

$\square$

(d) For $t > 0$ and $n ∈ N$, $t_n$ has the usual interpretation as $t·t···t$ ($n$ times). Show that

$$ 
\tag{2}
t^n = e^{n \log_{} t} \text{ for all } n \in \mathbf{N}
$$

**Proof**: 

From (c), we know

$$ 
n \log_{} t = \log_{} t^n 
$$

And from (a), we know

$$ 
e^ {\log_{} t^n } = t^n
$$

So (2) holds.

$\square$

### Definition 8.4.2.

Given $t > 0$, define the exponential function $t^x$ to be

$$ 
t^x = e^{x \log_{} t} \text{ for all } x \in \mathbf{R}
$$

### Exercise 8.4.7.

(a) Show $t^{m/n} = (\sqrt[n]{t})^m$ for all $m, n \in \mathbf{N}$.

**Proof**:

$$ 
(\sqrt[n]{t})^m =
e^{m \log_{} \sqrt[n]{t}}
$$

Let $p = \log_{} \sqrt[n]{t}$, then $e^p = \sqrt[n]{t}$,
$e^{pn} = t$, i.e. $n \log_{} e^p = \log_{} t$,
i.e. $\log_{} e^p = \frac{1}{n} \log_{} t$, i.e.
$\log_{} \sqrt[n]{t} = \frac{1}{n} \log_{} t$.

So

$$ 
e^{m \log_{} \sqrt[n]{t}} = e^{\frac{m}{n} \log_{} t}\\
= t^{\frac{m}{n}}
$$

$\square$

(b) Show $\log(t^x) = x\log t$, for all $t > 0$ and $x ∈ \mathbf{R}$.

**Proof**: Note

$$ 
e^{x\log t} = t^x \\
e^{\log(t^x)} = t^x
$$

So $\log(t^x) = x\log t$.

$\square$

(c) Show $t^x$ is diﬀerentiable on $\mathbf{R}$ and find the derivative.

**Proof**: Because $t^x = e^{x \log_{} t}$, let

$$ 
g(x) = x \log_{} t
$$

which is differentiable, and let $f(x) = e^x$ which is also
differentiable, then their composite function $f \circ g$
is also differentiable.

$$ 
(e^{x \log_{} t})' = e^{x \log_{} t} \log_{} t = t^x \log_{} t
$$

$\square$

### Exercise 8.4.8.

Inspired by the fact that $0! = 1$ and $1! = 1$, let $h(x)$ satisfy

(i) $h(x) = 1$ for all $0 ≤ x ≤ 1$, and

(ii) $h(x) = xh(x−1)$ for all $x ∈ \mathbf{R}$.

(a) Find a formula for $h(x)$ on $[1,2]$, $[2,3]$, and $[n,n + 1]$ for arbitrary $n \in \mathbf{N}$.

$$ 
h(x) = x h(x - 1) = x, x \in [1,2] \\
h(x) = x h(x - 1) = x(x-1), x \in [2,3] \\
h(x) = x h(x - 1) = x(x-1) \cdots 1, x \in [n, n+1] \\
$$

$\square$

(b) (c) skipped

### Improper Riemann Integrals

### Definition 8.4.3.

Assume $f$ is defined on $[a,∞)$ and integrable on every
interval of the form $[a,b]$. Then define $\int_{a}^{\infty }f$ to be

$$ 
\lim_{b \to \infty} \int_{a}^{b}f,
$$

provided the limit exists. In this case we say the improper integral $\int_{a}^{\infty }f$ converges.

### Exercise 8.4.9.

(a) Show that the improper integral $\int_{a}^{\infty }f$
converges if and only if, for all $ϵ > 0$ there exists
$M > a$ such that whenever $d > c \geq M$ it follows that

$$ 
\left| 
\int_{c}^{d} f
 \right| < \epsilon
$$

(In one direction it will be useful to consider the sequence
$a_n = \int_{a}^{a+n} f$.

**Proof**:

$\Rightarrow$ Assume $\int_{a}^{\infty }f$
converges, and assume $\lim_{b \to \infty} \int_{a}^{b}f = B$,
then we can find $M$, if $b \geq M$, then

$$ 
\left| 
\int_{a}^{b} f - B
 \right| < \epsilon / 2
$$

Consider $d > c \geq M$,

$$
\left| \int_{c}^{d} f \right| 
=
\left| \int_{a}^{d} f - \int_{a}^{c} f \right|
\leq
\left| \int_{a}^{d} f - B \right| +
\left| B - \int_{a}^{c} \right| <
\epsilon / 2 + \epsilon / 2 = \epsilon 
$$

$\Leftarrow$ Consider $a_n = \int_{a}^{a+n} f$ then
$a_n$ is Cauchy sequence and assume $\lim_{n \to \infty} a_n = B$.

For $\epsilon$, we can find $M_1$, such that $d > c \geq M_1$,

$$ 
\left| 
\int_{c}^{d} f
 \right| < \epsilon / 2
$$

We can also find $M_2$, if $a+n > M_2$, then
$|a_n - B| < \epsilon / 2$. Then let $M = \max \{M_1, M_2\}$.

If $b > M$, and find $n$ such that $a+n > M$  then

$$ 
\left| \int_{a}^{b} f - B \right| =
\left| \int_{a}^{b} f - \int_{a}^{a+n} f + \int_{a}^{a+n} f - B \right| < \\
\left| \int_{a}^{b} f - \int_{a}^{a+n} f \right| +
\left| \int_{a}^{a+n} f - B \right| < \\
\epsilon / 2 + \epsilon / 2 = \epsilon
$$

So

$$ 
\lim_{b \to \infty} \int_{a}^{b} f = B
$$

$\square$

(b) Show that if $0 ≤ f ≤ g$ and $\int_{a}^{b}g$ converges
then $\int_{a}^{b}f$ converges.

**Proof**: Since $\int_{a}^{b}g$ converges, then
we can find $M$, if $d > c \geq M$ then
$|\int_{c}^{d} g | = \int_{c}^{d} g < \epsilon$.
Since $0 ≤ f ≤ g$, then
$|\int_{c}^{d} f | = \int_{c}^{d} f \leq
\int_{c}^{d} g < \epsilon$

$\square$

(c) Part (a) is a Cauchy criterion, and part (b) is a comparison 
test. State and prove an absolute convergence test for improper 
integrals.

**Proof**: The absolute convergence test for improper 
integrals is: if $f$ is integrable on any interval $[a,b]$ and $\lim_{b \to \infty} \int_{a}^{b} |f|$ converges,
then $\lim_{b \to \infty} \int_{a}^{b} f$ converges.

Since $f$ is integrable on any interval $[a,b]$, then from Theorem 7.4.2. (v), $|f|$ is also integrable on any interval $[a,b]$. Since $\lim_{b \to \infty} \int_{a}^{b} f$ converges,
we can find a $M$ such that $d > c \geq M$, then

$$ 
\int_{c}^{d} |f| < \epsilon
$$

Again from Theorem 7.4.2. (v)

$$ 
\left| \int_{c}^{d} f \right| \leq
\int_{c}^{d} |f| < \epsilon 
$$

Then from part (a) $\lim_{b \to \infty} \int_{a}^{b} f$ converges.

$\square$

### Exercise 8.4.10.

(a) Use the properties of $e^t$ previously discussed to show

$$ 
\int_{0}^{\infty} e^{-t} dt = 1
$$

**Proof**: $e^t$ is continuous on $[0,b]$, so it's integrable.
Then we can use the first part of theorem 7.5.1, let

$$ 
F(t) = - e^{-t}
$$

and $F'(t) = e^{-t}$, so

$$ 
\int_{0}^{\infty} e^{-t} dt = \lim_{b \to \infty} F(b) - F(0)
= 1 - e^{-b} = 1
$$

$\square$

(b) Show

$$ 
\tag{3}
\frac{1}{\alpha }
= \int_{0}^{\infty}e^{-\alpha t} dt,
\text{ for all } \alpha > 0.
$$

**Proof**:

$e^{-\alpha t}$ is continuous on $[0,b]$, so it's integrable.

Let

$$ 
F(t) = - \frac{1}{\alpha} e^{-\alpha t}
$$

and $F'(t) = f(t)$.

$$ 
\int_{0}^{\infty} e^{-\alpha t} dt =
\lim_{b \to \infty} F(b) - F(0) = \frac{1}{\alpha}
$$

$\square$

### Exercise 8.4.11.

(a) Evaluate $\int_{0}^{b} t e^{-\alpha t}$ using the integration-by-parts formula from Exercise 7.5.6. The result will be an expression in α and b.

**Solution**:

Let

$$ 
h(t) = - \frac{1}{\alpha } e^{-\alpha t} \\
k(t) = t
$$

Then

$$ 
\int_{0}^{b} t e^{-\alpha t} =
\int_{0}^{b} k(t) h'(t) =
h(b) k(b) - h(0) k(0) - \int_{0}^{b} k'(t) h(t) = \\
- \frac{1}{\alpha } e^{-\alpha b} \cdot b -

\int_{0}^{b} -\frac{1}{\alpha } e^{-\alpha t} dt \\
=
\frac{1}{\alpha } \int_{0}^{b} e^{-\alpha t} dt -
\frac{b}{\alpha } e^{-\alpha b} \\
=
\frac{1}{\alpha } (\frac{1}{\alpha} -
\frac{1}{\alpha } e^{-\alpha b}) -
\frac{b}{\alpha } e^{-\alpha b}
$$

$\square$

(b) Now compute

$$ 
\int_{0}^{\infty} t e^{-\alpha t}
$$

and verify equation (4).

$$ 
\tag{4}
\frac{1}{\alpha ^2} =
\int_{0}^{\infty} t e^{-\alpha t} dt
$$

**Solution**:

$$ 
\lim_{b \to \infty} 
\frac{1}{\alpha } (\frac{1}{\alpha} -
\frac{1}{\alpha } e^{-\alpha b}) -
\frac{b}{\alpha } e^{-\alpha b} = \frac{1}{\alpha ^2}
$$

$\square$

### Diﬀerentiating Under the Integral

* Our sense of distance
between points $(x_0,t_0)$ and $(x,t)$ with the familiar Euclidean distance formula

$$ 
\| (x,t) - (x_0,t_0) \| =
\sqrt[]{(x - x_0^2) + (t - t_0)^2}
$$

### Definition 8.4.4.

A function $f : D → \mathbf{R}$ is continuous at $(x_0,t_0)$ if for all
$ϵ > 0$, there exists $δ > 0$ such that whenever
$\| (x,t) - (x_0,t_0) \| < \delta$, it follows
that

$$ 
\left| f(x, t) - f(x_0, t_0) \right| < \epsilon.
$$

### Exercise 8.4.12.

Assume the function $f(x,t)$ is continuous on the rectangle
$D = \{(x,t) : a \leq x \leq b, c \leq t \leq d\}$.
Explain why the function

$$ 
F(x) = \int_{c}^{d} f(x, t)dt
$$

is properly defined for all $x \in [a,b]$.

**Proof**: Fix $x$, $f(x, t)$ is a continuous function
defined on $[c,d]$. So it is integrable. So

$$ 
\int_{c}^{d} f(x, t)dt
$$

exists.

$\square$

It should not be too surprising that Theorem 4.4.7
has an analogue in the
$\mathbf{R}^2$ setting.
The set $D$ is compact in $\mathbf{R}^2$, and a continuous 
function on $D$ is
uniformly continuous in the sense that the
$δ$ in Definition 8.4.4 can be chosen
independently of the point $(x_0,t_0)$.

### Theorem 8.4.5.

If $f(x,t)$ is continuous on $D$, then
$F(x) = \int_{c}^{d} f(x,t) dt$ is uniformly continuous on
$[a,b]$.

### Exercise 8.4.13.

Prove Theorem 8.4.5.

**Proof**: We will prove $F(x)$ is continuous first.
Given $x_0$ in $[a, b]$ and $\epsilon > 0$, since $f(x,t)$
is uniformly continuous on $D$, we can find $\delta$,
as long as $x \in U_{\delta}(x_0)$,
$\left| f(x, t) - f(x_0, t) \right| < \frac{\epsilon}{d-c}$ for
all $t \in [c,d]$.

So

$$ 
|F(x) - F(x_0)| =
\left| \int_{c}^{d} f(x, t) -
\int_{c}^{d} f(x_0, t) \right| 
\leq
\int_{c}^{d}
\left| f(x, t) -
f(x_0, t) \right| \\
\leq
\frac{\epsilon }{d-c} (d-c) = \epsilon
$$

Since $F(x)$ is continuous then $F(x)$ is uniformly continuous.

$\square$

Taking inspiration from equations (3) and (4), let’s add the 
assumption that
for each fixed value of $t$ in $[c,d]$, the function
$f(x,t)$ is a diﬀerentiable function of $x$; that is,

$$ 
f_x(x, t) = \lim_{z \to x}
\frac{
f(z,t) - f(x,t)
}{z-x}
$$

exists for all $(x,t) ∈ D$.
In addition, let’s assume that the derivative function
$f_x(x,t)$ is continuous.

### Theorem 8.4.6.

If $f(x,t)$ and $f_x(x,t)$ are continuous on $D$, then the
function $F(x) = \int_{c}^{d} f(x,t) dt$ is diﬀerentiable and

$$ 
F'(x) = \int_{c}^{d} f_x(x,t) dt.
$$

**Proof**. Fix $x$ in $[a,b]$ and let $ϵ > 0$ be arbitrary.
Our task is to find a $δ > 0$ such that

$$
\tag{5}
\left| 
\frac{F(z) - F(x)}{z-x}
-
\int_{c}^{d} f_x(x,t)dt
 \right| < \epsilon
$$

whenever $0 < |z-x| < \delta$.

### Exercise 8.4.14.

Finish the proof of Theorem 8.4.6

**Proof**:

Because

$$ 
\left| 
\frac{F(z) - F(x)}{z-x}
-
\int_{c}^{d} f_x(x,t)dt
 \right| \\
=
\left| 
\frac{\int_{c}^{d} f(z,t) - \int_{c}^{d} f(x,t)}{z-x}
- f_x(x,t)
 \right| \\
=
\left| 
\int_{c}^{d}
\frac{f(z,t) - f(x,t)}{z-x} - f_x(x,t)
 \right| \\
 \leq
\int_{c}^{d}
\left| 
\frac{f(z,t) - f(x,t)}{z-x} - f_x(x,t)
\right| <
\frac{\epsilon}{d-c}(d-c) = \epsilon
$$

$\square$

### Improper Integrals, Revisited

Theorem 8.4.6 is a formal justification for diﬀerentiating under 
the integral sign,
but we need to extend this result to the case where the integral 
is improper.
Looking back one more time to our motivating example in equation 
(3), we see
that what we have is a function $f(x,t)$ where the domain of the 
variable $t$ is the
unbounded interval $c ≤ t < ∞$.

Let’s fix $x$ from some set $A ⊆ R$. For such an $x$, we define

$$ 
\tag{6}
F(x) = \int_{c}^{\infty} f(x,t)dt =
\lim_{d \to \infty} \int_{c}^{d} f(x,t)dt,
$$

provided the limit exists.

As we have seen on numerous occasions, the elixir required
to ensure that good behavior in the finite setting extends to
the infinite setting is uniformity.

### Definition 8.4.7.

Given $f(x,t)$ defined on $D= \{(x,t) : x ∈ A,c ≤ t\}$, assume
$F(x) = \int_{c}^{\infty}f(x,t)dt$ exists for all $x ∈ A$.
We say the improper integral converges
uniformly to $F(x)$ on $A$ if for all $ϵ > 0$, there exists
$M > c$ such that

$$ 
\left| 
F(x) - \int_{c}^{d} f(x,t) dt
 \right| < \epsilon 
$$

for all $d ≥ M$ and all $x ∈ A$.

### Exercise 8.4.15.

(a) Show that the improper integral
$\int_{0}^{\infty} e^{-xt} dt$ converges
uniformly to $1/x$ on the set $[1/2,∞)$.

**Proof**:

$$ 
\int_{0}^{b} e^{-xt} dt =
1 - \frac{1}{x} e^{-xb} \geq 1 - 2 e ^{-b/2}
$$

It does not depend on $x$.

$\square$

(b) Is the convergence uniform on $(0,∞)$?

**Solution**: No. For any fixed $x$,
$\int_{0}^{\infty} e^{-xt} dt = 1$, but give any $b$,
let $x = 1/b$

$$ 
\int_{0}^{b} e^{-xt} dt = 1 - b/e
$$

$\square$

### Exercise 8.4.16.

Prove the following analogue of the Weierstrass M-Test for
improper integrals: If $f(x,t)$ satisfies $|f(x,t)| ≤ g(t)$
for all $x ∈ A$ and $\int_{a}^{\infty} g(t)dt$ converges, then
$\int_{a}^{\infty} f(x,t)dt$ converges uniformly on $A$.

**Proof**:

Given $\epsilon$, since $\int_{a}^{\infty} g(t)dt$ converges,
we can find $M$, if $d > c \geq M$, we have
$|\int_{c}^{d} g(t) dt | = \int_{c}^{d} |g(t)| dt < \epsilon / 2$.

Then

$$ 
\left| \int_{c}^{d} f(x,t) dt \right|  \leq
\int_{c}^{d} |f(x,t)| dt \leq
\int_{c}^{d} g(t) dt < \epsilon / 2
$$

Then given any $x_0$, we can find $d_{x_0}$, such that

$$ 
\left| \int_{a}^{d_{x_0}} f(x_0, t) dt - F(x_0)
 \right| < \epsilon / 2
$$

Then

$$ 
\left| 
\int_{a}^{c} f(x_0, t) dt - F(x_0)
 \right| \leq 
\left| 
\int_{a}^{c} f(x_0, t) dt - \int_{a}^{d_{x_0}} f(x_0, t) dt
 \right| +
\left| 
\int_{a}^{d_{x_0}} f(x_0, t) dt - F(x_0)
 \right| \\
\leq \epsilon / 2 + \epsilon / 2 = \epsilon 
$$

$\square$

An immediate consequence of Definition 8.4.7 is that if the 
improper integral
converges uniformly then the sequence of functions defined by

$$ 
F_n(x) = \int_{c}^{c+n} f(x,t) dt
$$

converges uniformly to $F(x)$ on $[a,b]$. This observation gives us access to the
host of useful results we developed in Chapter 6.

### Theorem 8.4.8.

If $f(x,t)$ is continuous on $D= \{(x,t) : a ≤ x ≤ b,c ≤ t\}$,
then

$$ 
F(x) = \int_{c}^{\infty} f(x,t)dt
$$

is uniformly continuous on $[a,b]$, provided the integral converges uniformly.

**Proof**:

Let

$$ 
F_n(x) = \int_{c}^{c+n} f(x,t) dt
$$

From theorem 8.4.5., then $F_n(x)$ is continuous.
Since the integral converges uniformly, then $F_n(x)$ converges
to $F(x)$ uniformly.
Then according to theorem 6.2.6, $F(x)$ is continuous.

$\square$

### Theorem 8.4.9.

Assume the function $f(x,t)$ is continuous on
$D= \{(x,t) : a ≤ x ≤ b,c ≤ t\}$ and
$F(x) = \int_{c}^{\infty} f(x,t)dt$ exists for each $x ∈ [a,b]$.
If the derivative function
$f_x(x,t)$ exists and is continuous, then

$$ 
\tag{7}
F'(x) =
\int_{c}^{\infty} f_x(x,t) dt,
$$

provided the integral in (7) converges uniformly.

### Exercise 8.4.18.

Prove Theorem 8.4.9.

**Proof**:

Let $G(x) = \int_{c}^{\infty} f_x(x,t) dt$.

Again, consider

$$ 
F_n(x) = \int_{c}^{c+n} f(x,t) dt \text{ and }
G_n(x) = \int_{c}^{c+n} f_x(x,t) dt
$$

And let $D_n = \{(x,t) : a ≤ x ≤ b,c ≤ t ≤ c+n\}$.

Since $f(x,t)$ and $f_x(x,t)$ are continuous on $D_n$, then from theorem 8.4.6, $F_n'(x) = G_n(x)$.

Since $F_n(x)$ converges to $F(x)$ and $G_n(x)$ converges
uniformly to $G(x)$, then from theorem 6.3.1,
$F(x)$ is differentiable and $F'(x) = G(x)$.

$\square$

### The Factorial Function

It’s time to return our attention to equation (3) from earlier in this section:

$$ 
\frac{1}{\alpha }
= \int_{0}^{\infty}e^{-\alpha t} dt,
\text{ for all } \alpha > 0.
$$

### Exercise 8.4.19.

(a) Although we verified it directly, show how to use the
theorems in this section to give a second justification for the formula

$$ 
\frac{1}{\alpha ^2} =
\int_{0}^{\infty} t e^{-\alpha t} dt,
\text{ for all } \alpha > 0.
$$

**Proof**: Consider $f(x,t) = e^{-xt}$, and
$D = \{(x,t) : 1/2 ≤ x ≤ 3/2, 0 ≤ t\}$.

$$ 
f_x(x,t) = -t e^{-xt}
$$

is also continuous on $D$.

$$
\int_{0}^{b} t e^{-x t} =
\int_{0}^{b} k(t) h'(t) =
h(b) k(b) - h(0) k(0) - \int_{0}^{b} k'(t) h(t) = \\
- \frac{1}{x } e^{-x b} \cdot b -

\int_{0}^{b} -\frac{1}{x } e^{-x t} dt \\
=
\frac{1}{x } \int_{0}^{b} e^{-x t} dt -
\frac{b}{x } e^{-x b} \\
=
\frac{1}{x } (\frac{1}{x} -
\frac{1}{x } e^{-x b}) -
\frac{b}{x } e^{-x b} \\
= \frac{1}{x^2} - \frac{1}{x^2} e^{-x b} - \frac{b}{x } e^{-x b}
$$

So

$$ 
\int_{0}^{\infty} f_x(x, t) dt
$$

converges uniformly. We can apply theorem 8.4.9:

$$ 
-\frac{1}{x^2} = F'(x) = \int_{0}^{\infty} f_x(x,t) dt
= \int_{0}^{\infty} -t e^{-xt} dt
$$

So,

$$ 
\frac{1}{x^2} = \int_{0}^{\infty} t e^{-xt} dt
$$

Then we can plug $\alpha$ back.

$\square$

(b) Now derive the formula

$$ 
\tag{8}
\frac{n!}{\alpha ^ {n+1}} =
\int_{0}^{\infty}t^n e^{-\alpha t} dt
\text{ for all } \alpha > 0.
$$

**Proof**:

First, we prove $\int_{0}^{\infty}t^n e^{- x t} dt$ for any
$0 < a \leq x \leq b$.

$$ 
\left| t^n e^{- x t} \right|
= t^n e^{- x t} \leq t^n e^{- a t}
$$

Since

$$ 
e^{at} = 1 + (at) + \frac{(at)^2}{2!} + \cdots
+ \frac{(at)^{n+2}}{(n+2)!} + \cdots >
\frac{(at)^{n+2}}{(n+2)!}
$$

So

$$
t^n e^{- a t} \leq g(t) = \begin{cases}
    1 &\text{if } 0 \leq t \leq 1\\
    \frac{(n+2)!}{a^{n+2} t^2} &\text{if } t > 1\\
\end{cases} 
$$

The improper integral $\lim_{t \to \infty} g(t)$ converges.
So from exercise 8.4.16, $\int_{0}^{\infty}t^n e^{- x t} dt$
converges uniformly.

We can use induction, assume the improper integral holds

$$
\frac{(n-1)!}{x^{n}} = \int_{0}^{\infty}
t^{n-1} e^{-xt} dt
$$

Then $f(x,t)$ is continuous,
$f_x(x,t) = -t^n e^{-xt}$ continuous and
$\int_{0}^{\infty}f_x(x,t) dt$ converges uniformly.

So we have

$$ 
\frac{n!}{x^{n+1}} = \int_{0}^{\infty} t^n e^{-xt} dt
$$

$\square$

### Definition 8.4.10.

For $x ≥ 0$, define the factorial function

$$ 
x! = \int_{0}^{\infty} t^x e^{-t} dt .
$$

### Exercise 8.4.20.

(a) Show that $x!$ is an infinitely diﬀerentiable function on
$(0,∞)$ and produce a formula for the nth derivative.
In particular show that $(x!)'' > 0$.

**Proof**: Let $f(x,t) = t^x e^{-t}$ . Given $x$, since $t^x$ and $e^{-t}$ are continuous
functions on $[0, c]$, so they are integrable.

Also, if $0 < a \leq x \leq b$, we can find $k$,
such that $0 < 1/k < a \leq x \leq b < k$.
then for $t > 1$,

$$ 
t^x e^{-t} =
\frac{
    t^x
}{1 + \frac{t}{1!} + \frac{t^2}{2!} + \cdots +
\frac{t^{k+2}}{(k+2)!} + \cdots} \\
< \frac{(k+2)!}{t^2}
$$

define $g(x)$ as

$$
g(t) = \begin{cases}
    1 &\text{if } 0 \leq t \leq 1\\
    \frac{(k+2)!}{t^2} &\text{if } t > 1\\
\end{cases} 
$$

So

$$ 
|t^x e^{-t}| = t^x e^{-t} \leq g(x)
$$

Since the improper integral $\lim_{t \to \infty} g(t)$
converges, then $f(x,t)$ converges uniformly.

Now, let's consider the nth derivative of $f(x,t)$ w.r.t $x$:

$$ 
f_x^{(n)}(x, t) = t^x (\log_{} (t))^n e^{-t}
$$

Note that $f_x^{(n)}(x, t)$ is not defined at $t = 0$.
But we can use L’Hospital’s Rule: ∞/∞ case:

$$ 
\lim_{t \to 0} \frac{(\log_{} (t))^n}{t^{-x}}
=
\lim_{t \to 0}
\frac{n (\log_{} (t))^{n-1} (1/t)}{(-x)t^{-1-x}} \\
=
\lim_{t \to 0}
\frac{n}{(-x)} \frac{\log_{} (t))^{n-1}}{t^{-x}} \\
\lim_{t \to 0}
= \frac{n!}{(-x)^n} \frac{1}{t^{-x}} = 0
$$

Thus we can define $f_x^{(n)}(x, 0) = 0$.

When $x \in [a,b]$, and $t > 1$ 

$$ 
\left| t^x (\log_{} (t))^n e^{-t} \right|
= t^x (\log_{} (t))^n e^{-t} \\
\leq
t^b t^n e^{-t} \leq \frac{C}{t^2}
$$

where $C$ is a constant independent of $x$.
So the improper integral
$\int_{0}^{\infty} t^x (\log_{} (t))^n e^{-t}$
converges uniformly.

So the nth derivative is

$$ 
\int_{0}^{\infty} t^x (\log_{} (t))^n e^{-t} dt
$$

And the 2nd derivative is

$$ 
\int_{0}^{\infty} t^x (\log_{} (t))^2 e^{-t} dt
$$

For any $x > 0$, $t^x (\log_{} (t))^2 e^{-t} >0$,
so $(x!)'' > 0$.

$\square$

(b) Use the integration-by-parts formula employed earlier to show 
that $x!$ satisfies the functional equation.

$$ 
(x+1)! = (x+1)x! 
$$

**Proof**:

$$ 
(x+1)! = \int_{0}^{\infty} t^{x+1} e^{-t} dt
$$

So let $h(t) = \frac{t^{x+1}}{(x+1)}, k(t) = e^{-t}$
then

$$ 
\int_{0}^{b} t^{x} e^{-t} =
\int_{0}^{b} h'(t) k(t) \\
= h(b) k(b) - h(0) k(0) - \int_{0}^{b} h(t) k'(t)
\\ =
\frac{b^{x+1} e^{-b}}{x+1} - 0 +
\int_{0}^{b} \frac{t^{x+1}}{x+1} e^{-t} dt
$$

When $b \rightarrow \infty$, we have

$$ 
x! = \frac{(x+1)!}{x+1}
$$

$\square$

### Theorem 8.4.11 (Bohr–Mollerup Theorem).

There is a unique positive
function $f$ defined on $x ≥ 0$ satisfying

(i) $f(0) = 1$

(ii) $f(x+1) = (x+1)f(x)$, and

(iii) $\log(f(x))$ is convex.

Because $x!$ satisfies properties (i), (ii), and (iii), it follows that $f(x) = x!$.

**Proof**: We need one more geometrically plausible fact about convex functions.
If $[a,b]$ and $[a',b']$ are two intervals in the domain of a convex function $φ$, and
$a ≤ a'$ and $b ≤ b'$, then the slopes of the chords over these intervals satisfy

$$ 
\frac{\phi(b)-\phi(a)}{b-a}
\leq
\frac{\phi(b')-\phi(a')}{b'-a'}
$$

Because $f$ satisfies properties (i) and (ii) we know $f(n) = n!$ for all $n ∈ N$.
Now fix $n ∈ N$ and $x ∈ (0,1]$.

### Exercise 8.4.21.

(a) Use the convexity of $\log(f(x))$ and the three intervals
$[n−1,n]$, $[n,n+x]$, and $[n,n+1]$ to show

$$ 
x \log_{} (n) \leq
\log_{} (f(n+x)) - \log_{} (n!)
\leq
x \log_{} (n+1)
$$

**Proof**:

$$ 
\frac{\log(f(n)) - \log_{} f((n-1))}{1}
\leq
\frac{\log(f(n+x)) - \log_{} f((n))}{x}
\leq
\frac{\log(f(n+1)) - \log_{} f((n))}{1}
$$

This is the same as it asks.

$\square$

(b) Show $\log(f(n+x)) = \log(f(x))+\log((x+1)(x+2)···(x+n))$

**Proof**:

Since

$$ 
f(x+n) = (x+n)f(x+n-1)
= (x+n)(x+n-1)f(x+n-2)
\cdots
= (x+n)\cdots (x+1) f(x) 
$$

Then with exercise 8.4.6 (c), so we proved.

$\square$

(c) Now establish that

$$ 
0 \leq
\log_{} (f(x)) -
\log_{}
\left( 
\frac{n^xn!}{(x+1)(x+2)\cdots (x+n)}
 \right)
\leq
x \log_{} (1+\frac{1}{n})
$$

**Proof**:

We use (a) - $x \log_{} n$ and get

$$ 
\log_{} (f(n+x)) - \log_{} (n!) - x\log_{} n =\\
\log_{} f(x) + \log_{} ((x+1)(x+2)\cdots (x+n))
- \log_{} (n!) - x\log_{} n \\
= \log_{} f(x) -
\log_{}
\left( 
\frac{n^xn!}{(x+1)(x+2)\cdots (x+n)}
 \right)
$$

$\square$

(d) Conclude that

$$
f(x) = \lim_{n \to \infty} 
\frac{n^xn!}{(x+1)(x+2)\cdots (x+n)}
$$

**Proof**:

This is because

$$ 
\lim_{n \to \infty} x \log_{} (1 + \frac{1}{n}) = 0
$$

$\square$

(e) Finally, show that the conclusion in (d) holds for all
$x ≥ 0$.

**Proof**:

Assume $x \in (1, 2]$ then $x = 1 + x_0$, $x_0 \in (0,1]$.

$$ 
f(x) = f(x_0+1)
= (x_0+1) f(x_0) \\
= (x_0+1)
\lim_{n \to \infty} 
\frac{n^{x_0}n!}{(x_0+1)(x_0+2)\cdots (x_0+n)} \\
=
\lim_{n \to \infty} 
\frac{n^{x_0+1}(n-1)!}{(x_0+2)(x_0+3)\cdots (x_0+n)} \\
=
\lim_{n \to \infty} 
\frac{n^{x}(n-1)!}{(x+1)(x+2)\cdots (x+(n-1))} \\
=
\lim_{n \to \infty} 
\frac{n^{x}n!}{(x+1)(x+2)\cdots (x+n)} \\
$$

Then we can use induction for all $x > 0$.

$\square$

Because we have arrived at an explicit formula for $f(x)$, the function $f(x)$
must be unique. By virtue of the fact that $x!$ satisfies conditions (i), (ii), and(iii)
of the theorem, we can conclude that $x!$ is this unique function; i.e., $f(x) = x!$.
Thus, not only have we proved the theorem, but we have also discovered analternate representation for the factorial function called the Gauss product formula:

$$ 
\tag{9}
x! = \int_{0}^{\infty} t^x e^{-t} dt =
\lim_{n \to \infty} 
\frac{n^{x}n!}{(x+1)(x+2)\cdots (x+n)}
$$

For all $x \geq 0$.

Recall that when $x!$ is extended to all of $\mathbf{R}$ via the functional equation
$x! = x(x− 1)!$ we get asymptotes at every negative integer. Thus, there is a
compelling reason to consider the reciprocal function $1/x!$ which we can take to
be zero for $x =−1,−2,−3,...$.

### Exercise 8.4.22.

(a) Where does
$g(x) = \frac{x}{x!(−x)!}$ equal zero? What other
familiar function has the same set of roots?

**Solution**: $g(x) = 0$ for every integer.
$\sin \pi x$ also has the same set of roots.

(b) The function $e^{−x^2}$ provides the raw material for the all-important Gaussian bell curve from probability, where it is known that

$$ 
\int_{-\infty}^{\infty} e^{−x^2} dx = \sqrt[]{\pi}
$$

Use this fact (and some standard integration techniques) to evaluate $(1/2)!$.

**Solution**:

$$ 
(1/2)! = \int_{0}^{\infty} t^{1/2} e^{-t} dt
$$

Consider the integral

$$ 
\int_{0}^{b^2} t^{1/2} e^{-t} dt
$$

We apply 7.5.10 Change-of-variable Formula and let $g(x) = x^2$.
So

$$
\int_{0}^{b} f(g(x)) g'(x) dx =
\int_{0}^{b} (x^2)^{1/2} e^{-x^2} 2x dx \\
= \int_{0}^{b} 2x^2e^{-x^2} dx \\
= \int_{-b}^{b} x^2e^{-x^2} dx
$$

Let $h(x) = - \frac{1}{2} e^{-x^2}, k(x) = x$, then

$$ 
\int_{-b}^{b} x^2e^{-x^2} =
\int_{-b}^{b} h'(x) k(x) \\
= h(b)k(b) - h(-b)k(-b) - \int_{-b}^{b} (- \frac{1}{2} e^{-x^2}) dx \\
= (-e^{-b^2} \cdot (b)) - (-e^{-b^2} \cdot (-b)) +
\int_{-b}^{b} \frac{1}{2} e^{-x^2} dx
$$

So

$$ 
\lim_{b \to \infty} \int_{0}^{b^2} t^{1/2} e^{-t} dt \\
= \lim_{b \to \infty} \int_{-b}^{b} e^{-x^2} dx \\
= \frac{1}{2} \sqrt[]{\pi}
$$

$\square$

(c) Now use (a) and (b) to conjecture a striking relationship between the
factorial function and a well-known function from trigonometry.

**Solution**:

$$ 
(1/2)! = 1/2 \cdot (-1/2)! \\
(-1/2)! = 2 \cdot (1/2)!
$$

So

$$ 
g(1/2) = \frac{1/2}{(1/2)! \cdot 2 \cdot (1/2)!} \\
= \frac{1}{\pi}
$$

So my conjecture is

$$ 
\frac{x}{x!(−x)!} = \frac{1}{\pi} \sin (\pi x)
$$

$\square$

### Exercise 8.4.23.

As a parting shot, use the value for $(1/2)!$ and the Gauss
product formula in equation (9) to derive the famous product formula for $π$
discovered by John Wallis in the 1650s

$$ 
\frac{\pi }{2}
=\lim_{n \to \infty}
\left( \frac{2 \cdot 2}{1 \cdot 3} \right) 
\left( \frac{4 \cdot 4}{3 \cdot 5} \right) 
\left( \frac{6 \cdot 6}{5 \cdot 7} \right) 
\cdots 
\left( \frac{2n \cdot 2n}{(2n - 1) \cdot (2n + 1)} \right) 
$$

**Proof**:

$$ 
x! =
\lim_{n \to \infty} 
\frac{n^{x}n!}{(x+1)(x+2)\cdots (x+n)}
$$

We plug $x = 1/2$, and take square on both side. Then we have

$$
\frac{\pi}{2} =
\lim_{n \to \infty}
\left( \frac{2 \cdot 2}{1 \cdot 3} \right) 
\left( \frac{4 \cdot 4}{3 \cdot 5} \right) 
\left( \frac{6 \cdot 6}{5 \cdot 7} \right) 
\cdots 
\left( \frac{2n \cdot 2n}{(2n - 1) \cdot (2n + 1)} \right)
\cdot
\frac{2n}{2n+1} \\
=
\lim_{n \to \infty}
\left( \frac{2 \cdot 2}{1 \cdot 3} \right) 
\left( \frac{4 \cdot 4}{3 \cdot 5} \right) 
\left( \frac{6 \cdot 6}{5 \cdot 7} \right) 
\cdots
\lim_{n \to \infty}
\frac{2n}{2n+1} \\
=
\lim_{n \to \infty}
\left( \frac{2 \cdot 2}{1 \cdot 3} \right) 
\left( \frac{4 \cdot 4}{3 \cdot 5} \right) 
\left( \frac{6 \cdot 6}{5 \cdot 7} \right)
\cdots 
\left( \frac{2n \cdot 2n}{(2n - 1) \cdot (2n + 1)} \right)
$$

$\square$
