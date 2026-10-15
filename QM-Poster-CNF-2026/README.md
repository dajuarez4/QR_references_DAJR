Numerical Procedure: Real-Gas Models and Quarkyonic Matter

This work investigates the nuclear liquid-gas critical point and the equation of state (EoS) of quarkyonic matter using five real-gas models. The nucleonic sector is modeled with the van der Waals excluded-volume prescription and different attractive mean-field potentials.

1. Real-Gas Models and Excluded Volume

The available-volume fraction for the van der Waals prescription is

$$
f_{\mathrm{EV}}(n)=1-bn,
$$

where $b$ describes short-range repulsion. The five attractive mean-field potentials are:

|Model                    |Attractive potential $u(n)$                                                          |
|-------------------------|-------------------------------------------------------------------------------------|
|van der Waals (vdW)      |$u(n)=-an$                                                                           |
|Redlich–Kwong–Soave (RKS)|$u(n)=-\frac{a}{b}\ln(1+bn)$                                                         |
|Peng–Robinson (PR)       |$u(n)=-\frac{a}{2\sqrt{2}b}\ln\left(\frac{1+(1+\sqrt{2})bn}{1+(1-\sqrt{2})bn}\right)$|
|Clausius                 |$u(n)=-\frac{an}{1+cn}$                                                              |
|Dieterici                |$u(n)=-\frac{an^{\alpha-1}}{\alpha-1}$                                               |

Here, $a$ controls attraction, and $c$ and $\alpha$ are additional parameters in the Clausius and Dieterici models. The classical pressure is

$$
P(T,n)=\frac{nT}{1-bn}+n^2\frac{du(n)}{dn}.
$$

The models allow comparison of how different attractive interactions affect the nuclear incompressibility and liquid-gas critical point [1, 2, 5].

2. Symmetric Nuclear Matter: Saturation Fit

The parameters $a$ and $b$ are calibrated using the symmetric nuclear-matter saturation conditions:

$$
n_0=0.16\ \mathrm{fm}^{-3},\qquad P(0,n_0)=0,
$$

$$
\frac{\epsilon(0,n_0)}{n_0}-m_N=-16\ \mathrm{MeV}.
$$

Numerical steps

1. Select a mean-field model and fix $c$ or $\alpha$ when applicable.
2. Choose a trial excluded-volume parameter $b$, ensuring $1-bn_0>0$.
3. Compute the effective ideal Fermi-gas density:
  $$
n^{\mathrm{id}}=\frac{n_0}{1-bn_0}.
$$
4. Compute the Fermi momentum and evaluate the ideal-gas pressure and energy density:
  $$
k_F=\left(\frac{6\pi^2 n^{\mathrm{id}}}{d}\right)^{1/3},\qquad d=4.
$$
5. Use $P(0,n_0)=0$ to determine $a$ for the selected attractive potential.
6. Adjust $b$ by bisection until the binding-energy constraint is satisfied; recompute $a$ at each trial.
7. Repeat for the five models and for the scanned values of $c$ or $\alpha$.

This fixes the nuclear interaction parameters consistently with the ground-state constraints [2, 5].

3. Quantum EoS in the Grand Canonical Ensemble

At finite temperature, the quantum EoS includes Fermi–Dirac statistics:

$$
P(T,\mu)=p^{\mathrm{id}}(T,\mu^{*})+n^2u’(n),
$$

$$
n(T,\mu)=(1-bn)n^{\mathrm{id}}(T,\mu^{*}),
$$

$$
\epsilon(T,\mu)=(1-bn)\epsilon^{\mathrm{id}}(T,\mu^{*})+nu(n).
$$

Here $\mu^{}$ is the effective chemical potential and $u’(n)=du/dn$. For each trial $(T,n)$, solve the ideal-density relation for $\mu^{}$ using an iterative root finder, then calculate $P$ and $\epsilon$. Repeat to construct the full quantum EoS [1, 2].

4. Incompressibility and Liquid-Gas Critical Point

From the calibrated EoS, calculate the nuclear incompressibility:

$$
K_0=9\left.\frac{\partial P}{\partial n}\right|_{T=0,n=n_0}.
$$

Find the critical point $(T_c,n_c)$ from the horizontal-inflection conditions:

$$
\left.\frac{\partial P}{\partial n}\right|{T_c,n_c}=0,
\qquad
\left.\frac{\partial^2P}{\partial n^2}\right|{T_c,n_c}=0.
$$

Numerical steps

1. Evaluate finite-temperature pressure isotherms over a coarse $(T,n)$ grid.
2. Estimate the critical region where both derivatives approach zero.
3. Compute density derivatives using centered finite differences.
4. Refine $T_c$ and $n_c$ with a damped nonlinear root finder.
5. Compare $K_0$, $T_c$, and $n_c$ across the five models [2, 5].

5. Quarkyonic Matter and Neutron Stars

The calibrated nucleonic EoS is used in the quarkyonic description: quarks occupy low-momentum states while confined nucleons populate a higher-momentum shell [3, 4].

1. Construct the quarkyonic energy density with the selected nucleonic model.
2. Use the regulator $\Lambda=305\ \mathrm{MeV}$, as in the poster calculation.
3. Minimize the energy density with respect to the momentum variables $k_Q$ and $k_B+\Delta$ to obtain the equilibrium EoS.
4. Compute the pressure and squared speed of sound:
  $$
P=n_B^2\frac{d}{dn_B}\left(\frac{\epsilon}{n_B}\right),
\qquad
c_s^2=\frac{dP}{d\epsilon}.
$$
5. Use the resulting EoS, joined to a BPS crust, to integrate the Tolman–Oppenheimer–Volkoff (TOV) equations and obtain neutron-star mass–radius curves [3–5].

References

1. V. Vovchenko, D. V. Anchishkin, and M. I. Gorenstein, Particle Number Fluctuations for van der Waals Equation of State (2015). https://arxiv.org/abs/1501.03785
2. V. Vovchenko, D. V. Anchishkin, and M. I. Gorenstein, Van der Waals Equation of State with Fermi Statistics for Nuclear Matter (2015). https://arxiv.org/abs/1504.01363
3. Quantum van der Waals theory meets quarkyonic matter (2023). https://arxiv.org/abs/2307.13532
4. Quantum van der Waals quarkyonic matter at nonzero isospin asymmetry (2025). https://doi.org/10.1103/PhysRevC.111.025803
5. Correlations between nuclear incompressibility, liquid-gas critical point, and quarkyonic transition (2025). https://arxiv.org/abs/2501.16225