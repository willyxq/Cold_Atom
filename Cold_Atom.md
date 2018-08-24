guiding center $X=ta_x+k_yl^2$



$\frac{\Phi}{\Phi_0} = \frac{a^2B}{h/e}=\frac{T_V}{T_B}$, where $T_V$ is the characteristic period of electrons, with momentum $h/a$, in the periodic potential, $T_B$ is the characteristic period of the cyclotron dynamics in the magnetic field.

#### Continuum limit —— weak periodic potential

​	For perpendicular magnetic field $\vec{B} = \nabla \times \vec{A}=B\hat{z}$, choose the Landau gauge $\vec{A}=(0,Bx,0)$. Then the parabolic Hamiltonian becomes:
$$
\vec{p} \rightarrow \vec{p}-\frac{q}{c}\vec{A} \\
H_0=\frac{p_x^2+p_y^2}{2m} \rightarrow H=\frac{1}{2m} \big[p_x^2+(p_y+\frac{e}{c}Bx)^2 \big] = \frac{p_x^2}{2m} + \frac{1}{2}m\omega_c^2 \Big(x+\frac{\hbar k_y}{m\omega_c} \Big)^2 = \frac{p_x^2}{2m} + \frac{1}{2}m\omega_c^2 \Big(x-X \Big)^2 \\
E_n = \hbar \omega_c (n+\frac{1}{2})
$$
where $\hbar k_y$ is the eigenvalue of operator $p_y$, guiding center $X=-k_yl^2, \ l^2=\frac{\hbar c}{eB}=\frac{\Phi_0}{2\pi B}$. Eigenstates are denoted by $|n,X \rangle$. 

​	Focus on the lowest Landau level $n=0$, eigenstates are $|X \rangle = |k_y l^2 \rangle$. Map the eigenstate on the real space:
$$
\langle \vec{r}| X \rangle = \phi_{0,X} \propto e^{ik_yy} e^{-\frac{(x-X)^2}{2l^2}} = e^{-i\frac{X}{l^2}y}  e^{-\frac{(x-X)^2}{2l^2}} \\
\langle X^{\prime}|X \rangle = \delta_{X,X^{\prime}} \int dx  e^{-\frac{(x-X)^2}{l^2}} = \delta_{X,X^{\prime}} \\
$$

$$
\begin{array}{}
\langle X^{\prime} | e^{iQx}|X \rangle &= \int d\vec{r}^{\prime} d\vec{r} \langle X^{\prime} | \vec{r}^{\prime} \rangle \langle \vec{r}^{\prime} | e^{iQx}|\vec{r} \rangle \langle \vec{r} |X \rangle \\
& = \int d\vec{r}^{\prime} d\vec{r} e^{iQx} \delta(\vec{r}-\vec{r}^{\prime}) e^{-i\frac{X}{l^2}y} e^{i\frac{X^{\prime}}{l^2}y^{\prime}} e^{-\frac{(x-X)^2}{2l^2}} e^{-\frac{(x^{\prime}-X^{\prime})^2}{2l^2}} \\
& = \int d\vec{r} e^{iQx} e^{-i\frac{(X-X^{\prime})}{l^2}y} e^{-\frac{1}{2l^2}(X^2+X^{\prime2})} e^{-\frac{1}{l^2}[x^2-(X+X^{\prime})x]} \\
&=e^{-X^2/l^2} \delta_{X,X^{\prime}} \int  e^{-\frac{1}{l^2}[x^2-(2X+iQl^2)x]} dx \\
&= e^{\frac{-Q^2l^4 + i4QXl^2}{4l^2}} \delta_{X,X^{\prime}} \int e^{-\frac{1}{l^2}[x-(X+iQl^2/2)]^2} dx \\
&=e^{-\frac{Q^2l^2}{4}} e^{iQX} \delta_{X,X^{\prime}}
\end{array}
$$

Similarly, $\langle X^{\prime} | e^{-iQx}|X \rangle = e^{-\frac{Q^2l^2}{4}} e^{-iQX} \delta_{X,X^{\prime}}$, then
$$
\langle X^{\prime} |\cos (Qx)|X \rangle = \cos(QX) e^{-Q^2l^2/4} \delta_{X,X^{\prime}}
$$
Using the same integration procedure,
$$
\langle X^{\prime} | e^{iQy}|X \rangle =\delta_{X, X^{\prime}+Ql^2} e^{-Q^2l^2/4} \\
\langle X^{\prime} | e^{-iQy}|X \rangle =\delta_{X, X^{\prime}-Ql^2} e^{-Q^2l^2/4} \\
\langle X^{\prime} | \cos(Qy)|X \rangle = \frac{1}{2} e^{-Q^2l^2/4} \big( \delta_{X, X^{\prime}+Ql^2}+ \delta_{X, X^{\prime}-Ql^2} )  \\
$$
​	Now consider, as a perturbation, a periodic potential $V(x,y) = V(x+a,y) = V(x,y+b)$:
$$
V(x,y) = V_1 \cos(\frac{2\pi}{a}x) + V_2 \cos(\frac{2\pi}{b}y)
$$
The new Schr$\ddot{o}​$dinger equation is:
$$
H = H_0 + V(\vec{r}) \\
H\psi_{k_y}(\vec{r}) = E\psi_{k_y}(\vec{r})
$$
Expand the new eigenstate in terms of the unperturbed eigenstates $\phi_{k_y}$:
$$
\psi_{k_y}(\vec{r}) = \sum\limits_{n=-\infty}^{\infty} u_{G_n} \phi_{k_y+G_n}(\vec{r})
$$
where $G_n = \frac{2\pi n}{b}$, now $k_y \in [-\frac{\pi}{b}, \frac{\pi}{b}]$. Substitute into the Schr$\ddot{o}$dinger equation and we will arrive at
$$
\frac{\hbar \omega_c }{2}u_{G_n} + \sum\limits_{n^{\prime}} u_{G_{n^{\prime}}} \int d\vec{r} V(\vec{r}) \phi_{k_y+G_{n}}^{*} \phi_{k_y+G_{n^{\prime}}} = E u_{G_n} \\
\frac{\hbar \omega_c}{2} u_n + V_1 \cos \Big[\frac{2\pi}{a} \big(k_y+\frac{2\pi n}{b} \big) l^2 \Big] e^{-\pi^2 l^2/a^2} u_n + \frac{V_2}{2} e^{-\pi^2 l^2/b^2} \big( u_{n+1} + u_{n-1} \big) = E u_n \\
\Big\{ \frac{\hbar \omega_c}{2} + V_1 \cos \Big[\frac{2\pi}{a} \big(k_y+\frac{2\pi n}{b} \big) l^2 \Big] e^{-\pi^2 l^2/a^2} \Big\} u_n + \frac{V_2}{2} e^{-\pi^2 l^2/b^2} \big( u_{n+1} + u_{n-1} \big) = E u_n
$$
If $a=b$, then $\frac{\Phi_0}{2\pi Ba^2}=\frac{l^2}{a^2}=\frac{\Phi_0}{2\pi \Phi} = \frac{1}{2\pi \alpha}$, $\alpha = \frac{\Phi}{\Phi_0}$.
$$
\Big\{ \frac{\hbar \omega_c}{2} e^{\pi/2 \alpha} + V_1 \cos \Big(\frac{a k_y}{\alpha}+ \frac{2\pi n}{\alpha} \Big) \Big\} u_n + \frac{V_2}{2}  \big( u_{n+1} + u_{n-1} \big) = E e^{\pi/2 \alpha} u_n \ \ \ \ \ \ \ \ \ (*) \\
$$

