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

### 4.3.4

Assume $f$ and $g$ are defined on all of $\mathbf{R}$ and that
$\lim_{x \to p} f(x) = q$ and $\lim_{x \to q} g(x) = r$.

(a) Give an example to show that it may not be true that

$$ \lim_{x \to p} g(f(x)) = r. $$

Let $f$ be the Modified Dirichlet Function, i.e.

$$ f(x) =
\begin{cases}
    x &\text{if } x \in \mathbf{Q} \\
    0 &\text{if } x \not\in \mathbf{Q} \\
\end{cases}  $$

Let $g(x)$ be

$$ 
g(x) =
\begin{cases}
    1 &\text{if } x = 0 \\
    0 &\text{if } x \neq 0 \\
\end{cases} 
$$

Assume $(x_n) \rightarrow 0$ and $x_n$ are all irrational numbers.
Then $g(f(x_n)) \rightarrow 1$.

On the other hand, $(y_n) \rightarrow 0$ and $y_n$ are all rational numbers, so $g(f(y_n)) \rightarrow 0$.

$\lim_{x \to p} g(f(x))$ does not exist at all.

(b) Show that the result in (a) does follow if we assume $f$ and $g$ are continuous.

Proof: This is Theorem 4.3.9.

(c) Does the result in (a) hold if we only assume $f$ is continuous? How about if we only assume that $g$ is continuous?

Proof: if only $f$ is continuous, then (a) does not hold. Let

$$ 
f(x) = x \\
g(x) =
\begin{cases}
    1 &\text{if } x = 0 \\
    0 &\text{if } x \neq 0 \\
\end{cases} 
$$

Then $\lim_{x \to 0} g(f(x)) = 0$, but $g(f(0)) = 1$. So $g(f(x))$ is not continuous at $0$.

The above just proves a different thing.

Now if only $g$ is continuous. Let

$$ 
f(x) = 
\begin{cases}
    1 &\text{if } x = 0 \\
    0 &\text{if } x \neq 0 \\
\end{cases} \\
g(x) = x
$$

Then $\lim_{x \to 0} g(f(x)) = 0$, but $g(f(0)) = 1$. So $g(f(x))$ is not continuous at $0$.

### 4.3.5

Show using Definition 4.3.1 that if $c$ is an isolated point of $A ⊆ \mathbf{R}$, then $f : A → \mathbf{R}$ is continuous at $c$.

Proof: Since $c$ is an isolated point of $A$, there is a $\delta$, such that $V_{\delta_0}(c) \cap A = \left\{ c \right\}$. Given any $\epsilon > 0$, as long as $|x - c| < \delta_0$,
$|f(x) - f(c)| = |f(c) - f(c)| = 0 < \epsilon$ $\square$.

### 4.3.6

Provide an example of each or explain why the request is impossible.

(a) Two functions $f$ and $g$, neither of which is continuous at $0$ but such that $f(x)g(x)$ and $f(x) + g(x)$ are continuous at $0$.

Solution: Consider

$$f(x) = 
\begin{cases}
    1 &\text{if } x = 0 \\
    0 &\text{if } x \neq 0 \\
\end{cases} \\
$$

and

$$ 
g(x) = 
\begin{cases}
    1 &\text{if } x \neq 0 \\
    0 &\text{if } x = 0 \\
\end{cases} \\
$$

Then $f(x)g(x) = 0$ and $f(x) + g(x) = 1$ are continuous everywhere. 

### 4.3.10

Observe that if $a$ and $b$ are real numbers, then

$$\max \left\{ a, b \right\} = \frac{1}{2} [(a+b)+|a-b|].$$


1. show that if $f_1, f_2, \dots, f_n$ are continuous functions, then $g(x) = \max \left\{ f_1(x), f_2(x), \dots f_n(x) \right\}$ is a continuous function.

Proof: If $f(x)$ is a continuous function and given $c$, and $\epsilon > 0$, we can find $\delta > 0$, if $x \in V_{\delta }(c)$, then $|f(x) - f(c)| < \epsilon$. Since $||f(x)| - |f(c)|| \le |f(x) - f(c)| < \epsilon$, so $|f(x)|$ is also continuous function.

Then $g(x) = \max \left\{ f_1(x), f_2(x) \right\}= \frac{1}{2} [(f_1(x) + f_2(x)) + |f_1(x) - f_2(x)|]$ is also continuous.

Then we can use induction to see it's true for any $n$.

* another approach

For $c$, assume $g(c) = \max \left\{ f_1(c), f_2(c), \dots f_n(c) \right\} = f_1(c)$. Assume $(x_n) \rightarrow c$, and assume $(x_{n_k})$ is a subsequence and $g(x_{n_k}) = f_2(x_{n_k})$. Since $f_2$ is continuous, we have $(f_2(x_{n_k})) \rightarrow f_2(c)$. Since $\max \left\{ f_1(c), f_2(c), \dots f_n(c) \right\} = f_1(c)$, we have $f_1(c) \geq f_2(c)$. Since $f_1(x_{n_k}) \leq f_2(x_{n_k})$ and $(f_1(x_{n_k})) \rightarrow f_1(c)$, we have $f_1(c) \leq f_2(c)$. So $f_1(c) = f_2(c)$. This means $g(x_n) \rightarrow g(c)$. So $g(x)$ is continuous. 

