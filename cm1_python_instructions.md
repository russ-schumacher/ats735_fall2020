# Instructions for plotting CM1 output in python

## Installing python via miniconda
First, let's install the miniconda version of python.  (If you already have miniconda or anaconda installed on the computer you want to use, you can skip this step.)  Following the instructions used in the [Unidata python workshop](https://unidata.github.io/python-training/):

### Mac/Linux

- Download the [Miniconda bash installer](http://conda.pydata.org/miniconda.html).

- After downloading the bash installer, open a command prompt (terminal program on the Mac).

- Change the directory at the terminal to wherever the installer was downloaded. On most systems, this will default to the downloads directory in your user account. If that’s the case, `cd ~/Downloads` will get you there, or replace the path with wherever you saved the file.

- Run the installer script by typing `bash Miniconda3-latest-MacOSX-x86_64.sh`. Note: Your file name may be different depending upon your operating system! replace `Miniconda3-latest-MacOSX-x86_64.sh` with whatever the name of the file you downloaded was.

- Accept the defaults.

- After the installer has completed completely close and restart your terminal program (this sources the newly modified path).

- If bash isn't your default shell, switch to it by running the command bash.

- Verify that your install is working by running `conda --version`. You should see a response like `conda 4.8.0` or similar (though yours may be a slightly different version number).

## Setting up your environment

Now we will set up an environment with the packages we need to have installed. This should be a fairly short list for what's really needed, but you may also want to add more.  If you already have a working environment that has all of these packages, then you can just use that. A simple environment, named ats735, that should work is something like:

`conda create -n ats735 -c conda-forge xarray netcdf4 numpy scipy matplotlib pandas=1.0.5 jupyter`

(xarray doesn't play nice with the latest versions of pandas, so we'll install a slightly older one just to be safe.)  You can name your environment something other than "ats735" if you want.

- Run the command `conda activate ats735` to activate the unidata environment and verify that everything is ready.  (It may ask you to do something like `conda init bash`, if so then do that first.)

- If you find you want/need additional packages, you can install them with (for example):

`conda install -c conda-forge <package name>`


## Opening and running a jupyter notebook

There are different ways you can run and interact with python, but a great way to get started is with Jupyter notebooks.  They allow for you to write and test your code in a really user-friendly way. (People tried to sell them on me and I resisted for a long time, but once I started using them, now it's my favorite way to test out new code.)

- At the terminal, `cd` into whatever directory you want to work out of (this might be the directory where your model output is located, or one directory up from there)

- if you haven't, run `conda activate ats735` to activate the environment.

- I've put an example notebook for loading and plotting CM1 output [here](cm1_plots_examples.ipynb); download this file to the directory you're working from.

- Now, open Jupyter Lab, by simply running `jupyter lab`. This will open a new browser tab with Jupyter Lab in it. Or you can also simply use `jupyter notebook` if you prefer.

- Click on 'Python3' to launch the python kernel.

- Open up the `cm1_plots_examples.ipynb` notebook (double-click it from the menu) -- this will give you a feel for what a notebook looks like and how it works.

- Walk through the steps in this notebook (Hint: you can run the code in cells using `shift-R`, or using the "play button" at the top) and hopefully you will generate some plots that look roughly like the ones I've been showing in class.  If so, congratulations, you're well on your way!  

- As you go, you might want to save your notebook by clicking the 'save' button in the upper left.

- Now spend a little time experimenting with the code in this notebook, to get a sense for some of the options (for example, try changing the contour intervals, or the map boundaries, or the vertical level shown, etc.)

- You may want to learn more about notebooks and how they work: a good resource is the Unidata training at [https://unidata.github.io/python-training/workshop/Jupyter_Notebooks/jupyter-notebooks-introduction/](https://unidata.github.io/python-training/workshop/Jupyter_Notebooks/jupyter-notebooks-introduction/)

- When you're done with JupyterLab, simply go under the File menu and select "Shut down".  Once this happens, you can close that browser window.


