\begin{restatable}{lemma}{tracedistancepure}
 \label{lem:tracedistancepure}
    For the induced trace distance, it is sufficient to take the maximum over pure states, i.e. for any channels $\mathcal{E}$, $\mathcal{V}$
    \[
    \mathcal{D}  ( \mathcal{E}, \mathcal{V}  ) := \max_\rho ~ D\bigg ( \mathcal{E}(\rho), \mathcal{V}(\rho)\bigg ) =   \max_{\ket{\phi} } ~ D \bigg ( \mathcal{E}(\ketbra{\phi}), \mathcal{V}(\ketbra{\phi}) \bigg ) .
    \]
\end{restatable}
\begin{proof}
    \begin{align}
         \max_\rho D ( \mathcal{E}(\rho), \mathcal{V}(\rho)) &=  \max_{p_i, \psi_i} D \bigg ( \sum p_i \mathcal{E}( \psi_i), \sum p_i \mathcal{V}( \psi_i) \bigg ) \\
         &\leq \max_{p_i, \psi_i} \sum p_i D(  \mathcal{E}( \psi_i),  \mathcal{V}( \psi_i)) \\
         &\leq \max_{p_i, \psi_i} \sum p_i  \left ( \max_{\phi} D( \mathcal{E}(\phi), \mathcal{V}(\phi)) \right ) \\
         &=  \max_{\phi} D( \mathcal{E}(\phi), \mathcal{V}(\phi)) \\
         & \leq  \max_\rho D( \mathcal{E}(\rho), \mathcal{V}(\rho))
    \end{align}
where $\rho$ denotes a mixed state,  $\psi_i$ and $\phi$ denote pure states, and we used linearity of the channels and joint convexity of the trace distance \cite{nielsen2002quantum}.
\end{proof}


For pure states we also have that  \cite{wilde2013quantum}
\[
D \bigg (\ketbra{\psi}, \ketbra{\phi} \bigg ) = \sqrt{1 - \abs{\braket{\psi}{\phi}}^2}.
\]
Combining this with \cref{lem:tracedistancepure} leads to the following corollary:

\begin{corollary} \label{cor:tdistpure}
    The induced trace distance between unitary channels is given by
    \begin{align}
     \mathcal{D}( U, V ) &= \max_{\ket{\psi}} \sqrt{1- \abs{\bra{\psi}U^\dagger V\ket{\psi}}^2}.
    \end{align}
\end{corollary}