#### Interactions

##### Single-particle Hamiltonian

$$
\begin{array}{}
H_0 &= \sum\limits_{i,j} \sum\limits_{\alpha, \beta} h_{\alpha \beta}^{ij} |i \alpha \rangle \langle j \beta| \\
&= \sum\limits_i \sum\limits_{\alpha, \beta} h_{\alpha \beta} |i \alpha \rangle \langle i \beta|
\end{array}
$$

where $i,j$ label Bravais lattice sites (unit cells), $\alpha, \beta$ denote sites within a unit cell.
$$
|i \alpha \rangle = \frac{1}{\sqrt{N_c}} \sum\limits_k e^{-ikR_i} |k \alpha \rangle \\
\begin{array}{}
H_0 &= \frac{1}{N_c} \sum\limits_i \sum\limits_{\alpha, \beta} h_{\alpha \beta} \sum\limits_{k,k^{\prime}} e^{-i (k-k^{\prime}) R_i} |k\alpha \rangle \langle k^{\prime} \beta | \\
&= \sum\limits_k \sum\limits_{\alpha, \beta} h_{\alpha \beta} |k\alpha \rangle \langle k \beta | \\
\end{array}
$$
The eigenvalue problem
$$
\sum\limits_{\beta} h_{\alpha \beta}(k) u_n^{\beta}(k) = \epsilon_n(k) u_n^{\alpha}(k)
$$
defines the Bloch bands $\epsilon_{n}(k)$ and Bloch states $u_n^{\alpha}(k)$ satisfy $\sum\limits_{\alpha} |u_{n}^{\alpha}(k)|^2 = 1$. $n$ labels bands.

The corresponding eigenstates are given by
$$
|nk \rangle = \gamma^{\dagger}_{nk} |0\rangle = \sum\limits_{\alpha} u_n^{\alpha}(k) |k \alpha \rangle = \sum\limits_{\alpha} u_n^{\alpha}(k) a^{\dagger}_{k,\alpha}|0 \rangle
$$
In terms of operators $\gamma_{nk}$, we have $H_0 = \sum\limits_{n,k} \epsilon_n(k) \gamma_{nk}^{\dagger} \gamma_{nk}$.



##### Density-density interactions

​	Because of lattice effects, interactions do not necessarily lead to a FQHE many-body ground state. When there's a uniform magnetic field, the combination of lattice effects and interactions is not well understood upon increasing the plaquette flux.[1] In Refs. [2,3], the overlap between the Laughlin states on the torus and the lattice many-body ground states was close to unity when the plaquette flux is much smaller than the flux quantum, while it decreases when the plaquette flux becomes of the order of one quarter of the flux quantum. It is thus imperative to study how interactions lift the macroscopic degeneracy of a fractionally filled flat Bloch band and whether a gapped topological ground state emerges. 

​	Let's consider the density-density interactions $H_2$:
$$
H_2 = \frac{1}{2} \sum\limits_{i,j} U_{ij} \hat{n}_i \hat{n}_j
$$
Fourier transform:
$$
U_{ij} = U(R_i-R_j) = \frac{1}{\sqrt{N}} \sum\limits_q e^{-iq(R_i-R_j)}U(q) \\
\hat{n}_i = \hat{n}(R_i) = \frac{1}{N} \sum\limits_q e^{-iqR_i} \hat{n}_q \\
$$

$$
\begin{array}{}
\hat{n}_i &= a^{\dagger}_i a_i = \frac{1}{N} \sum\limits_{k,k^{\prime}} e^{ik^{\prime} R_i} a_{k^{\prime}}^{\dagger} e^{-ikR_i} a_k \\
&= \frac{1}{N} \sum\limits_q e^{-iqR_i} \sum\limits_k a_k^{\dagger} a_{k+q} \\
\hat{n}_q &=  \sum\limits_k a^{\dagger}_k a_{k+q} \\
\end{array} \\
$$

$$
\Rightarrow H_2 = \frac{1}{2} \sum\limits_q U(q) \hat{n}_q \hat{n}_{-q}
$$



Similarly, for $H_2 = \frac{1}{2} \sum\limits_{i,j} \sum\limits_{\alpha, \beta} U^{\alpha \beta}_{ij} \hat{n}_i^{\alpha} \hat{n}_j^{\beta}$, 
$$
U_{ij}^{\alpha \beta} = U(R_i+d_{\alpha}-R_j-d_{\beta}) = \frac{1}{\sqrt{N}} \sum\limits_q e^{-iq(R_i+d_{\alpha}-R_j-d_{\beta})}U(q)
$$

$$
\begin{array}{}
\hat{n}_i^{\alpha} 
&= a_{i,\alpha}^{\dagger} a_{i,\alpha} = \frac{1}{N} \sum\limits_{k,k^{\prime}} e^{-i(k-k^{\prime})(R_i+d_{\alpha})} a^{\dagger}_{k,\alpha} a_{k^{\prime},\alpha} \\
&= \frac{1}{N} \sum\limits_q e^{-iq(R_i+d_{\alpha})} \sum\limits_k a_{k,\alpha}^{\dagger} a_{k-q,\alpha} \\
&= \frac{1}{N} \sum\limits_q e^{-iq(R_i+d_{\alpha})} \hat{n}_{-q}^{\alpha}
\end{array}
$$

