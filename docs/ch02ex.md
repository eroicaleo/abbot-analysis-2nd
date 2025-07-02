# Chapter 2 Sequences and Series

## 2.8 Double Summations and Products of Infinite Series

We discovered in section 2.1 that there is a dangerous ambiguity in how we might define $\sum_{i,j = 1}^{\infty}a_{ij}$

Performing the sum over first one of the variables and then the
other is referred to as an *iterated* summation.

In our specific example, summing the rows first and then taking 
the sum of these totals produced a diﬀerent result
than first computing the sum of each column and adding these sums together. In short,

$$ 
\sum_{j = 1}^{\infty} \sum_{i = 1}^{\infty} a_{ij}
\not =
\sum_{i = 1}^{\infty} \sum_{j = 1}^{\infty} a_{ij}
$$

One natural idea
is to calculate a kind of partial sum by adding together finite numbers of terms in larger and larger “rectangles” in the array;
that is, for $m,n ∈ \mathbf{N}$, set

$$
\tag{1} 
s_{mn} = \sum_{i = 1}^{m} \sum_{j = 1}^{n} a_{ij}
$$

The order of the sum here is irrelevant because the sum is finite.
If the sequence $(s_{nn})$ converges, for instance, we
might wish to define

$$ 
\sum_{i,j = 1}^{\infty}a_{ij} = \lim_{n \to \infty} s_{nn}
$$

### Exercise 2.8.1.

Using the particular array $(a_{ij})$ from Section 2.1, compute
$\lim_{n \to \infty} s_{nn}$. How does this value compare to the
two iterated values for the sum already computed?

**Solution**:

Consider this example in section 2.1

$$ 
a_{ij} =
\begin{cases}
    1/2^{j-i} &\text{if } j > i\\
    -1 &\text{if } j = i\\
    0 &\text{if } j < i\\
\end{cases} 
$$

Then we have

$$ 
s_{11} = -1 \\
s_{22} = -\frac{3}{2} \\
s_{33} = -\frac{7}{4} \\
s_{44} = -\frac{15}{8} \\
$$

Then we have $\lim_{n \to \infty} s_{nn} = -2$. We have already 
seen

$$ 
\sum_{i = 1}^{\infty} \sum_{j = 1}^{\infty} a_{ij} = 0 \\
\sum_{j = 1}^{\infty} \sum_{i = 1}^{\infty} a_{ij} = -2 \\
$$

$\square$

### Exercise 2.8.2.

Show that if the iterated series

$$ 
\sum_{i = 1}^{\infty} \sum_{j = 1}^{\infty} |a_{ij}|
$$

converges (meaning that for each fixed $i ∈ N$ the series 
$\sum_{j = 1}^{\infty} |a_{ij}|$ converges to
some real number $b_i$, and the series $\sum_{i = 1}^{\infty} b_i$
convergesas well), then the iterated series

$$ 
\sum_{i = 1}^{\infty} \sum_{j = 1}^{\infty} a_{ij}
$$

converges.

**Proof**:

Since $\sum_{j = 1}^{\infty} |a_{ij}|$ converges, do does
$\sum_{j = 1}^{\infty} a_{ij}$. Assume $c_i = \sum_{j = 1}^{\infty} a_{ij}$, then $|c_i| < b_i$.

Since $\sum_{i = 1}^{\infty}b_i$ converges, so does
$\sum_{i = 1}^{\infty}c_i$.

So the iterated series

$$ 
\sum_{i = 1}^{\infty} \sum_{j = 1}^{\infty} a_{ij}
$$

converges.

$\square$

### Theorem 2.8.1.

Let $\{a_{ij} : i, j \in \mathbf{N}\}$
be a doubly indexed array of real numbers. If

$$ 
\sum_{i = 1}^{\infty} \sum_{j = 1}^{\infty} |a_{ij}|
$$

converges, then both
$\sum_{i = 1}^{\infty} \sum_{j = 1}^{\infty} a_{ij}$ 
and
$\sum_{j = 1}^{\infty} \sum_{i = 1}^{\infty} a_{ij}$
converge to the same value. Moreover,

$$ 
\lim_{n \to \infty} s_{nn} =
\sum_{i = 1}^{\infty} \sum_{j = 1}^{\infty} a_{ij}
= \sum_{j = 1}^{\infty} \sum_{i = 1}^{\infty} a_{ij}
$$

where $s_{nn} = \sum_{i = 1}^{n} \sum_{j = 1}^{n} a_{ij}$.

**Proof**: In the same way that we defined the rectangular partial sums smn above in equation (1), define

$$ 
t_{mn} = \sum_{i = 1}^{m} \sum_{j = 1}^{n} |a_{ij}|
$$

### Exercise 2.8.3.

(a) Prove that $(t_{nn})$ converges.

**Proof**:

Let $b_i = \sum_{j = 1}^{\infty} |a_{ij}|$, so $\sum_{i = 1}^{\infty} b_i$ converges. Since $0 \leq t_{nn} < \sum_{i = 1}^{n} b_i$, then $(t_{nn})$ converges.

