[[Combinatorics]]

If we do not care about the order of our total outcomes, this significantly reduces the set, considering that the sets, $\{A,B,C,D\}$ and $\{A,C,B,D\}$ are considered to be unique. For example, if we want to know how many different combinations we can make with 5 letters from the entire alphabet, we can find that we have $n=26$, and $k=5$. If we were worried about position, we would have the result:
$$
\frac{n!}{(n-k)!} = \frac{26!}{21!}=26\cdot 25 \cdot 24 \cdot 23 \cdot 22
$$
But since we don't care about the orderings, we can divide by the total combinations of our group to filter out situations where we have  $\{A,B,C,D,E\}$  and $\{A,B,C,E,D\}$. Since there are $5!$ of that set, and any set with 5 members, we now have the solution:
$$
\frac{26!}{21! \cdot 5!}
$$
We can generalize the combination formula to be:
$$
\frac{n!}{(n-k)!k!} = \begin{pmatrix} n \\ k\end{pmatrix}
$$
This reads as $n$ choose $k$

