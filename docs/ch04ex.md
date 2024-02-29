# Chapter 04 Functional Limits and Continuity

## 4.2 Functional Limits

### 4.2.3

Review the definition of Thomae’s function $t(x)$ from Section 4.1.

a. Construct three different sequences $(x_n)$, $(y_n)$ and $(z_n)$ , each of which
converges to 1 without using the number 1 as a term in the sequence.

Solution: consider

$$ 
x_n = \left\{ 1 + (1/2)^n \right\} \\
y_n = \left\{ 1 + (1/3)^n \right\} \\
z_n = \left\{ 1 + (1/4)^n \right\} \\
$$

b. Now, compute $\lim t(x_n)$, $\lim t(y_n)$, and $\lim t(z_n)$.

Solution:

$$
\lim t(x_n) = (1/2)^n \\
\lim t(y_n) = (1/3)^n \\
\lim t(z_n) = (1/4)^n \\
$$

c. Make an educated conjecture for $\lim_{x→1} t(x)$, and use Definition 4.2.1B to verify the claim. (Given $\epsilon > 0$, consider the set of points $\{x ∈ R : t(x) ≥ \epsilon \}$.
Argue that all the points in this set are isolated.)

Proof: For any $x$, if $x$ is irrational, then $t(x) = 0 < \epsilon$. If $x$ is rational, then assume $x = p/q$ and $1/N < \epsilon$. Then for any $n$, $p/q$ lies between $[k_n/n, (k_n+1)/n]$. For $n = 1, \dots, N$, we obtain $2n$ points. Let 

$$ 
\delta = \min \left\{ |\frac{k_n}{n} - x| \ne 0, |\frac{k_{n}+1}{n} - x| \ne 0,
n = 1 \dots N
\right\}
$$

And for any rational $y \in V_{\delta }(x), y \neq x$, it's denominator must be bigger than $N$, so $t(y) < \epsilon$. So $x$ is an isolated point.

### 4.2.4

Consider the reasonable but erroneous claim that

$$
\lim_{x→10}
\frac{1}{[[x]]} = 
\frac{1}{10}.
$$

a. Find the largest $δ$ that represents a proper response to the challenge of $\epsilon = 1/2$.

Solution:

$$ 
1/10 + 1/2 = 3/5 \\
1/10 - 1/2 = -2/5 \\
$$

So in this case if $\delta =8$, then $10 - 8 = 2$, $f(2) = 1/2 < 3/5$. And $10 + 8 = 18, f(18) = 1/17 < 3/5$.

b. Find the largest $δ$ that represents a proper response to $\epsilon = 1/50$.

Solution: $\delta = 1$. $1/10 - 1/9 = 1/90, 1/10 - 1/10 = 0$.

(c) Find the largest $\epsilon$ challenge for which there is no suitable $\delta$ response possible.

Solution: $1/90$.

### 4.2.6

Decide if the following claims are true or false, and give short
justifications for each conclusion.

(a) If a particular $δ$ has been constructed as a suitable response to a particular $\epsilon$ challenge, then any smaller positive $δ$ will also suffice.

Solution: Yes. Assume $\delta_0 < \delta$ then $V_{\delta_0}(x) \subset V_{\delta}(x)$, so any smaller positive $δ$ will also suffice.

(b) If $\lim_{x→a} f(x) = L$ and $a$ happens to be in the domain of $f$, then $L = f(a)$.

False: Consider Thomae’s function, $\lim_{x→1} f(x) = 0$, but $f(1) = 1$.

(c) If $\lim_{x→a} f(x) = L$, the If $\lim_{x→a} 3[f(x)-2]^2 = 3(L-2)^2$.

True: Corollary 4.2.4 (Algebraic Limit Theorem for Functional Limits).

(d) If $\lim_{x→a} f(x) = 0$, then $\lim_{x→a} f(x)g(x) = 0$ for any function $g$ (with domain equal to the domain of $f$.)

False: consider $f(x) = x - 1, g(x) = \frac{1}{x-1}$, then $\lim_{x→1} f(x)g(x) = 1$.

### 4.2.7

Let $g : A \rightarrow \mathbb{R}$ and assume $f$ is a bounded function on $A$ in the sense that there exists $M > 0$ satisfying $|f(x)| ≤ M$ for all $x ∈ A$. Show that if $\lim_{x→c} g(x) = 0$, then $\lim_{x→c} g(x)f(x) = 0$ as well.

Proof: Given $\epsilon$, we can find $\delta$ such that $\forall x \in V_{\delta}(c), g(x) < \frac{\epsilon}{M}$, then

$$ 
|f(x)g(x) - 0| = |f(x)g(x)| = |f(x)| |g(x)|
< M \frac{epsilon}{M} = \epsilon
$$

So $\lim_{x→c} g(x)f(x) = 0$.

### 4.2.8

Compute each limit or state that it does not exist. Use the tools developed in this section to justify each conclusion.

(a)

$$ 
\lim_{x \to 2} \frac{|x-2|}{x-2}
$$

Solution: dose not exist. Consider

$$ 
x_n = 2 + \frac{1}{n} \\
y_n = 2 - \frac{1}{n}
$$

Then $\lim_{n \to \infty} x_n = 1$ and $\lim_{n \to \infty} y_n - -1$. Based on Corollary 4.2.5, the limit does not exist.

(b)

$$ 
\lim_{x \to \frac{7}{4}} \frac{|x-2|}{x-2} $$

Solution: -1.

(c)

$$ \lim_{x \to 0} (-1)^{[[1/x]]} $$

