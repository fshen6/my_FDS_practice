# FDS Basic Workflow, Assumptions, Inputs, And Outputs

This note combines the Week 1 explanations on how Fire Dynamics Simulator (FDS) is used, what assumptions commonly enter an FDS model, what inputs and outputs are typical, and how FDS differs from some conventional CFD workflows.

FDS should be treated as a modelling workflow, not just a program to run. You define a simplified fire scenario, create an input file, run the transient solver, inspect logs and visualisations, post-process numerical outputs, and then interpret the result cautiously with clear assumptions and limitations.

## Basic FDS Workflow

### 1. Define The Engineering Question

Before writing an FDS file, decide what the model is meant to help you understand.

Examples:

- How does smoke move through this room?
- What temperatures occur near the ceiling?
- How quickly does visibility reduce at eye height?
- How sensitive are results to fire size or ventilation?

For a portfolio case, this can be written as a simple client or design question. The model should then be built around answering that question, rather than around making an impressive animation.

### 2. Define The Scenario

The scenario is the simplified world represented in the model.

It usually includes:

- room or enclosure dimensions
- openings, doors, vents, or windows
- fire location
- fire size or growth curve
- ventilation conditions
- simulation duration
- included and excluded objects
- key assumptions and limitations

This is where an assumptions register becomes useful. A good model starts with explicit assumptions before any solver settings are chosen.

### 3. Build The FDS Input File

FDS uses a plain text input file, usually ending in `.fds`.

The file tells FDS about:

- the case name and title
- the mesh and computational domain
- geometry and obstructions
- surfaces and materials
- fire source
- vents and openings
- output devices and visualisation outputs
- simulation time

The input file is essentially the recipe for the simulation.

### 4. Set Up The Mesh

The mesh divides the computational domain into grid cells. FDS solves the flow, heat transfer, and smoke transport over this grid.

Important mesh ideas:

- finer cells can resolve more detail but increase runtime
- coarse cells run faster but may miss important behaviour
- geometry is represented on a Cartesian grid
- small features below the grid scale may be lost or simplified
- mesh sensitivity is part of model quality assurance

At beginner level, the key point is that mesh size affects both computational cost and the reliability of key outputs.

### 5. Define The Fire

For beginner FDS work, the fire is often prescribed. That means you tell FDS what heat release rate behaviour to use, rather than asking FDS to predict the entire fire growth process from first principles.

Common fire definition choices include:

- fire location
- burner area
- heat release rate curve
- peak heat release rate
- growth rate or ramp
- soot yield, if visibility or smoke production matters
- CO yield, if toxicity is considered
- radiative fraction
- whether the fire spreads or stays fixed

The fire definition is one of the most important model assumptions. It should never be presented as "the real fire" unless it is strongly justified.

### 6. Define Outputs Before Running

FDS only saves the outputs you request.

Common output requests include:

- temperature devices
- visibility devices
- velocity devices
- gas concentration devices
- heat flux devices
- HRR output
- slice files for Smokeview
- boundary files for surface quantities

A good modelling habit is to decide what evidence you need before running the case.

### 7. Run FDS

The `.fds` input file is run through the FDS solver. FDS then produces log files, visualisation files, and numerical output files.

The first check after running is not whether the smoke looks interesting. The first check is whether the simulation ran correctly.

### 8. Check Logs, Warnings, And Solver Health

The `.out` file is a key QA file.

Check:

- whether the simulation started and finished correctly
- fatal errors
- warnings
- mesh and domain information
- HRR behaviour
- time-step behaviour
- pressure solver diagnostics
- maximum CFL number
- maximum divergence and velocity error indicators

These checks help you decide whether the model is numerically healthy before interpreting results.

### 9. Visualise In Smokeview

Smokeview is the companion visualisation tool for FDS outputs.

Use it to inspect:

- geometry
- smoke movement
- fire location
- temperature slices
- visibility slices
- flow paths
- doorway or vent behaviour
- whether the setup looks like the intended scenario

Smokeview is excellent for understanding behaviour, but screenshots alone are not enough for a professional report.

### 10. Post-Process Numerical Outputs

Python or another analysis tool is useful for plotting FDS numerical outputs.

Typical plots include:

- temperature vs time
- visibility vs time
- HRR vs time
- heat flux vs time
- velocity through an opening vs time
- comparison plots between cases

Post-processing gives quantitative evidence to support statements in a report.

### 11. Interpret Results Cautiously

The result of one FDS run is not "the answer." It is the result of one scenario under one set of assumptions.

Ask:

- What assumptions control this result?
- What happens if the fire size changes?
- What happens if ventilation changes?
- Is the mesh coarse?
- Were key outputs saved at useful locations?
- What physics were simplified or excluded?

