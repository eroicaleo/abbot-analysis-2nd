# Chapter 04 Functional Limits and Continuity

## 4.2 Functional Limits

***Definition 4.2.1 (Functional Limit).*** Let $f : A \rightarrow \mathbb{R}$, and let $c$ be a limit point of the domain $A$. We say that $\lim_{x \to c} f(x) = L$ provided that, for all $\epsilon > 0$, there exists a $\delta > 0$ such that whenever $0 < |x - c| < \delta$ and $x \in A$ it follows that $|f(x) - L| < \epsilon$.

***Definition 4.2.1B (Functional Limit: Topological Version).*** Let $f : A \rightarrow \mathbb{R}$, and let $c$ be a limit point of the domain $A$. We say that $\lim_{x \to c} f(x) = L$ provided that, for every $\epsilon$-neighborhood $V_{\epsilon}(L)$, there exists a $\delta$-neighborhood $V_{\delta}(c)$ around $c$ with the property that for all $x \in V_{\delta}(c)$ different from $c$ with $x \in A$ it follows that $f(x) \in V_{\epsilon}(L)$.

***Theorem 4.2.3 (Sequential Criterion for Functional Limits).*** Given a function $f : A \rightarrow \mathbb{R}$, and a limit point $c$ of $A$, the following two statements are equivalent:

(i) $\lim_{x \to c} f(x) = L$

(ii) For all sequences $(x_n) \subseteq A$ satisfying $x_n \neq c$ and $(x_n) \rightarrow c$, it follows $f(x_n) \rightarrow L$.

Summry of proof:

* $\Rightarrow$: Given $(x_n) \rightarrow c$, and $\epsilon > 0$.
Since $\lim_{x \to c} f(x) = L$, we can find $V_{\delta}(c)$, as long as $x \in V_{\delta}(c)$, $|f(x) - L| < \epsilon$. Since $(x_n) \rightarrow c$, we can find $N$, when $n > N$, $x_n \in V_{\delta}(c)$. So $|f(x_n) - L| < \epsilon$. Then $f(x_n) \rightarrow L$.
* $\Leftarrow$: Use contradiction. Assume ii holds, but $\lim_{x \to c} f(x) \ne L$. Then we can find an $\epsilon$, given any $\delta$, we can find $x_{\delta}$, such that $f(x_{\delta}) \notin V_{\epsilon}(L)$. Now let $\delta_n = 1/n$. Then we can construct $(x_n) \rightarrow c$, and $f(x_n) \not\rightarrow L$, so we have an contradiction.

***Corollary 4.2.4 (Algebraic Limit Theorem for Functional Limits).***

***Corollary 4.2.5 (Divergence Criterion for Functional Limits).*** Let $f$ be a function defined on $A$, and let $c$ be a limit point of $A$. If there exist two
sequences $(x_n)$ and $(y_n)$ in $A$ with $x_n \neq c$ and $y_n \neq c$ and $\lim x_n = \lim y_n = c$ but $\lim f(x_n) \neq \lim f(y_n)$, then we can conclude that functional limit $\lim_{x \to c} f(x)$ does not exist. 

## 4.3 Continuous Functions

***Definition 4.3.1 (Continuity).*** A function $f: A \rightarrow \mathbb{R}$ *is continuous at a point* $c \in A$ if for all $\epsilon > 0$, there exists a $\delta > 0$ such that whenever $|x-c| < \delta$ (and $x \in A$) it follows that $|f(x) - f(c)| < \epsilon$.

If f is continuous at every point in the domain $A$, then we say that $f$ is continuous on $A$.

***Theorem 4.3.2 (Characterizations of Continuity).*** Let $f: A \rightarrow \mathbb{R}$ and $c \in A$. A function $f$ is continuous at a point $c$ if and only if any one of the following
three conditions is met:

i. for all $\epsilon > 0$, there exists a $\delta > 0$ such that whenever $|x-c| < \delta$ (and $x \in A$) it follows that $|f(x) - f(c)| < \epsilon$.

ii. for all $V_{\epsilon}(f(c))$, there exists a $V_{\delta}(c)$ such that $x \in V_{\delta}(c)$ and $x \in A$ then $f(x) \in V_{\epsilon}(f(c))$.

