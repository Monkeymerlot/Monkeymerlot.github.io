---
layout: post
title:  "Release of Rotational Vibrational Spectroscopy Library"
---

# Welcome
Today marked the initial release of the Rotational Vibrational Spectroscopy package I created for Pitt CHEM 1430's IRS Lab. It provides an easy way to create report ready figures for an exported HCl DCl spectrum. Futhermore, it also provides a function that facilitates fitting peak data to predefined functions needed for this lab.

## Motivation
For this particular experiment, we are required to label all of the peaks in the spectrum with their wave number. Futhermore, we were required to label the peak with the branch, quantum transition number, proper axis, and title. After this was completed, we had to fit the plot of peak wavenumber values vs respective quantum transition numbers, and depending on the transition and the branch, there was a total of 4 different functions to fit the data to. The laboratory report suggested that this is done in Microsoft Excel, however, I felt that it is easier to graph and fit these functions in Python. Futhermore, the graphs are required to abide by ACS Journal of Physical Chemistry A's guidelines for figures. This is not particularly easy to do in Excel. 

With all of this in mind, I initially copied and pasted a lot of the code that I wrote for a single transition, however, I felt that I could modularize this and mess around with the functions until things like automatic detection of the correct isotope peaks and labelling seemed correct. As a result, I have created a library that does this automatically. Hopefully this might come in use for someone else who is taking Pitt's CHEM 1430 lab, or performing the same experiment at another university.

## Examples
By simply loading the data into Python using `readSpectrum()`, cropping the spectrum so it only contained a single transition, adding a title using `makeTitle()`, and then using `detectpeaks()`, I was able to get the resulting image as an output with only 5 short lines of code.
![First Overtone Transition for HCl](/assets/IRS_HCL2.jpg)

