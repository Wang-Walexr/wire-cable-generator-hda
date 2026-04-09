# Wire / Cable Generator HDA

A Houdini Digital Asset for generating game-ready wire and 
cable meshes from a curve input. Can be used in Unreal or Unity.
Built for environment artists who need fast, controllable wire dressing.


## The Problem

Dressing cables and wires across an environment level 
traditionally meant hand-modelling each wire individually 
and adjusting it by eye. For a single scene with 10 to 15 
cable runs this could take several hours, and any changes 
meant redoing the work manually.


## The Solution

A curve-driven HDA that generates the wire mesh procedurally. 
The artist draws a curve, drops the HDA, and adjusts 
parameters. No Houdini node knowledge required.


## Parameters

| Section               | Parameter                 | Description                                                   |
|-----------------------|---------------------------|---------------------------------------------------------------|
| Curve Settings        | Treat Polygon As          | Controls the curve profile at the conner making it smoother   |
| Main Cable            | Resolution                | General smoothness of the cable                               |
| -                     | Amount                    | The number of main cables                                     |
| -                     | Randomize Position        | Random postion of cables                                      |
| -                     | Spacing                   | Spacing between the main cables                               |
| -                     | Scale Multiplier          | Size of the main cables                                       |
| Small Cable           | Use Small Cable           | Whether to have or not have small cables                      |
| -                     | Randomize                 | Add randomness to the small cable by increasing amount        |
| -                     | Random Offset             | Random postion of small cables                                |
| -                     | Resolution                | General smoothness of the small cable                         |
| -                     | Amount                    | The number of small cables                                    |
| -                     | Scale                     | Size of the small cables                                      |
| Simulation            | Reset Simulation          | Reset cable simulation                                        |
| -                     | Enable Simulation         | Enable or disable cable simulation                            |
| -                     | Stretch                   | Stretch the cable (not length)                                |
| -                     | Friction                  | Friction between cables                                       |
| -                     | Output Frame              | The number of frame the cable simulation should run for       |
| Optimization          | Tolerance Cleanup         | Reduce polycount by adding details only at corners            |
| -                     | Main Cable Division       | The roundness of the main cable                               |
| -                     | Small Cable Division      | The roundness of the small cable                              |
| Material              | Material Type             | Select the engine shader to use (Unreal or Unity)             |
| -                     | Unreal/Unity Mat Path     | The path of the shader/material to be used                    |


## How to Use

1. Draw a NURBS or Bezier curve in your scene
2. Select the curve
3. Drop/Connect the Wire_Generator HDA onto it
4. Adjust parameters in the HDA parameter panel
5. Export as FBX for engine import or use the HDA file 
directly in game engine (Unreal or Unity).


## Requirements

- Houdini 19.5 or later
- No additional plugins required

## Demo

[Watch the 2-minute demo](https://youtu.be/aRCnfiybOTY)