$\square$

(b) Now, use the fact that $(t_{nn})$ is a Cauchy sequence to argue that $(s_{nn})$ converges.

**Proof**: Our goal is to prove $(s_{nn})$ is also a Cauchy
sequence. Assume $m > n$, then

$$ 
|s_{mm} - s_{nn}| = 
\left| 
\sum_{i = 1}^{n} \sum_{j = n+1}^{m} a_{ij} +
\sum_{i = n+1}^{m} \sum_{j = 1}^{n} a_{ij} +
\sum_{i = n+1}^{m} \sum_{j = n+1}^{n} a_{ij}
\right| \\
\leq
\sum_{i = 1}^{n} \sum_{j = n+1}^{m} | a_{ij} | +
\sum_{i = n+1}^{m} \sum_{j = 1}^{n} | a_{ij} | +
\sum_{i = n+1}^{m} \sum_{j = n+1}^{n} | a_{ij} |
= t_{mm} - t_{nn}
$$

So $(s_{nn})$ is also a Cauchy sequence.

$\square$

We can now set

$$ 
S = \lim_{n \to \infty} s_{nn}
$$

Because $\{t_{mn} : m, n \in \mathbf{N}\}$ is bounded above, we can let

$$ 
B = \sup \{t_{mn}: m, n \in \mathbf{N}\}
$$

### Exercise 2.8.4.

(a) Let $ϵ > 0$ be arbitrary and argue that there exists an
$N_1 ∈ N$ such that $m,n ≥ N_1$ implies $B−ϵ
/2 < t_{mn} ≤ B$.

**Proof**: Since $B = \sup \{t_{mn}: m, n \in \mathbf{N}\}$,
then we can find $t_{pq}$, such that
$B−ϵ /2 < t_{mn} ≤ B$. Let $N_1 = \max \{p, q\}$.

Then

$$ 
t_{mn} \geq t_{N_1N_1} \geq t_{pq} > B-\epsilon /2
$$

$\square$

(b) Now, show that there exists an $N$ such that

$$ 
\left| 
s_{mn} - S
 \right|
< \epsilon
$$

for all $m,n \geq N$.

**Proof**: Since $S = \lim_{n \to \infty} s_{nn}$, we can find
$N_2$, if $n > N_2$, then $|s_{nn} - S| < \epsilon / 2$.

Let $N = \max \{N_1, N_2\}$.

$$ 
\left| 
S_{mn} - S
 \right|
= \left| 
S_{mn} - S_{NN} + S_{NN} - s
 \right|
\leq \\
|S_{mn} - S_{NN}| + |S_{NN} - s|
<
|t_{mn} - t_{NN}| + \epsilon / 2 \\
<
\epsilon / 2 + \epsilon / 2 \\
= \epsilon
$$

$\square$

For the moment, consider $m ∈ \mathbf{N}$ to be fixed and write
$s_{mn}$ as

$$ 
s_{mn} =
\sum_{j = 1}^{n} a_{1j} +
\sum_{j = 2}^{n} a_{2j} +
\cdots +
\sum_{j = m}^{n} a_{mj}
$$

Our hypothesis guarantees that for each fixed row $i$, the series
$\sum_{j = 1}^{\infty} a_{ij}$
converges absolutely to some real number $r_i$.

### Exercise 2.8.5.

(a) Show that for all $m \geq N$,

$$ 
\left| 
(r_1 + r_2 + r_3 + \cdots + r_m) - S
 \right| \leq \epsilon
$$

Conclude that the iterated sum
$\sum_{i = 1}^{\infty} \sum_{j = 1}^{\infty} a_{ij}$
converges to $S$.

Proof: For each $n \geq N$, $|s_{nm} - S| < \epsilon$.
Then

$$ 
\lim_{n \to \infty} |s_{nm} - S| = \\
|(r_1 + r_2 + r_3 + \cdots + r_m) - S| \leq \epsilon
$$

Since it holds for $m \geq N$, that means

$$ 
|\sum_{i = 1}^{\infty} \sum_{j = 1}^{\infty} a_{ij} - S| \leq
\epsilon
$$

Since $\epsilon$ can be arbitrary small, the iterated sum
converges to $S$.

(b) Finish the proof by showing that the other iterated sum

$$ 
\sum_{j = 1}^{\infty} \sum_{i = 1}^{\infty} a_{ij}
$$

converges to $S$ as well. Notice that the same argument can be used once it is established that, for each fixed column $j$,
the sum $\sum_{i = 1}^{\infty}a_{ij}$ converges to to some real number $c_j$.

**Proof**:

$$ 
|a_{ij}| < \sum_{j = 1}^{\infty} |a_{ij}| = b_i
$$

Since $\sum_{i = 1}^{\infty} b_i$ converges, so does
$\sum_{i = 1}^{\infty} |a_{ij}|$, so does
$\sum_{i = 1}^{\infty} a_{ij}$.
Then we can assume $\sum_{i = 1}^{\infty} a_{ij} = c_j$.

