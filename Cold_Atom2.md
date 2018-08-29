#### Interactions

##### Single-particle Hamiltonian

$$
\begin{array}{}
H_0 &= \sum\limits_{i,j} \sum\limits_{\alpha, \beta} h_{\alpha \beta}^{ij} |i \alpha \rangle \langle j \beta|
\end{array}
$$

where $i,j$ label Bravais lattice sites (unit cells), $\alpha, \beta$ denote sites within a unit cell.
$$
|i \alpha \rangle = \frac{1}{\sqrt{N_c}} \sum\limits_k e^{-ikR_i} |k \alpha \rangle \\
\begin{array}{}
H_0 &= \frac{1}{N_c} \sum\limits_{i,j} \sum\limits_{\alpha, \beta} h_{\alpha \beta} ^{ij}\sum\limits_{k,k^{\prime}} e^{-i k R_i + ik^{\prime} R_j} |k\alpha \rangle \langle k^{\prime} \beta | \\
&= \frac{1}{N_c} \sum\limits_{i,l} \sum\limits_{\alpha, \beta} h_{\alpha \beta} ^{ij}\sum\limits_{k,k^{\prime}} e^{-i (k -k^{\prime})  R_i + ik^{\prime} (R_j- R_i)} |k\alpha \rangle \langle k^{\prime} \beta | \\
&=  \sum\limits_{l} \sum\limits_{\alpha, \beta} h_{\alpha \beta} (l)\sum\limits_{k} e^{ ik R_l} |k\alpha \rangle \langle k^{\prime} \beta | \\
&= \sum\limits_k \sum\limits_{\alpha, \beta} h_{\alpha \beta}(k) |k\alpha \rangle \langle k \beta | \\
\end{array}
$$
where $ l = j - i$, and $R_l = R_j - R_i$. and The fourier transfer is,
$$
h_{\alpha\beta} (k) = \sum_l h_{\alpha\beta}(l) e^{ikR_l}.
$$
During the derivation, we have used the assumption that the hopping only depends on the relative position, thus 
$$
h_{\alpha\beta} ^{ij} =  h_{\alpha\beta} ( l ). 
$$
We also used,
$$
\frac{1}{N_c} \sum_i  e^{-i(k-k^\prime) R_i}  = \delta _{k,k^\prime}.
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

Because of lattice effects, interactions do not necessarily lead to a FQHE many-body ground state. When there's a uniform magnetic field, the combination of lattice effects and interactions is not well understood upon increasing the plaquette flux.[1] In Refs. [2,3], the overlap between the Laughlin states on the torus and the lattice many-body ground states was close to unity when the plaquette flux is much smaller than the flux quantum, while it decreases when the plaquette flux becomes of the order of one quarter of the flux quantum. It is thus imperative to study how interactions lift the macroscopic degeneracy of a fractionally filled flat Bloch band and whether a gapped topological ground state emerges. 
Let's consider the density-density interactions $H_2$:
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
\hat{n}_i &= a^{\dagger}_i a_i = \frac{1}{N} \sum\limits_{k,k^{\prime}} e^{-ik R_i} a_{k}^{\dagger} e^{ik^{\prime}R_i} a_{k^{\prime}} \\
&= \frac{1}{N} \sum\limits_q e^{-iqR_i} \sum\limits_k a_k^{\dagger} a_{k-q} \\
\hat{n}_{-q} &=  \sum\limits_k a^{\dagger}_k a_{k-q} \\
\end{array} \\
$$

$$
\color{blue}{ \sum_i \hat a_i^\dagger a_i = \sum_k a_k^\dagger a_k }
$$



