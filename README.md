CMB Summer School - UT Austin 2024
==================================

Authors: Nick Galitzki, Subhajit Ghosh, Vivian Sabla, Elle Shaw

Here are lectures and notebooks prepared for a CMB Analysis Summer School, hosted at the University of Texas at Austin on May 7-10, 2024. Our notebooks and files, 
contained in `UT_Notebooks`, are based on the CMB-S4 CMB Summer School notebooks written by Jeff McMahon and Rene Hlozek (found at [https://github.com/jeffmcm1977/CMBAnalysis_SummerSchool](https://github.com/jeffmcm1977/CMBAnalysis_SummerSchool)). 

Before May 7th
--------------
Before the UT Summer School begins, we ask that all participants install the notebooks and necessary software so we can work out any installation problems outside of our valuable course schedule. We also ask that all participants work through the `Day0_FFT_intro_CMB_School.ipynb` Jupyter notebook which provides a brief introduction to Fourier Transforms, an integral mathematical concept for understanding the CMB and the work to be done in this school. Please follow the installation instructions below to install all necessary notebooks and software on your local machine. 

Installation and Setup
----------------------
We have provided a conda environment defined in CMBSchool_environment.yml which provides an easy set up of a virtual environment with all the dependencies installed in order to run the notebooks needed for this summer school. This however requires `conda` to be installed on your local machine. Instructions for installation on different operating systems can be found here: [Conda Installation](https://docs.conda.io/projects/conda/en/stable/user-guide/getting-started.html).

From the command line... 

1. Clone this repository with the command
   
   `git clone https://github.com/TexMExLab/UTAustin_CMBSummerSchool.git`

   or manually download the repository to your local machine, and naviagate to the `UTAustin_CMBSummerSchool` directory. 

2. Within the `UTAustin_CMBSummerSchool` directory, create the virtual environment via 

   `conda env create --file CMBSchool_environment.yml -n CMBSchool`

3. Activate your new environment

   `conda activate CMBSchool`
   
4. Add this environment to your Jupyter kernel

   `python -m ipykernel install --user --name=CMBSchool`

   Note: this step may not be necessary, but different machines behave differently and it doesn't hurt.

6. Open the Jupyter notebook `Day0_FFT_intro_CMB_School.ipynb` in the `UT_Notebooks` directory and run the cells under the "Necessary packages for UT CMB Summer School" heading. If all the cells evaluate without an error, you've successfully installed everything!
   * If any package does not properly import, try to install it directly from its source (google is your friend here). For problems importing `class`, `pyactlike`, or `cobaya`, please reach out to the summer school organizers directly as the installation can be more involved. 
   * Note: open the Jupyter notebooks in whatever way you like, i.e. via the command line by running `jupyter notebook` or through a code editor like [VSCode](https://code.visualstudio.com). If you have no experience with Jupyter notebooks, please contact the summer school organizers prior to the school.

**If you get stuck on any part of the installation process, please reach out to the summer school organizers for help!**

Repository Organization
----------------------

`UT_Notebooks`: Contains the Jupyter notebooks we will go through in the workbook sessions of this summer school. 
`Presentations`: Contains the slides for talks given in this summer school.
`CMB-S4_AnalysisSummerSchool`: A clone of the CMB-S4 Summer School notebooks that our school is based on. These are for the interested participant who may want to do more extended self study after the UT summer school concludes.
