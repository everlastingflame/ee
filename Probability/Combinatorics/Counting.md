[[Combinatorics]]
A basic principle of counting is that if we run $n$ experiments where each experiment $i$ has $k$ different outcomes, we can quantify the total number of outcomes as:

$$
\prod_{i=1}^n k_{i} = k_{1} \cdot k_{2} \cdot k_{3}\dots k_{n}
$$
Example: If we have a 10 character long password using letters from the alphabet and case doesn't matter, then we can calculate the total amount of possible passwords as:
$$
\prod_{i=1}^{10}26 = 26^{10} 
$$
Explanation: We have 10 total experiments or spots, each having 26 different outcomes or letters for each.

The terminology for this type of sampling is **with replacement**, which indicates that we can re-use letters for each spot. This applies to any experiment where we can sample with replacement.

When we sample **without replacement**, the number of outcomes changes significantly. If we run the same experiment, but this time we use only numbers, the password has to be 10 digits, then we know the first trial we have 10 options to choose from, the second trial we have 9, and so on. This would mean we have $10!$ total outcomes for the password problem. The only problem with this is that using the simplistic factorial function $n!$ is that it accounts for every single ordering for $n$ distinct items. If we don't care about this, and we still care about orderings, we can look toward permutations.