__Make the phase factor consistent. __
$$
\color{red}{a_i^\dagger = \frac{1}{\sqrt N} \sum_k e^{-ikR_i}a_k^\dagger}
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
&= a_{i,\alpha}^{\dagger} a_{i,\alpha} = \frac{1}{N} \sum\limits_{k,k^{\prime}} \color{red}{e^{-i(k-k^{\prime})(R_i+d_{\alpha})} }a^{\dagger}_{k,\alpha} a_{k^{\prime},\alpha} \\
&= \frac{1}{N} \sum\limits_q e^{-iq(R_i+d_{\alpha})} \sum\limits_k a_{k,\alpha}^{\dagger} a_{k-q,\alpha} \\
&= \frac{1}{N} \sum\limits_q e^{-iq(R_i+d_{\alpha})} \color{red}{\hat{n}_{-q}^{\alpha}}
\end{array}
$$

__The above convention is not consistent with the previous one. I agree with the above one. __

the Fourier transform of the interaction term is $H_2 = \frac{1}{2} \sum\limits_{q,\alpha,\beta} U(q) \hat{n}_q^{\alpha} \hat{n}_{-q}^{\beta} =  \frac{1}{2} \sum\limits_{q} U(q) \hat{n}_q \hat{n}_{-q}$, where $\hat n_q = \sum \limits_\alpha \hat n_q^\alpha$.

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

__comment:__ In other words, only the $m$ band is left. And flat band means $\epsilon (m) = constant$.
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
\bar{\rho}_{q;m} = \mathcal{P}_m \cdot  \sum_\alpha\hat{n}_q^{\alpha}\cdot \mathcal{P}_m  = \sum\limits_{k,\alpha} u_m^{\alpha*}(k) u_m^{\alpha}(k+q) \gamma_{m,k}^{\dagger} \gamma_{m,k+q}
$$



#### Two-body problem with on-site interaction (lattice model)

In continuum limit, Laughlin's wave function is the exact ground state of the two particle problem:
$$
\Psi_m(r_1,r_2) = f(Z)(z_1-z_2)^m e^{-|z_1-z_2|^2/8}e^{-|Z|^2/2}
$$
where $Z = \frac{1}{2}(z_1+z_2)$ is the complex-coordinate representation of the center-of-mass coordinate.

Can we numerically or analytically construct the Laughlin's wave function in the lattice model for two-particle problem with on-site interaction?



__1D*__: 

The second quantization is 
$$
H = - t \sum_i a_i^\dagger a_{i+1}  + h.c.+ \frac{U}{2} \sum_i n^2_i
$$
The first term is the single particle hopping energy. To focus on the many body physics for now, we assume a flat band that are well separated from others, thus the first term is simply ignore and we are left with the interaction,
$$
V =\frac{U}{2} \sum_i n^2_i
$$
which means an onsite interaction. 

The Hilbert space spanned by two particle states of Bosons can be explicitly written down, which has dimension of $N(N+1)/2$, with N the number of sites in 1D chain. It has two scenarios. The two particle on the same site,
$$
|0, 0, \dots, 2, \dots, 0\rang =\frac{1}{\sqrt 2!}a_i^{\dagger 2} |0\rang = |n_i=2\rang
$$
Or the two particle on difference sites,
$$
|0, 0, \dots, 1, \dots,1, \dots, 0\rang =a_i^{\dagger} a_j^\dagger |0\rang = |n_i=1,n_j=1\rang \ \ ( i<j)
$$
Thus the total dimension is $ N + C_N^2 =N + N(N-1)/2= N(N+1)/2 $ . 

The matrix elements between the states, which has three scenarios, are
$$
\lang n_i = 2| V|n_j=2\rang = 2U \delta_{ij}
$$

$$
\lang n_i = 2| V|n_j=1,n_k =1\rang = 0
$$

$$
\lang n_i=1,n_j =1| V|n_k=1,n_l =1\rang = \delta^i_k\delta^j_l U
$$

Thus the interaction matrix is diagonal, with $V = \{2U, U\}$

In the matrix form, if you list the states as
$$
\begin{array}{}
|n_0 = 2\rang \\
  \ \ \dots \\
