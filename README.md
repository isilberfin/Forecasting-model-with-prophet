# Forecasting model with prophet
Forecasting model built with Facebook's prophet algorithm on IBB's monthly water consumption in Istanbul dataset (cubic meters)

Data is taken from [İBB AÇIK VERİ PORTALI](https://data.ibb.gov.tr/) 

In order to use Prophet there are things to consider: 

1. Prophet works only for Python < 3.9 so a virtual environment with python 3.8 is recommended. 
```
conda create -n time_series_venv python=3.8
```

2. Activating
```
conda activate time_series
```

3. Other thing to consider is prophet requires  C++ compiler
```
conda install libpython m2w64-toolchain -c msys2
```

4. Now we can move on with installing libraries and dependencies
```
conda install numpy cython -c conda-forge
conda install matplotlib scipy pandas -c conda-forge
conda install pystan -c conda-forge
conda install -c anaconda ephem
```
```
!pip install pystan fbprophet
from fbprophet import Prophet
```
   In the documentation it is clearly stated that the model works better with daily data, but since in this project data we have is monthly, I have used the code accordingly.
   
   Resources
   
   1.https://facebook.github.io/prophet/docs/non-daily_data.html
   
   2.https://medium.com/data-folks-indonesia/installing-fbprophet-prophet-for-time-series-forecasting-in-jupyter-notebook-7de6db09f93e
   
   3.https://data.ibb.gov.tr
