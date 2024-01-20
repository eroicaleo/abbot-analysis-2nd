# Chapter 03 Basic Topology of $\mathbb{R}$ 

## 3.2 Open and Closed Sets

### 3.2.1

(a) Where in the proof of Theorem 3.2.3 part (ii) does the assumption that the collection of open sets be finite get used?

* Solution: Yes. To obtain $\epsilon = \min \left\{ \epsilon_1, \cdots, \epsilon_n \right\} > 0$. If there are infinite number of open sets, it's not guaranteed $\epsilon > 0$. So we might not be able to find $V_{\epsilon}(a)$. $\square$


(b) Give an example of a countable collection of open sets $\left\{ O_1,O_2,O_3, ... \right\}$ whose intersection $\cap_{n=1}^\infty O_n$ is closed, not empty and not all of $\mathbb{R}$.

* Solution: Consider $O_n = ( -\frac{1}{n}, \frac{1}{n} )$, then $\bigcap_{n=1}^{\infty}O_n = \left\{ 0 \right\}$ which is a non-empty closed set. $\square$

### 3.3.2

Let

$$
A = \left\{ (-1)^n + \frac{2}{n} : n = 1, 2, 3 \right\} \text{and } B = \left\{ x \in \mathbb{Q}: 0 < x < 1 \right\} 
$$

Answer the following questions for each set:
(a) What are the limit points?
(b) Is the set open? Closed?
(c) Does the set contain any isolated points?
(d) Find the closure of the set.

* Solution:
    * The limit points of $A$ are $\left\{ -1, 1 \right\}$. For $B$, it's $[0, 1]$.
    * Both $A$ and $B$ are neither open nor closed. For $A$, $-1 \not\in A$. For $B$, $1 \not\in B$.
    * All points in $A$ are isolated except $1$. $B$ does not contain any isolated points.
    * $\overline{A} = A \cup \left\{ -1\right\}$ and $\overline{B} = [0, 1]$.$\square$

### 3.2.3

Decide whether the following sets are open, closed, or neither. If a set is not open, find a point in the set for which there is no ε-neighborhood contained in the set. If a set is not closed, find a limit point that is not contained in the set.

(a) Q.