|n_{N-1} = 2\rang \\
|n_0=1,n_1 = 1\rang \\
|n_0=1,n_2 = 1\rang \\
\ \ \dots \\
|n_{N-2}=1,n_{N-1} = 1\rang \\
\end{array}
$$
The matrix form of $V$ is, for 3 sites
$$
\begin{array}{}
2,0,0,0,0,0 \\
0,2,0,0,0,0 \\
0,0,2,0,0,0 \\
0,0,0,1,0,0 \\
0,0,0,0,1,0\\
0,0,0,0,0,1
\end{array}
$$
Since the result we have now is trivial, next we add the hopping terms. Hopping can only have nonzero elements between 
$$
|n_i = 2 \rang \text{ and  }|n_i = 1, n_{i+ 1} = 1\rang
$$
or
$$
|n_i = 2 \rang \text{ and  }|n_{i-1} = 1, n_{i} = 1\rang 
$$
and 
$$
|n_i = 1, n_{j} = 1\rang \text{  and  } |n_i = 1, n_{j+1} = 1\rang
$$
or 
$$
|n_{i} = 1, n_{j} = 1\rang \text{  and  } |n_{i-1} = 1, n_{j} = 1\rang
$$
Note we keep using the convention $i<j$ to run over all the possibilities without double counting. Numerically, this process can be done in one loop for $i \in \{0,1, N-1\}$ , and the other for a double loop with constraint $i<j$. 

For the 3 site case
$$
\begin{array}{}
2,0,0,0,x,x \\
0,2,0,x,0,x \\
0,0,2,x,x,0 \\
0,x,x,1,x,x \\
x,0,x,x,1,x\\
x,x,0,x,x,1
\end{array}
$$
with $x = -t/U$ . We assumed a periodic chain. 



Once we obtain the H matrix, and henceforce the eigenvalue and eigenfunction, the profile of wavefunction in real space (sites) can be obtain 

However, to directly compare with the continum limit of Laughling's wavefunction, the 1D model should be promoted to a 2D version. 



##### 1D

$$
H = -t \sum\limits_i a^{\dagger}_{i+1}a_i + h.c. + \frac{U}{2} \sum\limits_i n_i (n_i-1)
$$

The wave function
$$
\begin{array}{}
| \Psi \rangle &= \sum\limits_{l \leq m} f(l,m)|1_l,1_m \rangle \\
&= \sum\limits_{l < m} f(l,m)|1_l,1_m \rangle + \sum\limits_{j=1}^N f(j,j)|2_j \rangle
\end{array}
$$

$$
\begin{array}{}
H|\Psi \rangle 
&= -t \sum\limits_{l \leq m} 
\Big[ 
|1_{l+1},1_m \rangle + |1_{l},1_{m+1} \rangle + |1_{l-1},1_{m} \rangle + |1_{l},1_{m-1} \rangle + \delta_{l,m}\sqrt{2}|1_l,1_{m+1} \rangle + \delta_{l,m}\sqrt{2}|1_{l-1},1_{m} \rangle
\Big]  
f(l,m) \\
&+ U \sum\limits_{l \leq m} \delta_{l,m} |1_l,1_m \rangle f(l,m) \\
&= \sum\limits_{l \leq m} 
\Big\{ 
-t \big[ f(l-1,m) + (1+\sqrt{2}\delta_{l,m-1})f(l,m-1) + (1+\sqrt{2}\delta_{l+1,m})f(l+1,m) + f(l,m+1) \big] \\
&+ U \delta_{l,m} f(l,m)
\Big\} |1_l,1_m \rangle  \\
&= E\sum\limits_{l \leq m}  f(l,m)|1_l,1_m \rangle 
\end{array}
$$

$$
-t \big[ f(l-1,m) + (1+\sqrt{2}\delta_{l,m-1})f(l,m-1) + (1+\sqrt{2}\delta_{l+1,m})f(l+1,m) + f(l,m+1) \big] + U \delta_{l,m} f(l,m) = E f(l,m)
$$

For two-body problem, the wave function can always be seperated to the center-of-mass motion and the relative motion:
$$
f(l,m) = e^{iKR}\psi_K(r) = e^{iKR}\psi_K(|l-m|)
$$
where $K$ is the total momentum of two particles, $R = \frac{1}{2} (R_l+R_m)$, $r = |R_l-R_m|$.