The rest can follow (a).

$\square$

Given a doubly indexed array $\{a_{ij} : i,j ∈ \mathbf{N}\}$,
let

$$ 
d_2 = a_{11}, d_3 = a_{12} + a_{21}, d_4 = a_{13} + a_{22} +
a_{31}
$$

and in general set

$$ 
d_k = a_{1,k-1} + a_{2, k-2} + \cdots + a_{k-1,1}
$$

### Exercise 2.8.6.

(a) Assuming the hypothesis—andhence the conclusion—of
Theorem 2.8.1, show that $\sum_{k = 2}^{\infty} d_k$
converges absolutely.

**Proof**: Note that $\sum_{k = 2}^{n} |d_k| \leq t_{nn}$,
since $(t_{nn})$ converges, so does $\sum_{k = 2}^{n} |d_k|$.

$\square$

(b) Imitate the strategy in the proof of Theorem 2.8.1 to
show that $\sum_{k = 2}^{\infty} d_k$ converges to
$S = \lim_{n \to \infty} s_{nn}$.

**Proof**: Let 

$$ 
D_n = \sum_{k = 2}^{n} d_k \\
\Delta_n = \sum_{k = 2}^{n} |d_k| \\
$$

Since we can find $N_1$, as long as $n, m > N_1$, we have
$|s_{mn} - S| < \epsilon / 2$ and $|t_{mn} - B| < \epsilon / 2$.

Fix $n, m > N_1$, and let $N = n+m, l > N$.

$$ 
|D_{l} - S| \\
 = |D_{l} - s_{mn} + s_{mn} - S| \\
\leq |D_{l} - s_{mn} | + |s_{mn} - S| \\
< (t_{l-1,l-1} - t_{mn}) + \epsilon / 2 \\
< \epsilon / 2 + \epsilon / 2 = \epsilon / 2
$$

It's better to draw a diagram to understand why
$|D_{l} - s_{mn} | \leq t_{l-1,l-1} - t_{mn}$ holds.

$\square$

### Products of Series

Conspicuously missing from the Algebraic Limit Theorem for Series
(Theorem 2.7.1) is any statement about the product of two 
convergent series. One way to formally carry out the algebra on 
such a product is to write

$$ 
\left( 
\sum_{i = 1}^{\infty}a_i
 \right) 
\left( 
\sum_{j = 1}^{\infty}b_j
 \right) =
(a_1 + a_2 + a_3 + \cdots)
(b_1 + b_2 + b_3 + \cdots)
= \sum_{k = 2}^{\infty}d_k,
$$

where

$$ 
d_k = a_{1}b_{k-1} + a_{2}b_{ k-2} + \cdots + a_{k-1}b_{1}
$$

### Exercise 2.8.7.

Assume that $\sum_{i = 1}^{\infty} a_i$ converges absolutely to $A$, 
and $\sum_{j = 1}^{\infty} b_j$ converges absolutely to $B$.

(a) Show that the iterated sum 
$\sum_{i = 1}^{\infty} \sum_{j = 1}^{\infty} |a_i b_j|$
converges so that we may apply Theorem 2.8.1.

**Proof**: Assume

$$
\sum_{n = 1}^{\infty} |a_n| = C \\
\sum_{n = 1}^{\infty} |b_n| = D \\
$$.

Fix $i$, then $\sum_{j = 1}^{\infty}|a_ib_j| = |a_iD|$.
Then $\sum_{i = 1}^{\infty} |a_iD| = CD$.

$\square$

(b) Let
$s_{nn} = \sum_{i = 1}^{n} \sum_{j = 1}^{n} a_ib_j$,
and prove that $\lim_{n \to \infty} s_{nn} = AB$.
Conclude that

$$ 
\sum_{i = 1}^{\infty} \sum_{j = 1}^{\infty} a_{ij}
=
\sum_{j = 1}^{\infty} \sum_{i = 1}^{\infty} a_{ij}
=
\sum_{k = 2}^{\infty}d_k
$$

where 

$$ 
d_k = a_{1}b_{k-1} + a_{2}b_{ k-2} + \cdots + a_{k-1}b_{1}
$$

**Proof**: Let

$$ 
A_n = \sum_{i = 1}^{n} a_i \\
B_n = \sum_{j = 1}^{n} b_j \\
$$

Then we have

$$ 
\lim_{n \to \infty} A_n = A \\
\lim_{n \to \infty} B_n = B \\
s_{nn} = A_n B_n \\
$$

Then from Theorem 2.3.3 (Algebraic Limit Theorem). (iii)

$$ 
\lim_{n \to \infty} s_{nn} = \lim_{n \to \infty} A_n B_n \\
= \lim_{n \to \infty} A_n \lim_{n \to \infty} B_n = AB
$$

The rest follows Exercise 2.8.5 and 2.8.6.

$\square$
