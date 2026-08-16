# sigmaSprayAngle

This is the Python code was developed to define the spray angle fitting domain of the pressure swirl hollow cone spraying system using a an image base statistical criterion that remove the user dependencies.

A detailed description of the can be found in the paper Fauzy and Wu, RESULTS ENG. 112403 (2026), [doi.org/10.1016/j.rineng.2026.112403]( https://doi.org/10.1016/j.rineng.2026.112403). Please cite this paper when using the code.

The code was developed using Python 3.10.16. The packages OpenCv-Python should be installed.

# How to use

The main file is

```sh
sigmaImageProcessing.py
```
More detailed descriptions can be found in the code.

Please note that calibration of pixel-to-mm ratio is specific for each experimental setup. Sample images (50 frames, P$_{inj}$ = 2.0 MPa) captured using the high speed camera are provided (see 'useful links' below), but these will only used to demonstrate the logic image processing from the raw image to obtain the two important markers (Z$_{\sigma,max}$ and Z$_{\sigma',min}$).

1. Edit CINE_PATH below to point at the .cine file for one pressure.
2. Edit BG_FRAME_INDEX if the non-spraying reference is not frame 0.
3. Run:  python sigmaImageProcessing.py
Outputs land in Results_cine_maxI/ next to the cine file (CSVs and per-frame uint16 PNGs). The CSV schema matches the TIFF pipelines so downstream analysis scripts (Z_b extraction, ROI sweeps) work unchanged.

# Useful links
[Rflow lab NCKU web](https://rflowlab.tw/)