##### (i) If $\alpha=\frac{1}{4}$

Eq.(*) becomes
$$
\Big\{ \frac{\hbar \omega_c}{2}e^{2\pi} + V_1 \cos \big(4a k_y \big)  \Big\} u_n + \frac{V_2}{2}  \big( u_{n+1} + u_{n-1} \big) = E e^{2\pi}u_n
$$
It looks like exactly the same as 1D Schr$\ddot{o}$dinger equation:
$$
(2t + V)\psi_n -t \psi_{n+1} -t \psi_{n-1} = E\psi_n
$$
where $t = \frac{\hbar^2}{2m \Delta^2}$.

In terms of transfer matrix
$$
\begin{pmatrix}
u_{n+1} \\
u_n
\end{pmatrix}
=
\begin{pmatrix}
\frac{2}{V_2} \big[E-\frac{\hbar \omega_c}{2}-V_1 \cos(4ak_y) \big] & -1 \\
1 & 0
\end{pmatrix}
\begin{pmatrix}
u_{n} \\
u_{n-1}
\end{pmatrix}
$$

##### (ii) If $\alpha=4$ 

Eq.(*) becomes
$$
\Big\{ \frac{\hbar \omega_c}{2} e^{\pi/8} + V_1 \cos \Big(\frac{a k_y}{4}+ \frac{2\pi n}{4} \Big) \Big\} u_n + \frac{V_2}{2}  \big( u_{n+1} + u_{n-1} \big) = E e^{\pi/8} u_n
$$
It is recursive for every four integers $n$. We only need to solve it for $n=0,1,2,3$. The 1D Hamiltonian is:
$$
H(k_y) = \frac{\hbar \omega_c}{2}e^{\pi/8} +
\begin{pmatrix}
 V_1 \cos \big(\frac{ak_y}{4} \big) & \frac{V_2}{2} & 0 & \frac{V_2}{2} \\
\frac{V_2}{2} & V_1 \cos \big(\frac{ak_y}{4}+\frac{\pi}{2} \big) &  \frac{V_2}{2} & 0 \\
0 &  \frac{V_2}{2} &  V_1 \cos \big(\frac{ak_y}{4}+\pi \big) &  \frac{V_2}{2} \\
\frac{V_2}{2} & 0  & \frac{V_2}{2} & V_1 \cos \big(\frac{ak_y}{4}+\frac{3\pi}{2} \big)
\end{pmatrix}
$$
<img src="/Users/jihangzhu/Library/Mobile Documents/com~apple~CloudDocs/Typora/Research/Cold_Atom/fig3.pdf" style="zoom:100%" />



#### Tight-binding limit —— strong periodic potential

Start with the tight-binding Hamiltonian,
$$
H_0 = -t\sum\limits_{m,n} (a_{m+1,n}^{\dagger}a_{m,n} + a_{m,n+1}^{\dagger}a_{m,n} + \text{h.c.} )
$$
Consider magnetic field $\vec{B}=B\hat{z}$, and gauge $\vec{A} = (0,Bx,0)$. Then the hopping term achieve a phase, called Peierls phase,
$$
H = -t\sum\limits_{m,n} (a_{m+1,n}^{\dagger}a_{m,n} + e^{i\phi^y_{m,n}}a_{m,n+1}^{\dagger}a_{m,n} + \text{h.c.} )
$$
and $\phi_{m,n}=-\frac{e}{\hbar}\int \vec{A} \cdot d\vec{r}$.
$$
\phi_{m,n}^y = -\frac{e}{\hbar} Bx\delta y = -\frac{e}{\hbar}Bmab = -2\pi m\frac{\Phi}{\Phi_0} = -2\pi m \alpha
$$
no change in $x$-hopping, but $t_y$ gets a phase,
$$
t_x = t \\
t_y = te^{-i \frac{\pi}{2} 4m\alpha} = t (-i)^{4m\alpha}
$$
<img src="/Users/jihangzhu/Library/Mobile Documents/com~apple~CloudDocs/Typora/Research/Cold_Atom/fig2.png" style="zoom:40%" />

Assume $a=b$ and act the Hamiltonian on the simultaneous eigenstates $\Psi_{m,n} = e^{ik_xma}e^{ik_yna}u_{m,n}$, where $u_{m,n} = a^{\dagger}_{m,n}|0\rangle$ is the single-particle state.
$$
H\Psi_{m,n} = E\Psi_{m,n} \\
-t \Big( e^{ik_x a} u_{m+1,n} + e^{-im2\pi \alpha}e^{ik_yb}u_{m,n+1}+e^{-ik_xa}u_{m-1,n}+e^{im2\pi a}e^{-ik_yb}u_{m,n-1} \Big) = E u_{m,n}
$$


##### (i) If $\alpha=\frac{1}{4}$

