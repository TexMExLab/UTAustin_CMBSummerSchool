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
   * If any package does not properly import, try to install it directly from its source (google is your friend here). For problems importing `CLASS`, `pyactlike`, or `cobaya`, please reach out to the summer school organizers directly as the installation can be more involved. 
   * Note: open the Jupyter notebooks in whatever way you like, i.e. via the command line by running `jupyter notebook` or through a code editor like [VSCode](https://code.visualstudio.com). If you have no experience with Jupyter notebooks, please contact the summer school organizers prior to the school.

**If you get stuck on any part of the installation process, please reach out to the summer school organizers for help!**

### Mac OS Recommendations

If you run into problems installing `pyactlike` through the provided conda environment, try a manual installation, described below. 

1. Within the `UTAustin_CMBSummerSchool` directory, clone the `pyactlike` repository:

   `git clone https://github.com/ACTCollaboration/pyactlike`
   
3. Manually install the code with the commands
   ```
   cd pyactlike
   python setup.py install
   pip install . --user
   ```

Similarly `CLASS` may need to be manually compiled and installed. Detailed instructions can be found on the [CLASS Wiki](https://github.com/lesgourg/class_public/wiki/Installation). We outline them below:

1. Within the `UTAustin_CMBSummerSchool` directory, clone the `CLASS` repository:

   `git clone https://github.com/lesgourg/class_public.git class`

2. Compile the main code
   ```
   cd class
   make
   ```
   The `make` command is set to create the class executable, the library `libclass.a`, and the Python wrapper `classy` which is what we will be using. Don't worry if the compilation returns lines a few lines of warning, this is normal. You can test the installation with the command `./class explanatory.ini`. The first line should start with `Running CLASS version ...` and the last line by `Writing output files in ....` If this worked, you can test that the Python wrapper was also compiled successfully by trying
   ```
   python
   >>> import classy
   >>> exit()
   ```
   If python does not complain with the `import classy` command, your installation was successful. If unsuccessful you can peruse some of the likely compilation issues on the  [CLASS Wiki](https://github.com/lesgourg/class_public/wiki/Installation) or reach out to one of the Summer School organizers for assistance. 

_Tips from personal experience:_ The most typical problem with installing `CLASS` on a Mac is the C-compiler being used. There is a dedicated section on the CLASS Wiki for fixing this problem. 

### Windows Recommendations

* Install Anaconda https://www.anaconda.com/download
* Open the CMB school notebooks using Jupyter Lab or Jupyter applications on Anaconda navigator. (Jupyter Lab allows many notebooks to be open at once on a single browser tab.)

Windows does not have a built in command line (this is very annoying!!). You can run most of the command line prompts specificed for the Mac installation directly in a Jupyter notebook cell by placing and exlcamation point in front of the command (ex: `!pip install pyactlike`). This trick will allow you to install certain packages which may not have been successfully installed through the provided environment. 

In troubleshooting our environment on Windows we found that many of the python packages were not properly installed with the activation of the environment but could easily be installed directly in a Jupyter notebook. Once in the `Day0_FFT_intro_CMB_School.ipynb` notebook, if you get an import error on any of the packages, your first step should be to try to manually `pip` install the package through the command line in the Jupyter notebook. For example, if you receive a `numpy` import error, create a new cell in the Jupyter notebook and execute the command

`!pip install numpy`

This should work seamlessly for `matplotlib`, `pylab`, `numpy`, `scipy`, `astropy`, `cobaya`, `getdist`, and `pyactlike`. However if you have an issue with `classy` please just immediately reach out to the Summer School organziers - we're still working on a proper fix for this. 

Repository Organization
----------------------

* `UT_Notebooks`: Contains the Jupyter notebooks we will go through in the workbook sessions of this summer school. 
* `Presentations`: Contains the slides for talks given in this summer school.
* `CMB-S4_AnalysisSummerSchool`: A clone of the CMB-S4 Summer School notebooks that our school is based on. These are for the interested participant who may want to do more extended self study after the UT summer school concludes.
