
Proof that $1-e^{-f(n)} = f(n) e^{-1}$ if $f(n) \leq 1 ~ \forall n$: 

$$
 \begin{align}
     1-e^{-f(n)} &= 1 - (1 - f(n) + \frac{f(n)^2}{2!} + \dots ) \\
     &= f(n) - \frac{f(n)^2}{2!} + \frac{f(n)^3}{3!} + \dots  \\
     &= f(n) \bigg (1 - \frac{f(n)}{2!} + \frac{f(n)^2}{3!} + \dots \bigg )  \\
     &\leq f(n) \bigg (1 - \frac{1}{2!} + \frac{1}{3!} + \dots \bigg )  \\
     &= f(n) e^{-1}
 \end{align}
 $$