# Setup a virtual environment with basic Geo components

This guide is for a windows 10 installation and assumes that the user has installed anaconda prior. For more detailed context please see my website https://www.acgeospatial.co.uk/python-geospatial-workflows-prt1-anaconda/

## Download and install anaconda fom here
https://www.anaconda.com/products/individual

## A useful link
https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html

------------------
## A digression
https://xkcd.com/1987/

https://www.python.org/downloads/

https://www.reddit.com/r/Python/comments/betkoj/why_use_anaconda/

-------------------

### Step 1
Open your anaconda prompt. Note the (base) part. This is your base environment. In this guide we will be creating a new virtual environment called 'grsg'

![alt text](https://github.com/acgeospatial/GRSG_lunchtime/blob/main/grsg_images/01_prompt.png)


### Step 2
Create a new Python 3.7.7 environment (you can change this if you wish to choose an alternative version)

`conda create -n grsg python=3.7.7`

when prompted type `y` for yes and follow on screen instructions as below:

![alt text](https://github.com/acgeospatial/GRSG_lunchtime/blob/main/grsg_images/02_prompt.png)

![alt text](https://github.com/acgeospatial/GRSG_lunchtime/blob/main/grsg_images/03_prompt.png)

![alt text](https://github.com/acgeospatial/GRSG_lunchtime/blob/main/grsg_images/04_prompt.png)

### Step 4
Activate the environment via

`conda activate grsg`

![alt text](https://github.com/acgeospatial/GRSG_lunchtime/blob/main/grsg_images/05_prompt.png)

You now have an activated virtual environment. Sometimes referred to as a venv

### Step 5
Install the required geospatial packages. It is perfectly resonable to run `conda install -c conda-forge gdal geopandas etc` as one line. For complete clarity I'm doing it package by package. Accept y where necessary.

`conda install -c conda-forge gdal`

`conda install -c conda-forge geopandas`

`pip uninstall rtree`

`conda install -c conda-forge matplotlib`

![alt text](https://github.com/acgeospatial/GRSG_lunchtime/blob/main/grsg_images/06_prompt.png)

when install finishes

![alt text](https://github.com/acgeospatial/GRSG_lunchtime/blob/main/grsg_images/07_prompt.png)

### Step 6
Getting Jupyter Notebook up and running

`conda install -c anaconda ipykernel`

`python -m ipykernel install --user --name=grsg`

`pip install rtree`

example

![alt text](https://github.com/acgeospatial/GRSG_lunchtime/blob/main/grsg_images/08_prompt.png)

### Step 7 
Additional libraries

`conda install -c conda-forge rasterio`

and whatever else you may need either now or the future

### Step 8
Testing

navigate to a working folder for your code or a root. In my case my root of d: drive

`d:`

use cd (change directory) if you need

and type 

`jupyter notebook`

![alt text](https://github.com/acgeospatial/GRSG_lunchtime/blob/main/grsg_images/09_prompt.png)

![alt text](https://github.com/acgeospatial/GRSG_lunchtime/blob/main/grsg_images/10_prompt.png)

sometimes... this does not work. If so try
`pip install jupyter`

you can check to see if it has installed by typing
`jupyter --version`

test to see if the libraries are installed correctly

`from osgeo import gdal
import geopandas as gpd
import rasterio`

with no errors you are all set

![alt text](https://github.com/acgeospatial/GRSG_lunchtime/blob/main/grsg_images/11_prompt.png)

## Removal in future (assuming grsg is the env name)

if you wish in the future to remove the kernel from Jupyter use the command
`jupyter kernelspec uninstall grsg`

if you wish to remove the venv at the conda prompt type
`conda env remove -n grsg`






