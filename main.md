---
title: Bio-image databases
author: Guillaume Gay, CENTURI
date: 9 Octobre 2020
fontsize: 11pt
width: 1080
height: 720
...


# Intro

> We are here to talk about micrscopy image databases. We are not going to talk a lot about the "database" part of that, because a lot has to be said about microscopy and images before that is more important.

## Course outline


## Why you are right to take this course

https://www.bbc.com/news/uk-54412581


## Who am I?


### Training

- Licence "Sciences Physiques" (Strasbourg)
- Maîtrise "Sciences Physiques" (Toulouse)
- DEA (today's Master 2 recherche) ""
- PhD in 2006 fundamental optics and 'cold' atoms. I studied how light goes through small apertures:

![subwavelength aperture](images/sub_wavelength.png)

I used a CCD camera from the late '90s:

![Good old TEA512](images/CCD_princetonTEA512.jpeg)


### Postdocs

- From 2006 to 2012 I was a postdoc in biology & biophysics labs

I started working on microscope images of the fission yeast _Schizosaccharomyces pombe_

- Widefield, 1 image stack (about 10 z) every 30s for 30 minutes, about 10 cells to track per field of view - 6 kinetochores per cell (so around 10 000 data points)

> Already a need for automation

![Automated segmentation of S. pombe cells](images/igor_fuseau.png)

- Then we did **laser ablation** & **Fluorescence recovery after photo-bleaching** experiments

> Very rich data : relaxation speeds, diffusion/binding coefficients...

I started working on modeling mechanical aspects of mitosis.


### Freelance

In 2012 I started working as a freelance to do data analysis and modeling for biology research and biotech. Worked for various labs, for L'Oréal, for a pattent for a antibiotic sensitivity assesment method, or a method to measure eyesight with VR gogles...

### Epithelium modeling

One of my main project is [tyssue](https://github.com/damcb/tyssue) which is a _library_ used to model epithelium.


# What have you learned before?

## All the '-omics' DBs

- What was important in Bianca's course?

- Primary / Secondary dbs

- **Homogeneity of input data** (basically strings of ACGTs)


> Images are much more messier - also bioinformaticians or computer scientists, microscopists are physicists.

Data management with bioimages are far less advanced.

## What are those dbs used for?

We'll see the contrast with image databases

# Some technique history

## Early Microscopes

### Single lens

[Antonie van Leewenhoek (1632–1723)](https://en.wikipedia.org/wiki/Antonie_van_Leeuwenhoek)

![A microscopic section of a one-year-old ash tree wood](https://en.wikipedia.org/wiki/Antonie_van_Leeuwenhoek#/media/File:Leeuwenhoek_Eschenholz.jpg)

![A replica of a microscope by van Leeuwenhoek](https://en.wikipedia.org/wiki/Antonie_van_Leeuwenhoek#/media/File:Leeuwenhoek_Microscope.png)

### Compound

[Robert Hooke (1635-1703)](https://en.wikipedia.org/wiki/Robert_Hooke)

![Hookes drawing of a flea](https://en.wikipedia.org/wiki/Robert_Hooke#/media/File:HookeFlea01.jpg)



First detector is the **eye**, data is registered through simple drawings.


[Santiago Ramón y Cajal (1852 - 934)](https://en.wikipedia.org/wiki/Santiago_Ramón_y_Cajal)


[Drawing of Purkinje cells](https://en.wikipedia.org/wiki/Santiago_Ram%C3%B3n_y_Cajal#/media/File:PurkinjeCell.jpg)

The eye + hand are still the best detector in the early XXth century.


### First photos



### First movies

### Haemanthus katherinae (1956!)

[Mitosis in Haemanthus katharinae endosperm](http://www.cellimagelibrary.org/images/11952)

<video width="800" height="600" controls>
  <source src="images/11952_web.mp4" type="video/mp4">
</video>



## Contrast methods

### Interference Contrast

### Polarization

### Fluorescence !

* specificity
* multiple colors

## What is a microscope again?

### The confocal microscope

### Super resolution

### Today: Lattice light sheet

https://vimeo.com/109402221

https://vimeo.com/109403013






### Here comes the CCD

> Photon counting

> The image is now a quantitative, digital, signal

### Sreens and plates


# The digital image

> What is important to know?



> Data and metadata

> Cite image formats

?

## TIFF (not the Toronto international film festival)


## A sad story

xkcd

OME to the rescue

> «It is possible to interpret images only if we know the context in which they were acquired»

## OME-XML


### XML

### OME-XML

Look for the important points you thought of.

What do you think of XML?


### Limits to OME-XML

* What did you say a microscope image was?

* image.sc posts


### The future: how to define flexible, "just general enough" file formats.

Let's look at ZARR



# Finally Databases!

## One DB system to rule them all: OMERO

## The Contender Cytomine (but still using BioFormats!)

https://forum.image.sc/t/centralised-online-image-processing-solutions-platforms/20779


# Using OMERO - A tour

## Let's go into some gritty details

## Web viewer

> What info do you see?

> Can you find the metadata we said were important?

> What's the difference with B. Habermann examples?


# Public microscopy image databases

## The Allen Institute

## A word on FAIR

## The IDR



https://www.princetoninstruments.com/learn/camera-fundamentals/
