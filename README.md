[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/wM4-KOzy)
# Little-o

In addition to the big-O, big-$\Omega$, and big-$\Theta$ notation that
we covered at the beginning of this class, a few other notations are sometimes
used in asymptotic analysis.  For example, "little-$o$" notation.

Prove (i.e.\ give a formal mathematical proof) that $f(n)\in o(g(n))$ implies
that $f(n)\in O(g(n))$.

Hint: The proof will be *very* short and *very* easy. You can start by
identifying the differences between the definitions of O and o.

I have started with the formal definition of $o$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

## Answer

$f(n)\in o(g(n)) \iff \forall c>0, \exists n_0, \forall n\ge n_0: f(n) < c g(n) \Rightarrow \exists c>0, \exists n_0, \forall n\ge n_0:f(n) \le c g(n)$

Observing the differences between, we can quickly see why little o is considered sticter than big O, and why $f(n)\in o(g(n))$ implies
that $f(n)\in O(g(n))$

There are two key differences:
1) We see that little o requires that the statement must hold $\forall c>0$. But this is changed to $\exists c>0$ in the definition of big O. "for all" of course implies that "there exists"; if the statement is true for every value in the scope, then there exists a value for which it is true.
2) The key inequality is different. In particular, the inequality changes from a strict less than ($<$) in the little o definition to a 'not-strict' less than or equal to ($\le$). And we know that
$f(n) < c g(n) \Rightarrow f(n) \le c g(n)$