Use cautious wording such as:

- "The model indicates..."
- "Within the simplified assumptions..."
- "The result is sensitive to..."
- "This should not be interpreted as a certified design..."

### Core Workflow

```text
Question
-> Scenario
-> Assumptions
-> FDS input file
-> Run solver
-> Check logs
-> View in Smokeview
-> Post-process numerical outputs
-> Interpret cautiously
-> Report assumptions and limitations
```

## Common Assumptions In FDS

FDS does not know the real fire scenario automatically. The modeller creates a simplified version of the world. The assumptions define what that simplified world includes and excludes.

### Geometry Assumptions

Real buildings and rooms are rarely modelled exactly.

Common assumptions:

- rooms are rectangular or block-like
- small objects are ignored
- furniture is simplified into large blocks
- walls, floors, and ceilings are flat
- small gaps, leakage paths, cable penetrations, or ducts may be ignored
- doors and windows are fixed as open, closed, or partly open

Example:

```text
A real workshop may contain benches, tools, shelves, cables, and uneven surfaces.
The FDS model may include only the room, one doorway, a few major obstructions, and a burner.
```

This can be acceptable for a learning model, but it must be stated clearly.

### Fire Assumptions

Fire assumptions are usually among the most important assumptions in the model.

Common assumptions:

- fire starts at a fixed location
- fire has a prescribed burner area
- HRR follows a specified curve
- peak HRR is fixed
- fuel type is simplified
- soot yield is fixed
- CO yield is fixed, if used
- radiative fraction is fixed
- fire spread is ignored or simplified

A simple learning case might assume:

```text
Fire location: centre of room
Fire type: prescribed burner
Peak HRR: fixed training value
Growth: prescribed ramp to peak
Fuel: simplified generic fuel
Fire spread: not included
```

The chosen fire should be treated as a scenario assumption, not as proof of what a real fire would do.

### Ventilation Assumptions

Ventilation strongly affects smoke movement, heat release, and tenability.

Common assumptions:

- a door is fully open for the full simulation
- a window is fully open or closed
- wind is ignored
- leakage is ignored
- mechanical ventilation is ignored
- fans are represented by fixed flow rates
- vents are treated as ideal openings

Example:

```text
Door assumed open.
No wind.
No mechanical extraction.
No leakage through construction joints.
```

Open-door vs closed-door cases can later become a useful sensitivity study.

### Material And Surface Assumptions

Beginner FDS models often simplify or ignore detailed material behaviour.

Common assumptions:

- walls are inert
- floor and ceiling are inert
- obstructions do not burn
- heat conduction into walls is simplified or ignored
- thermal degradation is not modelled
- furniture does not ignite or spread fire

This means the model may be useful for learning smoke and heat movement, but not necessarily for predicting realistic fire spread.

### Mesh Assumptions

The selected mesh is itself an assumption.

Common assumptions:

- the cell size is adequate for a training case
- small features below the mesh scale are ignored
- mesh sensitivity has not yet been fully tested
- the computational domain is large enough for the scenario
- grid resolution is sufficient near the fire and openings for the learning objective

Mesh sensitivity should be recorded as a limitation if it has not been tested.

### Ambient And Initial Condition Assumptions

Many beginner models start from simple ambient conditions.

Common assumptions:

- uniform initial temperature
- still air
- normal atmospheric pressure
- no initial smoke
- no initial thermal stratification
- no wind
- humidity effects ignored

Example:

```text
Initial room condition: 20 C, still air, no smoke.
```

### Suppression, Detection, And Human Response Assumptions

Beginner models often exclude active systems and human behaviour.

Common assumptions:

- no sprinklers
- no manual firefighting
- no alarm activation
- no detector response
- no occupant door-opening behaviour
- no suppression or intervention

These exclusions matter because real fires can be strongly affected by detection, suppression, and human actions.

### Occupant-Related Assumptions

FDS itself is not normally used as the main evacuation model in modern portfolio workflows. FDS+Evac is no longer supported in current FDS releases, so evacuation is usually handled separately through ASET/RSET reasoning or a tool such as Pathfinder.

For smoke studies, occupant-related assumptions often appear as assessment locations:

- eye height
- escape route locations
- doorway locations
- key tenability points
- measurement points near exits

## Common FDS Inputs

FDS inputs are written in a structured text file. The file contains namelist entries that begin with commands such as `&HEAD`, `&MESH`, and `&VENT`.

### Case Identity

The `HEAD` line defines the case identifier and title.

Example:

```text
&HEAD CHID='room_fire', TITLE='Simple Room Fire' /
```

Typical meaning:

- `CHID` controls the case name and output file names
- `TITLE` describes the case

### Simulation Time