Solution: consider

$$ 
x_n = \frac{1}{2n}\\
y_n = \frac{1}{2n+1} $$

Then $\lim_{n \to \infty} x_n = 1$ and $\lim_{n \to \infty} y_n - -1$. Based on Corollary 4.2.5, the limit does not exist.

(d)

$$ \lim_{x \to 0} \sqrt[3]{x} (-1)^{[[1/x]]}$$

Solution: 0. $\lim_{x \to 0} \sqrt[3]{x} = 0$. and $|(-1)^{[[1/x]]}| \leq 1$. Based on exercise 4.2.7, it's 0.

### 4.2.9 (Infinite Limits)

Definition: $\lim_{x \to c} f(x) = \infty$ means that for all $M > 0$ we can find a $δ > 0$ such that whenever $0 < |x − c| < δ$, it follows that $f(x) > M$.

(a) Show $\lim_{x \to 0} 1/x^2 = \infty$ in the sense described in the previous definition.

Proof: Given $M > 0$, let $\delta = 1/\sqrt{M}$, then when $0 < |x| < 1/\sqrt{M}$, $1/x^2 > M$.

(b) Now, construct a definition for the statement $\lim_{x \to \infty} f(x) = L$. Show $\lim_{x \to \infty} 1/x = 0$.

Solution: for all $\epsilon > 0$, we can find a $N$ such that whenever $x > N$, $f(x) \in V_{\epsilon}(L)$.

To prove $\lim_{x \to \infty} 1/x = 0$, given $\epsilon > 0$, let $N = 1/\epsilon$.

(c) What would a rigorous definition for $\lim_{x \to \infty} f(x) = \infty$  look like? Give an example of such a limit.

Solution: It means that for all $M > 0$ we can find a $N > 0$ such that whenever $x > N$, it follows that $f(x) > M$. One example is $f(x) = x$.

### 4.2.10 (Right and Left Limits)

(a) Give a proper definition in the style of Definition 4.2.1 for the right-hand and left-hand limit statements:

$$ 
\lim_{x \to a^+} f(x) = L
\text{ and}
\lim_{x \to a^-} f(x) = L
$$

Solution: $\lim_{x \to a^+} f(x) = L$ means for all $\epsilon > 0$, we can find $\delta$, such that whenever $0 < x - a < \delta$, $|f(x) - L| < \epsilon$.

(b) Prove that $\lim_{x \to a} f(x) = L$ if and only if both the right and left-hand limits equal $L$.

Proof:

* $\Rightarrow$ if $\lim_{x \to a} f(x) = L$, then for any $\epsilon > 0$, we can find $\delta$, such that whenever $|x-a| < \delta$, $|f(x)- L| < \epsilon$. Then, we find $\delta$ such that whenever $0 < x - a < \delta$, $|f(x) - L| < \epsilon$. So $\lim_{x \to a^+} f(x) = L$.
* $\Leftarrow$ if $\lim_{x \to a^+} f(x) = L$ and $\lim_{x \to a^-} f(x) = L$. Then given $\epsilon > 0$, we can find $\delta^+, \delta^-$ such that as long as $0 < x - a < \delta^+$ or $0 < a - x < \delta^-$, $|f(x) - L| < \epsilon$. Let $\delta = \min \left\{ \delta^+, \delta^- \right\}$. 

### 4.2.11 (Squeeze Theorem).

Let $f, g, h$ satisfy $f(x) \leq g(x) \leq h(x)$ for all $x$ in some common domain $A$. if $\lim_{x \to c} f(x) = L$ and $\lim_{x \to c} h(x) = L$ at some limit point $c$ of $A$, show $\lim_{x \to c} g(x) = L$.

Proof: Given any sequence $(x_n) \rightarrow c$, $f(x_n) \leq g(x_n) \leq h(x_n)$, so $\lim_{n \to \infty} g(x_n) = L$. According to Theorem 4.2.3, $\lim_{x \to c} g(x) = L$.

## 4.3 Continuous Functions

### 4.3.3 

(a) Supply a proof for Theorem 4.3.9 using the $\epsilon–δ$ characterization of continuity.

Proof: Let $d = f(c)$. Since $g$ is continuous at $d$, then given any $\epsilon > 0$, we can find 
$V_{\delta }(d)$, as long as $x \in V_{\delta }(d)$, $g(x) \in V_{\epsilon }(g(d))$.

And since $f$ is continuous at $c$, then we can find $\zeta > 0$, as long as $x \in V_{\zeta }(c)$, $f(x) \in V_{\delta }(d)$. And in turn, $g(f(x)) \in V_{\epsilon}(g(f(c))$. So $g \circ f$ is continuous at $c$.

### 4.3.12

Let $F ⊆ R$ be a nonempty closed set and define
$g(x) = \inf\{|x − a| : a ∈ F\}$.
Show that $g$ is continuous on all of $\mathbf{R}$ and $g(x) \neq 0$ for all $x \not\in F$.

Proof:

* If $c \in F$, then $g(c) = 0$, $|g(x) - g(c)| = |g(x)| \leq |x - c|$. So $g$ is continuous at $c$. 
* If $c \not\in F$, then we can find $x_1, x_2 \in F$ such that $c \in (x1, x2) \cap F = \emptyset$. So $g(c) = \min \left\{ c - x1, x2 - c \right\} \neq 0$. Choose $\delta < \min \left\{ c - x1, x2 - c \right\}$, then $|g(x) - g(c)| \leq  |x - c|$, so $g(x)$ is also continuous at $c \not\in F$.  