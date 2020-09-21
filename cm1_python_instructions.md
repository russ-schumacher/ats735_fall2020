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

Now we will set up an environment with the packages we need to have installed. This should be a fairly short list for what's really needed, but you may also want to add more.  A simple environment that should work is something like:

`conda create -n ats735 -c conda-forge xarray netcdf4 numpy scipy matplotlib pandas=1.0.5`

(xarray doesn't play nice with the latest versions of pandas, so we'll install a slightly older one just to be safe.)

- Run the command `conda activate ats735` to activate the unidata environment and verify that everything is ready.  (It may ask you to do something like `conda init bash`, if so then do that first.)


