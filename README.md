## Initial considerations

**Fundamental questions**:

- In equilibrium with gas phase O$`_2`$, Which of Pt, PtO, and PtO$`_2`$ is the most stable?
- How should we normalize the energy of the different materials?
- We need a method that includes information about the temperature and pressure of O$`_2`$. 

**Basic principles**

*Phase:* it is a homogeneous region of matter in which there is no spatial variation in average density, energy, composition, or other macroscopic properties.

At constant T and P in a single-component system, the phase that is observed is the one which has the lowest Gibbs free energy per particle, or, equivalently, the lowest chemical potential μ(T, P).

## General Theory
Grand potential of a metal oxide can be expressed as 

$$ \Omega (T,\mu_O, \mu_M) = E(N_M, N_O) - TS - \mu_O N_O - \mu_M N_M$$

Where $`E(N_M, N_O)`$ is the internal energy of the metal oxide, S is the material's entropy, and $`\mu_a`$ is the chemical potential of atomic species $`a`$. We can use this expression to define the grand potential of each material $`\Omega_i`$. We can associate the $`E(N_M, N_O)`$ with the total energy from a DFT calculation. 

The chemical potential of oxygen is defined by 

$$  \mu_{O_2} = \mu_{O_2}^o (T, p^o) + kT \ ln(p_{O_2}/p_{O_2}^o) $$

Where $`p_{O_2}^o`$ is the pressure of oxygen at 1 bar. Other useful relation is 

$$  \mu_{O_2} = E_{O_2}^{total} + \tilde \mu_{O_2}^o (T, p^o) + kT \ ln(p_{O_2}/p_{O_2}^o) $$

Here, $E_{O_2}^{total}$ is the total energy of an isolated oxygen molecule at $`T = 0`$ K. The second term on the rigth is the difference in the chemical potential of O$`_2`$ between $`T = 0 `$ K and the temperature of interest at the reference pressure. This chemical potential difference can be evaluated in the JANAF Thermochemical Tables. 

The chemical potential of molecular oxygen and atomic oxygen are related by 

$$  \mu_O = \dfrac{1}{2} \mu_{O_2}  $$


## Theory for metal clusters
The grand potential ($` \Omega `$) divided by N and assuming a constant number of metal atoms (e.g. Pt$`_2 `$)

$$  \omega (T,\mu_O, n) = \Delta E_{F,corr} (T) - T \cdot S_{Pt_2(O_2)n} + T \cdot S_{Pt_2}  - n \cdot \tilde \mu_{O_2} (p, T)  $$

Where $n$ is the number of oxygen molcules. A (p,T)-phase diagram can be constructed using the potential $` \omega `$. We can know the number $n$ of O$`_2`$ molecules which minimizes $` \omega `$
for a specified temperature and oxygen pressure. 

The formation energy of Pt$`_2`$(O$`_2`$)$`_n`$ clusters ($` \Delta E_{F,corr} (T) `$) is calculated as 

$$  \Delta E_{F,corr} = E_{Pt_2 (O_2)n} - E_{Pt_2} - n\cdot  E_{O_2} + E_{corr} (T) $$

E$`_{corr}`$ is introduced to account of the zero-point energy. The (T,p) dependence part of the chemical potential is expressed as 

$$  \tilde \mu_{O_2} (p,T) = \Delta H_{O_2} (p_0, T) - T\cdot S_{O_2} (p_0, T) + RT \ ln(p/p_0) $$

Where $` \Delta H_{O_2} `$  and $` S_{O_2} `$ are taken from the NIST database. Addionally, note that 

$$  \mu_{O_2}  = E_{O_2} + \tilde \mu_{O_2}   $$

## Thermochemistry

#### Zero-point vibrational energy

$$ E_0 = U_0 = E_{elec} + \sum_{i}^{modes} \dfrac{1}{2} h \omega_i  $$

Where $` E_{elec}`$ is the energy of the stationary point on the PES. 

#### Canonical ensemble

The partition function for the canonical ensemble is written as 

$$
Q(N,V,T) = \sum_i e^{E_i(N,V)/kT}
$$

Where i runs over all possible energy states of the system. The thermodynamic potentials are defined by the expressions

$$
U = kT^2 \bigg ( \dfrac{\partial ln \ Q}{\partial T} \bigg )_{N,V}
$$

$$
H = U + PV
$$

$$
S = k ln \ Q + kT \bigg ( \dfrac{\partial ln \ Q}{\partial T} \bigg )_{N,V}
$$

$$
G = H - TS
$$

#### Gas phase approximation

We assume that our ensemble is an ideal gas. This implies that gas molecules do not interact with each other. 

$$
Q(N,V,T) = \dfrac{[q(V,T)]^N}{N!}
$$

Where the factor $`1/N! `$ derives from the quantum mechanical indistinguishability of the particles. Now we assume
that the molecular energy $` \varepsilon `$ can be expressed as a separable sum of electronic, translational, rotational, 
and vibrational terms. 

$$
q(V,T) = q_{elec}(T)q_{trans}(V,T)q_{rot}(T)q_{vib}(T)
$$

#### Electronic contribution 



## References
* David S. Sholl, Janice A. Steckel. (2009). *Density Functional Theory: A Practical Introduction*. DOI:10.1002/9780470447710

* Karsten Reuter and Matthias Scheffler. *Physical Review B*. 2001, 65, 035406. DOI: 10.1103/PhysRevB.65.035406

* Mina Taleblou, Matteo Farnesi Camellone, Stefano Fabris, and Simone Piccinin. *The Journal of Physical Chemistry C*. 2022, 126, 10880−10888. DOI: 10.1021/acs.jpcc.2c02176

* David Buceta et al. *Chemistry -- A European Journal*. 2023, 29, e202301517. DOI: 10.1002/chem.202301517  