In momentum space, by using $a_i^\dagger = \frac{1}{\sqrt N} \sum_k e^{-ikR_i}a_k^\dagger$, the Hamiltonian is
$$
H = -t \sum\limits_k 2\cos(ka) a^{\dagger}_k a_k + \frac{U}{2N} \sum\limits_{q,k,k^{\prime}} a^{\dagger}_{k+q}a_k a^{\dagger}_{k^{\prime}-q} a_{k^{\prime}}
$$

$$
|\Psi \rangle = \sum\limits_{k_1,k_2} f(k_1,k_2) |k_1,k_2 \rangle
$$

here $|k_1,k_2 \rangle = \frac{1}{\sqrt{2}} (|k_1 \rangle \otimes |k_2 \rangle + |k_2 \rangle \otimes |k_1 \rangle )$.
$$
\begin{array}{}
\sum\limits_{q,k,k^{\prime}} a^{\dagger}_{k+q}a_k a^{\dagger}_{k^{\prime}-q} a_{k^{\prime}} |\Psi \rangle 
&= \sum\limits_{q,k,k^{\prime},k_1,k_2}a^{\dagger}_{k+q}a_k \Big(\delta_{k^{\prime},k_1}|k^{\prime}-q,k_2 \rangle + \delta_{k^{\prime},k_2}|k_1,k^{\prime}-q \rangle \Big)f(k_1,k_2) \\
&= \sum\limits_{q,k,k_1,k_2}a^{\dagger}_{k+q}a_k \Big(|k_1-q,k_2 \rangle + |k_1,k_2-q \rangle \Big)f(k_1,k_2) \\
&= \sum\limits_{q,k,k_1,k_2}  \Big( \delta_{k,k_1-q} |k+q,k_2 \rangle + \delta_{k,k_2} |k_1-q,k+q \rangle \\
&\ \ \ \ \ \ \ \ \ \ \ \ \  + \delta_{k,k_1} |k+q,k_2-q \rangle + \delta_{k,k_2-q} |k_1,k+q \rangle  \Big) f(k_1,k_2)\\
&= \sum\limits_{q,k_1,k_2} \Big( 2|k_1,k_2 \rangle + |k_1-q,k_2+q \rangle + |k_1+q,k_2-q \rangle \Big) f(k_1,k_2) \\
&= \sum\limits_{q,k_1,k_2} \Big( 2f(k_1,k_2) + f(k_1+q,k_2-q) + f(k_1-q,k_2+q) \Big) |k_1,k_2 \rangle
\end{array}
$$

$$
\begin{array}{}
H| \Psi \rangle 
&= \sum\limits_{k_1,k_2} -2t\big[ \cos(k_1a)+\cos(k_2a) \big] f(k_1,k_2) |k_1,k_2 \rangle \\
& \ + \frac{U}{2N} \sum\limits_{q,k_1,k_2} \Big( 2f(k_1,k_2) + f(k_1+q,k_2-q)+ f(k_1-q,k_2+q) \Big) |k_1,k_2 \rangle \\
&=E\sum\limits_{k_1,k_2}f(k_1,k_2) |k_1,k_2 \rangle
\end{array}
$$

$$
\Big[-2t \big( \cos(k_1a)+\cos(k_2a) \big) + U \Big]f(k_1,k_2) + \frac{U}{2N} \sum\limits_q \Big[ f(k_1+q,k_2-q) + f(k_1-q,k_2+q) \Big] =E f(k_1,k_2)
$$

Rewrite $f(k_1,k_2) = f_K(k)$, where $k_1 = \frac{K}{2}+k$, $k_2 = \frac{K}{2}-k$,
$$
\Big[-2t \big( \cos\big((\frac{K}{2}+k)a\big)+\cos\big((\frac{K}{2}-k)a\big) \big) + U \Big]f_K(k) + \frac{U}{2N} \sum\limits_q \Big[ f_K(k+q) + f_K(k-q) \Big] =E f_K(k)
$$