The periodic function $u_{m+4,n} = u_{m,n} = u_{m,n+1}$
$$
-t \Big( e^{ik_x a}u_{m+1,n}+e^{-i\frac{\pi}{2}m}e^{ik_yb}u_{m,n+1}+e^{-ik_xa}u_{m-1,n} + e^{i\frac{\pi}{2}m}e^{-ik_yb}u_{m,n-1} \Big) = Eu_{m,n}
$$
We can ignore the subscript $n$ because $u_{m,n+1}=u_{m,n}$,
$$
-t\Big(e^{ik_xa}u_{m+1} + e^{-ik_xa} u_{m-1} + 2\cos(k_yb-\frac{\pi}{2}m)u_m \Big) = E u_m
$$

$$
H(\vec{k}) = -t
\begin{pmatrix}
h_0(k_y) & e^{ik_xa} & 0 & e^{-ik_xa} \\
e^{-ik_xa} & h_1(k_y) & e^{ik_xa} & 0 \\
0 & e^{-ik_xa} & h_2(k_y) & e^{ik_xa} \\
e^{ik_xa} & 0 &e^{-ik_xa} & h_3(k_y) 
\end{pmatrix}
= -t
\begin{pmatrix}
h_0(k_y) & 1 & 0 & 1 \\
1 & h_1(k_y) & 1 & 0 \\
0 & 1 & h_2(k_y) & 1 \\
1 & 0 & 1 & h_3(k_y) 
\end{pmatrix}
$$

where $h_m(k_y)=2\cos(k_yb-\frac{\pi}{2}m)$, $m=0,1,2,3$.

<img src="/Users/jihangzhu/Library/Mobile Documents/com~apple~CloudDocs/Typora/Research/Cold_Atom/fig4.pdf" style="zoom:100%" />

<img src="/Users/jihangzhu/Library/Mobile Documents/com~apple~CloudDocs/Typora/Research/Cold_Atom/fig5.pdf" style="zoom:150%" />

<img src="/Users/jihangzhu/Library/Mobile Documents/com~apple~CloudDocs/Typora/Research/Cold_Atom/fig6.pdf" style="zoom:150%" />

<img src="/Users/jihangzhu/Library/Mobile Documents/com~apple~CloudDocs/Typora/Research/Cold_Atom/fig7.pdf" style="zoom:150%" />



##### (ii) If $\alpha=4$

The Peierls phase is zero and $H=H_0$,

Then the eigenvalue is
$$
E(\vec{k}) = 2t \Big(\cos(k_xa) + \cos(k_yb) \Big)
$$



##### (iii) if $\alpha=\frac{1}{8}$

$$
H(\vec{k}) = t
\begin{pmatrix}
h_0(k_y) & e^{ik_xa} & 0 & 0 & \cdots & e^{-ik_xa} \\
e^{-ik_xa} & h_1(k_y) & e^{ik_xa}& 0 & \cdots & 0 \\
0 & e^{-ik_xa} & h_2(k_y) & e^{ik_xa}& \cdots & 0 \\
\vdots & \\
e^{ik_xa} & 0 & \cdots & 0 &e^{-ik_xa} & h_7(k_y) 
\end{pmatrix}
$$

where $h_m(k_y)=2\cos(k_yb-\frac{\pi}{4}m)$, $m=0,1,2,\cdots,7$

np.

#### Analytical solve TB limit with $\alpha=\frac{1}{4}$

​	Using Mathematica, the eigenvalues and eigenstates of the Hamiltonian
$$
H = 
\begin{pmatrix}
2\cos(k_yb) & 1 & 0 & 1 \\
1 & 2\cos(k_yb-\frac{\pi}{2}) & 1 & 0 \\
0 & 1 & 2\cos(k_yb-\pi)  & 1 \\
1 & 0 & 1 & 2\cos(k_yb-\frac{3\pi}{2}) 
\end{pmatrix}
$$
are:
$$
E = 
\begin{pmatrix}
-\varepsilon_- & \varepsilon_- & -\varepsilon_+ & \varepsilon_+
\end{pmatrix} \\
$$

$$
u_1 = 
\begin{pmatrix}
-\frac{\varepsilon_-^2-2\big( \cos(k_yb)+\sin(k_yb) \big)\varepsilon_-+4\cos(k_yb)\sin(k_yb)}{2\varepsilon_-} \\
-1-\frac{\big[\varepsilon_--2\cos(k_yb)\big] \big[ -\varepsilon_-^2+2 \big(\sin(k_yb)-\cos(k_yb)\big)\varepsilon_- + 4\cos(k_yb)\sin(k_yb) \big]}{2\varepsilon_-} \\
\frac{-\varepsilon_-^2+2\big( \sin(k_yb)-\cos(k_yb) \big)\varepsilon_-+4\cos(k_yb)\sin(k_yb)}{2\varepsilon_-}  \\
1 
\end{pmatrix}
=
\begin{pmatrix}
-\frac{(\varepsilon_--2c) (\varepsilon_--2s)}{2 \varepsilon_-} \\
-1+\frac{(\varepsilon_--2c)(\varepsilon_-+2c)(\varepsilon_--2s)}{2\varepsilon_-} \\
-\frac{(\varepsilon_-+2c)(\varepsilon_--2s)}{2\varepsilon_-} \\
1
\end{pmatrix}
$$

$$
u_2=
\begin{pmatrix}
-\frac{-\varepsilon_-^2-2\big( \cos(k_yb)+\sin(k_yb) \big)\varepsilon_--4\cos(k_yb)\sin(k_yb)}{2\varepsilon_-} \\
-1+\frac{\big[-\varepsilon_- -2\cos(k_yb)\big] \big[ -\varepsilon_-^2-2 \big(\sin(k_yb)-\cos(k_yb)\big)\varepsilon_- + 4\cos(k_yb)\sin(k_yb) \big]}{2\varepsilon_-} \\
-\frac{-\varepsilon_-^2-2\big( \sin(k_yb)-\cos(k_yb) \big)\varepsilon_-+4\cos(k_yb)\sin(k_yb)}{2\varepsilon_-} \\
1
\end{pmatrix}
=
\begin{pmatrix}
\frac{(\varepsilon_-+2c) (\varepsilon_-+2s)}{2 \varepsilon_-} \\
-1+\frac{(\varepsilon_--2c)(\varepsilon_-+2c)(\varepsilon_-+2s)}{2\varepsilon_-} \\
\frac{(\varepsilon_--2c)(\varepsilon_-+2s)}{2\varepsilon_-} \\
1
\end{pmatrix}
$$

