
Let consider a subset $S$ of $n$ integers $[n]:=\{0, \dots n-1 \}$. What is the expected value of 

$$
\mathop{\mathbb{E}}_{S \subseteq [n]} \left [ d^{|S|}\right ]
$$

over all subsets $S\subseteq [n]$, for $d$ a constant, and where $|S|$ denotes the size of the of the set $S$? We can evaluate this as follows

$$
\begin{align}
\mathop{\mathbb{E}}_{S \subseteq [n]} \left [ d^{|S|}\right ] &= \frac{1}{2^n} \sum_{s=0}^{n} {n \choose s} d^s \\
&= \left ( \frac{1+d}{2} \right )^n
\end{align}
$$

What about 
$$
\mathop{\mathbb{E}}_{S,T \subseteq [n]} \left [ d^{|S \cap T|}\right ]
$$
$$
\mathop{\mathbb{E}}_{S,T \subseteq [n]} \left [ d^{|S \cap T| + |S \cap T^c|}\right ]
$$
$$
\mathop{\mathbb{E}}_{S,T \subseteq [n]} \left [ d^{|S \cap T| + |S^c \cap T^c|}\right ]
$$

$$
\mathop{\mathbb{E}}_{S_k \subseteq [n]} \left [ d^{|\cap_k S_k|}\right ]
$$
?