The `TIME` line defines the simulation duration.

Example:

```text
&TIME T_END=300. /
```

This runs the simulation to 300 seconds of simulated time.

### Mesh And Computational Domain

The `MESH` line defines the calculation grid and domain extents.

Example:

```text
&MESH IJK=40,30,25, XB=0,4, 0,3, 0,2.5 /
```

Conceptually, this means:

- x direction from 0 m to 4 m
- y direction from 0 m to 3 m
- z direction from 0 m to 2.5 m
- divided into grid cells

### Geometry

Common geometry-related inputs include:

- `OBST` for solid blocks and obstructions
- `HOLE` for openings cut through obstructions
- `VENT` for openings, burners, fans, or boundary conditions applied to faces

Typical uses:

```text
OBST = wall, table, cabinet, burner block
HOLE = doorway or window opening
VENT = open boundary, fire surface, supply vent, exhaust vent
```

### Surfaces And Materials

Common surface and material inputs include:

- `SURF`
- `MATL`

`SURF` defines how a surface behaves.

Examples:

- inert wall surface
- burner surface
- open boundary
- supply air surface
- exhaust surface
- prescribed temperature surface
- thermally thick wall

For beginner models, many surfaces may be inert unless the learning objective requires material heating or burning.

### Fire Inputs

A simple prescribed fire often uses a burner surface and a heat release rate per unit area.

The basic idea is:

```text
burner area x HRRPUA = approximate total HRR
```

Common fire input concepts:

- burner size
- `HRRPUA`
- HRR ramp
- fuel or reaction definition
- soot yield
- CO yield
- radiative fraction

At Week 1 level, the important point is not to memorise every parameter. The important point is to understand that the fire is an input assumption.

### Ventilation Inputs

Ventilation may be represented using openings, vents, or fans.

Examples:

- open doorway
- open window
- supply vent
- exhaust vent
- pressure boundary
- open exterior boundary
- fan or specified flow

For a simple room fire, a doorway might be represented as an open vent.

### Device Inputs

Devices are point measurements, commonly defined with `DEVC`.

Common device quantities:

- gas temperature
- visibility
- velocity
- oxygen concentration
- CO concentration
- heat flux
- pressure
- smoke detector response

Example measurement intentions:

```text
Measure gas temperature at eye height near the exit.
Measure visibility at eye height in the room.
Measure velocity through the doorway.
```

Device outputs are especially useful because they can be plotted later.

### Slice File Inputs

Slice files are 2D planes through the model, commonly defined with `SLCF`.

Common slices:

- vertical temperature slice through the fire
- horizontal visibility slice at eye height
- vertical velocity slice through a doorway
- soot density slice
- oxygen concentration slice

Slices are useful in Smokeview because they show field behaviour across an area rather than at one point.

### Boundary File Inputs

Boundary outputs, commonly associated with `BNDF`, record quantities on surfaces.

Common boundary outputs:

- wall temperature
- heat flux to a surface
- burning rate
- surface-related thermal quantities

These are useful when surface heating or heat flux is important, but they may not be needed in the first beginner model.

### Output Timing

FDS output frequency matters.

If outputs are too frequent:

- files become large
- runs may be harder to manage

If outputs are too sparse:

- important transient behaviour may be missed
- plots may be too coarse

Output timing should match the purpose of the case.

## Common FDS Outputs

FDS outputs can be grouped into logs, visualisation files, numerical data, and post-processed figures.

### Log Output

The `.out` file is a major quality-assurance output.

It can show:

- whether the model started correctly
- fatal errors
- warnings
- mesh information
- simulation progress
- HRR behaviour
- solver diagnostics
- completion status

Beginner rule:

```text
Check the .out file before trusting Smokeview images.
```

### Smokeview Files

FDS produces files that Smokeview uses for visualisation.

Smokeview can display:

- geometry
- smoke movement
- fire location
- slices
- boundary quantities
- velocity vectors
- particles
- isosurfaces

Smokeview is very useful for understanding the scenario, but screenshots should support specific technical observations.

### Device CSV Outputs

Device outputs are among the most useful report evidence.

Examples:

- time vs ceiling temperature
- time vs eye-height visibility
- time vs doorway velocity
- time vs heat flux
- time vs gas concentration

These outputs are normally plotted using Python or another analysis tool.

### HRR Output

HRR output helps check whether the fire behaved as intended.

Use it to check:

- whether the prescribed fire followed the intended curve
- whether peak HRR was reached
- whether HRR changed unexpectedly
- whether the run behaved plausibly

Even for a prescribed fire, HRR output should be checked.

### Slice Outputs

Slice outputs are visual field outputs.

Useful examples:

