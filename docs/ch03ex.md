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

### 3.2.5

A set $F \subset \mathbb{R}$ is closed if and only if every Cauchy sequence contained in $F$ has a limit that is also an element of $F$.

* Proof:
    * $\Rightarrow$ Assume $F \subset \mathbb{R}$ is closed, and $\left( a_n \right)$ is a Cauchy sequence contained in $F$. Then according to Theorem 2.6.4 (Cauchy Criterion), $\left( a_n \right)$ converges. Let $x = \lim a_n$.
        * If $\exists n, \text{such that } a_n = x$, then $x \in F$.
        * If $x \neq a_n, \forall n$, then according to Theorem 3.2.5, $x$ is a limit point of $F$, so $x \in F$.
    * $\Leftarrow$ Assume every Cauchy sequence contained in $F$ has a limit that is also an element of $F$ and $x$ is a limit point of $F$. According Theorem 3.2.5, we can find some sequence $(a_n)$ contained in $F$ satisfying $a_n \ne x$ for all $n \in \mathbb{N}$ and $x = \lim a_n$. Again according to Theorem 2.6.4, $(a_n)$ is a Cauchy sequence, then $x \in F$. $\square$
