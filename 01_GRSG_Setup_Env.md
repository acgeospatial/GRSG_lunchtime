# Setup a virtual environment with basic Geo components

This guide is for a windows 10 installation and assumes that the user has installed anaconda prior. For more detailed context please see my website https://www.acgeospatial.co.uk/python-geospatial-workflows-prt1-anaconda/


## A useful link
https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html

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