$$
u_3=
\begin{pmatrix}
-\frac{\varepsilon_+^2-2\big( \cos(k_yb)+\sin(k_yb) \big)\varepsilon_++4\cos(k_yb)\sin(k_yb)}{2\varepsilon_+} \\
-1-\frac{\big[\varepsilon_+-2\cos(k_yb)\big] \big[ -\varepsilon_+^2+2 \big(\sin(k_yb)-\cos(k_yb)\big)\varepsilon_+ + 4\cos(k_yb)\sin(k_yb) \big]}{2\varepsilon_+} \\
\frac{-\varepsilon_+^2+2\big( \sin(k_yb)-\cos(k_yb) \big)\varepsilon_++4\cos(k_yb)\sin(k_yb)}{2\varepsilon_+} \\
1
\end{pmatrix}
=
\begin{pmatrix}
-\frac{(\varepsilon_+-2c) (\varepsilon_+-2s)}{2 \varepsilon_+} \\
-1+\frac{(\varepsilon_+-2c)(\varepsilon_++2c)(\varepsilon_+-2s)}{2\varepsilon_+} \\
-\frac{(\varepsilon_++2c)(\varepsilon_+-2s)}{2\varepsilon_+} \\
1
\end{pmatrix}
$$

$$
u_4 = 
\begin{pmatrix}
-\frac{-\varepsilon_+^2-2\big( \cos(k_yb)+\sin(k_yb) \big)\varepsilon_+-4\cos(k_yb)\sin(k_yb)}{2\varepsilon_+} \\
-1+\frac{\big[-\varepsilon_+-2\cos(k_yb)\big] \big[ -\varepsilon_+^2-2 \big(\sin(k_yb)-\cos(k_yb)\big)\varepsilon_+ + 4\cos(k_yb)\sin(k_yb) \big]}{2\varepsilon_+} \\
-\frac{-\varepsilon_+^2-2\big( \sin(k_yb)-\cos(k_yb) \big)\varepsilon_++4\cos(k_yb)\sin(k_yb)}{2\varepsilon_+} \\
1
\end{pmatrix}
=
\begin{pmatrix}
\frac{(\varepsilon_++2c) (\varepsilon_++2s)}{2 \varepsilon_+} \\
-1+\frac{(\varepsilon_+-2c)(\varepsilon_++2c)(\varepsilon_++2s)}{2\varepsilon_+} \\
\frac{(\varepsilon_+-2c)(\varepsilon_++2s)}{2\varepsilon_+} \\
1
\end{pmatrix}
$$

where $\varepsilon_{\pm}=\sqrt{4 \pm \sqrt{2(7+\cos(4k_yb))}},\ \ c=\cos(k_yb),\ \ s = \sin(k_yb)$

​	Focus on the lowest band, $E=-\varepsilon_+$ and Fourier transform the corresponding eigenvector to Wannier function. 
$$
\begin{array}{}
W^{\alpha}_Y(y) &= \frac{1}{N} \sum\limits_{k_y} e^{-ik_yY} \psi_{k_y}^{\alpha}(y) \\
&=\frac{1}{N} \sum\limits_{k_y} e^{ik_y(y-Y)} u_{k_y}^{\alpha} \\
\end{array}
$$
where Bloch wave function $\psi_{k_y}(y) = e^{ik_yy}u_{k_y}$, $Y$ is any lattice vector. $\alpha=1,2,3,4$ labels 4 components of the eigenvector. Change the label $k_y$ to $n$:
$$
W^{\alpha}(\Delta y) = \frac{1}{N} \sum\limits_{n=0}^{N-1} e^{i\frac{2\pi n}{Nb}\Delta y} u_n^{\alpha}
$$
$\Delta y = y-Y$ is the distance to each lattice. 4 components and their sum of Wannier function are shown below:

<img src="/Users/jihangzhu/Library/Mobile Documents/com~apple~CloudDocs/Typora/Research/Cold_Atom/fig8.pdf" style="zoom:100%" />





#### Interaction matrix element

The Hamiltonian of the 2DEG subjected to a transverse magnetic field is[1]:
$$
H = \sum\limits_{n,X} \varepsilon_n c_{n,X}^{\dagger} c_{n,X}+\frac{1}{2S} \sum\limits_{\vec{q}} \sum\limits_{n_1,X_1, \dots, n_4,X_4} V(\vec{q}) \langle n_1,X_1|e^{i\vec{q}\cdot r} |n_4,X_4 \rangle  \langle n_2,X_2|e^{-i\vec{q}\cdot r} |n_3,X_3 \rangle c_{n_1,X_1}^{\dagger} c_{n_2,X_2}^{\dagger} c_{n_3,X_3} c_{n_4,X_4}
$$
For the lowest Landau level,
$$
\begin{array}{}
H &= \sum\limits_{X} \varepsilon_0 c_{X}^\dagger c_X + \frac{1}{2S} \sum\limits_{X_1,X_2,X_1^\prime,X_2^\prime} \langle X_1^\prime X_2^\prime |V(\vec{r}_1-\vec{r}_2)|X_1X_2 \rangle c_{X_1^\prime}^\dagger c_{X_2^\prime}^\dagger c_{X_1} c_{X_2} \\
&= \sum\limits_{X} \varepsilon_0 c_{X}^\dagger c_X + \frac{1}{2S} \sum\limits_{\vec{q}} \sum\limits_{X_1,X_2,X_1^\prime,X_2^\prime} V(\vec{q}) \langle X_1^\prime X_2^\prime |e^{i\vec{q} \cdot (\vec{r}_1 - \vec{r}_2)}|X_1X_2 \rangle c_{X_1^\prime}^\dagger c_{X_2^\prime}^\dagger c_{X_1} c_{X_2} \\
&=  \sum\limits_{X} \varepsilon_0 c_{X}^\dagger c_X + \frac{1}{2S} \sum\limits_{\vec{q}} \sum\limits_{X_1,X_2,X_1^\prime,X_2^\prime} V(\vec{q}) \langle X_1^\prime|e^{i\vec{q}\cdot \vec{r}_1}|X_1 \rangle \langle X_2^\prime|e^{-i\vec{q}\cdot \vec{r}_2}|X_2 \rangle c_{X_1^\prime}^\dagger c_{X_2^\prime}^\dagger c_{X_1} c_{X_2}
\end{array}
$$
We can easily prove that
$$
\begin{array}{}
\langle X^{\prime} |e^{i\vec{q}\cdot\vec{r}} | X \rangle &= \int d\vec{r}^{\prime} d\vec{r} e^{i\vec{q}\cdot \vec{r}} \delta(\vec{r}^{\prime}-\vec{r}) e^{i\frac{X^{\prime}}{l^2}y^{\prime}}e^{-\frac{(x^\prime-X^\prime)^2}{2l^2}} e^{-i\frac{X}{l^2}y}e^{-\frac{(x-X)^2}{2l^2}} \\
&= \int d\vec{r} e^{iq_xx} e^{iq_yy} e^{i\frac{X^\prime-X}{l^2}y} e^{-\frac{1}{2l^2}[(x-X^\prime)^2+(x-X)^2]} \\
&= \int dx dy e^{iq_xx}  e^{i \big(\frac{X^\prime-X}{l^2}+q_y \big)y} e^{-\frac{1}{2l^2}[(x-X^\prime)^2+(x-X)^2]} \\
&= \int dx \delta_{X^\prime,X-l^2q_y} e^{iq_xx} e^{-\frac{1}{2l^2}[(x-X^\prime)^2+(x-X)^2]} \\
&= \delta_{X^\prime,X-l^2q_y} e^{-l^2|q|^2/4} e^{iq_xX} e^{-il^2q_xq_y/2} \\
\langle X^{\prime} |e^{-i\vec{q}\cdot\vec{r}} | X \rangle &=  \delta_{X^\prime,X+l^2q_y} e^{-l^2|q|^2/4} e^{-iq_xX} e^{-il^2q_xq_y/2}
\end{array}
$$
Then 
$$
\begin{array}{}
\langle X_1^{\prime} X_2^{\prime} | V(\vec{r}_1-\vec{r}_2)| X_1 X_2 \rangle &= \sum\limits_{\vec{q}}V(\vec{q}) \langle X_1^{\prime} |e^{i\vec{q}\cdot \vec{r}_1} |X_1 \rangle \langle X_2^{\prime} |e^{-i\vec{q}\cdot \vec{r}_2} |X_2 \rangle \\
&= \sum\limits_{\vec{q}}V(\vec{q}) \delta_{X_1^\prime,X_1-l^2q_y} \delta_{X_2^\prime,X_2+l^2q_y} e^{-l^2|q|^2/2} e^{iq_x(X_1-X_2)} e^{-il^2q_xq_y}
\end{array}
$$

