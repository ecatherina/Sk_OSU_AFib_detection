# Atrial Fibrillation Drivers detection
A Python code for Master Thesis "Multi-modal Machine Learning Toolset for Spatio-Temporal
Characterization of Atrial Fibrillation Drivers in Human Heart"

## Requirements
- [Anaconda](https://www.anaconda.com/download/)
- plotly 


## Dataset

The dataset is the unregistered raw data from an explanted hearts affected by the atrial fibrillation. Data is provided by Dr.V.Fedorov team from the Department of Physiology and Cell Biology, The Ohio State University, Wexner Medical Center, USA. Human intact atrial preparations were mapped by dual-sided near-infrared optical mapping (NIOM) and by multi-electrode mapping (MEM) during sustained AF episodes. Data were divided into three classes: driver, nondriver and noise. 

Dataset has 27 dataframes with 1728 MEM recordings and 511 NIOM recordings in total with a duration from 8 to 18 seconds. Each dataframe contains 64 MEM recordings and the same or less number of corresponding NIOM recordings. 


## Usage

### Feature generation 
```
python Spectrum creation.ipynb

optional arguments:
--lowcut, highcut                   cutoff frequencies for Butterworth digital filter, default {4, 20}
```
Create spectrums of MEM and NIOM recordings 

```
python Feature generation.ipynb
```
Create spectral features of MEM and NIOM recordings, such as dominant frequencies, height, width, prominence of highest peaks  


### Visualization
```
python Visualization/Spectrum widget.ipynb
```
Plot spectrums

```
python Visualization/Spectrum widget 2.0.ipynb
```
Plot spectrums and raw MEM signal, requires plotly library


### Classification
```
python ML/SVM.ipynb
```






