## Initial considerations

**Fundamental questions**:

- In equilibrium with gas phase O$`_2`$, Which of Pt, PtO, and PtO$`_2`$ is the most stable?
- How should we normalize the energy of the different materials?
- We need a method that includes information about the temperature and pressure of O$`_2`$. 

**Basic principles**

*Phase:* it is a homogeneous region of matter in which there is no spatial variation in average density, energy, composition, or other macroscopic properties.

At constant T and P in a single-component system, the phase that is observed is the one which has the lowest Gibbs free energy per particle, or, equivalently, the lowest chemical potential μ(T, P).

## Theory
Grand potential of a metal oxide can be expressed as 

$$ \Omega (T,\mu_O, \mu_M) = E(N_M, N_O) - TS - \mu_O N_O - \mu_M N_M$$

Where $`E(N_M, N_O)`$ is the internal energy of the metal oxide, S is the material's entropy, and $`\mu_a`$ is the chemical potential of atomic species $`a`$. We can use this expression to define the grand potential of each material $`\Omega_i`$. We can associate the $`E(N_M, N_O)`$ with the total energy from a DFT calculation. 

The chemical potential of oxygen is defined by 

$$  \mu_{O_2} = \mu_{O_2}^o (T, p^o) + kT \ ln(p_{O_2}/p_{O_2}^o) $$

Where $`p_{O_2}^o`$ is the pressure of oxygen at 1 bar. Other useful relation is 

$$  \mu_{O_2} = E_{O_2}^{total} + \tilde \mu_{O_2}^o (T, p^o) + kT \ ln(p_{O_2}/p_{O_2}^o) $$

Here, $E_{O_2}^{total}$ is the total energy of an isolated oxygen molecule at $`T = 0`$ K. The second term on the rigth is the difference in the chemical potential of O$`_2`$ between $`T = 0 `$ K and the temperature of interest at the reference pressure. 

The chemical potential of molecular oxygen and atomic oxygen are related by 

$$  \mu_O = \dfrac{1}{2} \mu_{O_2}  $$




## References
* David S. Sholl, Janice A. Steckel. (2009). *Density Functional Theory: A Practical Introduction*. DOI:10.1002/9780470447710

* Karsten Reuter and Matthias Scheffler. *Physical Review B*. 2001, 65, 035406. DOI: 10.1103/PhysRevB.65.035406

* Mina Taleblou, Matteo Farnesi Camellone, Stefano Fabris, and Simone Piccinin. *The Journal of Physical Chemistry C*. 2022, 126, 10880−10888. DOI: 10.1021/acs.jpcc.2c02176
