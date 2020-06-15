[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3891944.svg)](https://doi.org/10.5281/zenodo.3891944)

# MMS SITL Ground Loop: Automating the burst data selection process

Global-scale energy flow throughout Earth’s magnetosphere is catalyzed by processes that occur at Earth’s magnetopause (MP) in the electron diffusion region (EDR) of magnetic reconnection. Magnetic reconnection is an explosive process by which magnetic field lines from the Earth and Sun break and reconnection, releasing vast amounts of energy. To study the electron dynamics that trigger reconnection, large volumes of high time resolution data are required -- more data than can be downlinked to Earth. To ensure the right data is returned, NASA science missions typically employ burst triggers, a type of look-up table of threshold values applied to data from each instrument. The Magnetospheric Multiscale (MMS) mission also uses a human Scientist-in-the-Loop (SITL) who searches through low time resolution data to identify (among other things) the magnetopause, the boundary between the Earth and Sun's magnetic field where reconnection is likely to occur.

We use machine learning to classify magnetopause crossings, thereby automating a critical SITL task. To do so, we used historical SITL classifications and data available to the SITL at the time they make their selections. Features are derived from the Analog Fluxgate Magnetometer, Electric Field Double Probes, and Fast Plasma Investigation instruments on MMS. We find that the initial model is able to correctly identify 75% of all burst selections classified as magnetopause crossings by the SITL, and 70% of all model selections are also selected by the SITL.

The code we used for this study is included in this repository as an ipython notebook (to view the ipython notebook, use the [Jupyter notebook viewer](http://nbviewer.jupyter.org/)). It uses libraries from [TensorFlow](https://www.tensorflow.org/) for the machine learning analysis. The ipython notebook and additional data files are also permanently available in the **Zenodo Digital Repository**. To read more about the research, see **Argall, Small, et al. (2006)**.

## Related links
Specific releases used in the development of the paper:

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3891992.svg)](https://doi.org/10.5281/zenodo.3891992) Notebooks to train and run the [GLS-MP](https://github.com/colinrsmall/GLS-MP) LSTM model.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3884266.svg)](https://doi.org/10.5281/zenodo.3884266) Data used to train, validate, and run the GLS-MP model. It also contains magnetopause predictions.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3894873.svg)](https://doi.org/10.5281/zenodo.3894873)
 [PyMMS](https://github.com/argallmr/pymms) software for downloading MMS data, burst selections, and ground loop models

## Citation
If you make use of any of this code or examples in a scientific publication, please consider citing our paper.

Here is the bibtex entry for the paper:


This software is archived in the digital repo Zenodo via the link above and can be cited as:

```
@software{argall_matthew_r_2020_3891944,
  author       = {Argall, Matthew R. and
                  Small, Colin, R. and
                  Petrik, Marek},
  title        = {{MMS SITL Ground Loop: Software to Reproduce 
                   Figures and Tables}},
  month        = jun,
  year         = 2020,
  publisher    = {Zenodo},
  version      = {v0.1.0},
  doi          = {10.5281/zenodo.3891944},
  url          = {https://doi.org/10.5281/zenodo.3891944}
}
```
