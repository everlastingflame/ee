[[Combinatorics]]

Permutations are helpful when we want to calculate the total number of orderings for a limited set. If we have $n$ members we're sampling from, and we only care about $k$ samples, we know that there are a total of $n!$ outcomes, but since we only want the first $k$ outcomes, we can divide by $n-k$ tot limit how many observations we look at. This becomes:
$$
\frac{n!}{(n-k)!}
$$
For example, in a horse race if we have 20 horses and we only care about who places in the top 3, this becomes:
$$
\frac{20!}{17!} = \frac{20\cdot 19 \cdot 18 \cdot 17!}{17!} = 20 \cdot 19 \cdot 18 \cdot \left( \frac{17!}{17!} \right) = 20 \cdot 19 \cdot 18
$$

