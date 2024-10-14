---
layout: post
title: Demonstration resources
description: Description of the data resources we explored within SoilPulse
image: 
nav-menu: true
---

## TUBAF data

The data from several experimental campaigns of the [TU Bergakademie Freiberg (TUBAF)](https://tu-freiberg.de/fakult3/ibf/bodenphysik-und-oekohydrologie) was curated within a dissertation thesis and is available in differing data structures from the zenodo publication [10.5281/zenodo.6654150](https://doi.org/10.5281/zenodo.6654150).

- One structure holds the relevant data in tabular form, within three tables
- Units, methods and concepts were manually assigned
- A pipeline was created to transform the data in a machine readable data structure

 
## SWIG

[10.1594/PANGAEA.885492](https://doi.pangaea.de/10.1594/PANGAEA.885492)
It comes in tabular form in csv files and alternatively in a single multi sheet xlsx.
To complex structure of time series, could not be readily transformed:
One table per concept (time, infiltration volume)
In those on column per experiment (column name identifies experiment)
Needs transformation step.table_melt() which is very resource intensive for >5000 columns
Correct joining of time with infiltration_volume could not be realized by now (position within sheet references from on table to the other)
Misses runoff measurements (so it is not in scope of cross data set query 1)

## Ries Data

[Ries et. al.](https://doi.org/10.6094/UNIFR/151460) preparation in progress…

## CTU data dump
