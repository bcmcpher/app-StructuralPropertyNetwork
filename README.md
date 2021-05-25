[![Abcdspec-compliant](https://img.shields.io/badge/ABCD_Spec-v1.1-green.svg)](https://github.com/brain-life/abcd-spec)
[![Run on Brainlife.io](https://img.shields.io/badge/Brainlife-bl.app.1-blue.svg)](https://doi.org/10.25663/bl.app.1)

# app-StructuralNetwork
This app uses the [[FiNE toolbox](https://github.com/bcmcpher/fine)] to take an input tractography and a labeled structural image to produce structural networks. It produces weighted networks using the most common streamline count metrics, including: 

<ul>
<li> count - the number of streamlines connecting each label 
<li> length - the average length of the streamlines connecting each label
<li> density - the number of streamlines connecting each label correcting for the size of the labels connected
<li> denlen - the number of streamlines connecting each label correcting for the size of the labels and normalized for length
</ul>

The networks are returned as adjacency matrices (conmat) and jsongraph (network) datatypes
 
### Author
- [Brent McPherson](bcmcpher@iu.edu)

### Contributors
- [Brent McPherson](bcmcpher@iu.edu)

#### Copyright (c) 2021 Brent McPherson, Indiana University

### Funding Acknowledgement
brainlife.io is publicly funded and for the sustainability of the project it is helpful to Acknowledge the use of the platform. We kindly ask that you acknowledge the funding below in your code and publications. Copy and past the following lines into your repository when using this code.

[![NSF-BCS-1734853](https://img.shields.io/badge/NSF_BCS-1734853-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1734853)
[![NSF-BCS-1636893](https://img.shields.io/badge/NSF_BCS-1636893-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1636893)
[![NSF-ACI-1916518](https://img.shields.io/badge/NSF_ACI-1916518-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1916518)
[![NSF-IIS-1912270](https://img.shields.io/badge/NSF_IIS-1912270-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1912270)
[![NIH-NIBIB-R01EB029272](https://img.shields.io/badge/NIH_NIBIB-R01EB029272-green.svg)](https://grantome.com/grant/NIH/R01-EB029272-01)
[![NIH-5T32MH103213-05](https://img.shields/io/badge/NIH_5T32MH103213-05-green.svg)](https://grantome.com/grant/NIH/5T32MH103213-05)

### Citations
We ask that you the following articles when publishing papers that used data, code or other resources created by the brainlife.io community.

1. Avesani, P., McPherson, B., Hayashi, S. et al. The open diffusion data derivatives, brain data upcycling via integrated publishing of derivatives and reproducible open cloud services. Sci Data 6, 69 (2019). [https://doi.org/10.1038/s41597-019-0073-y](https://doi.org/10.1038/s41597-019-0073-y)

### Local usage for the App:

To run locally, modify the config.json.example so the input fields that map to files (i.e. have a path to an input) point to the files on your local system you want to run. 

### Usage of the App on brainlife.io
When an App is requested to run on brainlife.io, the platform will do the following:

<ol>
<li> Stage the code inside this git repo on a computing resource.
<li> Stage the input data requested to run the App on.
<li> Create a config.json in the same working directory of the App and Data in the computing resource.
</ol>

The config.json file contains the parameters and the path to the input data needed for the App to run. The App paramters are set by the brainlife.io users interface when the App is called and saved inside the config.json. The input data (a T1w nifti file in this case) is selected by the user during the process of requesting the App on brainlife.io 

Running the App on brainlife.io really means "execute this main.m script on a computing resource." 

You can submit this App online at [https://doi.org/10.25663/bl.app.???](https://doi.org/10.25663/bl.app.???) via the "Execute" tab.