##### 2D with magnetic field $A= (0,Bx,0)$

$$
H = -t \sum\limits_{m,n} \Big( a^{\dagger}_{m+1,n}a_{m,n} + e^{i\phi_{m,n}^y} a^{\dagger}_{m,n+1}a_{m,n} + h.c. \Big) + \frac{U}{2}\sum\limits_{m,n} n_{m,n}n_{m,n}
$$

where $\phi_{m,n}^y =-\frac{e}{\hbar}\int \vec{A} \cdot d\vec{r} = -\frac{e}{\hbar} Bx\delta y = -\frac{e}{\hbar}Bmab = -2\pi m\frac{\Phi}{\Phi_0} = -2\pi m \alpha$.

Assuming $\alpha = 1/4$, then the lattice constant along the x the direction is, $a_1 = 4a$, when $\phi_{4,n}^y = - 2\pi$ completes one period. The atoms within one unit cell is labeled as $\{0,1,2,3\}$, and the creational operator is $a^\beta_{i,j} \text{for } \beta \in \{0,1,2,3\} $. 
$$
\begin{array}{}
H = -t \sum\limits_{i,j} \Big[ &a_{i,j}^{1\dagger}a_{i,j}^0 + a_{i,j}^{2\dagger}a_{i,j}^1 + a_{i,j}^{3\dagger}a_{i,j}^2 + a_{i+1,j}^{0\dagger}a_{i,j}^3  + h.c.\\
&+ a_{i,j+1}^{0\dagger}a_{i,j}^{0} +e^{-i\frac{\pi}{2}} a_{i,j+1}^{1\dagger}a_{i,j}^{1} +e^{-i\pi} a_{i,j+1}^{2\dagger}a_{i,j}^{2} +e^{-i\frac{3\pi}{2}} a_{i,j+1}^{3\dagger}a_{i,j}^{3} + h.c. \Big] \\
&+ \frac{U}{2} \sum\limits_{i,j}\sum\limits_{\beta=0}^3 n_{i,j}^{\beta} (n_{i,j}^{\beta}-1)
\end{array}
$$
where $i,j$ labels unit site.



Then transform into $k$ space gives us the following Hamiltonian, $ a_i^\dagger \sim a_k^\dagger e^{-ikR} $
$$
\begin{array}{}
H^0_k =  &- t (a_k^{1\dagger} a_k^0  + a_k^{2\dagger} a_k^1+ a_k^{3\dagger} a_k^2 + e^{-ik_x a_1} a_k^{0\dagger} a_k^3  + h.c.) \\
&-t ( e^{-ik_ya_2}a_k^{0\dagger}a_k^0  + e^{-ik_ya_2- i\pi/2 }a_k^{1\dagger}a_k^1  + e^{-ik_ya_2- i\pi}a_k^{2\dagger}a_k^2  + e^{-ik_ya_2- i3\pi/2}a_k^{3\dagger}a_k^3  + h.c.) \\
H^0_k =  &- t (a_k^{1\dagger} a_k^0  + a_k^{2\dagger} a_k^1+ a_k^{3\dagger} a_k^2 + e^{-ik_x a_1} a_k^{0\dagger} a_k^3  + h.c.) \\
&-2t \bigg[ \cos(k_ya_2)a_k^{0\dagger}a_k^0  + \cos({k_ya_2+\pi/2 })a_k^{1\dagger}a_k^1  + \cos({k_ya_2+\pi})a_k^{2\dagger}a_k^2  + \cos({k_ya_2+3\pi/2})a_k^{3\dagger}a_k^3\bigg ]
\end{array}
$$
Here $a_1 = 4a, a_2 = a​$.

