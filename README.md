# two-level-counting-corrections

Symbolic Mathematica derivations of the photon-counting statistics of a
two-level emitter with dephasing noise, accompanying the paper:

**The Transient Counting Statistics of Autonomous Quantum Clocks**, *Oscar Arandes and Sreenath K. Manikandan* 

The notebook provides closed-form expressions for the asymptotic counting
cumulants and their initial-state transient corrections, as derived in the
paper.

## Model

A driven two-level emitter under continuous dephasing, with a single counted
decay channel. In the conventions used throughout (ℏ = 1):

- Hamiltonian: `H = γ_d σ_x`
- counted jump operator: `L_w = √(γ_w) σ_-`  (rate `γ_w`)
- dephasing along `X = cosθ σ_x + sinθ σ_z`, at rate `γ_m`

The detected photons are treated as the ticks of a clock; `N` is the number of
clicks in an observation window of length `t`.

## Contents

The notebook derives, in closed form:

- the steady state `ρ_ss`;
- the stationary emission rate `k_ss` and variance rate `v_ss`
  (leading, time-extensive terms of `⟨N⟩_t` and `Var(N)_t`);
- the initial-state transient constants `c_1` and `c_2`, defined through the
  long-time expansions
  `⟨N⟩_t = k_ss t + c_1`,  `Var(N)_t = v_ss t + c_2`,
  for the preparations considered in the paper (ground, excited, steady state);
- the time-resolved deviations `⟨N⟩_t − k_ss t` and `Var(N)_t − v_ss t`
  used to show how the offsets are established during the transient.

All quantities are obtained via the tilted generator and the Drazin inverse, as
described in the paper.

## Requirements

Mathematica.
