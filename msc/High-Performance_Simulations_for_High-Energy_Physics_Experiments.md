The role of simulation and synthetic data generation for High-Energy Physics (HEP) 
research is profound. While there are physics-accurate simulation frameworks available to 
provide the most realistic data syntheses, these tools are computationally demanding. 
Additionally, the output from physics-accurate simulations is hard to comprehend, hard to 
manipulate and difficult to work with, as the data is rather close to the real case. 
These simulations consider accurate models of real-world detectors, which is another 
limitation.

Parametric and complexity-aware simulation frameworks on the other hand, can redefine the 
complexity space in drastically simplified terms and generate complexity-reduced data 
sets. It is also possible to consider a variety of detector models for these simulations. 
The applications of complexity-reduced simulations and data are numerous. We will be 
focusing on the role of such data as an enabler for Machine Learning (ML) model design 
research.

This project aims to extend REDVID simulation framework [1] [2] through addition of new 
features. With additional features, the user can configure REDVID for generation of data 
at various levels of complexity, i.e., how synthetic or real the data is.

> The main improvement considered for this project is the addition of a time dimension [3] 
to simulations. As particles go through different detector layer, their interaction is 
recorded. Future upgrades to LHC will provide collection of timestamps for specific 
detector layers.
>
> There may be other minor improvements required to support implementation of the time 
dimension. The time dimension will allow for so called 4-dimensional tracking. The 
student will test the impact of timing information on developed ML models.

The project is part of an ongoing effort to train and test ML models for particle track 
reconstruction for the HL-LHC. The improved version of REDVID can be used by the student 
and other users to generate training data for ML models.

Bonus: The student will be encouraged and supported to publish the output of this study 
in a relevant journal, such as "Data in Brief" by Elsevier.

Get in touch with your [potential future supervisors](mailto:u.odyurt@utwente.nl,v.zaytsev@utwente.nl) to discuss details!

### Appendix - Terminology

The terminology for the considered simulations and its features is domain-specific and 
are explained below:
- Synthetic data: Data generated during a simulation, which resembles real-data to 
  limited extent.
- Physics-accurate simulation: A type of simulation that strongly takes into account 
  real-world physical interactions and utilises physics formulas to achieve this.
- Complexity-aware simulation framework: A simulator which can be configured with 
  different levels of simulation complexity, making the simulation closer or further away 
  from the real-world case.
- Complexity-reduced data set: Simplified data resulting from simplified simulations. 
  This is in comparison to real data, or data generated by physics-accurate simulations.

### References

[1] U. Odyurt et al. 2023. "Reduced Simulations for High-Energy Physics, a Middle Ground 
    for Data-Driven Physics Research". 
    URL: https://doi.org/10.48550/arXiv.2309.03780

[2] U. Odyurt. 2023. "REDVID Simulation Framework". 
    URL: https://virtualdetector.com/redvid

[3] ATLAS collaboration. 2020. "Technical Design Report: A High-Granularity Timing 
    Detector for the ATLAS Phase-II Upgrade". 
    URL: https://cds.cern.ch/record/2719855