The interaction part is 
$$
\begin{array}{}
V = &\frac{U}{2} \sum \limits_{ij} \sum\limits_{\beta} n_{ij}^\beta (n_{ij}^\beta  -1) \\ 
  \ \ \ \  = & \sum_\beta \bigg[ \frac{U}{2N_xN_y} \sum_{q,k,k^\prime} a_{k+q}^\dagger a_k \cdot a_{k^\prime - q }^\dagger a_{k^\prime}  -\frac{U}{2} \sum_k a_k^\dagger a_k\bigg]^\beta
\end{array}
$$
Note $\sum_{\beta k} n_k^\beta = n_{total}$.  For fixed number of particle system, the second term is a constant, thus can be ignored. 
$$
V =\frac{U}{2N_xN_y} \sum \limits_\beta \sum_{q} \hat n_q^\beta \hat n_{-q}^\beta = \frac{U}{2N_xN_y} \sum \limits_\beta \sum_{q,k,k^\prime }a_{k+q}^\dagger  a_{k^\prime - q }^\dagger a_k  a_{k^\prime} 
$$
With $\hat n_q  = \sum_k a_{k+q}^\dagger a_k$ is the FT of $n_i = a_i^\dagger a_i$. The two body interaction conserves the total momentum
$$
K = k + k^\prime,
$$
But the relative momentum is changed by 
$$
K_- = k + q - (k^\prime - q)  = k- k^\prime  + 2q = K_- ^\prime + 2q.
$$
__The 2 body Hilbert space__

The Bosonic Hibert space in the particle number representation in $k$ space has the dimention of $N(N+1)/2$ , where $N = 4N_x N_y $. 

An observation in the Hopping and interaction is that the total momentum is conserved. Thus it is diagnolized in $K$ space. In the following, we focus on the $K = 0$ space. The trick thing is that the dimention of the Hilbert space depends on the site number. For example, in 1D, if N = 3, then it could be $|n_{k =0} = 2\rang, |n_{k = 2\pi/3} = 1, n_{k = 4\pi/3} = 1\rang$, 2 possibilities. If $N=4$, then it could be $ |n_{k = 0} = 2 \rang, |n_{k = \pi/2} = 1, n_{k = 3\pi/2} = 1\rang, |n_{k = \pi} = 2 \rang$ , 3 possiblities. 

A notation in relative momentum is 
$$
|  K_-= 0\rang, |K_- = 2\pi/3 \rang
$$
and 
$$
| K_- = 0 \rang, | K_- = \pi \rang, |K_- = 0\rang
$$
where we see a degeneracy in the $K_-, K$ representation, which can happen in time reserval points. In 1D dimension is $(N+2)/2$ for $N \in \text {even}$ .  In 2D, there are 4 points. Let's take both $N_x,N_y $ be even number. Then the dimension of the Hilbert space with $K =0$ is , 
$$
\frac{N_xN_y - 4}{2} + 4 = \frac{N_xN_y + 4}{2}.
$$


If there are degrees of freedom within unitcell, e.g. 4 in our example, there is an additional factor 
$$
4 + \frac{4(4-1)}{2} = 10
$$
The total dimention is then 
$$
\frac{N_xN_y + 4}{2} \cdot 10 = 5 (N_xN_y + 4).
$$
 We can list the $K_-$ space and atom space, then write down the matrix. 

There are the following kind of states, in $k$ space, 3 kind; in atom space, 2 kind. Totally 6 kind. 

The basis are composed of two different states, or one states with occupation number, 2. The latter has the following possibilities, when $k \in TRP$, which has 4 points, and atom labels are the same, which has 4. Thus totally 16 states has occupation number 2. All the other possiblities are composed of two different states, distinguashed by $k$ and/or atom. 
$$
|k_x, k_y, \beta_1,\beta_2\rang
$$