$$
\langle X_1-l^2q_y, X_2+l^2q_y | V(\vec{r}_1-\vec{r}_2) |X_1,X_2 \rangle = \sum\limits_{\vec{q}}V(\vec{q}) e^{-l^2|q|^2/2} e^{iq_x(X_1-X_2-l^2q_y)} \\
\Rightarrow V(\vec{q}) e^{-l^2|q|^2/2} = \sum\limits_{X_1-X_2} \langle X_1-l^2q_y, X_2+l^2q_y | V(\vec{r}_1-\vec{r}_2) |X_1,X_2 \rangle e^{-iq_x(X_1-X_2-l^2q_y)}
$$



#### Wannier function

$$
|k_x,k_y \rangle = \sum\limits_{n,t}e^{ik_x(n+tp)a}z_n(k_x,k_y) |n,t \rangle, \ \ \ n=0,1,\cdots,p-1 \\
\langle n,t |k_x,k_y \rangle = e^{ik_x(n+tp)a}z_n(k_x,k_y) 
$$

where $\langle x|n,t\rangle=\delta \big(x-(n+tp)a \big)$, $z \big((n+tp)a,k_x,k_y \big) = z\big( na,k_x,k_y \big) =z_n(k_x,k_y)$.
$$
\begin{array}{}
a_x &= -i \langle k_x,k_y|\partial_{k_x}| k_x,k_y \rangle \\
&= -i \sum\limits_{n} z_n^*(k_x,k_y) \frac{\partial z_n(k_x,k_y)}{\partial k_x} \\
a_y &= 0
\end{array}
$$
The maximally localized Wannier function is:
$$
|W(x,k_y) \rangle = \frac{1}{\sqrt{L_x}} \sum\limits_{k_x} e^{-i \int_0^{k_x}a_x(p_x,k_y)dp_x}e^{-ik_x[x-\theta(k_y)/2\pi]} |k_x,k_y \rangle
$$
where $\theta(k_y) = \int_0^{2\pi}a_x(p_x,k_y)dp_x$, $x \in Z$.
$$
\langle n,t |W(x,k_y) \rangle = \frac{1}{\sqrt{L_x}} \sum\limits_{k_x} e^{-i \int_0^{k_x}a_x(p_x,k_y)dp_x}e^{-ik_x[x-\theta(k_y)/2\pi]} e^{ik_x(n+tp)a}z_n(k_x,k_y)
$$

#### Wannier Function

Fourier transform the basis in real space to the momentum space:
$$
\phi_k^{\alpha}(r) = \frac{1}{\sqrt{N}} \sum\limits_{R_i} e^{ik(R_i+d_{\alpha})} \phi_{R_i+d_{\alpha}}(r)
$$
where $R_i$ denote the position of the $i$th unit cell, $N$ is the number of unit cells, $\alpha$ labels the lattices/orbitals/atoms in one unit cell, $d_{\alpha}$ is the position of the $\alpha$ orbital with respect to $R_i$. Here we only focus on one band, so the band index is ignored.

Then the Bloch eigenstate is:
$$
\psi_k(r) = \sum\limits_{\alpha} C^{\alpha}(k)\phi_{k}^{\alpha}(r)
$$
The Wannier function is:
$$
\begin{array}{}
W_{R}(r) &= \frac{1}{\sqrt{N}} \sum\limits_{k} e^{-ikR} \psi_k(r) \\
\end{array}\\
\begin{array}{}
W(r-R) &=\frac{1}{N} \sum\limits_{k,\alpha,R_i} e^{-ikR} C^{\alpha}(k) e^{ik(R_i+d_{\alpha})} \phi_{R_i+d_{\alpha}}(r) \\
&= \frac{1}{N} \sum\limits_{k,\alpha,R_i} e^{ik(R_i+d_{\alpha}-R)} C^{\alpha}(k) \delta(r-R_i-d_{\alpha}) \\
\end{array} 
$$

$$
\Rightarrow 
W(x) =\frac{1}{N} \sum\limits_k e^{ikx} C^{\alpha}(k) \delta(\alpha-x\%p)
$$

