## svd-ai-lab

We are a team of scientists and engineers connecting AI agents to software and hardware to automate engineering R&D.

### Projects

- **[sim-cli](https://github.com/svd-ai-lab/sim-cli)** — a CLI runtime that lets LLM agents launch, drive, and observe CAD/CAE simulators (Fluent, COMSOL, MATLAB, and more) through one protocol.
- **[sim-skills](https://github.com/svd-ai-lab/sim-skills)** — agent playbooks that teach LLMs how to drive every engineering tool, paired with the sim-cli runtime.
- **[sim-plugin-index](https://github.com/svd-ai-lab/sim-plugin-index)** — curated public index of out-of-tree drivers. `sim plugin install <name>` resolves bare names against this repo.

### sim plugins

Drivers ship as out-of-tree plugins so the core CLI stays small and each solver can move independently. Install any plugin in the index with:

```bash
sim plugin install <name>
```

Example — the LTspice driver, [`sim-plugin-ltspice`](https://github.com/svd-ai-lab/sim-plugin-ltspice), is a thin adapter that bundles the `.asc/.net/.raw/.log` library alongside the driver in one wheel:

```bash
sim plugin install ltspice
sim plugin doctor ltspice
```

Browse the full catalog in [`sim-plugin-index/index.json`](https://github.com/svd-ai-lab/sim-plugin-index/blob/main/index.json) — currently ~27 OSS solvers including OpenFOAM, CalculiX, Gmsh, ParaView, PyVista, LAMMPS, SU2, Elmer, PyBaMM, CoolProp, and more.
