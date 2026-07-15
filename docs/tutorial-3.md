# Analysing results from your gyre experiments

In this page, we show some results to compare how the eddy parameterisations can alter the gyre simulations. 
All the plots shown on this page have been generated using a python jupyter notebook (available in the _scripts_ folder of this repository).


## Setting up the Python environment
To run it without trouble, you will probably need to install a suite of python libraries. 
We thus provide a **GYRE_PISCES_eddy.yml** file in the _scripts_ folder. Make sure that you have cloned this demonstrator to your local machine to access this file and the python run script.

To create your environment, use conda (it can take some time):
```
conda env create --file GYRE_PISCES_eddy_demo.yml
```
Then load it:
```
conda activate GYRE_PISCES_eddy_demo
```

Before you run the python script, edit the path to point to your demo configuration directory:
```
# Absolute paths to the configuration
nemo_path = '/home/YOUR_PATH/nemo_5.0.2/'
config    = 'GYRE_DEMO'
```

Now run:
```
jupyter notebook GYRE_PISCES-eddy-postprocessing.ipynb
```

## Results overview

![alt_text](./imgs/temperature_ts.png)
__Figure:__ Evolution of the domain-avergaed temperature during our experiments.
<br>

![alt text](./imgs/Barotropic_streamfunction_map.png)
__Figure:__ Barotropic stream function in EXPCTRL (left), EXPEIV (middle) and EXPGEOM (right). 
<br>

![alt_text](./imgs/MLDmax_map.png)
__Figure:__ Annual maximum of the mixed layer depth (MLD) in EXPCTRL (left), EXPEIV (middle) and EXPGEOM (right). 
<br>

<p align="center">
  <img src="imgs/NO3_profile.png" alt="drawing" style="width:300px;"/>
</p>

__Figure:__ Averaged profiles of nitrogen (NO$$_3^{-1}$$) in EXPCTRL (blue), EXPEIV (orange) and EXPGEOM (green). 
<br>

<p align="center">
  <img src="imgs/EXPGEOM_Eddy-Energy.png" alt="drawing" style="width:300px;"/>
</p>

__Figure:__ Parameterised eddy energy in EXPGEOM.
<br>

## Summary

In this last page, we have shown few results from our numerical experiments that can be used to compare mesoscale parameterisation. 
It is worthnoting that in the gyre configuration, the circulation is mostly driven by the analytical atmospheric forcings and is therefore not really sensitive to changes in the mesoscale parameterisations. 
However, concentration of bio-geo-chemical matters can be altered by the parameterisations of mesoscale transport on longer timescale.
in this tutorial you have learn how to set-up a numerical protocol in NEMO5 which can be used with longer simulations or other configurations.