$$
|W_R \rangle = \frac{1}{\sqrt{N}} \sum\limits_k e^{-ikR} |\psi_k \rangle \\
|W_{R-\theta(k_y)/2\pi} \rangle = \frac{1}{\sqrt{N}} \sum\limits_{k_x} e^{-i\int_0^{k_x}a_x(p_x,k_y)dp_x} \cdot e^{-ik_x [R-\theta(k_y)/2\pi]} |\psi_k \rangle
$$

term $e^{-i\int_0^{k_x}a_x(p_x,k_y)dp_x}$ is to make sure the summation part is periodic for $k_x \rightarrow k_x+2\pi$. $R \in Z$ labels lattice sites and $-\frac{\theta(k_y)}{2\pi} = \bar{x} = \frac{i}{2\pi} \int_{BZ} \langle u_k | \partial_k |u_k \rangle dk$  is the charge polarization[3,4] (Wannier function center when $R=0$, that is the shift of the Wannier function away from the lattice site.)
$$
\begin{array}{}
W_{R-\theta(k_y)/2\pi}(r) &= \frac{1}{N} \sum\limits_{k_x,\alpha,R_i} e^{-i\int_0^{k_x}a_x(p_x,k_y)dp_x} \cdot e^{-ik_x [R-\theta(k_y)/2\pi]} C^{\alpha}(k) e^{ik_x (R_i+d_{\alpha}) } \phi_{R_i+d_{\alpha}}(r) \\
&= \frac{1}{N} \sum\limits_{k_x}  e^{-i\int_0^{k_x}a_x(p_x,k_y)dp_x} \cdot e^{ik_x [r-R+\theta(k_y)/2\pi]} C^{\alpha}(k) \delta(\alpha-r\%p)
\end{array}
$$
$r \in Z$ only take lattice site values. The Wannier function above is centered at $R-\theta(k_y)/2\pi$.



##### Numerically choose gauge $a_y=0$

$$
\begin{array}{}
a_y &= -i \langle u_j| \partial_{k_y} |u_j \rangle \\
&=-i\langle u_j | \frac{|u_{j+1}\rangle - |u_j \rangle}{\Delta k_y} \\
&=-\frac{i}{\Delta k_y}\Big( \langle u_j | u_{j+1} \rangle -1 \Big) = 0
\end{array} \\
\Rightarrow \langle u_j|u_{j+1} \rangle = 1 \ \ \ \ \ \ \ \ \ \ \ \text{for each step $j$}
$$

where $j$ labels $k_y$, and since $k_x$ is fixed we just ignore the index of $k_x$. That is choose the gauge:
$$
\Rightarrow |u_{j+1} \rangle = \frac{ |u_{j+1} \rangle }{ \big| \langle u_j|u_{j+1} \rangle \big| }
$$


#### Xiaoliang Qi's paper

##### Discrete geometric phase	

The phase difference $\Delta \varphi_{12}$ between two eigenstates at two different parameter points is[2]:
$$
e^{-i\Delta \varphi_{12}} = \frac{\langle \psi_1|\psi_2 \rangle}{|\langle \psi_1|\psi_2 \rangle|} \\
\Delta \varphi_{12} = -\text{Im} \log(\langle \psi_1|\psi_2 \rangle)
$$
For a finite number of parameter points, the total phase difference of a chosen path is:
$$
\begin{array}{}
\Delta \varphi_{14} &= \Delta \varphi_{12} + \Delta \varphi_{23} + \Delta \varphi_{34} \\
&=-\text{Im}\log ( \langle\psi_1|\psi_2 \rangle \langle\psi_2|\psi_3 \rangle \langle\psi_3|\psi_4 \rangle )
\end{array}
$$
$\Delta \varphi_{14}$ only depends the gauges of the first and last points, the gauge phases of intermediate points are cancelled out. We can see that the phase difference of a closed path is gauge-invariant.
$$
\Delta \varphi_{12} + \Delta \varphi_{23} + \Delta \varphi_{34}+ \Delta \varphi_{41} = -\text{Im}\log ( \langle\psi_1|\psi_2 \rangle \langle\psi_2|\psi_3 \rangle \langle\psi_3|\psi_4 \rangle  \langle\psi_4|\psi_1 \rangle )
$$

##### Berry's phase

​	Consider the continuum Berry's phase, the phase difference between any two contiguous points:
$$
e^{-i\Delta \varphi} = \frac{\langle \psi(k)|\psi(k+\Delta k) \rangle}{ |\langle \psi(k)|\psi(k+\Delta k) \rangle| }
$$
Assume that the gauge is so chosen that the phase varies in a differentiable way along the path, then to the first order $|\psi(k+\Delta k) \rangle \approx |\psi(k) \rangle +  \Delta k \ \partial_k |\psi(k) \rangle$,
$$
\langle \psi(k) | \psi(k+\Delta k) \rangle \approx 1 + \Delta k \ \lang \psi(k) | \partial_k | \psi(k) \rang \\
\Delta \varphi = -\text{Im}\log(1+\Delta k \ \lang \psi(k)|\partial_k|\psi(k) \rang)
$$
To the leading order in $\Delta k$, $ \log \big(1+\Delta k \lang \psi(k)|\partial_k| \psi(k)\rang \big) \approx \Delta k \lang \psi(k)|\partial_k| \psi(k)\rang$,
$$
\Delta \varphi = -\text{Im} \lang \psi(k)|\partial_k|\psi(k) \rang \Delta k \\
-i\Delta \varphi = \lang \psi(k)|\partial_k|\psi(k) \rang \Delta k
$$






The phase difference $\theta$ of a closed loop is $\theta(k_y) = \int_0^{2\pi}a_x(p_x,k_y)dp_x$, where $a_x = -i\langle k_x,k_y|\partial_{k_x}|k_x,k_y \rangle$, and $\langle \vec{r}|k_x,k_y \rangle$ is the periodic wavefunction instead of Bloch wavefunction.



#### Interactions

$$
H = \sum\limits_i \sum\limits_{\alpha, \beta} h_{\alpha \beta} |i \alpha \rangle \langle i \beta|
$$






















#### 2D Square Lattice

