# Collective behaviour from optic flow and retinal cues

## Team

| Name | GitHub |
| --- | --- |
| Luka Brodnik | lbrodnikl |

## Project description

This project recreates and extends the vision-based model of collective motion by Castro, Ruffier & Eloy (2024). In most self-propelled particle models, each agent knows the exact positions and headings of its neighbours. In this model, agents use only what an eye or a camera can measure: the angular size of shades in their visual field and the optic flow of those shades. I will first implement the reference "omniscient" model and the visual model in Python and reproduce the paper's main results: the swarming, schooling and milling phases, the phase diagrams over attraction and alignment strength for two blind-angle settings, and the noise-driven switching between milling and schooling. I will then extend the model in two ways. First, agents will have different body sizes. That breaks the model's assumption that a shade's angular width encodes its distance, and I will test how it changes the collective phases and whether agents sort by size within the group. Second, agents will have a finite visual range (a distance cutoff, contrast fading, or a minimum resolvable angle). I will measure how limited visibility affects milling, schooling and group cohesion. Finally, I will combine both: when large agents are visible from farther away than small ones, visibility becomes one-way, and I will test whether that makes large agents leaders.

## Starting point

- D. Castro, F. Ruffier, C. Eloy, *Modeling collective behaviors from optic flow and retinal cues*, Physical Review Research 6, 023016 (2024). https://doi.org/10.1103/PhysRevResearch.6.023016
- Authors' reference code: https://gitlab.com/FlokingByEyeDiego/flokingbyeye
- Related work: Bastien & Romanczuk, *A model of collective behavior based purely on vision*, Science Advances (2020); Pearce et al., *Role of projection in the control of bird flocks*, PNAS (2014).

## Plan and milestones

### Report 1 — [13.11.2026]: omniscient baseline and visual perception
- Simulation framework (Euler–Maruyama integration, initial conditions, P/M/O metrics, plots, animations)
- Omniscient model; reproduce the three phases
- Visual field pipeline: shades with occlusion, apparent distance R, optic flow O and divergence D, unit-tested on simple configurations
- First single runs of the visual model

### Report 2 — [11.12.2026]: full reproduction
- Visual model reproduces swarming, schooling and milling
- Phase diagrams over (k_att, k_align) for blind-angle settings eps = 0 and 1, both models (at reduced resolution if compute is limited)
- Milling–schooling bistability
- Add per-agent radii and a visual-range parameter to the code; first test runs of both extensions

### Report 3 — [8.1.2027]: extension and final analysis
- Different body sizes: size-spread sweep, phase diagram, size-vs-position sorting, two-type segregation
- Finite visual range: range sweep for the visual and omniscient models, phase diagram at limited range, group fragmentation
- Combined: one-way visibility network and size-driven leadership
- Final comparison of the original and extended model; conclusions and limitations

## Progress

| Milestone | Status |
| --- | --- |
| Report 1 | Not started |
| Report 2 | Not started |
| Report 3 | Not started |

## Repository structure (planned)

- `src/` — model code (omniscient model, visual model, metrics)
- `experiments/` — scripts for single runs and parameter sweeps
- `results/` — figures and data
- `report/` — milestone reports
- `logs/` - code logs for debugging
```
