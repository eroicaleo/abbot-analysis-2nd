# Chapter 3 Basic Topology of R

## 3.1 Discussion: The Cantor Set

Let

$$
C_0 = [0,1], \\
C_1 = [0, \frac{1}{3}] \cup [\frac{2}{3}, 1], \\
C_2 = [0, \frac{1}{9}] \cup [\frac{2}{9}, \frac{1}{3}]
      \cup [\frac{2}{3}, \frac{7}{9}]
      \cup [\frac{8}{9}, 1], \cdots 
$$

Then we define the Cantor set $C$ be 

$$
C = \cap_{n=0}^\infty C_n
$$

1. We notice $C$ is not empty, because $0 \in C$ and $1 \in C$.
2. We notice if $y$ is an endpoint in $C_n$, then $y \in C_n, \forall n$. Because endpoints are never removed.
3. If we calculate the length that are removed from $[0,1]$, it's $\frac{1}{3} + 2\left( \frac{1}{9} \right) + 4 \left( \frac{1}{27} \right) + \cdots = \frac{\frac{1}{3}}{1 - \frac{2}{3}} = 1$. So the length of $C$ is 0!.
4. We can establish a 1-1 correspondence between $C$ and $\left\{ 0, 1 \right\}$ sequence. So $C$ must be uncountable. The cardinality of $C$ is as large as $\mathbb{R}$.
5. What about $C$'s dimension? $2 = 3^x$, so $x = \log 2 / \log 3$

## 3.2 Open and Closed Sets

Given $a \in \mathbb{R}$ and $\epsilon > 0$, $\epsilon$-*neighborhood* of $a$ is the set

$$
V_{\epsilon}(a) = \{
x \in \mathbb{R} : |x-a| < \epsilon
\} = (a-\epsilon, a+\epsilon)
$$

***Definition 3.2.1*** A set $O \subseteq \mathbb{R}$ is open if for all points $a \in O$ there exists $\epsilon$-neighborhood $V_{\epsilon}(a) \subseteq O$.

***Example 3.2.2***

1. $\mathbb{R}$ is an open set.
2. $(c,d) = \{x \in \mathbb{R} : c < x < d \}$

***Theorem 3.2.3***

1. The union of an arbitrary collection of open sets is open.
2. The intersection of a finite collection of open sets is open.


Summary of proof of 2. Assume $\left\{ O_1, O_2, \cdots, O_n \right\}$ be a finite collection of open sets. Assume $V_{\epsilon_k} (a) \subseteq O_k$. Let $\epsilon = \min \left\{ \epsilon_1, \cdots \epsilon_n \right\}$, then $V_{\epsilon}(a) \subseteq V_{\epsilon_k}(a) \subseteq O_k$.

### Closed Sets

***Definition 3.2.4*** A point $x$ is a *limit point* of a set $A$ if every ε-neighborhood $V_{\epsilon}(x)$ of $x$ intersects the set $A$ at some point other than $x$.

***Theorem 3.2.5*** A point $x$ is a limit point of a set $A$ if and only if
$x = \lim a_n$ for some sequence $(a_n)$ contained in $A$ satisfying
$a_n \ne x$ for all $n \in \mathbb{N}$.

* Summary of the proof.
    * $\Rightarrow$  If $x$ is a limit point of a set $A$, pick $a_n \in V_{\frac{1}{n}}(x)$. Then $x = \lim a_n$.
    * $\Leftarrow$ If we can find such sequence, then given $\epsilon$, we can find $\left| a_n - x \right| < \epsilon$. Then $a_n \in V_{\epsilon}(x)$. So $x$ is a limit point.


***Definition 3.2.6*** A point $a ∈ A$ is an isolated point of $A$ if it is not a limit point of $A$.

***Definition 3.2.7*** A set $F ⊆ R$ is closed if it contains its limit points.

***Theorem 3.2.8*** A set $F ⊆ R$ is closed if and only if every Cauchy sequence contained in $F$ has a limit that is also an element of $F$.

* Proof: See exercise 3.2.5.

***Example 3.2.9***

(iii) The limit points of $\mathbb{Q}$ is $\mathbb{R}$.

* Proof: Consider $y \in \mathbb{R}$, based on Theorem 1.4.3, for any $V_{\epsilon}(y) = (y - \epsilon, y + \epsilon)$, there exists a rational number $r$, such that $r \in V_{\epsilon}(y)$. So $y$ is a limit point of $\mathbb{Q}$. $\square$

***Theorem 3.2.10 (Density of $\mathbb{Q}$ in $\mathbb{R}$)*** For every $y ∈ \mathbb{R}$, there exists a sequence of rational numbers that converges to $y$.

* Proof: Assume $y \in \mathbb{R}$, then based on previous example, $y$ is a limit point of $\mathbb{Q}$. Then according to Theorem 3.2.5, there exists some sequence in $\mathbb{Q}$ converges to $y$. $\square$

### Closure

***Definition 3.2.11*** Given a set $A ⊆ R$, let $L$ be the set of all limit points of $A$. The closure of $A$ is defined to be $\bar{A} = A ∪ L$.

***Theorem 3.2.12*** For any $A ⊆ R$, the closure $\bar{A}$ is a closed set and is the smallest closed set containing $A$.

* Summary of Proof: Assume $x$ is a limit point of $\bar{A}$, then given $V_{\epsilon}(x)$, we can find $a \in \bar{A}$ and $a \in V_{\epsilon}(x)$. If $a \not\in A$, then $a \in L$, then we can find $V_{\epsilon'}(a) \subseteq V_{\epsilon}(x)$ and $V_{\epsilon'}(a) \cap A \neq \emptyset$. Let $a' \in V_{\epsilon'}(a) \subseteq V_{\epsilon}(x)$, so $x$ is a limit point of $A$. Then $\bar{A}$ is a closed set.
    * Assume $A \subseteq C$ is a closed set, $c$ is a limited point of $A$. Then we can find a sequence $\left\{ a_n \right\}$ converges to $c$. Since $\left\{ a_n \right\}$ is also a sequence in $C$, based on Theorem 3.2.8, $c \in C$. So $L \subseteq C$, then $\bar{A} \subseteq C$. $\square$ 




