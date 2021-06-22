# streamflow_depletion_metrics

Changing precipitation patterns and increasing human reliance on groundwater resources drive changes in streamflow patterns and persistence. 
While streamflow depletion has wide-ranging effects for aquatic ecosystems and human populations, detecting and predicting the impacts of
streamflow depletion can be very difficult. Several low-flow metrics have been used in management to assess potential impacts of groundwater
withdrawals on streamflow, but the ecohydrological indicators most sensitive to groundwater withdrawals have not yet been identified. The code 
and data included in this repository constitute a comprehensive exploration of how stream hydrographs and thermographs respond to 
groundwater withdrawals, as measured by a suite of ecohydrological indicators. For a full description of methods and results, see 
REFERENCE TO UNPUBLISHED STUDY.

Programs included in this repository include:

- find_stations.ipynb: a jupyter notebook that identifies the set of GAGESII stations with continuous long-term stream temperature monitoring.

- end-member-thermo-model.ipynb: a jupyter notebook that evaluates the performance of an end-member mixing model for stream
temperature at GAGESII sites with at least 15 years of continuous stream temperature modeling. Hydrograph separation is performed
using the method described by Eckhardt (2005) as implemented in the [hydro python package](https://github.com/hydrogeog/hydro). Groundwater 
temperature is modeled as a 120-day rolling average of air temperature (min daily air temperature in the summer, max daily air temperature in the winter)
using [Gridmet data](http://www.climatologylab.org/gridmet.html) (Abatzoglou, 2013). Maximum (minimum) surface water temperature is modeled as 
maximum (minimum) daily air temeprature. Mean surface water temperature is modeled as the 2-day rolling mean of the daily mean air temperature.

# References
Abatzoglou, J. T. (2013), Development of gridded surface meteorological data for ecological applications and modelling. Int. J. Climatol., 33: 121–131.

Eckhardt, Klaus. "How to construct recursive digital filters for baseflow separation." Hydrological Processes: An International Journal 19.2 (2005): 507-515.
