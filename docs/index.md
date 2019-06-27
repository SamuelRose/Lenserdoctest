---
layout: default
title: Documentation
---

## Table of Contents
1. [Overview](#overview)
2. [Installation](#installation)
3. [Implementation](#implementation)
    - [lenser_galaxy](#lenser_galaxy)
    - [lenser_aim](#lenser_galaxy)
    


## Overview
Lenser is a package of python programs used to analyze FITS files of galaxies. First, the user must input a "postage stamp" containing one galaxy. Next, Lenser will deproject the image to show what the galaxy looked like before the contortion due to gravitanal lensing. Then, Lenser will output the four flexion parameters associated with the inputted galaxy.

Lenser is a powerful tool that will quickly compute lensing data for a given galaxy. It uses a pipeline of programs that refine and improve the prediction and measurment of the deprojection and flexion values. The three programs in the pipeline are [lenser_galaxy](#lenser_galaxy), lenser_aim.


The Lenser package uses two main files: lenser_galaxy and lenser_aim. The lenser_galaxy file can be used to clean an image of a galaxy by getting rid of background radiation, adjusting for noise, and masking out irrelevant data. These images can then be manipulated using the lenser-aim file which will predict how the galaxy looks without the presence of gravitational lensing.

<img src="https://i.imgur.com/uFtAFu0.jpg" width="300">



## Installation
This package uses python 3, and you will need to have astropy, scipy, numpy, and matplotlib installed. These are standard with most python insallations. Depending on the environment you run the code from, you may also need to install a LaTex compiler (MikTex should work).
## Implementation
[lenser_galaxy](#lenser_galaxy)
[lenser_aim](#lenser_aim)

### lenser_galaxy
lenser_galaxy consists of a Galaxy class, an Image class, and a Lens class. Using this class you can preform many manipulations on a "postage stamp" of a galaxy including subtracting background radiation, estimating noise, and masking tangential radiation to only show relevant data. These three functions prepare the data to be inputted into [lenser_aim](#lenser_aim)
1. [Using the Galaxy class](#Galaxy)
    - [Instantiation](#Instantiation)
    - [setName](#setName)
    - [setPar](#setPar)
    - [setLens](#setLens)
    - [Background subtraction]
    - [Noise estimation]
    - [Masking]
2. [Using the Image class](#Image)
3. [Using the Lens class](#Lens)

#### Using the Galaxy class<a name="Basics"></a>
<a name="Instantiation"></a> The galaxy object contains the set of paramaters relevant to lensing. Each parameter is given a default value, so no attributes are required at instantiation:
```python
mygalaxy = Galaxy(xc=0,yc=0,ns=0.5,rs=1.0,q=1.0,phi=0.0,galaxyLens=None)
```
This is the default galaxy object. xc is SOMETHING, yc is SOMETHING, ns is the factor by which the intensity falls of, rs is the **Einstein radius????** or the radius at which the intensity has fallen off by one half, q is the ratio of the semimajor and semiminor axes of the galaxy, phi is the angle of rotation of the galaxy in radians, and galaxyLens is a [Lens object](#Lens) or None.
    
<a name="setName"></a>
You can change the name of your galaxy object using the setName method. 

```python
mygalaxy.setName(newname)
#your galaxy object will now have the new name of "newname"
```
<a name="setPar"></a>
You can change any of the parameters using the setPar function. This function takes two arguments: the new value and the value type.

```python
mygalaxy.setPar(val = newvalue, type = valuetype)
#mygalaxy will now have its valuetype parameter changed to whatever newvalue is
```

The acceptable values for the type argument are the first six attributes of the galaxy class: "xc", "yx", "ns", "rs", "q", "phi". Using one of these as the type argument will change that prospective attribute of your galaxy object to whatever the val argument is.
    
<a name="setLens"></a>
The setLens method can be used to change the Lens attribute of the Galaxyobject. 
```python
mygalaxy.setLens(newlens = myLens)
#mygalaxy.Lens is now equal to myLens
```
The newlens argument must be a [Lens object](#Lens).

#### Using the Image class<a name="Image"></a>

#### Using the Lens class<a name="Lens"></a>
### lenser_aim
This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. This takes up space. 

