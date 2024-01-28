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

## 3.5 Baire’s Theorem

***Definition 3.5.1.*** A set $A ⊆ R$ is called an $F_σ$ set if it can be written as the countable union of closed sets. A set $B ⊆ R$ is called a $G_δ$ set if it can be written as the countable intersection of open sets.

***Exercise 3.5.1.***  Argue that a set A is a $G_δ$ set if and only if its complement is an $F_σ$ set.

Proof. Use De Morgan’s Laws.

***Exercise 3.5.2.*** Replace each underscore with the word finite or countable, depending on which is more appropriate.

(a) The finite/countable union of $F_σ$ sets is an $F_σ$ set.

Both are correct. This is because countable union of countable sets is still countable union of sets.
See also [here](https://math.stackexchange.com/questions/2255466/proof-the-countable-union-of-f-sigma-sets-is-an-f-sigma-set).

(b) The finite/countable intersection of $F_σ$ sets is an $F_σ$ set.

Proof: First, countable intersection of $F_σ$ sets might not be an $F_σ$ set. Consider $U_r = \left\{ x | x \neq r \right\}$ where $r$ is an rational number. Then $U_r$ is $F_σ$ set. But their intersection is $I$, which is all irrational numbers. As shown in Exercise 3.5.6, $I$ cannot be $F_σ$ set.

Then finite intersection of $F_σ$ sets might not be an $F_σ$ set. Assume $U = \cup U_i$ and $V = \cup V_j$. Then $U \cap V = \cup U_i \cap V_j$. Since $U_i \cap V_j$ is closed. And there are countable of them, so $U \cap V$ is $F_σ$.

(c) The finite/countable union of $G_δ$ sets is a $G_δ$ set.

See (b) and De Morgan's law.

(d) The finite/countable intersection of $G_δ$ sets is a $G_δ$ set.

See (a) and De Morgan's law.

Recall that a set $G ⊆ \mathbb{R}$ is dense in $\mathbb{R}$ if, given any two real numbers $a<b$,
it is possible to find a point $x ∈ G$ with $a<x<b$.

***Theorem 3.5.2.*** If ${G_1, G_2, G_3,...}$ is a countable collection of dense, open sets, then the intersection $\cap_{n=1}^\infty G_n$  is not empty.

***Exercise 3.5.4.*** Prove Theorem 3.5.2.

Proof: Since $G_1$ is open, we can find $[a_1, b_1] \subseteq G_1$. Since $G_2$ is dense, we can find $[a_2, b_2] \subseteq [a_1, b_1]$ and $[a_2, b_2] \subseteq G_2$. Then we construct a nested sequence
of closed intervals $I_1 ⊇ I_2 ⊇ I_3 ⊇···$ satisfying $I_n ⊆ G_n$.

***Exercise 3.5.5.*** Show that it is impossible to write

$$
R = \cup_{n=1}^{\infty} F_n
$$

where for each $n ∈ N$, $F_n$ is a closed set containing no nonempty open intervals.

Proof: Consider $G_n = (F_n)^c$, so $G_n$ is open, and it's also dense.
Then from 3.5.4, the intersection of $G_n$ is not empty. So the union of $F_n$
cannot be the whole $R$.

***Exercise 3.5.6.*** Show how the previous exercise implies that the set $I$ of irrationals cannot be an $F_σ$ set, and $Q$ cannot be a $G_δ$ set.

Proof: Assume $I$ is an $F_{\sigma}$ set.

$$
I = \cup_{n=1}^{\infty} F_n
$$

$F_n$ is a closed set containing no nonempty open intervals. And $Q$ can be
written as

$$
Q = \cup_{n=1}^{\infty} \{q_n | q_n \in Q\}
$$

$Q_n$ is a closed set containing no nonempty open intervals.

And $R = I \cup Q$. We have a contradiction.

***Exercise 3.5.7.*** Using Exercise 3.5.6 and versions of the statements in
Exercise 3.5.2, construct a set that is neither in $F_σ$ nor in $G_δ$.

Solution: Let $A = \left\{ x | x \in [-1, 0] \cap \mathbf{I}\right\}$ and $B = \left\{ x | x \in [0, 1] \cap \mathbf{Q}\right\}$. Let $C = A \cup B$.

Assume $C$ is $F_σ$. We have $C \cap [-1, 0] = (A \cup B) \cap [-1, 0] = (A \cap [-1, 0]) \cup (B \cap [-1, 0]) = A \cup \emptyset = A$. So $A$ is $F_σ$. But then $\mathbf{I}$ will be $F_σ$. We have a contradiction.

Assume $C$ is $G_δ$. $C \cap [0, 1] = (A \cup B) \cap [0, 1] = (A \cap [0, 1]) \cup (B \cap [0, 1]) = \emptyset \cup B = B$. We want to show $B$ is not $G_δ$ set. Assume otherwise. Consider $B^c = (-\infty, 0) \cup ([0, 1] \cap \mathbf{I}) \cup (1, \infty)$, which has to be $F_σ$. Then $([0, 1] \cap \mathbf{I})$ has to be $F_σ$, which is impossible.

So $C$ is neither in $F_σ$ nor in $G_δ$.

***Definition 3.5.3.*** A set $E$ is nowhere-dense if $\overline{E}$ contains no nonempty open intervals.

***Definition*** $G$ is dense in $\mathbb{R}$  if and only if $\overline{G} = \mathbb{R}$.

***Exercise 3.5.8.*** Show that a set $E$ is nowhere-dense in $\mathbb{R}$ if and only if the complement of $\overline{E}$ is dense in R.

Proof. 

* $\Leftarrow$ Assume the complement of $\overline{E}$ is dense in $\mathbb{R}$, also assume
$(a, b) \subset \overline{E}$. Further assume $a < c < b$. Since $(a, b) \cap \overline{E}^c = \emptyset$. $c$ cannot be a limit point of $\overline{E}^c$, so
$\overline{\overline{E}^c} \ne \mathbb{R}$, so it's not dense, we have a contradiction.

* $\Rightarrow$ Conversely, assume $E$ is nowhere-dense in $\mathbb{R}$ and $a \in \overline{E}$, because $\overline{E}$ does not contain
open interval, in every $V_{\epsilon}(a)$, we can find $b \in \overline{E}^c$, it means
$a$ is a limit point of $\overline{E}^c$. So $\overline{\overline{E}^c} = \mathbb{R}$. So the complement of $\overline{E}$ is dense in $\mathbb{R}$.

***Exercise 3.5.9.*** Decide whether the following sets are dense in $\mathbb{R}$, nowhere-dense in $\mathbb{R}$, or somewhere in between.

(a) $A=Q∩[0,5]$.

Some where is between. Apparently, $\overline{A} = [0,5]$ which contains open interval.
So it's not nowhere-dense. But it's not $\mathbb{R}$, so it's not dense. But it's dense in $[0,5]$. 

(b) $B =\{1/n:n∈N\}$.

nowhere-dense.

(c) the set of irrationals.

dense, since it's closure is $\mathbb{R}$

(d) the Cantor set.

nowhere-dense. Since itself is a closed set. And it does not contain open interval.
See exercise 3.4.8.

***Theorem 3.5.4 (Baire’s Theorem).*** The set of real numbers R cannot be written as the countable union of nowhere-dense sets.

Proof. For contradiction, assume that $E_1,E_2,E_3,...$ are each nowhere-dense and satisfy $\mathbb{R} = \cup^{∞}_{n=1} E_n$.

***Exercise 3.5.10.*** Finish the proof by finding a contradiction to the results in this section.

Proof. We consider $\cup^{∞}_{n=1} \overline{E_n}$, then diretly apply 
Exercise 3.5.5. We can prove it. Since the closure of them cannot cover $R$, let alone
themselves.