iii. For all $(x_n) \rightarrow c$ with $x_n \in A$, it follows $f(x_n) \rightarrow f(c)$.

If $c$ is a limit point of $A$, then the above conditions are equivalent to

iv. $\lim_{x \to c} f(x) = f(c)$.

Summary of proof:

* The equivalence of (i) and (iii). Use similar argument in theorem 4.2.3.

***Corollary 4.3.3 (Criterion for Discontinuity).*** Let $f: A \rightarrow \mathbb{R}$ and $c \in A$ be a limit point of $A$. If there exists a sequence $(x_n) \subseteq A$ where $(x_n) \rightarrow c$ but such that $f(x_n)$ does not converge to $f(x)$, we may conclude that $f$ is not continuous at $c$.

***Theorem 4.3.4 (Algebraic Continuity Theorem).***

* $kf(x)$ is continuous at $c$ for all $k ∈ R$;
* $f(x) + g(x)$ is continuous at $c$.
* $f(x)g(x)$
* $f(x)/g(x)$

***Example 4.3.5.*** All polynomials are continuous on $\mathbb{R}$.

***Example 4.3.6.*** 

$$ g(x) = 
\begin{cases}
    x \sin (1/x) &\text{if } x \neq 0\\
    0            &\text{if } x = 0\\
\end{cases}  $$

* To see $g(x)$ is continuous at 0, we can see $|g(x) - 0| = |x \sin (1/x)| \leq |x|$. So given $\epsilon$, we just need to set $\delta = \epsilon$.

***Example 4.3.7.*** The greatest integer function $h(x) = [[x]]$.

* When $m \in \mathbf{Z}$, consider the sequence $(x_n) = m-1/n$. Then $(x_n) \rightarrow m-1 \neq m = h(m)$.
* When $c \not\in \mathbf{Z}$, let $\delta = \min \left\{ c - n, (n+1) - c \right\}$, then $h(x) = h(c) = n$.

***Theorem 4.3.9 (Composition of Continuous Functions).*** Given $f : A→R$ and $g : B → R$, assume that the range $f(A) = {f(x) : x ∈ A}$ is contained in the domain $B$ so that the composition $g ◦ f(x) = g(f(x))$ is defined on $A$.

If $f$ is continuous at $c ∈ A$, and if $g$ is continuous at $f(c) ∈ B$, then $g ◦ f$ is continuous at $c$.

## 4.4 Continuous Functions on Compact Sets

***Theorem 4.4.1 (Preservation of Compact Sets).*** Let $f : A → R$ be continuous on $A$. If $K ⊆ A$ is compact, then $f(K)$ is compact as well.

* Proof: Assume $(y_n)$ is a sequence in $f(K)$. We can find $(x_n)$ such that $f(x_n) = y_n$. Since $K$ is compact, there is a subsequence $(x_{n_k}) \rightarrow x$. Because $f$ is continuous at $x$, then $\lim_{n_k \to \infty} y_{n_k} = f(x) \in f(K)$. So
we find subsequence $(y_{k_n}) \rightarrow f(x)$. So $f(K)$ is compact.

***Theorem 4.4.2 (Extreme Value Theorem).*** If $f : K → R$ is continuous on a compact set $K ⊆ R$, then $f$ attains a maximum and minimum value. In other words, there exist $x_0,x_1 ∈ K$ such that $f(x_0) ≤ f(x) ≤ f(x_1)$ for all $x ∈ K$.

***Definition 4.4.4 (Uniform Continuity).*** A function $f : A → R$ is uniformly continuous on $A$ if for every $ε > 0$ there exists a $δ > 0$ such that for all $x, y ∈ A$, $|x−y|<δ$ implies $|f(x)−f(y)|<ε$.

***Theorem 4.4.5 (Sequential Criterion for Absence of Uniform Continuity).*** A function $f : A → R$ fails to be uniformly continuous on $A$ if and only if there exists a particular $ε_0 > 0$ and two sequences $(x_n)$ and $(y_n)$ in A satisfying
$|x_n − y_n|→0$ but $|f(x_n)−f(y_n)|≥ε_0$.
