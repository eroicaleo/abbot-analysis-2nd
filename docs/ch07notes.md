# Chapter 07 The Riemann Integral

## 7.4 Properties of the Integral

### 7.4.2.

Assume $f$ and $g$ are integrable functions on the interval $[a,b]$.

(i) The function $f + g$ is integrable on $[a,b]$ with
$\int_{a}^{b} (f+g) = \int_{a}^{b}f + \int_{a}^{b} g$ 

Proof: Given any $\epsilon$, we can find partition $P$

$$ 
\int_{a}^{b} (f+g) \leq U(f+g, P) = U(f, P) + U(g, P)
< L(f, P) + L(g, P) + \epsilon \\
< \int_{a}^{b} f + \int_{a}^{b} g + \epsilon
$$

On the other hand,

$$ 
\int_{a}^{b} f + \int_{a}^{b} g \leq U(f, P) + U(g, P)
< L(f, P) + L(g, P) + \epsilon
= L(f+g, P) + \epsilon \\
\leq \int_{a}^{b} (f+g) + \epsilon 
$$

So we have $\int_{a}^{b} (f+g) = \int_{a}^{b}f + \int_{a}^{b} g$.

$\square$

(ii) For $k ∈ \mathbf{R}$, the function $kf$ is integrable with $\int_{a}^{b} kf = k \int_{a}^{b} f$.

**Proof**:

$$ 
\int_{a}^{b} kf \leq U(kf, P) = k U(f, P) < k L(f, P) + \epsilon \leq k \int_{a}^{b} f
$$

On the other hand

$$ 
k \int_{a}^{b} f \leq k U(f, P) < k L(f, P) + \epsilon
= L(kf, P) + \epsilon \leq \int_{a}^{b} kf + \epsilon
$$

$\square$

## 7.5 The Fundamental Theorem of Calculus

### Theorem 7.5.1 (Fundamental Theorem of Calculus).

(i) If $f : [a,b] \rightarrow \mathbf{R}$ is integrable, and $F : [a,b] \rightarrow \mathbf{R}$
satisfies $F'(x) = f(x)$ for all $x \in [a, b]$,
then

$$ 
\int_{a}^{b} f = F(b) - F(a).
$$

$\square$

(ii) Let $g:[a, b] \rightarrow \mathbf{R}$ be
integrable, and for $x \in [a, b]$, define

$$ 
G(x) = \int_{a}^{x} g(x)
$$

Then $G$ is continuous on $[a,b]$.
If $g$ is continuous at some point $c ∈ [a,b]$,
then $G$ is diﬀerentiable at $c$ and $G'(c) = g(c)$
.

**Proof**:

(i) Given a partition $P, a = x_0 < x_1 < \cdots < x_n = b$.

$$ 
F(x_{k+1}) - F(x_k) = f(x'_k) (x_{k+1} - x_k)
$$

Since $m_k \leq f(x'_k) \leq M_k$,
then $L(f, P) \leq F(b) - F(a) \leq U(f, P)$,

So $\int_{a}^{b} f = F(b) - F(a)$.

(ii)

$$ 
|G(y) - G(x)| = 
\left| \int_{x}^{y} g(t) \right| 
\leq \int_{x}^{y} |g(t)| \\
\leq M(x - y)
$$

$G$ is Lipschitz and so is uniformly continuous on
$[a,b]$.

For the second part:

$$ 
\left| 
\frac{
    G(x) - G(c)
}{
    x - c
} - g(c)
\right| 
=
\frac{1}{x - c}
\left| 
\int_{c}^{x} g(t) - g(c) (x - c)
 \right| \\
 =
\frac{1}{x - c}
\left| 
\int_{c}^{x} (g(t) - g(c))
 \right| \\
\leq
\frac{1}{x - c}
\int_{c}^{x} \left| (g(t) - g(c)) \right| \\
\leq \frac{1}{x - c} \epsilon (x - c) = \epsilon.
$$

$\square$
