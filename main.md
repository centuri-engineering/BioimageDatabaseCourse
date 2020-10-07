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

---------


## Why you are right to take this course

[An excel file does not consitute a database (it is an accounting tool)](https://www.bbc.com/news/uk-54412581)



## Who am I?


### Training

- Licence "Sciences Physiques" (Strasbourg)
- Maîtrise "Sciences Physiques" (Toulouse)
- DEA (today's Master 2 recherche)
- PhD in 2006 fundamental optics and [_cold atoms_](https://en.wikipedia.org/wiki/Laser_cooling).

---------

I also studied how light goes through small apertures:

![subwavelength aperture](images/sub_wavelength.png)

---------

I used a CCD camera from the late '90s:

![Good old TEA512](images/CCD_princetonTEA512.jpeg)


### Postdocs

- From 2006 to 2012 I was a postdoc in biology & biophysics labs

I started working on microscope images of the fission yeast _Schizosaccharomyces pombe_



---------

- Widefield, 1 image stack (about 10 z) every 30 s for 30 min
- 10 cells to track per field of view
- 6 kinetochores per cell (so around 10 000 data points)

![Automated segmentation of S. pombe cells](images/igor_fuseau.png)


---------


- Then we did **laser ablation** & **Fluorescence recovery after photo-bleaching** experiments

> Very rich data : relaxation speeds, diffusion/binding coefficients...

I started working on modeling mechanical aspects of mitosis.



### Freelance

In 2012 I started working as a freelance to do data analysis and modeling for biology research and biotech. Worked for various labs, for L'Oréal, for a pattent for a antibiotic sensitivity assesment method, or a method to measure eyesight with VR gogles...

![Model of fold formation](images/fold_ellipsoid.gif)


One of my main project is [tyssue](https://github.com/damcb/tyssue) which is a _library_ used to model epithelium.



## Course outline


# What have you learned before?


## All the '-omics' DBs


- What was important in Bianca's course? (give me 3 take home messages)

For me:

* Primary / Secondary dbs

* Need for curation

* Lots of re-use (due to the homongeneity of input)


------------



> Images are much more messier

(_also bioinformaticians are computer scientists, microscopists are physicists_)



> Data management with bioimages is far less advanced.


# Some technique history


## Early Microscopes


### Single lens

[Antonie van Leewenhoek (1632–1723)](https://en.wikipedia.org/wiki/Antonie_van_Leeuwenhoek)

:::::::::::::: {.columns}
::: {.column width="50%"}
<p><a href="https://commons.wikimedia.org/wiki/File:Leeuwenhoek_Eschenholz.jpg#/media/File:Leeuwenhoek_Eschenholz.jpg"><img src="https://upload.wikimedia.org/wikipedia/commons/1/1c/Leeuwenhoek_Eschenholz.jpg" alt="See caption"></a><br>By Antoni van Leeuwenhoek - T. Cremer, Von der Zellenlehre zur Chromosomentheorie, Springer Verlag Berlin Heidelberg New York Tokyo, 1985, &lt;a href="//commons.wikimedia.org/wiki/Special:BookSources/3-540-13987-7" title="Special:BookSources/3-540-13987-7"&gt;ISBN&amp;nbsp;3-540-13987-7&lt;/a&gt;. &lt;a rel="nofollow" class="external text" href="http://www.t-cremer.de/main_de/cremer/personen/info_T_Cremer.htm#book"&gt;Online Version&lt;/a&gt;. Source given in there: The collected letters from Antoni van Leeuwenhoek, Vol. II, Amsterdam, Sweets and Zeitlinger LTD (1941), Public Domain, <a href="https://commons.wikimedia.org/w/index.php?curid=3652421">Link</a></p>
:::
::: {.column width="50%"}
<p><a href="https://commons.wikimedia.org/wiki/File:Leeuwenhoek_Microscope.png#/media/File:Leeuwenhoek_Microscope.png"><img src="https://upload.wikimedia.org/wikipedia/commons/d/de/Leeuwenhoek_Microscope.png" alt="See caption"></a><br>By Jeroen Rouwkema, <a href="https://creativecommons.org/licenses/by-sa/3.0" title="Creative Commons Attribution-Share Alike 3.0">CC BY-SA 3.0</a>, <a href="https://commons.wikimedia.org/w/index.php?curid=3657142">Link</a></p>
:::
::::::::::::::



### Compound lenses

[Robert Hooke (1635-1703)](https://en.wikipedia.org/wiki/Robert_Hooke)

![Hooke's drawing of a flea](https://en.wikipedia.org/wiki/Robert_Hooke#/media/File:HookeFlea01.jpg)


First detector is the **eye**, data is registered through simple drawings.

### XXth century

[Santiago Ramón y Cajal (1852 - 1934)](https://en.wikipedia.org/wiki/Santiago_Ramón_y_Cajal)


![Drawing of Purkinje cells (around 1930)](https://en.wikipedia.org/wiki/Santiago_Ram%C3%B3n_y_Cajal#/media/File:PurkinjeCell.jpg)

The eye + hand are still the best detector in the early XXth century.


### First photos


[Henry Fox Talbot](https://en.wikipedia.org/wiki/Henry_Fox_Talbot)


![Photomicrograph_of_insect_wings_-_By_William_Henry_Fox_Talbot](https://upload.wikimedia.org/wikipedia/commons/6/68/Photomicrograph_of_insect_wings_-_By_William_Henry_Fox_Talbot.jpg)


See [this article](http://www.microscopy-uk.org.uk/mag/artmar10/history_photomicrography_ed3.pdf)


### First movies

[Jean Comandon in 1909](https://www.dailymotion.com/video/x6h3aas)


<iframe width="560" height="315" src="https://www.youtube.com/embed/09i1zdv3KVM" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


### Haemanthus katherinae (1956!)

[Mitosis in Haemanthus katharinae endosperm](http://www.cellimagelibrary.org/images/11952)

<video width="800" height="600" controls>
  <source src="images/11952_web.mp4" type="video/mp4">
</video>


## Technique evolution


### Fluorescence !

* dark field
* multiple colors
* **specificity** - we observe not only the organism but a precise _molecule_ within the organism.


### The confocal microscope

[Davidovits & Egger 1969](https://doi.org/10.1038/223831a0)

* The detector is a photomuliplier - first time the image from the microscope is a **signal**
* Only the light emitted at the focal point is recorded.


### Here comes the CCD

* Photon counting!

* The image is a quantitative, digital, signal

> From now on, an image is represented by a matrix of pixels


## Modern microscopes


### The super resolution revolution

Do you know Abbe low?

$$r = \frac {\lambda}{2 \sin \mathrm{NA}}  $$

The minimum size of a motif - for exemple the distance between two spots, observable under a microscope is limited by the objective numerical aperture and the emission wavelength.


We invented ways to beat that limit (can you site super resolution microscopes?)

### An exemple: STORM:

![Christophe Leterrier, NeuroCyto, INP, Marseille](https://i2.wp.com/www.neurocytolab.org/wp-content/uploads/2016/12/SYNMJ_Synapses_z-1.jpg)

Now instead of aquiring an image plane by plane (epifluorescence), or by scanning a pinhole (confocal), we detect individual proteins and point their positions. A single image is the combination of all thoses individual localisations.


### An other: Lattice light sheet


https://vimeo.com/109402221

https://vimeo.com/109403013



### Sreens and plates

> Multiple wells under a microscope on a moving stage

[An exemple of such system](https://www.perkinelmer.com/fr/product/opera-phenix-system-hh14000000)



## Conclusion

> Image aquisition methods have always been immediatly applied to microscopy

> The eye was surpassed only recently

> The image became _digital_ only 20 years ago!


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
