# Single-photon self-imaging

Code and data for the study *Exact Photon-Count Recurrence with Low Optical-Mode Overlap in Wavelength-Scale Periodic Fields*.

A spatially resolving photon counter can record the same outcome distribution at two planes while the underlying optical mode has changed. The notebooks compare the complete outcome distribution of a single-photon position measurement, including the no-click outcome, with the squared state overlap maximized over lateral translations. They cover:

- a three-order mode with an overlap floor of 1/2 attained at an exact image recurrence;
- square nine-mode states, whose maximum overlap is reached at one of four shifts, including a construction with identical pixel and no-click probabilities and a maximum overlap of exactly 1/4;
- perfectly conducting slit screens with three and with five propagating orders, solved for TE and TM incidence, including a scan of one-, two- and three-slit screens, an imaging-receiver model, a harmonic audit, convergence checks, an independent discretization and a sensitivity analysis.

## Contents

| Path | Content |
|---|---|
| `notebooks/Self_Imaging_Recurrence_Scan_and_Sensitivity.ipynb` | Reproduces every number, table and figure of the study in one run |
| `notebooks/Quantum_Click_Self_Imaging_2D.ipynb` | Standalone nine-mode benchmark on a 1.7-wavelength square cell |
| `notebooks/Quantum_Field_Diffraction_Intensity_Self_Imaging.ipynb` | Stochastic (differential-evolution) search over the same slit families |
| `results/self_imaging_recurrence_summary.json` | All reported quantities, as written by the main notebook |
| `results/*.pdf` | Figures produced by the main notebook |
| `Self_Imaging_Propagation.html` | Interactive animation of the three-order mode; open in a browser |

## Running

```
pip install -r requirements.txt
jupyter nbconvert --to notebook --execute notebooks/Self_Imaging_Recurrence_Scan_and_Sensitivity.ipynb
```

The main notebook runs in about 35 minutes on two CPU cores and prints its progress. Figures and the summary are written to `outputs/Quantum_Field_Diffraction/`. On Google Colab they are written to `/content` and copied to `MyDrive/Outputs/Quantum_Field_Diffraction/`. The stored outputs were produced with Python 3.13, NumPy 2.5, SciPy 1.18 and Matplotlib 3.11.

All lengths are in units of the wavelength. The screens are zero-thickness perfect conductors, invariant along the slits, under monochromatic normal incidence. The detector models are stated in the notebooks. No measured data are used.

## License

MIT. See `LICENSE`.
