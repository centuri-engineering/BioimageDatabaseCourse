title: BioImage Databases - training session
author: Guillaume Gay



# The TIFF file format


## Create a tiff in Python with `imageio`

- Create an array
- Use different data types


## Open a tiff with `scikit-image`

- Re-open the previous tiffs with skimage


## Open an ome.tiff with `aicsimageio`


### Read metadata

# Omero

> Learn to read the documentation!

https://docs.openmicroscopy.org/omero/5.6.3/index.html

https://docs.openmicroscopy.org/omero/5.6.3/developers/Python.html

## Install omero

```
conda install -c ome omero
```


## Log in the web client

- Open data
- Find The x resolution
- Open the 3D viewer



## Annotate and browse

- setup project / dataset

- Add a tag and a comment

- Search for DAPI images



## API

- connect to OMERO

- Download data

- Read metadata



# An example of automated workflow

Loop over all images in the dataset, compute average intensity per plane.




# The IDR

## Remember FAIR?

- Findable
- Accessible
- Interoperable
- Reusable


## Submission process

- Describe the important points


-----------------------------



## IDR public API

### From this article, find the original data in IDR (1/5)

https://elifesciences.org/articles/55913


### Write a code that connects to IDR (2/5) and read metadata from one of the above datasets (2/5)

### If we have time, use napari (or the new ipygani) to display the data