​	In the presence of a magnetic field, $\varphi \rightarrow e^{i\phi}\varphi = e^{-i\frac{e}{\hbar}\vec{A}\cdot \vec{r}} \varphi$  because of the Peierls phase. And the hopping:
$$
\langle \vec{R}^{\prime} | t | \vec{R} \rangle \rightarrow e^{-i \frac{2\pi}{\Phi_0}\vec{A} \cdot (\vec{R}-\vec{R}^{\prime})} \langle \vec{R}^{\prime} | t | \vec{R} \rangle
$$
Choose the Landau gauge $\vec{A} = (0,Bx,0)$, then the Hamiltonian becomes:
$$
H = -t\sum\limits_{m,n} (a^{\dagger}_{m+1,n}a_{m,n} + e^{i\phi_{m,n}^y} a^{\dagger}_{m,n+1}a_{m,n} + \text{h.c.} )
$$
no change in $x$-hopping, but $y$-hopping changes from $t \rightarrow te^{i\phi_{m,n}^y } = t e^{-i\frac{\Phi}{\Phi_0}2\pi m}$, where $\Phi = Ba^2$.

​	Take the quarter flux for example, $\frac{\Phi}{\Phi_0} = \frac{1}{4}$,
$$
t_x = t \\
t_y = te^{-i \frac{\pi}{2} m} = t (-i)^m
$$
<img src="/Users/jihangzhu/Library/Mobile Documents/com~apple~CloudDocs/Typora/Research/Cold_Atom/fig2.png" style="zoom:40%" />

Substitute into the Hamiltonian and act the Hamiltonian on the simultaneous eigenstates $\Psi_{m,n} = e^{ik_xma}e^{ik_yna}\psi_{m,n}$, where periodic function $\psi_{m+4,n} = \psi_{m,n} = \psi_{m,n+1}$:
$$
H\Psi_{m,n} = E\Psi_{m,n} \\
\Rightarrow -t\Big[ \big( (-i)^me^{ik_ya}+i^m e^{-ik_ya} \big)\psi_m + e^{ik_xa}\psi_{m+1} + e^{-ik_xa}\psi_{m-1} \Big] = E\psi_{m}  \\
\Rightarrow -t\Big[ h_m\psi_m + e^{ik_xa}\psi_{m+1} + e^{-ik_xa}\psi_{m-1} \Big] = E\psi_{m}
$$

$$
H(\vec{k}) = -t
\begin{pmatrix}
h_0(k_y) & e^{ik_xa} & 0 & e^{-ik_xa} \\
e^{-ik_xa} & h_1(k_y) & e^{ik_xa} & 0 \\
0 & e^{-ik_xa} & h_2(k_y) & e^{ik_xa} \\
e^{ik_xa} & 0 &e^{-ik_xa} & h_3(k_y) 
\end{pmatrix}
$$

The diagonal term $h_m(k_y) = (-i)^m e^{ik_ya} + i^m e^{-ik_ya} = e^{i(k_ya-\frac{\pi}{2}m)} + e^{-i(k_ya-\frac{\pi}{2}m)} = 2\cos(k_ya-\frac{\pi}{2}m), m = 0,1,2,3.$







##### Magnetic Translation Operators

​	The hubbard model is a good approximation to describe particles in periodic potentials at low temperatures that all particles are in the lowest Bloch band. Ignore the on-site interactions for now, the Hamiltonian of a single electron in a 2D lattice is:
$$
H_0 = -J\sum\limits_{m,n} (a^{\dagger}_{m+1,n}a_{m,n} + a^{\dagger}_{m,n+1}a_{m,n} + \text{h.c.} )
$$
It is invariant under the translation by one lattice unit vector. The lattice translation operators $T_i^0$ commute with Hamiltonian:
$$
T_x^0 = \sum\limits_{m,n} a^{\dagger}_{m+1,n}a_{m,n}\\
T_{y}^0 =  \sum\limits_{m,n} a^{\dagger}_{m,n+1}a_{m,n}
$$
​	In the presence of a magnetic field, hopping in the lattice is accompanied by a phase $\phi_{m,n} = -\frac{e}{\hbar} \vec{A}_{m,n} \cdot \vec{r} \Rightarrow \phi_{m,n}^i=-\frac{e}{\hbar} A_{m,n}^ia = -\frac{2\pi}{\Phi_0} A_{m,n}^ia$ , $i = \{x,y\}$ and magnetic flux quantum $\Phi_0 = \frac{h}{e}$. This is known as **Peierls phase**. The modified Hamiltonian is:
$$
H = -J\sum\limits_{m,n} (e^{i\phi_{m,n}^x} a^{\dagger}_{m+1,n}a_{m,n} + e^{i\phi_{m,n}^y} a^{\dagger}_{m,n+1}a_{m,n} + \text{h.c.} )
$$
The Hamiltonian is no longer invariant under the translation by one lattice unit vector because vector potential $A_{m,n}​$ is not invariant.

To recover the translation invariance, new operators are constructed:	
$$
T_x^M = \sum\limits_{m,n} e^{i\theta_{m,n}^x} a^{\dagger}_{m+1,n}a_{m,n}\\
T_{y}^M =  \sum\limits_{m,n} e^{i\theta_{m,n}^y} a^{\dagger}_{m,n+1}a_{m,n}
$$
these are called **magnetic translation operators (MTOs)**, they commute with the Hamiltonian, and 
$$
\theta_{m,n}^x = \phi_{m,n}^x + \Phi_{m,n}n\\
\theta_{m,n}^y = \phi_{m,n}^y - \Phi_{m,n}m
$$
$\Phi_{m,n}=\phi_{m,n}^x + \phi_{m+1,n}^y - \phi_{m,n+1}^x - \phi_{m,n}^y$ is the flux per unit cell.	MTOs do not necessarily commute with each other,
$$
[T_x^M,T_y^M] \psi_{i,j} = \big( e^{i(\theta_{i,j+1}^x + \theta_{i,j}^y)} - e^{i(\theta_{i,j}^x + \theta_{i+1,j}^y)} \big) \psi_{i+1,j+1}
$$
where $\psi_{i,j}=a^{\dagger}_{i,j}|0\rangle$ is the single-particle state.

