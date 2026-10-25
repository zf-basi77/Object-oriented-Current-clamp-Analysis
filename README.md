# Object-oriented-Current-clamp-Analysis

CClamp — Current-Clamp Electrophysiology Analysis
CClamp is a Python class for organizing and analyzing current-clamp electrophysiology recordings. It maintains a unified pandas DataFrame containing recording metadata, voltage traces, current injections, and derived measurements.

Features

Data management: Load recordings from individual pickle files or batch-process an entire folder, with optional protocol filtering.
Preprocessing: Calculate corrected current injections and generate identifiers for recording series.
Action potential detection: Automatically detect AP peaks or manually tune detection parameters through an interactive GUI.
Intrinsic excitability: Generate firing-rate versus current (F-I) plots and estimate steady-state voltage responses and input resistance.
Action potential characterization: Measure maximum and minimum dV/dt, fit exponential decay time constants, calculate AP half-width, and manually annotate AP threshold and afterhyperpolarization (AHP).
Visualization: Plot voltage traces, detected peaks, waveform features, regression fits, and F-I relationships.
Analysis methods generally append their results to self.df and return the CClamp instance, supporting chained analysis workflows.

Dependencies: NumPy, pandas, Matplotlib, SciPy, pathlib, and Tkinter, with Matplotlib's Tkinter backend for interactive annotation.


--Workflow:
1) Obtain HEKA .dat files from current-clamp recordings
2) Process .dat files via Matlab (HEKA Patchmaster importer, https://www.mathworks.com/matlabcentral/fileexchange/70164-heka-patchmaster-importer?s_tid=FX_rc1_behav)
3) read and save data in a python/pandas dataframe structure (use mat2ptyhon_HEKAimmporter.ipynb)
4) read and analyze the structure via CurrentClamp_class


- TO DO:
- add images of visualization exampled (Phase plots, AP plots, diagnostic plots, etc)
- add sample data for user to understand workflow and file structures