the Fourier transform of the interaction term is $H_2 = \frac{1}{2} \sum\limits_{q,\alpha,\beta} U(q) \hat{n}_q^{\alpha} \hat{n}_{-q}^{\beta}$



##### Project to the flat band

$$
H = H_0 + H_2 = \sum\limits_{k,\alpha,\beta} h_{\alpha \beta}(k) a^{\dagger}_{k,\alpha} a_{k,\beta} + \frac{1}{2} \sum\limits_{q,\alpha,\beta} U(q) \sum\limits_{k,k^{\prime}} a^{\dagger}_{k,\alpha} a_{k+q,\alpha} a^{\dagger}_{k^{\prime}, \beta} a_{k^{\prime}-q, \beta}
$$

Project the Hamiltonian to the flat band $m$. The corresponding projection operator is
$$
\mathcal{P}_m = \sum\limits_k |mk \rangle \langle mk|
$$
and use the relations
$$
\langle mk | k^{\prime} \beta \rangle = \sum\limits_{\alpha} u_{m}^{\alpha*}(k) \langle k \alpha| k^{\prime} \beta \rangle = u_{m}^{\beta*}(k) \delta_{kk^{\prime}} \\
\langle k^{\prime} \beta | mk \rangle = \sum\limits_{\alpha} u_{m}^{\alpha}(k) \langle k^{\prime} \beta| k \alpha  \rangle = u_{m}^{\beta}(k) \delta_{kk^{\prime}} \\
$$
The projected Hamiltonian is:
$$
\begin{array}{}
\bar{H}_0 
&= \mathcal{P}_m H_0 \mathcal{P}_m \\
&= \sum\limits_{k_1} |mk_1 \rangle \langle mk_1|  \sum\limits_{k,\alpha,\beta} h_{\alpha \beta}(k) |k \alpha \rangle \langle k \beta|   \sum\limits_{k_2} |mk_2 \rangle \langle mk_2| \\
&= \sum\limits_{k_1,k_2,k,\alpha,\beta} h_{\alpha \beta}(k) u_m^{\alpha *}(k) u_m^{\beta}(k) \delta_{kk_1} \delta_{kk_2} |mk_1 \rangle \langle mk_2 | \\
&= \sum\limits_{k,\alpha} \Big( \sum\limits_{\beta} h_{\alpha \beta}(k) u_m^{\beta}(k) \Big) u_m^{\alpha *}(k)  |mk \rangle \langle mk | \\
&= \sum\limits_{k} \epsilon_m(k)  \sum\limits_{\alpha} |u_m^{\alpha}(k)|^2 |mk \rangle \langle mk| \\
&= \sum\limits_k \epsilon_m(k) |mk \rangle \langle mk | \\
&= \sum\limits_k \epsilon_m(k) \gamma_{mk}^{\dagger} \gamma_{mk}
\end{array}
$$

$$
\begin{array}{}
\bar{H}_2 
&= \mathcal{P}_m H_2 \mathcal{P}_m =  \frac{1}{2} \sum\limits_{q,\alpha,\beta} U(q)  \mathcal{P}_m \hat{n}_q^{\alpha} \hat{n}_{-q}^{\beta}  \mathcal{P}_m \\
&= \frac{1}{2} \sum\limits_{q,\alpha,\beta} U(q)  \mathcal{P}_m \hat{n}_q^{\alpha} (\mathcal{P}_m^2+\mathcal{P}_{\bar{m}}^2) \hat{n}_{-q}^{\beta}  \mathcal{P}_m \\
&\approx  \frac{1}{2} \sum\limits_{q,\alpha,\beta} U(q)  \mathcal{P}_m \hat{n}_q^{\alpha} \mathcal{P}_m \mathcal{P}_m \hat{n}_{-q}^{\beta}  \mathcal{P}_m \\
\end{array}
$$

where we used $1=\mathcal{P}_m + \mathcal{P}_{\bar{m}}$, $\mathcal{P}_m^2 = \mathcal{P}_m$.
$$
\begin{array}{}
\mathcal{P}_m \hat{n}_q^{\alpha} \mathcal{P}_m 
&= \sum\limits_{k_1,k_2,k} |mk_1 \rangle \langle mk_1| a^{\dagger}_{k,\alpha} a_{k+q,\alpha} |mk_2 \rangle \langle mk_2| \\
&= \sum\limits_{k_1,k_2,k} |mk_1 \rangle \langle mk_1| k \alpha \rangle \langle k+q,\alpha |mk_2 \rangle \langle mk_2| \\
&= \sum\limits_{k_1,k_2,k} u_m^{\alpha*}(k) \delta_{k,k_1} u_m^{\alpha}(k+q) \delta_{k+q,k_2}|mk_1 \rangle \langle mk_2| \\
&= \sum\limits_k u_m^{\alpha*}(k) u_m^{\alpha}(k+q) |m,k \rangle \langle m,k+q| \\
&= \sum\limits_k u_m^{\alpha*}(k) u_m^{\alpha}(k+q) \gamma_{m,k}^{\dagger} \gamma_{m,k+q}
\end{array} \\
$$

