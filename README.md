# BioComputerObject
## This document is for my Summer Internship with Mazumder Group. 
* It is a project to build BCO(BioComputer Object) using the synthetic data generated for [HIVE platform](https://hive.biochemistry.gwu.edu/dna.cgi?cmd=home). I generated 10G, 100G and 1000G data for the test. 
* I manipulated the data on [Galaxy](https://usegalaxy.org) with some [simple pipelines](https://www.melbournebioinformatics.org.au/tutorials/tutorials/variant_calling_galaxy_1/variant_calling_galaxy_1/) to create the workflow history. 
* With the workflow history (it is a json file), we can transfer it to the format we want. 
* Next step is to use the [BCO editor](http://www.biocomputeobject.org/bco_editor/) to create the BCO.
* Final step, I built a Galaxy server on AWS and ran those same pipelines with the same data on it to create BCOs.

## Step 1: Generate data from HIVE platform.

## Step 2: Find a proper pipeline to run the data from the previous step on Galaxy.

## Step 3: Extract the work history, use jsonResolver to transfer the data to what we want.

## Step 4: Create BCO on the BCO Editor (half data maually and half from the result after jsonResolver).