We know 
$$
n_{ij} = a_{ij}^\dagger a_{ij} = \frac{1}{N_xN_y} \sum \limits_{k k ^\prime}e^{-i(k - k^\prime )R_{ij}} a_k^\dagger a_{k^\prime}  = \frac{1}{N_xN_y} \sum_q  e^{-iqR_{ij}}\sum_k a_{k+q}^\dagger a_k
$$
In momentum space, by using $a_{m,n}^\dagger = \frac{1}{N} \sum\limits_k e^{-ik_xma} e^{-ik_yna} a_k^\dagger$, the Hamiltonian is
$$
\begin{array}{}
H =& -t \Big[\sum\limits_{k} 2\cos(k_xa) a^{\dagger}_k a_k + \sum\limits_{k,k^{\prime}} \delta_{k_y,k_y^{\prime}} \big(\delta_{k_x-k_x^{\prime},-\frac{2\pi \alpha}{a}} e^{-ik_ya} + \delta_{k_x-k_x^{\prime},\frac{2\pi \alpha}{a}} e^{ik_ya} \big) a^{\dagger}_k a_{k^{\prime}}  \Big] \\
&+ \frac{U}{2N^2} \sum\limits_{q,k,k^{\prime}} a^{\dagger}_{k+q} a_k a^{\dagger}_{k^{\prime}-q} a_{k^{\prime}}
\end{array}
$$

$$
|\Psi \rangle = \sum\limits_{k_1,k_2} f(k_1,k_2) |k_{1},k_{2} \rangle
$$

$$
\begin{array}{}
H|\Psi \rangle 
&= -t \sum\limits_{k_1,k_2}\Big\{ 2 \big[ \cos(k_{1x}a) + \cos(k_{2x}a) \big] f(k_1,k_2) \\
&+ e^{-ik_{1y}a} f(k_{1x}+2\pi \alpha/a,k_{1y},k_2) 
+ e^{ik_{1y}a} f(k_{1x}-2\pi \alpha/a,k_{1y},k_2) \\
&+ e^{-ik_{2y}a} f(k_1,k_{2x}+2\pi \alpha/a,k_{2y})
+ e^{ik_{2y}a} f(k_1,k_{2x}-2\pi \alpha/a,k_{2y})
\Big\} |k_1,k_2 \rangle \\
&+ U \sum\limits_{k_1,k_2} f(k_1,k_2) |k_1,k_2 \rangle + \frac{U}{2N^2} \sum\limits_{q,k_1,k_2} \big[ f(k_1+q,k_2-q) + f(k_1-q,k_2+q) \big] |k_1,k_2 \rangle \\
&=E \sum\limits_{k_1,k_2} f(k_1,k_2) |k_1,k_2 \rangle
\end{array}
$$

$$
\begin{array}{}
-t 
\Big\{ 2\big[ \cos(k_{1x}a)+\cos(k_{2x}a) - \frac{U}{2t} \big] f(k_1,k_2) \\
+ e^{-ik_{1y}a} f(k_{1x}+2\pi \alpha/a,k_{1y},k_2) 
+ e^{ik_{1y}a} f(k_{1x}-2\pi \alpha/a,k_{1y},k_2) \\
+ e^{-ik_{2y}a} f(k_1,k_{2x}+2\pi \alpha/a,k_{2y})
+ e^{ik_{2y}a} f(k_1,k_{2x}-2\pi \alpha/a,k_{2y})
\Big\} \\
+ \frac{U}{2N^2} \sum\limits_q \big[ f(k_1+q,k_2-q) + f(k_1-q,k_2+q) \big] \\
=E f(k_1,k_2)
\end{array}
$$

$$
\begin{array}{}
-t 
\Big\{ 2\big[ \cos(\frac{K_x}{2}+k_x)a+\cos(\frac{K_x}{2}-k_x)a - \frac{U}{2t} \big] f_{K_x,K_y}(k_x,k_y) \\
+ e^{-i(\frac{K_y}{2}+k_y)a} f_{K_x+k_0,K_y}(k_x+k_0/2,k_y) 
+ e^{i(\frac{K_y}{2}+k_y)a} f_{K_x-k_0,K_y}(k_x-k_0/2,k_y)  \\
+ e^{-i(\frac{K_y}{2}-k_y)a} f_{K_x+k_0,K_y}(k_x-k_0/2,k_y)
+ e^{i(\frac{K_y}{2}-k_y)a} f_{K_x-k_0,K_y}(k_x+k_0/2,k_y)
\Big\} \\
+ \frac{U}{2N^2} \sum\limits_q \big[ f_{K_x,K_y}(k_x+q_x,k_y+q_y) + f_{K_x,K_y}(k_x-q_x,k_y-q_y) \big] \\
=E f_{K_x,K_y}(k_x,k_y)
\end{array}
$$