$$
\begin{array}{}
\bar{H}_2 
&= \frac{1}{2} \sum\limits_{q,k_1,k_2} U(q) \sum\limits_{\alpha, \beta} u_m^{\alpha*}(k_1) u_m^{\alpha}(k_1+q)  u_m^{\beta*}(k_2) u_m^{\beta}(k_2-q)   \gamma_{m,k_1}^{\dagger} \gamma_{m,k_1+q} \gamma_{m,k_2}^{\dagger} \gamma_{m,k_2-q} \\
&= \frac{1}{2} \sum\limits_{q} U(q) \bar{\rho}_{q;m} \bar{\rho}_{-q;m} 
\end{array} 
$$

where
$$
\bar{\rho}_{q;m} = \sum\limits_{k,\alpha} u_m^{\alpha*}(k) u_m^{\alpha}(k+q) \gamma_{m,k}^{\dagger} \gamma_{m,k+q}
$$


#### Two-body problem with on-site interaction (lattice model)

##### 1D

$$
H = -t \sum\limits_i |x_i^1 \rangle \langle x_{i+1}^1 | + |x_i^2 \rangle \langle x_{i+1}^2 | + h.c. + \frac{U}{2} \sum\limits_i |x_i^1, x_i^2 \rangle \langle x_i^1, x_i^2 |
$$

where the superscripts 1,2 denote two particles and subscripts $i$ denote lattice sites. The wave function
$$
|\Psi \rangle = \sum\limits_{i,j} f( x_i^1, x_j^2 ) |x_i^1, x_j^2 \rangle
$$

$$
\begin{array}{}
H|\Psi \rangle &= -t\sum\limits_{i,m,n} f(x_m^1,x_n^2) \Big[ \delta_{i+1,m} |x_i^1, x_n^2 \rangle + \delta_{i,m} |x_{i+1}^1, x_n^2 \rangle + \delta_{i+1,n} |x_m^1,x_i^2 \rangle + \delta_{i,n} |x_m^1,x_{i+1}^2 \rangle \Big] \\
& \ \ \ \ + \frac{U}{2} \sum\limits_{i,m,n} f(x_m^1,x_n^2) \delta_{i,m} \delta_{i,n} |x_i^1, x_i^2 \rangle \\
&= -t \sum\limits_{m,n} f(x_m^1,x_n^2) \Big[ |x_{m-1}^1, x_n^2 \rangle +  |x_{m+1}^1, x_n^2 \rangle +  |x_m^1,x_{n-1}^2 \rangle + |x_m^1,x_{n+1}^2 \rangle \Big] \\
& \ \ \ \ + \frac{U}{2} \sum\limits_{m,n} f(x_m^1,x_n^2) \delta_{m,n} |x_m^1, x_n^2 \rangle \\
&= \sum\limits_{m,n} \Big\{ -t \big[ f(x_{m+1}^1,x_n^2) + f(x_{m-1}^1,x_n^2) +  f(x_{m}^1,x_{n+1}^2) + f(x_{m}^1,x_{n-1}^2) \big] + \frac{U}{2} f(x_{m}^1,x_n^2) \delta_{m,n} \Big\} |x_{m}^1, x_n^2 \rangle \\
& = \sum\limits_{m,n} E  f(x_{m}^1,x_n^2) |x_{m}^1, x_n^2 \rangle
 \end{array}
$$

$$
-t \big[ f(x_{m+1}^1,x_n^2) + f(x_{m-1}^1,x_n^2) +  f(x_{m}^1,x_{n+1}^2) + f(x_{m}^1,x_{n-1}^2) \big] + \frac{U}{2} f(x_{m}^1,x_n^2) \delta_{m,n} = E  f(x_{m}^1,x_n^2) 
$$

For two-body problem, the wave function can always be seperated to the center-of-mass motion and the relative motion:
$$
f(x_i^1,x_j^2) = e^{ iKR} \psi_K(r)
$$
where $K=k^1+k^2$, $R = \frac{1}{2}(x_i^1+x_j^2)$, $r=x_i^1-x_j^2$.
$$
-2t \cos(Ka/2) \big[ \psi_K(j+1) + \psi_K(j-1) \big] + \frac{U}{2} \delta_{j,0} \psi_K(j) = E \psi_K(j)
$$
$j=m-n \in 1-N, \dots, N-1$ and $N$ is the number of lattice sites.











[1] Titus Neupert et al., Fractional Quantum Hall States at Zero Magnetic Field.

[2] A. S. Sorensen, E. Demler, and M. D. Lukin, Phys. Rev. Lett. 94, 086803 (2005).

[3] M. Hafezi, A. S. Sorensen, E. Demler, and M. D. Lukin, Phys. Rev. A 76, 023613 (2007).