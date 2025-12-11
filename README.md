PROJECT DESCRIPTION
This project on computational gravitational physics analyses raw data regarding the strain
occurring in the arms of LIGO interferometers in case of contact with a gravitational wave.
Gravitational waves disturb the spacetime along which it travels, and hence it causes spatial
consequences like strain. LIGO arms are designed such that they always produce destructive
interference, but when there is change in spacetime, one of the lengths of the arms increases
while the other (perpendicular to it) decreases. Thus, the light in the two arms are no longer
out of phase for destructive interference and light is observed in the detector; this is how strain
is measured.
However, the raw strain data is very noisy due to other spatial reasons, and gravitational waves
cannot be directly deciphered from it. Hence, lot of derivations and computations are required
on the raw strain data before the existence of gravitational waves can be concluded.
The first gravitational wave was observed through LIGO interferometers on 14 September 2015
(named GW150914).
This project replicates the computations and plots involved in concluding the existence of
GW150914. It lies an essential achievement in the history of science, not only because it
validates the predictions made by the General Theory of Relativity, but also because of the
computations involved in it that make science even easier.

METHODOLOGY
All data used in the project is open source, taken from 'gwosc' and 'gwpy' modules of python for
gravitational wave analysis and 'pycbc' module for template matching to expected results (from
General Theory of Relativity).
1. Fetch raw strain data
2. Normalise and whiten the data to amplify weak signals
3. Introduce a bandpass filter (35Hz - 350Hz)
4. Create a spectrogram of the data
5. Download a template of expected strain data when a gravitational wave may occur, and tally
it with current data to obtain signal-to-noise ratio
All of these steps of carried out for H1 (Hanford) and L1 (Livingston) detectors of LIGO for
Observational Run 1 (O1) of GW150914, and both are also compared at the same time,
keeping in mind that the GW arrived at L1 6.9ms later and was also inverted due to geometric
arrangement of the detector

KEY RESULTS
1. All results were obtained as expected from Abbott et al., PRL 2016
2. There occurs a distinctive chirp in the whitened and filtered strain data due to the FW
3. L1 data appears to be slightly fainter than H1
4. SNR of H1 is around 17, while that of L1 is around 12
5. The spectrogram resembles that of a binary black-hole merger

FILES STRUCTURE
1. 01_TimeSeries : fetching open source strain data of GW150914 from GWOSC database using
gwpy module in python and then plotting it.
2. 02_Filtering : whitening and filtering the data with a bandpass filter of 35Hz - 350Hz and
notches at harmonics of 60Hz
3. 03_spectrogram : plotting a spectrogram as a contour plot and saving plots for H1 and L1
separately
4. 04_SNR : finding a template which represents the GW150914 binary black hole merger and
matching it against the data using pycbc module
5. 05_Results : combining all derived result plots

REFERENCES
1. gwosc.readthedocs.io
2. gwpy.readthedocs.io
3. ligo.caltech.edu
4. physicstoday.aip.org/news/ligo-detects-gravitational-waves
5. B.  P. Abbott et al., “Observation of Gravitational Waves from a Binary Black Hole Merger,”
Physical Review Letters, vol. 116, no. 6, Feb. 2016, doi:
https://doi.org/10.1103/physrevlett.116.061102.
