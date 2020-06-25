# NIST-Fluid-Thermodynamic-State-Models
Repository for various thermodynamic property models of common saturated fluids obtained from the NIST Thermophysical Properties of 
Fluid Systems Database (https://webbook.nist.gov/chemistry/fluid/). Files are available for select properties of the liquid and vapor
phases as functions of saturation pressure. All units are SI. 

Currently, only models for saturated water are available. Properties that have been modeled for each phase as a function of pressure
are specific volume, enthalpy, the first derivative of specific volume with respect to saturation pressure, and the first derivative
of enthalpy with respect to saturation pressure. Power fit models are available as MATLAB function handles in .mat format and are valid for
pressures below 1 MPa. Data points used to create the models are discrete and are taken at the smallest resolution available from NIST, 
which is 1.666 kPa. For the derivatives of properties with respect to pressure, N - 1 centered finite differences are taken from the N
data points, and then a power fit is applied to these finite differences. It should be evident that some additional errors accumulate
in both taking finite differences and applying a regression fit, but the power fit models are still sufficiently accurate for most
applications. Where appropriate, plots comparing the raw data with the power fits are shown.

For pressures larger than 1 MPa, you can take advantage of look-up tables, which are available in .mat and .csv format. 
