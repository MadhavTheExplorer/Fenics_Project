# FEniCS Heat And Structural Optimization Studies

A collection of finite-element learning and research experiments developed with legacy FEniCS/DOLFIN. The work covers introductory PDE examples, transient laser heating, parametric membrane optimization, and topology optimization.

## Project Areas

| Area | Representative entry point | Purpose |
| --- | --- | --- |
| Heat conduction | `Heat_Conduction_Problem/heat_conduction.py` | Transient moving-laser heat conduction for surface-hardening studies. |
| Parametric shape optimization | `Para_Shape_Opt/pshape.py` | Membrane thickness and shape experiments. |
| Topology optimization | `Topology_Opt/Heatsink_TO2.py` | Heat-sink and cantilever material-distribution studies. |
| FEniCS exercises | `fenics_trial/` | Poisson, heat, membrane, and other introductory examples. |

## Environment

These scripts target the legacy FEniCS stack (`from fenics import *`), not FEniCSx. A compatible Ubuntu-era environment should include:

- Python 3
- FEniCS/DOLFIN
- NumPy and Matplotlib
- Jupyter for the notebooks
- meshio tooling where mesh conversion is required
- FreeFEM++ for `fenics_trial/membrane.edp`

Because legacy FEniCS packages are tightly coupled to system libraries, use a compatible FEniCS container or conda environment rather than installing modern FEniCSx packages into an arbitrary Python environment.

## Running A Study

Run each study from its own directory because several scripts use relative mesh and output paths. For example:

```bash
cd Heat_Conduction_Problem
python heat_conduction.py
```

Review mesh names, output directories, physical units, and solver settings inside a script before execution. The code is preserved as an archived research/learning record and may require path or API updates on current installations.

## Generated Results

PVD, VTU, HDF5, NumPy archive, and topology-optimization output files are generated artifacts and are ignored for future runs. Existing tracked results remain as historical references. Notebook outputs may also be large and should be cleared before substantial future edits.

## Attribution

Several introductory scripts and notebooks follow examples from the FEniCS and FreeFEM learning ecosystems or coursework. Consult source comments and notebook context before reuse. No repository-wide open-source license has been declared.

## Portfolio Metadata

`.explorer/project.yml` classifies this repository in the `computational-engineering` family.
