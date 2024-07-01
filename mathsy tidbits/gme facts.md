\subsection{Proof of \cref{fact:schmidt}} \label{app:schmidt}

\schmidt*


\begin{proof}~
\begin{enumerate}[(i)]
    \item Write $\ket{\psi} = \sum_i \gamma_i \ket{u_i}\ket{v_i}$ in Schmidt decomposition, with $\ket{u_i}$ and $\ket{v_i}$ respectively orthonormal sets and $\gamma_i$ non-negative and non-increasing with $i$. Denote $\gamma_{\max} \equiv \gamma_0$ as the maximum Schmidt coefficient. Clearly taking $\ket{\alpha} = \ket{u_0}$ and $\ket{\beta} = \ket{v_0}$ shows that
\[
    \gamma_{\max} \leq {\max}_{\alpha, \beta} \abs{\bra{\psi} ~ \ket{\alpha} \ket{\beta}}.
\]
We also have that

\begin{align}
    {\max}_{\alpha, \beta} \abs{\bra{\psi} ~ \ket{\alpha} \ket{\beta}}  &\leq \sum \gamma_i \abs{\braket{\alpha}{u_i} \braket{\beta}{v_i}} \\
    &\leq \gamma_{\max}  \sum \abs{\braket{\alpha}{u_i} \braket{\beta}{v_i}} \\
    &\leq \gamma_{\max}  \sqrt{\sum_i \abs{\braket{\alpha}{u_i}}^2 \sum_j \abs{\braket{\beta}{v_j}}^2} \\
    &= \gamma_{\max},
\end{align}
where we used the Triangle and Cauchy-Schwarz inequalities.

\item 
Recall the well known relation between trace distance and fidelity for pure states
\[
    \tfrac{1}{2}\norm{\ketbra{\psi} - \ketbra{\phi}}_1 =  \sqrt{1 - \abs{\braket{\psi}{\phi}}^2}.
\]

    Now let $\ket{\phi} = \ket{\alpha}\ket{\beta}$ be a BP state (written across some bipartition). Then
    \[
    \tfrac{1}{2}\norm{\ketbra{\psi} - \ketbra{\phi}}_1 =  \sqrt{1 - \abs{\bra{\psi} ~ \ket{\alpha}\ket{\beta}}^2} \geq \sqrt{1 - \gamma^2},
    \]
    where the last inequality follows from part $(i)$.
    \end{enumerate}

\end{proof}

\subsection{Proof of \cref{fact:haar}} \label{app:haar} 

\haarcloseness*

\begin{proof}

We can write 

\[
\rho' = \frac{1}{1-p} \int d \phi ~ \ketbra{\phi}^{\otimes k} \mathbf{1}_S (\phi),
\]

where $\mathbf{1}_S (\phi) = 1$ if $\ket{\phi} \in S$ and $0$ otherwise (the indicator function), and $p$ is a normalisation factor enforcing $\text{Tr}(\rho)=1$. Then we have 

\begin{align}
    \norm{\rho - \rho'}_1 &= \norm{\int d\psi ~ \ketbra{\psi}^{\otimes k}  \bigg (\id  - \frac{1}{1-p} \mathbf{1}_S \bigg )}_1 \\
    &\leq \int d\psi ~ \norm{\ketbra{\psi}^{\otimes k}}_1  \abs{1  - \frac{1}{1-p} \mathbf{1}_S } \\
    &= \int d\psi ~ \abs{1  - \frac{1}{1-p} \mathbf{1}_S } \\
    &= \int_S d\psi ~ \left ( \frac{1}{1-p} - 1  \right ) + \int_{S^c} d\psi \\
    &= (1-p)  \left ( \frac{1}{1-p} - 1  \right ) + p \\
    &= 2 p.
\end{align}

