# PV-modelling
<p align="center"><a href="https://twinsolar.eu/"><img src="https://twinsolar.eu/wp-content/uploads/2023/03/logo_twinsolar_seul.png" width="200"></a></p>

## PV_production.ipynb
Jupyter notebook containing a script to simulate a PV plant operation using PV modules and inverter data from their technical sheets. Based on pvlib package (https://pvlib-python.readthedocs.io/en/stable/#).

## Custom-cec-modules.csv and Custom-cec-Inverters.csv
Files with the technical specifications of modules and inverters with the CEC format. For the modules, only the data available on the manufacturer's technical sheet are needed. The remaining data (Il, I0, Rs, Rsh, etc.)  will be generated by the code. For the inverters, unfortunatly pvlib does not provide a function to derive the efficiency curve parameters (CO, C1, etc.) from the manufacturer's data sheet. The best way is to select a inverter from the same brand within the CEC database (available in pvlib) and to modify the AC/DC rated/maximum power, voltage and intensity.

## Meteo_Terre_Sainte_2022_10min.txt
A weather file with at least: global horizontal (GHI), diffuse horizontal (DHI) and direct nomal (DNI) irradiances, air temperature and wind speed. With coarse-grained data, timestamping should be done in the middle of the recording period. For example, if we assume an hourly record covering the time slot ranging from 10am to 11am, timestamp must be 10:30am.
