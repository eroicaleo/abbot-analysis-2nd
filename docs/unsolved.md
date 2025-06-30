
# Unsolved Problems

## Chapter 3

### Theorem 3.4.3

### Ex 3.4.9 (c)

## Chapter 5

### Ex 5.2.9 (c)

If $f$ is differentiable on an interval containing zero and if $\lim_{x \to 0} f'(x) = L$, then it must be that
$L = f'(0)$.

Proof: I realized later we can either use Darboux's theorem
or L'Hospital rule to prove.

### Ex 5.3.1 (b)

This is a extension of this problem, can we remove
the condition that $f'(x)$ needs to be continuous?

### Ex 5.4.4 (c)
### Ex 5.4.8

### Ex 6.2.6(e)

If each $f_n$ has at most a countable number of discontinuities,
and $(f_n(x)) \rightarrow f(x)$ uniformly,
then $f$ has at most a countable number of discontinuities.

### Ex 6.4.7 (b)

Let

$$ 
f(x) = \sum_{k = 1}^{\infty } \frac{\sin (kx)}{k^3} 
$$

Can we determine if f is twice-diﬀerentiable?

### Ex 6.6.9 (b)

### Ex 7.3.4 (b)

If $f$ is increasing and $g$ is integrable, then $g◦f$ is integrable.

### Exercise 8.3.7.

Let

$$ 
c_n = \frac{
1 \cdot 3 \cdot 5 \cdots (2n - 1)
}{
2 \cdot 4 \cdot 6 \cdots 2n
}
$$

Show that $\lim c_n = 0$ but $\sum_{n=0}^{∞} c_n$ diverges.

**Discussion**: I have to rely on the fact mentioned in
the book that

$$
\lim_{n \to \infty} \frac{1}{c_n \sqrt[]{n}} = \sqrt[]{\pi}
$$

Can we have some other ways to prove directly?

# Open Question

1. This is related chapter 5. $f(x)$ is a differentiable on $[a, b]$, $(x_n) \rightarrow c$,
$(y_n) \rightarrow c$, and $c \in (a,b)$.
Is the following true:

$$ 
\lim_{n \to \infty}
\frac{f(x_n)-f(y_n)}{
x_n - y_n
} = f'(c)
$$

Discussion: If $f'(x)$ is continuous. Then this
assumption is true based on L'Hospital rule.

If we have $x_n < x < y_n$, then it becomes exercise 5.4.7.

If $f'(x)$ is not continuous,
then it might not be true.
What if we add a condition that $|f'(x)| < 1$.
 