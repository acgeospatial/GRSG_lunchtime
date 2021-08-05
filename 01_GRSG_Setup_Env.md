# Setup a virtual environment with basic Geo components

https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html

conda create -n geo python=3.7.7

activate geo

conda install -c conda-forge gdal

conda install -c conda-forge geopandas

pip uninstall rtree

conda install -c conda-forge matplotlib

conda install -c anaconda ipykernel

python -m ipykernel install --user --name=geo

pip install rtree
