
## QE input files BCC iron AIMD: nonmagnetic and noncollinear calculations

Each case contains three preparatory self-consistent-field (SCF) inputs followed by a molecular-dynamics (MD) input:

| Input file | Purpose | Main setting |
| --- | --- | --- |
| `stage1_4e-3.in` | Initial SCF and spin-state setup | `conv_thr=4.0e-3`; noncollinear constraint starts at `lambda=0.005` |
| `stage2_1e-3.in` | Refine the SCF solution | `conv_thr=1.0e-3`; `lambda=0.020` |
| `stage3_1e-4.in` | Final SCF preparation | `conv_thr=1.0e-4`; `lambda=0.100` |
| `md_50steps.in` | AIMD production trajectory | In the 200-step package, `nstep=200` despite the legacy filename |


## Shared QE settings

The nonmagnetic and noncollinear calculations use the same underlying DFT setup where applicable: PBE with the Fe PAW pseudopotential `Fe.pbe-spn-kjpaw_psl.1.0.0.UPF`, `ecutwfc=71 Ry`, `ecutrho=496 Ry`, and Fermi-Dirac occupations with `degauss=0.025334 Ry`. The nonmagnetic reference uses a non-spin-polarized calculation; it does not use the noncollinear magnetic constraints listed below.

The noncollinear production inputs use:

- `calculation='md'`, `nat=32`, and `ibrav=0`, with the BCC cell supplied explicitly (4×2×2 supercell).
- `noncolin=.true.`, `lspinorb=.false.`, and `constrained_magnetization='atomic'`.
- Thirty-two Fe species labels, one per atom, with `starting_magnetization(i)=0.125` and atom-specific `angle1(i)`/`angle2(i)` spin directions.
- `lambda=0.1` for production MD and `report=1`.
- `dt=20.67` atomic units and, for the extended200 inputs, `nstep=200`.
- Stochastic velocity rescaling (`ion_temperature='svr'`), `nraise=20`, and `tempw` set to 4,000, 5,000, or 6,000 K. Velocities are provided in the input and have center-of-mass motion removed.
- SCF convergence threshold `1.0e-4` during MD, up to 2,500 electronic iterations, local-TF mixing with `mixing_beta=0.01`, and conjugate-gradient diagonalization.
- Spin-orbit coupling disabled (`lspinorb=.false.`).



## Initial configurations and provenance

The intended comparison uses nonmagnetic BCC AIMD as the structural reference for noncollinear BCC32. In the sigma-based initialization workflow, the displacement width is fitted to the latter half of the matching nonmagnetic trajectory; a 32-atom BCC starting structure is then generated from that width, with center-of-mass motion removed and the displacement RMS and minimum pair distance constrained. This uses the nonmagnetic trajectory as a source of thermal-displacement statistics, rather than copying a 128-atom snapshot directly.