- vertical temperature slice through the fire centreline
- horizontal visibility slice at 1.8 m height
- vertical velocity slice through a doorway
- smoke or soot density slice

These outputs help explain spatial behaviour, such as smoke layer development and flow paths.

### Boundary Outputs

Boundary outputs describe surface quantities.

Examples:

- wall temperature
- heat flux to a surface
- ceiling heating
- burner surface output

These become more important in cases involving surface heating, ignition risk, or heat flux assessment.

### Post-Processed Figures

Post-processed figures are created after the run, often using Python.

Examples:

```text
temperature_vs_time.png
visibility_eye_height.png
hrr_curve.png
doorway_velocity.png
case_comparison_visibility.png
```

These figures are important for reproducible analysis and professional reporting.

## Convergence, Residuals, And Solver Health

FDS does not normally use convergence residual graphs in the same way as many steady-state RANS CFD workflows.

In some CFD tools, it is common to monitor residuals such as:

- continuity residual
- x-velocity residual
- y-velocity residual
- energy residual
- turbulence residuals

The goal in those cases may be to reduce residuals toward a convergence target.

FDS is different. It is usually used as a transient, LES-style fire model. The main question is not:

```text
Have the residuals converged?
```

The better questions are:

```text
Is the time-marching simulation numerically stable?
Are the outputs physically reasonable?
Are solver diagnostics acceptable?
Are key results reasonably insensitive to mesh and input changes?
```

### What To Monitor In FDS

Important checks include:

- the simulation completes without fatal errors
- warnings are understood
- time step behaviour is reasonable
- CFL number is not problematic
- pressure iterations behave normally
- maximum velocity error is not concerning
- maximum divergence indicators are not concerning
- HRR follows the intended curve
- temperature, visibility, velocity, and other outputs are plausible
- key results are checked against mesh or scenario sensitivity where possible

These are solver health and model quality checks, not a simple residual-convergence graph.

### Mesh Sensitivity As A Form Of Confidence Building

For FDS, mesh sensitivity is often more important than looking for a residual plot.

A mesh sensitivity check might compare:

- temperature at selected points
- visibility at eye height
- HRR behaviour
- smoke layer development
- flow through openings
- time to a selected threshold

If key results change greatly when the mesh changes, the model is mesh-sensitive and the result needs cautious interpretation.

### Transient Fluctuations

Because LES is unsteady, outputs can fluctuate. You should often interpret:

- trends
- peaks
- time to threshold
- moving averages where justified
- scenario comparisons

Do not expect a transient FDS result to behave like a steady residual-converged RANS solution.

## Boundary Layers And Mesh Considerations

Boundary layers matter physically, but FDS does not usually mesh them in the same way as many body-fitted CFD workflows.

In many CFD tools, especially RANS workflows, it is common to create:

- prism layers
- inflation layers
- wall-normal refinement
- y-plus targets
- wall-resolved boundary layers

FDS normally does not work like that.

### No Typical Inflation-Layer Workflow

FDS uses a rectilinear Cartesian mesh. Geometry is represented on that grid rather than with a body-fitted mesh around every wall and object.

So, for ordinary FDS fire modelling:

```text
You usually do not create inflation layers or prism layers.
```

### But Near-Wall Behaviour Still Matters

Near-wall velocity and temperature gradients can matter for:

- ceiling jets
- wall jets
- convective heat transfer
- wall heat flux
- smoke movement near surfaces
- tunnel or duct-like flows
- forced ventilation cases

However, in practical building-scale fire simulations, the true viscous boundary layer may be much smaller than the grid size. FDS therefore relies on near-wall modelling rather than requiring the modeller to resolve every viscous sublayer with inflation cells.

### What Mesh Issues Matter More In Beginner FDS Work

For early FDS cases, focus on:

- fire and plume resolution
- opening and doorway resolution
- smoke layer resolution
- obstruction representation
- avoiding unnecessary tiny geometry features
- sensible cell aspect ratios
- output device placement
- mesh sensitivity

A useful practical statement for reports is:

```text
The model uses a simplified Cartesian mesh suitable for a training case.
Boundary layers are not directly resolved; near-wall behaviour is treated through FDS wall modelling.
Key outputs should therefore be interpreted with mesh sensitivity and model limitations in mind.
```

## Useful Official Sources

- [NIST FDS-SMV homepage](https://pages.nist.gov/fds-smv/)
- [NIST FDS-SMV manuals](https://pages.nist.gov/fds-smv/manuals.html)
- [FDS User Guide source repository](https://github.com/firemodels/fds/tree/master/Manuals/FDS_User_Guide)
- [FDS Technical Reference Guide source repository](https://github.com/firemodels/fds/tree/master/Manuals/FDS_Technical_Reference_Guide)

