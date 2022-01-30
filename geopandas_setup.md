*activate python 3.8

## setup virtualenv
`python -m venv ./<env_name>`

activate environment in terminal
windows cmd `venv\Scripts\activate`
bash  `source venv/bin/activate`



export environment `pip freeze > geopandas_req.txt`


## Finding the right wheel file
there are issues with gdal and fiona installing properly on with pip alone and a lot of people find it easier to install the wheel files. This is when you bipass pip making the descision on which version to choose and you choose the version yourself. this is not a great practice to always do, but is very useful in this situation.

### where to find wheel files
https://www.lfd.uci.edu/~gohlke/pythonlibs/

## needed libraries for installing geopandas (install in this order)
1. [gdal](https://www.lfd.uci.edu/~gohlke/pythonlibs/#gdal)
2. [fiona](https://www.lfd.uci.edu/~gohlke/pythonlibs/#fiona)
3. pyproj
4. rtree
5. shapely
6. geopandas

### install commands for windows
`pip install .\wheel\GDAL-3.4.1-cp38-cp38-win_amd64.whl`
`pip install .\wheel\Fiona-1.8.20-cp38-cp38-win_amd64.whl`
`pip install pyproj rtree shapely geopandas`

*osx and linux do not have as hard of a time with installing geopandas and its dependencies. simply try `pip3 install geopandas`

