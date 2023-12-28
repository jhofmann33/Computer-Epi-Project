#README for Code files

Packages used throughout the code:

Python:
- pip install pandas
- pip install xlrd
- pip install numpy
- pip install DateTime
- pip install 
- pip install matplotlib
- pip install statsmodels
- pip install scikit-learn
- pip install tensorflow
- pip install tensorflow keras

R:
- writexl
- readxl
- dplyr


To keep the file upload size small we ommited some models and datasets from the final submission.
If interested in running a specific script we will include links to Jordan's GitHub for the relavent datasets
to download and test the code. Since these are mostly Juypter notebook files alot of the models should be embedded with the 
scripts submitted.

Emperical Directory Guide:
The emperical directory is divided into the three subset country folders (China, Sweden, United States)
The following files should be in each directory:

Policy_Influenza_Covid_{Country Name}.ipynb
These models are represenative of quantifying different policies, and creating the cumulative influenza, policy, 
and Covid model.

Subset_Models_Covid_{Country Name}.ipynb
These are emperical covid models that were created.

Subset_Models_Influenza_{Country Name}.ipynb
These are the emperical Influenza models that were created.


Forecasting Directory Guide:
For the forecasting scripts they are again divied into the subset countries within the directory. We reccommend running the US
to get started since it is has markdown with the code to walk through the process and what each snippet means. Again we will attach
links to the other data sets used if initerested in running the other forecasting models. The US model along with the other forecast
models will output a forects excel sheet that can be used with the analysis code.

IMPORTANT NOTE:
Befoe running this model YOU MUST ensure that all kernel's are shut down. If there are kernels still running in the notbook the code
will not compile and will error out as soon as training beggins. If you are using Juypter notebook to test the code there is a 
shut down all kernels button. I'm not sure if this is a bug with tensorflow, and have never had this issue with pyTorch.


Merging Directory Guide:

- addPopulationData.R
This is a R code script to append the population a country to the end of every row in an excel file. 
This will only compare against the "Country" column, so data and code will not matter, 
but consistency of Country Names is vital. 

- DataSplice.ipynb
This splicing is for taking weekly reported Influenza data and averaging it into daily. 
This is important since policies are daily decisions and we need to capture changes within weeks.

- Covid_DataSplice.ipynb 
This is a slight variation of DataSpice.ipynb for the Covid data set.

- reSplice.R
This takes the raw influenza data that has various rows of the same data for various recording 
means and combines them into proper totals. This gives us one total per day for each country.

- setMerging.ipynb
The most important code, setMerging combines data sets that have matching information. 
When iterated for all of our data sets we are left with the final set where all fields have values. This is then used for the analysis phase.