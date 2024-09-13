# OCEAN
Framework for regular habitat suitability predictions based on Environmental Niche Models

![image](https://github.com/user-attachments/assets/ebb539f6-f9a5-45b5-9660-c3d7572294b2)

This repository contains code in R to develop and operationalize regular predictions of habitats with high probability of whale [or any other organism] occurrence.

NOTICE: The code is still under development and annotation is underway. It is assumed that users are familiar with statistical modelling of animal distributions.

The code presented here is intended to illustrate how to produce regular predictions based on an Environmental Niche Model (aka Species Distribution Model) and export the predictions to an external server.
The code is developed in the scope of Work Package 4 of the project OCEAN funded by the European Union’s Horizon Europe research and innovation programme (grant agreement No.101076983). Detailed information about project OCEAN's goals and results can be found in https://ocean-navigation-awareness.eu.

The work in project OCEAN's Work Package 4 is tailored at reducing risk of ship collision with marine mammals (namely large whales) by providing mariners with up-to-date information about risk along their routes. Different strategies are used to identify risk areas based on three approaches: 1) identification of suitable habitat for animal occurrence; 2) voluntary reporting of visual detections; and 3) passive acoustic monitoring (PAM) of acoustically active animals.

The code in this repository supports the first approach (identification of suitable habitat for animal occurrence), using the sperm whale (_Physeter macrocephalus_) in the Azores archipelago (Portugal) as a study case. In the scope of the work developed in Task 4.2 of the OCEAN project a Generalized Additive Model (GAM) was fitted to sightings per unit effort from data obtained by the Azores Fisheries Observer Program (https://www.popaobserver.org). The model fitting approach is documented in GAMmodelDOM.txt. Nevertheless, the framework is independent from modelling approach.

The code enables producing predictions as raster files and converting rasters to polygons based on a threshold, in order to comply with current maritime communication standards. The code also contains a routine to communicate with the European Navigational Hazard Infrastructure also developed by the OCEAN Project.

The tasks performed by the different routines are illustrated below

![image](https://github.com/user-attachments/assets/1a9e0e65-273d-4838-ba06-887315d6a397)

The routines include code to:

- Fit Generalized Linear Models and test model performance
- Obtain and prepare [predictive] covariates from an external data server using an API
- Create predictive maps in raster format on a regular basis [daily]
- Use a threshold to produce polygons from the raster maps and clean polygons delete a certain size
- Export polygons to an external data server [European Navigational Hazard Infrastructure] using an API 


![image](https://github.com/user-attachments/assets/e0ff0b71-6f24-494e-8af1-ef0d2761c065)

Project OCEAN received funding from the European Union’s Horizon Europe research and innovation programme under grant agreement No.101076983. UK participants in Project OCEAN are supported by UKRI grant numbers 10038659 (Lloyds Register) and 10052942 (The Nautical Institute).