where $k_0=2\pi \alpha/a$.



##### 2D with magnetic field $A= -\frac{B}{2}(y,-x,0)$

$$
H = -t \sum\limits_{m,n} \Big( e^{i\phi_{m,n}^x} a^{\dagger}_{m+1,n}a_{m,n} + e^{i\phi_{m,n}^y} a^{\dagger}_{m,n+1}a_{m,n} + h.c. \Big) + \frac{U}{2}\sum\limits_{m,n} n_{m,n}n_{m,n}
$$

here $\phi_{m,n}^y = -\pi m \alpha$, $\phi_{m,n}^x = \pi n \alpha$
$$
\begin{array}{}
H =& -t \sum\limits_{k,k^{\prime}} \Big[ \delta_{k_x,k_x^{\prime}} \big( \delta_{k_y-k_y^{\prime},\frac{\pi \alpha}{a}} e^{-ik_xa} + \delta_{k_y-k_y^{\prime},-\frac{\pi \alpha}{a}} e^{ik_xa} \big)
+ \delta_{k_y,k_y^{\prime}} \big( \delta_{k_x-k_x^{\prime},-\frac{\pi \alpha}{a}} e^{-ik_ya} + \delta_{k_x-k_x^{\prime},\frac{\pi \alpha}{a}} e^{ik_ya} \big) \Big] a^{\dagger}_k a_{k^{\prime}} \\
&+ \frac{U}{2N^2} \sum\limits_{q,k,k^{\prime}} a^{\dagger}_{k+q} a_k a^{\dagger}_{k^{\prime}-q} a_{k^{\prime}}
\end{array}
$$

$$
\begin{array}{}
H|\Psi \rangle 
&= -t \sum\limits_{k_1,k_2}\Big\{  \\
&+ e^{-ik_{1x}a} f(k_{1x},k_{1y}-\pi \alpha/a,k_2) 
+ e^{ik_{1x}a} f(k_{1x},k_{1y}+\pi \alpha/a,k_2) \\
&+ e^{-ik_{2x}a} f(k_1,k_{2x},k_{2y}-\pi \alpha/a)
+ e^{ik_{2x}a} f(k_1,k_{2x},k_{2y}+\pi \alpha/a) \\
&+ e^{-ik_{1y}a} f(k_{1x}+\pi \alpha/a,k_{1y},k_2) 
+ e^{ik_{1y}a} f(k_{1x}-\pi \alpha/a,k_{1y},k_2) \\
&+ e^{-ik_{2y}a} f(k_1,k_{2x}+\pi \alpha/a,k_{2y})
+ e^{ik_{2y}a} f(k_1,k_{2x}-\pi \alpha/a,k_{2y})
\Big\} |k_1,k_2 \rangle \\
&+ U \sum\limits_{k_1,k_2} f(k_1,k_2) |k_1,k_2 \rangle + \frac{U}{2N^2} \sum\limits_{q,k_1,k_2} \big[ f(k_1+q,k_2-q) + f(k_1-q,k_2+q) \big] |k_1,k_2 \rangle \\
&=E \sum\limits_{k_1,k_2} f(k_1,k_2) |k_1,k_2 \rangle
\end{array}
$$



##### Mean-field approach









[1] Titus Neupert et al., Fractional Quantum Hall States at Zero Magnetic Field.

[2] A. S. Sorensen, E. Demler, and M. D. Lukin, Phys. Rev. Lett. 94, 086803 (2005).

[3] M. Hafezi, A. S. Sorensen, E. Demler, and M. D. Lukin, Phys. Rev. A 76, 023613 (2007).