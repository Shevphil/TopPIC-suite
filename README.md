# TopPIC: TOP-Down Mass Spectrometry Based Proteoform Identification and Characterization Guide
For manual and reference, please visit https://www.toppic.org/software/toppic/
<br>




### File Format Conversion


<p>We use <em>MSConvertGUI</em> to convert the raw files to mzML files. The filter <br> <em>"Peak Picking vendor msLevel=1-"</em> <br> is selected. The peak picking filter is used to generate centroid, not profile, mzML data files, which are required by the spectral deconvolution tool TopFD.</p>
 <br>


### Mass Spectral Deconvolution

  We use <em>topfd_gui</em> for top-down mass spectral deconvolution.

I do not make any selections at this stage in the process but a few things are preselected. The screenshot of topfd_gui is shown below.

![topfd_screenshot.png](https://github.com/Shevphil/TopPIC-suite/blob/main/topfd_screenshot.PNG)

<br>


### Mass Spectral Identification

  We use <em>toppic_gui</em> to search the MS/MS spectra in msalign files against the protein database to identify PrSMs. <br>
  - *C57 is selected as the fixed modification<br>
   >C57 is selected as the fixed modification because proteins were reduced with dithiothreitol and alkylated with iodoacetamide before the MS experiment. When proteins are not reduced, no fixed modification should be selected.
  - *FDR is selected as the spectrum level cutoff type
   >A shuffled decoy database is concatenated to the target database to estimate spectrum-level and proteoform-level FDRs. All identified PrSMs are first filtered by a 1% spectrum-level FDR and the resulting PrSMs are reported
  - *FDR is also selected as the proteoform level cutoff type
   >The proteoforms corresponding to the PrSMs are further filtered using a 1% proteoform-level FDR and the resulting proteoforms and their corresponding best PrSMs are reported

The screenshots of TopPIC gui are shown below.

![topPic_screenshot](https://github.com/Shevphil/TopPIC-suite/blob/main/Screen%20Shot%202022-12-03%20at%203.22.35%20PM.png)
![topPIC_screen](https://github.com/Shevphil/TopPIC-suite/blob/main/Screen%20Shot%202022-12-03%20at%203.22.45%20PM.png)

