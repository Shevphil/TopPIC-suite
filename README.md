# TopPIC: TOP-Down Mass Spectrometry Based Proteoform Identification and Characterization Guide
For manual and reference, please visit https://www.toppic.org/software/toppic/




File Format Conversion


We use MSConvertGUI to convert the raw files to mzML files.

The filter "Peak Picking vendor msLevel=1-" is selected. The peak picking filter (step 3) is used to generate centroid, not profile, mzML data files, which are required by the spectral deconvolution tool TopFD.


Mass Spectral Deconvolution

We use topfd_gui for top-down mass spectral deconvolution.

I do not make any selections at this stage in the process but a few things are preselected. The screenshot of topfd_gui is shown below.

![topfd_screenshot] [topfd_screenshot.png](https://github.com/Shevphil/TopPIC-suite/blob/main/topfd_screenshot.PNG)


Mass Spectral Identification

We use toppic_gui to search the MS/MS spectra in msalign files against the protein database to identify PrSMs.


