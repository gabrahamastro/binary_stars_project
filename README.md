# Binary Stars Group Project

This repository contains the code and report relating to a group project undertaken at Keele University (2024-25) for the module PHY-30006 Astrophysics Group Project and Science Communication. 

## Aim

The project aim was to, using Gaia DR3 Epoch photometry and TESS light curves of eclipsing binary stars in the PLATO LOPS2 field, find high-priority targets for observation by the upcoming PLATO mission.

## Acknowledgements 

This project was completed with the guidance, help, advice and many useful resources provided by [Pierre Maxted](https://www.astro.keele.ac.uk/pflm/).

## Licence

Please note that these works are under copyleft licenses (details in the `LICENCE.md` files within the respective folders).

## Workflow
The following are files in the `code` directory:
1. `master_notebook_TESS.ipynb`: Used to download TESS data, remove bad data, detrend and save in a format to be used in [`jktebop`](https://www.astro.keele.ac.uk/jkt/codes/jktebop.html), task 3.
2. `jktebop_plots.ipynb`: Used to plot data outputted by `jktebop` (for TESS and Gaia data). Note that it assumes a particular format of file name (e.g. `model.out.3` and `lcfit.out.3` for outputted model and data to be fitted respectively).
3. `master_notebook_Gaia_NewFormat.ipynb`: Used to process Gaia data (using the output of analysis of TESS data with `jktebop` to help). Note that this uses the updated version (as of January 2025) of the data output (for reading the previous format, refer to `master_notebook_Gaia_OldFormat.ipynb`.
4. Again use `jktebop_plots.ipynb` (but now for reading in Gaia data, processed using `jktebop`).
5. `Overplot_models.ipynb`: For overplotting models generated for green, red and blue Gaia data, along with TESS data.
6. `CMD_single.ipynb`: For plotting a colour-magnitude diagram (CMD) of the outputted data (where data come from processing the BP, RP and G band data with `jktebop` in task 8. Note it uses the [MIST model](https://waps.cfa.harvard.edu/MIST/model_grids.html) `MIST_v1.2_feh_p0.00_afe_p0.0_vvcrit0.0_UBVRIplus.iso`, available from [here](https://waps.cfa.harvard.edu/MIST/data/tarballs_v1.2/MIST_v1.2_vvcrit0.0_UBVRIplus.txz)
7. `CMD_multiple.ipynb`: For plotting a colour-magnitude diagram (CMD) of the outputted data for multiple stars (again from the outputs of `jktebop` task 8 and the same MIST model data).

The `Report` directory consists of the `.pdf` output and LaTeX files which were used to generate this (using the AAAS Research Note template on Overleaf).
## Quick Start
To get started, first run the following commands:
```
pip install lightkuve

pip install astropy

pip install PyAstronomy.pyasl
```
`jktebop` can be downloaded from [here](https://www.astro.keele.ac.uk/jkt/codes/jktebop.html), whilst `read_mist_models` is available [here](https://waps.cfa.harvard.edu/MIST/resources.html).

## Software Versions
During this project the following software/Python packages were used:
- [`jktebop`](https://www.astro.keele.ac.uk/jkt/codes/jktebop.html): v43
- [`lightkurve`](https://lightkurve.github.io/lightkurve/): 2.5.0
- [`astropy`](https://www.astropy.org): 6.1.4
- [`PyAstronomy`](https://pyastronomy.readthedocs.io/en/latest/): 0.22.0
- [`uncertainties`](https://pythonhosted.org/uncertainties/): 3.2.2 
