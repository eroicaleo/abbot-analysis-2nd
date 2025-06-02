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



