# AstronomicalDataProcessing2022
For Astronomical Data processing code and general setup guide

# How to setup the needed environments
For the course you'll need two seperate environments, one to contain Pynot and one for the rest of the course. This page will give an example on how to setup with windows and linux/mac. For general python usage and ease of setup in case you are new: 

- For windows I recommend using Anaconda navigator
- For mac/linux, you'll need a command terminal, your computer generally comes with it for mac, and if you are running linux, I presume you know what you are doing and just here for the code.

## Windows
The steps to setting up your environment in anaconda navigator are pretty simple:
- On the left side of your screen, click onto the tab called environments
- Here there should be a list of your environments and a tab showing all installed packages, if you are completely new, you'll likely only have the 'base' environment
- Above the list of environments hit the button 'New environment', give it a fitting name (For this course i named my environments 'ADP' and 'pynot') and wait until it is done setting up
- Once it is done setting up, left click the arrow next to the environment and open up a command terminal with that environment active
- At this point, you probably need to repeat the steps above if you have not made two environments yet.
- In the command terminal for your first environment, install the following packages:
    - scipy, sympy, ccdproc, astroquery, uncertainties, lmfit, imexam
    - This can be done via the command: pip install package_name
    - While some of these might work with conda install instead, pip have usually been the fastest way to get these installed.
    - Note on conda install: Not every package works with conda install or it needs a path specified.
- Now for pynot, again open the terminal with your second environment active.
    - Pynot has a tendency to break environments due to requiring older packages, this is why a seperate environment is made.
    - To install pynot you repeat the process from above, pip install pynot-redux, however the newest version can at times be unstable.
    - If the newest version doesn't work, uninstall pynot-redux and run pip install pynot-redux==999 to see availble versions, this will give an error.
    - From the list given by the error pick an earlier version and specify it in the command example: pip install pynot-redux==1.0.3
    - For windows last known (for me) working version is 0.2.22 on windows 10
Now for both environments you'll need an editor, i recommend Spyder, Jupyterlab or Jupyter Notebook, VS studio is another option, but i cannot provide a full guide to that as i don't use it, many of the same steps are applicable though.

## Linux/MAC
I work on a linux system currently, but previously had it on windows, here are the steps i used to getting my setup running.
For getting started on mac follow the installation guide on: https://docs.conda.io/projects/continuumio-conda/en/latest/user-guide/install/macos.html, once you have conda installed, the rest of the steps are applied in the same manner:
- Open your terminal
- To create your environments write: conda create --name ADP python=3.6 and when that is done conda create --name pynot python=3.6
- Then write: conda activate ADP
  - pip install package_name will install all the packages you need.
  - In case you skipped the windows section, these are the packages: scipy, sympy, ccdproc, astroquery, uncertainties, lmfit, imexam
  - Installing these should get you most basic packages you'll need
  - To deactivate the environment write conda deactivate
- For the second environment, conda activate pynot
  - Last known functional version as of writing this is 1.0.4 (current), to install the specific version: pip install pynot-redux==1.0.4
  - This will install dependancies and get your where you need to be, from this point on, be aware the pynot-redux is experimental and as such can change.
  - Once this is done, run conda install jupyter to get jupyter notebook. To launch Jupyter notebook with the environment activated simply write jupyter notebook