2. Let’s explore whether the result in (a) extends to the infinite case. For each $n ∈ \mathbf{N}$, define $f_n$ on $\mathbf{R}$ by

$$ 
f_n(x) =
\begin{cases}
    1 &\text{if } |x| \geq 1/n \\
    n|x| &\text{if } |x| < 1/n \\
\end{cases}
$$

Now explicitly compute $h(x) = \sup \left\{f_1(x), f_2(x), f_3(x), \dots\right\}$.

Solution:

$$ 
h(x) = 
\begin{cases}
    1 &\text{if } x \neq 0 \\
    0 &\text{if } x = 0 \\
\end{cases}
$$

So $h(x)$ is not continuous at $0$.

### 4.3.11 (Contraction Mapping Theorem).

Let $f$ be a function defined on all of $\mathbf{R}$, and assume there is a constant $c$ such that $0 <c< 1$ and

$$ \left| f(x) - f(y) \right| \leq c|x-y| $$

for all $x, y \in \mathbf{R}$.

i. Show that $f(x)$ is continuous on $\mathbf{R}$.

Proof: Given $\epsilon$, let $\delta = \epsilon / c$. Then $\left| f(x) - f(y) \right| \leq c|x-y| < c (\epsilon / c) = \epsilon$.

ii. Pick some point $y_1 ∈ \mathbf{R}$ and construct the sequence

$$ (y_1, f(y_1), f(f(y_1)), \dots)$$

In general, if $y_{n+1} = f(y_n)$, show that the resulting sequence $(y_n)$ is a Cauchy sequence. Hence we may let $y = \lim y_n$.

Proof: First, we prove $(y_n)$ is bounded. Assume $|y_2 - y_1| = M$, then $|y_2| \leq \left| y_1 \right| + M$.

$$ 
\left| y_3 - y_2 \right| \leq c |y_2 - y_1| = cM \\
|y_3| \leq |y_2| + cM \leq |y_1| + (1 + c)M \\
|y_n| \leq |y_1| + \frac{1}{1 - c}M = K
$$

So assume $n > m$, 

$$ 
|y_n - y_m| = c^{m-1} | y_{n-m+1} - y_1| \leq c^{m-1} 2K
$$

So $(y_n)$ is Cauchy sequence.

iii. Prove that $y$ is a fixed point of $f$ (i.e., $f(y) = y$) and that it is unique in this regard.

Proof: Assume $f(y) \neq y$. Since $(y_n) \rightarrow y$, we can find $y_1$ and $y_2 = f(y_1)$, which are close enough to $y$. And $|y_1 - y| < \epsilon$, $|y_2 - y| < \epsilon$ but $|y_2 - f(y)| > \epsilon$. Then $\epsilon < |y_2 - f(y)| = |f(y_1)-f(y)| \leq c|y_1-y| < |y_1 - y| < \epsilon$, we have a contradiction.

iv. Finally, prove that if $x$ is any arbitrary point in , then the sequence
$(x, f(x), f(f(x)),...)$ converges to $y$ defined in (2).

Proof: Assume $(x_n) \rightarrow x$ and $(y_n) \rightarrow y$, then
$|x - y| \le |x - x_n | + |x_n - y_n | + | y_n - y | < \epsilon +
c^n|x - y| + \epsilon$ and can be arbitrarily small. So $x = y$. 

### 4.3.12

Let $F ⊆ R$ be a nonempty closed set and define
$g(x) = \inf\{|x − a| : a ∈ F\}$.
Show that $g$ is continuous on all of $\mathbf{R}$ and $g(x) \neq 0$ for all $x \not\in F$.

Proof:

* If $c \in F$, then $g(c) = 0$, $|g(x) - g(c)| = |g(x)| \leq |x - c|$. So $g$ is continuous at $c$. 
* If $c \not\in F$, then we can find $x_1, x_2 \in F$ such that $c \in (x1, x2) \cap F = \emptyset$. So $g(c) = \min \left\{ c - x1, x2 - c \right\} \neq 0$. Choose $\delta < \min \left\{ c - x_1, x_2 - c \right\}$, then $|g(x) - g(c)| \leq  |x - c|$, so $g(x)$ is also continuous at $c \not\in F$.

### 4.3.14

(a) Let $F$ be a closed set. Construct a function $f : \mathbf{R} \mapsto \mathbf{R}$, such that the set of points where $f$ fails to be continuous is precisely $F$. (The concept of the interior of a set, discussed in Exercise 3.2.14, may be useful.)

Solution: consider

$$ f(x) = 
\begin{cases}
    0 &\text{if } x \not\in F\\
    1 &\text{if } x \in F \cap \mathbf{Q}\\
    -1 &\text{if } x \in F \cap \overline{\mathbf{Q}}\\
\end{cases}
$$

If $x \in E^o$, then we can find $(x-\epsilon , x+\epsilon) \subset F$, since both $\mathbf{Q}$ and  