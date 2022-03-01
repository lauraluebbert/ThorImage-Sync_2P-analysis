# ThorImage/ThorSync_2P-analysis
[![DOI](https://zenodo.org/badge/275931002.svg)](https://zenodo.org/badge/latestdoi/275931002)
Notebook to synchronize and analyze ThorImage + ThorSync 2-photon calcium imaging data with light stimulation.  

The notebook requires the user to draw ROIs as described [here](https://github.com/lauraluebbert/confocal_z-stack_analysis/blob/master/README.md). The ROIs are drawn on an automatically computed sum projection. The stimulation information is automatically obtained from the ThorSync file.

# Output returned by notebook:

### 1. Dataframe containing information per frame in the format:

Channel + Sample	 | Filename	        | Frame	|Mean pixel value in ROI | Mean pixel value in bkg area |	Norm_mean_pixel_value_in_ROI |	Time passed (s) |	dF/F0	| LED (ON/OFF)|
-------------------|------------------|-------|------------------------|------------------------------|------------------------------|------------------|-------|-------------|
ChanA (001_001_001)| ChanA_001_001_001|	1.0	  |542.6812468577175	     | 541.7430997876858	          |0.9381470700317323.           |	0.0             |	0.95  |	0           |
. . .              | . . .            |	. . . |. . .	                 | . . .	                      |. . .	                       |	. . .           |	. . .	| . . .       |

### 2. Pickled dictionary containing raw and analyzed data, including ROI coordinates

### 3. dF/F0 over time showing stimulation:
![R72A10-Chrimson_R52G12-GCaMP5_i003_df-f0](https://user-images.githubusercontent.com/56094636/156092081-a81363a3-789d-4090-9104-e7ad5bd791df.png)
The notebook also returns raw mean and background normalized mean traces.

### 4. dF/F0 heatmap (sum over all frames):
![2020-11-13_R70H05GCaMP_R72A10Chrim+ATR_thor6_df-f0_heatmap](https://user-images.githubusercontent.com/56094636/156091730-463c4883-5d9b-494a-944d-a6a562c62710.png)

### 5. dF/F0 heatmap movie over time showing stimulation

### 6. Raw and background normalized mean fluorescence graph showing stimulation:
![2020-11-13_R70H05GCaMP_R72A10Chrim+ATR_thor6_bkg-norm-mean-fluorescence](https://user-images.githubusercontent.com/56094636/156091390-bb15c02f-ba78-44c3-96ef-40e34fdb2bc6.png)

### 7. ROIs drawn for area of interest and background:
![2020-11-13_R70H05GCaMP_R72A10Chrim+ATR_thor6_rois_0](https://user-images.githubusercontent.com/56094636/156091221-d2ebeef5-7a64-40b5-a63c-8d4f2858223c.png)
![2020-11-13_R70H05GCaMP_R72A10Chrim+ATR_thor6_bkg_rois_0](https://user-images.githubusercontent.com/56094636/156091196-315b928f-a331-4093-9131-3eda1ace2a77.png)

Written by Laura Luebbert for use in the Lois lab at Caltech.  