​	For **homogeneous magnetic fields**, flux is a constant for each unit cell. $\Phi_{m,n}=\Phi$. Then it can be easily verified that
$$
T_x^MT_y^M = e^{i\Phi} T_y^MT_x^M
$$
MTOs commute with each other when $\Phi$ is an integer multiple of $2\pi$, then we could use the Bloch theorem: one can find simultaneous eigenstates $\Psi_{􏰁m,n}$ so that
$$
T_x^M \Psi_{m,n} = e^{ik_xa} \Psi_{m,n} \\
T_y^M \Psi_{m,n} = e^{ik_ya} \Psi_{m,n}
$$

where $a$ is the lattice constant, $m,n$ are two good quantum numbers.		
	

<img src="/Users/jihangzhu/Library/Mobile Documents/com~apple~CloudDocs/Typora/Research/Cold_Atom/fig1.png" style="zoom:30%" />

​	If $\Phi=2\pi \alpha = 2\pi \frac{p}{q}$ instead of an integer multiple of $2\pi$, commuting magnetic operators can be constructed if they enclose a super-cell on the lattice pierced by a magnetic flux equal to an integer multiple of $2π$. For a super-cell with dimension $k\times l$,
$$
(T_x^M)^k (T_y^M)^l = e^{ikl\Phi} (T_y^M)^l (T_x^M)^k
$$
The smallest possible super-cell is $kl = q$ and this is called **magnetic unit cell**. Define the new operators:
$$
M_x^k = (T_x^M)^k, \ \ M_y^l = (T_y^M)^l
$$
then
$$
M_x^k \Psi_{m,n} = e^{ik_x ka} \Psi_{m,n} \\
M_y^l \Psi_{m,n} = e^{ik_y la} \Psi_{m,n}
$$
$\Psi_{m,n}$ are simultaneous eigenstates of $M_x^k, M_y^l$ and $H$.

​			

##### Quarter Flux		

$\Phi = 2\pi \alpha$ and $\alpha=1/4$. For magnetic field $\vec{B}=B\hat{z}$, choose Landau gauge $\vec{A} = (-By,0,0) = (-Bna,0,0)$,$\phi_{m,n} = -\frac{e}{\hbar}A_{m,n}= (Bna,0,0)=(\frac{2\pi \alpha n}{a},0,0)$. ?

$\phi_{m,n} = (-2\pi \alpha n,0,0)$, and $\theta_{m,n}^x=0, \theta_{m,n}^y=-2\pi \alpha m$.
$$
H = -J\sum\limits_{m,n} (e^{-i\Phi n} a^{\dagger}_{m+1,n}a_{m,n} + a^{\dagger}_{m,n+1}a_{m,n} + \text{h.c.} )
$$
This is known as the famous **Harper-Hofstadter Hamiltonian**.

​	Let's choose a magnetic unit cell oriented along $y$ direction, then the commuting MTOs are:
$$
M_x^1 = \sum\limits_{m,n} a_{m+1,n}^{\dagger}a_{m,n} \\
M_y^4 = \sum\limits_{m,n} a_{m,n+4}^{\dagger}a_{m,n}
$$
these are equivalent to the usual lattice translation operators $T_x^0, T_y^0$ without magnetic fields. Commuting MTOs act on the simultaneous eigenstates $\Psi_{m,n}$:
$$
M_x^1 \Psi_{m,n} = e^{ik_xa} \Psi_{m,n} \\
M_y^4 \Psi_{m,n} = e^{ik_y4a} \Psi_{m,n}
$$
and $\Psi_{m,n} = e^{ik_xma}e^{ik_yna}\psi_{m,n}$, where $\psi_{m+1,n} = \psi_{m,n}= \psi_{m,n+4}$ is periodic functions.

Then
$$
H\Psi_{m,n} = -J \Big( e^{-i\Phi n}\Psi_{m+1,n}+ \Psi_{m,n+1} + e^{i\Phi n}\Psi_{m-1,n} + \Psi_{m,n-1} \Big) = E\Psi_{m,n} \\
-J\Big( e^{-i\Phi n} e^{ik_xa} \psi_{m+1,n} + e^{ik_ya}\psi_{m,n+1} + e^{i\Phi n}e^{-ik_xa}\psi_{m-1,n} + e^{-ik_ya}\psi_{m,n-1}   \Big) = E \psi_{m,n}
$$
Because of the relation $\psi_{m+1,n} = \psi_{m,n}$, we can ignore the $x$-direction index $m$ in periodic functions. Then the Schr$\ddot{o}$dinger equation becomes:
$$
-J\Big( e^{-i\Phi n} e^{ik_xa} \psi_{n} + e^{ik_ya}\psi_{n+1} + e^{i\Phi n}e^{-ik_xa}\psi_{n} + e^{-ik_ya}\psi_{n-1}   \Big) = E \psi_{n} \\
-J\Big( 2\cos(\Phi n-k_x a) \psi_{n} + e^{ik_ya}\psi_{n+1} + e^{-ik_ya}\psi_{n-1}   \Big) = E \psi_{n} 
$$

$$
H(\vec{k}) = -J
\begin{pmatrix}
2\cos(-k_xa) & e^{ik_ya} & 0 & e^{-ik_ya} \\
e^{-ik_ya} & 2\cos(\Phi-k_xa) & e^{ik_ya} & 0 \\
0 & e^{-ik_ya} & 2\cos(2\Phi-k_xa)  & e^{ik_ya} \\
e^{ik_ya} & 0 & e^{-ik_ya} & 2\cos(3\Phi-k_xa) \\
\end{pmatrix}
$$

More generally, 
$$
H(\vec{k}) = -J
\begin{pmatrix}
h_0 & e^{ik_ya} & \cdots & e^{-ik_ya} \\
e^{-ik_ya} & h_1 & \cdots & 0 \\
\vdots & \vdots &   & \vdots \\
e^{ik_ya} & 0 & e^{-ik_ya} & h_{q-1} \\
\end{pmatrix}
$$
where $h_n = 2\cos(n\Phi-k_xa)$, $\Phi = 2\pi \alpha = 2\pi \frac{p}{q}$. $q$ lattice unit cells in $y$ direction consist a minimum magnetic unit cell.

​			



[1] R. Cote, A. H. MacDonald, Collective modes of the two-dimensional Wigner crystal in a strong magnetic field. PRB 1991.

[2] Raffaele Resta, Manifestations of Berry’s phase in molecules and condensed matter.

[3] R. D. King-Smith and David Vanderbilt, Theory of polarization of crystalline solids

[4] Alexey A. Soluyanov and David Vanderbilt, Computing topological invariants without inversion symmetry 