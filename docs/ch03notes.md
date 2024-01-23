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

## 3.3 Compact Sets

* Employing compact sets in a proof often has the effect of bringing a finite quality to the argument, thereby making it much more tractable.

***Definition 3.3.1 (Compactness).*** A set $K \subseteq R$ is compact if every sequence in $K$ has a subsequence that converges to a limit that is also in $K$.

***Example 3.3.2.*** The most basic example of a compact set is a closed interval.

* What are the properties of closed intervals that we used in the preceding argument?
    * The Bolzano–Weierstrass Theorem requires boundedness
    * and we used the fact that closed sets contain their limit points.

***Definition 3.3.3.*** A set $A ⊆ R$ is bounded if there exists $M > 0$ such that $|a|≤M$ for all $a∈A$.

***Theorem 3.3.4 (Characterization of Compactness in R).*** A set $K \subseteq R$ is compact if and only if it is closed and bounded.

* Proof: $\Rightarrow$

## 3.4 Perfect Sets and Connected Sets

* One of the underlying goals of topology is to strip away all of the extraneous
information that comes with our intuitive picture of the real numbers and isolate
just those properties that are responsible for the phenomenon we are studying.

***Definition 3.4.1.*** A set $P ⊆ \mathbb{R}$ is perfect if it is closed and contains no isolated points.

***Example 3.4.2 (Cantor Set).*** It is not too hard to see that the Cantor set is perfect. See exercise  3.4.3.

***Theorem 3.4.3.*** A nonempty perfect set is uncountable.

* Summary of proof: Assume $P$ is countable, and $P = \{x_1, x_2, \dots\}$. Let $I_1$ be
an interval such that $x_1$ in the interior of $I_1$. Since $x_1$ is not
isolated, we can find $y_2$ in the interior of $I_1$. Then we can construct $I_2$ such that $y_2$ is in the middle of $I_2$ and 
$I_2 \subset I_1$ and $x_1 \notin I_2$.

We can continue this process and they satisfy:

1. $I_{n+1} \subseteq I_n$
2. $x_n \notin I_{n+1}$
3. $x_{n-1} \neq y_n\in I_n \cap P \neq \emptyset$.

And let $K_n = I_n \cap P$. Then based on Nested Compact Set Property,
$\cap K_n$ is not empty. However, since $x_n \notin K_{n+1}$, $\cap K_n = \emptyset$. We got a contradiction.

### Connected Sets

***Definition 3.4.4.*** Two nonempty sets $A, B ⊆ R$ are separated if $\overline{A} ∩ B$ and $A ∩ \overline{B}$ are both empty. A set $E ⊆ R$ is disconnected if it can be written as $E = A ∪ B$, where $A$ and $B$ are nonempty separated sets.

A set that is not disconnected is called a connected set.

***Example 3.4.5.*** the set of rational numbers is disconnected. Just need
to consider $A = (-\infty, \sqrt{2})$ and $B = (\sqrt{2}, \infty)$.

***Theorem 3.4.6.*** A set $E ⊆ R$ is connected if and only if, for all nonempty disjoint sets $A$ and $B$ satisfying $E = A ∪ B$, there always exists a convergent sequence $(x_n) → x$ with $(x_n)$ contained in one of $A$ or $B$, and $x$ an element of the other.

* Proof:
* $\Rightarrow$ Assume $E ⊆ R$ is connected and nonempty disjoint sets $A$ and $B$ satisfying $E = A ∪ B$. Assume there is no such sequence in both $A$ and $B$. It means $A$ has no limit points of $B$ and $B$ has no limit points of $A$. So $A \cap \overline{B} = \emptyset$ and $B \cap \overline{A} = \emptyset$. Then $E$ is not connected.
* $\Leftarrow$ Assume for all nonempty disjoint sets $A$ and $B$ satisfying $E = A ∪ B$, there always exists a convergent sequence $(x_n) → x$ with $(x_n)$ contained in one of $A$ or $B$, and $x$ an element of the other. Then it means $A \cap \overline{B} \neq \emptyset$ or $B \cap \overline{A} \neq \emptyset$.

***Theorem 3.4.7.*** A set $E ⊆ R$ is connected if and only if whenever $a < c < b$ with $a, b ∈ E$, it follows that $c ∈ E$ as well.

* Proof:
    * $\Rightarrow$: Assume $E \subseteq R$ is connected. Given $a < c < b$ with $a, b ∈ E$,
and assume $c \notin E$. Consider $A = \{a \in E | a < c\}$, $B = \{b \in E | b > c\}$. For any $(x_n) \in A$, since $x_n < c$, then $(x_n) \rightarrow x \le c$. So $x \notin B$. Similarly, if $(x_n) \rightarrow x \in B$ ,then $x \notin A$. Then from Theorem 3.4.6, $E$ is not connected. We have a contradiction.
    * $\Leftarrow$: Conversely assume $a < c < b$ with $a, b ∈ E$, it follows that $c ∈ E$. Assume $E = A \cup B, a \in A, b \in B, a < b$. Let $A' = A \cap (-\infty, b), c = \sup A'$. So we have $a \le c \le b, c \in E$.
        * If $c \in B$, then $\overline{A} \cap B \ne \emptyset$.
        * If $c \in A$, then $c \neq b$, then $(c, b] \subseteq E$. So $c$ is a limit point of  $(c, b]$, thus a limit point of $B$. So $\overline{B} \cap A \ne \emptyset$.
    * Textbook method to prove $\Leftarrow$ (more elegant): assume $a < c < b$ with $a, b ∈ E$, it follows that $c ∈ E$. Assume $E = A \cup B, a_0 \in A, b_0 \in B, a_0 < b_0, I_0 = [a_0, b_0]$. Let $c = (a_0 + b_0)/2$:
        * if $c \in A$, then $a_1 = c, b_1 = b_0$.  
        * if $c \in B$, then $a_1 = a_0, b_1 = c, I_1 = [a_1, b_1]$.
    * Then we have $I_0 \supset I_1 \supset \cdots$. From Nested Interval Property, we have $\lim a_n = \lim b_n = x \in \cap I_n$.  

