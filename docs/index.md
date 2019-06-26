---
layout: default
title: Documentation
---

## Table of Contents
1. [Overview](#overview)
2. [Installation](#installation)
3. [Implementation](#implementation)
    - [lenser_galaxy](#lenser_galaxy)
    


## Overview
Lenser is a package of python programs used to analyze FITS files of galaxies. First, the user must input a "postage stamp" containing one galaxy. Next, Lenser will deproject the image to show what the galaxy looked like before the contortion due to gravitanal lensing. Then, Lenser will output the four flexion parameters associated with the inputted galaxy.

Lenser is a powerful tool that will quickly compute lensing data for a given galaxy. It uses a pipeline of programs that refine and improve the prediction and measurment of the deprojection and flexion values. The three programs in the pipeline are [lenser_galaxy](#lenser_galaxy), lenser_aim, and lenser_lens.




<img src="https://i.imgur.com/uFtAFu0.jpg" width="300">



## Installation
This package uses python 3 (mostly, except for Evan's print statements). You will need to have astropy, scipy, numpy, and matplotlib installed on your computer. These are standard with most python insallations. Depending on the environment you run the code from, you may also need to install a LaTex compiler (MikTex should work). Additionally you may need to go into this package and change all of the tabs because of an inconsistant use of tabs and spaces.
## Implementation
Here is how to use every little part of this
Here is how to use every little part of this
Here is how to use every little part of this

```python
#just testing if I can display code
def function(a):
  counter = 0
  b = 4
  for i in range(a):
    counter += b
```

Here is how to use every little part of this
Here is how to use every little part of this
Here is how to use every little part of this
Here is how to use every little part of this
Here is how to use every little part of this
Here is how to use every little part of this
### lenser_galaxy
lenser_galaxy consists of a galaxy class. Using this class you can preform many manipulations on a "postage stamp" of a galaxy including subtracting background radiation, estimating noise, and masking tangential radiation to only show relevant data. These three functions prepare the data to be inputted into [lenser_aim](#lenser_aim)
1. [Basics of Implementing a Galaxy Object](#Basics)
    - [Instantiation](#To-instantiate)
    - [setName](#The-galaxy-class)
1. [Background subtraction]
1. [Noise estimation]
1. [Masking]
#### Basics of Implementing a Galaxy Object
To instantiate a galaxy object simply set your object name equal to $galaxy(data, galaxyname)$. For example:

```python
mygalaxy = galaxy(data, galaxyname)
```

The galaxy class only takes a maximum of two inputted attributes. However, the name attribute is not required to instantiate your galaxy, and when left out it will be defaulted to "blank." This name can be changed using the setName method:

```python
mygalaxy.setName(newname)
#your galaxy object will now have the new name of "newname"
```
The "data" argument is required to be a 2d list or numpy array. This data is best derived from a FITS file. If you are unfamiliar with FITS file handling, here is an easy way to extract the necessary data from a FITS file:

```python
infile="galaxy_image"#whatever your FITS file is named. Be sure you call it from the correct directory
hdu_list = fits.open(infile)
objname=hdu_list[0].header['OBJECT']
myval=hdu_list[0].data
hdu_list.close()
```

### lenser_aim
This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. 