Neither. Every point. $\sqrt{2}$.
Also see [here](https://math.stackexchange.com/questions/116721/are-the-rationals-a-closed-or-open-set-in-mathbbr).

(b) $\mathbb{N}$

Closed. Every point.

(c) $\{x \in R:x \ne 0\}$\

Open. $0$.

(d) $\{1+1/4+1/9+\cdots+1/n^2: n \in N\}$.

Neither. Everypoint. It's limit.

(e) $\{1 + 1/2 + 1/3 + \cdots + 1/n : n \in N\}$.

Closed. Everypoint.

### 3.2.4

Let $A$ be nonempty and bounded above so that $s = \sup A$ exists.

(a) Show that $s ∈ \overline{A}$.

* Proof: According to Lemma 1.3.8., $s$ is a limited point of $A$. 
So $s ∈ \overline{A}$.

(b) Can an open set contain its supremum?

* Proof: No. If $V_{\epsilon}(s) = (s - \epsilon, s + \epsilon) \subset A$.
Then $s < s + \epsilon/2 \in A$. Then $s$ is not the supremum. We got
a contradiction.

See also [here](https://math.stackexchange.com/questions/1727959/can-an-open-set-contain-its-supremum).


### 3.2.5

A set $F \subset \mathbb{R}$ is closed if and only if every Cauchy sequence contained in $F$ has a limit that is also an element of $F$.

* Proof:
    * $\Rightarrow$ Assume $F \subset \mathbb{R}$ is closed, and $\left( a_n \right)$ is a Cauchy sequence contained in $F$. Then according to Theorem 2.6.4 (Cauchy Criterion), $\left( a_n \right)$ converges. Let $x = \lim a_n$.
        * If $\exists n, \text{such that } a_n = x$, then $x \in F$.
        * If $x \neq a_n, \forall n$, then according to Theorem 3.2.5, $x$ is a limit point of $F$, so $x \in F$.
    * $\Leftarrow$ Assume every Cauchy sequence contained in $F$ has a limit that is also an element of $F$ and $x$ is a limit point of $F$. According Theorem 3.2.5, we can find some sequence $(a_n)$ contained in $F$ satisfying $a_n \ne x$ for all $n \in \mathbb{N}$ and $x = \lim a_n$. Again according to Theorem 2.6.4, $(a_n)$ is a Cauchy sequence, then $x \in F$. $\square$

### 3.2.6

Decide whether the following statements are true or false. Provide counterexamples for those that are false, and supply proofs for those that are true.

(a) An open set that contains every rational number must necessarily be all of R.

No. Consider $\mathbb{R} - \{\pi\}$.

(b) The Nested Interval Property remains true if the term “closed interval” is replaced by “closed set.”

False. Let $I_n = [n, \infty)$, which is closed. Then $\cap I_n = \emptyset$.

See discussion [here](https://math.stackexchange.com/questions/489242/nested-sequence-of-closed-sets).

But if the "closed set" is bounded. Then assume $a_n = \inf I_n, b_n = \sup I_n$. Then we have $a_n, b_n \in I_n$. Now let $a = \sup \{a_n\}$, because
$a$ is a limit point of $I_n$. so $a \in I_n, \forall n$.

(c) Every nonempty open set contains a rational number.

True. $\mathbb{Q}$ is dense.

(d) Every bounded infinite closed set contains a rational number.

False. Consider $A = \{\pi + (1/n) : n\in \mathbb{N} \} \cup \pi$.

Also see [here](https://math.stackexchange.com/questions/1440516/t-f-every-bounded-infinite-closed-set-contains-a-rational-number)

(e) The Cantor set is closed.

True. By definition in section 3.1

$$
C = \cap_{n=0}^\infty C_n
$$
Each $C_n$ is the union of finite closed set so it is closed from Theorem 3.2.14. Then $C$ is the intersection of them, so it is also closed.

### 3.2.7

Given $A ⊆ R$, let $L$ be the set of all limit points of $A$.

(a) Show that the set $L$ is closed.

* Proof: Assume $x$ is limit point of L, then for every $V_{\epsilon}(x)$,
we can find $x' \in L$ and $x' \in V_{\epsilon}(x)$. Then $x'$ is a limit
point of $A$, so we can find $a \in A$, such that $a \in V_{\epsilon}(x)$.
The $x$ itself is a limited point of $A$. So $x \in L$. So $L$ is closed.

(b) Argue that if $x$ is a limit point of $A \cup L$, then $x$ is a limit point of $A$. Use this observation to furnish a proof for Theorem 3.2.12.

* Proof. If $l \in L$ and $l \in V_{\epsilon}(x)$, then we can find
$a \in V_{\epsilon'}(l) \subset V_{\epsilon}(x)$. So $l$ is a limit point
of $A$. Then $l \in L \subseteq A \cup L$. Then $A \cup L$ is closed.


### 3.2.8

Assume $A$ is an open set and $B$ is a closed set. Determine if
the following sets are definitely open, definitely closed, both, or neither.

(a) $\overline{A∪B}$

Definitely closed.

(b) $A - B= \{x∈A:x \notin B\}$

Definitely open. Assume $x \in A - B$, then $x \notin B$, so $x$ is not a limit point of $B$.
Then we can find $V_{\epsilon_1}(x) \cap B = \emptyset$. Since $A$ is open,
we can find $V_{\epsilon_2}(x) \subset A$. So we can find $\epsilon = \min(\epsilon_1, \epsilon_2)$ such that $V_{\epsilon}(x) \in A - B$.

(c) $(A^c ∪ B)^c$

$A^c$ is closed, then $(A^c ∪ B)$ is closed. Then $(A^c ∪ B)^c$ is open.

(d) $(A∩B)∪(A^c ∩B)$

It's equal to $B$, so closed.

(e) $\overline{A}^c ∩ \overline{A^c}$

We prove $\overline{A^c} \supset \overline{A}^c$. Assume $a \in \overline{A}^c$, then $a \notin \overline{A}$ so $a \notin A$, then
$a \in A^c \subset \overline{A^c}$. So $\overline{A}^c \subset \overline{A^c}$.

Then $\overline{A}^c ∩ \overline{A^c} = \overline{A^c}$. Then it is
definitely closed.


### 3.2.10

Only one of the following three descriptions can be realized. Provide an example that illustrates the viable description, and explain why the other two cannot exist.

(i) A countable set contained in $[0, 1]$ with no limit points.

* This is not possible because of Bolzano-Weierstrass Theorem.

(ii) A countable set contained in [0, 1] with no isolated points.

* This is possible for $\mathbb{Q} \cap [0, 1]$.

(iii) A set with an uncountable number of isolated points.

* Proof:

This is impossible. Assume $A$  is such set,
$x$ is an isolated points, such that $V_{\epsilon}(x) \cap A =\{x\}$.
We will show we can find 
$V_{\epsilon_1}(x)$ does not intersect with any $V_{\epsilon_y}(y)$.

Assume $V_{\epsilon}(x) \cap V_{\epsilon_y}(y) \ne \emptyset$ and
$y > x$. First we will show $V_{\epsilon}(x) \cap V_{\epsilon_z}(z) = \emptyset, \forall z > x$.
If this is not the case, and $y > z$, then $z \in V_{\epsilon_y}(y)$ or
$z \in V_{\epsilon}(x)$. This is not possible.
If $z > y$, then $y \in V_{\epsilon_z}(z)$. This is also not possible.

The same argument holds for $y < x$. So we can shrink $V_{\epsilon}(x)$
small enough. And this can be performed for any $x \in A$.

That means we have an uncountable set of open set and any two of them
does not intersect with each other. But that means we can have
uncountable many rational numbers. We have a contradiction. $\square$

Also search this question in stack overflow, like
[here](https://math.stackexchange.com/questions/1951645/does-there-exist-an-uncountable-number-of-isolated-points)

### 3.2.11

(a) Prove that $\overline{A ∪ B} = \overline{A} ∪ \overline{B}$.

* Proof:
    * We first prove $\overline{A ∪ B} \subset \overline{A} ∪ \overline{B}$. $A \subset \overline{A} ∪ \overline{B}$ and
$B \subset \overline{A} ∪ \overline{B}$, so
$A ∪ B \subset \overline{A} ∪ \overline{B}$. Because $\overline{A} ∪ \overline{B}$ is also a closed set, it must contain the closure of $A ∪ B$ according to Theorem 3.2.12. So
$\overline{A ∪ B} \subset \overline{A} ∪ \overline{B}$.

    * On the other hand, $A \subset \overline{A ∪ B}$ so
$\overline{A} \subset \overline{A ∪ B}$.
For the same reason, $\overline{B} \subset \overline{A ∪ B}$.
So $\overline{A} ∪ \overline{B} \subset \overline{A ∪ B}$.
    * So we have $\overline{A ∪ B} = \overline{A} ∪ \overline{B}$. $\square$

(b) Does this result about closures extend to infinite unions of sets?

* Proof: No. Consider $A_1 = [1/2, 1], ..., A_n = [1/(n+1), 1/n]$.
Then $\cup \overline{A_n} = (0, 1]$. However $\cup A_n = (0, 1]$, so $\overline{\cup A_n} = [0, 1]$.

### 3.2.12

Let $A$ be an uncountable set and let $B$ be the set of real numbers that divides $A$ into two uncountable sets; that is, $s ∈ B$ if both $\{x : x∈A \text{ and } x<s\}$ and $\{x:x∈A \text{ and } x>s\}$ are uncountable. Show $B$ is nonempty and open.

* Proof:
    * Define $C_s = (-\infty, s]$ and $C = \left\{ s : A \cap C_s \text{ is countable} \right\}$. We can see $C \ne \mathbb{R}$. Otherwise, $A = \cup_{i = 1}^{\infty} (A \cap C_i)$ is countable. This means $C$ is upper bounded. Let $c = \sup C$, we will show $c \in C$. $A \cap C_c = \cup_{i = 1}^{\infty} (A \cap C_{c-\frac{1}{i}}) \cup (A \cap \left\{ c \right\} )$ is countable. So $c \in C$. Furthurmore $C = (-\infty, c]$.
    * Similarly, define $D_s = [s, \infty)$ and $D = \left\{ s : A \cap D_s \text{ is countable} \right\}$. We can show $D = [d, \infty)$ for some $d$.
    * Furthur more $C \cap D = \emptyset$. Otherwise $A$ is countable.
    * So finally, we have $B = (c, d)$ is nonempty and open.

### 3.2.13

Prove that the only sets that are both open and closed are $\mathbb{R}$ and the empty set $\emptyset$.

* Proof:

Consider $a \in A \ne \emptyset$ and $b \in A^c \ne \emptyset$.
WLOG, assume $a < b$. Let $A' = A \cap [a, b]$. Since the intersection of 2 closed sets are closed, $A'$ is closed. Let $s = \sup A'$. since $A'$ is closed, $s \in A'$ (Exercise 3.2.4). $b$ is an upper bound of $A'$, so $s \leq b$.

* If $s = b$, then $s \in A^c$. We have a contradiction.
* If $s < b$, since $A$ is open, there exists $V_{\epsilon}(s) \subset A \cap [a, b] = A'$, then $s$ is not a superem of $A'$. We have another contradiction. $\square$

Also see stackexchange [here](https://math.stackexchange.com/questions/751886/if-a-nonempty-set-of-real-numbers-is-open-and-closed-is-it-mathbbr-why-wh).

### 3.2.14

A dual notion to the closure of a set is the interior of a set. The interior of $E$ is denoted $E^o$ and is defined as

$$
E^o = \{x \in E: \text{there exists } V_{\epsilon}(x)⊆E \}.
$$

a. Show that $E$ is closed if and only if $E=\overline{E}$. Show that $E$ is open if and only if $E^o = E$.

* Proof: $E$ is closed so it contains all its limited points, i.e. $L \subset E$, so $E \supset E \cup L = \overline{E}$. On the other hand, $E \subset \overline{E}$. So $E = \overline{E}$.
* $E$ is open, so if $x \in E$ then there exists $V_{\epsilon}(x) \subseteq E$. so $x \in E^o$, and $E \subseteq E^o$. On the other hand, $E \supseteq E^o$. So $E = E^o$. $\square$

b. Show that $\overline{E}^c = (E^c)^o$, and similarly that
$(E^o)^c = \overline{E^c}$.

* Proof: First statement. Assume $x \in \overline{E}^c$, then $x \notin \overline{E}$. Then $x \notin E$, so $x \in E^c$. Furthermore $x$ is not a
limit point of $E$, so there exists $V_{\epsilon}(x)⊆ E^c$. Then
$x \in (E^c)^o$.

* On the other hand if $x \in (E^c)^o$, then there exists $V_{\epsilon}(x)⊆ E^c$. So $x \notin \overline{E}$, so $x \in \overline{E}^c$.

* Second statement. Assume $x \in (E^o)^c$, then $x \notin E^o$. Then $x$
is a limit point of $E^c$, so $x \in \overline{E^c}$.

* On the other hand, assume $x \in \overline{E^c}$. If $x \in E^c$, then
$x \in (E^o)^c$. If $x \notin E^c$, $x$ is a limit point of $E^c$. So
there doesn't exist $V_{\epsilon}(x)⊆ E$, then $x \notin E^o$.
So $x \in (E^o)^c$. $\square$

### 3.2.15

A set $A$ is called an $F_σ$ set if it can be written as the countable union of closed sets. A set $B$ is called a $G_δ$ set if it can be written as the countable intersection of open sets.

(a) Show that a closed interval $[a, b]$ is a $G_δ$ set.

* Proof: Let $A_n = (a - 1/n, b + 1/n)$. Then $[a,b] = \cap_{i = 1}^{\infty} A_n$.

(b) Show that the half-open interval $(a, b]$ is both a $G_δ$ and an $F_σ$ set.

* Proof: Let $A_n = [a+\frac{1}{n}, b]$, then $(a, b]$ is $F_σ$.
Let $B_n = (a, b+\frac{1}{n})$, then $(a, b]$ is $G_δ$.

(c) Show that $Q$ is an $F_σ$ set, and the set of irrationals $I$ forms a $G_δ$ set.

* Proof: Let $A_q = \{q\}$. Then it's a closed set. Since $Q$ is countable,
the union of them is $Q$.
* Let $B_q = R - \{q\}$, then $B_q$ is open. The intersection of them is $I$. $\square$

## 3.3 Compact Sets

### 3.3.2

Decide which of the following sets are compact. For those that are not compact, show how Definition 3.3.1 breaks down. In other words, give an example of a sequence contained in the given set that does not possess a subsequence converging to a limit in the set.

(a) N.

Not compact. Itself.

(b) $Q \cap [0,1]$

Not compact. A sequence converges to $\sqrt{2}/2$.

(c) The Cantor set.

Compact. Close and bounded.

(d) $\{1+1/2^2 +1/3^2 +···+1/n^2 :n∈N\}$.

Not closed. Itself.

(e) $\{1,1/2,2/3,3/4,4/5,...\}.$

Compact. Closed and bounded.
It has 1 limit point which is 1, so it's closed.

### 3.3.6.

This exercise is meant to illustrate the point made in the opening paragraph to Section 3.3. Verify that the following three statements are true if every blank is filled in with the word “finite.” Which are true if every blank is filled in with the word “compact”? Which are true if every blank is filled in with the word “closed”?

(a) 

* Every finite set has a maximum. True.
* Every compact set has a maximum. True. Bounded and closed. Exercise 3.2.4.
* Every closed set has a maximum. False. $[0, \infty)$.

(b)

* If $A$ and $B$ are finite, then $A+B={a+b:a∈A,b∈B}$ is also finite. True.
* If $A$ and $B$ are compact, then $A+B={a+b:a∈A,b∈B}$ is also compact. True.

proof: Assume $c$ is a limit point of $A+B$, we can find a sequence $\{a_n + b_n\} \rightarrow c$. For $\{a_n\}$, since $A$ is compact, we can find a subsequence
$\{a_{n_k}\} \rightarrow a \in A$. Again $\{a_{n_k} + b_{n_k}\} \rightarrow c$. We can find a subsequence $b_{n_{k_l}} \rightarrow b$. So $a_{n_{k_l}} + b_{n_{k_l}} \rightarrow c$ and $a_{n_{k_l}} + b_{n_{k_l}} \rightarrow a + b$.
So $c = a + b$. So $c \in A+B$.

See also [here](https://math.stackexchange.com/questions/2432845/prove-that-the-sum-of-two-compact-sets-in-mathbb-rn-is-compact)

* If $A$ and $B$ are closed, then $A+B={a+b:a∈A,b∈B}$ is also closed. False.

Consdier

$$
A = \{n + \frac{1}{10^n}: n = 1, 2, \cdots\} \\
B = \{-n : n = 1, 2, \cdots\}
$$
Both sets are closed. And $0$ is a limit point of $A+B$. And $0 \notin A+B$.

See also [here](https://math.stackexchange.com/questions/124130/sum-of-two-closed-sets-in-mathbb-r-is-closed).

(c)

* If $\{A_n: n \in \mathbb{N}\}$ is a collection of ***finite*** sets with the property that every finite subcollection has a nonempty intersection,
the $\cap A_n \ne \emptyset$.

Proof: This is true. Assume otherwise. Consider

$$
B_n = \cap_{i=1}^n A_n
$$

Consider $a_1 \in A_1 = B_1$, since $a_1 \notin \cap A_n = \cap B_n$, we can find $N_1$, such
that $a \notin B_n, \forall n > N_1$.
We can check for all elements in $a_i \in A_1$ and find $N_{i}$ for each $a_i$. Then we choose $N = \max \left\{ N_1, N_2, \dots \right\}$. Then for any $n > N, a_i \not\in B_n$. $B_n$ is empty.
This contradicts to every finite subcollection has a nonempty intersection. So this statement is true. $\square$ 

* If $\{A_n: n \in \mathbb{N}\}$ is a collection of ***compact*** sets with the property that every finite subcollection has a nonempty intersection,
the $\cap A_n \ne \emptyset$.

Proof: This is true. Again consider

$$
B_n = \cap_{i=1}^n A_n
$$

Then we have

$$
B_1 \supseteq B_2 \supseteq \dots
$$

They are all compact. So from Theorem 3.3.5 (Nested Compact Set Property),
$A$ is not empty.

* If $\{A_n: n \in \mathbb{N}\}$ is a collection of ***closed*** sets with the property that every finite subcollection has a nonempty intersection,
then $\cap A_n \ne \emptyset$.

Proof: False. Consider $A_n = [n, \infty)$.

### 3.3.7

As some more evidence of the surprising nature of the Cantor set, follow these steps to show that the sum $C +C = \{x+y : x,y ∈ C\}$ is equal to the closed interval $[0, 2]$. (Keep in mind that C has zero length and contains no intervals.)

Because $C ⊆ [0,1], C + C ⊆ [0,2]$, so we only need to prove the reverse inclusion $[0,2] ⊆ \{x + y : x,y ∈ C\}$. Thus, given $s ∈ [0,2]$, we must find two elements $x,y∈C$ satisfying $x+y=s$.

(a) Show that there exist $x_1 , y_1 ∈ C1$ for which $x_1 + y_1 = s$. Show in general that, for an arbitrary $n ∈ N$, we can always find $x_n,y_n ∈ C_n$ for which $x_n + y_n = s$.

* Proof: Let's start with $C_0 = [0, 1]$. Given any $s$ in $[0,2]$, choose any $x_0, y_0$ such that $s = x_0 + y_0$. So how do we find $x_1, y_1 \in C_1$ such that $s = x_1 + y_1$? We distinguish the following cases:
* If both $x_0, y_0$ are in $[0, 1/3]$ or $[2/3, 1]$ then let $x_1 = x_0 \in C_1$ and $y_1 = y_0 \in C_1$.
* If none of $x_0, y_0$ are in $[0, 1/3]$ or $[2/3, 1]$, then it means $x_0, y_0 \in (1/3, 2/3)$. Then lets $x_1 = x_0 - 1/3 \in [0, 1/3] \subset C_1$ and $y_1 = y_0 + 1/3 \in [2/3, 1] \subset C_1$.
* If $x_0 \in [0, 1/3]$ and $y_0 \in (1/3, 2/3)$. Then let $c_l = x_0 - 0, c_r = 1/3 - x_0$ and $d_l = y_0 - 1/3, d_r = 2/3 - y_0$.
    * if $c_l \geq d_r$, then let $x_1 = x_0 - d_r \in [0, 1/3]$, $y_1 = y_0 + d_r = 2/3 \in [2/3, 1]$, then $x_1, y_1 \in C_1$.
    * if $c_l < d_r$, then $c_r >= d_l$. Then let $x_1 = x_0 + d_l \in [0, 1/3]$ and $y_1 = y_0 - d_r = 1/3 \in [0, 1/3]$. So $x_1, y_1 \in C_1$.
* Similar argument can be applied when $x_0 \in [2/3, 1]$ and $y_0 \in (1/3, 2/3)$.
* In conclusion, we proved we can find there exist $x_1 , y_1 ∈ C1$ for which $x_1 + y_1 = s$. Use induction and the similar argument, we can show for an arbitrary $n ∈ N$, we can always find $x_n,y_n ∈ C_n$ for which $x_n + y_n = s$. $\square$ 

(b) Keeping in mind that the sequences $(x_n)$ and $(y_n)$ do not necessarily converge, show how they can nevertheless be used to produce the desired $x$ and $y$ in $C$ satisfying $x + y = s$.

* Proof: Assume $x_n \in C_n$ and $x_n \in I_n$. $|I_n| = 1/3^n$. Using the method in (a) to find $x_{n+1}$, we know $x_{n+1} \in I_n$, and it's either in the left $1/3$ or in the right $1/3$ part of $I_n$, call it $I_{n+1}$. Then
we produce $I_1 \supset I_2 \supset \dots$, such that $x_n \in I_n$. According to NIP, there exists
$x$ in all of them, that's $(x_n)$ converge to.
* Next, we prove $x \in C$. Because $x_1, x_2, \dots \in I_1$ which is closed, so $x \in I_1$. For the same reason, $x \in I_n \subset C_n, \forall n$. So $x \in C$. Simiarly, we can find the $y$ we need.
* Finally, we also have $x + y = \lim x_n + \lim y_n = \lim (x_n + y_n) = s$. $\square$

See also the [stackoverflow discussion](https://math.stackexchange.com/questions/309080/cantor-set-cantor-set-0-2).


### 3.3.8

Let $K$ and $L$ be nonempty compact sets, and define

$$
d = \inf \{ |x − y| : x ∈ K \text{ and } y ∈ L \}.
$$

This turns out to be a reasonable definition for the distance between $K$ and $L$.

(a) If $K$ and $L$ are disjoint,show $d>0$ and that $d=|x_0−y_0|$ for some $x_0 ∈K$ and $y_0 ∈ L$.

Proof: Consider sequence $x_n - y_n \rightarrow d$, since $K$ and $L$ are compact, we can find subsequence
$\{x_{n_k}\} \rightarrow x$, from there we can find another subsequence
$\{y_{n_{k_{l}} }\} \rightarrow y$, then $x - y = d$. Since $x \in X$ and
$y \in Y$, then $x - y \ne 0$.

(b) Show that it’s possible to have $d = 0$ if we assume only that the disjoint sets $K$ and $L$ are closed.

Consider

$$
K = \{1-\frac{1}{10}, 2-\frac{1}{100},\dots\} \\
L = \{1, 2, \dots\}
$$
Then the distance can be 0.

See also two stackexchange discussions:

* [Q&A 1](https://math.stackexchange.com/questions/48714/a-and-b-disjoint-a-compact-and-b-closed-implies-there-is-positive-distance-bet)
* [Q&A 2](https://math.stackexchange.com/questions/391396/for-two-disjoint-compact-subsets-a-and-b-of-a-metric-space-x-d-show-that)

### 3.3.9

Follow these steps to prove the final implication in Theorem 3.3.8.

Assume $K$ satisfies (i) and (ii), and let $\left\{ O_{\lambda}(x) : \lambda \in \Lambda \right\}$ be an open cover for
$K$. For contradiction, let’s assume that no finite subcover exists. Let $I_0$ be a closed interval containing $K$.

(a) Show that there exists a nested sequence of closed intervals
$I_0 \supseteq I_1 \supseteq I_2 \cdots$ with the property that, for each $n$, $I_n \cap K$ cannot be finitely covered and $\lim |I_0| = 0$.

Proof: Because $I_0 \cap K = K$, so $I_0 \cap K$ cannot be finitely covered. Let $I_0 = [a_0, b_0]$. Now consider $[a_0, (a_0+b_0)/2]$ and $[(a_0+b_0)/2, b_0]$. One of them intersecting with $K$ must not be finitely covered. So we found $I_1$. We can continue this process to find $I_n$. They satisfy the property. $\square$ 

(b) Argue that there exists an $x ∈ K$ such that $x ∈ I_n$ for all $n$.

Proof: $I_n \cap K$ is non empty since it cannot be finitely covered. It is also closed set since both $I_0$ and $K$ are closed. Then based on Theorem 3.3.5 (Nested Compact Set Property), the intersection is non-empty. $\square$ 

(c) Because $x ∈ K$, there must exist an open set $O_{\lambda_0}$ from the original collection that contains $x$ as an element. Explain how this leads to the desired contradiction.

Proof: Since $O_{\lambda_0}$ covers $x$, we can find
$V_{\epsilon}(x) \subset O_{\lambda_0}$. Then as long as $|I_n| < \epsilon/2$, $I_n$ is covered by  $V_{\epsilon}(x) \subset O_{\lambda_0}$. However, $I_n$ cannot be finitely covered. We have a contradiction. $\square$

### 3.3.10

Here is an alternate proof to the one given in Exercise 3.3.9 for the final implication in the Heine–Borel Theorem.

Consider the special case where $K$ is a closed interval. Let $\{O_λ : λ ∈ Λ\}$ be an open cover for $[a,b]$ and define $S$ to be the set of all $x ∈ [a,b]$ such that $[a,x]$ has a finite subcover from $\{O_λ : λ ∈ Λ\}$.

(a) Argue that $S$ is nonempty and bounded, and thus $s = \sup S$ exists.

Proof. Consider $a$ is cover by $O_a$, then we can find $V_{\epsilon}(a) \subset O_a$, then $[a, a+\epsilon/2] \subset V_{\epsilon}(a)$. So $S$ is
nonempty.

Furthermore, we will prove $s \in S$. Assume $O_s$ covers $s$. Then we can find $V_{\epsilon}(s) \subset O_s$, the $[s, s-\epsilon/2] \subset V_{\epsilon}(s)$. And $[a, s-\epsilon/2]$ has a finite subcover.
So $[a, s]$ has a finite subcover. $\square$

(b) Now show $s = b$, which implies $[a, b]$ has a finite subcover.

Proof. Assume $s = c < b$. Then $c$ is covered by $O_c$. Since $O_c$ is
open, then we can find $c < c' \in O_c$, then $[a, c']$ has a finite subcover. We have a contradiction. $\square$

(c) Finally, prove the theorem for an arbitrary closed and bounded set $K$.

Proof. Since $K$ is bounded, then we can assume $K \subseteq [a,b]$.
Assume $O_\lambda$ is an open cover of $K$. And assume $c \notin K, c \in [a,b]$. Since $K$ is closed, we know $c$ is not a limit point of $K$.
Then we can find $V_{\epsilon}(c) \cap K = \emptyset$.
This way, we can construct an open cover of $[a, b]$, i.e 
$O_\lambda \cup V_{\epsilon}(c)$.
Then we can find a finite cover. From that finite cover, we can find
a sub finite cover which is in $O_\lambda$. $\square$ 

### 3.3.11

Consider each of the sets listed in Exercise 3.3.2. For each
one that is not compact, find an open cover for which there is no finite subcover.

(a) N.

$(n-1/2, n+1/2)$

(b) $Q \cap [0,1]$

$(q-\epsilon/2, q+\epsilon/2)$ where $\epsilon$ is distance
between $q$ and $\sqrt{2}/2$.

(d) $\{1+1/2^2 +1/3^2 +···+1/n^2 :n∈N\}$.

Let $a_n = 1+1/2^2 +1/3^2 +···+1/n^2$ and let $O_n = (a-1/2(n+1)^2, a+ 1/2(n+1)^2)$

### 3.3.12

Using the concept of open covers (and explicitly avoiding the Bolzano–Weierstrass Theorem), prove that every bounded infinite set has a limit point.

* Proof: We use contradiction. Assume $K$ is a bounded infinite set, and $K \subset [a, b]$. Assume $K$ has no limit point.
Since none of the point in $[a,b]$ is a limit point of $K$. Then for
any $x \in [a,b]$, we can find $V_{ε}(x) \cap K = \{x\}$. Then we can
find a finite cover of $[a,b]$, which is also a finite cover of $K$.
So $K$ is finite.

See also [here](https://math.stackexchange.com/questions/1718788/proving-every-bounded-infinite-set-has-a-limit-point-without-using-bolzano-weier)

### 3.3.13

Let’s call a set clompact if it has the property that every closed cover (i.e., a cover consisting of closed sets) admits a finite subcover. Describe all of the clompact subsets of $R$.

* Solution: all clompact are finite set. Because one point set $\{x\}$ is a closed set.

See also [here](https://math.stackexchange.com/questions/2989359/which-sets-are-clompact)