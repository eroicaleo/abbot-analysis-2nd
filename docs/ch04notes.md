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

