# South Pole Telescope

SPT-3G, the third generation camera on the South Pole Telescope (SPT), was 
deployed in the 2016-2017 Austral summer season. The SPT is a 10-meter 
telescope located at the geographic South Pole and designed for observations in 
the millimeter-wave and submillimeter-wave regions of the electromagnetic 
spectrum. The SPT is primarily used to study the cosmic microwave background 
(CMB). 

## Requirements

The upgraded camera produces an order of magnitude more data than the 
previous generations of SPT cameras. The telescope is expected to collect a 
petabyte (PB) of data over course of five years, which is a significantly 
larger data volume than any other CMB telescope in operation. The increase 
in data rate required radical changes to the SPT computing model both at the 
South Pole and University of Chicago. This paper will describe the overall 
integration of distributed storage and compute resources into a common 
interface, deployment of on-site data reduction and storage infrastructure, 
and the usage of the Open Science Grid (OSG) by the SPT collaboration.

Data requirements:

* ~ 150-200 TB of compressed raw data coming north every year in big boxes of 
hard drives 
* ~30 TB/year of reduced-rate data arriving continuously by satellite.

Computing Requirements:

* ~ 150 cores with 4 GB
* ~ 10M core hours

## Resources

SPT has two dedicated login nodes. These are used for user analysis and job 
submission to OSG. To facilitate user analysis, there are Jupyterhub instances 
running on each of the login nodes. 

In addition to the login nodes, there are two dedicated production resources: 
`spt-buffer` and `spt-mgmt`. `spt-buffer` is dedicated virtual machine that is 
required to retrieve the data via satellite from pole. United States Antarctic 
Program (USAP)  

## NERSC Backups

There is automated 