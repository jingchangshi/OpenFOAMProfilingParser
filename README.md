# Overview

[OpenFOAM profiling] generates the profiling statistics of a running case.
OpenFOAM's `profilingSummary` collects the results from each processor and combine them ina single file in `postProcessing/profiling/[YourTimeStep]/profiling`.

Use this python script to parse this profiling file and generates a figure to show a better representation of the profiling results.

# Requirements

- `graphviz` to call `dot` to draw the figure
  - `apt install graphviz`
  - python packages: `pip install graphviz`

# Usage

Run

```
python3 OFProfilingParser.py input.json
```

`input.json` contains the configurations.

- `profiling_file`: the file name of the OpenFOAM profiling results
- `dot_format`: the figure format
- `dot_shape`: the shape of the node in the dot script
- `case_name`: the case name which affects the figure file name

# Example

<img src="https://raw.github.com/jingchangshi/OpenFOAMProfilingParser/master/OpenFOAM_Profiling_motorBike_GAMG_GridM_Dot.gv.svg">

