\section{Difference in resource content lower bounds the distance between objects} \label{app:differencecontentlowerbound}

Fix some distance measure $D$ on quantum states. For $\mathcal{F}$ a set of free states, suppose a resource quantifier is defined as 
\[
    Q(\rho) := \min_{\sigma \in \mathcal{F}} D(\rho, \sigma).
\]

\begin{proposition}
    
\label{prop:resourcebounds}

For all states $\rho$, $\sigma$:
\[
\abs{Q(\rho) - Q(\sigma)} \leq D(\rho, \sigma)
\]
\end{proposition} 

\begin{proof}
Consider
\[
    Q(\rho) - Q(\sigma) = \min_{a \in \mathcal{F}}D(\rho, a) - \min_{b \in \mathcal{F}}D(\sigma, b)
\]
and define $\sigma^* = \arg\min_{b \in \mathcal{F}}D(\sigma, b)$. Then in particular, $D(\rho, \sigma^*) \geq \min_{a \in \mathcal{F}}D(\rho, a)$, and we have
\begin{align}
    Q(\rho) - Q(\sigma) & = \min_{a \in \mathcal{F}}D(\rho, a) - \min_{b \in \mathcal{F}}D(\sigma, b) \\
    & \leq D(\rho, \sigma^*) -  D(\sigma, \sigma^*) \\
    & \leq D(\rho, \sigma) \hspace{100pt} \text{(triangle ineq.)}
\end{align}
As $D(\rho, \sigma)$ is symmetric in its arguments, we also have $Q(\sigma) - Q(\rho) \leq D(\rho, \sigma)$, giving the result.
\end{proof}



Now consider the induced distance on channels:
\[
D(\mathcal{E}, \Lambda) := \max_\rho D(\mathcal{E}(\rho), \Lambda (\rho))
\]
and the induced resource quantifier on channels:
\begin{align}
Q(\mathcal{E}) &:= \max_{\rho \in \mathcal{F}} Q(\mathcal{E}(\rho)) \\
&= \max_{\rho \in \mathcal{F}} \min_{\sigma \in \mathcal{F}} D(\mathcal{E}(\rho), \sigma)
\end{align}

\begin{proposition}
    
For all channels $\mathcal{E}$, $\Lambda$:
\[
\abs{Q(\mathcal{E}) - Q(\Lambda)} \leq D(\mathcal{E}, \Lambda)
\]
\end{proposition}

\begin{proof}

\begin{align}
    Q(\mathcal{E}) - Q(\Lambda) &= \max_{\rho \in \mathcal{F}} Q(\mathcal{E}(\rho)) - \max_{\sigma \in \mathcal{F}} Q(\Lambda(\sigma))
\end{align}
Let $\rho^* := \arg \max_{\rho \in \mathcal{F}} Q(\mathcal{E}(\rho))$, so in particular $ - \max_{\sigma \in \mathcal{F}} Q(\Lambda(\sigma)) \leq - Q(\Lambda(\rho^*))$. Then we have
\begin{align}
    Q(\mathcal{E}) - Q(\Lambda) &= \max_{\rho \in \mathcal{F}} Q(\mathcal{E}(\rho)) - \max_{\sigma \in \mathcal{F}} Q(\Lambda(\sigma)) \\
& \leq Q(\mathcal{E}(\rho^*)) -  Q(\Lambda(\rho^*)) \\
& \leq D(\mathcal{E}(\rho^*), \Lambda(\rho^*)) \hspace{100pt}\text{\cref{prop:resourcebounds}}\\
& \leq \max_\tau D(\mathcal{E}(\tau), \Lambda (\tau)) \\
& = D(\mathcal{E}, \Lambda)
\end{align}
    By symmetry of $D(\mathcal{E}, \Lambda)$ we get the result.
\end{proof}

These results could be used to lower bound the distance between two objects if their resource contents are known. Clearly if two objects have the same resource, these bounds become trivial and one cannot say anything (they could in fact be the same object). Perhaps similar results could hold more generally, that is, for any resource quantifier (not just a distance based one). The intuition would be the same, if they have different resource contents, then they must be some non-zero distance away from each other.