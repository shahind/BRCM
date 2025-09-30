# Introduction
This repo updates the BRCM Toolbox developed by the [Automatic Control Lab, ETH Zurich](https://brcm.ethz.ch) for MATLAB 2024b. Potentially it should work for 2019b and above but it is just tested on 2024b. It may work or not on other versions.

## What is it?
The Building Resistance-Capacitance Modeling (BRCM) Matlab Toolbox facilitates the physical modeling of buildings for MPC. The Toolbox provides a means for the fast generation of (bi-)linear resistance-capacitance type models from basic geometry, construction and building systems data. Moreover, it supports the generation of the corresponding potentially time-varying costs and constraints. The Toolbox is based on validated modeling principles.

## Features
* Generation of a discrete-time bilinear state-space model of the building
* Loading from / writing to strictly structured building data files
* Visualization of the building
* Programmatical parameter manipulation
* Providing functions to generate time-varying costs and constraints for the MPC optimization
* Simulation of the model
* Input data generation from EnergyPlus input data files

# Installation
Originally it was developed to be available through ``tbxmanager``:
```
tbxmanager install brcm 
```
however the download links do not work anymore and the publisher is not able to update them [See their explanation here](https://control.ee.ethz.ch/software/BRCM-Toolbox.html)

Right now, you can download the repo and put the files inside the ``toolboxes`` directory where you have installed the ``tbxmanager`` and run the following commands:
```
tbxmanager install brcm
tbxmanager enable brcm
```
this should add the ``brcm`` directory to the MATLAB directories. Or simply download and put the files in a certain directory and add the directory to the MATLAB directories:
```MATLAB
addpath(PATH_TO_YOUR_DIRECTORY)
```
 Then run the following command in your MATLAB Command Window:
```MATLAB
BCRM_Setup
```
After this, you should be able to run sample project:
```MATLAB
BCRM_DemoFile
```