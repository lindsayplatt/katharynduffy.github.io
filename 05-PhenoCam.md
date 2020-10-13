
# PhenoCam: Digital Repeat Photography Networks & Methods

> Estimated Time: 4 hours


**Course participants**: As you review this information, please
consider the final course project
that you will work on at the over this semester. At the end of this section, you will
document an initial research question or idea and associated data needed to
address that question, that you may want to explore while pursuing this course.



## Digital Repeat Photography Networks Learning Objectives

At the end of this activity, you will be able to:

  1. Understand how phenology is a large driver of biosphere-atmosphere interactions, and is a sensitive indicator of climate change.
  
  2. Summarize data which can be pulled out of digital repeat imagery
  
  3. Describe basic processing of digital repeat photography
  
  3. Perform basic image processing.

  4. Estimate image haziness as an indication of fog, cloud or other natural or artificial factors using the `hazer`R package.

  5. Define and use a Region of Interest, or ROI, for digitial repeat photography methods.

  6. Handle Field-of-View (FOV) shifts in digital repeat photography.

  7. Extract timeseries data from a stack of images using color-based metrics.

## The PhenoCam Network Mission & Design

<iframe width="560" height="315" src="https://www.youtube.com/embed/_4uHLXL1yZA" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

**Since its inception, the objective of the PhenoCam network has been to serve as a repository for phenologically-relevant, digital, repeat (time-lapse) imagery, and to make that imagery, and derived data products, freely available to a wide array of third-party data end-users, including researchers, educators, and the general public.**


"Thus, imagery from the PhenoCam archive is made publicly available, without restriction, and we encourage you to download imagery and datasets for use in your own research and teaching. In return, we ask that you acknowledge the source of the data and imagery, and abide by the terms of the Creative Commons CC BY Attribution License." 



### Relevant documents & background information:

* [The PhenoCam Gallery](https://phenocam.sr.unh.edu/webcam/gallery/)

* [A map of PhenoCam locations](https://phenocam.sr.unh.edu/webcam/network/map/)

* [A site table of all PhenoCams](https://phenocam.sr.unh.edu/webcam/network/table/)

* [PhenoCam metadata](https://phenocam.sr.unh.edu/webcam/tools/site_metadata_format/)

## PhenoCam’s Spatial design:

The PhenoCam Network is:

* A voluntary 'opt in' network with collaborators who are varied, including: 

  + Individual research labs or field sites in North America, Europe, Asia, Africa, South America

  + Individuals who think it would be cool to be part of a network like this
  


The project is largely run by the Richardson Lab at NAU, with support from key collaborators at the University of New Hampshire who provide server and website management.

Anyone can buy a relatively inexpensive camera, run some simple scripts to correct for things like auto-white balance (which we will cover later), and patch in to the netowrk.  PhenoCam then retrieves, archieves and processess imagery for distribution.



### PhenoCam as a Near Surface Remote Sensing Technique

<iframe width="560" height="315" src="https://www.youtube.com/embed/l3d3shbF2_s" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

> 6 years of PhenoCam imagery at Harvard Forest


* PhenoCam uses imagery from networked digital cameras for continuous monitoring of plant canopies

* Images are recorded approximately every 30 minutes (every 15 minutes for NEON), sunrise to sunset, 365 days a year

* The scale of observations is comparable to that of tower-based land-atmosphere flux measurements

* PhenoCams provide a direct link between what is happening on the ground and what is seen by satellites
PhenoCams cover a wide array of:

* Plant Funtional Types (PFTs)

<img src="./images/phenocams.png" width="1471" />

* Ecoregions

<img src="./images/phenocam_zones.png" width="959" />

> Spatial distribution of PhenoCam data across ecological regions of North America. Background map
illustrates USA Environmental Protection Agency Level I Ecoregions. Data counts have been aggregated to
a spatial resolution of 4°, and the size of each circle corresponds to the number of site-years of data in the 4×4°
grid cell. Sites in Hawaii, Puerto Rico, Central and South America, Europe, Asia and Africa (total of 88 site
years) are not shown. (Seyednasrollah et al., 2019)

* Co-Located Networks
 
 + [Flux towers](https://phenocam.sr.unh.edu/webcam/network/search/?sitename=spruce&type=I&primary_vegtype=&dominant_species=&active=unknown&fluxdata=unknown&group=)
 
 + [NEON](https://phenocam.sr.unh.edu/webcam/network/search/?sitename=&type=I&primary_vegtype=&dominant_species=&active=unknown&fluxdata=false&group=NEON)
 
 + [LTER/LTAR](https://phenocam.sr.unh.edu/webcam/network/search/?sitename=&type=I&primary_vegtype=&dominant_species=&active=unknown&fluxdata=false&group=LTAR)

* Ambient vs. Experimental set ups

<img src="./images/spruce_phenocam.png" width="300" />


  - [SEGA sites](https://phenocam.sr.unh.edu/webcam/network/search/?sitename=sega&type=I&primary_vegtype=&dominant_species=&active=unknown&fluxdata=unknown&group=)

  - [SPRUCE Experiment](https://phenocam.sr.unh.edu/webcam/network/search/?sitename=spruce&type=I&primary_vegtype=&dominant_species=&active=unknown&fluxdata=unknown&group=)

### How PhenoCams Pull Data

<img src="./images/Screen Shot 2020-09-13 at 5.46.32 PM.png" width="1193" />

### Leveraging camera near-infrared (NIR) capabilities

[Petach et al., Agricultural & Forest Meteorology 2014](http://harvardforest.fas.harvard.edu/publications/pdfs/Petach_AgriForestMeteor_2014.pdf)

CMOS sensor is sensitive to \lambda > 700 nm

<img src="./images/phenocamNIR.png" width="277" />

A software-controlled filter enables sequential VIS (RGB color) and VIS+NIR (monochrome) images
Potential applications:

* false color images

* “camera NDVI” as alternative to GCC

<img src="./images/phenocamFALSE1.png" width="320" /><img src="./images/phenocamFALSE2.png" width="320" />



## Digital Repeat Photography Written Questions


*Suggested completion: Before Digital Repeat Photography methods (day 2 PhenoCam)*

**Question 1:** What do you see as the value of the images themselves?  The 1 or 3-day products, the transition dates?  How could they be used for different applications?

**Question 2:** Why does PhenoCam take photos every 15-30 minutes, but summarize to 1 or 3-day products?

**Question 3:** Why does canopy color coordiante with photosynthesis in many ecosystems?  Name an example of a situation where it wouldn't and explain why.

**Question 4:** Why are there sometimes multiple **Regions of Interest (ROIs)** for a PhenoCam?

**Question 5:** How might or does the PhenoCam project
intersect with your current research or future career goals? *(1 paragraph)*

**Question 6:**
Use the map on the [PhenoCam website](https://phenocam.sr.unh.edu/webcam/network/map/) to answer the following questions. Consider the research question that you may explore as your final semester project or a current project that you are working on and answer each of the following questions:

* Are there PhenoCams that are in study regions of interest to you?  
* Which PhenoCam sites does your current research or final project ideas
coincide with?  
* Are they connected to other networks (e.g. LTAR, NEON, Fluxnet)?  
* What is the data record length for the sites you're interested in?

**Question 7:**
Consider either your current or future research, or a question you’d like to
address durring this course:

* Which types of PhenoCam data may be more useful to address these questions?
* What non-PhenoCam data resources could be combined to help address your question?
* What challenges, if any, could you foresee when beginning to work with these
data?



## Introduction to Digital Repeat Photography Methods

The concept of repeat photography for studying environmental has been
introduced to scientists long time ago (See Stephens et al., 1987).
But in the past decade the idea has gained much popularity for monitoring
environmental change (e.g., Sonnentag et al., 2012).
One of the main applications of digital repeat photography is studying vegetation
phenology for a diverse range of ecosystems and biomes (Richardson et al., 2019).
The methods has also shown great applicability in other fields such as:

1. assessing the seasonality of gross primary production,

2. salt marsh restoration,

3. monitoring tidal wetlands,

4. investigating growth in croplands, and

5. evaluating phenological data products derived from satellite remote sensing.

Obtaining quantitative data from digital repeat photography images is usually
performed by defining appropriate region of interest, also know as ROI's,
and for the red (R), green (G) and blue (B) color channels, calculating
pixel value (intensity) statistics across the pixels within each ROI.
ROI boundaries are delineated by mask files which define which pixels
are included and which are excluded from these calculations.

The masks are then used to extract color-based time series from a stack of images.
Following the time-series, statistical metrics are used to obtain
1-day and 3-day summary time series.
From the summary product time series, phenological transition dates
corresponding to the start and the end of green-up and green-down
phenological phases are calculated.
In this chapter we explain this process by starting from general
image processing tools and then to phenocam-based software applications.

For more details about digital repeat photogrpahy you can check out the following publications:
- <a href="https://bnasr.github.io/papers/Seyednasrollah_et_al_2019_SciData.pdf">Seyednarollah, et al. 2019, "Tracking vegetation phenology across diverse biomes using Version 2.0 of the PhenoCam Dataset "</a>.
- <a href="https://bnasr.github.io/papers/Seyednasrollah_et_al_2019_PRS.pdf">Seyednarollah, et al. 2019, "Data extraction from digital repeat photography using xROI: An interactive framework to facilitate the process"</a>.

## Pulling Data via the *phenocamapi* Package

The <a href="https://cran.r-project.org/web/packages/phenocamapi/index.html" target="_blank"> *phenocamapi* R package</a>
is developed to simplify interacting with the
<a href="https://phenocam.sr.unh.edu" target="_blank">PhenoCam network</a>
dataset and perform data wrangling steps on PhenoCam sites' data and metadata.

This tutorial will show you the basic commands for accessing PhenoCam data
through the PhenoCam API. The *phenocampapi* R package is developed and maintained by
<a href="https://bnasr.github.io/" target="_blank">Bijan Seyednarollah</a>.
The most recent release is available on GitHub (<a href="https://github.com/bnasr/phenocamapi" target="_blank">PhenocamAPI</a>).
<a href="https://github.com/bnasr/phenocamapi/tree/master/vignettes" target ="_blank">Additional vignettes</a>
can be found on how to merge external time-series (e.g. Flux data) with the
PhenoCam time-series.

We begin with several useful skills and tools for extracting PhenoCam data
directly from the server:

- Exploring the PhenoCam metadata
- Filtering the dataset by site attributes
- Extracting the list of midday images
- Downloading midday images for a given time range

## Exploring PhenoCam metadata

Each PhenoCam site has specific metadata including but not limited to how a site
is set up and where it is located, what vegetation type is visible from the
camera, and its climate regime. Each PhenoCam may have zero to several Regions
of Interest (ROIs) per vegetation type. The *phenocamapi* package is an
interface to interact with the PhenoCam server to extract those data and
process them in an R environment.

To explore the PhenoCam data, we'll use several packages for this tutorial.



```r
library(data.table)
library(phenocamapi)
```

```
## Loading required package: rjson
```

```
## Loading required package: RCurl
```

```
## Warning: package 'RCurl' was built under R version 3.6.2
```

```r
library(lubridate)
```

```
## Warning: package 'lubridate' was built under R version 3.6.2
```

```
## 
## Attaching package: 'lubridate'
```

```
## The following objects are masked from 'package:data.table':
## 
##     hour, isoweek, mday, minute, month, quarter, second, wday, week,
##     yday, year
```

```
## The following objects are masked from 'package:base':
## 
##     date, intersect, setdiff, union
```

```r
library(jpeg)
```


We can obtain an up-to-date `data.frame` of the metadata of the entire PhenoCam
network using the `get_phenos()` function. The returning value would be a
`data.table` in order to simplify further data exploration.



```r
# obtaining the phenocam site metadata from the server as data.table
phenos <- phenocamapi::get_phenos()

# checking out the first few sites
head(phenos$site)
```

```
## [1] "aafcottawacfiaf14e" "aafcottawacfiaf14w" "acadia"            
## [4] "aguatibiaeast"      "aguatibianorth"     "ahwahnee"
```

```r
# checking out the columns
colnames(phenos)
```

```
##  [1] "site"                      "lat"                      
##  [3] "lon"                       "elev"                     
##  [5] "active"                    "utc_offset"               
##  [7] "date_first"                "date_last"                
##  [9] "infrared"                  "contact1"                 
## [11] "contact2"                  "site_description"         
## [13] "site_type"                 "group"                    
## [15] "camera_description"        "camera_orientation"       
## [17] "flux_data"                 "flux_networks"            
## [19] "flux_sitenames"            "dominant_species"         
## [21] "primary_veg_type"          "secondary_veg_type"       
## [23] "site_meteorology"          "MAT_site"                 
## [25] "MAP_site"                  "MAT_daymet"               
## [27] "MAP_daymet"                "MAT_worldclim"            
## [29] "MAP_worldclim"             "koeppen_geiger"           
## [31] "ecoregion"                 "landcover_igbp"           
## [33] "dataset_version1"          "site_acknowledgements"    
## [35] "modified"                  "flux_networks_name"       
## [37] "flux_networks_url"         "flux_networks_description"
```

Now we have a better idea of the types of metadata that are available for the
Phenocams.

### Remove null values

We may want to explore some of the patterns in the metadata before we jump into
specific locations.

Let's look at Mean Annual Precipitation (MAP) and Mean Annual
Temperature (MAT) across the different field site and classify those by the
primary vegetation type (`primary_veg_type`) for each site. We can find out what
the abbreviations for the vegetation types mean from the following table:


|Abbreviation|Description|
|-|-|
| AG |	agriculture |
| DB |	deciduous broadleaf |
| DN |	deciduous needleleaf |
| EB |	evergreen broadleaf |
| EN |	evergreen needleleaf |
| GR |	grassland |
| MX |	mixed vegetation (generally EN/DN, DB/EN, or DB/EB) |
| SH |	shrubs |
| TN |	tundra (includes sedges, lichens, mosses, etc.) |
| WT |	wetland |
| NV |	non-vegetated |
| RF |	reference panel | 	 
| XX |	unspecified |


To do this we'd first want to remove the sites where there is not data and then
plot the data.



```r
# removing the sites with unkown MAT and MAP values
phenos <- phenos[!((MAT_worldclim == -9999)|(MAP_worldclim == -9999))]

# extracting the PhenoCam climate space based on the WorldClim dataset
# and plotting the sites across the climate space different vegetation type as different symbols and colors
phenos[primary_veg_type=='DB', plot(MAT_worldclim, MAP_worldclim, pch = 19, col = 'green', xlim = c(-5, 27), ylim = c(0, 4000))]
```

```
## NULL
```

```r
phenos[primary_veg_type=='DN', points(MAT_worldclim, MAP_worldclim, pch = 1, col = 'darkgreen')]
```

```
## NULL
```

```r
phenos[primary_veg_type=='EN', points(MAT_worldclim, MAP_worldclim, pch = 17, col = 'brown')]
```

```
## NULL
```

```r
phenos[primary_veg_type=='EB', points(MAT_worldclim, MAP_worldclim, pch = 25, col = 'orange')]
```

```
## NULL
```

```r
phenos[primary_veg_type=='AG', points(MAT_worldclim, MAP_worldclim, pch = 12, col = 'yellow')]
```

```
## NULL
```

```r
phenos[primary_veg_type=='SH', points(MAT_worldclim, MAP_worldclim, pch = 23, col = 'red')]
```

```
## NULL
```

```r
legend('topleft', legend = c('DB','DN', 'EN','EB','AG', 'SH'),
       pch = c(19, 1, 17, 25, 12, 23),
       col =  c('green', 'darkgreen', 'brown',  'orange',  'yellow',  'red' ))
```

<img src="05-PhenoCam_files/figure-html/unnamed-chunk-9-1.png" width="672" />



### Filtering using attributes

Alternatively, we may want to only include Phenocams with certain attributes in
our datasets. For example, we may be interested only in sites with a co-located
flux tower. For this, we'd want to filter for those with a flux tower using the
`flux_sitenames` attribute in the metadata.




```r
# store sites with flux_data available and the FLUX site name is specified
phenofluxsites <- phenos[flux_data==TRUE&!is.na(flux_sitenames)&flux_sitenames!='',
                         .(PhenoCam=site, Flux=flux_sitenames)] # return as table
#and specify which variables to retain

phenofluxsites <- phenofluxsites[Flux!='']

# see the first few rows
head(phenofluxsites)
```

```
##                PhenoCam                               Flux
## 1:       alligatorriver                             US-NC4
## 2:          arsbrooks10 US-Br1: Brooks Field Site 10- Ames
## 3:          arsbrooks11 US-Br3: Brooks Field Site 11- Ames
## 4:        arscolesnorth                               LTAR
## 5:        arscolessouth                               LTAR
## 6: arsgreatbasinltar098                             US-Rws
```

We could further identify which of those Phenocams with a flux tower and in
deciduous broadleaf forests (`primary_veg_type=='DB'`).



```r
#list deciduous broadleaf sites with flux tower
DB.flux <- phenos[flux_data==TRUE&primary_veg_type=='DB',
                  site]  # return just the site names as a list

# see the first few rows
head(DB.flux)
```

```
## [1] "alligatorriver" "bartlett"       "bartlettir"     "bbc1"          
## [5] "bbc2"           "bbc3"
```



## Download midday images

While PhenoCam sites may have many images in a given day, many simple analyses
can use just the midday image when the sun is most directly overhead the canopy.
Therefore, extracting a list of midday images (only one image a day) can be useful.




```r
# obtaining midday_images for dukehw
duke_middays <- get_midday_list('dukehw')

# see the first few rows
head(duke_middays)
```

```
## [1] "http://phenocam.sr.unh.edu/data/archive/dukehw/2013/05/dukehw_2013_05_31_150331.jpg"
## [2] "http://phenocam.sr.unh.edu/data/archive/dukehw/2013/06/dukehw_2013_06_01_120111.jpg"
## [3] "http://phenocam.sr.unh.edu/data/archive/dukehw/2013/06/dukehw_2013_06_02_120109.jpg"
## [4] "http://phenocam.sr.unh.edu/data/archive/dukehw/2013/06/dukehw_2013_06_03_120110.jpg"
## [5] "http://phenocam.sr.unh.edu/data/archive/dukehw/2013/06/dukehw_2013_06_04_120119.jpg"
## [6] "http://phenocam.sr.unh.edu/data/archive/dukehw/2013/06/dukehw_2013_06_05_120110.jpg"
```

Now we have a list of all the midday images from this Phenocam. Let's download
them and plot



```r
# download a file
destfile <- tempfile(fileext = '.jpg')

# download only the first available file
# modify the `[1]` to download other images
download.file(duke_middays[1], destfile = destfile, mode = 'wb')

# plot the image
img <- try(readJPEG(destfile))
if(class(img)!='try-error'){
  par(mar= c(0,0,0,0))
  plot(0:1,0:1, type='n', axes= FALSE, xlab= '', ylab = '')
  rasterImage(img, 0, 0, 1, 1)
}
```

<img src="05-PhenoCam_files/figure-html/unnamed-chunk-13-1.png" width="672" />



### Download midday images for a given time range

Now we can access all the midday images and download them one at a time. However,
we frequently want all the images within a specific time range of interest. We'll
learn how to do that next.



```r
# open a temporary directory
tmp_dir <- tempdir()

# download a subset. Example dukehw 2017
download_midday_images(site = 'dukehw', # which site
                       y = 2017, # which year(s)
                       months = 1:12, # which month(s)
                       days = 15, # which days on month(s)
                       download_dir = tmp_dir) # where on your computer
```

```
## 
```

```
## [1] "/var/folders/5n/vxrdb72140b43_jhsmhfy514pqgq1n/T//RtmpQu9McA"
```

```r
# list of downloaded files
duke_middays_path <- dir(tmp_dir, pattern = 'dukehw*', full.names = TRUE)

head(duke_middays_path)
```

```
## [1] "/var/folders/5n/vxrdb72140b43_jhsmhfy514pqgq1n/T//RtmpQu9McA/dukehw_2017_01_15_120109.jpg"
## [2] "/var/folders/5n/vxrdb72140b43_jhsmhfy514pqgq1n/T//RtmpQu9McA/dukehw_2017_02_15_120108.jpg"
## [3] "/var/folders/5n/vxrdb72140b43_jhsmhfy514pqgq1n/T//RtmpQu9McA/dukehw_2017_03_15_120151.jpg"
## [4] "/var/folders/5n/vxrdb72140b43_jhsmhfy514pqgq1n/T//RtmpQu9McA/dukehw_2017_04_15_120110.jpg"
## [5] "/var/folders/5n/vxrdb72140b43_jhsmhfy514pqgq1n/T//RtmpQu9McA/dukehw_2017_05_15_120108.jpg"
## [6] "/var/folders/5n/vxrdb72140b43_jhsmhfy514pqgq1n/T//RtmpQu9McA/dukehw_2017_06_15_120120.jpg"
```

We can demonstrate the seasonality of Duke forest observed from the camera. (Note
this code may take a while to run through the loop).


```r
n <- length(duke_middays_path)
par(mar= c(0,0,0,0), mfrow=c(4,3), oma=c(0,0,3,0))

for(i in 1:n){
  img <- readJPEG(duke_middays_path[i])
  plot(0:1,0:1, type='n', axes= FALSE, xlab= '', ylab = '')
  rasterImage(img, 0, 0, 1, 1)
  mtext(month.name[i], line = -2)
}
mtext('Seasonal variation of forest at Duke Hardwood Forest', font = 2, outer = TRUE)
```

<img src="05-PhenoCam_files/figure-html/unnamed-chunk-15-1.png" width="672" />


The goal of this section was to show how to download a limited number of midday images from the PhenoCam server. However, more extensive datasets should be downloaded from the <a href="https://phenocam.sr.unh.edu/webcam/network/download/"> PhenoCam </a>.


The *phenocamapi* R package is developed and maintained by
<a href="https://bnasr.github.io/">Bijan Seyednarollah</a>.
The most recent release is available from
<a href="https://github.com/bnasr/phenocamapi" target="_blank">https://github.com/bnasr/phenocamapi</a>.

## Detecting Foggy Images using the 'hazer' R Package

#### Read & Plot an Image

We will use several packages in this tutorial. All are available from CRAN.



```r
# load packages
library(hazer)
library(jpeg)
library(data.table)
library(dplyr)
```

```
## Warning: package 'dplyr' was built under R version 3.6.2
```

```
## 
## Attaching package: 'dplyr'
```

```
## The following objects are masked from 'package:data.table':
## 
##     between, first, last
```

```
## The following objects are masked from 'package:stats':
## 
##     filter, lag
```

```
## The following objects are masked from 'package:base':
## 
##     intersect, setdiff, setequal, union
```



Before we start the image processing steps, let's read in and plot an image. This
image is an example image that comes with the *hazer* package.



```r
# read the path to the example image
jpeg_file <- system.file(package = 'hazer', 'pointreyes.jpg')

# read the image as an array
rgb_array <- jpeg::readJPEG(jpeg_file)

# plot the RGB array on the active device panel


# first set the margin in this order:(bottom, left, top, right)
par(mar=c(0,0,3,0))  
plotRGBArray(rgb_array, bty = 'n', main = 'Point Reyes National Seashore')
```

<img src="05-PhenoCam_files/figure-html/unnamed-chunk-17-1.png" width="672" />


When we work with images, all data we work with is generally on the scale of each
individual pixel in the image. Therefore, for large images we will be working with
large matrices that hold the value for each pixel. Keep this in mind before opening
some of the matrices we'll be creating this tutorial as it can take a while for
them to load.

#### Histogram of RGB channels

A histogram of the colors can be useful to understanding what our image is made
up of. Using the `density()` function from the base *stats* package, we can extract
density distribution of each color channel.



```r
# color channels can be extracted from the matrix
red_vector <- rgb_array[,,1]
green_vector <- rgb_array[,,2]
blue_vector <- rgb_array[,,3]

# plotting
par(mar=c(5,4,4,2))
plot(density(red_vector), col = 'red', lwd = 2,
     main = 'Density function of the RGB channels', ylim = c(0,5))
lines(density(green_vector), col = 'green', lwd = 2)
lines(density(blue_vector), col = 'blue', lwd = 2)
```

<img src="05-PhenoCam_files/figure-html/unnamed-chunk-18-1.png" width="672" />


In *hazer* we can also extract three basic elements of an RGB image :

1. Brightness
2. Darkness
3. Contrast

#### Brightness

The brightness matrix comes from the maximum value of the R, G, or B channel. We
can extract and show the brightness matrix using the `getBrightness()` function.



```r
# extracting the brightness matrix
brightness_mat <- getBrightness(rgb_array)

# unlike the RGB array which has 3 dimensions, the brightness matrix has only two
# dimensions and can be shown as a grayscale image,
# we can do this using the same plotRGBArray function
par(mar=c(0,0,3,0))
plotRGBArray(brightness_mat, bty = 'n', main = 'Brightness matrix')
```

<img src="05-PhenoCam_files/figure-html/unnamed-chunk-19-1.png" width="672" />


Here the grayscale is used to show the value of each pixel's maximum brightness
of the R, G or B color channel.

To extract a single brightness value for the image, depending on our needs we can
perform some statistics or we can just use the mean of this matrix.



```r
# the main quantiles
quantile(brightness_mat)
```

```
##         0%        25%        50%        75%       100% 
## 0.09019608 0.43529412 0.62745098 0.80000000 0.91764706
```



```r
# create histogram
par(mar=c(5,4,4,2))
hist(brightness_mat)
```

<img src="05-PhenoCam_files/figure-html/unnamed-chunk-21-1.png" width="672" />


**Question for the class:** Why are we getting so many images up in the high range of the brightness? Where
does this correlate to on the RGB image?

#### Darkness

Darkness is determined by the minimum of the R, G or B color channel. In the
Similarly, we can extract and show the darkness matrix using the `getDarkness()` function.



```r
# extracting the darkness matrix
darkness_mat <- getDarkness(rgb_array)

# the darkness matrix has also two dimensions and can be shown as a grayscale image
par(mar=c(0,0,3,0))
plotRGBArray(darkness_mat, bty = 'n', main = 'Darkness matrix')
```

<img src="05-PhenoCam_files/figure-html/unnamed-chunk-22-1.png" width="672" />

```r
# main quantiles
quantile(darkness_mat)
```

```
##         0%        25%        50%        75%       100% 
## 0.03529412 0.23137255 0.36470588 0.47843137 0.83529412
```




```r
# histogram
par(mar=c(5,4,4,2))
hist(darkness_mat)
```

<img src="05-PhenoCam_files/figure-html/unnamed-chunk-23-1.png" width="672" />



#### Contrast

The contrast of an image is the difference between the darkness and brightness
of the image. The contrast matrix is calculated by difference between the
darkness and brightness matrices.

The contrast of the image can quickly be extracted using the `getContrast()` function.



```r
# extracting the contrast matrix
contrast_mat <- getContrast(rgb_array)

# the contrast matrix has also 2D and can be shown as a grayscale image
par(mar=c(0,0,3,0))
plotRGBArray(contrast_mat, bty = 'n', main = 'Contrast matrix')
```

<img src="05-PhenoCam_files/figure-html/unnamed-chunk-24-1.png" width="672" />

```r
# main quantiles
quantile(contrast_mat)
```

```
##        0%       25%       50%       75%      100% 
## 0.0000000 0.1450980 0.2470588 0.3333333 0.4509804
```



```r
# histogram
par(mar=c(5,4,4,2))
hist(contrast_mat)
```

<img src="05-PhenoCam_files/figure-html/unnamed-chunk-25-1.png" width="672" />


#### Image fogginess & haziness

Haziness of an image can be estimated using the `getHazeFactor()` function. This
function is based on the method described in
<a href="https://www.omicsonline.org/open-access/detecting-foggy-images-and-estimating-the-haze-degree-factor-jcsb.1000226.pdf">Mao et al. (2014)</a>.
The technique was originally developed to for *"detecting foggy images and
estimating the haze degree factor"* for a wide range of outdoor conditions.

The function returns a vector of two numeric values:

1.  **haze** as the haze degree and
2.  **A0** as the global atmospheric light, as it is explained in the original paper.

The PhenoCam standards classify any image with the haze degree greater
than 0.4 as a significantly foggy image.



```r
# extracting the haze matrix
haze_degree <- getHazeFactor(rgb_array)

print(haze_degree)
```

```
## $haze
## [1] 0.2251633
## 
## $A0
## [1] 0.7105258
```


Here we have the haze values for our image. Note that the values might be
slightly different due to rounding errors on different platforms.

#### Process sets of images

We can use `for` loops or the `lapply` functions to extract the haze values for
a stack of images.

You can download the related datasets from
<a href="http://bit.ly/2F8w2Ia">here (direct download)</a>.
Download and extract the zip file to be used as input data for the following step.



```r
#pointreyes_url <- 'http://bit.ly/2F8w2Ia'

# set up the input image directory
data_dir <- 'data/'
#dir.create(data_dir, showWarnings = F)

#pointreyes_zip <- paste0(data_dir, 'pointreyes.zip')
pointreyes_dir <- paste0(data_dir, 'pointreyes')

#download zip file
#download.file(pointreyes_url, destfile = pointreyes_zip)
#unzip(pointreyes_zip, exdir = data_dir)

# get a list of all .jpg files in the directory
pointreyes_images <- dir(path = 'data/pointreyes',
                         pattern = '*.jpg',
                         ignore.case = TRUE,
                         full.names = TRUE)
```


Now we can use a for loop to process all of the images to get the haze and A0
values.



```r
# number of images
n <- length(pointreyes_images)

# create an empty matrix to fill with haze and A0 values
haze_mat <- data.frame()

# the process takes a bit, a progress bar lets us know it is working.
pb <- txtProgressBar(0, n, style = 3)
```

```
## 
```



```r
for(i in 1:n) {
  image_path <- pointreyes_images[i]
  img <- jpeg::readJPEG(image_path)
  hz <- getHazeFactor(img)

  haze_mat <- rbind(haze_mat,
                    data.frame(file = as.character(image_path),
                               haze = hz[1],
                               A0 = hz[2]))

  setTxtProgressBar(pb, i)
}
```

```
## 
```


Now we have a matrix with haze and A0 values for all our images. Let's
compare top three images with low and high haze values.



```r
top10_high_haze <- haze_mat %>%
  dplyr::arrange(desc(haze)) %>%
  slice(1:3)
top10_low_haze <-  haze_mat %>%
  arrange(haze)%>%
  slice(1:3)


par(mar= c(0,0,0,0), mfrow=c(3,2), oma=c(0,0,3,0))

for(i in 1:3){
  img <- readJPEG(as.character(top10_low_haze$file[i]))
  plot.new()
  rasterImage(img, par()$usr[1], par()$usr[3], par()$usr[2], par()$usr[4])

  img <- readJPEG(as.character(top10_high_haze$file[i]))
  plot.new()
  rasterImage(img, par()$usr[1], par()$usr[3], par()$usr[2], par()$usr[4])

}
mtext('Top images with low (left) and high (right) haze values at Point Reyes', font = 2, outer = TRUE)
```

<img src="05-PhenoCam_files/figure-html/unnamed-chunk-30-1.png" width="672" />


Let's classify those into hazy and non-hazy as per the PhenoCam standard of 0.4.



```r
# classify image as hazy: T/F
haze_mat=haze_mat%>%
  mutate(haze_mat, foggy=ifelse(haze>.4, TRUE, FALSE))

head(haze_mat)
```

```
##                                               file      haze        A0 foggy
## 1 data/pointreyes/pointreyes_2017_01_01_120056.jpg 0.2249810 0.6970257 FALSE
## 2 data/pointreyes/pointreyes_2017_01_06_120210.jpg 0.2339372 0.6826148 FALSE
## 3 data/pointreyes/pointreyes_2017_01_16_120105.jpg 0.2312940 0.7009978 FALSE
## 4 data/pointreyes/pointreyes_2017_01_21_120105.jpg 0.4536108 0.6209055  TRUE
## 5 data/pointreyes/pointreyes_2017_01_26_120106.jpg 0.2297961 0.6813884 FALSE
## 6 data/pointreyes/pointreyes_2017_01_31_120125.jpg 0.4206842 0.6315728  TRUE
```


Now we can save all the foggy images to a new folder that will retain the
foggy images but keep them separate from the non-foggy ones that we want to
analyze.



```r
# identify directory to move the foggy images to
foggy_dir <- paste0(pointreyes_dir, 'foggy')
clear_dir <- paste0(pointreyes_dir, 'clear')

# if a new directory, create new directory at this file path
dir.create(foggy_dir,  showWarnings = FALSE)
dir.create(clear_dir,  showWarnings = FALSE)

# copy the files to the new directories
#file.copy(haze_mat[foggy==TRUE,file], to = foggy_dir)

#file.copy(haze_mat[foggy==FALSE,file], to = clear_dir)
```

Now that we have our images separated, we can get the full list of haze
values only for those images that are not classified as "foggy".  



```r
# this is an alternative approach instead of a for loop

# loading all the images as a list of arrays
pointreyes_clear_images <- dir(path = clear_dir,
                               pattern = '*.jpg',
                               ignore.case = TRUE,
                               full.names = TRUE)

img_list <- lapply(pointreyes_clear_images, FUN = jpeg::readJPEG)

# getting the haze value for the list
# patience - this takes a bit of time
haze_list <- t(sapply(img_list, FUN = getHazeFactor))

# view first few entries
head(haze_list)
```

```
##      haze      A0       
## [1,] 0.224981  0.6970257
## [2,] 0.2339372 0.6826148
## [3,] 0.231294  0.7009978
## [4,] 0.2297961 0.6813884
## [5,] 0.2152078 0.6949932
## [6,] 0.345584  0.6789334
```


We can then use these values for further analyses and data correction.


***

The *hazer* R package is developed and maintained by
<a href="https://bnasr.github.io/">Bijan Seyednarollah</a>.
The most recent release is available from
<a href="https://github.com/bnasr/hazer" target="_blank">https://github.com/bnasr/hazer</a>.


## Extracting Timeseries from Images using the xROI R Package

In this section, we'll learn how to use an interactive open-source toolkit, the
<a href="https://cran.r-project.org/web/packages/xROI/index.html" target="_blank">xROI R package</a>
that facilitates the process of time series extraction and improves the quality
of the final data. The xROI package provides a responsive environment for
scientists to interactively:

a) delineate regions of interest (ROIs),
b) handle field of view (FOV) shifts, and
c) extract and export time series data characterizing color-based metrics.

Using the *xROI* R package, the user can detect FOV shifts with minimal difficulty.
The software gives user the opportunity to re-adjust mask files or redraw new
ones every time an FOV shift occurs.

<img src="docs/images/xROI.png" width="544" />

### xROI Design


The R language and Shiny package were used as the main development tool for xROI,
while Markdown, HTML, CSS and JavaScript languages were used to improve the
interactivity. While Shiny apps are primarily used for web-based applications to
be used online, the package authors used Shiny for its graphical user interface
capabilities. In other words, both the User Interface (UI) and server modules are run
locally from the same machine and hence no internet connection is required (after
installation). The xROI's UI element presents a side-panel for data entry and
three main tab-pages, each responsible for a specific task. The server-side
element consists of R and bash scripts. Image processing and geospatial features
were performed using the `Geospatial Data Abstraction Library (GDAL)` and the
`rgdal` and `raster` R packages.

### Install xROI

The xROI R package has been published on The Comprehensive R Archive Network (CRAN).
The latest tested xROI package can be installed from the
<a href="https://cran.r-project.org/package=xROI" target="_blank">CRAN packages repository</a> by running the following command in an R environment.



```r
utils::install.packages('xROI', repos = "http://cran.us.r-project.org" )
```

Alternatively, the latest beta release of xROI can be directly downloaded and
installed from the development GitHub repository.



```r
# install devtools first
utils::install.packages('devtools', repos = "http://cran.us.r-project.org" )

# use devtools to install from GitHub
devtools::install_github("bnasr/xROI")
```

xROI depends on many R packages including: `raster`, `rgdal`, `sp`, `jpeg`,
`tiff`, `shiny`, `shinyjs`, `shinyBS`, `shinyAce`, `shinyTime`, `shinyFiles`,
`shinydashboard`, `shinythemes`, `colourpicker`, `rjson`, `stringr`, `data.table`,
`lubridate`, `plotly`, `moments`, and `RCurl`. All the required libraries and
packages will be automatically installed with installation of *xROI*. The package
offers a fully interactive high-level interface as well as a set of low-level
functions for ROI processing.

### Launch xROI

A comprehensive user manual for low-level image processing using *xROI* is available from
<a href="https://cran.r-project.org/package=xROI/xROI.pdf" target="_blank">CRAN xROI.pdf</a>.
While the user manual includes a set of examples for each function; here we
will learn to use the graphical interactive mode.

Calling the `Launch()` function, as we'll do below, opens up the interactive
mode in your operating system’s default web browser. The landing page offers an
example dataset to explore different modules or upload a new dataset of images.

You can launch the interactive mode can be launched from an interactive R environment.



```r
# load xROI
library(xROI)

# launch xROI
Launch()
```

Or from the command line (e.g. bash in Linux, Terminal in macOS and Command
Prompt in Windows machines) where an R engine is already installed.


```bash

Rscript -e “xROI::Launch(Interactive = TRUE)”

```


### End xROI

When you are done with the xROI interface you can close the tab in your browser
and end the session in R by using one of the following options

**In RStudio:** Press the <Esc> key on your keyboard.
**In R Terminal:** Press <Ctrl + C> on your keyboard.

### Use xROI

To get some hands-on experience with `xROI`, we can analyze images from the
<a href="https://phenocam.sr.unh.edu/webcam/sites/dukehw/">dukehw</a>
of the PhenoCam network.

You can download the data set from
<a href="http://bit.ly/2PzZ2fL">this link (direct download)</a>.

Follow the steps below:

First,save and extract (unzip) the file on your computer.

Second, open the data set in `xROI` by setting the file path to your data



```r
# launch data in ROI
# first edit the path below to the dowloaded directory you just extracted
xROI::Launch('/path/to/extracted/directory')

# alternatively, you can run without specifying a path and use the interface to browse
```

Now, draw an ROI and the metadata.

Then, save the metadata and explore its content.

Now we can explore if there is any FOV shift in the dataset using the `CLI processer` tab.

Finally, we can go to the `Time series extraction` tab. Extract the time-series. Save the output and explore the dataset in R.


## Documentation and Citation

More documentation about **xROI** can be found from: <a href="https://bnasr.github.io/papers/Seyednasrollah_et_al_2019_PRS.pdf">Seyednarollah, et al. 2019</a>.


```r
knitr::include_graphics('docs/images/xROI-ms2019.png')
```

<img src="docs/images/xROI-ms2019.png" width="694" />
>xROI published in ISPRS Journal of Photogrammetry and Remote Sensing, 2019

### Challenge: Use xROI

Let's use xROI on a little more challenging site with field of view shifts.

Download and extract the data set from
<a href="http://bit.ly/2DrZgA1">this link (direct download, 218 MB)</a>
and follow the above steps to extract the time-series.


The *xROI* R package is developed and maintained by
<a href="https://bnasr.github.io/">Bijan Seyednarollah</a>.
The most recent release is available from <a href="https://github.com/bnasr/xROI" target="_blank">https://github.com/bnasr/xROI</a>.



## Hands on: Digital Repeat Photography Computational
First let's load some packages:



```r
library(jsonlite)
```

```
## 
## Attaching package: 'jsonlite'
```

```
## The following objects are masked from 'package:rjson':
## 
##     fromJSON, toJSON
```

```r
library(phenocamapi)
library(plotly)
```

```
## Loading required package: ggplot2
```

```
## 
## Attaching package: 'plotly'
```

```
## The following object is masked from 'package:ggplot2':
## 
##     last_plot
```

```
## The following object is masked from 'package:stats':
## 
##     filter
```

```
## The following object is masked from 'package:graphics':
## 
##     layout
```

```r
library(phenocamr)
library(dplyr)
```

As a refresher, there are two main ways to pull in PhenoCam data.  First, directly via the API:


```r
c      = jsonlite::fromJSON('https://phenocam.sr.unh.edu/api/cameras/?format=json&limit=2000')
c = c$results
c_m=c$sitemetadata
c$sitemetadata=NULL
cams_=cbind(c, c_m)
cams_[is.na(cams_)] = 'N'
cams_[, 2:4] <- sapply(cams_[, 2:4], as.numeric) #changing lat/lon/elev from string values into numeric
```

```
## Warning in lapply(X = X, FUN = FUN, ...): NAs introduced by coercion

## Warning in lapply(X = X, FUN = FUN, ...): NAs introduced by coercion

## Warning in lapply(X = X, FUN = FUN, ...): NAs introduced by coercion
```

```r
head(cams_)
```

```
##             Sitename      Lat        Lon Elev active utc_offset date_first
## 1 aafcottawacfiaf14e 45.29210  -75.76640   90   TRUE         -5 2020-04-27
## 2 aafcottawacfiaf14w 45.29210  -75.76640   90   TRUE         -5 2020-05-01
## 3             acadia 44.37694  -68.26083  158   TRUE         -5 2007-03-15
## 4      aguatibiaeast 33.62200 -116.86700 1086  FALSE         -8 2007-08-16
## 5     aguatibianorth 33.60222 -117.34368 1090  FALSE         -8 2003-10-01
## 6           ahwahnee 37.74670 -119.58160 1199   TRUE         -8 2008-08-28
##    date_last infrared                                                 contact1
## 1 2020-09-28        N Elizabeth Pattey <elizabeth DOT pattey AT canada DOT ca>
## 2 2020-09-28        N Elizabeth Pattey <elizabeth DOT pattey AT canada DOT ca>
## 3 2020-10-12        N                     Dee Morse <dee_morse AT nps DOT gov>
## 4 2019-01-25        N              Ann E Mebane <amebane AT fs DOT fed DOT us>
## 5 2006-10-25        N                                                         
## 6 2020-10-12        N                     Dee Morse <dee_morse AT nps DOT gov>
##                                              contact2
## 1 Luc Pelletier <luc DOT pelletier3 AT canada DOT ca>
## 2 Luc Pelletier <luc DOT pelletier3 AT canada DOT ca>
## 3              John Gross <John_Gross AT nps DOT gov>
## 4       Kristi Savig <KSavig AT air-resource DOT com>
## 5                                                    
## 6              John Gross <John_Gross AT nps DOT gov>
##                                               site_description site_type
## 1  AAFC Site - Ottawa (On) - CFIA - Field F14 -East Flux Tower        II
## 2  AAFC Site - Ottawa (On) - CFIA - Field F14 -West Flux Tower        II
## 3 Acadia National Park, McFarland Hill, near Bar Harbor, Maine       III
## 4                            Agua Tibia Wilderness, California       III
## 5                            Agua Tibia Wilderness, California       III
## 6          Ahwahnee Meadow, Yosemite National Park, California       III
##                   group       camera_description camera_orientation flux_data
## 1                     N Campbell Scientific CCFC                 NE      TRUE
## 2                     N Campbell Scientific CCFC                WNW      TRUE
## 3 National Park Service                  unknown                 NE     FALSE
## 4                  USFS                  unknown                 SW     FALSE
## 5                  USFS                  unknown                 NE     FALSE
## 6 National Park Service                  unknown                  E     FALSE
##                 flux_networks flux_sitenames
## 1                        NULL              N
## 2 OTHER, , Other/Unaffiliated              N
## 3                        NULL               
## 4                        NULL               
## 5                        NULL               
## 6                        NULL               
##                                           dominant_species primary_veg_type
## 1 Zea mays, Triticum aestivum, Brassica napus, Glycine max               AG
## 2 Zea mays, Triticum aestivum, Brassica napus, Glycine max               AG
## 3                                                                        DB
## 4                                                                        SH
## 5                                                                        SH
## 6                                                                        EN
##   secondary_veg_type site_meteorology MAT_site MAP_site MAT_daymet MAP_daymet
## 1                 AG             TRUE      6.4      943        6.3        952
## 2                 AG             TRUE      6.4      943        6.3        952
## 3                 EN            FALSE        N        N       7.05       1439
## 4                               FALSE        N        N      15.75        483
## 5                               FALSE        N        N         16        489
## 6                 GR            FALSE        N        N      12.25        871
##   MAT_worldclim MAP_worldclim koeppen_geiger ecoregion landcover_igbp
## 1             6           863            Dfb         8             12
## 2             6           863            Dfb         8             12
## 3           6.5          1303            Dfb         8              5
## 4          14.9           504            Csa        11              7
## 5          13.8           729            Csa        11              7
## 6          11.8           886            Csb         6              8
##                                                                                                                                                                                                                                                                                                                         site_acknowledgements
## 1  Camera funded by Agriculture and Agri-Food Canada (AAFC) Project J-001735 - Commercial inhibitors’ impact on crop productivity and emissions of nitrous oxide led by Dr. Elizabeth Pattey; Support provided by Drs, Luc Pelletier and Elizabeth  Pattey, Micrometeorologiccal Laboratory of AAFC - Ottawa Research and Development Centre.
## 2 Cameras funded by Agriculture and Agri-Food Canada (AAFC) Project J-001735 - Commercial inhibitors’ impact on crop productivity and emissions of nitrous oxide led by Dr. Elizabeth Pattey; Support provided by Drs, Luc Pelletier and Elizabeth  Pattey, Micrometeorologiccal Laboratory of AAFC - Ottawa Research and Development Centre.
## 3                                                                                                                                                                                                                           Camera images from Acadia National Park are provided courtesy of the National Park Service Air Resources Program.
## 4                                                                                                                                                                                                                 Camera images from Agua Tibia Wilderness are provided courtesy of the USDA Forest Service Air Resources Management Program.
## 5                                                                                                                                                                                                                 Camera images from Agua Tibia Wilderness are provided courtesy of the USDA Forest Service Air Resources Management Program.
## 6                                                                                                                                                                                                                         Camera images from Yosemite National Park are provided courtesy of the National Park Service Air Resources Program.
##                           modified
## 1 2020-05-04T10:46:30.065790-04:00
## 2 2020-05-04T10:46:32.523976-04:00
## 3 2016-11-01T15:42:15.016778-04:00
## 4 2016-11-01T15:42:15.086984-04:00
## 5 2016-11-01T15:42:15.095277-04:00
## 6 2016-11-01T15:42:15.111916-04:00
```

And second, via the phenocamapi package:



```r
phenos=get_phenos()
head(phenos)
```

```
##                  site      lat        lon elev active utc_offset date_first
## 1: aafcottawacfiaf14e 45.29210  -75.76640   90   TRUE         -5 2020-04-27
## 2: aafcottawacfiaf14w 45.29210  -75.76640   90   TRUE         -5 2020-05-01
## 3:             acadia 44.37694  -68.26083  158   TRUE         -5 2007-03-15
## 4:      aguatibiaeast 33.62200 -116.86700 1086  FALSE         -8 2007-08-16
## 5:     aguatibianorth 33.60222 -117.34368 1090  FALSE         -8 2003-10-01
## 6:           ahwahnee 37.74670 -119.58160 1199   TRUE         -8 2008-08-28
##     date_last infrared                                      contact1
## 1: 2020-09-28        N Elizabeth Pattey <elizabeth.pattey@canada.ca>
## 2: 2020-09-28        N Elizabeth Pattey <elizabeth.pattey@canada.ca>
## 3: 2020-10-12        N                 Dee Morse <dee_morse@nps.gov>
## 4: 2019-01-25        N              Ann E Mebane <amebane@fs.fed.us>
## 5: 2006-10-25        N                                              
## 6: 2020-10-12        N                 Dee Morse <dee_morse@nps.gov>
##                                    contact2
## 1: Luc Pelletier <luc.pelletier3@canada.ca>
## 2: Luc Pelletier <luc.pelletier3@canada.ca>
## 3:          John Gross <John_Gross@nps.gov>
## 4:   Kristi Savig <KSavig@air-resource.com>
## 5:                                         
## 6:          John Gross <John_Gross@nps.gov>
##                                                site_description site_type
## 1:  AAFC Site - Ottawa (On) - CFIA - Field F14 -East Flux Tower        II
## 2:  AAFC Site - Ottawa (On) - CFIA - Field F14 -West Flux Tower        II
## 3: Acadia National Park, McFarland Hill, near Bar Harbor, Maine       III
## 4:                            Agua Tibia Wilderness, California       III
## 5:                            Agua Tibia Wilderness, California       III
## 6:          Ahwahnee Meadow, Yosemite National Park, California       III
##                    group       camera_description camera_orientation flux_data
## 1:                  <NA> Campbell Scientific CCFC                 NE      TRUE
## 2:                  <NA> Campbell Scientific CCFC                WNW      TRUE
## 3: National Park Service                  unknown                 NE     FALSE
## 4:                  USFS                  unknown                 SW     FALSE
## 5:                  USFS                  unknown                 NE     FALSE
## 6: National Park Service                  unknown                  E     FALSE
##    flux_networks flux_sitenames
## 1:     <list[0]>           <NA>
## 2:     <list[1]>           <NA>
## 3:     <list[0]>               
## 4:     <list[0]>               
## 5:     <list[0]>               
## 6:     <list[0]>               
##                                            dominant_species primary_veg_type
## 1: Zea mays, Triticum aestivum, Brassica napus, Glycine max               AG
## 2: Zea mays, Triticum aestivum, Brassica napus, Glycine max               AG
## 3:                                                                        DB
## 4:                                                                        SH
## 5:                                                                        SH
## 6:                                                                        EN
##    secondary_veg_type site_meteorology MAT_site MAP_site MAT_daymet MAP_daymet
## 1:                 AG             TRUE      6.4      943       6.30        952
## 2:                 AG             TRUE      6.4      943       6.30        952
## 3:                 EN            FALSE       NA       NA       7.05       1439
## 4:                               FALSE       NA       NA      15.75        483
## 5:                               FALSE       NA       NA      16.00        489
## 6:                 GR            FALSE       NA       NA      12.25        871
##    MAT_worldclim MAP_worldclim koeppen_geiger ecoregion landcover_igbp
## 1:           6.0           863            Dfb         8             12
## 2:           6.0           863            Dfb         8             12
## 3:           6.5          1303            Dfb         8              5
## 4:          14.9           504            Csa        11              7
## 5:          13.8           729            Csa        11              7
## 6:          11.8           886            Csb         6              8
##    dataset_version1
## 1:               NA
## 2:               NA
## 3:               NA
## 4:               NA
## 5:               NA
## 6:               NA
##                                                                                                                                                                                                                                                                                                                          site_acknowledgements
## 1:  Camera funded by Agriculture and Agri-Food Canada (AAFC) Project J-001735 - Commercial inhibitors’ impact on crop productivity and emissions of nitrous oxide led by Dr. Elizabeth Pattey; Support provided by Drs, Luc Pelletier and Elizabeth  Pattey, Micrometeorologiccal Laboratory of AAFC - Ottawa Research and Development Centre.
## 2: Cameras funded by Agriculture and Agri-Food Canada (AAFC) Project J-001735 - Commercial inhibitors’ impact on crop productivity and emissions of nitrous oxide led by Dr. Elizabeth Pattey; Support provided by Drs, Luc Pelletier and Elizabeth  Pattey, Micrometeorologiccal Laboratory of AAFC - Ottawa Research and Development Centre.
## 3:                                                                                                                                                                                                                           Camera images from Acadia National Park are provided courtesy of the National Park Service Air Resources Program.
## 4:                                                                                                                                                                                                                 Camera images from Agua Tibia Wilderness are provided courtesy of the USDA Forest Service Air Resources Management Program.
## 5:                                                                                                                                                                                                                 Camera images from Agua Tibia Wilderness are provided courtesy of the USDA Forest Service Air Resources Management Program.
## 6:                                                                                                                                                                                                                         Camera images from Yosemite National Park are provided courtesy of the National Park Service Air Resources Program.
##                            modified flux_networks_name flux_networks_url
## 1: 2020-05-04T10:46:30.065790-04:00               <NA>              <NA>
## 2: 2020-05-04T10:46:32.523976-04:00              OTHER                  
## 3: 2016-11-01T15:42:15.016778-04:00               <NA>              <NA>
## 4: 2016-11-01T15:42:15.086984-04:00               <NA>              <NA>
## 5: 2016-11-01T15:42:15.095277-04:00               <NA>              <NA>
## 6: 2016-11-01T15:42:15.111916-04:00               <NA>              <NA>
##    flux_networks_description
## 1:                      <NA>
## 2:        Other/Unaffiliated
## 3:                      <NA>
## 4:                      <NA>
## 5:                      <NA>
## 6:                      <NA>
```

To familiarize yourself with the phenocam API, let's explore the structure:
[https://phenocam.sr.unh.edu/api/](https://phenocam.sr.unh.edu/api/)

Explore the options for filtering, file type and so forth.

### PhenoCam time series

PhenoCam time series are extracted time series data obtained from ROI's for a
given site.

### Obtain ROIs
To download the phenological time series from the PhenoCam, we need to know the
site name, vegetation type and ROI ID. This information can be obtained from each
specific PhenoCam page on the
<a href="https://phenocam.sr.unh.edu/webcam/gallery/" target="_blank">PhenoCam website</a>
or by using the `get_rois()` function.




```r
# obtaining the list of all the available ROI's on the PhenoCam server
rois <- get_rois()

# view what information is returned
colnames(rois)
```

```
##  [1] "roi_name"          "site"              "lat"              
##  [4] "lon"               "roitype"           "active"           
##  [7] "show_link"         "show_data_link"    "sequence_number"  
## [10] "description"       "first_date"        "last_date"        
## [13] "site_years"        "missing_data_pct"  "roi_page"         
## [16] "roi_stats_file"    "one_day_summary"   "three_day_summary"
## [19] "data_release"
```

```r
# view first few locations
head(rois$roi_name)
```

```
## [1] "alligatorriver_DB_1000"   "arbutuslake_DB_1000"     
## [3] "arbutuslakeinlet_DB_1000" "arbutuslakeinlet_EN_1000"
## [5] "arbutuslakeinlet_EN_2000" "archboldavir_AG_1000"
```

### Download time series

The `get_pheno_ts()` function can download a time series and return the result
as a `data.table`.
Let's work with the
<a href="https://phenocam.sr.unh.edu/data/archive/dukehw/ROI/dukehw_DB_1000.html">Duke Forest Hardwood Stand (`dukehw`) PhenoCam</a>
and specifically the ROI
<a href="https://phenocam.sr.unh.edu/data/archive/dukehw/ROI/dukehw_DB_1000.html">`DB_1000`</a>
we can run the following code.



```r
# list ROIs for dukehw
rois[site=='dukehw',]
```

```
##          roi_name   site      lat       lon roitype active show_link
## 1: dukehw_DB_1000 dukehw 35.97358 -79.10037      DB   TRUE      TRUE
##    show_data_link sequence_number                                   description
## 1:           TRUE            1000 canopy level DB forest at awesome Duke forest
##    first_date  last_date site_years missing_data_pct
## 1: 2013-06-01 2020-10-13        7.2              3.0
##                                                  roi_page
## 1: https://phenocam.sr.unh.edu/webcam/roi/dukehw/DB_1000/
##                                                                     roi_stats_file
## 1: https://phenocam.sr.unh.edu/data/archive/dukehw/ROI/dukehw_DB_1000_roistats.csv
##                                                                one_day_summary
## 1: https://phenocam.sr.unh.edu/data/archive/dukehw/ROI/dukehw_DB_1000_1day.csv
##                                                              three_day_summary
## 1: https://phenocam.sr.unh.edu/data/archive/dukehw/ROI/dukehw_DB_1000_3day.csv
##    data_release
## 1:           NA
```

```r
# to obtain the DB 1000 from dukehw
dukehw_DB_1000 <- get_pheno_ts(site = 'dukehw', vegType = 'DB', roiID = 1000, type = '3day')

# what data are available
str(dukehw_DB_1000)
```

```
## Classes 'data.table' and 'data.frame':	900 obs. of  35 variables:
##  $ date                : Factor w/ 900 levels "2013-06-01","2013-06-04",..: 1 2 3 4 5 6 7 8 9 10 ...
##  $ year                : int  2013 2013 2013 2013 2013 2013 2013 2013 2013 2013 ...
##  $ doy                 : int  152 155 158 161 164 167 170 173 176 179 ...
##  $ image_count         : int  57 76 77 77 77 78 21 0 0 0 ...
##  $ midday_filename     : Factor w/ 871 levels "dukehw_2013_06_01_120111.jpg",..: 1 2 3 4 5 6 7 871 871 871 ...
##  $ midday_r            : num  91.3 76.4 60.6 76.5 88.9 ...
##  $ midday_g            : num  97.9 85 73.2 82.2 95.7 ...
##  $ midday_b            : num  47.4 33.6 35.6 37.1 51.4 ...
##  $ midday_gcc          : num  0.414 0.436 0.432 0.42 0.406 ...
##  $ midday_rcc          : num  0.386 0.392 0.358 0.391 0.377 ...
##  $ r_mean              : num  87.6 79.9 72.7 80.9 83.8 ...
##  $ r_std               : num  5.9 6 9.5 8.23 5.89 ...
##  $ g_mean              : num  92.1 86.9 84 88 89.7 ...
##  $ g_std               : num  6.34 5.26 7.71 7.77 6.47 ...
##  $ b_mean              : num  46.1 38 39.6 43.1 46.7 ...
##  $ b_std               : num  4.48 3.42 5.29 4.73 4.01 ...
##  $ gcc_mean            : num  0.408 0.425 0.429 0.415 0.407 ...
##  $ gcc_std             : num  0.00859 0.0089 0.01318 0.01243 0.01072 ...
##  $ gcc_50              : num  0.408 0.427 0.431 0.416 0.407 ...
##  $ gcc_75              : num  0.414 0.431 0.435 0.424 0.415 ...
##  $ gcc_90              : num  0.417 0.434 0.44 0.428 0.421 ...
##  $ rcc_mean            : num  0.388 0.39 0.37 0.381 0.38 ...
##  $ rcc_std             : num  0.01176 0.01032 0.01326 0.00881 0.00995 ...
##  $ rcc_50              : num  0.387 0.391 0.373 0.383 0.382 ...
##  $ rcc_75              : num  0.391 0.396 0.378 0.388 0.385 ...
##  $ rcc_90              : num  0.397 0.399 0.382 0.391 0.389 ...
##  $ max_solar_elev      : num  76 76.3 76.6 76.8 76.9 ...
##  $ snow_flag           : logi  NA NA NA NA NA NA ...
##  $ outlierflag_gcc_mean: logi  NA NA NA NA NA NA ...
##  $ outlierflag_gcc_50  : logi  NA NA NA NA NA NA ...
##  $ outlierflag_gcc_75  : logi  NA NA NA NA NA NA ...
##  $ outlierflag_gcc_90  : logi  NA NA NA NA NA NA ...
##  $ YEAR                : int  2013 2013 2013 2013 2013 2013 2013 2013 2013 2013 ...
##  $ DOY                 : int  152 155 158 161 164 167 170 173 176 179 ...
##  $ YYYYMMDD            : chr  "2013-06-01" "2013-06-04" "2013-06-07" "2013-06-10" ...
##  - attr(*, ".internal.selfref")=<externalptr>
```

We now have a variety of data related to this ROI from the Hardwood Stand at Duke
Forest.

Green Chromatic Coordinate (GCC) is a measure of "greenness" of an area and is
widely used in Phenocam images as an indicator of the green pigment in vegetation.
Let's use this measure to look at changes in GCC over time at this site. Looking
back at the available data, we have several options for GCC. `gcc90` is the 90th
quantile of GCC in the pixels across the ROI (for more details,
<a href="https://daac.ornl.gov/VEGETATION/guides/PhenoCam_V1.html" target="_blank"> PhenoCam v1 description</a>).
We'll use this as it tracks the upper greenness values while not including many
outliners.  

Before we can plot `gcc-90` we do need to fix our dates and convert them from
Factors to Date to correctly plot.



```r
# date variable into date format
dukehw_DB_1000[,date:=as.Date(date)]

# plot gcc_90
dukehw_DB_1000[,plot(date, gcc_90, col = 'green', type = 'b')]
```

```
## NULL
```

```r
mtext('Duke Forest, Hardwood', font = 2)
```

<img src="05-PhenoCam_files/figure-html/unnamed-chunk-45-1.png" width="672" />

Now, based on either direct API access or via the phenocamapi package, generate a dataframe of phenocam sites.  Select two phenocam sites from *different* plant functional types to explore (e.g. one grassland site and one evergreen needleleaf site)



```r
#example
GrassSites=cams_%>%
  filter(cams_$primary_veg_type=='GR')
head(GrassSites)
```

```
##        Sitename      Lat        Lon Elev active utc_offset date_first
## 1 archboldbahia 27.16560  -81.21611    8   TRUE         -5 2017-03-21
## 2  arizonagrass 31.59070 -110.50920 1469  FALSE         -7 2008-01-01
## 3      arsgacp2 31.43950  -83.59146  101  FALSE          2 2016-04-27
## 4       bozeman 45.78306 -110.77778 2332  FALSE         -7 2015-08-16
## 5         butte 45.95304 -112.47964 1682   TRUE         -7 2008-04-01
## 6  coaloilpoint 34.41369 -119.88023    6  FALSE         -8 2008-05-11
##    date_last infrared                                              contact1
## 1 2020-10-12        Y      Amartya Saha <asaha AT archbold-station DOT org>
## 2 2010-04-25        N           Mark Heuer <Mark DOT Heuer AT noaa DOT gov>
## 3 2018-01-23        Y David Bosch <David DOT Bosch AT ars DOT usda DOT gov>
## 4 2019-12-18        Y            Paul Stoy <paul DOT stoy AT gmail DOT com>
## 5 2020-10-12        N       James Gallagher <jgallagher AT opendap DOT org>
## 6 2012-12-05        N                Roberts <dar AT geog DOT ucsb DOT edu>
##                                                     contact2
## 1 Elizabeth Boughton <eboughton AT archbold-station DOT org>
## 2          Tilden Meyers <tilden DOT meyers AT noaa DOT gov>
## 3                                                           
## 4                                                           
## 5                     Martha Apple <MApple AT mtech DOT edu>
## 6                                                           
##                                              site_description site_type
## 1                   Archbold Biological Station, Florida, USA         I
## 2                                       Sierra Vista, Arizona       III
## 3 Southeast Watershed Research Laboratory EC2 Tifton, Georgia         I
## 4      Bangtail Study Area, Montana State University, Montana         I
## 5                          Continental Divide, Butte, Montana         I
## 6   Coal Oil Point Natural Reserve, Santa Barbara, California        II
##                   group camera_description camera_orientation flux_data
## 1                  LTAR  StarDot NetCam SC                  N     FALSE
## 2                 GEWEX     Olympus D-360L                  N     FALSE
## 3                  LTAR                  N                  N     FALSE
## 4 AmericaView AMERIFLUX  StarDot NetCam SC                  N      TRUE
## 5              PhenoCam  StarDot NetCam SC                  E     FALSE
## 6                                  unknown                        FALSE
##                                            flux_networks       flux_sitenames
## 1                                                   NULL                    N
## 2                                                   NULL                    N
## 3                                                   NULL                    N
## 4 AMERIFLUX, http://ameriflux.lbl.gov, AmeriFlux Network US-MTB (forthcoming)
## 5                                                   NULL                     
## 6                                                   NULL                     
##                                                                                                                                                                                                                                                                dominant_species
## 1                                                                                                                                                                                                                                                                              
## 2                                                                                                                                                                                                                                                                              
## 3                                                                                                                                                                                                                                                                              
## 4                                                                                                                                                                                                                                                            Festuca idahoensis
## 5 Agropyron cristatum, Poa pratensis, Phalaris arundinaceae, Carex. sp., Geum triflorum, Ericameria nauseousa, Centaurea macula, Achillea millefolium, Senecio sp., Lupinus sp., Penstemon sp., Linaria vulgaris, Cirsium arvense; Alnus incana, Salix sp., Populus tremuloides
## 6                                                                                                                                                                                 Lolium multiflorum, Bromus horadaceous, Avena fatua, Plantago lanceolata, Sisyrinchium bellum
##   primary_veg_type secondary_veg_type site_meteorology MAT_site MAP_site
## 1               GR                  N            FALSE        N        N
## 2               GR                  N            FALSE        N        N
## 3               GR                  N            FALSE        N        N
## 4               GR                 EN            FALSE        5      850
## 5               GR                 SH            FALSE        N        N
## 6               GR                 SH            FALSE     14.4      424
##   MAT_daymet MAP_daymet MAT_worldclim MAP_worldclim koeppen_geiger ecoregion
## 1      22.85       1302          22.5          1208            Cfa         8
## 2      16.25        468          15.3           446            BSk        12
## 3         19       1251          18.7          1213            Cfa         8
## 4        2.3        981           0.9           728            Dfb         6
## 5       5.05        365           4.3           311            BSk         6
## 6      16.15        623          15.4           405            Csb        11
##   landcover_igbp
## 1             14
## 2              7
## 3             14
## 4             10
## 5             10
## 6              7
##                                                                                                                                                                                                                                                 site_acknowledgements
## 1                                                                                                                                                                                                                                                                    
## 2                                                                                                                                                                                                                                                                    
## 3                                                                                                                                                                                                                                                                    
## 4 Research at the Bozeman site is supported by Colorado State University and the AmericaView program (grants G13AC00393, G11AC20461, G15AC00056) with phenocam equipment and deployment sponsored by the Department of Interior North Central Climate Science Center.
## 5                                                         Research at the Continental Divide PhenoCam Site in Butte, Montana is supported by the National Science Foundation-EPSCoR (grant NSF-0701906), OpenDap, Inc., and Montana Tech of the University of Montana
## 6                                                                                                                                                                                                                                                                    
##                           modified
## 1 2019-01-07T18:36:07.631244-05:00
## 2 2018-04-13T10:46:23.462958-04:00
## 3 2018-06-18T20:27:17.280524-04:00
## 4 2016-11-01T15:42:19.771057-04:00
## 5 2016-11-01T15:42:19.846100-04:00
## 6 2016-11-01T15:42:19.929455-04:00
```



```r
FirstSite=GrassSites[5, ] #randomly chose the fifth site in the table
FirstSite
```

```
##   Sitename      Lat       Lon Elev active utc_offset date_first  date_last
## 5    butte 45.95304 -112.4796 1682   TRUE         -7 2008-04-01 2020-10-12
##   infrared                                        contact1
## 5        N James Gallagher <jgallagher AT opendap DOT org>
##                                 contact2                   site_description
## 5 Martha Apple <MApple AT mtech DOT edu> Continental Divide, Butte, Montana
##   site_type    group camera_description camera_orientation flux_data
## 5         I PhenoCam  StarDot NetCam SC                  E     FALSE
##   flux_networks flux_sitenames
## 5          NULL               
##                                                                                                                                                                                                                                                                dominant_species
## 5 Agropyron cristatum, Poa pratensis, Phalaris arundinaceae, Carex. sp., Geum triflorum, Ericameria nauseousa, Centaurea macula, Achillea millefolium, Senecio sp., Lupinus sp., Penstemon sp., Linaria vulgaris, Cirsium arvense; Alnus incana, Salix sp., Populus tremuloides
##   primary_veg_type secondary_veg_type site_meteorology MAT_site MAP_site
## 5               GR                 SH            FALSE        N        N
##   MAT_daymet MAP_daymet MAT_worldclim MAP_worldclim koeppen_geiger ecoregion
## 5       5.05        365           4.3           311            BSk         6
##   landcover_igbp
## 5             10
##                                                                                                                                                                                         site_acknowledgements
## 5 Research at the Continental Divide PhenoCam Site in Butte, Montana is supported by the National Science Foundation-EPSCoR (grant NSF-0701906), OpenDap, Inc., and Montana Tech of the University of Montana
##                           modified
## 5 2016-11-01T15:42:19.846100-04:00
```

Chose your own sites and build out your code chunk here:


```r
print('build your code here')
```

```
## [1] "build your code here"
```

[Koen Huffkens](https://khufkens.com/) developed the [phenocamr package](https://cran.r-project.org/web/packages/phenocamr/index.html), which streamlines access to quality controlled data.  We will now use this package to download and process site based data according to a standardized methodology.

A full description of the methodology is provided in [Scientific Data: Tracking vegetation phenology across diverse North American biomes using PhenoCam imagery (Richardson et al. 2018)](https://www.nature.com/articles/sdata201828).



```r
#uncomment if you need to install via devtools
#if(!require(devtools)){install.package(devtools)}
#devtools::install_github("khufkens/phenocamr")
library(phenocamr)
```


Use the dataframe of sites that you want to analyze to feed the phenocamr package.
*Note: you can choose either a 1 or 3 day product*



```r
dir.create('data/', showWarnings = F)

phenocamr::download_phenocam(
  frequency = 3,
  veg_type = 'DB',
  roi_id = 1000,
  site = 'harvard',
  phenophase = TRUE,
  out_dir = "data/"
)
```

```
## Downloading: harvard_DB_1000_3day.csv
```

```
## -- Flagging outliers!
```

```
## -- Smoothing time series!
```

```
## -- Estimating transition dates!
```

```
## Downloading: harvardbarn_DB_1000_3day.csv
```

```
## -- Flagging outliers!
```

```
## -- Smoothing time series!
```

```
## -- Estimating transition dates!
```

```
## Downloading: harvardbarn2_DB_1000_3day.csv
```

```
## -- Flagging outliers!
```

```
## -- Smoothing time series!
```

```
## -- Estimating transition dates!
```

```
## Downloading: harvardhemlock_DB_1000_3day.csv
```

```
## -- Flagging outliers!
```

```
## -- Smoothing time series!
```

```
## -- Estimating transition dates!
```

```
## Downloading: harvardlph_DB_1000_3day.csv
```

```
## -- Flagging outliers!
```

```
## -- Smoothing time series!
```

```
## -- Estimating transition dates!
```

```r
#> Downloading: harvard_DB_1000_3day.csv
#> -- Flagging outliers!
#> -- Smoothing time series!
#> -- Estimating transition dates!
```

Now look in your working directory.  You have data!  Read it in:



```r
# load the time series data but replace the csv filename with whatever you downloaded
df <- read.table("data/harvard_DB_1000_3day.csv", header = TRUE, sep = ",")

# read in the transidation date file
td <- read.table("data/harvard_DB_1000_3day_transition_dates.csv",
                header = TRUE,
                sep = ",")
```

Let's take a look at the data:



```r
p = plot_ly() %>%
  add_trace(
    data = df,
    x = ~ as.Date(date),
    y = ~ smooth_gcc_90,
    name = 'Smoothed GCC',
    showlegend = TRUE,
    type = 'scatter',
    mode = 'line'
  ) %>% add_markers(
    data=df,
    x ~ as.Date(date),
    y = ~gcc_90,
    name = 'GCC',
    type = 'scatter',
    color ='#07A4B5',
    opacity=.5
  )
p
```

```
## Warning: `arrange_()` is deprecated as of dplyr 0.7.0.
## Please use `arrange()` instead.
## See vignette('programming') for more help
## This warning is displayed once every 8 hours.
## Call `lifecycle::last_warnings()` to see where this warning was generated.
```

```
## Warning: Ignoring 3239 observations
```

```
## Warning in RColorBrewer::brewer.pal(N, "Set2"): minimal value for n is 3, returning requested palette with 3 different levels

## Warning in RColorBrewer::brewer.pal(N, "Set2"): minimal value for n is 3, returning requested palette with 3 different levels
```

<!--html_preserve--><div id="htmlwidget-04988765864c13dbbb59" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-04988765864c13dbbb59">{"x":{"visdat":{"8bee2b4c8da8":["function () ","plotlyVisDat"],"8bee2ee826cd":["function () ","data"],"8beeb4b74ca":["function () ","data"]},"cur_data":"8beeb4b74ca","attrs":{"8bee2ee826cd":{"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"x":{},"y":{},"name":"Smoothed GCC","showlegend":true,"type":"scatter","mode":"line","inherit":true},"8beeb4b74ca":{"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"x":{},"y":{},"type":"scatter","mode":"markers","name":"GCC","color":"#07A4B5","opacity":0.5,"inherit":true}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"xaxis":{"domain":[0,1],"automargin":true,"title":"as.Date(date)"},"yaxis":{"domain":[0,1],"automargin":true,"title":"smooth_gcc_90"},"hovermode":"closest","showlegend":true},"source":"A","config":{"showSendToCloud":false},"data":[{"x":["2008-01-06","2008-01-07","2008-01-08","2008-01-09","2008-01-10","2008-01-11","2008-01-12","2008-01-13","2008-01-14","2008-01-15","2008-01-16","2008-01-17","2008-01-18","2008-01-19","2008-01-20","2008-01-21","2008-01-22","2008-01-23","2008-01-24","2008-01-25","2008-01-26","2008-01-27","2008-01-28","2008-01-29","2008-01-30","2008-01-31","2008-02-01","2008-02-02","2008-02-03","2008-02-04","2008-02-05","2008-02-06","2008-02-07","2008-02-08","2008-02-09","2008-02-10","2008-02-11","2008-02-12","2008-02-13","2008-02-14","2008-02-15","2008-02-16","2008-02-17","2008-02-18","2008-02-19","2008-02-20","2008-02-21","2008-02-22","2008-02-23","2008-02-24","2008-02-25","2008-02-26","2008-02-27","2008-02-28","2008-02-29","2008-03-01","2008-03-02","2008-03-03","2008-03-04","2008-03-05","2008-03-06","2008-03-07","2008-03-08","2008-03-09","2008-03-10","2008-03-11","2008-03-12","2008-03-13","2008-03-14","2008-03-15","2008-03-16","2008-03-17","2008-03-18","2008-03-19","2008-03-20","2008-03-21","2008-03-22","2008-03-23","2008-03-24","2008-03-25","2008-03-26","2008-03-27","2008-03-28","2008-03-29","2008-03-30","2008-03-31","2008-04-01","2008-04-02","2008-04-03","2008-04-04","2008-04-05","2008-04-06","2008-04-07","2008-04-08","2008-04-09","2008-04-10","2008-04-11","2008-04-12","2008-04-13","2008-04-14","2008-04-15","2008-04-16","2008-04-17","2008-04-18","2008-04-19","2008-04-20","2008-04-21","2008-04-22","2008-04-23","2008-04-24","2008-04-25","2008-04-26","2008-04-27","2008-04-28","2008-04-29","2008-04-30","2008-05-01","2008-05-02","2008-05-03","2008-05-04","2008-05-05","2008-05-06","2008-05-07","2008-05-08","2008-05-09","2008-05-10","2008-05-11","2008-05-12","2008-05-13","2008-05-14","2008-05-15","2008-05-16","2008-05-17","2008-05-18","2008-05-19","2008-05-20","2008-05-21","2008-05-22","2008-05-23","2008-05-24","2008-05-25","2008-05-26","2008-05-27","2008-05-28","2008-05-29","2008-05-30","2008-05-31","2008-06-01","2008-06-02","2008-06-03","2008-06-04","2008-06-05","2008-06-06","2008-06-07","2008-06-08","2008-06-09","2008-06-10","2008-06-11","2008-06-12","2008-06-13","2008-06-14","2008-06-15","2008-06-16","2008-06-17","2008-06-18","2008-06-19","2008-06-20","2008-06-21","2008-06-22","2008-06-23","2008-06-24","2008-06-25","2008-06-26","2008-06-27","2008-06-28","2008-06-29","2008-06-30","2008-07-01","2008-07-02","2008-07-03","2008-07-04","2008-07-05","2008-07-06","2008-07-07","2008-07-08","2008-07-09","2008-07-10","2008-07-11","2008-07-12","2008-07-13","2008-07-14","2008-07-15","2008-07-16","2008-07-17","2008-07-18","2008-07-19","2008-07-20","2008-07-21","2008-07-22","2008-07-23","2008-07-24","2008-07-25","2008-07-26","2008-07-27","2008-07-28","2008-07-29","2008-07-30","2008-07-31","2008-08-01","2008-08-02","2008-08-03","2008-08-04","2008-08-05","2008-08-06","2008-08-07","2008-08-08","2008-08-09","2008-08-10","2008-08-11","2008-08-12","2008-08-13","2008-08-14","2008-08-15","2008-08-16","2008-08-17","2008-08-18","2008-08-19","2008-08-20","2008-08-21","2008-08-22","2008-08-23","2008-08-24","2008-08-25","2008-08-26","2008-08-27","2008-08-28","2008-08-29","2008-08-30","2008-08-31","2008-09-01","2008-09-02","2008-09-03","2008-09-04","2008-09-05","2008-09-06","2008-09-07","2008-09-08","2008-09-09","2008-09-10","2008-09-11","2008-09-12","2008-09-13","2008-09-14","2008-09-15","2008-09-16","2008-09-17","2008-09-18","2008-09-19","2008-09-20","2008-09-21","2008-09-22","2008-09-23","2008-09-24","2008-09-25","2008-09-26","2008-09-27","2008-09-28","2008-09-29","2008-09-30","2008-10-01","2008-10-02","2008-10-03","2008-10-04","2008-10-05","2008-10-06","2008-10-07","2008-10-08","2008-10-09","2008-10-10","2008-10-11","2008-10-12","2008-10-13","2008-10-14","2008-10-15","2008-10-16","2008-10-17","2008-10-18","2008-10-19","2008-10-20","2008-10-21","2008-10-22","2008-10-23","2008-10-24","2008-10-25","2008-10-26","2008-10-27","2008-10-28","2008-10-29","2008-10-30","2008-10-31","2008-11-01","2008-11-02","2008-11-03","2008-11-04","2008-11-05","2008-11-06","2008-11-07","2008-11-08","2008-11-09","2008-11-10","2008-11-11","2008-11-12","2008-11-13","2008-11-14","2008-11-15","2008-11-16","2008-11-17","2008-11-18","2008-11-19","2008-11-20","2008-11-21","2008-11-22","2008-11-23","2008-11-24","2008-11-25","2008-11-26","2008-11-27","2008-11-28","2008-11-29","2008-11-30","2008-12-01","2008-12-02","2008-12-03","2008-12-04","2008-12-05","2008-12-06","2008-12-07","2008-12-08","2008-12-09","2008-12-10","2008-12-11","2008-12-12","2008-12-13","2008-12-14","2008-12-15","2008-12-16","2008-12-17","2008-12-18","2008-12-19","2008-12-20","2008-12-21","2008-12-22","2008-12-23","2008-12-24","2008-12-25","2008-12-26","2008-12-27","2008-12-28","2008-12-29","2008-12-30","2008-12-31","2009-01-01","2009-01-02","2009-01-03","2009-01-04","2009-01-05","2009-01-06","2009-01-07","2009-01-08","2009-01-09","2009-01-10","2009-01-11","2009-01-12","2009-01-13","2009-01-14","2009-01-15","2009-01-16","2009-01-17","2009-01-18","2009-01-19","2009-01-20","2009-01-21","2009-01-22","2009-01-23","2009-01-24","2009-01-25","2009-01-26","2009-01-27","2009-01-28","2009-01-29","2009-01-30","2009-01-31","2009-02-01","2009-02-02","2009-02-03","2009-02-04","2009-02-05","2009-02-06","2009-02-07","2009-02-08","2009-02-09","2009-02-10","2009-02-11","2009-02-12","2009-02-13","2009-02-14","2009-02-15","2009-02-16","2009-02-17","2009-02-18","2009-02-19","2009-02-20","2009-02-21","2009-02-22","2009-02-23","2009-02-24","2009-02-25","2009-02-26","2009-02-27","2009-02-28","2009-03-01","2009-03-02","2009-03-03","2009-03-04","2009-03-05","2009-03-06","2009-03-07","2009-03-08","2009-03-09","2009-03-10","2009-03-11","2009-03-12","2009-03-13","2009-03-14","2009-03-15","2009-03-16","2009-03-17","2009-03-18","2009-03-19","2009-03-20","2009-03-21","2009-03-22","2009-03-23","2009-03-24","2009-03-25","2009-03-26","2009-03-27","2009-03-28","2009-03-29","2009-03-30","2009-03-31","2009-04-01","2009-04-02","2009-04-03","2009-04-04","2009-04-05","2009-04-06","2009-04-07","2009-04-08","2009-04-09","2009-04-10","2009-04-11","2009-04-12","2009-04-13","2009-04-14","2009-04-15","2009-04-16","2009-04-17","2009-04-18","2009-04-19","2009-04-20","2009-04-21","2009-04-22","2009-04-23","2009-04-24","2009-04-25","2009-04-26","2009-04-27","2009-04-28","2009-04-29","2009-04-30","2009-05-01","2009-05-02","2009-05-03","2009-05-04","2009-05-05","2009-05-06","2009-05-07","2009-05-08","2009-05-09","2009-05-10","2009-05-11","2009-05-12","2009-05-13","2009-05-14","2009-05-15","2009-05-16","2009-05-17","2009-05-18","2009-05-19","2009-05-20","2009-05-21","2009-05-22","2009-05-23","2009-05-24","2009-05-25","2009-05-26","2009-05-27","2009-05-28","2009-05-29","2009-05-30","2009-05-31","2009-06-01","2009-06-02","2009-06-03","2009-06-04","2009-06-05","2009-06-06","2009-06-07","2009-06-08","2009-06-09","2009-06-10","2009-06-11","2009-06-12","2009-06-13","2009-06-14","2009-06-15","2009-06-16","2009-06-17","2009-06-18","2009-06-19","2009-06-20","2009-06-21","2009-06-22","2009-06-23","2009-06-24","2009-06-25","2009-06-26","2009-06-27","2009-06-28","2009-06-29","2009-06-30","2009-07-01","2009-07-02","2009-07-03","2009-07-04","2009-07-05","2009-07-06","2009-07-07","2009-07-08","2009-07-09","2009-07-10","2009-07-11","2009-07-12","2009-07-13","2009-07-14","2009-07-15","2009-07-16","2009-07-17","2009-07-18","2009-07-19","2009-07-20","2009-07-21","2009-07-22","2009-07-23","2009-07-24","2009-07-25","2009-07-26","2009-07-27","2009-07-28","2009-07-29","2009-07-30","2009-07-31","2009-08-01","2009-08-02","2009-08-03","2009-08-04","2009-08-05","2009-08-06","2009-08-07","2009-08-08","2009-08-09","2009-08-10","2009-08-11","2009-08-12","2009-08-13","2009-08-14","2009-08-15","2009-08-16","2009-08-17","2009-08-18","2009-08-19","2009-08-20","2009-08-21","2009-08-22","2009-08-23","2009-08-24","2009-08-25","2009-08-26","2009-08-27","2009-08-28","2009-08-29","2009-08-30","2009-08-31","2009-09-01","2009-09-02","2009-09-03","2009-09-04","2009-09-05","2009-09-06","2009-09-07","2009-09-08","2009-09-09","2009-09-10","2009-09-11","2009-09-12","2009-09-13","2009-09-14","2009-09-15","2009-09-16","2009-09-17","2009-09-18","2009-09-19","2009-09-20","2009-09-21","2009-09-22","2009-09-23","2009-09-24","2009-09-25","2009-09-26","2009-09-27","2009-09-28","2009-09-29","2009-09-30","2009-10-01","2009-10-02","2009-10-03","2009-10-04","2009-10-05","2009-10-06","2009-10-07","2009-10-08","2009-10-09","2009-10-10","2009-10-11","2009-10-12","2009-10-13","2009-10-14","2009-10-15","2009-10-16","2009-10-17","2009-10-18","2009-10-19","2009-10-20","2009-10-21","2009-10-22","2009-10-23","2009-10-24","2009-10-25","2009-10-26","2009-10-27","2009-10-28","2009-10-29","2009-10-30","2009-10-31","2009-11-01","2009-11-02","2009-11-03","2009-11-04","2009-11-05","2009-11-06","2009-11-07","2009-11-08","2009-11-09","2009-11-10","2009-11-11","2009-11-12","2009-11-13","2009-11-14","2009-11-15","2009-11-16","2009-11-17","2009-11-18","2009-11-19","2009-11-20","2009-11-21","2009-11-22","2009-11-23","2009-11-24","2009-11-25","2009-11-26","2009-11-27","2009-11-28","2009-11-29","2009-11-30","2009-12-01","2009-12-02","2009-12-03","2009-12-04","2009-12-05","2009-12-06","2009-12-07","2009-12-08","2009-12-09","2009-12-10","2009-12-11","2009-12-12","2009-12-13","2009-12-14","2009-12-15","2009-12-16","2009-12-17","2009-12-18","2009-12-19","2009-12-20","2009-12-21","2009-12-22","2009-12-23","2009-12-24","2009-12-25","2009-12-26","2009-12-27","2009-12-28","2009-12-29","2009-12-30","2009-12-31","2010-01-01","2010-01-02","2010-01-03","2010-01-04","2010-01-05","2010-01-06","2010-01-07","2010-01-08","2010-01-09","2010-01-10","2010-01-11","2010-01-12","2010-01-13","2010-01-14","2010-01-15","2010-01-16","2010-01-17","2010-01-18","2010-01-19","2010-01-20","2010-01-21","2010-01-22","2010-01-23","2010-01-24","2010-01-25","2010-01-26","2010-01-27","2010-01-28","2010-01-29","2010-01-30","2010-01-31","2010-02-01","2010-02-02","2010-02-03","2010-02-04","2010-02-05","2010-02-06","2010-02-07","2010-02-08","2010-02-09","2010-02-10","2010-02-11","2010-02-12","2010-02-13","2010-02-14","2010-02-15","2010-02-16","2010-02-17","2010-02-18","2010-02-19","2010-02-20","2010-02-21","2010-02-22","2010-02-23","2010-02-24","2010-02-25","2010-02-26","2010-02-27","2010-02-28","2010-03-01","2010-03-02","2010-03-03","2010-03-04","2010-03-05","2010-03-06","2010-03-07","2010-03-08","2010-03-09","2010-03-10","2010-03-11","2010-03-12","2010-03-13","2010-03-14","2010-03-15","2010-03-16","2010-03-17","2010-03-18","2010-03-19","2010-03-20","2010-03-21","2010-03-22","2010-03-23","2010-03-24","2010-03-25","2010-03-26","2010-03-27","2010-03-28","2010-03-29","2010-03-30","2010-03-31","2010-04-01","2010-04-02","2010-04-03","2010-04-04","2010-04-05","2010-04-06","2010-04-07","2010-04-08","2010-04-09","2010-04-10","2010-04-11","2010-04-12","2010-04-13","2010-04-14","2010-04-15","2010-04-16","2010-04-17","2010-04-18","2010-04-19","2010-04-20","2010-04-21","2010-04-22","2010-04-23","2010-04-24","2010-04-25","2010-04-26","2010-04-27","2010-04-28","2010-04-29","2010-04-30","2010-05-01","2010-05-02","2010-05-03","2010-05-04","2010-05-05","2010-05-06","2010-05-07","2010-05-08","2010-05-09","2010-05-10","2010-05-11","2010-05-12","2010-05-13","2010-05-14","2010-05-15","2010-05-16","2010-05-17","2010-05-18","2010-05-19","2010-05-20","2010-05-21","2010-05-22","2010-05-23","2010-05-24","2010-05-25","2010-05-26","2010-05-27","2010-05-28","2010-05-29","2010-05-30","2010-05-31","2010-06-01","2010-06-02","2010-06-03","2010-06-04","2010-06-05","2010-06-06","2010-06-07","2010-06-08","2010-06-09","2010-06-10","2010-06-11","2010-06-12","2010-06-13","2010-06-14","2010-06-15","2010-06-16","2010-06-17","2010-06-18","2010-06-19","2010-06-20","2010-06-21","2010-06-22","2010-06-23","2010-06-24","2010-06-25","2010-06-26","2010-06-27","2010-06-28","2010-06-29","2010-06-30","2010-07-01","2010-07-02","2010-07-03","2010-07-04","2010-07-05","2010-07-06","2010-07-07","2010-07-08","2010-07-09","2010-07-10","2010-07-11","2010-07-12","2010-07-13","2010-07-14","2010-07-15","2010-07-16","2010-07-17","2010-07-18","2010-07-19","2010-07-20","2010-07-21","2010-07-22","2010-07-23","2010-07-24","2010-07-25","2010-07-26","2010-07-27","2010-07-28","2010-07-29","2010-07-30","2010-07-31","2010-08-01","2010-08-02","2010-08-03","2010-08-04","2010-08-05","2010-08-06","2010-08-07","2010-08-08","2010-08-09","2010-08-10","2010-08-11","2010-08-12","2010-08-13","2010-08-14","2010-08-15","2010-08-16","2010-08-17","2010-08-18","2010-08-19","2010-08-20","2010-08-21","2010-08-22","2010-08-23","2010-08-24","2010-08-25","2010-08-26","2010-08-27","2010-08-28","2010-08-29","2010-08-30","2010-08-31","2010-09-01","2010-09-02","2010-09-03","2010-09-04","2010-09-05","2010-09-06","2010-09-07","2010-09-08","2010-09-09","2010-09-10","2010-09-11","2010-09-12","2010-09-13","2010-09-14","2010-09-15","2010-09-16","2010-09-17","2010-09-18","2010-09-19","2010-09-20","2010-09-21","2010-09-22","2010-09-23","2010-09-24","2010-09-25","2010-09-26","2010-09-27","2010-09-28","2010-09-29","2010-09-30","2010-10-01","2010-10-02","2010-10-03","2010-10-04","2010-10-05","2010-10-06","2010-10-07","2010-10-08","2010-10-09","2010-10-10","2010-10-11","2010-10-12","2010-10-13","2010-10-14","2010-10-15","2010-10-16","2010-10-17","2010-10-18","2010-10-19","2010-10-20","2010-10-21","2010-10-22","2010-10-23","2010-10-24","2010-10-25","2010-10-26","2010-10-27","2010-10-28","2010-10-29","2010-10-30","2010-10-31","2010-11-01","2010-11-02","2010-11-03","2010-11-04","2010-11-05","2010-11-06","2010-11-07","2010-11-08","2010-11-09","2010-11-10","2010-11-11","2010-11-12","2010-11-13","2010-11-14","2010-11-15","2010-11-16","2010-11-17","2010-11-18","2010-11-19","2010-11-20","2010-11-21","2010-11-22","2010-11-23","2010-11-24","2010-11-25","2010-11-26","2010-11-27","2010-11-28","2010-11-29","2010-11-30","2010-12-01","2010-12-02","2010-12-03","2010-12-04","2010-12-05","2010-12-06","2010-12-07","2010-12-08","2010-12-09","2010-12-10","2010-12-11","2010-12-12","2010-12-13","2010-12-14","2010-12-15","2010-12-16","2010-12-17","2010-12-18","2010-12-19","2010-12-20","2010-12-21","2010-12-22","2010-12-23","2010-12-24","2010-12-25","2010-12-26","2010-12-27","2010-12-28","2010-12-29","2010-12-30","2010-12-31","2011-01-01","2011-01-02","2011-01-03","2011-01-04","2011-01-05","2011-01-06","2011-01-07","2011-01-08","2011-01-09","2011-01-10","2011-01-11","2011-01-12","2011-01-13","2011-01-14","2011-01-15","2011-01-16","2011-01-17","2011-01-18","2011-01-19","2011-01-20","2011-01-21","2011-01-22","2011-01-23","2011-01-24","2011-01-25","2011-01-26","2011-01-27","2011-01-28","2011-01-29","2011-01-30","2011-01-31","2011-02-01","2011-02-02","2011-02-03","2011-02-04","2011-02-05","2011-02-06","2011-02-07","2011-02-08","2011-02-09","2011-02-10","2011-02-11","2011-02-12","2011-02-13","2011-02-14","2011-02-15","2011-02-16","2011-02-17","2011-02-18","2011-02-19","2011-02-20","2011-02-21","2011-02-22","2011-02-23","2011-02-24","2011-02-25","2011-02-26","2011-02-27","2011-02-28","2011-03-01","2011-03-02","2011-03-03","2011-03-04","2011-03-05","2011-03-06","2011-03-07","2011-03-08","2011-03-09","2011-03-10","2011-03-11","2011-03-12","2011-03-13","2011-03-14","2011-03-15","2011-03-16","2011-03-17","2011-03-18","2011-03-19","2011-03-20","2011-03-21","2011-03-22","2011-03-23","2011-03-24","2011-03-25","2011-03-26","2011-03-27","2011-03-28","2011-03-29","2011-03-30","2011-03-31","2011-04-01","2011-04-02","2011-04-03","2011-04-04","2011-04-05","2011-04-06","2011-04-07","2011-04-08","2011-04-09","2011-04-10","2011-04-11","2011-04-12","2011-04-13","2011-04-14","2011-04-15","2011-04-16","2011-04-17","2011-04-18","2011-04-19","2011-04-20","2011-04-21","2011-04-22","2011-04-23","2011-04-24","2011-04-25","2011-04-26","2011-04-27","2011-04-28","2011-04-29","2011-04-30","2011-05-01","2011-05-02","2011-05-03","2011-05-04","2011-05-05","2011-05-06","2011-05-07","2011-05-08","2011-05-09","2011-05-10","2011-05-11","2011-05-12","2011-05-13","2011-05-14","2011-05-15","2011-05-16","2011-05-17","2011-05-18","2011-05-19","2011-05-20","2011-05-21","2011-05-22","2011-05-23","2011-05-24","2011-05-25","2011-05-26","2011-05-27","2011-05-28","2011-05-29","2011-05-30","2011-05-31","2011-06-01","2011-06-02","2011-06-03","2011-06-04","2011-06-05","2011-06-06","2011-06-07","2011-06-08","2011-06-09","2011-06-10","2011-06-11","2011-06-12","2011-06-13","2011-06-14","2011-06-15","2011-06-16","2011-06-17","2011-06-18","2011-06-19","2011-06-20","2011-06-21","2011-06-22","2011-06-23","2011-06-24","2011-06-25","2011-06-26","2011-06-27","2011-06-28","2011-06-29","2011-06-30","2011-07-01","2011-07-02","2011-07-03","2011-07-04","2011-07-05","2011-07-06","2011-07-07","2011-07-08","2011-07-09","2011-07-10","2011-07-11","2011-07-12","2011-07-13","2011-07-14","2011-07-15","2011-07-16","2011-07-17","2011-07-18","2011-07-19","2011-07-20","2011-07-21","2011-07-22","2011-07-23","2011-07-24","2011-07-25","2011-07-26","2011-07-27","2011-07-28","2011-07-29","2011-07-30","2011-07-31","2011-08-01","2011-08-02","2011-08-03","2011-08-04","2011-08-05","2011-08-06","2011-08-07","2011-08-08","2011-08-09","2011-08-10","2011-08-11","2011-08-12","2011-08-13","2011-08-14","2011-08-15","2011-08-16","2011-08-17","2011-08-18","2011-08-19","2011-08-20","2011-08-21","2011-08-22","2011-08-23","2011-08-24","2011-08-25","2011-08-26","2011-08-27","2011-08-28","2011-08-29","2011-08-30","2011-08-31","2011-09-01","2011-09-02","2011-09-03","2011-09-04","2011-09-05","2011-09-06","2011-09-07","2011-09-08","2011-09-09","2011-09-10","2011-09-11","2011-09-12","2011-09-13","2011-09-14","2011-09-15","2011-09-16","2011-09-17","2011-09-18","2011-09-19","2011-09-20","2011-09-21","2011-09-22","2011-09-23","2011-09-24","2011-09-25","2011-09-26","2011-09-27","2011-09-28","2011-09-29","2011-09-30","2011-10-01","2011-10-02","2011-10-03","2011-10-04","2011-10-05","2011-10-06","2011-10-07","2011-10-08","2011-10-09","2011-10-10","2011-10-11","2011-10-12","2011-10-13","2011-10-14","2011-10-15","2011-10-16","2011-10-17","2011-10-18","2011-10-19","2011-10-20","2011-10-21","2011-10-22","2011-10-23","2011-10-24","2011-10-25","2011-10-26","2011-10-27","2011-10-28","2011-10-29","2011-10-30","2011-10-31","2011-11-01","2011-11-02","2011-11-03","2011-11-04","2011-11-05","2011-11-06","2011-11-07","2011-11-08","2011-11-09","2011-11-10","2011-11-11","2011-11-12","2011-11-13","2011-11-14","2011-11-15","2011-11-16","2011-11-17","2011-11-18","2011-11-19","2011-11-20","2011-11-21","2011-11-22","2011-11-23","2011-11-24","2011-11-25","2011-11-26","2011-11-27","2011-11-28","2011-11-29","2011-11-30","2011-12-01","2011-12-02","2011-12-03","2011-12-04","2011-12-05","2011-12-06","2011-12-07","2011-12-08","2011-12-09","2011-12-10","2011-12-11","2011-12-12","2011-12-13","2011-12-14","2011-12-15","2011-12-16","2011-12-17","2011-12-18","2011-12-19","2011-12-20","2011-12-21","2011-12-22","2011-12-23","2011-12-24","2011-12-25","2011-12-26","2011-12-27","2011-12-28","2011-12-29","2011-12-30","2011-12-31","2012-01-01","2012-01-02","2012-01-03","2012-01-04","2012-01-05","2012-01-06","2012-01-07","2012-01-08","2012-01-09","2012-01-10","2012-01-11","2012-01-12","2012-01-13","2012-01-14","2012-01-15","2012-01-16","2012-01-17","2012-01-18","2012-01-19","2012-01-20","2012-01-21","2012-01-22","2012-01-23","2012-01-24","2012-01-25","2012-01-26","2012-01-27","2012-01-28","2012-01-29","2012-01-30","2012-01-31","2012-02-01","2012-02-02","2012-02-03","2012-02-04","2012-02-05","2012-02-06","2012-02-07","2012-02-08","2012-02-09","2012-02-10","2012-02-11","2012-02-12","2012-02-13","2012-02-14","2012-02-15","2012-02-16","2012-02-17","2012-02-18","2012-02-19","2012-02-20","2012-02-21","2012-02-22","2012-02-23","2012-02-24","2012-02-25","2012-02-26","2012-02-27","2012-02-28","2012-02-29","2012-03-01","2012-03-02","2012-03-03","2012-03-04","2012-03-05","2012-03-06","2012-03-07","2012-03-08","2012-03-09","2012-03-10","2012-03-11","2012-03-12","2012-03-13","2012-03-14","2012-03-15","2012-03-16","2012-03-17","2012-03-18","2012-03-19","2012-03-20","2012-03-21","2012-03-22","2012-03-23","2012-03-24","2012-03-25","2012-03-26","2012-03-27","2012-03-28","2012-03-29","2012-03-30","2012-03-31","2012-04-01","2012-04-02","2012-04-03","2012-04-04","2012-04-05","2012-04-06","2012-04-07","2012-04-08","2012-04-09","2012-04-10","2012-04-11","2012-04-12","2012-04-13","2012-04-14","2012-04-15","2012-04-16","2012-04-17","2012-04-18","2012-04-19","2012-04-20","2012-04-21","2012-04-22","2012-04-23","2012-04-24","2012-04-25","2012-04-26","2012-04-27","2012-04-28","2012-04-29","2012-04-30","2012-05-01","2012-05-02","2012-05-03","2012-05-04","2012-05-05","2012-05-06","2012-05-07","2012-05-08","2012-05-09","2012-05-10","2012-05-11","2012-05-12","2012-05-13","2012-05-14","2012-05-15","2012-05-16","2012-05-17","2012-05-18","2012-05-19","2012-05-20","2012-05-21","2012-05-22","2012-05-23","2012-05-24","2012-05-25","2012-05-26","2012-05-27","2012-05-28","2012-05-29","2012-05-30","2012-05-31","2012-06-01","2012-06-02","2012-06-03","2012-06-04","2012-06-05","2012-06-06","2012-06-07","2012-06-08","2012-06-09","2012-06-10","2012-06-11","2012-06-12","2012-06-13","2012-06-14","2012-06-15","2012-06-16","2012-06-17","2012-06-18","2012-06-19","2012-06-20","2012-06-21","2012-06-22","2012-06-23","2012-06-24","2012-06-25","2012-06-26","2012-06-27","2012-06-28","2012-06-29","2012-06-30","2012-07-01","2012-07-02","2012-07-03","2012-07-04","2012-07-05","2012-07-06","2012-07-07","2012-07-08","2012-07-09","2012-07-10","2012-07-11","2012-07-12","2012-07-13","2012-07-14","2012-07-15","2012-07-16","2012-07-17","2012-07-18","2012-07-19","2012-07-20","2012-07-21","2012-07-22","2012-07-23","2012-07-24","2012-07-25","2012-07-26","2012-07-27","2012-07-28","2012-07-29","2012-07-30","2012-07-31","2012-08-01","2012-08-02","2012-08-03","2012-08-04","2012-08-05","2012-08-06","2012-08-07","2012-08-08","2012-08-09","2012-08-10","2012-08-11","2012-08-12","2012-08-13","2012-08-14","2012-08-15","2012-08-16","2012-08-17","2012-08-18","2012-08-19","2012-08-20","2012-08-21","2012-08-22","2012-08-23","2012-08-24","2012-08-25","2012-08-26","2012-08-27","2012-08-28","2012-08-29","2012-08-30","2012-08-31","2012-09-01","2012-09-02","2012-09-03","2012-09-04","2012-09-05","2012-09-06","2012-09-07","2012-09-08","2012-09-09","2012-09-10","2012-09-11","2012-09-12","2012-09-13","2012-09-14","2012-09-15","2012-09-16","2012-09-17","2012-09-18","2012-09-19","2012-09-20","2012-09-21","2012-09-22","2012-09-23","2012-09-24","2012-09-25","2012-09-26","2012-09-27","2012-09-28","2012-09-29","2012-09-30","2012-10-01","2012-10-02","2012-10-03","2012-10-04","2012-10-05","2012-10-06","2012-10-07","2012-10-08","2012-10-09","2012-10-10","2012-10-11","2012-10-12","2012-10-13","2012-10-14","2012-10-15","2012-10-16","2012-10-17","2012-10-18","2012-10-19","2012-10-20","2012-10-21","2012-10-22","2012-10-23","2012-10-24","2012-10-25","2012-10-26","2012-10-27","2012-10-28","2012-10-29","2012-10-30","2012-10-31","2012-11-01","2012-11-02","2012-11-03","2012-11-04","2012-11-05","2012-11-06","2012-11-07","2012-11-08","2012-11-09","2012-11-10","2012-11-11","2012-11-12","2012-11-13","2012-11-14","2012-11-15","2012-11-16","2012-11-17","2012-11-18","2012-11-19","2012-11-20","2012-11-21","2012-11-22","2012-11-23","2012-11-24","2012-11-25","2012-11-26","2012-11-27","2012-11-28","2012-11-29","2012-11-30","2012-12-01","2012-12-02","2012-12-03","2012-12-04","2012-12-05","2012-12-06","2012-12-07","2012-12-08","2012-12-09","2012-12-10","2012-12-11","2012-12-12","2012-12-13","2012-12-14","2012-12-15","2012-12-16","2012-12-17","2012-12-18","2012-12-19","2012-12-20","2012-12-21","2012-12-22","2012-12-23","2012-12-24","2012-12-25","2012-12-26","2012-12-27","2012-12-28","2012-12-29","2012-12-30","2012-12-31","2013-01-01","2013-01-02","2013-01-03","2013-01-04","2013-01-05","2013-01-06","2013-01-07","2013-01-08","2013-01-09","2013-01-10","2013-01-11","2013-01-12","2013-01-13","2013-01-14","2013-01-15","2013-01-16","2013-01-17","2013-01-18","2013-01-19","2013-01-20","2013-01-21","2013-01-22","2013-01-23","2013-01-24","2013-01-25","2013-01-26","2013-01-27","2013-01-28","2013-01-29","2013-01-30","2013-01-31","2013-02-01","2013-02-02","2013-02-03","2013-02-04","2013-02-05","2013-02-06","2013-02-07","2013-02-08","2013-02-09","2013-02-10","2013-02-11","2013-02-12","2013-02-13","2013-02-14","2013-02-15","2013-02-16","2013-02-17","2013-02-18","2013-02-19","2013-02-20","2013-02-21","2013-02-22","2013-02-23","2013-02-24","2013-02-25","2013-02-26","2013-02-27","2013-02-28","2013-03-01","2013-03-02","2013-03-03","2013-03-04","2013-03-05","2013-03-06","2013-03-07","2013-03-08","2013-03-09","2013-03-10","2013-03-11","2013-03-12","2013-03-13","2013-03-14","2013-03-15","2013-03-16","2013-03-17","2013-03-18","2013-03-19","2013-03-20","2013-03-21","2013-03-22","2013-03-23","2013-03-24","2013-03-25","2013-03-26","2013-03-27","2013-03-28","2013-03-29","2013-03-30","2013-03-31","2013-04-01","2013-04-02","2013-04-03","2013-04-04","2013-04-05","2013-04-06","2013-04-07","2013-04-08","2013-04-09","2013-04-10","2013-04-11","2013-04-12","2013-04-13","2013-04-14","2013-04-15","2013-04-16","2013-04-17","2013-04-18","2013-04-19","2013-04-20","2013-04-21","2013-04-22","2013-04-23","2013-04-24","2013-04-25","2013-04-26","2013-04-27","2013-04-28","2013-04-29","2013-04-30","2013-05-01","2013-05-02","2013-05-03","2013-05-04","2013-05-05","2013-05-06","2013-05-07","2013-05-08","2013-05-09","2013-05-10","2013-05-11","2013-05-12","2013-05-13","2013-05-14","2013-05-15","2013-05-16","2013-05-17","2013-05-18","2013-05-19","2013-05-20","2013-05-21","2013-05-22","2013-05-23","2013-05-24","2013-05-25","2013-05-26","2013-05-27","2013-05-28","2013-05-29","2013-05-30","2013-05-31","2013-06-01","2013-06-02","2013-06-03","2013-06-04","2013-06-05","2013-06-06","2013-06-07","2013-06-08","2013-06-09","2013-06-10","2013-06-11","2013-06-12","2013-06-13","2013-06-14","2013-06-15","2013-06-16","2013-06-17","2013-06-18","2013-06-19","2013-06-20","2013-06-21","2013-06-22","2013-06-23","2013-06-24","2013-06-25","2013-06-26","2013-06-27","2013-06-28","2013-06-29","2013-06-30","2013-07-01","2013-07-02","2013-07-03","2013-07-04","2013-07-05","2013-07-06","2013-07-07","2013-07-08","2013-07-09","2013-07-10","2013-07-11","2013-07-12","2013-07-13","2013-07-14","2013-07-15","2013-07-16","2013-07-17","2013-07-18","2013-07-19","2013-07-20","2013-07-21","2013-07-22","2013-07-23","2013-07-24","2013-07-25","2013-07-26","2013-07-27","2013-07-28","2013-07-29","2013-07-30","2013-07-31","2013-08-01","2013-08-02","2013-08-03","2013-08-04","2013-08-05","2013-08-06","2013-08-07","2013-08-08","2013-08-09","2013-08-10","2013-08-11","2013-08-12","2013-08-13","2013-08-14","2013-08-15","2013-08-16","2013-08-17","2013-08-18","2013-08-19","2013-08-20","2013-08-21","2013-08-22","2013-08-23","2013-08-24","2013-08-25","2013-08-26","2013-08-27","2013-08-28","2013-08-29","2013-08-30","2013-08-31","2013-09-01","2013-09-02","2013-09-03","2013-09-04","2013-09-05","2013-09-06","2013-09-07","2013-09-08","2013-09-09","2013-09-10","2013-09-11","2013-09-12","2013-09-13","2013-09-14","2013-09-15","2013-09-16","2013-09-17","2013-09-18","2013-09-19","2013-09-20","2013-09-21","2013-09-22","2013-09-23","2013-09-24","2013-09-25","2013-09-26","2013-09-27","2013-09-28","2013-09-29","2013-09-30","2013-10-01","2013-10-02","2013-10-03","2013-10-04","2013-10-05","2013-10-06","2013-10-07","2013-10-08","2013-10-09","2013-10-10","2013-10-11","2013-10-12","2013-10-13","2013-10-14","2013-10-15","2013-10-16","2013-10-17","2013-10-18","2013-10-19","2013-10-20","2013-10-21","2013-10-22","2013-10-23","2013-10-24","2013-10-25","2013-10-26","2013-10-27","2013-10-28","2013-10-29","2013-10-30","2013-10-31","2013-11-01","2013-11-02","2013-11-03","2013-11-04","2013-11-05","2013-11-06","2013-11-07","2013-11-08","2013-11-09","2013-11-10","2013-11-11","2013-11-12","2013-11-13","2013-11-14","2013-11-15","2013-11-16","2013-11-17","2013-11-18","2013-11-19","2013-11-20","2013-11-21","2013-11-22","2013-11-23","2013-11-24","2013-11-25","2013-11-26","2013-11-27","2013-11-28","2013-11-29","2013-11-30","2013-12-01","2013-12-02","2013-12-03","2013-12-04","2013-12-05","2013-12-06","2013-12-07","2013-12-08","2013-12-09","2013-12-10","2013-12-11","2013-12-12","2013-12-13","2013-12-14","2013-12-15","2013-12-16","2013-12-17","2013-12-18","2013-12-19","2013-12-20","2013-12-21","2013-12-22","2013-12-23","2013-12-24","2013-12-25","2013-12-26","2013-12-27","2013-12-28","2013-12-29","2013-12-30","2013-12-31","2014-01-01","2014-01-02","2014-01-03","2014-01-04","2014-01-05","2014-01-06","2014-01-07","2014-01-08","2014-01-09","2014-01-10","2014-01-11","2014-01-12","2014-01-13","2014-01-14","2014-01-15","2014-01-16","2014-01-17","2014-01-18","2014-01-19","2014-01-20","2014-01-21","2014-01-22","2014-01-23","2014-01-24","2014-01-25","2014-01-26","2014-01-27","2014-01-28","2014-01-29","2014-01-30","2014-01-31","2014-02-01","2014-02-02","2014-02-03","2014-02-04","2014-02-05","2014-02-06","2014-02-07","2014-02-08","2014-02-09","2014-02-10","2014-02-11","2014-02-12","2014-02-13","2014-02-14","2014-02-15","2014-02-16","2014-02-17","2014-02-18","2014-02-19","2014-02-20","2014-02-21","2014-02-22","2014-02-23","2014-02-24","2014-02-25","2014-02-26","2014-02-27","2014-02-28","2014-03-01","2014-03-02","2014-03-03","2014-03-04","2014-03-05","2014-03-06","2014-03-07","2014-03-08","2014-03-09","2014-03-10","2014-03-11","2014-03-12","2014-03-13","2014-03-14","2014-03-15","2014-03-16","2014-03-17","2014-03-18","2014-03-19","2014-03-20","2014-03-21","2014-03-22","2014-03-23","2014-03-24","2014-03-25","2014-03-26","2014-03-27","2014-03-28","2014-03-29","2014-03-30","2014-03-31","2014-04-01","2014-04-02","2014-04-03","2014-04-04","2014-04-05","2014-04-06","2014-04-07","2014-04-08","2014-04-09","2014-04-10","2014-04-11","2014-04-12","2014-04-13","2014-04-14","2014-04-15","2014-04-16","2014-04-17","2014-04-18","2014-04-19","2014-04-20","2014-04-21","2014-04-22","2014-04-23","2014-04-24","2014-04-25","2014-04-26","2014-04-27","2014-04-28","2014-04-29","2014-04-30","2014-05-01","2014-05-02","2014-05-03","2014-05-04","2014-05-05","2014-05-06","2014-05-07","2014-05-08","2014-05-09","2014-05-10","2014-05-11","2014-05-12","2014-05-13","2014-05-14","2014-05-15","2014-05-16","2014-05-17","2014-05-18","2014-05-19","2014-05-20","2014-05-21","2014-05-22","2014-05-23","2014-05-24","2014-05-25","2014-05-26","2014-05-27","2014-05-28","2014-05-29","2014-05-30","2014-05-31","2014-06-01","2014-06-02","2014-06-03","2014-06-04","2014-06-05","2014-06-06","2014-06-07","2014-06-08","2014-06-09","2014-06-10","2014-06-11","2014-06-12","2014-06-13","2014-06-14","2014-06-15","2014-06-16","2014-06-17","2014-06-18","2014-06-19","2014-06-20","2014-06-21","2014-06-22","2014-06-23","2014-06-24","2014-06-25","2014-06-26","2014-06-27","2014-06-28","2014-06-29","2014-06-30","2014-07-01","2014-07-02","2014-07-03","2014-07-04","2014-07-05","2014-07-06","2014-07-07","2014-07-08","2014-07-09","2014-07-10","2014-07-11","2014-07-12","2014-07-13","2014-07-14","2014-07-15","2014-07-16","2014-07-17","2014-07-18","2014-07-19","2014-07-20","2014-07-21","2014-07-22","2014-07-23","2014-07-24","2014-07-25","2014-07-26","2014-07-27","2014-07-28","2014-07-29","2014-07-30","2014-07-31","2014-08-01","2014-08-02","2014-08-03","2014-08-04","2014-08-05","2014-08-06","2014-08-07","2014-08-08","2014-08-09","2014-08-10","2014-08-11","2014-08-12","2014-08-13","2014-08-14","2014-08-15","2014-08-16","2014-08-17","2014-08-18","2014-08-19","2014-08-20","2014-08-21","2014-08-22","2014-08-23","2014-08-24","2014-08-25","2014-08-26","2014-08-27","2014-08-28","2014-08-29","2014-08-30","2014-08-31","2014-09-01","2014-09-02","2014-09-03","2014-09-04","2014-09-05","2014-09-06","2014-09-07","2014-09-08","2014-09-09","2014-09-10","2014-09-11","2014-09-12","2014-09-13","2014-09-14","2014-09-15","2014-09-16","2014-09-17","2014-09-18","2014-09-19","2014-09-20","2014-09-21","2014-09-22","2014-09-23","2014-09-24","2014-09-25","2014-09-26","2014-09-27","2014-09-28","2014-09-29","2014-09-30","2014-10-01","2014-10-02","2014-10-03","2014-10-04","2014-10-05","2014-10-06","2014-10-07","2014-10-08","2014-10-09","2014-10-10","2014-10-11","2014-10-12","2014-10-13","2014-10-14","2014-10-15","2014-10-16","2014-10-17","2014-10-18","2014-10-19","2014-10-20","2014-10-21","2014-10-22","2014-10-23","2014-10-24","2014-10-25","2014-10-26","2014-10-27","2014-10-28","2014-10-29","2014-10-30","2014-10-31","2014-11-01","2014-11-02","2014-11-03","2014-11-04","2014-11-05","2014-11-06","2014-11-07","2014-11-08","2014-11-09","2014-11-10","2014-11-11","2014-11-12","2014-11-13","2014-11-14","2014-11-15","2014-11-16","2014-11-17","2014-11-18","2014-11-19","2014-11-20","2014-11-21","2014-11-22","2014-11-23","2014-11-24","2014-11-25","2014-11-26","2014-11-27","2014-11-28","2014-11-29","2014-11-30","2014-12-01","2014-12-02","2014-12-03","2014-12-04","2014-12-05","2014-12-06","2014-12-07","2014-12-08","2014-12-09","2014-12-10","2014-12-11","2014-12-12","2014-12-13","2014-12-14","2014-12-15","2014-12-16","2014-12-17","2014-12-18","2014-12-19","2014-12-20","2014-12-21","2014-12-22","2014-12-23","2014-12-24","2014-12-25","2014-12-26","2014-12-27","2014-12-28","2014-12-29","2014-12-30","2014-12-31","2015-01-01","2015-01-02","2015-01-03","2015-01-04","2015-01-05","2015-01-06","2015-01-07","2015-01-08","2015-01-09","2015-01-10","2015-01-11","2015-01-12","2015-01-13","2015-01-14","2015-01-15","2015-01-16","2015-01-17","2015-01-18","2015-01-19","2015-01-20","2015-01-21","2015-01-22","2015-01-23","2015-01-24","2015-01-25","2015-01-26","2015-01-27","2015-01-28","2015-01-29","2015-01-30","2015-01-31","2015-02-01","2015-02-02","2015-02-03","2015-02-04","2015-02-05","2015-02-06","2015-02-07","2015-02-08","2015-02-09","2015-02-10","2015-02-11","2015-02-12","2015-02-13","2015-02-14","2015-02-15","2015-02-16","2015-02-17","2015-02-18","2015-02-19","2015-02-20","2015-02-21","2015-02-22","2015-02-23","2015-02-24","2015-02-25","2015-02-26","2015-02-27","2015-02-28","2015-03-01","2015-03-02","2015-03-03","2015-03-04","2015-03-05","2015-03-06","2015-03-07","2015-03-08","2015-03-09","2015-03-10","2015-03-11","2015-03-12","2015-03-13","2015-03-14","2015-03-15","2015-03-16","2015-03-17","2015-03-18","2015-03-19","2015-03-20","2015-03-21","2015-03-22","2015-03-23","2015-03-24","2015-03-25","2015-03-26","2015-03-27","2015-03-28","2015-03-29","2015-03-30","2015-03-31","2015-04-01","2015-04-02","2015-04-03","2015-04-04","2015-04-05","2015-04-06","2015-04-07","2015-04-08","2015-04-09","2015-04-10","2015-04-11","2015-04-12","2015-04-13","2015-04-14","2015-04-15","2015-04-16","2015-04-17","2015-04-18","2015-04-19","2015-04-20","2015-04-21","2015-04-22","2015-04-23","2015-04-24","2015-04-25","2015-04-26","2015-04-27","2015-04-28","2015-04-29","2015-04-30","2015-05-01","2015-05-02","2015-05-03","2015-05-04","2015-05-05","2015-05-06","2015-05-07","2015-05-08","2015-05-09","2015-05-10","2015-05-11","2015-05-12","2015-05-13","2015-05-14","2015-05-15","2015-05-16","2015-05-17","2015-05-18","2015-05-19","2015-05-20","2015-05-21","2015-05-22","2015-05-23","2015-05-24","2015-05-25","2015-05-26","2015-05-27","2015-05-28","2015-05-29","2015-05-30","2015-05-31","2015-06-01","2015-06-02","2015-06-03","2015-06-04","2015-06-05","2015-06-06","2015-06-07","2015-06-08","2015-06-09","2015-06-10","2015-06-11","2015-06-12","2015-06-13","2015-06-14","2015-06-15","2015-06-16","2015-06-17","2015-06-18","2015-06-19","2015-06-20","2015-06-21","2015-06-22","2015-06-23","2015-06-24","2015-06-25","2015-06-26","2015-06-27","2015-06-28","2015-06-29","2015-06-30","2015-07-01","2015-07-02","2015-07-03","2015-07-04","2015-07-05","2015-07-06","2015-07-07","2015-07-08","2015-07-09","2015-07-10","2015-07-11","2015-07-12","2015-07-13","2015-07-14","2015-07-15","2015-07-16","2015-07-17","2015-07-18","2015-07-19","2015-07-20","2015-07-21","2015-07-22","2015-07-23","2015-07-24","2015-07-25","2015-07-26","2015-07-27","2015-07-28","2015-07-29","2015-07-30","2015-07-31","2015-08-01","2015-08-02","2015-08-03","2015-08-04","2015-08-05","2015-08-06","2015-08-07","2015-08-08","2015-08-09","2015-08-10","2015-08-11","2015-08-12","2015-08-13","2015-08-14","2015-08-15","2015-08-16","2015-08-17","2015-08-18","2015-08-19","2015-08-20","2015-08-21","2015-08-22","2015-08-23","2015-08-24","2015-08-25","2015-08-26","2015-08-27","2015-08-28","2015-08-29","2015-08-30","2015-08-31","2015-09-01","2015-09-02","2015-09-03","2015-09-04","2015-09-05","2015-09-06","2015-09-07","2015-09-08","2015-09-09","2015-09-10","2015-09-11","2015-09-12","2015-09-13","2015-09-14","2015-09-15","2015-09-16","2015-09-17","2015-09-18","2015-09-19","2015-09-20","2015-09-21","2015-09-22","2015-09-23","2015-09-24","2015-09-25","2015-09-26","2015-09-27","2015-09-28","2015-09-29","2015-09-30","2015-10-01","2015-10-02","2015-10-03","2015-10-04","2015-10-05","2015-10-06","2015-10-07","2015-10-08","2015-10-09","2015-10-10","2015-10-11","2015-10-12","2015-10-13","2015-10-14","2015-10-15","2015-10-16","2015-10-17","2015-10-18","2015-10-19","2015-10-20","2015-10-21","2015-10-22","2015-10-23","2015-10-24","2015-10-25","2015-10-26","2015-10-27","2015-10-28","2015-10-29","2015-10-30","2015-10-31","2015-11-01","2015-11-02","2015-11-03","2015-11-04","2015-11-05","2015-11-06","2015-11-07","2015-11-08","2015-11-09","2015-11-10","2015-11-11","2015-11-12","2015-11-13","2015-11-14","2015-11-15","2015-11-16","2015-11-17","2015-11-18","2015-11-19","2015-11-20","2015-11-21","2015-11-22","2015-11-23","2015-11-24","2015-11-25","2015-11-26","2015-11-27","2015-11-28","2015-11-29","2015-11-30","2015-12-01","2015-12-02","2015-12-03","2015-12-04","2015-12-05","2015-12-06","2015-12-07","2015-12-08","2015-12-09","2015-12-10","2015-12-11","2015-12-12","2015-12-13","2015-12-14","2015-12-15","2015-12-16","2015-12-17","2015-12-18","2015-12-19","2015-12-20","2015-12-21","2015-12-22","2015-12-23","2015-12-24","2015-12-25","2015-12-26","2015-12-27","2015-12-28","2015-12-29","2015-12-30","2015-12-31","2016-01-01","2016-01-02","2016-01-03","2016-01-04","2016-01-05","2016-01-06","2016-01-07","2016-01-08","2016-01-09","2016-01-10","2016-01-11","2016-01-12","2016-01-13","2016-01-14","2016-01-15","2016-01-16","2016-01-17","2016-01-18","2016-01-19","2016-01-20","2016-01-21","2016-01-22","2016-01-23","2016-01-24","2016-01-25","2016-01-26","2016-01-27","2016-01-28","2016-01-29","2016-01-30","2016-01-31","2016-02-01","2016-02-02","2016-02-03","2016-02-04","2016-02-05","2016-02-06","2016-02-07","2016-02-08","2016-02-09","2016-02-10","2016-02-11","2016-02-12","2016-02-13","2016-02-14","2016-02-15","2016-02-16","2016-02-17","2016-02-18","2016-02-19","2016-02-20","2016-02-21","2016-02-22","2016-02-23","2016-02-24","2016-02-25","2016-02-26","2016-02-27","2016-02-28","2016-02-29","2016-03-01","2016-03-02","2016-03-03","2016-03-04","2016-03-05","2016-03-06","2016-03-07","2016-03-08","2016-03-09","2016-03-10","2016-03-11","2016-03-12","2016-03-13","2016-03-14","2016-03-15","2016-03-16","2016-03-17","2016-03-18","2016-03-19","2016-03-20","2016-03-21","2016-03-22","2016-03-23","2016-03-24","2016-03-25","2016-03-26","2016-03-27","2016-03-28","2016-03-29","2016-03-30","2016-03-31","2016-04-01","2016-04-02","2016-04-03","2016-04-04","2016-04-05","2016-04-06","2016-04-07","2016-04-08","2016-04-09","2016-04-10","2016-04-11","2016-04-12","2016-04-13","2016-04-14","2016-04-15","2016-04-16","2016-04-17","2016-04-18","2016-04-19","2016-04-20","2016-04-21","2016-04-22","2016-04-23","2016-04-24","2016-04-25","2016-04-26","2016-04-27","2016-04-28","2016-04-29","2016-04-30","2016-05-01","2016-05-02","2016-05-03","2016-05-04","2016-05-05","2016-05-06","2016-05-07","2016-05-08","2016-05-09","2016-05-10","2016-05-11","2016-05-12","2016-05-13","2016-05-14","2016-05-15","2016-05-16","2016-05-17","2016-05-18","2016-05-19","2016-05-20","2016-05-21","2016-05-22","2016-05-23","2016-05-24","2016-05-25","2016-05-26","2016-05-27","2016-05-28","2016-05-29","2016-05-30","2016-05-31","2016-06-01","2016-06-02","2016-06-03","2016-06-04","2016-06-05","2016-06-06","2016-06-07","2016-06-08","2016-06-09","2016-06-10","2016-06-11","2016-06-12","2016-06-13","2016-06-14","2016-06-15","2016-06-16","2016-06-17","2016-06-18","2016-06-19","2016-06-20","2016-06-21","2016-06-22","2016-06-23","2016-06-24","2016-06-25","2016-06-26","2016-06-27","2016-06-28","2016-06-29","2016-06-30","2016-07-01","2016-07-02","2016-07-03","2016-07-04","2016-07-05","2016-07-06","2016-07-07","2016-07-08","2016-07-09","2016-07-10","2016-07-11","2016-07-12","2016-07-13","2016-07-14","2016-07-15","2016-07-16","2016-07-17","2016-07-18","2016-07-19","2016-07-20","2016-07-21","2016-07-22","2016-07-23","2016-07-24","2016-07-25","2016-07-26","2016-07-27","2016-07-28","2016-07-29","2016-07-30","2016-07-31","2016-08-01","2016-08-02","2016-08-03","2016-08-04","2016-08-05","2016-08-06","2016-08-07","2016-08-08","2016-08-09","2016-08-10","2016-08-11","2016-08-12","2016-08-13","2016-08-14","2016-08-15","2016-08-16","2016-08-17","2016-08-18","2016-08-19","2016-08-20","2016-08-21","2016-08-22","2016-08-23","2016-08-24","2016-08-25","2016-08-26","2016-08-27","2016-08-28","2016-08-29","2016-08-30","2016-08-31","2016-09-01","2016-09-02","2016-09-03","2016-09-04","2016-09-05","2016-09-06","2016-09-07","2016-09-08","2016-09-09","2016-09-10","2016-09-11","2016-09-12","2016-09-13","2016-09-14","2016-09-15","2016-09-16","2016-09-17","2016-09-18","2016-09-19","2016-09-20","2016-09-21","2016-09-22","2016-09-23","2016-09-24","2016-09-25","2016-09-26","2016-09-27","2016-09-28","2016-09-29","2016-09-30","2016-10-01","2016-10-02","2016-10-03","2016-10-04","2016-10-05","2016-10-06","2016-10-07","2016-10-08","2016-10-09","2016-10-10","2016-10-11","2016-10-12","2016-10-13","2016-10-14","2016-10-15","2016-10-16","2016-10-17","2016-10-18","2016-10-19","2016-10-20","2016-10-21","2016-10-22","2016-10-23","2016-10-24","2016-10-25","2016-10-26","2016-10-27","2016-10-28","2016-10-29","2016-10-30","2016-10-31","2016-11-01","2016-11-02","2016-11-03","2016-11-04","2016-11-05","2016-11-06","2016-11-07","2016-11-08","2016-11-09","2016-11-10","2016-11-11","2016-11-12","2016-11-13","2016-11-14","2016-11-15","2016-11-16","2016-11-17","2016-11-18","2016-11-19","2016-11-20","2016-11-21","2016-11-22","2016-11-23","2016-11-24","2016-11-25","2016-11-26","2016-11-27","2016-11-28","2016-11-29","2016-11-30","2016-12-01","2016-12-02","2016-12-03","2016-12-04","2016-12-05","2016-12-06","2016-12-07","2016-12-08","2016-12-09","2016-12-10","2016-12-11","2016-12-12","2016-12-13","2016-12-14","2016-12-15","2016-12-16","2016-12-17","2016-12-18","2016-12-19","2016-12-20","2016-12-21","2016-12-22","2016-12-23","2016-12-24","2016-12-25","2016-12-26","2016-12-27","2016-12-28","2016-12-29","2016-12-30","2016-12-31","2017-01-01","2017-01-02","2017-01-03","2017-01-04","2017-01-05","2017-01-06","2017-01-07","2017-01-08","2017-01-09","2017-01-10","2017-01-11","2017-01-12","2017-01-13","2017-01-14","2017-01-15","2017-01-16","2017-01-17","2017-01-18","2017-01-19","2017-01-20","2017-01-21","2017-01-22","2017-01-23","2017-01-24","2017-01-25","2017-01-26","2017-01-27","2017-01-28","2017-01-29","2017-01-30","2017-01-31","2017-02-01","2017-02-02","2017-02-03","2017-02-04","2017-02-05","2017-02-06","2017-02-07","2017-02-08","2017-02-09","2017-02-10","2017-02-11","2017-02-12","2017-02-13","2017-02-14","2017-02-15","2017-02-16","2017-02-17","2017-02-18","2017-02-19","2017-02-20","2017-02-21","2017-02-22","2017-02-23","2017-02-24","2017-02-25","2017-02-26","2017-02-27","2017-02-28","2017-03-01","2017-03-02","2017-03-03","2017-03-04","2017-03-05","2017-03-06","2017-03-07","2017-03-08","2017-03-09","2017-03-10","2017-03-11","2017-03-12","2017-03-13","2017-03-14","2017-03-15","2017-03-16","2017-03-17","2017-03-18","2017-03-19","2017-03-20","2017-03-21","2017-03-22","2017-03-23","2017-03-24","2017-03-25","2017-03-26","2017-03-27","2017-03-28","2017-03-29","2017-03-30","2017-03-31","2017-04-01","2017-04-02","2017-04-03","2017-04-04","2017-04-05","2017-04-06","2017-04-07","2017-04-08","2017-04-09","2017-04-10","2017-04-11","2017-04-12","2017-04-13","2017-04-14","2017-04-15","2017-04-16","2017-04-17","2017-04-18","2017-04-19","2017-04-20","2017-04-21","2017-04-22","2017-04-23","2017-04-24","2017-04-25","2017-04-26","2017-04-27","2017-04-28","2017-04-29","2017-04-30","2017-05-01","2017-05-02","2017-05-03","2017-05-04","2017-05-05","2017-05-06","2017-05-07","2017-05-08","2017-05-09","2017-05-10","2017-05-11","2017-05-12","2017-05-13","2017-05-14","2017-05-15","2017-05-16","2017-05-17","2017-05-18","2017-05-19","2017-05-20","2017-05-21","2017-05-22","2017-05-23","2017-05-24","2017-05-25","2017-05-26","2017-05-27","2017-05-28","2017-05-29","2017-05-30","2017-05-31","2017-06-01","2017-06-02","2017-06-03","2017-06-04","2017-06-05","2017-06-06","2017-06-07","2017-06-08","2017-06-09","2017-06-10","2017-06-11","2017-06-12","2017-06-13","2017-06-14","2017-06-15","2017-06-16","2017-06-17","2017-06-18","2017-06-19","2017-06-20","2017-06-21","2017-06-22","2017-06-23","2017-06-24","2017-06-25","2017-06-26","2017-06-27","2017-06-28","2017-06-29","2017-06-30","2017-07-01","2017-07-02","2017-07-03","2017-07-04","2017-07-05","2017-07-06","2017-07-07","2017-07-08","2017-07-09","2017-07-10","2017-07-11","2017-07-12","2017-07-13","2017-07-14","2017-07-15","2017-07-16","2017-07-17","2017-07-18","2017-07-19","2017-07-20","2017-07-21","2017-07-22","2017-07-23","2017-07-24","2017-07-25","2017-07-26","2017-07-27","2017-07-28","2017-07-29","2017-07-30","2017-07-31","2017-08-01","2017-08-02","2017-08-03","2017-08-04","2017-08-05","2017-08-06","2017-08-07","2017-08-08","2017-08-09","2017-08-10","2017-08-11","2017-08-12","2017-08-13","2017-08-14","2017-08-15","2017-08-16","2017-08-17","2017-08-18","2017-08-19","2017-08-20","2017-08-21","2017-08-22","2017-08-23","2017-08-24","2017-08-25","2017-08-26","2017-08-27","2017-08-28","2017-08-29","2017-08-30","2017-08-31","2017-09-01","2017-09-02","2017-09-03","2017-09-04","2017-09-05","2017-09-06","2017-09-07","2017-09-08","2017-09-09","2017-09-10","2017-09-11","2017-09-12","2017-09-13","2017-09-14","2017-09-15","2017-09-16","2017-09-17","2017-09-18","2017-09-19","2017-09-20","2017-09-21","2017-09-22","2017-09-23","2017-09-24","2017-09-25","2017-09-26","2017-09-27","2017-09-28","2017-09-29","2017-09-30","2017-10-01","2017-10-02","2017-10-03","2017-10-04","2017-10-05","2017-10-06","2017-10-07","2017-10-08","2017-10-09","2017-10-10","2017-10-11","2017-10-12","2017-10-13","2017-10-14","2017-10-15","2017-10-16","2017-10-17","2017-10-18","2017-10-19","2017-10-20","2017-10-21","2017-10-22","2017-10-23","2017-10-24","2017-10-25","2017-10-26","2017-10-27","2017-10-28","2017-10-29","2017-10-30","2017-10-31","2017-11-01","2017-11-02","2017-11-03","2017-11-04","2017-11-05","2017-11-06","2017-11-07","2017-11-08","2017-11-09","2017-11-10","2017-11-11","2017-11-12","2017-11-13","2017-11-14","2017-11-15","2017-11-16","2017-11-17","2017-11-18","2017-11-19","2017-11-20","2017-11-21","2017-11-22","2017-11-23","2017-11-24","2017-11-25","2017-11-26","2017-11-27","2017-11-28","2017-11-29","2017-11-30","2017-12-01","2017-12-02","2017-12-03","2017-12-04","2017-12-05","2017-12-06","2017-12-07","2017-12-08","2017-12-09","2017-12-10","2017-12-11","2017-12-12","2017-12-13","2017-12-14","2017-12-15","2017-12-16","2017-12-17","2017-12-18","2017-12-19","2017-12-20","2017-12-21","2017-12-22","2017-12-23","2017-12-24","2017-12-25","2017-12-26","2017-12-27","2017-12-28","2017-12-29","2017-12-30","2017-12-31","2018-01-01","2018-01-02","2018-01-03","2018-01-04","2018-01-05","2018-01-06","2018-01-07","2018-01-08","2018-01-09","2018-01-10","2018-01-11","2018-01-12","2018-01-13","2018-01-14","2018-01-15","2018-01-16","2018-01-17","2018-01-18","2018-01-19","2018-01-20","2018-01-21","2018-01-22","2018-01-23","2018-01-24","2018-01-25","2018-01-26","2018-01-27","2018-01-28","2018-01-29","2018-01-30","2018-01-31","2018-02-01","2018-02-02","2018-02-03","2018-02-04","2018-02-05","2018-02-06","2018-02-07","2018-02-08","2018-02-09","2018-02-10","2018-02-11","2018-02-12","2018-02-13","2018-02-14","2018-02-15","2018-02-16","2018-02-17","2018-02-18","2018-02-19","2018-02-20","2018-02-21","2018-02-22","2018-02-23","2018-02-24","2018-02-25","2018-02-26","2018-02-27","2018-02-28","2018-03-01","2018-03-02","2018-03-03","2018-03-04","2018-03-05","2018-03-06","2018-03-07","2018-03-08","2018-03-09","2018-03-10","2018-03-11","2018-03-12","2018-03-13","2018-03-14","2018-03-15","2018-03-16","2018-03-17","2018-03-18","2018-03-19","2018-03-20","2018-03-21","2018-03-22","2018-03-23","2018-03-24","2018-03-25","2018-03-26","2018-03-27","2018-03-28","2018-03-29","2018-03-30","2018-03-31","2018-04-01","2018-04-02","2018-04-03","2018-04-04","2018-04-05","2018-04-06","2018-04-07","2018-04-08","2018-04-09","2018-04-10","2018-04-11","2018-04-12","2018-04-13","2018-04-14","2018-04-15","2018-04-16","2018-04-17","2018-04-18","2018-04-19","2018-04-20","2018-04-21","2018-04-22","2018-04-23","2018-04-24","2018-04-25","2018-04-26","2018-04-27","2018-04-28","2018-04-29","2018-04-30","2018-05-01","2018-05-02","2018-05-03","2018-05-04","2018-05-05","2018-05-06","2018-05-07","2018-05-08","2018-05-09","2018-05-10","2018-05-11","2018-05-12","2018-05-13","2018-05-14","2018-05-15","2018-05-16","2018-05-17","2018-05-18","2018-05-19","2018-05-20","2018-05-21","2018-05-22","2018-05-23","2018-05-24","2018-05-25","2018-05-26","2018-05-27","2018-05-28","2018-05-29","2018-05-30","2018-05-31","2018-06-01","2018-06-02","2018-06-03","2018-06-04","2018-06-05","2018-06-06","2018-06-07","2018-06-08","2018-06-09","2018-06-10","2018-06-11","2018-06-12","2018-06-13","2018-06-14","2018-06-15","2018-06-16","2018-06-17","2018-06-18","2018-06-19","2018-06-20","2018-06-21","2018-06-22","2018-06-23","2018-06-24","2018-06-25","2018-06-26","2018-06-27","2018-06-28","2018-06-29","2018-06-30","2018-07-01","2018-07-02","2018-07-03","2018-07-04","2018-07-05","2018-07-06","2018-07-07","2018-07-08","2018-07-09","2018-07-10","2018-07-11","2018-07-12","2018-07-13","2018-07-14","2018-07-15","2018-07-16","2018-07-17","2018-07-18","2018-07-19","2018-07-20","2018-07-21","2018-07-22","2018-07-23","2018-07-24","2018-07-25","2018-07-26","2018-07-27","2018-07-28","2018-07-29","2018-07-30","2018-07-31","2018-08-01","2018-08-02","2018-08-03","2018-08-04","2018-08-05","2018-08-06","2018-08-07","2018-08-08","2018-08-09","2018-08-10","2018-08-11","2018-08-12","2018-08-13","2018-08-14","2018-08-15","2018-08-16","2018-08-17","2018-08-18","2018-08-19","2018-08-20","2018-08-21","2018-08-22","2018-08-23","2018-08-24","2018-08-25","2018-08-26","2018-08-27","2018-08-28","2018-08-29","2018-08-30","2018-08-31","2018-09-01","2018-09-02","2018-09-03","2018-09-04","2018-09-05","2018-09-06","2018-09-07","2018-09-08","2018-09-09","2018-09-10","2018-09-11","2018-09-12","2018-09-13","2018-09-14","2018-09-15","2018-09-16","2018-09-17","2018-09-18","2018-09-19","2018-09-20","2018-09-21","2018-09-22","2018-09-23","2018-09-24","2018-09-25","2018-09-26","2018-09-27","2018-09-28","2018-09-29","2018-09-30","2018-10-01","2018-10-02","2018-10-03","2018-10-04","2018-10-05","2018-10-06","2018-10-07","2018-10-08","2018-10-09","2018-10-10","2018-10-11","2018-10-12","2018-10-13","2018-10-14","2018-10-15","2018-10-16","2018-10-17","2018-10-18","2018-10-19","2018-10-20","2018-10-21","2018-10-22","2018-10-23","2018-10-24","2018-10-25","2018-10-26","2018-10-27","2018-10-28","2018-10-29","2018-10-30","2018-10-31","2018-11-01","2018-11-02","2018-11-03","2018-11-04","2018-11-05","2018-11-06","2018-11-07","2018-11-08","2018-11-09","2018-11-10","2018-11-11","2018-11-12","2018-11-13","2018-11-14","2018-11-15","2018-11-16","2018-11-17","2018-11-18","2018-11-19","2018-11-20","2018-11-21","2018-11-22","2018-11-23","2018-11-24","2018-11-25","2018-11-26","2018-11-27","2018-11-28","2018-11-29","2018-11-30","2018-12-01","2018-12-02","2018-12-03","2018-12-04","2018-12-05","2018-12-06","2018-12-07","2018-12-08","2018-12-09","2018-12-10","2018-12-11","2018-12-12","2018-12-13","2018-12-14","2018-12-15","2018-12-16","2018-12-17","2018-12-18","2018-12-19","2018-12-20","2018-12-21","2018-12-22","2018-12-23","2018-12-24","2018-12-25","2018-12-26","2018-12-27","2018-12-28","2018-12-29","2018-12-30","2018-12-31","2019-01-01","2019-01-02","2019-01-03","2019-01-04","2019-01-05","2019-01-06","2019-01-07","2019-01-08","2019-01-09","2019-01-10","2019-01-11","2019-01-12","2019-01-13","2019-01-14","2019-01-15","2019-01-16","2019-01-17","2019-01-18","2019-01-19","2019-01-20","2019-01-21","2019-01-22","2019-01-23","2019-01-24","2019-01-25","2019-01-26","2019-01-27","2019-01-28","2019-01-29","2019-01-30","2019-01-31","2019-02-01","2019-02-02","2019-02-03","2019-02-04","2019-02-05","2019-02-06","2019-02-07","2019-02-08","2019-02-09","2019-02-10","2019-02-11","2019-02-12","2019-02-13","2019-02-14","2019-02-15","2019-02-16","2019-02-17","2019-02-18","2019-02-19","2019-02-20","2019-02-21","2019-02-22","2019-02-23","2019-02-24","2019-02-25","2019-02-26","2019-02-27","2019-02-28","2019-03-01","2019-03-02","2019-03-03","2019-03-04","2019-03-05","2019-03-06","2019-03-07","2019-03-08","2019-03-09","2019-03-10","2019-03-11","2019-03-12","2019-03-13","2019-03-14","2019-03-15","2019-03-16","2019-03-17","2019-03-18","2019-03-19","2019-03-20","2019-03-21","2019-03-22","2019-03-23","2019-03-24","2019-03-25","2019-03-26","2019-03-27","2019-03-28","2019-03-29","2019-03-30","2019-03-31","2019-04-01","2019-04-02","2019-04-03","2019-04-04","2019-04-05","2019-04-06","2019-04-07","2019-04-08","2019-04-09","2019-04-10","2019-04-11","2019-04-12","2019-04-13","2019-04-14","2019-04-15","2019-04-16","2019-04-17","2019-04-18","2019-04-19","2019-04-20","2019-04-21","2019-04-22","2019-04-23","2019-04-24","2019-04-25","2019-04-26","2019-04-27","2019-04-28","2019-04-29","2019-04-30","2019-05-01","2019-05-02","2019-05-03","2019-05-04","2019-05-05","2019-05-06","2019-05-07","2019-05-08","2019-05-09","2019-05-10","2019-05-11","2019-05-12","2019-05-13","2019-05-14","2019-05-15","2019-05-16","2019-05-17","2019-05-18","2019-05-19","2019-05-20","2019-05-21","2019-05-22","2019-05-23","2019-05-24","2019-05-25","2019-05-26","2019-05-27","2019-05-28","2019-05-29","2019-05-30","2019-05-31","2019-06-01","2019-06-02","2019-06-03","2019-06-04","2019-06-05","2019-06-06","2019-06-07","2019-06-08","2019-06-09","2019-06-10","2019-06-11","2019-06-12","2019-06-13","2019-06-14","2019-06-15","2019-06-16","2019-06-17","2019-06-18","2019-06-19","2019-06-20","2019-06-21","2019-06-22","2019-06-23","2019-06-24","2019-06-25","2019-06-26","2019-06-27","2019-06-28","2019-06-29","2019-06-30","2019-07-01","2019-07-02","2019-07-03","2019-07-04","2019-07-05","2019-07-06","2019-07-07","2019-07-08","2019-07-09","2019-07-10","2019-07-11","2019-07-12","2019-07-13","2019-07-14","2019-07-15","2019-07-16","2019-07-17","2019-07-18","2019-07-19","2019-07-20","2019-07-21","2019-07-22","2019-07-23","2019-07-24","2019-07-25","2019-07-26","2019-07-27","2019-07-28","2019-07-29","2019-07-30","2019-07-31","2019-08-01","2019-08-02","2019-08-03","2019-08-04","2019-08-05","2019-08-06","2019-08-07","2019-08-08","2019-08-09","2019-08-10","2019-08-11","2019-08-12","2019-08-13","2019-08-14","2019-08-15","2019-08-16","2019-08-17","2019-08-18","2019-08-19","2019-08-20","2019-08-21","2019-08-22","2019-08-23","2019-08-24","2019-08-25","2019-08-26","2019-08-27","2019-08-28","2019-08-29","2019-08-30","2019-08-31","2019-09-01","2019-09-02","2019-09-03","2019-09-04","2019-09-05","2019-09-06","2019-09-07","2019-09-08","2019-09-09","2019-09-10","2019-09-11","2019-09-12","2019-09-13","2019-09-14","2019-09-15","2019-09-16","2019-09-17","2019-09-18","2019-09-19","2019-09-20","2019-09-21","2019-09-22","2019-09-23","2019-09-24","2019-09-25","2019-09-26","2019-09-27","2019-09-28","2019-09-29","2019-09-30","2019-10-01","2019-10-02","2019-10-03","2019-10-04","2019-10-05","2019-10-06","2019-10-07","2019-10-08","2019-10-09","2019-10-10","2019-10-11","2019-10-12","2019-10-13","2019-10-14","2019-10-15","2019-10-16","2019-10-17","2019-10-18","2019-10-19","2019-10-20","2019-10-21","2019-10-22","2019-10-23","2019-10-24","2019-10-25","2019-10-26","2019-10-27","2019-10-28","2019-10-29","2019-10-30","2019-10-31","2019-11-01","2019-11-02","2019-11-03","2019-11-04","2019-11-05","2019-11-06","2019-11-07","2019-11-08","2019-11-09","2019-11-10","2019-11-11","2019-11-12","2019-11-13","2019-11-14","2019-11-15","2019-11-16","2019-11-17","2019-11-18","2019-11-19","2019-11-20","2019-11-21","2019-11-22","2019-11-23","2019-11-24","2019-11-25","2019-11-26","2019-11-27","2019-11-28","2019-11-29","2019-11-30","2019-12-01","2019-12-02","2019-12-03","2019-12-04","2019-12-05","2019-12-06","2019-12-07","2019-12-08","2019-12-09","2019-12-10","2019-12-11","2019-12-12","2019-12-13","2019-12-14","2019-12-15","2019-12-16","2019-12-17","2019-12-18","2019-12-19","2019-12-20","2019-12-21","2019-12-22","2019-12-23","2019-12-24","2019-12-25","2019-12-26","2019-12-27","2019-12-28","2019-12-29","2019-12-30","2019-12-31","2020-01-01","2020-01-02","2020-01-03","2020-01-04","2020-01-05","2020-01-06","2020-01-07","2020-01-08","2020-01-09","2020-01-10","2020-01-11","2020-01-12","2020-01-13","2020-01-14","2020-01-15","2020-01-16","2020-01-17","2020-01-18","2020-01-19","2020-01-20","2020-01-21","2020-01-22","2020-01-23","2020-01-24","2020-01-25","2020-01-26","2020-01-27","2020-01-28","2020-01-29","2020-01-30","2020-01-31","2020-02-01","2020-02-02","2020-02-03","2020-02-04","2020-02-05","2020-02-06","2020-02-07","2020-02-08","2020-02-09","2020-02-10","2020-02-11","2020-02-12","2020-02-13","2020-02-14","2020-02-15","2020-02-16","2020-02-17","2020-02-18","2020-02-19","2020-02-20","2020-02-21","2020-02-22","2020-02-23","2020-02-24","2020-02-25","2020-02-26","2020-02-27","2020-02-28","2020-02-29","2020-03-01","2020-03-02","2020-03-03","2020-03-04","2020-03-05","2020-03-06","2020-03-07","2020-03-08","2020-03-09","2020-03-10","2020-03-11","2020-03-12","2020-03-13","2020-03-14","2020-03-15","2020-03-16","2020-03-17","2020-03-18","2020-03-19","2020-03-20","2020-03-21","2020-03-22","2020-03-23","2020-03-24","2020-03-25","2020-03-26","2020-03-27","2020-03-28","2020-03-29","2020-03-30","2020-03-31","2020-04-01","2020-04-02","2020-04-03","2020-04-04","2020-04-05","2020-04-06","2020-04-07","2020-04-08","2020-04-09","2020-04-10","2020-04-11","2020-04-12","2020-04-13","2020-04-14","2020-04-15","2020-04-16","2020-04-17","2020-04-18","2020-04-19","2020-04-20","2020-04-21","2020-04-22","2020-04-23","2020-04-24","2020-04-25","2020-04-26","2020-04-27","2020-04-28","2020-04-29","2020-04-30","2020-05-01","2020-05-02","2020-05-03","2020-05-04","2020-05-05","2020-05-06","2020-05-07","2020-05-08","2020-05-09","2020-05-10","2020-05-11","2020-05-12","2020-05-13","2020-05-14","2020-05-15","2020-05-16","2020-05-17","2020-05-18","2020-05-19","2020-05-20","2020-05-21","2020-05-22","2020-05-23","2020-05-24","2020-05-25","2020-05-26","2020-05-27","2020-05-28","2020-05-29","2020-05-30","2020-05-31","2020-06-01","2020-06-02","2020-06-03","2020-06-04","2020-06-05","2020-06-06","2020-06-07","2020-06-08","2020-06-09","2020-06-10","2020-06-11","2020-06-12","2020-06-13","2020-06-14","2020-06-15","2020-06-16","2020-06-17","2020-06-18","2020-06-19","2020-06-20","2020-06-21","2020-06-22","2020-06-23","2020-06-24","2020-06-25","2020-06-26","2020-06-27","2020-06-28","2020-06-29","2020-06-30","2020-07-01","2020-07-02","2020-07-03","2020-07-04","2020-07-05","2020-07-06","2020-07-07","2020-07-08","2020-07-09","2020-07-10","2020-07-11","2020-07-12","2020-07-13","2020-07-14","2020-07-15","2020-07-16","2020-07-17","2020-07-18","2020-07-19","2020-07-20","2020-07-21","2020-07-22","2020-07-23","2020-07-24","2020-07-25","2020-07-26","2020-07-27","2020-07-28","2020-07-29","2020-07-30","2020-07-31","2020-08-01","2020-08-02","2020-08-03","2020-08-04","2020-08-05","2020-08-06","2020-08-07","2020-08-08","2020-08-09","2020-08-10","2020-08-11","2020-08-12","2020-08-13","2020-08-14","2020-08-15","2020-08-16","2020-08-17","2020-08-18","2020-08-19","2020-08-20","2020-08-21","2020-08-22","2020-08-23","2020-08-24","2020-08-25","2020-08-26","2020-08-27","2020-08-28","2020-08-29","2020-08-30","2020-08-31","2020-09-01","2020-09-02","2020-09-03","2020-09-04","2020-09-05","2020-09-06","2020-09-07","2020-09-08","2020-09-09","2020-09-10","2020-09-11","2020-09-12","2020-09-13","2020-09-14","2020-09-15","2020-09-16","2020-09-17","2020-09-18","2020-09-19","2020-09-20","2020-09-21","2020-09-22","2020-09-23","2020-09-24","2020-09-25","2020-09-26","2020-09-27","2020-09-28","2020-09-29","2020-09-30","2020-10-01","2020-10-02","2020-10-03","2020-10-04","2020-10-05","2020-10-06","2020-10-07","2020-10-08","2020-10-09","2020-10-10","2020-10-11","2020-10-12","2020-10-13","2020-10-14","2020-10-15","2020-10-16","2020-10-17","2020-10-18","2020-10-19","2020-10-20","2020-10-21","2020-10-22","2020-10-23","2020-10-24","2020-10-25","2020-10-26","2020-10-27","2020-10-28","2020-10-29","2020-10-30","2020-10-31","2020-11-01","2020-11-02","2020-11-03","2020-11-04","2020-11-05","2020-11-06","2020-11-07","2020-11-08","2020-11-09","2020-11-10","2020-11-11","2020-11-12","2020-11-13","2020-11-14","2020-11-15","2020-11-16","2020-11-17","2020-11-18","2020-11-19","2020-11-20","2020-11-21","2020-11-22","2020-11-23","2020-11-24","2020-11-25","2020-11-26","2020-11-27","2020-11-28","2020-11-29","2020-11-30","2020-12-01","2020-12-02","2020-12-03","2020-12-04","2020-12-05","2020-12-06","2020-12-07","2020-12-08","2020-12-09","2020-12-10","2020-12-11","2020-12-12","2020-12-13","2020-12-14","2020-12-15","2020-12-16","2020-12-17","2020-12-18","2020-12-19","2020-12-20","2020-12-21","2020-12-22","2020-12-23","2020-12-24","2020-12-25","2020-12-26","2020-12-27","2020-12-28","2020-12-29","2020-12-30","2020-12-31","2021-01-01","2021-01-02","2021-01-03","2021-01-04","2021-01-05","2021-01-06","2021-01-07","2021-01-08","2021-01-09","2021-01-10","2021-01-11"],"y":[0.37247,0.37247,0.37247,0.3724,0.37233,0.37226,0.37221,0.37216,0.37211,0.37207,0.37203,0.372,0.37197,0.37195,0.37193,0.37192,0.37191,0.3719,0.37189,0.37189,0.37188,0.37187,0.37187,0.37187,0.37187,0.37187,0.37187,0.37187,0.37186,0.37186,0.37184,0.37182,0.3718,0.37177,0.37174,0.37172,0.37171,0.37171,0.37173,0.37176,0.37182,0.37188,0.37196,0.37203,0.37211,0.37218,0.37224,0.37228,0.37231,0.37232,0.37232,0.37232,0.37232,0.37232,0.37232,0.37235,0.37239,0.37245,0.37254,0.37264,0.37275,0.37287,0.37298,0.3731,0.3732,0.37329,0.37338,0.37348,0.37358,0.37368,0.37378,0.37386,0.37394,0.37399,0.37403,0.3741,0.37425,0.37442,0.37455,0.37459,0.37449,0.37423,0.37387,0.37344,0.37298,0.37253,0.37212,0.37167,0.3711,0.37045,0.36977,0.36908,0.36844,0.36789,0.36746,0.36719,0.36707,0.36705,0.3671,0.36722,0.3674,0.36762,0.36788,0.36816,0.36844,0.36864,0.36871,0.3687,0.3687,0.36876,0.36896,0.36935,0.37002,0.37101,0.37231,0.37382,0.37554,0.37745,0.37955,0.38184,0.38429,0.38691,0.38969,0.39279,0.39632,0.40017,0.40423,0.4084,0.41256,0.41661,0.42043,0.42393,0.42729,0.43077,0.43428,0.43777,0.44117,0.44441,0.44742,0.45015,0.45252,0.45462,0.45657,0.45834,0.45992,0.46129,0.46243,0.46331,0.46393,0.46426,0.46399,0.46302,0.46164,0.46013,0.45877,0.45784,0.45698,0.45575,0.45435,0.45294,0.45172,0.45087,0.45039,0.45014,0.45006,0.4501,0.4502,0.45032,0.45039,0.45036,0.45019,0.44987,0.44949,0.44904,0.44854,0.44801,0.44745,0.44688,0.44632,0.44577,0.44521,0.44462,0.44401,0.4434,0.44281,0.44226,0.44177,0.44136,0.44104,0.44082,0.44068,0.44058,0.44052,0.44049,0.44045,0.44039,0.44031,0.44017,0.44,0.43982,0.43964,0.43945,0.43927,0.43909,0.43891,0.43874,0.43857,0.43843,0.43832,0.43822,0.43814,0.43805,0.43795,0.43782,0.43766,0.43746,0.43719,0.43683,0.43642,0.43597,0.43551,0.43505,0.43463,0.43427,0.43398,0.43372,0.43342,0.43312,0.43286,0.43267,0.43257,0.43261,0.43277,0.43299,0.43326,0.43354,0.43378,0.43406,0.43447,0.43497,0.4355,0.43602,0.4365,0.43688,0.43714,0.43721,0.4371,0.43682,0.43644,0.43598,0.4355,0.43503,0.43461,0.43429,0.43411,0.43409,0.43419,0.43437,0.43459,0.43481,0.43499,0.43509,0.43507,0.43489,0.43469,0.43459,0.43454,0.43447,0.43431,0.43399,0.43346,0.43265,0.43149,0.42998,0.42818,0.42613,0.42387,0.42144,0.41887,0.41621,0.4135,0.41077,0.40785,0.40461,0.40112,0.39745,0.39369,0.3899,0.38616,0.38256,0.37916,0.37568,0.37187,0.36789,0.36391,0.36007,0.35653,0.35345,0.35099,0.34931,0.34844,0.34822,0.34845,0.34897,0.34957,0.35008,0.35109,0.35305,0.35553,0.35812,0.36041,0.36199,0.36307,0.36414,0.36518,0.36616,0.36706,0.36787,0.36855,0.3691,0.36948,0.36967,0.3697,0.36959,0.36939,0.36913,0.36884,0.36856,0.36833,0.36818,0.36806,0.36789,0.36769,0.36747,0.36725,0.36703,0.36682,0.36665,0.36653,0.36648,0.36652,0.36663,0.36679,0.36699,0.36719,0.36739,0.36757,0.3677,0.36799,0.36858,0.36936,0.37022,0.37104,0.37171,0.37212,0.37217,0.37172,0.37101,0.37029,0.36959,0.3689,0.36824,0.3676,0.36699,0.36641,0.36588,0.36544,0.36514,0.36494,0.36483,0.36479,0.3648,0.36483,0.36487,0.3649,0.36497,0.36511,0.36531,0.36551,0.3657,0.36584,0.36593,0.366,0.36608,0.36615,0.36625,0.36636,0.3665,0.36667,0.36685,0.36704,0.36724,0.36743,0.36761,0.36777,0.36791,0.36805,0.3682,0.36835,0.36851,0.36866,0.36879,0.3689,0.36897,0.369,0.36897,0.36887,0.36871,0.36852,0.36831,0.3681,0.36792,0.36777,0.36768,0.36764,0.36761,0.3676,0.3676,0.36762,0.36765,0.3677,0.36777,0.36785,0.36797,0.36814,0.36834,0.36856,0.36879,0.36901,0.36922,0.36939,0.36952,0.36962,0.3697,0.36977,0.36982,0.36986,0.36988,0.36989,0.36988,0.36986,0.3698,0.36969,0.36955,0.36938,0.36921,0.36906,0.36893,0.36886,0.36885,0.36889,0.36897,0.36908,0.3692,0.36933,0.36947,0.36962,0.36981,0.37003,0.37025,0.37048,0.3707,0.37085,0.37089,0.37088,0.37085,0.37085,0.37091,0.37109,0.37142,0.37195,0.37254,0.3731,0.37367,0.37432,0.37509,0.37607,0.37729,0.37882,0.38072,0.38305,0.3858,0.3889,0.39225,0.3958,0.39945,0.40315,0.4068,0.41033,0.41402,0.41811,0.42245,0.42693,0.43139,0.43572,0.43977,0.44342,0.44652,0.44919,0.4516,0.45378,0.45572,0.45744,0.45895,0.46025,0.46136,0.46228,0.46289,0.46311,0.46302,0.4627,0.46223,0.46167,0.46111,0.46063,0.46029,0.46003,0.45972,0.45938,0.45902,0.45864,0.45826,0.45789,0.45754,0.45721,0.45695,0.45674,0.45654,0.45634,0.45608,0.45574,0.45528,0.45466,0.45385,0.45279,0.45149,0.45,0.44838,0.44671,0.44505,0.44346,0.44199,0.44072,0.43952,0.43824,0.43694,0.43566,0.43446,0.43339,0.4325,0.43183,0.43146,0.43143,0.43175,0.43233,0.4331,0.43397,0.43487,0.43571,0.43643,0.43693,0.43732,0.43775,0.43819,0.43862,0.439,0.43932,0.43955,0.43965,0.43962,0.43938,0.43894,0.43835,0.43766,0.43692,0.43618,0.43549,0.43491,0.43449,0.43419,0.43394,0.43374,0.43357,0.43344,0.43333,0.43324,0.43316,0.43308,0.43305,0.4331,0.4332,0.43332,0.43344,0.43352,0.43353,0.43345,0.43325,0.43285,0.43228,0.43163,0.43097,0.4304,0.43,0.42975,0.42953,0.42933,0.42913,0.42893,0.42869,0.42845,0.42823,0.42803,0.42785,0.42768,0.42752,0.42737,0.42723,0.42709,0.42696,0.42681,0.42664,0.42647,0.42628,0.42607,0.42585,0.42561,0.42536,0.42519,0.42517,0.42524,0.42537,0.42548,0.42552,0.42545,0.42521,0.42474,0.42419,0.42371,0.42322,0.42266,0.42197,0.42109,0.41995,0.41849,0.41665,0.41424,0.41124,0.40778,0.40399,0.4,0.39595,0.39197,0.3882,0.38478,0.38133,0.37754,0.37356,0.36957,0.36572,0.36217,0.35911,0.35668,0.35505,0.35435,0.35447,0.35524,0.3565,0.35807,0.35978,0.36146,0.36294,0.36405,0.36519,0.36671,0.3684,0.37004,0.37142,0.37232,0.37271,0.37278,0.37266,0.37244,0.37226,0.37221,0.37222,0.37211,0.37192,0.37167,0.3714,0.37112,0.37087,0.37068,0.37056,0.37052,0.37051,0.37053,0.37055,0.37058,0.3706,0.3706,0.37058,0.37051,0.3704,0.37028,0.37014,0.36998,0.36981,0.36964,0.36946,0.36927,0.36909,0.36888,0.36862,0.36833,0.36802,0.3677,0.36738,0.36708,0.36682,0.36659,0.36639,0.36617,0.36596,0.36576,0.36559,0.36546,0.36539,0.36538,0.36547,0.36565,0.3659,0.3662,0.36653,0.36686,0.36717,0.36743,0.36764,0.36779,0.36793,0.36806,0.36817,0.36826,0.36834,0.36839,0.36841,0.36841,0.36836,0.36823,0.36808,0.36791,0.36778,0.3677,0.36769,0.36772,0.36776,0.36781,0.36785,0.36785,0.36783,0.36781,0.36779,0.36777,0.36775,0.36772,0.36768,0.36764,0.36758,0.36747,0.36731,0.36711,0.36689,0.36667,0.36646,0.36628,0.36616,0.3661,0.36611,0.36616,0.36625,0.36636,0.36651,0.36668,0.36687,0.36708,0.36731,0.36758,0.36792,0.3683,0.36872,0.36916,0.3696,0.37002,0.37041,0.37075,0.37104,0.37131,0.37155,0.37176,0.37195,0.37212,0.37227,0.3724,0.37252,0.3726,0.37265,0.37268,0.3727,0.37272,0.37276,0.37282,0.37292,0.37307,0.37328,0.37353,0.37381,0.37411,0.37442,0.37472,0.375,0.37526,0.37548,0.37558,0.37553,0.37539,0.37521,0.37503,0.37491,0.37491,0.37507,0.37545,0.37583,0.37603,0.37618,0.3764,0.37682,0.37754,0.37869,0.38039,0.38276,0.38592,0.38978,0.39418,0.39894,0.40392,0.40893,0.4138,0.41839,0.42251,0.42657,0.43101,0.43565,0.44035,0.44496,0.44931,0.45326,0.45664,0.4593,0.46129,0.46279,0.46386,0.46458,0.46502,0.46523,0.46529,0.46527,0.46523,0.46497,0.46429,0.46328,0.46205,0.4607,0.45931,0.45798,0.45682,0.45591,0.45518,0.45446,0.45376,0.45309,0.45243,0.4518,0.45119,0.4506,0.45003,0.44953,0.44913,0.44879,0.44849,0.44821,0.44791,0.44757,0.44717,0.44668,0.44599,0.44509,0.44409,0.44307,0.44213,0.44139,0.44067,0.43985,0.439,0.43822,0.43761,0.43727,0.4372,0.43733,0.43762,0.43802,0.43847,0.43892,0.43933,0.43964,0.43981,0.43995,0.44018,0.44046,0.44076,0.44103,0.44125,0.44136,0.44134,0.44115,0.44072,0.44005,0.43922,0.43827,0.43728,0.43631,0.43542,0.43466,0.43412,0.43372,0.43338,0.43309,0.43284,0.43263,0.43244,0.43228,0.43213,0.43199,0.43192,0.43195,0.43206,0.43223,0.43244,0.43266,0.43288,0.43307,0.43321,0.43333,0.43346,0.43361,0.43373,0.43384,0.43389,0.43389,0.43382,0.43366,0.43336,0.43293,0.4324,0.43181,0.43119,0.43058,0.43001,0.42952,0.42915,0.42885,0.42857,0.4283,0.42805,0.42783,0.42765,0.4276,0.42773,0.42795,0.42819,0.42836,0.42838,0.42826,0.4281,0.4279,0.42769,0.42747,0.42726,0.42708,0.42692,0.42682,0.4269,0.42722,0.42769,0.4282,0.42867,0.429,0.42909,0.42885,0.42818,0.42712,0.42579,0.42422,0.42243,0.42045,0.41831,0.41602,0.41362,0.41113,0.40833,0.40507,0.40148,0.39769,0.39381,0.38999,0.38634,0.38298,0.38006,0.37737,0.37468,0.37203,0.36948,0.36709,0.36491,0.363,0.36141,0.3602,0.3594,0.35899,0.35889,0.35905,0.35942,0.35994,0.36054,0.36118,0.36179,0.36259,0.36375,0.36517,0.36675,0.36839,0.36998,0.37142,0.37261,0.37345,0.374,0.37442,0.37472,0.37494,0.37509,0.3752,0.37514,0.37485,0.37441,0.37393,0.37349,0.37319,0.37296,0.37266,0.37231,0.37194,0.37156,0.37119,0.37084,0.37054,0.3703,0.37012,0.36997,0.36985,0.36976,0.36969,0.36965,0.36962,0.36961,0.36962,0.36965,0.36973,0.36985,0.36999,0.37015,0.37031,0.37045,0.37058,0.37067,0.37075,0.37083,0.37091,0.37098,0.37103,0.37106,0.37106,0.37103,0.37096,0.37085,0.37072,0.37056,0.37039,0.3702,0.37,0.3698,0.3696,0.36936,0.36907,0.36875,0.3684,0.36806,0.36773,0.36744,0.36721,0.36705,0.36695,0.36689,0.36687,0.36687,0.36689,0.36694,0.367,0.36707,0.36715,0.36726,0.3674,0.36757,0.36776,0.36797,0.36819,0.36841,0.36863,0.36884,0.36905,0.3693,0.36956,0.36983,0.3701,0.37035,0.37058,0.37078,0.37093,0.37105,0.37117,0.37128,0.37137,0.37145,0.37149,0.37151,0.37149,0.37144,0.37131,0.37109,0.3708,0.37047,0.37013,0.36981,0.36952,0.3693,0.36917,0.36912,0.36912,0.36916,0.36923,0.36932,0.36942,0.36953,0.36964,0.36973,0.36983,0.36996,0.37012,0.37029,0.37046,0.37062,0.37077,0.37089,0.37097,0.37101,0.37099,0.37094,0.37087,0.3708,0.37073,0.3707,0.3707,0.37076,0.37088,0.37105,0.37124,0.37147,0.3717,0.37194,0.37217,0.37239,0.37258,0.37273,0.37285,0.37296,0.37307,0.37321,0.37338,0.37355,0.37365,0.37374,0.37384,0.37401,0.37428,0.37447,0.37446,0.37434,0.3742,0.37412,0.3742,0.37453,0.37521,0.37632,0.3778,0.37954,0.38152,0.38375,0.3862,0.38888,0.39178,0.39489,0.39819,0.402,0.40647,0.41144,0.41671,0.42211,0.42747,0.43259,0.4373,0.44141,0.44515,0.44881,0.45234,0.45568,0.45878,0.46158,0.46402,0.46606,0.46762,0.46867,0.46923,0.4694,0.46927,0.46893,0.46845,0.46794,0.46747,0.46714,0.4668,0.46627,0.4656,0.46482,0.46398,0.46313,0.4623,0.46155,0.4609,0.46031,0.45968,0.45902,0.45833,0.45761,0.45687,0.45611,0.45533,0.45455,0.45371,0.45281,0.45189,0.45098,0.45013,0.44937,0.44867,0.44796,0.44726,0.44658,0.44595,0.44539,0.4449,0.44445,0.44405,0.44371,0.44341,0.44317,0.44297,0.44283,0.44273,0.44273,0.44283,0.44301,0.44324,0.44349,0.44373,0.44393,0.44407,0.44411,0.44406,0.44395,0.4438,0.44361,0.4434,0.44319,0.44297,0.44277,0.44259,0.44243,0.44226,0.44209,0.44192,0.44175,0.44159,0.44144,0.44131,0.44119,0.44112,0.44111,0.44113,0.44117,0.44119,0.44118,0.44112,0.44099,0.44075,0.44038,0.43989,0.4393,0.43866,0.43801,0.43738,0.43683,0.43639,0.43609,0.43595,0.43595,0.43603,0.43618,0.43635,0.43651,0.43663,0.43667,0.4366,0.43644,0.43624,0.43601,0.43578,0.43557,0.43538,0.43512,0.43472,0.43425,0.43378,0.43338,0.43312,0.43307,0.43322,0.43351,0.43388,0.43427,0.43461,0.43486,0.43495,0.43481,0.43449,0.43406,0.43353,0.43291,0.4322,0.43142,0.43056,0.42965,0.42867,0.42763,0.42649,0.42527,0.42397,0.42259,0.42114,0.41962,0.41805,0.41642,0.41473,0.41299,0.41119,0.40935,0.40747,0.40556,0.40361,0.40164,0.39965,0.39749,0.39504,0.39242,0.38969,0.38694,0.38428,0.38177,0.37952,0.3776,0.37593,0.37437,0.37293,0.37163,0.37047,0.36948,0.36865,0.368,0.36755,0.36739,0.36759,0.36805,0.36871,0.36949,0.37032,0.37112,0.37183,0.37235,0.37288,0.37359,0.37436,0.3751,0.3757,0.37606,0.37615,0.37605,0.37583,0.37556,0.37532,0.37518,0.37507,0.37491,0.3747,0.37447,0.37422,0.37396,0.37373,0.37352,0.37335,0.37322,0.37309,0.37298,0.37287,0.37278,0.37268,0.3726,0.37251,0.37243,0.37234,0.37223,0.37212,0.372,0.37189,0.3718,0.37173,0.37168,0.37166,0.3717,0.3718,0.37194,0.37209,0.37225,0.37239,0.37249,0.37255,0.37254,0.37251,0.37245,0.37237,0.37228,0.37218,0.37209,0.37201,0.37194,0.37189,0.37183,0.37176,0.3717,0.37165,0.37161,0.37158,0.37156,0.37157,0.37161,0.3717,0.37182,0.37196,0.37211,0.37224,0.37235,0.37242,0.37244,0.3724,0.37232,0.37221,0.37208,0.37196,0.37186,0.37174,0.37157,0.37139,0.37121,0.37105,0.37093,0.37083,0.37073,0.37061,0.37049,0.37037,0.37025,0.37015,0.37006,0.36999,0.36993,0.36987,0.36982,0.36979,0.36978,0.36981,0.36987,0.36998,0.37015,0.37039,0.3707,0.37108,0.37151,0.37196,0.37242,0.37288,0.37331,0.37371,0.3741,0.37451,0.37494,0.37537,0.37577,0.37614,0.37645,0.37668,0.37683,0.37688,0.37685,0.37675,0.37661,0.37644,0.37627,0.37612,0.37601,0.37596,0.3759,0.37579,0.37565,0.3755,0.37537,0.37528,0.37527,0.37535,0.37556,0.37588,0.37627,0.37673,0.37724,0.3778,0.3784,0.37902,0.37965,0.38029,0.38075,0.38099,0.38117,0.38144,0.38198,0.38294,0.38403,0.38494,0.38587,0.38701,0.38856,0.39071,0.39354,0.39693,0.40078,0.40498,0.40942,0.41399,0.41857,0.42307,0.42737,0.4319,0.43703,0.44254,0.4482,0.45379,0.4591,0.46389,0.46795,0.47107,0.47329,0.4749,0.47598,0.4766,0.47686,0.47685,0.47663,0.47631,0.47595,0.4753,0.47411,0.47252,0.47066,0.46865,0.46664,0.46476,0.46314,0.46191,0.46097,0.46014,0.45939,0.45872,0.45811,0.45755,0.45701,0.4565,0.45599,0.4555,0.45504,0.4546,0.45418,0.45377,0.45337,0.45296,0.45254,0.4521,0.45164,0.45116,0.45069,0.45022,0.44976,0.44933,0.44893,0.44857,0.44826,0.44796,0.44763,0.4473,0.447,0.44676,0.44661,0.44656,0.44659,0.44668,0.4468,0.44694,0.44706,0.44721,0.44743,0.44769,0.44799,0.4483,0.4486,0.44888,0.44911,0.44927,0.4494,0.44952,0.44963,0.44972,0.44979,0.44984,0.44986,0.44984,0.44978,0.44968,0.44957,0.44944,0.44929,0.4491,0.44888,0.44862,0.44831,0.44797,0.44754,0.44701,0.44641,0.44577,0.4451,0.44443,0.44378,0.44318,0.44265,0.44216,0.44167,0.44118,0.44072,0.44029,0.43992,0.43962,0.4394,0.43928,0.4393,0.43949,0.43979,0.44014,0.4405,0.44082,0.44105,0.44113,0.44103,0.44072,0.44026,0.43969,0.43904,0.43835,0.43765,0.43698,0.43638,0.43586,0.43548,0.43522,0.43505,0.43493,0.43483,0.43474,0.4346,0.4344,0.43411,0.43378,0.43349,0.4332,0.43287,0.43245,0.43191,0.43122,0.43032,0.42919,0.42786,0.42639,0.42477,0.42301,0.42109,0.41903,0.4168,0.41441,0.41186,0.40892,0.40547,0.40167,0.3977,0.39371,0.38988,0.38636,0.38332,0.38093,0.37903,0.37733,0.37583,0.37453,0.37343,0.37252,0.37181,0.37128,0.37094,0.37102,0.37166,0.3727,0.37402,0.37546,0.37689,0.37815,0.37912,0.37965,0.37979,0.37973,0.37952,0.37919,0.3788,0.37837,0.37796,0.37761,0.37735,0.37715,0.37693,0.3767,0.37647,0.37623,0.37599,0.37575,0.37552,0.3753,0.37508,0.37485,0.37463,0.37441,0.37421,0.37402,0.37385,0.37368,0.37351,0.37336,0.3732,0.37305,0.37291,0.37277,0.37263,0.3725,0.37239,0.37228,0.37218,0.3721,0.37202,0.37196,0.37191,0.37186,0.37182,0.37179,0.37177,0.37176,0.37176,0.37176,0.37179,0.37184,0.37191,0.372,0.37209,0.37219,0.37227,0.37234,0.37239,0.37245,0.37252,0.37261,0.37271,0.3728,0.37288,0.37294,0.37297,0.37296,0.37289,0.37276,0.37258,0.37237,0.37214,0.37191,0.3717,0.37151,0.37136,0.37124,0.3711,0.37097,0.37083,0.37071,0.3706,0.37052,0.37047,0.37046,0.3705,0.37061,0.37076,0.37095,0.37116,0.37138,0.37159,0.37179,0.37196,0.37214,0.37238,0.37263,0.37286,0.37303,0.3731,0.37307,0.37298,0.37285,0.3727,0.37255,0.37243,0.37229,0.37208,0.37181,0.37152,0.37122,0.37094,0.37071,0.37054,0.37046,0.37048,0.3706,0.37078,0.371,0.37125,0.37151,0.37175,0.37195,0.37209,0.37218,0.37224,0.37228,0.37231,0.37233,0.37235,0.37237,0.3724,0.37245,0.3725,0.37254,0.37258,0.37262,0.37266,0.3727,0.37276,0.37284,0.37293,0.37305,0.37319,0.37334,0.3735,0.37367,0.37385,0.37402,0.3742,0.37436,0.37451,0.37465,0.37478,0.37491,0.37504,0.37518,0.37532,0.37548,0.37566,0.37573,0.37561,0.37537,0.37509,0.37483,0.37467,0.37468,0.37493,0.37548,0.37602,0.3763,0.37659,0.37713,0.37816,0.37994,0.38256,0.38583,0.38953,0.39343,0.39734,0.40103,0.40492,0.40946,0.41447,0.41977,0.42516,0.43048,0.43555,0.44017,0.44417,0.4477,0.451,0.45407,0.45691,0.4595,0.46184,0.46393,0.46575,0.4673,0.46855,0.46951,0.47022,0.47071,0.47103,0.47121,0.47129,0.4713,0.4713,0.47116,0.47077,0.47019,0.46946,0.46864,0.46777,0.46691,0.46611,0.46541,0.46473,0.46395,0.46309,0.4622,0.46129,0.4604,0.45955,0.45878,0.45811,0.45753,0.45702,0.45656,0.45614,0.45574,0.45536,0.45496,0.45455,0.45411,0.45364,0.45316,0.45266,0.45216,0.45165,0.45114,0.45062,0.4501,0.44958,0.44906,0.44852,0.44798,0.44745,0.44693,0.44644,0.44598,0.44557,0.44521,0.44488,0.44455,0.44422,0.44391,0.44361,0.44333,0.44308,0.44287,0.44269,0.44257,0.44252,0.44253,0.44258,0.44265,0.44273,0.4428,0.44285,0.44285,0.44285,0.44287,0.44292,0.44297,0.44302,0.44305,0.44306,0.44304,0.44298,0.44284,0.44263,0.44238,0.4421,0.44182,0.44156,0.44136,0.44124,0.44121,0.44133,0.4416,0.44197,0.4424,0.44284,0.44324,0.44355,0.44374,0.44375,0.4436,0.44337,0.44307,0.44268,0.44223,0.44172,0.44116,0.44055,0.4399,0.43917,0.43833,0.43742,0.43645,0.43547,0.4345,0.43356,0.43268,0.4319,0.43115,0.43036,0.42957,0.42878,0.42803,0.42734,0.42681,0.42645,0.42618,0.42589,0.42549,0.42489,0.42422,0.42368,0.42318,0.42266,0.42204,0.42125,0.42022,0.41887,0.41715,0.41489,0.41211,0.40893,0.40548,0.40191,0.39835,0.39492,0.39177,0.38903,0.38648,0.38385,0.3812,0.37862,0.37617,0.37391,0.37192,0.37026,0.369,0.36822,0.36789,0.36791,0.36821,0.36869,0.36927,0.36986,0.37039,0.37075,0.37109,0.37156,0.37214,0.37278,0.37343,0.37406,0.37463,0.37509,0.37541,0.37563,0.37579,0.37592,0.37601,0.37607,0.37609,0.37609,0.37606,0.37601,0.37591,0.37573,0.37549,0.3752,0.37489,0.37457,0.37427,0.374,0.37379,0.37357,0.37333,0.37308,0.37285,0.37268,0.37259,0.37259,0.37264,0.37272,0.37283,0.37293,0.37301,0.37311,0.37328,0.3735,0.37374,0.37398,0.3742,0.37439,0.37451,0.37455,0.37448,0.37433,0.3741,0.37384,0.37355,0.37326,0.37299,0.37277,0.37262,0.37254,0.3725,0.37249,0.3725,0.37252,0.37255,0.37258,0.37259,0.3726,0.37261,0.37263,0.37265,0.37267,0.37269,0.3727,0.37271,0.37271,0.37269,0.37267,0.37265,0.37262,0.37259,0.37257,0.37255,0.37254,0.37254,0.37257,0.37263,0.37272,0.37282,0.37292,0.373,0.37306,0.37309,0.37306,0.37297,0.3728,0.37258,0.37233,0.37207,0.37182,0.37161,0.37145,0.37136,0.37136,0.37141,0.3715,0.37161,0.3717,0.37177,0.37183,0.37192,0.37203,0.37214,0.37226,0.37235,0.37245,0.37254,0.37264,0.37274,0.37283,0.37292,0.373,0.37306,0.37311,0.37315,0.3732,0.37325,0.37329,0.37333,0.37337,0.37339,0.3734,0.37339,0.37335,0.37326,0.37314,0.37299,0.37285,0.37271,0.37259,0.37251,0.37247,0.37249,0.37253,0.3726,0.37269,0.3728,0.37293,0.37307,0.37322,0.37338,0.37356,0.37376,0.37399,0.37422,0.37446,0.37471,0.37495,0.37518,0.37539,0.3756,0.37582,0.37604,0.37625,0.37647,0.37667,0.37686,0.37704,0.37719,0.3772,0.377,0.37666,0.37627,0.37589,0.37561,0.3755,0.37564,0.3761,0.37665,0.3771,0.37755,0.37811,0.37889,0.37999,0.38154,0.38363,0.38638,0.39002,0.39458,0.39984,0.40559,0.41161,0.41769,0.42362,0.42918,0.43417,0.43899,0.44412,0.4494,0.45467,0.45978,0.46457,0.46888,0.47256,0.47544,0.47753,0.479,0.47993,0.48043,0.48059,0.48052,0.4803,0.48004,0.47984,0.47947,0.47872,0.47768,0.47641,0.47502,0.47358,0.47216,0.47087,0.46977,0.4687,0.46748,0.46616,0.4648,0.46347,0.46222,0.46112,0.46023,0.4596,0.45928,0.45922,0.45936,0.45963,0.45999,0.46036,0.46069,0.46093,0.461,0.46096,0.46089,0.46079,0.46066,0.46051,0.46034,0.46013,0.4599,0.45965,0.45928,0.45876,0.45817,0.45758,0.45708,0.45673,0.45656,0.4565,0.4565,0.45653,0.45656,0.45653,0.45648,0.45646,0.45646,0.45647,0.45648,0.45647,0.45644,0.45637,0.45625,0.45608,0.45586,0.4556,0.45531,0.45501,0.45471,0.45442,0.45415,0.45392,0.4537,0.45349,0.45329,0.45309,0.4529,0.45272,0.45256,0.45242,0.4523,0.45219,0.45209,0.452,0.45192,0.45184,0.45176,0.45169,0.45163,0.45157,0.45155,0.4516,0.45171,0.45183,0.45196,0.45207,0.45213,0.45213,0.45204,0.45184,0.45155,0.45119,0.45077,0.45033,0.44987,0.44942,0.44899,0.44862,0.44828,0.44795,0.44763,0.44733,0.44705,0.44679,0.44656,0.44636,0.4462,0.44634,0.44692,0.44768,0.44837,0.44874,0.44855,0.44817,0.44801,0.44785,0.44746,0.44665,0.4452,0.443,0.44017,0.43684,0.43313,0.42918,0.42509,0.42101,0.41705,0.41335,0.40956,0.40538,0.40094,0.3964,0.3919,0.38759,0.38361,0.38011,0.37725,0.37494,0.373,0.37138,0.37006,0.369,0.36817,0.36754,0.36707,0.36673,0.36669,0.36705,0.36773,0.36863,0.36967,0.37076,0.3718,0.37271,0.37339,0.37397,0.37459,0.37525,0.37592,0.37656,0.37716,0.3777,0.37815,0.37849,0.37875,0.37897,0.37915,0.37929,0.37937,0.3794,0.37936,0.37926,0.37908,0.37875,0.37825,0.37763,0.37692,0.37619,0.37547,0.37482,0.37429,0.37391,0.37363,0.37335,0.37309,0.37286,0.37268,0.37257,0.37262,0.37286,0.3732,0.37356,0.37388,0.37407,0.37418,0.37432,0.37446,0.37461,0.37473,0.37483,0.37487,0.37486,0.37476,0.37457,0.37428,0.37393,0.37355,0.37316,0.37279,0.37248,0.37225,0.37208,0.37191,0.37176,0.37162,0.37151,0.37142,0.37136,0.37133,0.37134,0.37141,0.37158,0.37181,0.37207,0.37234,0.3726,0.37282,0.37297,0.37303,0.37301,0.37293,0.37281,0.37266,0.37248,0.37229,0.37209,0.37189,0.3717,0.3715,0.37124,0.37095,0.37065,0.37035,0.37006,0.36982,0.36963,0.36951,0.36946,0.36945,0.36949,0.36955,0.36964,0.36975,0.36986,0.36997,0.37008,0.3702,0.37034,0.37049,0.37066,0.37083,0.371,0.3712,0.37145,0.37173,0.372,0.37224,0.3724,0.37251,0.37261,0.37269,0.37275,0.3728,0.37284,0.37286,0.37288,0.37287,0.37284,0.37274,0.37261,0.37245,0.37228,0.37212,0.37198,0.37187,0.37182,0.3718,0.37181,0.37183,0.37187,0.37193,0.372,0.37208,0.37219,0.3723,0.37243,0.37259,0.37277,0.37297,0.37318,0.3734,0.37363,0.37386,0.37409,0.37433,0.37459,0.37486,0.37513,0.3754,0.37566,0.3759,0.37612,0.3763,0.37627,0.37594,0.37542,0.37481,0.37424,0.37381,0.37364,0.37383,0.3745,0.37556,0.37685,0.37838,0.38014,0.38214,0.38439,0.38689,0.38965,0.39265,0.39637,0.40099,0.40609,0.41127,0.41613,0.42025,0.42411,0.42832,0.43264,0.43686,0.44075,0.44409,0.44693,0.44948,0.45176,0.45381,0.45565,0.45731,0.45882,0.46021,0.4615,0.46265,0.46362,0.46442,0.46507,0.4656,0.46603,0.46638,0.46666,0.46692,0.46705,0.46697,0.46674,0.46638,0.46594,0.46544,0.46494,0.46446,0.46405,0.46366,0.46323,0.46277,0.46229,0.46179,0.46128,0.46076,0.46026,0.45976,0.45924,0.45867,0.45807,0.45745,0.45683,0.45622,0.45565,0.45513,0.45468,0.45431,0.454,0.45376,0.45356,0.45339,0.45324,0.45311,0.45298,0.45283,0.45267,0.45251,0.45234,0.45218,0.45202,0.45186,0.4517,0.45155,0.4514,0.45129,0.45123,0.4512,0.45117,0.45112,0.45102,0.4508,0.45047,0.45009,0.44972,0.44943,0.44929,0.44929,0.44936,0.44949,0.44967,0.44988,0.45011,0.45034,0.45056,0.45074,0.45097,0.45127,0.45163,0.452,0.45235,0.45266,0.45289,0.45299,0.45295,0.4527,0.45223,0.4516,0.45087,0.45009,0.44932,0.44862,0.44805,0.44765,0.44742,0.44731,0.44729,0.44734,0.44745,0.44758,0.44771,0.44783,0.4479,0.44798,0.44812,0.44828,0.44844,0.44859,0.44869,0.44873,0.44868,0.44851,0.4482,0.44776,0.44723,0.44664,0.44604,0.44544,0.4449,0.44445,0.44412,0.44401,0.44412,0.44439,0.44475,0.44511,0.44541,0.44557,0.44552,0.44518,0.44466,0.44407,0.44338,0.44258,0.44162,0.44049,0.43913,0.43753,0.43575,0.43384,0.43185,0.42985,0.42775,0.42547,0.42303,0.42046,0.41778,0.41502,0.41221,0.40937,0.40653,0.40344,0.39994,0.39618,0.39231,0.38848,0.38485,0.38156,0.37877,0.37663,0.37509,0.37398,0.37324,0.37278,0.37256,0.37249,0.37251,0.37256,0.37257,0.37273,0.37324,0.374,0.37491,0.3759,0.37685,0.37769,0.37831,0.37863,0.37866,0.37853,0.37827,0.37793,0.37753,0.37713,0.37677,0.37647,0.3763,0.37619,0.37607,0.37595,0.37583,0.37572,0.37562,0.37553,0.37546,0.37541,0.3754,0.37543,0.37549,0.37557,0.37567,0.37576,0.37585,0.37592,0.37597,0.376,0.37602,0.37603,0.37604,0.37603,0.37602,0.37599,0.37595,0.3759,0.37583,0.37576,0.37568,0.37559,0.37549,0.37538,0.37526,0.37513,0.37498,0.37479,0.37457,0.37434,0.37411,0.37388,0.37367,0.37348,0.37332,0.37317,0.37301,0.37283,0.37267,0.37251,0.37239,0.3723,0.37225,0.37227,0.37238,0.3726,0.37289,0.37323,0.37358,0.37392,0.37421,0.37443,0.37453,0.37453,0.37445,0.37432,0.37414,0.37393,0.37373,0.37354,0.37338,0.37327,0.3732,0.37311,0.37303,0.37295,0.37288,0.37283,0.37279,0.37277,0.37278,0.37283,0.37291,0.37301,0.37314,0.37327,0.37342,0.37355,0.37368,0.37378,0.37385,0.37387,0.37388,0.37389,0.37393,0.37401,0.37416,0.37438,0.37463,0.37488,0.37509,0.37524,0.37534,0.37543,0.37551,0.37558,0.37564,0.37569,0.37572,0.37575,0.37577,0.37575,0.3757,0.37562,0.37552,0.37542,0.37531,0.37523,0.37516,0.37514,0.37513,0.37513,0.37514,0.37515,0.37518,0.37522,0.37528,0.37537,0.37548,0.37563,0.3758,0.37601,0.37623,0.37647,0.37672,0.37697,0.37723,0.37747,0.37773,0.37801,0.37831,0.37863,0.37894,0.37924,0.37952,0.37978,0.37999,0.38003,0.37982,0.37944,0.379,0.3786,0.37832,0.37827,0.37854,0.37922,0.38015,0.38115,0.38226,0.38353,0.38501,0.38675,0.38879,0.3912,0.39401,0.39746,0.40159,0.40617,0.41094,0.41567,0.42011,0.42494,0.43067,0.43682,0.44291,0.44846,0.453,0.45689,0.46075,0.46449,0.46805,0.47133,0.47426,0.47676,0.47874,0.48012,0.48069,0.48041,0.47946,0.47803,0.4763,0.47445,0.47266,0.47112,0.47001,0.46912,0.46814,0.46712,0.46608,0.46507,0.46413,0.46331,0.46263,0.46213,0.46181,0.4616,0.46149,0.46147,0.4615,0.46159,0.4617,0.46183,0.46195,0.46215,0.46247,0.46289,0.46335,0.46383,0.46427,0.46465,0.46491,0.46501,0.465,0.46492,0.46479,0.46462,0.46441,0.46416,0.4639,0.46361,0.46332,0.46296,0.4625,0.46195,0.46136,0.46076,0.46019,0.45966,0.45923,0.45891,0.45877,0.45879,0.4589,0.45904,0.45911,0.45907,0.459,0.459,0.45903,0.45904,0.45899,0.45885,0.45857,0.45817,0.45769,0.45714,0.45656,0.45596,0.45538,0.45483,0.45436,0.4539,0.45341,0.45291,0.45241,0.45195,0.45152,0.45115,0.45087,0.45067,0.45063,0.45074,0.45097,0.45128,0.45162,0.45197,0.45228,0.4525,0.4526,0.45263,0.45264,0.45264,0.45263,0.4526,0.45256,0.4525,0.45242,0.45232,0.45216,0.45189,0.45156,0.45118,0.4508,0.45044,0.45013,0.4499,0.44978,0.44984,0.45008,0.45045,0.45088,0.45132,0.45171,0.452,0.45213,0.45204,0.45189,0.45183,0.4518,0.45172,0.45154,0.45119,0.45061,0.44972,0.44847,0.44678,0.44466,0.44219,0.43946,0.43655,0.43353,0.43049,0.4275,0.42465,0.4218,0.41881,0.4157,0.41251,0.40927,0.40602,0.40279,0.39961,0.39653,0.39336,0.38995,0.38642,0.38287,0.3794,0.37613,0.37315,0.37056,0.36848,0.36682,0.3654,0.36422,0.36327,0.36254,0.36204,0.36174,0.36165,0.36176,0.36232,0.36351,0.36516,0.36711,0.3692,0.37128,0.37319,0.37476,0.37583,0.37649,0.37692,0.37717,0.37728,0.37728,0.37722,0.37712,0.37703,0.37699,0.37694,0.37681,0.37662,0.37639,0.37615,0.37589,0.37566,0.37546,0.37532,0.37522,0.37514,0.37508,0.37503,0.37498,0.37493,0.37488,0.37482,0.37474,0.37466,0.3746,0.37454,0.37447,0.37439,0.3743,0.37414,0.37391,0.37366,0.37342,0.37322,0.3731,0.37304,0.37301,0.37301,0.37301,0.37303,0.37307,0.37311,0.37315,0.3732,0.37328,0.37339,0.37354,0.3737,0.37386,0.37401,0.37415,0.37425,0.3743,0.3743,0.37428,0.37423,0.37416,0.37408,0.37399,0.3739,0.37381,0.37374,0.37366,0.37357,0.37347,0.37337,0.37326,0.37315,0.37305,0.37295,0.37287,0.37277,0.37264,0.37249,0.37234,0.3722,0.3721,0.37205,0.37206,0.37216,0.37237,0.37269,0.37309,0.37355,0.37403,0.3745,0.37492,0.37528,0.37553,0.3757,0.37583,0.37593,0.376,0.37603,0.37603,0.376,0.37593,0.37582,0.3756,0.37523,0.37479,0.37434,0.37398,0.37376,0.37366,0.37359,0.37354,0.37352,0.37351,0.37351,0.37355,0.37363,0.37376,0.37391,0.37408,0.37425,0.37441,0.37454,0.37465,0.37471,0.37473,0.37474,0.37474,0.37474,0.37475,0.37479,0.37486,0.37498,0.37515,0.37537,0.37562,0.3759,0.37619,0.37649,0.37677,0.37704,0.37727,0.37744,0.37753,0.37756,0.37758,0.3776,0.37767,0.37781,0.37806,0.37844,0.37888,0.37932,0.37978,0.38028,0.38084,0.38148,0.38222,0.3831,0.38411,0.38509,0.38591,0.38667,0.38749,0.38849,0.38978,0.39147,0.39368,0.39651,0.40013,0.4045,0.40946,0.41484,0.42048,0.42621,0.43188,0.43733,0.44238,0.44789,0.45443,0.46139,0.46818,0.47418,0.4788,0.48245,0.48588,0.48897,0.49163,0.49373,0.49515,0.49563,0.4951,0.49377,0.49185,0.48957,0.48713,0.48475,0.48264,0.48101,0.47958,0.47794,0.47616,0.47429,0.47238,0.47052,0.46874,0.46711,0.4657,0.46444,0.46327,0.46217,0.46115,0.46021,0.45936,0.45858,0.45789,0.45729,0.45681,0.45646,0.45622,0.45606,0.45596,0.45589,0.45582,0.45574,0.45562,0.4555,0.45542,0.45537,0.45534,0.4553,0.45524,0.45514,0.455,0.45478,0.45448,0.4541,0.45365,0.45317,0.45267,0.45217,0.45169,0.45126,0.4509,0.45062,0.45039,0.45021,0.45006,0.44994,0.44981,0.44968,0.44952,0.44933,0.4491,0.44886,0.44861,0.44835,0.4481,0.44784,0.4476,0.44737,0.44715,0.44695,0.44676,0.44657,0.44638,0.44618,0.44597,0.44574,0.44549,0.44522,0.44492,0.44459,0.44424,0.44389,0.44354,0.44321,0.44291,0.44264,0.44241,0.44223,0.44206,0.44191,0.44179,0.4417,0.44164,0.44161,0.44163,0.44168,0.44178,0.44194,0.44213,0.44235,0.44259,0.44282,0.44303,0.44322,0.44336,0.44348,0.44361,0.44374,0.44386,0.44397,0.44405,0.44411,0.44414,0.44412,0.44408,0.44403,0.44397,0.44389,0.44378,0.44366,0.4435,0.44332,0.44309,0.44289,0.44275,0.44264,0.44252,0.44235,0.44211,0.44175,0.44124,0.44055,0.43972,0.4388,0.43779,0.43668,0.43545,0.4341,0.43264,0.43108,0.4294,0.4276,0.42567,0.42359,0.42125,0.41862,0.41575,0.41272,0.40958,0.40642,0.40328,0.40025,0.39738,0.39443,0.39121,0.38782,0.38441,0.38109,0.37799,0.37524,0.37296,0.37128,0.37025,0.36977,0.36973,0.37004,0.37058,0.37125,0.37195,0.37257,0.373,0.37343,0.37408,0.37487,0.37574,0.37663,0.37745,0.37815,0.37866,0.37891,0.3789,0.37871,0.37838,0.37795,0.37748,0.37699,0.37654,0.37616,0.3759,0.37571,0.37554,0.37538,0.37523,0.37508,0.37494,0.37481,0.37468,0.37456,0.37445,0.37436,0.37427,0.3742,0.37413,0.37408,0.37404,0.37402,0.374,0.37397,0.37391,0.37384,0.37378,0.37375,0.37375,0.37383,0.37398,0.37415,0.37432,0.37444,0.37455,0.37469,0.37486,0.37503,0.37521,0.37538,0.37553,0.37564,0.37571,0.37574,0.37574,0.37571,0.37566,0.37559,0.37552,0.37544,0.37536,0.37528,0.3752,0.37508,0.37495,0.37481,0.37466,0.37451,0.37437,0.37425,0.37416,0.37407,0.37396,0.37386,0.37376,0.37368,0.37362,0.37361,0.37364,0.37373,0.37392,0.37423,0.37463,0.37507,0.37552,0.37596,0.37635,0.37666,0.37685,0.37694,0.37697,0.37694,0.37688,0.37677,0.37663,0.37646,0.37626,0.37606,0.37578,0.37539,0.37493,0.37442,0.37391,0.37343,0.37301,0.37268,0.37247,0.37239,0.37238,0.37242,0.3725,0.3726,0.3727,0.37288,0.37321,0.37361,0.37401,0.37437,0.3746,0.37473,0.37483,0.37491,0.37497,0.37501,0.37504,0.37507,0.37509,0.37511,0.37512,0.37508,0.37502,0.37495,0.37488,0.37481,0.37477,0.37476,0.37479,0.37486,0.37493,0.37501,0.37512,0.37524,0.37539,0.37557,0.37578,0.37603,0.3762,0.37624,0.3762,0.37614,0.37612,0.3762,0.37645,0.37692,0.37769,0.37857,0.37941,0.38029,0.38129,0.38247,0.38393,0.38573,0.38795,0.39067,0.39409,0.39827,0.40303,0.40821,0.41362,0.41911,0.4245,0.42962,0.43431,0.43897,0.44401,0.44924,0.45451,0.45964,0.46445,0.46878,0.47245,0.47528,0.47728,0.47866,0.47957,0.48012,0.48048,0.48078,0.48052,0.47936,0.47765,0.47575,0.47404,0.47287,0.47196,0.47085,0.46961,0.46828,0.46695,0.46567,0.46451,0.46353,0.4628,0.46232,0.46203,0.46188,0.46186,0.4619,0.46199,0.46207,0.46211,0.46208,0.46202,0.46201,0.46202,0.46204,0.46205,0.46203,0.46196,0.46183,0.46161,0.46126,0.46075,0.46013,0.45945,0.45874,0.45805,0.45743,0.45691,0.45653,0.45631,0.45618,0.45614,0.45616,0.45623,0.45632,0.45642,0.45652,0.45658,0.45667,0.45682,0.45703,0.45726,0.45749,0.4577,0.45786,0.45795,0.45796,0.45789,0.45778,0.45763,0.45744,0.45722,0.45696,0.45666,0.45633,0.45596,0.45557,0.45516,0.45472,0.45425,0.45375,0.45322,0.45255,0.45171,0.45079,0.44986,0.44903,0.44838,0.44781,0.44722,0.44661,0.44601,0.44545,0.44496,0.44455,0.44425,0.44409,0.44412,0.44433,0.44468,0.44514,0.44567,0.44621,0.44673,0.44719,0.44755,0.44786,0.44819,0.44854,0.44888,0.4492,0.44948,0.44971,0.44987,0.44995,0.44992,0.44979,0.44958,0.44932,0.44903,0.44874,0.44847,0.44825,0.4481,0.44808,0.44819,0.44839,0.44864,0.44887,0.44904,0.44911,0.44903,0.44874,0.44828,0.44772,0.44706,0.4463,0.44546,0.44455,0.44355,0.44249,0.44137,0.44014,0.43876,0.43725,0.43566,0.43401,0.43232,0.43062,0.42895,0.42733,0.42586,0.42453,0.42324,0.42186,0.4203,0.41842,0.41634,0.41423,0.41205,0.40976,0.40736,0.40479,0.40184,0.39839,0.3946,0.39066,0.38672,0.38296,0.37955,0.37665,0.37443,0.37288,0.3718,0.37113,0.3708,0.37072,0.37083,0.37105,0.37131,0.37153,0.37191,0.37262,0.37356,0.37464,0.37577,0.37684,0.37777,0.37845,0.3788,0.37891,0.37896,0.37896,0.37891,0.37884,0.37875,0.37865,0.37856,0.37848,0.37841,0.37835,0.37828,0.37822,0.37816,0.3781,0.37804,0.37798,0.37792,0.37787,0.37782,0.37777,0.37774,0.3777,0.37766,0.37762,0.37759,0.37755,0.37752,0.37751,0.37752,0.37754,0.37755,0.37754,0.3775,0.37743,0.37732,0.37718,0.37703,0.37686,0.37669,0.37652,0.37631,0.37604,0.37573,0.37543,0.37515,0.37493,0.37474,0.37453,0.37431,0.37411,0.37391,0.37375,0.37363,0.37356,0.37356,0.37364,0.37381,0.37404,0.37431,0.37461,0.37489,0.37516,0.37537,0.37551,0.37561,0.37571,0.37581,0.3759,0.37598,0.37605,0.3761,0.37612,0.37612,0.37606,0.37594,0.37577,0.37557,0.37535,0.37514,0.37494,0.37477,0.37465,0.37456,0.37448,0.37441,0.37434,0.37429,0.37425,0.37423,0.37422,0.37423,0.37427,0.37433,0.37441,0.3745,0.37461,0.37472,0.37484,0.37495,0.37506,0.37519,0.37534,0.37551,0.37569,0.37588,0.37606,0.37624,0.37639,0.37652,0.37662,0.37668,0.37671,0.37673,0.37674,0.37674,0.37676,0.37679,0.37684,0.37691,0.37698,0.37705,0.37713,0.37721,0.37732,0.37744,0.37759,0.37777,0.37798,0.37823,0.37851,0.37881,0.37912,0.37943,0.37974,0.38004,0.38032,0.38056,0.38076,0.38094,0.38111,0.38128,0.38146,0.38167,0.38191,0.3822,0.38244,0.38257,0.38264,0.38271,0.38285,0.38311,0.38354,0.38422,0.38519,0.38633,0.38752,0.38881,0.39022,0.39181,0.39363,0.39571,0.3981,0.40085,0.40413,0.408,0.41234,0.417,0.42185,0.42674,0.43156,0.43615,0.44038,0.44463,0.44926,0.45408,0.45894,0.46364,0.46801,0.47188,0.47508,0.47742,0.47879,0.47935,0.47936,0.47905,0.47869,0.4785,0.47795,0.47656,0.47467,0.47265,0.47086,0.46965,0.46887,0.46813,0.46742,0.46674,0.46608,0.46544,0.46482,0.46421,0.4636,0.46298,0.46232,0.46163,0.46093,0.46023,0.45954,0.45886,0.45822,0.45762,0.45701,0.45635,0.45568,0.455,0.45435,0.45375,0.45323,0.4528,0.45251,0.45238,0.4524,0.45255,0.45278,0.45306,0.45333,0.45358,0.45375,0.45381,0.4538,0.4538,0.45381,0.4538,0.45378,0.45373,0.45366,0.45355,0.4534,0.45317,0.45284,0.45244,0.45198,0.4515,0.45102,0.45056,0.45014,0.44979,0.44952,0.44931,0.44915,0.44902,0.44891,0.4488,0.44869,0.44854,0.44836,0.44813,0.44785,0.44756,0.44726,0.44698,0.44674,0.44649,0.44621,0.44591,0.44564,0.44541,0.44525,0.44517,0.44513,0.44513,0.44516,0.44522,0.44531,0.44541,0.44552,0.44563,0.44581,0.44607,0.4464,0.44674,0.44707,0.44735,0.44753,0.44758,0.44746,0.44714,0.44664,0.446,0.44527,0.44451,0.44375,0.44306,0.44247,0.44204,0.44179,0.44169,0.4417,0.44178,0.44188,0.44195,0.44197,0.44187,0.44163,0.44144,0.44147,0.44162,0.44175,0.44177,0.44156,0.441,0.43999,0.43841,0.43615,0.43326,0.42987,0.4261,0.42208,0.41793,0.41378,0.40975,0.40597,0.40197,0.39737,0.3924,0.38728,0.38227,0.37759,0.37348,0.37016,0.36789,0.36672,0.36638,0.36662,0.36716,0.36774,0.36811,0.36887,0.37056,0.37276,0.37506,0.37705,0.37832,0.37902,0.3796,0.38005,0.3804,0.38067,0.38086,0.381,0.38109,0.38115,0.38118,0.38117,0.38111,0.38102,0.38089,0.38072,0.38052,0.3803,0.38004,0.37969,0.37922,0.37865,0.37801,0.37735,0.37668,0.37606,0.37549,0.37503,0.37461,0.37417,0.37372,0.3733,0.37291,0.3726,0.37236,0.37224,0.37225,0.37245,0.37285,0.3734,0.37403,0.3747,0.37535,0.37592,0.37636,0.37663,0.37671,0.37669,0.37658,0.37641,0.37622,0.37602,0.37585,0.37572,0.37568,0.37569,0.3757,0.37572,0.37574,0.37577,0.37581,0.37586,0.37591,0.376,0.37614,0.37632,0.37652,0.37672,0.37691,0.37708,0.3772,0.37726,0.37729,0.37731,0.37732,0.37731,0.37729,0.37725,0.37718,0.37709,0.37697,0.37679,0.37653,0.3762,0.37584,0.37547,0.37511,0.37477,0.37449,0.37429,0.37413,0.37398,0.37384,0.37373,0.37365,0.3736,0.3736,0.37365,0.37375,0.37395,0.37425,0.37462,0.37505,0.37551,0.37596,0.37638,0.37675,0.37703,0.37725,0.37744,0.37761,0.37776,0.3779,0.37802,0.37813,0.37824,0.37835,0.37846,0.37856,0.37865,0.37872,0.37879,0.37883,0.37886,0.37887,0.37886,0.3788,0.3787,0.37855,0.37839,0.37821,0.37805,0.3779,0.3778,0.37775,0.37773,0.3777,0.37768,0.37767,0.37771,0.37779,0.37795,0.37821,0.37853,0.37885,0.37916,0.3794,0.37961,0.37986,0.38014,0.38042,0.38068,0.38092,0.38111,0.38124,0.38129,0.38128,0.38123,0.38115,0.38105,0.38094,0.38083,0.38072,0.38063,0.38055,0.38045,0.38029,0.3801,0.37988,0.37966,0.37947,0.37932,0.37923,0.37923,0.37913,0.37878,0.37828,0.37772,0.37721,0.37682,0.37665,0.3768,0.37735,0.37828,0.37949,0.38098,0.38276,0.38485,0.38725,0.38997,0.39302,0.3964,0.40052,0.40558,0.41133,0.4175,0.42384,0.43009,0.43599,0.44127,0.44568,0.44952,0.45326,0.45682,0.46016,0.46321,0.46592,0.46824,0.4701,0.47145,0.47198,0.47164,0.47075,0.46962,0.46857,0.4679,0.4672,0.46598,0.46449,0.46296,0.46163,0.46073,0.46015,0.45961,0.4591,0.45863,0.45819,0.45778,0.45739,0.45703,0.4567,0.45642,0.45624,0.45612,0.45604,0.45599,0.45592,0.45583,0.45569,0.45547,0.45517,0.4548,0.45439,0.45395,0.45349,0.45304,0.45261,0.45222,0.45187,0.45159,0.45136,0.45117,0.451,0.45086,0.45072,0.45058,0.45042,0.45023,0.45,0.44972,0.44941,0.44908,0.44874,0.44842,0.44812,0.44785,0.44764,0.44749,0.44738,0.4473,0.44725,0.44723,0.44722,0.44722,0.44723,0.44723,0.44723,0.44722,0.44722,0.44723,0.44726,0.44732,0.44742,0.44757,0.44777,0.44812,0.44864,0.44925,0.44983,0.45031,0.45058,0.45072,0.45084,0.45093,0.45099,0.451,0.45096,0.45085,0.45067,0.45041,0.45011,0.44975,0.44935,0.44891,0.44845,0.44797,0.44741,0.44672,0.44595,0.44514,0.44433,0.44359,0.44294,0.44243,0.44212,0.44202,0.44208,0.44228,0.44255,0.44285,0.44314,0.44337,0.44349,0.44346,0.44344,0.44358,0.44381,0.44406,0.44424,0.44428,0.44411,0.44365,0.44283,0.44167,0.44028,0.4387,0.43696,0.43512,0.43321,0.43127,0.42936,0.42751,0.42566,0.42371,0.42167,0.41952,0.41728,0.41493,0.41247,0.40991,0.40724,0.40402,0.40001,0.39548,0.3907,0.38596,0.38153,0.37768,0.37469,0.37283,0.37186,0.37127,0.371,0.37097,0.37111,0.37135,0.3716,0.3718,0.37187,0.37195,0.37221,0.37261,0.37311,0.37365,0.37419,0.37469,0.3751,0.37538,0.37556,0.37573,0.37586,0.37598,0.37606,0.37611,0.37612,0.3761,0.37603,0.3759,0.3757,0.37544,0.37514,0.37483,0.37453,0.37425,0.37402,0.37385,0.37374,0.37365,0.37358,0.37352,0.37348,0.37345,0.37342,0.3734,0.37338,0.37337,0.37338,0.37341,0.37344,0.37347,0.3735,0.37351,0.37351,0.37347,0.37342,0.37335,0.37328,0.3732,0.37311,0.37302,0.37294,0.37286,0.37278,0.37272,0.37265,0.37259,0.37254,0.37249,0.37245,0.37241,0.37238,0.37235],"name":"Smoothed GCC","showlegend":true,"type":"scatter","mode":"line","marker":{"color":"rgba(31,119,180,1)","line":{"color":"rgba(31,119,180,1)"}},"error_y":{"color":"rgba(31,119,180,1)"},"error_x":{"color":"rgba(31,119,180,1)"},"line":{"color":"rgba(31,119,180,1)"},"xaxis":"x","yaxis":"y","frame":null},{"x":["2008-04-05","2008-04-08","2008-04-11","2008-04-14","2008-04-17","2008-04-20","2008-04-23","2008-04-26","2008-04-29","2008-05-02","2008-05-05","2008-05-08","2008-05-11","2008-05-14","2008-05-17","2008-05-20","2008-05-23","2008-05-26","2008-05-29","2008-06-01","2008-06-04","2008-06-07","2008-06-10","2008-06-13","2008-06-16","2008-06-19","2008-06-22","2008-06-25","2008-06-28","2008-07-01","2008-07-04","2008-07-07","2008-07-10","2008-07-13","2008-07-16","2008-07-19","2008-07-22","2008-07-25","2008-07-28","2008-07-31","2008-08-03","2008-08-06","2008-08-09","2008-08-12","2008-08-15","2008-08-18","2008-08-21","2008-08-24","2008-08-27","2008-08-30","2008-09-02","2008-09-05","2008-09-08","2008-09-11","2008-09-14","2008-09-17","2008-09-20","2008-09-23","2008-09-26","2008-09-29","2008-10-02","2008-10-05","2008-10-08","2008-10-11","2008-10-14","2008-10-17","2008-10-20","2008-10-23","2008-10-26","2008-10-29","2008-11-01","2008-11-04","2008-11-07","2008-11-10","2008-11-13","2008-11-16","2008-11-19","2008-11-22","2008-11-25","2008-11-28","2008-12-01","2008-12-04","2008-12-07","2008-12-10","2008-12-16","2008-12-19","2008-12-22","2008-12-25","2008-12-28","2008-12-31","2009-01-02","2009-01-05","2009-01-08","2009-01-11","2009-01-14","2009-01-17","2009-01-20","2009-01-23","2009-01-26","2009-01-29","2009-02-01","2009-02-04","2009-02-07","2009-02-10","2009-02-13","2009-02-16","2009-02-19","2009-02-22","2009-02-25","2009-02-28","2009-03-03","2009-03-06","2009-03-09","2009-03-12","2009-03-15","2009-03-18","2009-03-21","2009-03-24","2009-03-27","2009-03-30","2009-04-02","2009-04-05","2009-04-08","2009-04-11","2009-04-14","2009-04-17","2009-04-20","2009-04-23","2009-04-26","2009-04-29","2009-05-02","2009-05-05","2009-05-08","2009-05-11","2009-05-14","2009-05-17","2009-05-20","2009-05-23","2009-05-26","2009-05-29","2009-06-01","2009-06-04","2009-06-07","2009-06-10","2009-06-13","2009-06-16","2009-06-19","2009-06-22","2009-06-25","2009-06-28","2009-07-01","2009-07-04","2009-07-07","2009-07-10","2009-07-13","2009-07-16","2009-07-19","2009-07-22","2009-07-25","2009-07-28","2009-07-31","2009-08-03","2009-08-06","2009-08-09","2009-08-12","2009-08-15","2009-08-18","2009-08-21","2009-08-24","2009-08-27","2009-08-30","2009-09-02","2009-09-05","2009-09-08","2009-09-11","2009-09-14","2009-09-17","2009-09-20","2009-09-23","2009-09-26","2009-09-29","2009-10-02","2009-10-05","2009-10-08","2009-10-11","2009-10-14","2009-10-17","2009-10-20","2009-10-23","2009-10-26","2009-10-29","2009-11-01","2009-11-04","2009-11-07","2009-11-10","2009-11-13","2009-11-16","2009-11-19","2009-11-22","2009-11-25","2009-11-28","2009-12-01","2009-12-04","2009-12-07","2009-12-10","2009-12-13","2009-12-16","2009-12-19","2009-12-22","2009-12-25","2009-12-28","2009-12-31","2010-01-02","2010-01-05","2010-01-08","2010-01-11","2010-01-14","2010-01-17","2010-01-20","2010-01-23","2010-01-26","2010-01-29","2010-02-01","2010-02-04","2010-02-07","2010-02-10","2010-02-13","2010-02-16","2010-02-19","2010-02-22","2010-02-25","2010-02-28","2010-03-03","2010-03-06","2010-03-09","2010-03-12","2010-03-15","2010-03-18","2010-03-21","2010-03-24","2010-03-27","2010-03-30","2010-04-02","2010-04-05","2010-04-08","2010-04-11","2010-04-14","2010-04-17","2010-04-20","2010-04-23","2010-04-26","2010-04-29","2010-05-02","2010-05-05","2010-05-11","2010-05-14","2010-05-17","2010-05-20","2010-05-23","2010-05-26","2010-05-29","2010-06-01","2010-06-04","2010-06-07","2010-06-10","2010-06-13","2010-06-16","2010-06-19","2010-06-22","2010-06-25","2010-06-28","2010-07-01","2010-07-04","2010-07-07","2010-07-10","2010-07-13","2010-07-16","2010-07-19","2010-07-22","2010-07-25","2010-07-28","2010-07-31","2010-08-03","2010-08-06","2010-08-09","2010-08-12","2010-08-15","2010-08-18","2010-08-21","2010-08-24","2010-08-27","2010-08-30","2010-09-02","2010-09-05","2010-09-08","2010-09-11","2010-09-14","2010-09-17","2010-09-20","2010-09-23","2010-09-26","2010-09-29","2010-10-02","2010-10-05","2010-10-08","2010-10-11","2010-10-14","2010-10-17","2010-10-20","2010-10-23","2010-10-26","2010-10-29","2010-11-01","2010-11-04","2010-11-07","2010-11-10","2010-11-13","2010-11-16","2010-11-19","2010-11-22","2010-11-25","2010-11-28","2010-12-01","2010-12-04","2010-12-07","2010-12-10","2010-12-13","2010-12-16","2010-12-19","2010-12-22","2010-12-25","2010-12-28","2010-12-31","2011-01-02","2011-01-05","2011-01-08","2011-01-11","2011-01-14","2011-01-17","2011-01-20","2011-01-23","2011-01-26","2011-01-29","2011-02-01","2011-02-04","2011-02-07","2011-02-10","2011-02-13","2011-02-16","2011-02-19","2011-02-22","2011-02-25","2011-02-28","2011-03-03","2011-03-06","2011-03-09","2011-03-12","2011-03-15","2011-03-18","2011-03-21","2011-03-24","2011-03-27","2011-03-30","2011-04-02","2011-04-05","2011-04-08","2011-04-11","2011-04-14","2011-04-17","2011-04-20","2011-04-23","2011-04-26","2011-04-29","2011-05-02","2011-05-05","2011-05-08","2011-05-11","2011-05-14","2011-05-17","2011-05-20","2011-05-23","2011-05-26","2011-05-29","2011-06-01","2011-06-04","2011-06-07","2011-06-10","2011-06-13","2011-06-16","2011-06-19","2011-06-22","2011-06-25","2011-06-28","2011-07-01","2011-07-04","2011-07-07","2011-07-10","2011-07-13","2011-07-16","2011-07-19","2011-07-22","2011-07-25","2011-07-28","2011-07-31","2011-08-03","2011-08-06","2011-08-09","2011-08-12","2011-08-15","2011-08-18","2011-08-21","2011-08-24","2011-08-27","2011-08-30","2011-09-02","2011-09-05","2011-09-08","2011-09-11","2011-09-14","2011-09-17","2011-09-20","2011-09-23","2011-09-26","2011-09-29","2011-10-02","2011-10-05","2011-10-08","2011-10-11","2011-10-14","2011-10-17","2011-10-20","2011-10-23","2011-10-26","2011-10-29","2011-11-01","2011-11-04","2011-11-07","2011-11-10","2011-11-13","2011-11-16","2011-11-19","2011-11-22","2011-11-25","2011-11-28","2011-12-01","2011-12-04","2011-12-07","2011-12-10","2011-12-13","2011-12-16","2011-12-19","2011-12-22","2011-12-25","2011-12-28","2011-12-31","2012-01-02","2012-01-05","2012-01-08","2012-01-11","2012-01-14","2012-01-17","2012-01-20","2012-01-23","2012-01-26","2012-01-29","2012-02-01","2012-02-04","2012-02-07","2012-02-10","2012-02-13","2012-02-16","2012-02-19","2012-02-22","2012-02-25","2012-02-28","2012-03-02","2012-03-05","2012-03-08","2012-03-11","2012-03-14","2012-03-17","2012-03-20","2012-03-23","2012-03-26","2012-03-29","2012-04-01","2012-04-04","2012-04-07","2012-04-10","2012-04-13","2012-04-16","2012-04-19","2012-04-22","2012-04-25","2012-04-28","2012-05-01","2012-05-04","2012-05-07","2012-05-10","2012-05-13","2012-05-16","2012-05-19","2012-05-22","2012-05-25","2012-05-28","2012-05-31","2012-06-03","2012-06-06","2012-06-09","2012-06-12","2012-06-15","2012-06-18","2012-06-21","2012-06-24","2012-06-27","2012-06-30","2012-07-03","2012-07-06","2012-07-09","2012-07-12","2012-07-15","2012-07-18","2012-07-21","2012-07-24","2012-07-27","2012-07-30","2012-08-02","2012-08-05","2012-08-08","2012-08-11","2012-08-14","2012-08-17","2012-08-20","2012-08-23","2012-08-26","2012-08-29","2012-09-01","2012-09-04","2012-09-07","2012-09-10","2012-09-13","2012-09-16","2012-09-19","2012-09-22","2012-09-25","2012-09-28","2012-10-01","2012-10-04","2012-10-07","2012-10-10","2012-10-13","2012-10-16","2012-10-19","2012-10-22","2012-10-25","2012-10-28","2012-10-31","2012-11-03","2012-11-06","2012-11-09","2012-11-12","2012-11-15","2012-11-18","2012-11-21","2012-11-24","2012-11-27","2012-11-30","2012-12-03","2012-12-06","2012-12-09","2012-12-12","2012-12-15","2012-12-18","2012-12-21","2012-12-24","2012-12-27","2012-12-30","2013-01-02","2013-01-05","2013-01-08","2013-01-11","2013-01-14","2013-01-17","2013-01-20","2013-01-23","2013-01-26","2013-01-29","2013-02-01","2013-02-04","2013-02-07","2013-02-10","2013-02-13","2013-02-16","2013-02-19","2013-02-22","2013-02-25","2013-02-28","2013-03-03","2013-03-06","2013-03-09","2013-03-12","2013-03-15","2013-03-18","2013-03-21","2013-03-24","2013-03-27","2013-03-30","2013-04-02","2013-04-05","2013-04-08","2013-04-11","2013-04-14","2013-04-17","2013-04-20","2013-04-23","2013-04-26","2013-04-29","2013-05-02","2013-05-05","2013-05-08","2013-05-11","2013-05-14","2013-05-17","2013-05-20","2013-05-23","2013-05-26","2013-05-29","2013-06-01","2013-06-04","2013-06-07","2013-06-10","2013-06-13","2013-06-16","2013-06-19","2013-06-22","2013-06-25","2013-06-28","2013-07-01","2013-07-04","2013-07-07","2013-07-10","2013-07-13","2013-07-16","2013-07-19","2013-07-22","2013-07-25","2013-07-28","2013-07-31","2013-08-03","2013-08-06","2013-08-09","2013-08-12","2013-08-15","2013-08-18","2013-08-21","2013-08-24","2013-08-27","2013-08-30","2013-09-02","2013-09-05","2013-09-08","2013-09-11","2013-09-14","2013-09-17","2013-09-20","2013-09-23","2013-09-26","2013-09-29","2013-10-02","2013-10-05","2013-10-08","2013-10-11","2013-10-14","2013-10-17","2013-10-20","2013-10-23","2013-10-26","2013-10-29","2013-11-01","2013-11-04","2013-11-07","2013-11-10","2013-11-13","2013-11-16","2013-11-19","2013-11-22","2013-11-25","2013-11-28","2013-12-01","2013-12-04","2013-12-07","2013-12-10","2013-12-13","2013-12-16","2013-12-19","2013-12-22","2013-12-25","2013-12-28","2013-12-31","2014-01-02","2014-01-05","2014-01-08","2014-01-11","2014-01-14","2014-01-17","2014-01-20","2014-01-23","2014-01-26","2014-01-29","2014-02-01","2014-02-04","2014-02-07","2014-02-10","2014-02-13","2014-02-16","2014-02-19","2014-02-22","2014-02-25","2014-02-28","2014-03-03","2014-03-06","2014-03-09","2014-03-12","2014-03-15","2014-03-18","2014-03-21","2014-03-24","2014-03-27","2014-03-30","2014-04-02","2014-04-05","2014-04-08","2014-04-11","2014-04-14","2014-04-17","2014-04-20","2014-04-23","2014-04-26","2014-04-29","2014-05-02","2014-05-05","2014-05-08","2014-05-11","2014-05-14","2014-05-17","2014-05-20","2014-05-23","2014-05-26","2014-05-29","2014-06-01","2014-06-04","2014-06-07","2014-06-10","2014-06-13","2014-06-16","2014-06-19","2014-06-22","2014-06-25","2014-06-28","2014-07-01","2014-07-04","2014-07-07","2014-07-10","2014-07-13","2014-07-16","2014-07-19","2014-07-22","2014-07-25","2014-07-28","2014-07-31","2014-08-03","2014-08-06","2014-08-09","2014-08-12","2014-08-15","2014-08-18","2014-08-21","2014-08-24","2014-08-27","2014-08-30","2014-09-02","2014-09-05","2014-09-08","2014-09-11","2014-09-14","2014-09-17","2014-09-20","2014-09-23","2014-09-26","2014-09-29","2014-10-02","2014-10-05","2014-10-08","2014-10-11","2014-10-14","2014-10-17","2014-10-20","2014-10-23","2014-10-26","2014-10-29","2014-11-01","2014-11-04","2014-11-07","2014-11-10","2014-11-13","2014-11-16","2014-11-19","2014-11-22","2014-11-25","2014-12-01","2014-12-04","2014-12-07","2014-12-10","2014-12-13","2014-12-16","2014-12-19","2014-12-22","2014-12-25","2014-12-28","2014-12-31","2015-01-02","2015-01-05","2015-01-08","2015-01-11","2015-01-14","2015-01-17","2015-01-20","2015-01-23","2015-01-26","2015-01-29","2015-02-01","2015-02-04","2015-02-07","2015-02-10","2015-02-13","2015-02-16","2015-02-19","2015-02-22","2015-02-25","2015-02-28","2015-03-03","2015-03-06","2015-03-09","2015-03-12","2015-03-15","2015-03-18","2015-03-21","2015-03-24","2015-03-27","2015-03-30","2015-04-02","2015-04-05","2015-04-08","2015-04-11","2015-04-14","2015-04-17","2015-04-20","2015-04-23","2015-04-26","2015-04-29","2015-05-02","2015-05-05","2015-05-08","2015-05-11","2015-05-14","2015-05-17","2015-05-20","2015-05-23","2015-05-26","2015-05-29","2015-06-01","2015-06-04","2015-06-07","2015-06-10","2015-06-13","2015-06-16","2015-06-19","2015-06-22","2015-06-25","2015-06-28","2015-07-01","2015-07-04","2015-07-07","2015-07-10","2015-07-13","2015-07-16","2015-07-19","2015-07-22","2015-07-25","2015-07-28","2015-07-31","2015-08-03","2015-08-06","2015-08-09","2015-08-12","2015-08-15","2015-08-18","2015-08-21","2015-08-24","2015-08-27","2015-08-30","2015-09-02","2015-09-05","2015-09-08","2015-09-11","2015-09-14","2015-09-17","2015-09-20","2015-09-23","2015-09-26","2015-09-29","2015-10-02","2015-10-05","2015-10-08","2015-10-11","2015-10-14","2015-10-17","2015-10-20","2015-10-23","2015-10-26","2015-10-29","2015-11-01","2015-11-04","2015-11-07","2015-11-10","2015-11-13","2015-11-16","2015-11-19","2015-11-22","2015-11-25","2015-11-28","2015-12-01","2015-12-04","2015-12-07","2015-12-10","2015-12-13","2015-12-16","2015-12-19","2015-12-22","2015-12-25","2015-12-28","2015-12-31","2016-01-02","2016-01-05","2016-01-08","2016-01-11","2016-01-14","2016-01-17","2016-01-20","2016-01-23","2016-01-26","2016-01-29","2016-02-01","2016-02-04","2016-02-07","2016-02-10","2016-02-13","2016-02-16","2016-02-19","2016-02-22","2016-02-25","2016-02-28","2016-03-02","2016-03-05","2016-03-08","2016-03-11","2016-03-14","2016-03-17","2016-03-20","2016-03-23","2016-03-26","2016-03-29","2016-04-01","2016-04-04","2016-04-07","2016-04-10","2016-04-13","2016-04-16","2016-04-19","2016-04-22","2016-04-25","2016-04-28","2016-05-01","2016-05-04","2016-05-07","2016-05-10","2016-05-13","2016-05-16","2016-05-19","2016-05-22","2016-05-25","2016-05-28","2016-05-31","2016-06-03","2016-06-06","2016-06-09","2016-06-12","2016-06-15","2016-06-18","2016-06-21","2016-06-24","2016-06-27","2016-06-30","2016-07-03","2016-07-06","2016-07-09","2016-07-12","2016-07-15","2016-07-18","2016-07-21","2016-07-24","2016-07-27","2016-07-30","2016-08-02","2016-08-05","2016-08-08","2016-08-11","2016-08-14","2016-08-17","2016-08-20","2016-08-23","2016-08-26","2016-08-29","2016-09-01","2016-09-04","2016-09-07","2016-09-10","2016-09-13","2016-09-16","2016-09-19","2016-09-22","2016-09-25","2016-09-28","2016-10-01","2016-10-04","2016-10-07","2016-10-10","2016-10-13","2016-10-16","2016-10-19","2016-10-22","2016-10-25","2016-10-28","2016-10-31","2016-11-03","2016-11-06","2016-11-09","2016-11-12","2016-11-15","2016-11-18","2016-11-21","2016-11-24","2016-11-27","2016-11-30","2016-12-03","2016-12-06","2016-12-09","2016-12-12","2016-12-15","2016-12-18","2016-12-21","2016-12-24","2016-12-27","2016-12-30","2017-01-02","2017-01-05","2017-01-08","2017-01-11","2017-01-14","2017-01-17","2017-01-20","2017-01-23","2017-01-26","2017-01-29","2017-02-01","2017-02-04","2017-02-07","2017-02-10","2017-02-13","2017-02-16","2017-02-19","2017-02-22","2017-02-25","2017-02-28","2017-03-03","2017-03-06","2017-03-09","2017-03-12","2017-03-15","2017-03-18","2017-03-21","2017-03-24","2017-03-27","2017-03-30","2017-04-02","2017-04-05","2017-04-08","2017-04-11","2017-04-14","2017-04-17","2017-04-20","2017-04-23","2017-04-26","2017-04-29","2017-05-02","2017-05-05","2017-05-08","2017-05-11","2017-05-14","2017-05-17","2017-05-20","2017-05-23","2017-05-26","2017-05-29","2017-06-01","2017-06-04","2017-06-07","2017-06-10","2017-06-13","2017-06-16","2017-06-19","2017-06-22","2017-06-25","2017-06-28","2017-07-01","2017-07-04","2017-07-07","2017-07-10","2017-07-13","2017-07-16","2017-07-19","2017-07-22","2017-07-25","2017-07-28","2017-07-31","2017-08-03","2017-08-06","2017-08-09","2017-08-12","2017-08-15","2017-08-18","2017-08-21","2017-08-24","2017-08-27","2017-08-30","2017-09-02","2017-09-05","2017-09-08","2017-09-11","2017-09-14","2017-09-17","2017-09-20","2017-09-23","2017-09-26","2017-09-29","2017-10-02","2017-10-05","2017-10-08","2017-10-11","2017-10-14","2017-10-17","2017-10-20","2017-10-23","2017-10-26","2017-10-29","2017-11-01","2017-11-04","2017-11-07","2017-11-10","2017-11-13","2017-11-16","2017-11-19","2017-11-22","2017-11-25","2017-11-28","2017-12-01","2017-12-04","2017-12-07","2017-12-10","2017-12-13","2017-12-16","2017-12-19","2017-12-22","2017-12-25","2017-12-28","2017-12-31","2018-01-02","2018-01-05","2018-01-08","2018-01-11","2018-01-14","2018-01-17","2018-01-20","2018-01-23","2018-01-26","2018-01-29","2018-02-01","2018-02-04","2018-02-07","2018-02-10","2018-02-13","2018-02-16","2018-02-19","2018-02-22","2018-02-25","2018-02-28","2018-03-03","2018-03-06","2018-03-09","2018-03-12","2018-03-15","2018-03-18","2018-03-21","2018-03-24","2018-03-27","2018-03-30","2018-04-02","2018-04-05","2018-04-08","2018-04-11","2018-04-14","2018-04-17","2018-04-20","2018-04-23","2018-04-26","2018-04-29","2018-05-02","2018-05-05","2018-05-08","2018-05-11","2018-05-14","2018-05-17","2018-05-20","2018-05-23","2018-05-26","2018-05-29","2018-06-01","2018-06-04","2018-06-07","2018-06-10","2018-06-13","2018-06-16","2018-06-19","2018-06-22","2018-06-25","2018-06-28","2018-07-01","2018-07-04","2018-07-07","2018-07-10","2018-07-13","2018-07-16","2018-07-19","2018-07-22","2018-07-25","2018-07-28","2018-07-31","2018-08-03","2018-08-06","2018-08-09","2018-08-12","2018-08-15","2018-08-18","2018-08-21","2018-08-24","2018-08-27","2018-08-30","2018-09-02","2018-09-05","2018-09-08","2018-09-11","2018-09-14","2018-09-17","2018-09-20","2018-09-23","2018-09-26","2018-09-29","2018-10-02","2018-10-05","2018-10-08","2018-10-11","2018-10-14","2018-10-17","2018-10-20","2018-10-23","2018-10-26","2018-10-29","2018-11-01","2018-11-04","2018-11-07","2018-11-10","2018-11-13","2018-11-28","2018-12-01","2018-12-04","2018-12-07","2018-12-10","2018-12-13","2018-12-16","2018-12-19","2018-12-22","2018-12-25","2018-12-28","2018-12-31","2019-01-02","2019-01-05","2019-01-08","2019-01-11","2019-01-14","2019-01-17","2019-01-20","2019-01-23","2019-01-29","2019-02-01","2019-02-04","2019-02-07","2019-02-10","2019-02-13","2019-02-16","2019-02-19","2019-02-22","2019-02-25","2019-02-28","2019-03-03","2019-03-06","2019-03-09","2019-03-12","2019-03-15","2019-03-18","2019-03-21","2019-03-24","2019-03-27","2019-03-30","2019-04-02","2019-04-05","2019-04-08","2019-04-11","2019-04-14","2019-04-17","2019-04-20","2019-04-23","2019-04-26","2019-04-29","2019-05-02","2019-05-05","2019-05-08","2019-05-11","2019-05-14","2019-05-17","2019-05-20","2019-05-23","2019-05-26","2019-05-29","2019-06-01","2019-06-04","2019-06-07","2019-06-10","2019-06-13","2019-06-16","2019-06-19","2019-06-22","2019-06-25","2019-06-28","2019-07-01","2019-07-04","2019-07-07","2019-07-10","2019-07-13","2019-07-16","2019-07-19","2019-07-22","2019-07-25","2019-07-28","2019-07-31","2019-08-03","2019-08-06","2019-08-09","2019-08-12","2019-08-15","2019-08-18","2019-08-21","2019-08-24","2019-08-27","2019-08-30","2019-09-02","2019-09-05","2019-09-08","2019-09-11","2019-09-14","2019-09-17","2019-09-20","2019-09-23","2019-09-26","2019-09-29","2019-10-02","2019-10-05","2019-10-08","2019-10-11","2019-10-14","2019-10-17","2019-10-23","2019-10-26","2019-10-29","2019-11-01","2019-11-04","2019-11-07","2019-11-10","2019-11-13","2019-11-16","2019-11-19","2019-11-22","2019-11-25","2019-11-28","2019-12-01","2019-12-04","2019-12-07","2019-12-10","2019-12-13","2019-12-16","2019-12-19","2019-12-22","2019-12-25","2019-12-28","2019-12-31","2020-01-02","2020-01-05","2020-01-08","2020-01-11","2020-01-14","2020-01-17","2020-01-20","2020-01-23","2020-01-26","2020-01-29","2020-02-01","2020-02-04","2020-02-07","2020-02-10","2020-02-13","2020-02-16","2020-02-19","2020-02-22","2020-02-25","2020-02-28","2020-03-02","2020-03-05","2020-03-08","2020-03-11","2020-03-14","2020-03-17","2020-03-20","2020-03-23","2020-03-26","2020-03-29","2020-04-01","2020-04-04","2020-04-07","2020-04-10","2020-04-13","2020-04-16","2020-04-19","2020-05-04","2020-05-07","2020-05-10","2020-05-13","2020-05-16","2020-05-19","2020-05-22","2020-05-25","2020-05-28","2020-05-31","2020-06-03","2020-06-06","2020-06-09","2020-06-12","2020-06-15","2020-06-18","2020-06-21","2020-06-24","2020-06-27","2020-06-30","2020-07-03","2020-07-06","2020-07-09","2020-07-12","2020-07-15","2020-07-18","2020-07-21","2020-07-24","2020-07-27","2020-07-30","2020-08-02","2020-08-05","2020-08-08","2020-08-11","2020-08-14","2020-08-17","2020-08-20","2020-08-23","2020-08-26","2020-08-29","2020-09-01","2020-09-04","2020-09-07","2020-09-10","2020-09-13","2020-09-16","2020-09-19","2020-09-22","2020-09-25","2020-09-28","2020-10-01","2020-10-04","2020-10-07","2020-10-10","2020-10-13"],"y":[0.35909,0.36557,0.36554,0.36537,0.37027,0.3708,0.37058,0.37208,0.36901,0.37264,0.37909,0.39558,0.40069,0.42004,0.43538,0.43521,0.43893,0.4585,0.4578,0.46991,0.47149,0.4625,0.44934,0.44908,0.44893,0.44486,0.45703,0.45444,0.44772,0.44275,0.44916,0.44139,0.43981,0.44227,0.43696,0.44033,0.44643,0.4399,0.4353,0.43618,0.43762,0.44057,0.43764,0.43769,0.43497,0.43208,0.43049,0.43416,0.43195,0.43595,0.43466,0.43542,0.4373,0.44057,0.43762,0.43256,0.42536,0.42969,0.44281,0.43916,0.43482,0.42634,0.42557,0.41312,0.41114,0.40081,0.38423,0.37726,0.37438,0.34399,0.33894,0.33929,0.35486,0.36392,0.36789,0.37016,0.36801,0.36754,0.36713,0.37033,0.36803,0.36824,0.36701,0.36532,0.36625,0.36523,0.36735,0.36992,0.36409,0.36771,0.36785,0.36717,0.362,0.3646,0.36541,0.36633,0.36376,0.36857,0.3678,0.36303,0.36879,0.36663,0.3687,0.37149,0.36784,0.36824,0.36847,0.36733,0.36794,0.36765,0.36589,0.36989,0.36858,0.3692,0.37091,0.36995,0.36967,0.36965,0.36969,0.36808,0.36905,0.36832,0.37036,0.37154,0.37201,0.37253,0.37193,0.37194,0.37621,0.37972,0.38657,0.39548,0.41295,0.42068,0.43611,0.45175,0.45122,0.4621,0.46594,0.46323,0.45875,0.45856,0.45421,0.46746,0.45164,0.45324,0.45647,0.4589,0.45214,0.44671,0.43979,0.43278,0.43063,0.43311,0.43079,0.43591,0.43437,0.43986,0.44472,0.4365,0.44193,0.4355,0.43226,0.43063,0.43671,0.43154,0.43124,0.43991,0.42993,0.43001,0.43826,0.42453,0.42291,0.42609,0.43693,0.42706,0.42737,0.41752,0.42822,0.42986,0.42403,0.42051,0.42298,0.42217,0.4194,0.40535,0.40433,0.39109,0.37848,0.34386,0.34686,0.35532,0.3594,0.36859,0.37405,0.37087,0.37257,0.37242,0.37173,0.36775,0.37138,0.37102,0.37108,0.36957,0.37115,0.36955,0.36928,0.36627,0.36847,0.36895,0.36636,0.36596,0.35991,0.36677,0.36739,0.36814,0.3701,0.36918,0.36606,0.36869,0.36848,0.36622,0.36834,0.36811,0.36714,0.36836,0.36875,0.36285,0.36876,0.3687,0.36151,0.36682,0.36933,0.371,0.37152,0.37032,0.37163,0.37366,0.3738,0.37363,0.37086,0.37102,0.37594,0.37694,0.3774,0.37663,0.37704,0.37297,0.37808,0.38202,0.3896,0.39112,0.442,0.44022,0.46093,0.4598,0.46432,0.46923,0.46479,0.45823,0.45668,0.45179,0.44669,0.44758,0.45052,0.45844,0.44225,0.44074,0.43983,0.4436,0.43971,0.43143,0.43533,0.44001,0.44877,0.44318,0.43617,0.43862,0.43934,0.43419,0.43006,0.42961,0.43633,0.43142,0.43366,0.43133,0.43133,0.43158,0.43989,0.43956,0.4248,0.42361,0.43224,0.4246,0.42807,0.43173,0.42956,0.4271,0.42286,0.42309,0.42792,0.43107,0.43015,0.42282,0.41221,0.39698,0.38751,0.38075,0.37059,0.37073,0.35614,0.35503,0.3577,0.35984,0.36799,0.37307,0.37562,0.37443,0.37374,0.37479,0.37427,0.3711,0.3709,0.37008,0.37034,0.3712,0.36564,0.36977,0.37216,0.37228,0.36887,0.37029,0.37369,0.37013,0.36997,0.36969,0.36791,0.36857,0.36744,0.36522,0.36641,0.36803,0.36729,0.36813,0.3704,0.36859,0.36809,0.3719,0.37345,0.3712,0.37021,0.37262,0.36839,0.3713,0.36539,0.37048,0.36954,0.36938,0.37311,0.3714,0.37008,0.37015,0.37056,0.37131,0.37099,0.37332,0.37392,0.37389,0.37333,0.3736,0.37493,0.37651,0.37969,0.37983,0.38372,0.39108,0.40215,0.44258,0.44499,0.44671,0.46647,0.46473,0.48271,0.46654,0.45778,0.45708,0.47214,0.46109,0.4609,0.45011,0.4628,0.45156,0.44611,0.44308,0.45127,0.44322,0.44295,0.44234,0.44018,0.44405,0.44175,0.45194,0.44306,0.44014,0.44067,0.44084,0.44109,0.43629,0.45202,0.43788,0.43926,0.43626,0.43765,0.42937,0.43753,0.4386,0.44245,0.43199,0.43571,0.42547,0.43492,0.43814,0.43074,0.43215,0.43762,0.43565,0.41709,0.41432,0.42346,0.40858,0.41259,0.39794,0.38847,0.38547,0.37853,0.37551,0.36757,0.3584,0.37039,0.37064,0.37617,0.37399,0.37473,0.37746,0.3762,0.37434,0.37133,0.37378,0.37283,0.37375,0.37252,0.37303,0.37049,0.37065,0.37127,0.37319,0.37254,0.37374,0.37351,0.37028,0.37196,0.37104,0.36995,0.37316,0.37236,0.37388,0.37079,0.3717,0.3727,0.37058,0.36918,0.37074,0.37129,0.37019,0.3722,0.36394,0.37108,0.37372,0.37548,0.37495,0.37462,0.37781,0.37849,0.3767,0.37494,0.37397,0.37665,0.37547,0.37577,0.37835,0.38116,0.3809,0.38927,0.38589,0.38476,0.39771,0.40386,0.43327,0.4417,0.46189,0.47864,0.47118,0.48555,0.47945,0.46678,0.46122,0.46242,0.45853,0.45318,0.465,0.44951,0.45343,0.453,0.45266,0.44802,0.4476,0.4454,0.45014,0.44486,0.44682,0.4484,0.44555,0.45413,0.4455,0.45493,0.44807,0.44594,0.45423,0.44172,0.45127,0.44512,0.44415,0.43719,0.4394,0.43956,0.4349,0.44086,0.44908,0.44531,0.43391,0.43016,0.43027,0.44154,0.42929,0.43251,0.43358,0.43816,0.42322,0.41221,0.41165,0.40702,0.40102,0.38018,0.35538,0.36623,0.37612,0.38188,0.37899,0.37728,0.37821,0.37974,0.37677,0.3759,0.3771,0.37513,0.37332,0.37438,0.37499,0.37248,0.37079,0.3743,0.37244,0.36899,0.37328,0.37251,0.37355,0.36855,0.37279,0.3736,0.37312,0.37244,0.37358,0.37004,0.37488,0.36907,0.37019,0.36897,0.37258,0.37099,0.37146,0.37124,0.37395,0.37406,0.37402,0.37261,0.36628,0.37177,0.37086,0.37017,0.3734,0.37312,0.3726,0.37305,0.37051,0.37263,0.37271,0.37523,0.37284,0.37467,0.37499,0.37428,0.3758,0.37689,0.37748,0.37676,0.37804,0.37997,0.38203,0.38663,0.41862,0.44951,0.44286,0.44608,0.45814,0.48115,0.46895,0.47135,0.46783,0.46445,0.47403,0.46115,0.47119,0.45494,0.45766,0.4528,0.4574,0.45343,0.45875,0.44898,0.44638,0.45164,0.44385,0.4442,0.44465,0.44395,0.44666,0.44133,0.44082,0.4399,0.4389,0.45509,0.44223,0.43831,0.44233,0.43865,0.43794,0.44334,0.45118,0.44862,0.43502,0.43483,0.44165,0.43641,0.43068,0.42875,0.42593,0.42592,0.4244,0.41921,0.42901,0.41643,0.411,0.4064,0.38609,0.37442,0.36909,0.3694,0.36817,0.37252,0.36966,0.37201,0.37393,0.37489,0.37854,0.37699,0.37601,0.37376,0.3741,0.37363,0.3754,0.37287,0.37129,0.37053,0.37314,0.37638,0.37714,0.37273,0.37467,0.37269,0.36825,0.37401,0.3726,0.37245,0.37466,0.3733,0.37268,0.36996,0.37174,0.37239,0.37693,0.37209,0.37199,0.37257,0.37087,0.36949,0.37157,0.37389,0.37316,0.37306,0.37076,0.37267,0.37419,0.37435,0.37343,0.37329,0.37236,0.3717,0.37244,0.37346,0.37329,0.37329,0.37467,0.37611,0.37754,0.37408,0.37821,0.37786,0.37858,0.37702,0.37798,0.37848,0.38105,0.39413,0.40944,0.44142,0.4482,0.47905,0.47517,0.48113,0.47216,0.48751,0.46835,0.47755,0.47797,0.46107,0.45808,0.45637,0.46064,0.45864,0.46109,0.47005,0.45814,0.45431,0.45958,0.45857,0.45612,0.45557,0.45373,0.46041,0.45318,0.46196,0.45219,0.44952,0.4589,0.44965,0.44883,0.45923,0.44914,0.45076,0.45214,0.45219,0.451,0.4468,0.45869,0.45302,0.44141,0.44528,0.4401,0.44585,0.45154,0.4533,0.44739,0.43601,0.42572,0.41962,0.40043,0.3783,0.37956,0.36964,0.36552,0.36392,0.37003,0.37129,0.37561,0.3776,0.37564,0.37745,0.37887,0.38111,0.37838,0.3781,0.37367,0.36656,0.37336,0.37562,0.37379,0.37537,0.37507,0.37564,0.37332,0.37521,0.37059,0.37055,0.37213,0.36958,0.37235,0.37329,0.3739,0.37146,0.37415,0.37248,0.36921,0.36954,0.37063,0.36862,0.36858,0.37167,0.37003,0.37185,0.37083,0.37135,0.37311,0.37419,0.37411,0.37195,0.37099,0.37077,0.374,0.37122,0.37136,0.37435,0.37301,0.3724,0.37478,0.37676,0.37783,0.37681,0.37713,0.37501,0.3763,0.37916,0.38375,0.40109,0.43205,0.43528,0.44798,0.45237,0.4506,0.46135,0.46138,0.47971,0.45992,0.4676,0.46182,0.46099,0.47106,0.4552,0.46705,0.45417,0.45476,0.45368,0.45108,0.46025,0.45134,0.44977,0.44846,0.45817,0.45001,0.44824,0.45189,0.45073,0.44936,0.44639,0.4465,0.45989,0.44995,0.4516,0.45815,0.4486,0.44479,0.44561,0.4486,0.44304,0.44628,0.45689,0.45538,0.44367,0.4417,0.44071,0.43903,0.45021,0.45109,0.43997,0.44401,0.43046,0.43283,0.41929,0.41977,0.40928,0.39857,0.38536,0.33899,0.35048,0.37836,0.37854,0.37806,0.37805,0.37701,0.37602,0.37726,0.37786,0.37518,0.37568,0.37431,0.37558,0.3754,0.37748,0.37411,0.37658,0.37856,0.37367,0.37509,0.37493,0.37413,0.37547,0.37363,0.37359,0.36992,0.37199,0.37227,0.37455,0.37403,0.37677,0.37456,0.37373,0.3705,0.37021,0.37428,0.37454,0.3744,0.37292,0.3752,0.37159,0.37332,0.37698,0.37621,0.3767,0.37639,0.37375,0.37543,0.37396,0.37556,0.37906,0.3716,0.37749,0.3754,0.3764,0.37882,0.38087,0.38137,0.38018,0.37889,0.38065,0.38195,0.38132,0.3892,0.41293,0.41712,0.42994,0.45271,0.47169,0.4839,0.4802,0.47789,0.47994,0.46052,0.46816,0.46091,0.46135,0.46234,0.46053,0.46887,0.46152,0.45649,0.46066,0.48013,0.45833,0.46869,0.45851,0.45547,0.45843,0.45626,0.46306,0.46613,0.45571,0.44908,0.46146,0.4555,0.45559,0.45159,0.44541,0.45177,0.44806,0.4568,0.45001,0.45834,0.45531,0.44433,0.43978,0.46774,0.44954,0.43847,0.45622,0.45377,0.45437,0.43995,0.45234,0.43193,0.43168,0.40648,0.40544,0.38956,0.39765,0.37909,0.3762,0.34971,0.3515,0.36062,0.37263,0.37755,0.37593,0.37616,0.37624,0.37704,0.37743,0.37636,0.37413,0.37557,0.37433,0.37229,0.37574,0.37598,0.37615,0.3709,0.3704,0.37389,0.37068,0.37705,0.37475,0.37416,0.3747,0.37033,0.37537,0.37423,0.3735,0.37369,0.37328,0.36994,0.37114,0.37178,0.37545,0.37644,0.37761,0.377,0.37375,0.37545,0.37554,0.3719,0.37141,0.37393,0.37531,0.37659,0.37433,0.37397,0.37604,0.37264,0.37622,0.37979,0.37844,0.3791,0.3772,0.37934,0.3793,0.38417,0.38946,0.39763,0.39381,0.39857,0.41317,0.44274,0.4664,0.49167,0.48662,0.50251,0.48394,0.49246,0.48601,0.46645,0.46266,0.47007,0.47098,0.45595,0.45466,0.45214,0.45719,0.45145,0.46426,0.45227,0.4603,0.45035,0.44954,0.44725,0.45729,0.45092,0.44555,0.44647,0.45309,0.44406,0.44363,0.44917,0.44896,0.44372,0.44102,0.43965,0.44273,0.44135,0.44671,0.43994,0.43949,0.44295,0.44444,0.44896,0.44305,0.44304,0.44639,0.43474,0.43829,0.45531,0.43884,0.43739,0.43072,0.42829,0.42447,0.4182,0.40921,0.40462,0.3853,0.37268,0.36396,0.36929,0.36976,0.37681,0.37709,0.37948,0.3784,0.37696,0.37833,0.37833,0.37324,0.37107,0.3746,0.37803,0.37464,0.37395,0.37327,0.37118,0.37466,0.37285,0.37851,0.37693,0.37414,0.37259,0.37843,0.3735,0.3772,0.37433,0.37403,0.37472,0.37149,0.37299,0.37531,0.37555,0.37637,0.37827,0.37772,0.37823,0.37301,0.37409,0.3692,0.37357,0.37242,0.37415,0.37422,0.37557,0.37589,0.37575,0.37496,0.37392,0.37351,0.37528,0.37775,0.37536,0.37544,0.37885,0.37867,0.38062,0.38405,0.38709,0.39504,0.42206,0.42691,0.44884,0.47607,0.48267,0.48007,0.47307,0.47852,0.47904,0.46485,0.46133,0.46621,0.45857,0.46147,0.46263,0.45863,0.46925,0.46117,0.45965,0.45814,0.45426,0.45759,0.45706,0.45048,0.45806,0.46482,0.45582,0.45461,0.45825,0.45736,0.45179,0.45492,0.45292,0.45078,0.44235,0.44204,0.44573,0.44617,0.4453,0.44566,0.44959,0.4519,0.44831,0.4512,0.4517,0.44156,0.45141,0.44395,0.45047,0.44851,0.44796,0.44621,0.43285,0.42662,0.42728,0.42631,0.41905,0.41587,0.40176,0.35074,0.35199,0.36979,0.37226,0.37894,0.37996,0.37876,0.37766,0.37717,0.37847,0.37999,0.37803,0.37634,0.37609,0.37816,0.37807,0.37707,0.3788,0.37624,0.37448,0.37489,0.37488,0.37273,0.37522,0.37204,0.37435,0.37904,0.37754,0.37581,0.37317,0.37701,0.37233,0.37626,0.37384,0.37524,0.37472,0.3721,0.37521,0.37596,0.37815,0.37538,0.37696,0.37604,0.37678,0.37834,0.37716,0.37682,0.37859,0.37817,0.38238,0.37897,0.38509,0.38166,0.38284,0.38314,0.38543,0.38563,0.39056,0.41052,0.40505,0.41808,0.43917,0.4581,0.46838,0.486,0.49063,0.47335,0.46676,0.46808,0.46735,0.46193,0.46837,0.45937,0.46444,0.45456,0.45435,0.45337,0.45371,0.45408,0.45074,0.45149,0.45295,0.46365,0.4484,0.4523,0.45027,0.44919,0.45044,0.4499,0.44614,0.44637,0.44924,0.44809,0.44276,0.44534,0.44113,0.44738,0.44884,0.44164,0.45407,0.45097,0.44041,0.43785,0.44111,0.44078,0.43703,0.44789,0.44078,0.43771,0.43471,0.42094,0.41275,0.36922,0.36306,0.35647,0.37066,0.3815,0.3808,0.38026,0.38002,0.38096,0.37961,0.38023,0.38023,0.38031,0.37612,0.37767,0.37522,0.36532,0.37201,0.37365,0.37493,0.37945,0.38007,0.3789,0.36713,0.37637,0.37408,0.37768,0.38083,0.37764,0.37326,0.37546,0.37886,0.378,0.37606,0.37712,0.3755,0.37136,0.3692,0.37616,0.37574,0.37589,0.37716,0.37871,0.37658,0.37838,0.37748,0.38008,0.3803,0.37821,0.37804,0.37708,0.37662,0.3778,0.3803,0.37802,0.37996,0.38025,0.38312,0.38219,0.37975,0.37963,0.37987,0.3818,0.38019,0.38165,0.38782,0.40787,0.43116,0.44975,0.46664,0.47044,0.46843,0.46972,0.46472,0.47326,0.45451,0.45643,0.45628,0.4549,0.45691,0.4642,0.45445,0.44897,0.45419,0.45169,0.4486,0.4564,0.44967,0.44722,0.44759,0.44776,0.45082,0.44528,0.44558,0.44613,0.45047,0.44872,0.44409,0.45084,0.45046,0.4566,0.45238,0.44583,0.44382,0.44938,0.44739,0.44045,0.43968,0.43925,0.43974,0.45042,0.45002,0.43793,0.43949,0.43084,0.42859],"type":"scatter","mode":"markers","name":"GCC","opacity":0.5,"marker":{"color":"rgba(252,141,98,1)","line":{"color":"rgba(252,141,98,1)"}},"textfont":{"color":"rgba(252,141,98,1)"},"error_y":{"color":"rgba(252,141,98,1)"},"error_x":{"color":"rgba(252,141,98,1)"},"line":{"color":"rgba(252,141,98,1)"},"xaxis":"x","yaxis":"y","frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->


What patterns do you notice?  How would we go about determining say the start of spring? (SOS)

### Threshold values

Let's subset the transition date (td) for each year when 25% of the greenness amplitude (of the 90^th) percentile is reached (threshold_25).



```r
# select the rising (spring dates) for 25% threshold of Gcc 90
spring <- td[td$direction == "rising" & td$gcc_value == "gcc_90",]
```

Let's create a simple plot_ly line graph of the smooth Green Chromatic Coordinate (Gcc) and add points for transition dates:




```r
p = plot_ly() %>%
  add_trace(
    data = df,
    x = ~ as.Date(date),
    y = ~ smooth_gcc_90,
    name = 'PhenoCam GCC',
    showlegend = TRUE,
    type = 'scatter',
    mode = 'line'
  ) %>% add_markers(
    data= spring,
    x = ~ as.Date(spring$transition_25, origin = "1970-01-01"),
    y = ~ spring$threshold_25,
    type = 'scatter',
    mode = 'marker',
    name = 'Spring Dates')

p
```

<!--html_preserve--><div id="htmlwidget-f585b3e04f52f6d9c7eb" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-f585b3e04f52f6d9c7eb">{"x":{"visdat":{"8beea5c83f3":["function () ","plotlyVisDat"],"8bee3fdacbd5":["function () ","data"],"8bee357c2db3":["function () ","data"]},"cur_data":"8bee357c2db3","attrs":{"8bee3fdacbd5":{"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"x":{},"y":{},"name":"PhenoCam GCC","showlegend":true,"type":"scatter","mode":"line","inherit":true},"8bee357c2db3":{"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"x":{},"y":{},"type":"scatter","mode":"markers","name":"Spring Dates","inherit":true}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"xaxis":{"domain":[0,1],"automargin":true,"title":"as.Date(date)"},"yaxis":{"domain":[0,1],"automargin":true,"title":"smooth_gcc_90"},"hovermode":"closest","showlegend":true},"source":"A","config":{"showSendToCloud":false},"data":[{"x":["2008-01-06","2008-01-07","2008-01-08","2008-01-09","2008-01-10","2008-01-11","2008-01-12","2008-01-13","2008-01-14","2008-01-15","2008-01-16","2008-01-17","2008-01-18","2008-01-19","2008-01-20","2008-01-21","2008-01-22","2008-01-23","2008-01-24","2008-01-25","2008-01-26","2008-01-27","2008-01-28","2008-01-29","2008-01-30","2008-01-31","2008-02-01","2008-02-02","2008-02-03","2008-02-04","2008-02-05","2008-02-06","2008-02-07","2008-02-08","2008-02-09","2008-02-10","2008-02-11","2008-02-12","2008-02-13","2008-02-14","2008-02-15","2008-02-16","2008-02-17","2008-02-18","2008-02-19","2008-02-20","2008-02-21","2008-02-22","2008-02-23","2008-02-24","2008-02-25","2008-02-26","2008-02-27","2008-02-28","2008-02-29","2008-03-01","2008-03-02","2008-03-03","2008-03-04","2008-03-05","2008-03-06","2008-03-07","2008-03-08","2008-03-09","2008-03-10","2008-03-11","2008-03-12","2008-03-13","2008-03-14","2008-03-15","2008-03-16","2008-03-17","2008-03-18","2008-03-19","2008-03-20","2008-03-21","2008-03-22","2008-03-23","2008-03-24","2008-03-25","2008-03-26","2008-03-27","2008-03-28","2008-03-29","2008-03-30","2008-03-31","2008-04-01","2008-04-02","2008-04-03","2008-04-04","2008-04-05","2008-04-06","2008-04-07","2008-04-08","2008-04-09","2008-04-10","2008-04-11","2008-04-12","2008-04-13","2008-04-14","2008-04-15","2008-04-16","2008-04-17","2008-04-18","2008-04-19","2008-04-20","2008-04-21","2008-04-22","2008-04-23","2008-04-24","2008-04-25","2008-04-26","2008-04-27","2008-04-28","2008-04-29","2008-04-30","2008-05-01","2008-05-02","2008-05-03","2008-05-04","2008-05-05","2008-05-06","2008-05-07","2008-05-08","2008-05-09","2008-05-10","2008-05-11","2008-05-12","2008-05-13","2008-05-14","2008-05-15","2008-05-16","2008-05-17","2008-05-18","2008-05-19","2008-05-20","2008-05-21","2008-05-22","2008-05-23","2008-05-24","2008-05-25","2008-05-26","2008-05-27","2008-05-28","2008-05-29","2008-05-30","2008-05-31","2008-06-01","2008-06-02","2008-06-03","2008-06-04","2008-06-05","2008-06-06","2008-06-07","2008-06-08","2008-06-09","2008-06-10","2008-06-11","2008-06-12","2008-06-13","2008-06-14","2008-06-15","2008-06-16","2008-06-17","2008-06-18","2008-06-19","2008-06-20","2008-06-21","2008-06-22","2008-06-23","2008-06-24","2008-06-25","2008-06-26","2008-06-27","2008-06-28","2008-06-29","2008-06-30","2008-07-01","2008-07-02","2008-07-03","2008-07-04","2008-07-05","2008-07-06","2008-07-07","2008-07-08","2008-07-09","2008-07-10","2008-07-11","2008-07-12","2008-07-13","2008-07-14","2008-07-15","2008-07-16","2008-07-17","2008-07-18","2008-07-19","2008-07-20","2008-07-21","2008-07-22","2008-07-23","2008-07-24","2008-07-25","2008-07-26","2008-07-27","2008-07-28","2008-07-29","2008-07-30","2008-07-31","2008-08-01","2008-08-02","2008-08-03","2008-08-04","2008-08-05","2008-08-06","2008-08-07","2008-08-08","2008-08-09","2008-08-10","2008-08-11","2008-08-12","2008-08-13","2008-08-14","2008-08-15","2008-08-16","2008-08-17","2008-08-18","2008-08-19","2008-08-20","2008-08-21","2008-08-22","2008-08-23","2008-08-24","2008-08-25","2008-08-26","2008-08-27","2008-08-28","2008-08-29","2008-08-30","2008-08-31","2008-09-01","2008-09-02","2008-09-03","2008-09-04","2008-09-05","2008-09-06","2008-09-07","2008-09-08","2008-09-09","2008-09-10","2008-09-11","2008-09-12","2008-09-13","2008-09-14","2008-09-15","2008-09-16","2008-09-17","2008-09-18","2008-09-19","2008-09-20","2008-09-21","2008-09-22","2008-09-23","2008-09-24","2008-09-25","2008-09-26","2008-09-27","2008-09-28","2008-09-29","2008-09-30","2008-10-01","2008-10-02","2008-10-03","2008-10-04","2008-10-05","2008-10-06","2008-10-07","2008-10-08","2008-10-09","2008-10-10","2008-10-11","2008-10-12","2008-10-13","2008-10-14","2008-10-15","2008-10-16","2008-10-17","2008-10-18","2008-10-19","2008-10-20","2008-10-21","2008-10-22","2008-10-23","2008-10-24","2008-10-25","2008-10-26","2008-10-27","2008-10-28","2008-10-29","2008-10-30","2008-10-31","2008-11-01","2008-11-02","2008-11-03","2008-11-04","2008-11-05","2008-11-06","2008-11-07","2008-11-08","2008-11-09","2008-11-10","2008-11-11","2008-11-12","2008-11-13","2008-11-14","2008-11-15","2008-11-16","2008-11-17","2008-11-18","2008-11-19","2008-11-20","2008-11-21","2008-11-22","2008-11-23","2008-11-24","2008-11-25","2008-11-26","2008-11-27","2008-11-28","2008-11-29","2008-11-30","2008-12-01","2008-12-02","2008-12-03","2008-12-04","2008-12-05","2008-12-06","2008-12-07","2008-12-08","2008-12-09","2008-12-10","2008-12-11","2008-12-12","2008-12-13","2008-12-14","2008-12-15","2008-12-16","2008-12-17","2008-12-18","2008-12-19","2008-12-20","2008-12-21","2008-12-22","2008-12-23","2008-12-24","2008-12-25","2008-12-26","2008-12-27","2008-12-28","2008-12-29","2008-12-30","2008-12-31","2009-01-01","2009-01-02","2009-01-03","2009-01-04","2009-01-05","2009-01-06","2009-01-07","2009-01-08","2009-01-09","2009-01-10","2009-01-11","2009-01-12","2009-01-13","2009-01-14","2009-01-15","2009-01-16","2009-01-17","2009-01-18","2009-01-19","2009-01-20","2009-01-21","2009-01-22","2009-01-23","2009-01-24","2009-01-25","2009-01-26","2009-01-27","2009-01-28","2009-01-29","2009-01-30","2009-01-31","2009-02-01","2009-02-02","2009-02-03","2009-02-04","2009-02-05","2009-02-06","2009-02-07","2009-02-08","2009-02-09","2009-02-10","2009-02-11","2009-02-12","2009-02-13","2009-02-14","2009-02-15","2009-02-16","2009-02-17","2009-02-18","2009-02-19","2009-02-20","2009-02-21","2009-02-22","2009-02-23","2009-02-24","2009-02-25","2009-02-26","2009-02-27","2009-02-28","2009-03-01","2009-03-02","2009-03-03","2009-03-04","2009-03-05","2009-03-06","2009-03-07","2009-03-08","2009-03-09","2009-03-10","2009-03-11","2009-03-12","2009-03-13","2009-03-14","2009-03-15","2009-03-16","2009-03-17","2009-03-18","2009-03-19","2009-03-20","2009-03-21","2009-03-22","2009-03-23","2009-03-24","2009-03-25","2009-03-26","2009-03-27","2009-03-28","2009-03-29","2009-03-30","2009-03-31","2009-04-01","2009-04-02","2009-04-03","2009-04-04","2009-04-05","2009-04-06","2009-04-07","2009-04-08","2009-04-09","2009-04-10","2009-04-11","2009-04-12","2009-04-13","2009-04-14","2009-04-15","2009-04-16","2009-04-17","2009-04-18","2009-04-19","2009-04-20","2009-04-21","2009-04-22","2009-04-23","2009-04-24","2009-04-25","2009-04-26","2009-04-27","2009-04-28","2009-04-29","2009-04-30","2009-05-01","2009-05-02","2009-05-03","2009-05-04","2009-05-05","2009-05-06","2009-05-07","2009-05-08","2009-05-09","2009-05-10","2009-05-11","2009-05-12","2009-05-13","2009-05-14","2009-05-15","2009-05-16","2009-05-17","2009-05-18","2009-05-19","2009-05-20","2009-05-21","2009-05-22","2009-05-23","2009-05-24","2009-05-25","2009-05-26","2009-05-27","2009-05-28","2009-05-29","2009-05-30","2009-05-31","2009-06-01","2009-06-02","2009-06-03","2009-06-04","2009-06-05","2009-06-06","2009-06-07","2009-06-08","2009-06-09","2009-06-10","2009-06-11","2009-06-12","2009-06-13","2009-06-14","2009-06-15","2009-06-16","2009-06-17","2009-06-18","2009-06-19","2009-06-20","2009-06-21","2009-06-22","2009-06-23","2009-06-24","2009-06-25","2009-06-26","2009-06-27","2009-06-28","2009-06-29","2009-06-30","2009-07-01","2009-07-02","2009-07-03","2009-07-04","2009-07-05","2009-07-06","2009-07-07","2009-07-08","2009-07-09","2009-07-10","2009-07-11","2009-07-12","2009-07-13","2009-07-14","2009-07-15","2009-07-16","2009-07-17","2009-07-18","2009-07-19","2009-07-20","2009-07-21","2009-07-22","2009-07-23","2009-07-24","2009-07-25","2009-07-26","2009-07-27","2009-07-28","2009-07-29","2009-07-30","2009-07-31","2009-08-01","2009-08-02","2009-08-03","2009-08-04","2009-08-05","2009-08-06","2009-08-07","2009-08-08","2009-08-09","2009-08-10","2009-08-11","2009-08-12","2009-08-13","2009-08-14","2009-08-15","2009-08-16","2009-08-17","2009-08-18","2009-08-19","2009-08-20","2009-08-21","2009-08-22","2009-08-23","2009-08-24","2009-08-25","2009-08-26","2009-08-27","2009-08-28","2009-08-29","2009-08-30","2009-08-31","2009-09-01","2009-09-02","2009-09-03","2009-09-04","2009-09-05","2009-09-06","2009-09-07","2009-09-08","2009-09-09","2009-09-10","2009-09-11","2009-09-12","2009-09-13","2009-09-14","2009-09-15","2009-09-16","2009-09-17","2009-09-18","2009-09-19","2009-09-20","2009-09-21","2009-09-22","2009-09-23","2009-09-24","2009-09-25","2009-09-26","2009-09-27","2009-09-28","2009-09-29","2009-09-30","2009-10-01","2009-10-02","2009-10-03","2009-10-04","2009-10-05","2009-10-06","2009-10-07","2009-10-08","2009-10-09","2009-10-10","2009-10-11","2009-10-12","2009-10-13","2009-10-14","2009-10-15","2009-10-16","2009-10-17","2009-10-18","2009-10-19","2009-10-20","2009-10-21","2009-10-22","2009-10-23","2009-10-24","2009-10-25","2009-10-26","2009-10-27","2009-10-28","2009-10-29","2009-10-30","2009-10-31","2009-11-01","2009-11-02","2009-11-03","2009-11-04","2009-11-05","2009-11-06","2009-11-07","2009-11-08","2009-11-09","2009-11-10","2009-11-11","2009-11-12","2009-11-13","2009-11-14","2009-11-15","2009-11-16","2009-11-17","2009-11-18","2009-11-19","2009-11-20","2009-11-21","2009-11-22","2009-11-23","2009-11-24","2009-11-25","2009-11-26","2009-11-27","2009-11-28","2009-11-29","2009-11-30","2009-12-01","2009-12-02","2009-12-03","2009-12-04","2009-12-05","2009-12-06","2009-12-07","2009-12-08","2009-12-09","2009-12-10","2009-12-11","2009-12-12","2009-12-13","2009-12-14","2009-12-15","2009-12-16","2009-12-17","2009-12-18","2009-12-19","2009-12-20","2009-12-21","2009-12-22","2009-12-23","2009-12-24","2009-12-25","2009-12-26","2009-12-27","2009-12-28","2009-12-29","2009-12-30","2009-12-31","2010-01-01","2010-01-02","2010-01-03","2010-01-04","2010-01-05","2010-01-06","2010-01-07","2010-01-08","2010-01-09","2010-01-10","2010-01-11","2010-01-12","2010-01-13","2010-01-14","2010-01-15","2010-01-16","2010-01-17","2010-01-18","2010-01-19","2010-01-20","2010-01-21","2010-01-22","2010-01-23","2010-01-24","2010-01-25","2010-01-26","2010-01-27","2010-01-28","2010-01-29","2010-01-30","2010-01-31","2010-02-01","2010-02-02","2010-02-03","2010-02-04","2010-02-05","2010-02-06","2010-02-07","2010-02-08","2010-02-09","2010-02-10","2010-02-11","2010-02-12","2010-02-13","2010-02-14","2010-02-15","2010-02-16","2010-02-17","2010-02-18","2010-02-19","2010-02-20","2010-02-21","2010-02-22","2010-02-23","2010-02-24","2010-02-25","2010-02-26","2010-02-27","2010-02-28","2010-03-01","2010-03-02","2010-03-03","2010-03-04","2010-03-05","2010-03-06","2010-03-07","2010-03-08","2010-03-09","2010-03-10","2010-03-11","2010-03-12","2010-03-13","2010-03-14","2010-03-15","2010-03-16","2010-03-17","2010-03-18","2010-03-19","2010-03-20","2010-03-21","2010-03-22","2010-03-23","2010-03-24","2010-03-25","2010-03-26","2010-03-27","2010-03-28","2010-03-29","2010-03-30","2010-03-31","2010-04-01","2010-04-02","2010-04-03","2010-04-04","2010-04-05","2010-04-06","2010-04-07","2010-04-08","2010-04-09","2010-04-10","2010-04-11","2010-04-12","2010-04-13","2010-04-14","2010-04-15","2010-04-16","2010-04-17","2010-04-18","2010-04-19","2010-04-20","2010-04-21","2010-04-22","2010-04-23","2010-04-24","2010-04-25","2010-04-26","2010-04-27","2010-04-28","2010-04-29","2010-04-30","2010-05-01","2010-05-02","2010-05-03","2010-05-04","2010-05-05","2010-05-06","2010-05-07","2010-05-08","2010-05-09","2010-05-10","2010-05-11","2010-05-12","2010-05-13","2010-05-14","2010-05-15","2010-05-16","2010-05-17","2010-05-18","2010-05-19","2010-05-20","2010-05-21","2010-05-22","2010-05-23","2010-05-24","2010-05-25","2010-05-26","2010-05-27","2010-05-28","2010-05-29","2010-05-30","2010-05-31","2010-06-01","2010-06-02","2010-06-03","2010-06-04","2010-06-05","2010-06-06","2010-06-07","2010-06-08","2010-06-09","2010-06-10","2010-06-11","2010-06-12","2010-06-13","2010-06-14","2010-06-15","2010-06-16","2010-06-17","2010-06-18","2010-06-19","2010-06-20","2010-06-21","2010-06-22","2010-06-23","2010-06-24","2010-06-25","2010-06-26","2010-06-27","2010-06-28","2010-06-29","2010-06-30","2010-07-01","2010-07-02","2010-07-03","2010-07-04","2010-07-05","2010-07-06","2010-07-07","2010-07-08","2010-07-09","2010-07-10","2010-07-11","2010-07-12","2010-07-13","2010-07-14","2010-07-15","2010-07-16","2010-07-17","2010-07-18","2010-07-19","2010-07-20","2010-07-21","2010-07-22","2010-07-23","2010-07-24","2010-07-25","2010-07-26","2010-07-27","2010-07-28","2010-07-29","2010-07-30","2010-07-31","2010-08-01","2010-08-02","2010-08-03","2010-08-04","2010-08-05","2010-08-06","2010-08-07","2010-08-08","2010-08-09","2010-08-10","2010-08-11","2010-08-12","2010-08-13","2010-08-14","2010-08-15","2010-08-16","2010-08-17","2010-08-18","2010-08-19","2010-08-20","2010-08-21","2010-08-22","2010-08-23","2010-08-24","2010-08-25","2010-08-26","2010-08-27","2010-08-28","2010-08-29","2010-08-30","2010-08-31","2010-09-01","2010-09-02","2010-09-03","2010-09-04","2010-09-05","2010-09-06","2010-09-07","2010-09-08","2010-09-09","2010-09-10","2010-09-11","2010-09-12","2010-09-13","2010-09-14","2010-09-15","2010-09-16","2010-09-17","2010-09-18","2010-09-19","2010-09-20","2010-09-21","2010-09-22","2010-09-23","2010-09-24","2010-09-25","2010-09-26","2010-09-27","2010-09-28","2010-09-29","2010-09-30","2010-10-01","2010-10-02","2010-10-03","2010-10-04","2010-10-05","2010-10-06","2010-10-07","2010-10-08","2010-10-09","2010-10-10","2010-10-11","2010-10-12","2010-10-13","2010-10-14","2010-10-15","2010-10-16","2010-10-17","2010-10-18","2010-10-19","2010-10-20","2010-10-21","2010-10-22","2010-10-23","2010-10-24","2010-10-25","2010-10-26","2010-10-27","2010-10-28","2010-10-29","2010-10-30","2010-10-31","2010-11-01","2010-11-02","2010-11-03","2010-11-04","2010-11-05","2010-11-06","2010-11-07","2010-11-08","2010-11-09","2010-11-10","2010-11-11","2010-11-12","2010-11-13","2010-11-14","2010-11-15","2010-11-16","2010-11-17","2010-11-18","2010-11-19","2010-11-20","2010-11-21","2010-11-22","2010-11-23","2010-11-24","2010-11-25","2010-11-26","2010-11-27","2010-11-28","2010-11-29","2010-11-30","2010-12-01","2010-12-02","2010-12-03","2010-12-04","2010-12-05","2010-12-06","2010-12-07","2010-12-08","2010-12-09","2010-12-10","2010-12-11","2010-12-12","2010-12-13","2010-12-14","2010-12-15","2010-12-16","2010-12-17","2010-12-18","2010-12-19","2010-12-20","2010-12-21","2010-12-22","2010-12-23","2010-12-24","2010-12-25","2010-12-26","2010-12-27","2010-12-28","2010-12-29","2010-12-30","2010-12-31","2011-01-01","2011-01-02","2011-01-03","2011-01-04","2011-01-05","2011-01-06","2011-01-07","2011-01-08","2011-01-09","2011-01-10","2011-01-11","2011-01-12","2011-01-13","2011-01-14","2011-01-15","2011-01-16","2011-01-17","2011-01-18","2011-01-19","2011-01-20","2011-01-21","2011-01-22","2011-01-23","2011-01-24","2011-01-25","2011-01-26","2011-01-27","2011-01-28","2011-01-29","2011-01-30","2011-01-31","2011-02-01","2011-02-02","2011-02-03","2011-02-04","2011-02-05","2011-02-06","2011-02-07","2011-02-08","2011-02-09","2011-02-10","2011-02-11","2011-02-12","2011-02-13","2011-02-14","2011-02-15","2011-02-16","2011-02-17","2011-02-18","2011-02-19","2011-02-20","2011-02-21","2011-02-22","2011-02-23","2011-02-24","2011-02-25","2011-02-26","2011-02-27","2011-02-28","2011-03-01","2011-03-02","2011-03-03","2011-03-04","2011-03-05","2011-03-06","2011-03-07","2011-03-08","2011-03-09","2011-03-10","2011-03-11","2011-03-12","2011-03-13","2011-03-14","2011-03-15","2011-03-16","2011-03-17","2011-03-18","2011-03-19","2011-03-20","2011-03-21","2011-03-22","2011-03-23","2011-03-24","2011-03-25","2011-03-26","2011-03-27","2011-03-28","2011-03-29","2011-03-30","2011-03-31","2011-04-01","2011-04-02","2011-04-03","2011-04-04","2011-04-05","2011-04-06","2011-04-07","2011-04-08","2011-04-09","2011-04-10","2011-04-11","2011-04-12","2011-04-13","2011-04-14","2011-04-15","2011-04-16","2011-04-17","2011-04-18","2011-04-19","2011-04-20","2011-04-21","2011-04-22","2011-04-23","2011-04-24","2011-04-25","2011-04-26","2011-04-27","2011-04-28","2011-04-29","2011-04-30","2011-05-01","2011-05-02","2011-05-03","2011-05-04","2011-05-05","2011-05-06","2011-05-07","2011-05-08","2011-05-09","2011-05-10","2011-05-11","2011-05-12","2011-05-13","2011-05-14","2011-05-15","2011-05-16","2011-05-17","2011-05-18","2011-05-19","2011-05-20","2011-05-21","2011-05-22","2011-05-23","2011-05-24","2011-05-25","2011-05-26","2011-05-27","2011-05-28","2011-05-29","2011-05-30","2011-05-31","2011-06-01","2011-06-02","2011-06-03","2011-06-04","2011-06-05","2011-06-06","2011-06-07","2011-06-08","2011-06-09","2011-06-10","2011-06-11","2011-06-12","2011-06-13","2011-06-14","2011-06-15","2011-06-16","2011-06-17","2011-06-18","2011-06-19","2011-06-20","2011-06-21","2011-06-22","2011-06-23","2011-06-24","2011-06-25","2011-06-26","2011-06-27","2011-06-28","2011-06-29","2011-06-30","2011-07-01","2011-07-02","2011-07-03","2011-07-04","2011-07-05","2011-07-06","2011-07-07","2011-07-08","2011-07-09","2011-07-10","2011-07-11","2011-07-12","2011-07-13","2011-07-14","2011-07-15","2011-07-16","2011-07-17","2011-07-18","2011-07-19","2011-07-20","2011-07-21","2011-07-22","2011-07-23","2011-07-24","2011-07-25","2011-07-26","2011-07-27","2011-07-28","2011-07-29","2011-07-30","2011-07-31","2011-08-01","2011-08-02","2011-08-03","2011-08-04","2011-08-05","2011-08-06","2011-08-07","2011-08-08","2011-08-09","2011-08-10","2011-08-11","2011-08-12","2011-08-13","2011-08-14","2011-08-15","2011-08-16","2011-08-17","2011-08-18","2011-08-19","2011-08-20","2011-08-21","2011-08-22","2011-08-23","2011-08-24","2011-08-25","2011-08-26","2011-08-27","2011-08-28","2011-08-29","2011-08-30","2011-08-31","2011-09-01","2011-09-02","2011-09-03","2011-09-04","2011-09-05","2011-09-06","2011-09-07","2011-09-08","2011-09-09","2011-09-10","2011-09-11","2011-09-12","2011-09-13","2011-09-14","2011-09-15","2011-09-16","2011-09-17","2011-09-18","2011-09-19","2011-09-20","2011-09-21","2011-09-22","2011-09-23","2011-09-24","2011-09-25","2011-09-26","2011-09-27","2011-09-28","2011-09-29","2011-09-30","2011-10-01","2011-10-02","2011-10-03","2011-10-04","2011-10-05","2011-10-06","2011-10-07","2011-10-08","2011-10-09","2011-10-10","2011-10-11","2011-10-12","2011-10-13","2011-10-14","2011-10-15","2011-10-16","2011-10-17","2011-10-18","2011-10-19","2011-10-20","2011-10-21","2011-10-22","2011-10-23","2011-10-24","2011-10-25","2011-10-26","2011-10-27","2011-10-28","2011-10-29","2011-10-30","2011-10-31","2011-11-01","2011-11-02","2011-11-03","2011-11-04","2011-11-05","2011-11-06","2011-11-07","2011-11-08","2011-11-09","2011-11-10","2011-11-11","2011-11-12","2011-11-13","2011-11-14","2011-11-15","2011-11-16","2011-11-17","2011-11-18","2011-11-19","2011-11-20","2011-11-21","2011-11-22","2011-11-23","2011-11-24","2011-11-25","2011-11-26","2011-11-27","2011-11-28","2011-11-29","2011-11-30","2011-12-01","2011-12-02","2011-12-03","2011-12-04","2011-12-05","2011-12-06","2011-12-07","2011-12-08","2011-12-09","2011-12-10","2011-12-11","2011-12-12","2011-12-13","2011-12-14","2011-12-15","2011-12-16","2011-12-17","2011-12-18","2011-12-19","2011-12-20","2011-12-21","2011-12-22","2011-12-23","2011-12-24","2011-12-25","2011-12-26","2011-12-27","2011-12-28","2011-12-29","2011-12-30","2011-12-31","2012-01-01","2012-01-02","2012-01-03","2012-01-04","2012-01-05","2012-01-06","2012-01-07","2012-01-08","2012-01-09","2012-01-10","2012-01-11","2012-01-12","2012-01-13","2012-01-14","2012-01-15","2012-01-16","2012-01-17","2012-01-18","2012-01-19","2012-01-20","2012-01-21","2012-01-22","2012-01-23","2012-01-24","2012-01-25","2012-01-26","2012-01-27","2012-01-28","2012-01-29","2012-01-30","2012-01-31","2012-02-01","2012-02-02","2012-02-03","2012-02-04","2012-02-05","2012-02-06","2012-02-07","2012-02-08","2012-02-09","2012-02-10","2012-02-11","2012-02-12","2012-02-13","2012-02-14","2012-02-15","2012-02-16","2012-02-17","2012-02-18","2012-02-19","2012-02-20","2012-02-21","2012-02-22","2012-02-23","2012-02-24","2012-02-25","2012-02-26","2012-02-27","2012-02-28","2012-02-29","2012-03-01","2012-03-02","2012-03-03","2012-03-04","2012-03-05","2012-03-06","2012-03-07","2012-03-08","2012-03-09","2012-03-10","2012-03-11","2012-03-12","2012-03-13","2012-03-14","2012-03-15","2012-03-16","2012-03-17","2012-03-18","2012-03-19","2012-03-20","2012-03-21","2012-03-22","2012-03-23","2012-03-24","2012-03-25","2012-03-26","2012-03-27","2012-03-28","2012-03-29","2012-03-30","2012-03-31","2012-04-01","2012-04-02","2012-04-03","2012-04-04","2012-04-05","2012-04-06","2012-04-07","2012-04-08","2012-04-09","2012-04-10","2012-04-11","2012-04-12","2012-04-13","2012-04-14","2012-04-15","2012-04-16","2012-04-17","2012-04-18","2012-04-19","2012-04-20","2012-04-21","2012-04-22","2012-04-23","2012-04-24","2012-04-25","2012-04-26","2012-04-27","2012-04-28","2012-04-29","2012-04-30","2012-05-01","2012-05-02","2012-05-03","2012-05-04","2012-05-05","2012-05-06","2012-05-07","2012-05-08","2012-05-09","2012-05-10","2012-05-11","2012-05-12","2012-05-13","2012-05-14","2012-05-15","2012-05-16","2012-05-17","2012-05-18","2012-05-19","2012-05-20","2012-05-21","2012-05-22","2012-05-23","2012-05-24","2012-05-25","2012-05-26","2012-05-27","2012-05-28","2012-05-29","2012-05-30","2012-05-31","2012-06-01","2012-06-02","2012-06-03","2012-06-04","2012-06-05","2012-06-06","2012-06-07","2012-06-08","2012-06-09","2012-06-10","2012-06-11","2012-06-12","2012-06-13","2012-06-14","2012-06-15","2012-06-16","2012-06-17","2012-06-18","2012-06-19","2012-06-20","2012-06-21","2012-06-22","2012-06-23","2012-06-24","2012-06-25","2012-06-26","2012-06-27","2012-06-28","2012-06-29","2012-06-30","2012-07-01","2012-07-02","2012-07-03","2012-07-04","2012-07-05","2012-07-06","2012-07-07","2012-07-08","2012-07-09","2012-07-10","2012-07-11","2012-07-12","2012-07-13","2012-07-14","2012-07-15","2012-07-16","2012-07-17","2012-07-18","2012-07-19","2012-07-20","2012-07-21","2012-07-22","2012-07-23","2012-07-24","2012-07-25","2012-07-26","2012-07-27","2012-07-28","2012-07-29","2012-07-30","2012-07-31","2012-08-01","2012-08-02","2012-08-03","2012-08-04","2012-08-05","2012-08-06","2012-08-07","2012-08-08","2012-08-09","2012-08-10","2012-08-11","2012-08-12","2012-08-13","2012-08-14","2012-08-15","2012-08-16","2012-08-17","2012-08-18","2012-08-19","2012-08-20","2012-08-21","2012-08-22","2012-08-23","2012-08-24","2012-08-25","2012-08-26","2012-08-27","2012-08-28","2012-08-29","2012-08-30","2012-08-31","2012-09-01","2012-09-02","2012-09-03","2012-09-04","2012-09-05","2012-09-06","2012-09-07","2012-09-08","2012-09-09","2012-09-10","2012-09-11","2012-09-12","2012-09-13","2012-09-14","2012-09-15","2012-09-16","2012-09-17","2012-09-18","2012-09-19","2012-09-20","2012-09-21","2012-09-22","2012-09-23","2012-09-24","2012-09-25","2012-09-26","2012-09-27","2012-09-28","2012-09-29","2012-09-30","2012-10-01","2012-10-02","2012-10-03","2012-10-04","2012-10-05","2012-10-06","2012-10-07","2012-10-08","2012-10-09","2012-10-10","2012-10-11","2012-10-12","2012-10-13","2012-10-14","2012-10-15","2012-10-16","2012-10-17","2012-10-18","2012-10-19","2012-10-20","2012-10-21","2012-10-22","2012-10-23","2012-10-24","2012-10-25","2012-10-26","2012-10-27","2012-10-28","2012-10-29","2012-10-30","2012-10-31","2012-11-01","2012-11-02","2012-11-03","2012-11-04","2012-11-05","2012-11-06","2012-11-07","2012-11-08","2012-11-09","2012-11-10","2012-11-11","2012-11-12","2012-11-13","2012-11-14","2012-11-15","2012-11-16","2012-11-17","2012-11-18","2012-11-19","2012-11-20","2012-11-21","2012-11-22","2012-11-23","2012-11-24","2012-11-25","2012-11-26","2012-11-27","2012-11-28","2012-11-29","2012-11-30","2012-12-01","2012-12-02","2012-12-03","2012-12-04","2012-12-05","2012-12-06","2012-12-07","2012-12-08","2012-12-09","2012-12-10","2012-12-11","2012-12-12","2012-12-13","2012-12-14","2012-12-15","2012-12-16","2012-12-17","2012-12-18","2012-12-19","2012-12-20","2012-12-21","2012-12-22","2012-12-23","2012-12-24","2012-12-25","2012-12-26","2012-12-27","2012-12-28","2012-12-29","2012-12-30","2012-12-31","2013-01-01","2013-01-02","2013-01-03","2013-01-04","2013-01-05","2013-01-06","2013-01-07","2013-01-08","2013-01-09","2013-01-10","2013-01-11","2013-01-12","2013-01-13","2013-01-14","2013-01-15","2013-01-16","2013-01-17","2013-01-18","2013-01-19","2013-01-20","2013-01-21","2013-01-22","2013-01-23","2013-01-24","2013-01-25","2013-01-26","2013-01-27","2013-01-28","2013-01-29","2013-01-30","2013-01-31","2013-02-01","2013-02-02","2013-02-03","2013-02-04","2013-02-05","2013-02-06","2013-02-07","2013-02-08","2013-02-09","2013-02-10","2013-02-11","2013-02-12","2013-02-13","2013-02-14","2013-02-15","2013-02-16","2013-02-17","2013-02-18","2013-02-19","2013-02-20","2013-02-21","2013-02-22","2013-02-23","2013-02-24","2013-02-25","2013-02-26","2013-02-27","2013-02-28","2013-03-01","2013-03-02","2013-03-03","2013-03-04","2013-03-05","2013-03-06","2013-03-07","2013-03-08","2013-03-09","2013-03-10","2013-03-11","2013-03-12","2013-03-13","2013-03-14","2013-03-15","2013-03-16","2013-03-17","2013-03-18","2013-03-19","2013-03-20","2013-03-21","2013-03-22","2013-03-23","2013-03-24","2013-03-25","2013-03-26","2013-03-27","2013-03-28","2013-03-29","2013-03-30","2013-03-31","2013-04-01","2013-04-02","2013-04-03","2013-04-04","2013-04-05","2013-04-06","2013-04-07","2013-04-08","2013-04-09","2013-04-10","2013-04-11","2013-04-12","2013-04-13","2013-04-14","2013-04-15","2013-04-16","2013-04-17","2013-04-18","2013-04-19","2013-04-20","2013-04-21","2013-04-22","2013-04-23","2013-04-24","2013-04-25","2013-04-26","2013-04-27","2013-04-28","2013-04-29","2013-04-30","2013-05-01","2013-05-02","2013-05-03","2013-05-04","2013-05-05","2013-05-06","2013-05-07","2013-05-08","2013-05-09","2013-05-10","2013-05-11","2013-05-12","2013-05-13","2013-05-14","2013-05-15","2013-05-16","2013-05-17","2013-05-18","2013-05-19","2013-05-20","2013-05-21","2013-05-22","2013-05-23","2013-05-24","2013-05-25","2013-05-26","2013-05-27","2013-05-28","2013-05-29","2013-05-30","2013-05-31","2013-06-01","2013-06-02","2013-06-03","2013-06-04","2013-06-05","2013-06-06","2013-06-07","2013-06-08","2013-06-09","2013-06-10","2013-06-11","2013-06-12","2013-06-13","2013-06-14","2013-06-15","2013-06-16","2013-06-17","2013-06-18","2013-06-19","2013-06-20","2013-06-21","2013-06-22","2013-06-23","2013-06-24","2013-06-25","2013-06-26","2013-06-27","2013-06-28","2013-06-29","2013-06-30","2013-07-01","2013-07-02","2013-07-03","2013-07-04","2013-07-05","2013-07-06","2013-07-07","2013-07-08","2013-07-09","2013-07-10","2013-07-11","2013-07-12","2013-07-13","2013-07-14","2013-07-15","2013-07-16","2013-07-17","2013-07-18","2013-07-19","2013-07-20","2013-07-21","2013-07-22","2013-07-23","2013-07-24","2013-07-25","2013-07-26","2013-07-27","2013-07-28","2013-07-29","2013-07-30","2013-07-31","2013-08-01","2013-08-02","2013-08-03","2013-08-04","2013-08-05","2013-08-06","2013-08-07","2013-08-08","2013-08-09","2013-08-10","2013-08-11","2013-08-12","2013-08-13","2013-08-14","2013-08-15","2013-08-16","2013-08-17","2013-08-18","2013-08-19","2013-08-20","2013-08-21","2013-08-22","2013-08-23","2013-08-24","2013-08-25","2013-08-26","2013-08-27","2013-08-28","2013-08-29","2013-08-30","2013-08-31","2013-09-01","2013-09-02","2013-09-03","2013-09-04","2013-09-05","2013-09-06","2013-09-07","2013-09-08","2013-09-09","2013-09-10","2013-09-11","2013-09-12","2013-09-13","2013-09-14","2013-09-15","2013-09-16","2013-09-17","2013-09-18","2013-09-19","2013-09-20","2013-09-21","2013-09-22","2013-09-23","2013-09-24","2013-09-25","2013-09-26","2013-09-27","2013-09-28","2013-09-29","2013-09-30","2013-10-01","2013-10-02","2013-10-03","2013-10-04","2013-10-05","2013-10-06","2013-10-07","2013-10-08","2013-10-09","2013-10-10","2013-10-11","2013-10-12","2013-10-13","2013-10-14","2013-10-15","2013-10-16","2013-10-17","2013-10-18","2013-10-19","2013-10-20","2013-10-21","2013-10-22","2013-10-23","2013-10-24","2013-10-25","2013-10-26","2013-10-27","2013-10-28","2013-10-29","2013-10-30","2013-10-31","2013-11-01","2013-11-02","2013-11-03","2013-11-04","2013-11-05","2013-11-06","2013-11-07","2013-11-08","2013-11-09","2013-11-10","2013-11-11","2013-11-12","2013-11-13","2013-11-14","2013-11-15","2013-11-16","2013-11-17","2013-11-18","2013-11-19","2013-11-20","2013-11-21","2013-11-22","2013-11-23","2013-11-24","2013-11-25","2013-11-26","2013-11-27","2013-11-28","2013-11-29","2013-11-30","2013-12-01","2013-12-02","2013-12-03","2013-12-04","2013-12-05","2013-12-06","2013-12-07","2013-12-08","2013-12-09","2013-12-10","2013-12-11","2013-12-12","2013-12-13","2013-12-14","2013-12-15","2013-12-16","2013-12-17","2013-12-18","2013-12-19","2013-12-20","2013-12-21","2013-12-22","2013-12-23","2013-12-24","2013-12-25","2013-12-26","2013-12-27","2013-12-28","2013-12-29","2013-12-30","2013-12-31","2014-01-01","2014-01-02","2014-01-03","2014-01-04","2014-01-05","2014-01-06","2014-01-07","2014-01-08","2014-01-09","2014-01-10","2014-01-11","2014-01-12","2014-01-13","2014-01-14","2014-01-15","2014-01-16","2014-01-17","2014-01-18","2014-01-19","2014-01-20","2014-01-21","2014-01-22","2014-01-23","2014-01-24","2014-01-25","2014-01-26","2014-01-27","2014-01-28","2014-01-29","2014-01-30","2014-01-31","2014-02-01","2014-02-02","2014-02-03","2014-02-04","2014-02-05","2014-02-06","2014-02-07","2014-02-08","2014-02-09","2014-02-10","2014-02-11","2014-02-12","2014-02-13","2014-02-14","2014-02-15","2014-02-16","2014-02-17","2014-02-18","2014-02-19","2014-02-20","2014-02-21","2014-02-22","2014-02-23","2014-02-24","2014-02-25","2014-02-26","2014-02-27","2014-02-28","2014-03-01","2014-03-02","2014-03-03","2014-03-04","2014-03-05","2014-03-06","2014-03-07","2014-03-08","2014-03-09","2014-03-10","2014-03-11","2014-03-12","2014-03-13","2014-03-14","2014-03-15","2014-03-16","2014-03-17","2014-03-18","2014-03-19","2014-03-20","2014-03-21","2014-03-22","2014-03-23","2014-03-24","2014-03-25","2014-03-26","2014-03-27","2014-03-28","2014-03-29","2014-03-30","2014-03-31","2014-04-01","2014-04-02","2014-04-03","2014-04-04","2014-04-05","2014-04-06","2014-04-07","2014-04-08","2014-04-09","2014-04-10","2014-04-11","2014-04-12","2014-04-13","2014-04-14","2014-04-15","2014-04-16","2014-04-17","2014-04-18","2014-04-19","2014-04-20","2014-04-21","2014-04-22","2014-04-23","2014-04-24","2014-04-25","2014-04-26","2014-04-27","2014-04-28","2014-04-29","2014-04-30","2014-05-01","2014-05-02","2014-05-03","2014-05-04","2014-05-05","2014-05-06","2014-05-07","2014-05-08","2014-05-09","2014-05-10","2014-05-11","2014-05-12","2014-05-13","2014-05-14","2014-05-15","2014-05-16","2014-05-17","2014-05-18","2014-05-19","2014-05-20","2014-05-21","2014-05-22","2014-05-23","2014-05-24","2014-05-25","2014-05-26","2014-05-27","2014-05-28","2014-05-29","2014-05-30","2014-05-31","2014-06-01","2014-06-02","2014-06-03","2014-06-04","2014-06-05","2014-06-06","2014-06-07","2014-06-08","2014-06-09","2014-06-10","2014-06-11","2014-06-12","2014-06-13","2014-06-14","2014-06-15","2014-06-16","2014-06-17","2014-06-18","2014-06-19","2014-06-20","2014-06-21","2014-06-22","2014-06-23","2014-06-24","2014-06-25","2014-06-26","2014-06-27","2014-06-28","2014-06-29","2014-06-30","2014-07-01","2014-07-02","2014-07-03","2014-07-04","2014-07-05","2014-07-06","2014-07-07","2014-07-08","2014-07-09","2014-07-10","2014-07-11","2014-07-12","2014-07-13","2014-07-14","2014-07-15","2014-07-16","2014-07-17","2014-07-18","2014-07-19","2014-07-20","2014-07-21","2014-07-22","2014-07-23","2014-07-24","2014-07-25","2014-07-26","2014-07-27","2014-07-28","2014-07-29","2014-07-30","2014-07-31","2014-08-01","2014-08-02","2014-08-03","2014-08-04","2014-08-05","2014-08-06","2014-08-07","2014-08-08","2014-08-09","2014-08-10","2014-08-11","2014-08-12","2014-08-13","2014-08-14","2014-08-15","2014-08-16","2014-08-17","2014-08-18","2014-08-19","2014-08-20","2014-08-21","2014-08-22","2014-08-23","2014-08-24","2014-08-25","2014-08-26","2014-08-27","2014-08-28","2014-08-29","2014-08-30","2014-08-31","2014-09-01","2014-09-02","2014-09-03","2014-09-04","2014-09-05","2014-09-06","2014-09-07","2014-09-08","2014-09-09","2014-09-10","2014-09-11","2014-09-12","2014-09-13","2014-09-14","2014-09-15","2014-09-16","2014-09-17","2014-09-18","2014-09-19","2014-09-20","2014-09-21","2014-09-22","2014-09-23","2014-09-24","2014-09-25","2014-09-26","2014-09-27","2014-09-28","2014-09-29","2014-09-30","2014-10-01","2014-10-02","2014-10-03","2014-10-04","2014-10-05","2014-10-06","2014-10-07","2014-10-08","2014-10-09","2014-10-10","2014-10-11","2014-10-12","2014-10-13","2014-10-14","2014-10-15","2014-10-16","2014-10-17","2014-10-18","2014-10-19","2014-10-20","2014-10-21","2014-10-22","2014-10-23","2014-10-24","2014-10-25","2014-10-26","2014-10-27","2014-10-28","2014-10-29","2014-10-30","2014-10-31","2014-11-01","2014-11-02","2014-11-03","2014-11-04","2014-11-05","2014-11-06","2014-11-07","2014-11-08","2014-11-09","2014-11-10","2014-11-11","2014-11-12","2014-11-13","2014-11-14","2014-11-15","2014-11-16","2014-11-17","2014-11-18","2014-11-19","2014-11-20","2014-11-21","2014-11-22","2014-11-23","2014-11-24","2014-11-25","2014-11-26","2014-11-27","2014-11-28","2014-11-29","2014-11-30","2014-12-01","2014-12-02","2014-12-03","2014-12-04","2014-12-05","2014-12-06","2014-12-07","2014-12-08","2014-12-09","2014-12-10","2014-12-11","2014-12-12","2014-12-13","2014-12-14","2014-12-15","2014-12-16","2014-12-17","2014-12-18","2014-12-19","2014-12-20","2014-12-21","2014-12-22","2014-12-23","2014-12-24","2014-12-25","2014-12-26","2014-12-27","2014-12-28","2014-12-29","2014-12-30","2014-12-31","2015-01-01","2015-01-02","2015-01-03","2015-01-04","2015-01-05","2015-01-06","2015-01-07","2015-01-08","2015-01-09","2015-01-10","2015-01-11","2015-01-12","2015-01-13","2015-01-14","2015-01-15","2015-01-16","2015-01-17","2015-01-18","2015-01-19","2015-01-20","2015-01-21","2015-01-22","2015-01-23","2015-01-24","2015-01-25","2015-01-26","2015-01-27","2015-01-28","2015-01-29","2015-01-30","2015-01-31","2015-02-01","2015-02-02","2015-02-03","2015-02-04","2015-02-05","2015-02-06","2015-02-07","2015-02-08","2015-02-09","2015-02-10","2015-02-11","2015-02-12","2015-02-13","2015-02-14","2015-02-15","2015-02-16","2015-02-17","2015-02-18","2015-02-19","2015-02-20","2015-02-21","2015-02-22","2015-02-23","2015-02-24","2015-02-25","2015-02-26","2015-02-27","2015-02-28","2015-03-01","2015-03-02","2015-03-03","2015-03-04","2015-03-05","2015-03-06","2015-03-07","2015-03-08","2015-03-09","2015-03-10","2015-03-11","2015-03-12","2015-03-13","2015-03-14","2015-03-15","2015-03-16","2015-03-17","2015-03-18","2015-03-19","2015-03-20","2015-03-21","2015-03-22","2015-03-23","2015-03-24","2015-03-25","2015-03-26","2015-03-27","2015-03-28","2015-03-29","2015-03-30","2015-03-31","2015-04-01","2015-04-02","2015-04-03","2015-04-04","2015-04-05","2015-04-06","2015-04-07","2015-04-08","2015-04-09","2015-04-10","2015-04-11","2015-04-12","2015-04-13","2015-04-14","2015-04-15","2015-04-16","2015-04-17","2015-04-18","2015-04-19","2015-04-20","2015-04-21","2015-04-22","2015-04-23","2015-04-24","2015-04-25","2015-04-26","2015-04-27","2015-04-28","2015-04-29","2015-04-30","2015-05-01","2015-05-02","2015-05-03","2015-05-04","2015-05-05","2015-05-06","2015-05-07","2015-05-08","2015-05-09","2015-05-10","2015-05-11","2015-05-12","2015-05-13","2015-05-14","2015-05-15","2015-05-16","2015-05-17","2015-05-18","2015-05-19","2015-05-20","2015-05-21","2015-05-22","2015-05-23","2015-05-24","2015-05-25","2015-05-26","2015-05-27","2015-05-28","2015-05-29","2015-05-30","2015-05-31","2015-06-01","2015-06-02","2015-06-03","2015-06-04","2015-06-05","2015-06-06","2015-06-07","2015-06-08","2015-06-09","2015-06-10","2015-06-11","2015-06-12","2015-06-13","2015-06-14","2015-06-15","2015-06-16","2015-06-17","2015-06-18","2015-06-19","2015-06-20","2015-06-21","2015-06-22","2015-06-23","2015-06-24","2015-06-25","2015-06-26","2015-06-27","2015-06-28","2015-06-29","2015-06-30","2015-07-01","2015-07-02","2015-07-03","2015-07-04","2015-07-05","2015-07-06","2015-07-07","2015-07-08","2015-07-09","2015-07-10","2015-07-11","2015-07-12","2015-07-13","2015-07-14","2015-07-15","2015-07-16","2015-07-17","2015-07-18","2015-07-19","2015-07-20","2015-07-21","2015-07-22","2015-07-23","2015-07-24","2015-07-25","2015-07-26","2015-07-27","2015-07-28","2015-07-29","2015-07-30","2015-07-31","2015-08-01","2015-08-02","2015-08-03","2015-08-04","2015-08-05","2015-08-06","2015-08-07","2015-08-08","2015-08-09","2015-08-10","2015-08-11","2015-08-12","2015-08-13","2015-08-14","2015-08-15","2015-08-16","2015-08-17","2015-08-18","2015-08-19","2015-08-20","2015-08-21","2015-08-22","2015-08-23","2015-08-24","2015-08-25","2015-08-26","2015-08-27","2015-08-28","2015-08-29","2015-08-30","2015-08-31","2015-09-01","2015-09-02","2015-09-03","2015-09-04","2015-09-05","2015-09-06","2015-09-07","2015-09-08","2015-09-09","2015-09-10","2015-09-11","2015-09-12","2015-09-13","2015-09-14","2015-09-15","2015-09-16","2015-09-17","2015-09-18","2015-09-19","2015-09-20","2015-09-21","2015-09-22","2015-09-23","2015-09-24","2015-09-25","2015-09-26","2015-09-27","2015-09-28","2015-09-29","2015-09-30","2015-10-01","2015-10-02","2015-10-03","2015-10-04","2015-10-05","2015-10-06","2015-10-07","2015-10-08","2015-10-09","2015-10-10","2015-10-11","2015-10-12","2015-10-13","2015-10-14","2015-10-15","2015-10-16","2015-10-17","2015-10-18","2015-10-19","2015-10-20","2015-10-21","2015-10-22","2015-10-23","2015-10-24","2015-10-25","2015-10-26","2015-10-27","2015-10-28","2015-10-29","2015-10-30","2015-10-31","2015-11-01","2015-11-02","2015-11-03","2015-11-04","2015-11-05","2015-11-06","2015-11-07","2015-11-08","2015-11-09","2015-11-10","2015-11-11","2015-11-12","2015-11-13","2015-11-14","2015-11-15","2015-11-16","2015-11-17","2015-11-18","2015-11-19","2015-11-20","2015-11-21","2015-11-22","2015-11-23","2015-11-24","2015-11-25","2015-11-26","2015-11-27","2015-11-28","2015-11-29","2015-11-30","2015-12-01","2015-12-02","2015-12-03","2015-12-04","2015-12-05","2015-12-06","2015-12-07","2015-12-08","2015-12-09","2015-12-10","2015-12-11","2015-12-12","2015-12-13","2015-12-14","2015-12-15","2015-12-16","2015-12-17","2015-12-18","2015-12-19","2015-12-20","2015-12-21","2015-12-22","2015-12-23","2015-12-24","2015-12-25","2015-12-26","2015-12-27","2015-12-28","2015-12-29","2015-12-30","2015-12-31","2016-01-01","2016-01-02","2016-01-03","2016-01-04","2016-01-05","2016-01-06","2016-01-07","2016-01-08","2016-01-09","2016-01-10","2016-01-11","2016-01-12","2016-01-13","2016-01-14","2016-01-15","2016-01-16","2016-01-17","2016-01-18","2016-01-19","2016-01-20","2016-01-21","2016-01-22","2016-01-23","2016-01-24","2016-01-25","2016-01-26","2016-01-27","2016-01-28","2016-01-29","2016-01-30","2016-01-31","2016-02-01","2016-02-02","2016-02-03","2016-02-04","2016-02-05","2016-02-06","2016-02-07","2016-02-08","2016-02-09","2016-02-10","2016-02-11","2016-02-12","2016-02-13","2016-02-14","2016-02-15","2016-02-16","2016-02-17","2016-02-18","2016-02-19","2016-02-20","2016-02-21","2016-02-22","2016-02-23","2016-02-24","2016-02-25","2016-02-26","2016-02-27","2016-02-28","2016-02-29","2016-03-01","2016-03-02","2016-03-03","2016-03-04","2016-03-05","2016-03-06","2016-03-07","2016-03-08","2016-03-09","2016-03-10","2016-03-11","2016-03-12","2016-03-13","2016-03-14","2016-03-15","2016-03-16","2016-03-17","2016-03-18","2016-03-19","2016-03-20","2016-03-21","2016-03-22","2016-03-23","2016-03-24","2016-03-25","2016-03-26","2016-03-27","2016-03-28","2016-03-29","2016-03-30","2016-03-31","2016-04-01","2016-04-02","2016-04-03","2016-04-04","2016-04-05","2016-04-06","2016-04-07","2016-04-08","2016-04-09","2016-04-10","2016-04-11","2016-04-12","2016-04-13","2016-04-14","2016-04-15","2016-04-16","2016-04-17","2016-04-18","2016-04-19","2016-04-20","2016-04-21","2016-04-22","2016-04-23","2016-04-24","2016-04-25","2016-04-26","2016-04-27","2016-04-28","2016-04-29","2016-04-30","2016-05-01","2016-05-02","2016-05-03","2016-05-04","2016-05-05","2016-05-06","2016-05-07","2016-05-08","2016-05-09","2016-05-10","2016-05-11","2016-05-12","2016-05-13","2016-05-14","2016-05-15","2016-05-16","2016-05-17","2016-05-18","2016-05-19","2016-05-20","2016-05-21","2016-05-22","2016-05-23","2016-05-24","2016-05-25","2016-05-26","2016-05-27","2016-05-28","2016-05-29","2016-05-30","2016-05-31","2016-06-01","2016-06-02","2016-06-03","2016-06-04","2016-06-05","2016-06-06","2016-06-07","2016-06-08","2016-06-09","2016-06-10","2016-06-11","2016-06-12","2016-06-13","2016-06-14","2016-06-15","2016-06-16","2016-06-17","2016-06-18","2016-06-19","2016-06-20","2016-06-21","2016-06-22","2016-06-23","2016-06-24","2016-06-25","2016-06-26","2016-06-27","2016-06-28","2016-06-29","2016-06-30","2016-07-01","2016-07-02","2016-07-03","2016-07-04","2016-07-05","2016-07-06","2016-07-07","2016-07-08","2016-07-09","2016-07-10","2016-07-11","2016-07-12","2016-07-13","2016-07-14","2016-07-15","2016-07-16","2016-07-17","2016-07-18","2016-07-19","2016-07-20","2016-07-21","2016-07-22","2016-07-23","2016-07-24","2016-07-25","2016-07-26","2016-07-27","2016-07-28","2016-07-29","2016-07-30","2016-07-31","2016-08-01","2016-08-02","2016-08-03","2016-08-04","2016-08-05","2016-08-06","2016-08-07","2016-08-08","2016-08-09","2016-08-10","2016-08-11","2016-08-12","2016-08-13","2016-08-14","2016-08-15","2016-08-16","2016-08-17","2016-08-18","2016-08-19","2016-08-20","2016-08-21","2016-08-22","2016-08-23","2016-08-24","2016-08-25","2016-08-26","2016-08-27","2016-08-28","2016-08-29","2016-08-30","2016-08-31","2016-09-01","2016-09-02","2016-09-03","2016-09-04","2016-09-05","2016-09-06","2016-09-07","2016-09-08","2016-09-09","2016-09-10","2016-09-11","2016-09-12","2016-09-13","2016-09-14","2016-09-15","2016-09-16","2016-09-17","2016-09-18","2016-09-19","2016-09-20","2016-09-21","2016-09-22","2016-09-23","2016-09-24","2016-09-25","2016-09-26","2016-09-27","2016-09-28","2016-09-29","2016-09-30","2016-10-01","2016-10-02","2016-10-03","2016-10-04","2016-10-05","2016-10-06","2016-10-07","2016-10-08","2016-10-09","2016-10-10","2016-10-11","2016-10-12","2016-10-13","2016-10-14","2016-10-15","2016-10-16","2016-10-17","2016-10-18","2016-10-19","2016-10-20","2016-10-21","2016-10-22","2016-10-23","2016-10-24","2016-10-25","2016-10-26","2016-10-27","2016-10-28","2016-10-29","2016-10-30","2016-10-31","2016-11-01","2016-11-02","2016-11-03","2016-11-04","2016-11-05","2016-11-06","2016-11-07","2016-11-08","2016-11-09","2016-11-10","2016-11-11","2016-11-12","2016-11-13","2016-11-14","2016-11-15","2016-11-16","2016-11-17","2016-11-18","2016-11-19","2016-11-20","2016-11-21","2016-11-22","2016-11-23","2016-11-24","2016-11-25","2016-11-26","2016-11-27","2016-11-28","2016-11-29","2016-11-30","2016-12-01","2016-12-02","2016-12-03","2016-12-04","2016-12-05","2016-12-06","2016-12-07","2016-12-08","2016-12-09","2016-12-10","2016-12-11","2016-12-12","2016-12-13","2016-12-14","2016-12-15","2016-12-16","2016-12-17","2016-12-18","2016-12-19","2016-12-20","2016-12-21","2016-12-22","2016-12-23","2016-12-24","2016-12-25","2016-12-26","2016-12-27","2016-12-28","2016-12-29","2016-12-30","2016-12-31","2017-01-01","2017-01-02","2017-01-03","2017-01-04","2017-01-05","2017-01-06","2017-01-07","2017-01-08","2017-01-09","2017-01-10","2017-01-11","2017-01-12","2017-01-13","2017-01-14","2017-01-15","2017-01-16","2017-01-17","2017-01-18","2017-01-19","2017-01-20","2017-01-21","2017-01-22","2017-01-23","2017-01-24","2017-01-25","2017-01-26","2017-01-27","2017-01-28","2017-01-29","2017-01-30","2017-01-31","2017-02-01","2017-02-02","2017-02-03","2017-02-04","2017-02-05","2017-02-06","2017-02-07","2017-02-08","2017-02-09","2017-02-10","2017-02-11","2017-02-12","2017-02-13","2017-02-14","2017-02-15","2017-02-16","2017-02-17","2017-02-18","2017-02-19","2017-02-20","2017-02-21","2017-02-22","2017-02-23","2017-02-24","2017-02-25","2017-02-26","2017-02-27","2017-02-28","2017-03-01","2017-03-02","2017-03-03","2017-03-04","2017-03-05","2017-03-06","2017-03-07","2017-03-08","2017-03-09","2017-03-10","2017-03-11","2017-03-12","2017-03-13","2017-03-14","2017-03-15","2017-03-16","2017-03-17","2017-03-18","2017-03-19","2017-03-20","2017-03-21","2017-03-22","2017-03-23","2017-03-24","2017-03-25","2017-03-26","2017-03-27","2017-03-28","2017-03-29","2017-03-30","2017-03-31","2017-04-01","2017-04-02","2017-04-03","2017-04-04","2017-04-05","2017-04-06","2017-04-07","2017-04-08","2017-04-09","2017-04-10","2017-04-11","2017-04-12","2017-04-13","2017-04-14","2017-04-15","2017-04-16","2017-04-17","2017-04-18","2017-04-19","2017-04-20","2017-04-21","2017-04-22","2017-04-23","2017-04-24","2017-04-25","2017-04-26","2017-04-27","2017-04-28","2017-04-29","2017-04-30","2017-05-01","2017-05-02","2017-05-03","2017-05-04","2017-05-05","2017-05-06","2017-05-07","2017-05-08","2017-05-09","2017-05-10","2017-05-11","2017-05-12","2017-05-13","2017-05-14","2017-05-15","2017-05-16","2017-05-17","2017-05-18","2017-05-19","2017-05-20","2017-05-21","2017-05-22","2017-05-23","2017-05-24","2017-05-25","2017-05-26","2017-05-27","2017-05-28","2017-05-29","2017-05-30","2017-05-31","2017-06-01","2017-06-02","2017-06-03","2017-06-04","2017-06-05","2017-06-06","2017-06-07","2017-06-08","2017-06-09","2017-06-10","2017-06-11","2017-06-12","2017-06-13","2017-06-14","2017-06-15","2017-06-16","2017-06-17","2017-06-18","2017-06-19","2017-06-20","2017-06-21","2017-06-22","2017-06-23","2017-06-24","2017-06-25","2017-06-26","2017-06-27","2017-06-28","2017-06-29","2017-06-30","2017-07-01","2017-07-02","2017-07-03","2017-07-04","2017-07-05","2017-07-06","2017-07-07","2017-07-08","2017-07-09","2017-07-10","2017-07-11","2017-07-12","2017-07-13","2017-07-14","2017-07-15","2017-07-16","2017-07-17","2017-07-18","2017-07-19","2017-07-20","2017-07-21","2017-07-22","2017-07-23","2017-07-24","2017-07-25","2017-07-26","2017-07-27","2017-07-28","2017-07-29","2017-07-30","2017-07-31","2017-08-01","2017-08-02","2017-08-03","2017-08-04","2017-08-05","2017-08-06","2017-08-07","2017-08-08","2017-08-09","2017-08-10","2017-08-11","2017-08-12","2017-08-13","2017-08-14","2017-08-15","2017-08-16","2017-08-17","2017-08-18","2017-08-19","2017-08-20","2017-08-21","2017-08-22","2017-08-23","2017-08-24","2017-08-25","2017-08-26","2017-08-27","2017-08-28","2017-08-29","2017-08-30","2017-08-31","2017-09-01","2017-09-02","2017-09-03","2017-09-04","2017-09-05","2017-09-06","2017-09-07","2017-09-08","2017-09-09","2017-09-10","2017-09-11","2017-09-12","2017-09-13","2017-09-14","2017-09-15","2017-09-16","2017-09-17","2017-09-18","2017-09-19","2017-09-20","2017-09-21","2017-09-22","2017-09-23","2017-09-24","2017-09-25","2017-09-26","2017-09-27","2017-09-28","2017-09-29","2017-09-30","2017-10-01","2017-10-02","2017-10-03","2017-10-04","2017-10-05","2017-10-06","2017-10-07","2017-10-08","2017-10-09","2017-10-10","2017-10-11","2017-10-12","2017-10-13","2017-10-14","2017-10-15","2017-10-16","2017-10-17","2017-10-18","2017-10-19","2017-10-20","2017-10-21","2017-10-22","2017-10-23","2017-10-24","2017-10-25","2017-10-26","2017-10-27","2017-10-28","2017-10-29","2017-10-30","2017-10-31","2017-11-01","2017-11-02","2017-11-03","2017-11-04","2017-11-05","2017-11-06","2017-11-07","2017-11-08","2017-11-09","2017-11-10","2017-11-11","2017-11-12","2017-11-13","2017-11-14","2017-11-15","2017-11-16","2017-11-17","2017-11-18","2017-11-19","2017-11-20","2017-11-21","2017-11-22","2017-11-23","2017-11-24","2017-11-25","2017-11-26","2017-11-27","2017-11-28","2017-11-29","2017-11-30","2017-12-01","2017-12-02","2017-12-03","2017-12-04","2017-12-05","2017-12-06","2017-12-07","2017-12-08","2017-12-09","2017-12-10","2017-12-11","2017-12-12","2017-12-13","2017-12-14","2017-12-15","2017-12-16","2017-12-17","2017-12-18","2017-12-19","2017-12-20","2017-12-21","2017-12-22","2017-12-23","2017-12-24","2017-12-25","2017-12-26","2017-12-27","2017-12-28","2017-12-29","2017-12-30","2017-12-31","2018-01-01","2018-01-02","2018-01-03","2018-01-04","2018-01-05","2018-01-06","2018-01-07","2018-01-08","2018-01-09","2018-01-10","2018-01-11","2018-01-12","2018-01-13","2018-01-14","2018-01-15","2018-01-16","2018-01-17","2018-01-18","2018-01-19","2018-01-20","2018-01-21","2018-01-22","2018-01-23","2018-01-24","2018-01-25","2018-01-26","2018-01-27","2018-01-28","2018-01-29","2018-01-30","2018-01-31","2018-02-01","2018-02-02","2018-02-03","2018-02-04","2018-02-05","2018-02-06","2018-02-07","2018-02-08","2018-02-09","2018-02-10","2018-02-11","2018-02-12","2018-02-13","2018-02-14","2018-02-15","2018-02-16","2018-02-17","2018-02-18","2018-02-19","2018-02-20","2018-02-21","2018-02-22","2018-02-23","2018-02-24","2018-02-25","2018-02-26","2018-02-27","2018-02-28","2018-03-01","2018-03-02","2018-03-03","2018-03-04","2018-03-05","2018-03-06","2018-03-07","2018-03-08","2018-03-09","2018-03-10","2018-03-11","2018-03-12","2018-03-13","2018-03-14","2018-03-15","2018-03-16","2018-03-17","2018-03-18","2018-03-19","2018-03-20","2018-03-21","2018-03-22","2018-03-23","2018-03-24","2018-03-25","2018-03-26","2018-03-27","2018-03-28","2018-03-29","2018-03-30","2018-03-31","2018-04-01","2018-04-02","2018-04-03","2018-04-04","2018-04-05","2018-04-06","2018-04-07","2018-04-08","2018-04-09","2018-04-10","2018-04-11","2018-04-12","2018-04-13","2018-04-14","2018-04-15","2018-04-16","2018-04-17","2018-04-18","2018-04-19","2018-04-20","2018-04-21","2018-04-22","2018-04-23","2018-04-24","2018-04-25","2018-04-26","2018-04-27","2018-04-28","2018-04-29","2018-04-30","2018-05-01","2018-05-02","2018-05-03","2018-05-04","2018-05-05","2018-05-06","2018-05-07","2018-05-08","2018-05-09","2018-05-10","2018-05-11","2018-05-12","2018-05-13","2018-05-14","2018-05-15","2018-05-16","2018-05-17","2018-05-18","2018-05-19","2018-05-20","2018-05-21","2018-05-22","2018-05-23","2018-05-24","2018-05-25","2018-05-26","2018-05-27","2018-05-28","2018-05-29","2018-05-30","2018-05-31","2018-06-01","2018-06-02","2018-06-03","2018-06-04","2018-06-05","2018-06-06","2018-06-07","2018-06-08","2018-06-09","2018-06-10","2018-06-11","2018-06-12","2018-06-13","2018-06-14","2018-06-15","2018-06-16","2018-06-17","2018-06-18","2018-06-19","2018-06-20","2018-06-21","2018-06-22","2018-06-23","2018-06-24","2018-06-25","2018-06-26","2018-06-27","2018-06-28","2018-06-29","2018-06-30","2018-07-01","2018-07-02","2018-07-03","2018-07-04","2018-07-05","2018-07-06","2018-07-07","2018-07-08","2018-07-09","2018-07-10","2018-07-11","2018-07-12","2018-07-13","2018-07-14","2018-07-15","2018-07-16","2018-07-17","2018-07-18","2018-07-19","2018-07-20","2018-07-21","2018-07-22","2018-07-23","2018-07-24","2018-07-25","2018-07-26","2018-07-27","2018-07-28","2018-07-29","2018-07-30","2018-07-31","2018-08-01","2018-08-02","2018-08-03","2018-08-04","2018-08-05","2018-08-06","2018-08-07","2018-08-08","2018-08-09","2018-08-10","2018-08-11","2018-08-12","2018-08-13","2018-08-14","2018-08-15","2018-08-16","2018-08-17","2018-08-18","2018-08-19","2018-08-20","2018-08-21","2018-08-22","2018-08-23","2018-08-24","2018-08-25","2018-08-26","2018-08-27","2018-08-28","2018-08-29","2018-08-30","2018-08-31","2018-09-01","2018-09-02","2018-09-03","2018-09-04","2018-09-05","2018-09-06","2018-09-07","2018-09-08","2018-09-09","2018-09-10","2018-09-11","2018-09-12","2018-09-13","2018-09-14","2018-09-15","2018-09-16","2018-09-17","2018-09-18","2018-09-19","2018-09-20","2018-09-21","2018-09-22","2018-09-23","2018-09-24","2018-09-25","2018-09-26","2018-09-27","2018-09-28","2018-09-29","2018-09-30","2018-10-01","2018-10-02","2018-10-03","2018-10-04","2018-10-05","2018-10-06","2018-10-07","2018-10-08","2018-10-09","2018-10-10","2018-10-11","2018-10-12","2018-10-13","2018-10-14","2018-10-15","2018-10-16","2018-10-17","2018-10-18","2018-10-19","2018-10-20","2018-10-21","2018-10-22","2018-10-23","2018-10-24","2018-10-25","2018-10-26","2018-10-27","2018-10-28","2018-10-29","2018-10-30","2018-10-31","2018-11-01","2018-11-02","2018-11-03","2018-11-04","2018-11-05","2018-11-06","2018-11-07","2018-11-08","2018-11-09","2018-11-10","2018-11-11","2018-11-12","2018-11-13","2018-11-14","2018-11-15","2018-11-16","2018-11-17","2018-11-18","2018-11-19","2018-11-20","2018-11-21","2018-11-22","2018-11-23","2018-11-24","2018-11-25","2018-11-26","2018-11-27","2018-11-28","2018-11-29","2018-11-30","2018-12-01","2018-12-02","2018-12-03","2018-12-04","2018-12-05","2018-12-06","2018-12-07","2018-12-08","2018-12-09","2018-12-10","2018-12-11","2018-12-12","2018-12-13","2018-12-14","2018-12-15","2018-12-16","2018-12-17","2018-12-18","2018-12-19","2018-12-20","2018-12-21","2018-12-22","2018-12-23","2018-12-24","2018-12-25","2018-12-26","2018-12-27","2018-12-28","2018-12-29","2018-12-30","2018-12-31","2019-01-01","2019-01-02","2019-01-03","2019-01-04","2019-01-05","2019-01-06","2019-01-07","2019-01-08","2019-01-09","2019-01-10","2019-01-11","2019-01-12","2019-01-13","2019-01-14","2019-01-15","2019-01-16","2019-01-17","2019-01-18","2019-01-19","2019-01-20","2019-01-21","2019-01-22","2019-01-23","2019-01-24","2019-01-25","2019-01-26","2019-01-27","2019-01-28","2019-01-29","2019-01-30","2019-01-31","2019-02-01","2019-02-02","2019-02-03","2019-02-04","2019-02-05","2019-02-06","2019-02-07","2019-02-08","2019-02-09","2019-02-10","2019-02-11","2019-02-12","2019-02-13","2019-02-14","2019-02-15","2019-02-16","2019-02-17","2019-02-18","2019-02-19","2019-02-20","2019-02-21","2019-02-22","2019-02-23","2019-02-24","2019-02-25","2019-02-26","2019-02-27","2019-02-28","2019-03-01","2019-03-02","2019-03-03","2019-03-04","2019-03-05","2019-03-06","2019-03-07","2019-03-08","2019-03-09","2019-03-10","2019-03-11","2019-03-12","2019-03-13","2019-03-14","2019-03-15","2019-03-16","2019-03-17","2019-03-18","2019-03-19","2019-03-20","2019-03-21","2019-03-22","2019-03-23","2019-03-24","2019-03-25","2019-03-26","2019-03-27","2019-03-28","2019-03-29","2019-03-30","2019-03-31","2019-04-01","2019-04-02","2019-04-03","2019-04-04","2019-04-05","2019-04-06","2019-04-07","2019-04-08","2019-04-09","2019-04-10","2019-04-11","2019-04-12","2019-04-13","2019-04-14","2019-04-15","2019-04-16","2019-04-17","2019-04-18","2019-04-19","2019-04-20","2019-04-21","2019-04-22","2019-04-23","2019-04-24","2019-04-25","2019-04-26","2019-04-27","2019-04-28","2019-04-29","2019-04-30","2019-05-01","2019-05-02","2019-05-03","2019-05-04","2019-05-05","2019-05-06","2019-05-07","2019-05-08","2019-05-09","2019-05-10","2019-05-11","2019-05-12","2019-05-13","2019-05-14","2019-05-15","2019-05-16","2019-05-17","2019-05-18","2019-05-19","2019-05-20","2019-05-21","2019-05-22","2019-05-23","2019-05-24","2019-05-25","2019-05-26","2019-05-27","2019-05-28","2019-05-29","2019-05-30","2019-05-31","2019-06-01","2019-06-02","2019-06-03","2019-06-04","2019-06-05","2019-06-06","2019-06-07","2019-06-08","2019-06-09","2019-06-10","2019-06-11","2019-06-12","2019-06-13","2019-06-14","2019-06-15","2019-06-16","2019-06-17","2019-06-18","2019-06-19","2019-06-20","2019-06-21","2019-06-22","2019-06-23","2019-06-24","2019-06-25","2019-06-26","2019-06-27","2019-06-28","2019-06-29","2019-06-30","2019-07-01","2019-07-02","2019-07-03","2019-07-04","2019-07-05","2019-07-06","2019-07-07","2019-07-08","2019-07-09","2019-07-10","2019-07-11","2019-07-12","2019-07-13","2019-07-14","2019-07-15","2019-07-16","2019-07-17","2019-07-18","2019-07-19","2019-07-20","2019-07-21","2019-07-22","2019-07-23","2019-07-24","2019-07-25","2019-07-26","2019-07-27","2019-07-28","2019-07-29","2019-07-30","2019-07-31","2019-08-01","2019-08-02","2019-08-03","2019-08-04","2019-08-05","2019-08-06","2019-08-07","2019-08-08","2019-08-09","2019-08-10","2019-08-11","2019-08-12","2019-08-13","2019-08-14","2019-08-15","2019-08-16","2019-08-17","2019-08-18","2019-08-19","2019-08-20","2019-08-21","2019-08-22","2019-08-23","2019-08-24","2019-08-25","2019-08-26","2019-08-27","2019-08-28","2019-08-29","2019-08-30","2019-08-31","2019-09-01","2019-09-02","2019-09-03","2019-09-04","2019-09-05","2019-09-06","2019-09-07","2019-09-08","2019-09-09","2019-09-10","2019-09-11","2019-09-12","2019-09-13","2019-09-14","2019-09-15","2019-09-16","2019-09-17","2019-09-18","2019-09-19","2019-09-20","2019-09-21","2019-09-22","2019-09-23","2019-09-24","2019-09-25","2019-09-26","2019-09-27","2019-09-28","2019-09-29","2019-09-30","2019-10-01","2019-10-02","2019-10-03","2019-10-04","2019-10-05","2019-10-06","2019-10-07","2019-10-08","2019-10-09","2019-10-10","2019-10-11","2019-10-12","2019-10-13","2019-10-14","2019-10-15","2019-10-16","2019-10-17","2019-10-18","2019-10-19","2019-10-20","2019-10-21","2019-10-22","2019-10-23","2019-10-24","2019-10-25","2019-10-26","2019-10-27","2019-10-28","2019-10-29","2019-10-30","2019-10-31","2019-11-01","2019-11-02","2019-11-03","2019-11-04","2019-11-05","2019-11-06","2019-11-07","2019-11-08","2019-11-09","2019-11-10","2019-11-11","2019-11-12","2019-11-13","2019-11-14","2019-11-15","2019-11-16","2019-11-17","2019-11-18","2019-11-19","2019-11-20","2019-11-21","2019-11-22","2019-11-23","2019-11-24","2019-11-25","2019-11-26","2019-11-27","2019-11-28","2019-11-29","2019-11-30","2019-12-01","2019-12-02","2019-12-03","2019-12-04","2019-12-05","2019-12-06","2019-12-07","2019-12-08","2019-12-09","2019-12-10","2019-12-11","2019-12-12","2019-12-13","2019-12-14","2019-12-15","2019-12-16","2019-12-17","2019-12-18","2019-12-19","2019-12-20","2019-12-21","2019-12-22","2019-12-23","2019-12-24","2019-12-25","2019-12-26","2019-12-27","2019-12-28","2019-12-29","2019-12-30","2019-12-31","2020-01-01","2020-01-02","2020-01-03","2020-01-04","2020-01-05","2020-01-06","2020-01-07","2020-01-08","2020-01-09","2020-01-10","2020-01-11","2020-01-12","2020-01-13","2020-01-14","2020-01-15","2020-01-16","2020-01-17","2020-01-18","2020-01-19","2020-01-20","2020-01-21","2020-01-22","2020-01-23","2020-01-24","2020-01-25","2020-01-26","2020-01-27","2020-01-28","2020-01-29","2020-01-30","2020-01-31","2020-02-01","2020-02-02","2020-02-03","2020-02-04","2020-02-05","2020-02-06","2020-02-07","2020-02-08","2020-02-09","2020-02-10","2020-02-11","2020-02-12","2020-02-13","2020-02-14","2020-02-15","2020-02-16","2020-02-17","2020-02-18","2020-02-19","2020-02-20","2020-02-21","2020-02-22","2020-02-23","2020-02-24","2020-02-25","2020-02-26","2020-02-27","2020-02-28","2020-02-29","2020-03-01","2020-03-02","2020-03-03","2020-03-04","2020-03-05","2020-03-06","2020-03-07","2020-03-08","2020-03-09","2020-03-10","2020-03-11","2020-03-12","2020-03-13","2020-03-14","2020-03-15","2020-03-16","2020-03-17","2020-03-18","2020-03-19","2020-03-20","2020-03-21","2020-03-22","2020-03-23","2020-03-24","2020-03-25","2020-03-26","2020-03-27","2020-03-28","2020-03-29","2020-03-30","2020-03-31","2020-04-01","2020-04-02","2020-04-03","2020-04-04","2020-04-05","2020-04-06","2020-04-07","2020-04-08","2020-04-09","2020-04-10","2020-04-11","2020-04-12","2020-04-13","2020-04-14","2020-04-15","2020-04-16","2020-04-17","2020-04-18","2020-04-19","2020-04-20","2020-04-21","2020-04-22","2020-04-23","2020-04-24","2020-04-25","2020-04-26","2020-04-27","2020-04-28","2020-04-29","2020-04-30","2020-05-01","2020-05-02","2020-05-03","2020-05-04","2020-05-05","2020-05-06","2020-05-07","2020-05-08","2020-05-09","2020-05-10","2020-05-11","2020-05-12","2020-05-13","2020-05-14","2020-05-15","2020-05-16","2020-05-17","2020-05-18","2020-05-19","2020-05-20","2020-05-21","2020-05-22","2020-05-23","2020-05-24","2020-05-25","2020-05-26","2020-05-27","2020-05-28","2020-05-29","2020-05-30","2020-05-31","2020-06-01","2020-06-02","2020-06-03","2020-06-04","2020-06-05","2020-06-06","2020-06-07","2020-06-08","2020-06-09","2020-06-10","2020-06-11","2020-06-12","2020-06-13","2020-06-14","2020-06-15","2020-06-16","2020-06-17","2020-06-18","2020-06-19","2020-06-20","2020-06-21","2020-06-22","2020-06-23","2020-06-24","2020-06-25","2020-06-26","2020-06-27","2020-06-28","2020-06-29","2020-06-30","2020-07-01","2020-07-02","2020-07-03","2020-07-04","2020-07-05","2020-07-06","2020-07-07","2020-07-08","2020-07-09","2020-07-10","2020-07-11","2020-07-12","2020-07-13","2020-07-14","2020-07-15","2020-07-16","2020-07-17","2020-07-18","2020-07-19","2020-07-20","2020-07-21","2020-07-22","2020-07-23","2020-07-24","2020-07-25","2020-07-26","2020-07-27","2020-07-28","2020-07-29","2020-07-30","2020-07-31","2020-08-01","2020-08-02","2020-08-03","2020-08-04","2020-08-05","2020-08-06","2020-08-07","2020-08-08","2020-08-09","2020-08-10","2020-08-11","2020-08-12","2020-08-13","2020-08-14","2020-08-15","2020-08-16","2020-08-17","2020-08-18","2020-08-19","2020-08-20","2020-08-21","2020-08-22","2020-08-23","2020-08-24","2020-08-25","2020-08-26","2020-08-27","2020-08-28","2020-08-29","2020-08-30","2020-08-31","2020-09-01","2020-09-02","2020-09-03","2020-09-04","2020-09-05","2020-09-06","2020-09-07","2020-09-08","2020-09-09","2020-09-10","2020-09-11","2020-09-12","2020-09-13","2020-09-14","2020-09-15","2020-09-16","2020-09-17","2020-09-18","2020-09-19","2020-09-20","2020-09-21","2020-09-22","2020-09-23","2020-09-24","2020-09-25","2020-09-26","2020-09-27","2020-09-28","2020-09-29","2020-09-30","2020-10-01","2020-10-02","2020-10-03","2020-10-04","2020-10-05","2020-10-06","2020-10-07","2020-10-08","2020-10-09","2020-10-10","2020-10-11","2020-10-12","2020-10-13","2020-10-14","2020-10-15","2020-10-16","2020-10-17","2020-10-18","2020-10-19","2020-10-20","2020-10-21","2020-10-22","2020-10-23","2020-10-24","2020-10-25","2020-10-26","2020-10-27","2020-10-28","2020-10-29","2020-10-30","2020-10-31","2020-11-01","2020-11-02","2020-11-03","2020-11-04","2020-11-05","2020-11-06","2020-11-07","2020-11-08","2020-11-09","2020-11-10","2020-11-11","2020-11-12","2020-11-13","2020-11-14","2020-11-15","2020-11-16","2020-11-17","2020-11-18","2020-11-19","2020-11-20","2020-11-21","2020-11-22","2020-11-23","2020-11-24","2020-11-25","2020-11-26","2020-11-27","2020-11-28","2020-11-29","2020-11-30","2020-12-01","2020-12-02","2020-12-03","2020-12-04","2020-12-05","2020-12-06","2020-12-07","2020-12-08","2020-12-09","2020-12-10","2020-12-11","2020-12-12","2020-12-13","2020-12-14","2020-12-15","2020-12-16","2020-12-17","2020-12-18","2020-12-19","2020-12-20","2020-12-21","2020-12-22","2020-12-23","2020-12-24","2020-12-25","2020-12-26","2020-12-27","2020-12-28","2020-12-29","2020-12-30","2020-12-31","2021-01-01","2021-01-02","2021-01-03","2021-01-04","2021-01-05","2021-01-06","2021-01-07","2021-01-08","2021-01-09","2021-01-10","2021-01-11"],"y":[0.37247,0.37247,0.37247,0.3724,0.37233,0.37226,0.37221,0.37216,0.37211,0.37207,0.37203,0.372,0.37197,0.37195,0.37193,0.37192,0.37191,0.3719,0.37189,0.37189,0.37188,0.37187,0.37187,0.37187,0.37187,0.37187,0.37187,0.37187,0.37186,0.37186,0.37184,0.37182,0.3718,0.37177,0.37174,0.37172,0.37171,0.37171,0.37173,0.37176,0.37182,0.37188,0.37196,0.37203,0.37211,0.37218,0.37224,0.37228,0.37231,0.37232,0.37232,0.37232,0.37232,0.37232,0.37232,0.37235,0.37239,0.37245,0.37254,0.37264,0.37275,0.37287,0.37298,0.3731,0.3732,0.37329,0.37338,0.37348,0.37358,0.37368,0.37378,0.37386,0.37394,0.37399,0.37403,0.3741,0.37425,0.37442,0.37455,0.37459,0.37449,0.37423,0.37387,0.37344,0.37298,0.37253,0.37212,0.37167,0.3711,0.37045,0.36977,0.36908,0.36844,0.36789,0.36746,0.36719,0.36707,0.36705,0.3671,0.36722,0.3674,0.36762,0.36788,0.36816,0.36844,0.36864,0.36871,0.3687,0.3687,0.36876,0.36896,0.36935,0.37002,0.37101,0.37231,0.37382,0.37554,0.37745,0.37955,0.38184,0.38429,0.38691,0.38969,0.39279,0.39632,0.40017,0.40423,0.4084,0.41256,0.41661,0.42043,0.42393,0.42729,0.43077,0.43428,0.43777,0.44117,0.44441,0.44742,0.45015,0.45252,0.45462,0.45657,0.45834,0.45992,0.46129,0.46243,0.46331,0.46393,0.46426,0.46399,0.46302,0.46164,0.46013,0.45877,0.45784,0.45698,0.45575,0.45435,0.45294,0.45172,0.45087,0.45039,0.45014,0.45006,0.4501,0.4502,0.45032,0.45039,0.45036,0.45019,0.44987,0.44949,0.44904,0.44854,0.44801,0.44745,0.44688,0.44632,0.44577,0.44521,0.44462,0.44401,0.4434,0.44281,0.44226,0.44177,0.44136,0.44104,0.44082,0.44068,0.44058,0.44052,0.44049,0.44045,0.44039,0.44031,0.44017,0.44,0.43982,0.43964,0.43945,0.43927,0.43909,0.43891,0.43874,0.43857,0.43843,0.43832,0.43822,0.43814,0.43805,0.43795,0.43782,0.43766,0.43746,0.43719,0.43683,0.43642,0.43597,0.43551,0.43505,0.43463,0.43427,0.43398,0.43372,0.43342,0.43312,0.43286,0.43267,0.43257,0.43261,0.43277,0.43299,0.43326,0.43354,0.43378,0.43406,0.43447,0.43497,0.4355,0.43602,0.4365,0.43688,0.43714,0.43721,0.4371,0.43682,0.43644,0.43598,0.4355,0.43503,0.43461,0.43429,0.43411,0.43409,0.43419,0.43437,0.43459,0.43481,0.43499,0.43509,0.43507,0.43489,0.43469,0.43459,0.43454,0.43447,0.43431,0.43399,0.43346,0.43265,0.43149,0.42998,0.42818,0.42613,0.42387,0.42144,0.41887,0.41621,0.4135,0.41077,0.40785,0.40461,0.40112,0.39745,0.39369,0.3899,0.38616,0.38256,0.37916,0.37568,0.37187,0.36789,0.36391,0.36007,0.35653,0.35345,0.35099,0.34931,0.34844,0.34822,0.34845,0.34897,0.34957,0.35008,0.35109,0.35305,0.35553,0.35812,0.36041,0.36199,0.36307,0.36414,0.36518,0.36616,0.36706,0.36787,0.36855,0.3691,0.36948,0.36967,0.3697,0.36959,0.36939,0.36913,0.36884,0.36856,0.36833,0.36818,0.36806,0.36789,0.36769,0.36747,0.36725,0.36703,0.36682,0.36665,0.36653,0.36648,0.36652,0.36663,0.36679,0.36699,0.36719,0.36739,0.36757,0.3677,0.36799,0.36858,0.36936,0.37022,0.37104,0.37171,0.37212,0.37217,0.37172,0.37101,0.37029,0.36959,0.3689,0.36824,0.3676,0.36699,0.36641,0.36588,0.36544,0.36514,0.36494,0.36483,0.36479,0.3648,0.36483,0.36487,0.3649,0.36497,0.36511,0.36531,0.36551,0.3657,0.36584,0.36593,0.366,0.36608,0.36615,0.36625,0.36636,0.3665,0.36667,0.36685,0.36704,0.36724,0.36743,0.36761,0.36777,0.36791,0.36805,0.3682,0.36835,0.36851,0.36866,0.36879,0.3689,0.36897,0.369,0.36897,0.36887,0.36871,0.36852,0.36831,0.3681,0.36792,0.36777,0.36768,0.36764,0.36761,0.3676,0.3676,0.36762,0.36765,0.3677,0.36777,0.36785,0.36797,0.36814,0.36834,0.36856,0.36879,0.36901,0.36922,0.36939,0.36952,0.36962,0.3697,0.36977,0.36982,0.36986,0.36988,0.36989,0.36988,0.36986,0.3698,0.36969,0.36955,0.36938,0.36921,0.36906,0.36893,0.36886,0.36885,0.36889,0.36897,0.36908,0.3692,0.36933,0.36947,0.36962,0.36981,0.37003,0.37025,0.37048,0.3707,0.37085,0.37089,0.37088,0.37085,0.37085,0.37091,0.37109,0.37142,0.37195,0.37254,0.3731,0.37367,0.37432,0.37509,0.37607,0.37729,0.37882,0.38072,0.38305,0.3858,0.3889,0.39225,0.3958,0.39945,0.40315,0.4068,0.41033,0.41402,0.41811,0.42245,0.42693,0.43139,0.43572,0.43977,0.44342,0.44652,0.44919,0.4516,0.45378,0.45572,0.45744,0.45895,0.46025,0.46136,0.46228,0.46289,0.46311,0.46302,0.4627,0.46223,0.46167,0.46111,0.46063,0.46029,0.46003,0.45972,0.45938,0.45902,0.45864,0.45826,0.45789,0.45754,0.45721,0.45695,0.45674,0.45654,0.45634,0.45608,0.45574,0.45528,0.45466,0.45385,0.45279,0.45149,0.45,0.44838,0.44671,0.44505,0.44346,0.44199,0.44072,0.43952,0.43824,0.43694,0.43566,0.43446,0.43339,0.4325,0.43183,0.43146,0.43143,0.43175,0.43233,0.4331,0.43397,0.43487,0.43571,0.43643,0.43693,0.43732,0.43775,0.43819,0.43862,0.439,0.43932,0.43955,0.43965,0.43962,0.43938,0.43894,0.43835,0.43766,0.43692,0.43618,0.43549,0.43491,0.43449,0.43419,0.43394,0.43374,0.43357,0.43344,0.43333,0.43324,0.43316,0.43308,0.43305,0.4331,0.4332,0.43332,0.43344,0.43352,0.43353,0.43345,0.43325,0.43285,0.43228,0.43163,0.43097,0.4304,0.43,0.42975,0.42953,0.42933,0.42913,0.42893,0.42869,0.42845,0.42823,0.42803,0.42785,0.42768,0.42752,0.42737,0.42723,0.42709,0.42696,0.42681,0.42664,0.42647,0.42628,0.42607,0.42585,0.42561,0.42536,0.42519,0.42517,0.42524,0.42537,0.42548,0.42552,0.42545,0.42521,0.42474,0.42419,0.42371,0.42322,0.42266,0.42197,0.42109,0.41995,0.41849,0.41665,0.41424,0.41124,0.40778,0.40399,0.4,0.39595,0.39197,0.3882,0.38478,0.38133,0.37754,0.37356,0.36957,0.36572,0.36217,0.35911,0.35668,0.35505,0.35435,0.35447,0.35524,0.3565,0.35807,0.35978,0.36146,0.36294,0.36405,0.36519,0.36671,0.3684,0.37004,0.37142,0.37232,0.37271,0.37278,0.37266,0.37244,0.37226,0.37221,0.37222,0.37211,0.37192,0.37167,0.3714,0.37112,0.37087,0.37068,0.37056,0.37052,0.37051,0.37053,0.37055,0.37058,0.3706,0.3706,0.37058,0.37051,0.3704,0.37028,0.37014,0.36998,0.36981,0.36964,0.36946,0.36927,0.36909,0.36888,0.36862,0.36833,0.36802,0.3677,0.36738,0.36708,0.36682,0.36659,0.36639,0.36617,0.36596,0.36576,0.36559,0.36546,0.36539,0.36538,0.36547,0.36565,0.3659,0.3662,0.36653,0.36686,0.36717,0.36743,0.36764,0.36779,0.36793,0.36806,0.36817,0.36826,0.36834,0.36839,0.36841,0.36841,0.36836,0.36823,0.36808,0.36791,0.36778,0.3677,0.36769,0.36772,0.36776,0.36781,0.36785,0.36785,0.36783,0.36781,0.36779,0.36777,0.36775,0.36772,0.36768,0.36764,0.36758,0.36747,0.36731,0.36711,0.36689,0.36667,0.36646,0.36628,0.36616,0.3661,0.36611,0.36616,0.36625,0.36636,0.36651,0.36668,0.36687,0.36708,0.36731,0.36758,0.36792,0.3683,0.36872,0.36916,0.3696,0.37002,0.37041,0.37075,0.37104,0.37131,0.37155,0.37176,0.37195,0.37212,0.37227,0.3724,0.37252,0.3726,0.37265,0.37268,0.3727,0.37272,0.37276,0.37282,0.37292,0.37307,0.37328,0.37353,0.37381,0.37411,0.37442,0.37472,0.375,0.37526,0.37548,0.37558,0.37553,0.37539,0.37521,0.37503,0.37491,0.37491,0.37507,0.37545,0.37583,0.37603,0.37618,0.3764,0.37682,0.37754,0.37869,0.38039,0.38276,0.38592,0.38978,0.39418,0.39894,0.40392,0.40893,0.4138,0.41839,0.42251,0.42657,0.43101,0.43565,0.44035,0.44496,0.44931,0.45326,0.45664,0.4593,0.46129,0.46279,0.46386,0.46458,0.46502,0.46523,0.46529,0.46527,0.46523,0.46497,0.46429,0.46328,0.46205,0.4607,0.45931,0.45798,0.45682,0.45591,0.45518,0.45446,0.45376,0.45309,0.45243,0.4518,0.45119,0.4506,0.45003,0.44953,0.44913,0.44879,0.44849,0.44821,0.44791,0.44757,0.44717,0.44668,0.44599,0.44509,0.44409,0.44307,0.44213,0.44139,0.44067,0.43985,0.439,0.43822,0.43761,0.43727,0.4372,0.43733,0.43762,0.43802,0.43847,0.43892,0.43933,0.43964,0.43981,0.43995,0.44018,0.44046,0.44076,0.44103,0.44125,0.44136,0.44134,0.44115,0.44072,0.44005,0.43922,0.43827,0.43728,0.43631,0.43542,0.43466,0.43412,0.43372,0.43338,0.43309,0.43284,0.43263,0.43244,0.43228,0.43213,0.43199,0.43192,0.43195,0.43206,0.43223,0.43244,0.43266,0.43288,0.43307,0.43321,0.43333,0.43346,0.43361,0.43373,0.43384,0.43389,0.43389,0.43382,0.43366,0.43336,0.43293,0.4324,0.43181,0.43119,0.43058,0.43001,0.42952,0.42915,0.42885,0.42857,0.4283,0.42805,0.42783,0.42765,0.4276,0.42773,0.42795,0.42819,0.42836,0.42838,0.42826,0.4281,0.4279,0.42769,0.42747,0.42726,0.42708,0.42692,0.42682,0.4269,0.42722,0.42769,0.4282,0.42867,0.429,0.42909,0.42885,0.42818,0.42712,0.42579,0.42422,0.42243,0.42045,0.41831,0.41602,0.41362,0.41113,0.40833,0.40507,0.40148,0.39769,0.39381,0.38999,0.38634,0.38298,0.38006,0.37737,0.37468,0.37203,0.36948,0.36709,0.36491,0.363,0.36141,0.3602,0.3594,0.35899,0.35889,0.35905,0.35942,0.35994,0.36054,0.36118,0.36179,0.36259,0.36375,0.36517,0.36675,0.36839,0.36998,0.37142,0.37261,0.37345,0.374,0.37442,0.37472,0.37494,0.37509,0.3752,0.37514,0.37485,0.37441,0.37393,0.37349,0.37319,0.37296,0.37266,0.37231,0.37194,0.37156,0.37119,0.37084,0.37054,0.3703,0.37012,0.36997,0.36985,0.36976,0.36969,0.36965,0.36962,0.36961,0.36962,0.36965,0.36973,0.36985,0.36999,0.37015,0.37031,0.37045,0.37058,0.37067,0.37075,0.37083,0.37091,0.37098,0.37103,0.37106,0.37106,0.37103,0.37096,0.37085,0.37072,0.37056,0.37039,0.3702,0.37,0.3698,0.3696,0.36936,0.36907,0.36875,0.3684,0.36806,0.36773,0.36744,0.36721,0.36705,0.36695,0.36689,0.36687,0.36687,0.36689,0.36694,0.367,0.36707,0.36715,0.36726,0.3674,0.36757,0.36776,0.36797,0.36819,0.36841,0.36863,0.36884,0.36905,0.3693,0.36956,0.36983,0.3701,0.37035,0.37058,0.37078,0.37093,0.37105,0.37117,0.37128,0.37137,0.37145,0.37149,0.37151,0.37149,0.37144,0.37131,0.37109,0.3708,0.37047,0.37013,0.36981,0.36952,0.3693,0.36917,0.36912,0.36912,0.36916,0.36923,0.36932,0.36942,0.36953,0.36964,0.36973,0.36983,0.36996,0.37012,0.37029,0.37046,0.37062,0.37077,0.37089,0.37097,0.37101,0.37099,0.37094,0.37087,0.3708,0.37073,0.3707,0.3707,0.37076,0.37088,0.37105,0.37124,0.37147,0.3717,0.37194,0.37217,0.37239,0.37258,0.37273,0.37285,0.37296,0.37307,0.37321,0.37338,0.37355,0.37365,0.37374,0.37384,0.37401,0.37428,0.37447,0.37446,0.37434,0.3742,0.37412,0.3742,0.37453,0.37521,0.37632,0.3778,0.37954,0.38152,0.38375,0.3862,0.38888,0.39178,0.39489,0.39819,0.402,0.40647,0.41144,0.41671,0.42211,0.42747,0.43259,0.4373,0.44141,0.44515,0.44881,0.45234,0.45568,0.45878,0.46158,0.46402,0.46606,0.46762,0.46867,0.46923,0.4694,0.46927,0.46893,0.46845,0.46794,0.46747,0.46714,0.4668,0.46627,0.4656,0.46482,0.46398,0.46313,0.4623,0.46155,0.4609,0.46031,0.45968,0.45902,0.45833,0.45761,0.45687,0.45611,0.45533,0.45455,0.45371,0.45281,0.45189,0.45098,0.45013,0.44937,0.44867,0.44796,0.44726,0.44658,0.44595,0.44539,0.4449,0.44445,0.44405,0.44371,0.44341,0.44317,0.44297,0.44283,0.44273,0.44273,0.44283,0.44301,0.44324,0.44349,0.44373,0.44393,0.44407,0.44411,0.44406,0.44395,0.4438,0.44361,0.4434,0.44319,0.44297,0.44277,0.44259,0.44243,0.44226,0.44209,0.44192,0.44175,0.44159,0.44144,0.44131,0.44119,0.44112,0.44111,0.44113,0.44117,0.44119,0.44118,0.44112,0.44099,0.44075,0.44038,0.43989,0.4393,0.43866,0.43801,0.43738,0.43683,0.43639,0.43609,0.43595,0.43595,0.43603,0.43618,0.43635,0.43651,0.43663,0.43667,0.4366,0.43644,0.43624,0.43601,0.43578,0.43557,0.43538,0.43512,0.43472,0.43425,0.43378,0.43338,0.43312,0.43307,0.43322,0.43351,0.43388,0.43427,0.43461,0.43486,0.43495,0.43481,0.43449,0.43406,0.43353,0.43291,0.4322,0.43142,0.43056,0.42965,0.42867,0.42763,0.42649,0.42527,0.42397,0.42259,0.42114,0.41962,0.41805,0.41642,0.41473,0.41299,0.41119,0.40935,0.40747,0.40556,0.40361,0.40164,0.39965,0.39749,0.39504,0.39242,0.38969,0.38694,0.38428,0.38177,0.37952,0.3776,0.37593,0.37437,0.37293,0.37163,0.37047,0.36948,0.36865,0.368,0.36755,0.36739,0.36759,0.36805,0.36871,0.36949,0.37032,0.37112,0.37183,0.37235,0.37288,0.37359,0.37436,0.3751,0.3757,0.37606,0.37615,0.37605,0.37583,0.37556,0.37532,0.37518,0.37507,0.37491,0.3747,0.37447,0.37422,0.37396,0.37373,0.37352,0.37335,0.37322,0.37309,0.37298,0.37287,0.37278,0.37268,0.3726,0.37251,0.37243,0.37234,0.37223,0.37212,0.372,0.37189,0.3718,0.37173,0.37168,0.37166,0.3717,0.3718,0.37194,0.37209,0.37225,0.37239,0.37249,0.37255,0.37254,0.37251,0.37245,0.37237,0.37228,0.37218,0.37209,0.37201,0.37194,0.37189,0.37183,0.37176,0.3717,0.37165,0.37161,0.37158,0.37156,0.37157,0.37161,0.3717,0.37182,0.37196,0.37211,0.37224,0.37235,0.37242,0.37244,0.3724,0.37232,0.37221,0.37208,0.37196,0.37186,0.37174,0.37157,0.37139,0.37121,0.37105,0.37093,0.37083,0.37073,0.37061,0.37049,0.37037,0.37025,0.37015,0.37006,0.36999,0.36993,0.36987,0.36982,0.36979,0.36978,0.36981,0.36987,0.36998,0.37015,0.37039,0.3707,0.37108,0.37151,0.37196,0.37242,0.37288,0.37331,0.37371,0.3741,0.37451,0.37494,0.37537,0.37577,0.37614,0.37645,0.37668,0.37683,0.37688,0.37685,0.37675,0.37661,0.37644,0.37627,0.37612,0.37601,0.37596,0.3759,0.37579,0.37565,0.3755,0.37537,0.37528,0.37527,0.37535,0.37556,0.37588,0.37627,0.37673,0.37724,0.3778,0.3784,0.37902,0.37965,0.38029,0.38075,0.38099,0.38117,0.38144,0.38198,0.38294,0.38403,0.38494,0.38587,0.38701,0.38856,0.39071,0.39354,0.39693,0.40078,0.40498,0.40942,0.41399,0.41857,0.42307,0.42737,0.4319,0.43703,0.44254,0.4482,0.45379,0.4591,0.46389,0.46795,0.47107,0.47329,0.4749,0.47598,0.4766,0.47686,0.47685,0.47663,0.47631,0.47595,0.4753,0.47411,0.47252,0.47066,0.46865,0.46664,0.46476,0.46314,0.46191,0.46097,0.46014,0.45939,0.45872,0.45811,0.45755,0.45701,0.4565,0.45599,0.4555,0.45504,0.4546,0.45418,0.45377,0.45337,0.45296,0.45254,0.4521,0.45164,0.45116,0.45069,0.45022,0.44976,0.44933,0.44893,0.44857,0.44826,0.44796,0.44763,0.4473,0.447,0.44676,0.44661,0.44656,0.44659,0.44668,0.4468,0.44694,0.44706,0.44721,0.44743,0.44769,0.44799,0.4483,0.4486,0.44888,0.44911,0.44927,0.4494,0.44952,0.44963,0.44972,0.44979,0.44984,0.44986,0.44984,0.44978,0.44968,0.44957,0.44944,0.44929,0.4491,0.44888,0.44862,0.44831,0.44797,0.44754,0.44701,0.44641,0.44577,0.4451,0.44443,0.44378,0.44318,0.44265,0.44216,0.44167,0.44118,0.44072,0.44029,0.43992,0.43962,0.4394,0.43928,0.4393,0.43949,0.43979,0.44014,0.4405,0.44082,0.44105,0.44113,0.44103,0.44072,0.44026,0.43969,0.43904,0.43835,0.43765,0.43698,0.43638,0.43586,0.43548,0.43522,0.43505,0.43493,0.43483,0.43474,0.4346,0.4344,0.43411,0.43378,0.43349,0.4332,0.43287,0.43245,0.43191,0.43122,0.43032,0.42919,0.42786,0.42639,0.42477,0.42301,0.42109,0.41903,0.4168,0.41441,0.41186,0.40892,0.40547,0.40167,0.3977,0.39371,0.38988,0.38636,0.38332,0.38093,0.37903,0.37733,0.37583,0.37453,0.37343,0.37252,0.37181,0.37128,0.37094,0.37102,0.37166,0.3727,0.37402,0.37546,0.37689,0.37815,0.37912,0.37965,0.37979,0.37973,0.37952,0.37919,0.3788,0.37837,0.37796,0.37761,0.37735,0.37715,0.37693,0.3767,0.37647,0.37623,0.37599,0.37575,0.37552,0.3753,0.37508,0.37485,0.37463,0.37441,0.37421,0.37402,0.37385,0.37368,0.37351,0.37336,0.3732,0.37305,0.37291,0.37277,0.37263,0.3725,0.37239,0.37228,0.37218,0.3721,0.37202,0.37196,0.37191,0.37186,0.37182,0.37179,0.37177,0.37176,0.37176,0.37176,0.37179,0.37184,0.37191,0.372,0.37209,0.37219,0.37227,0.37234,0.37239,0.37245,0.37252,0.37261,0.37271,0.3728,0.37288,0.37294,0.37297,0.37296,0.37289,0.37276,0.37258,0.37237,0.37214,0.37191,0.3717,0.37151,0.37136,0.37124,0.3711,0.37097,0.37083,0.37071,0.3706,0.37052,0.37047,0.37046,0.3705,0.37061,0.37076,0.37095,0.37116,0.37138,0.37159,0.37179,0.37196,0.37214,0.37238,0.37263,0.37286,0.37303,0.3731,0.37307,0.37298,0.37285,0.3727,0.37255,0.37243,0.37229,0.37208,0.37181,0.37152,0.37122,0.37094,0.37071,0.37054,0.37046,0.37048,0.3706,0.37078,0.371,0.37125,0.37151,0.37175,0.37195,0.37209,0.37218,0.37224,0.37228,0.37231,0.37233,0.37235,0.37237,0.3724,0.37245,0.3725,0.37254,0.37258,0.37262,0.37266,0.3727,0.37276,0.37284,0.37293,0.37305,0.37319,0.37334,0.3735,0.37367,0.37385,0.37402,0.3742,0.37436,0.37451,0.37465,0.37478,0.37491,0.37504,0.37518,0.37532,0.37548,0.37566,0.37573,0.37561,0.37537,0.37509,0.37483,0.37467,0.37468,0.37493,0.37548,0.37602,0.3763,0.37659,0.37713,0.37816,0.37994,0.38256,0.38583,0.38953,0.39343,0.39734,0.40103,0.40492,0.40946,0.41447,0.41977,0.42516,0.43048,0.43555,0.44017,0.44417,0.4477,0.451,0.45407,0.45691,0.4595,0.46184,0.46393,0.46575,0.4673,0.46855,0.46951,0.47022,0.47071,0.47103,0.47121,0.47129,0.4713,0.4713,0.47116,0.47077,0.47019,0.46946,0.46864,0.46777,0.46691,0.46611,0.46541,0.46473,0.46395,0.46309,0.4622,0.46129,0.4604,0.45955,0.45878,0.45811,0.45753,0.45702,0.45656,0.45614,0.45574,0.45536,0.45496,0.45455,0.45411,0.45364,0.45316,0.45266,0.45216,0.45165,0.45114,0.45062,0.4501,0.44958,0.44906,0.44852,0.44798,0.44745,0.44693,0.44644,0.44598,0.44557,0.44521,0.44488,0.44455,0.44422,0.44391,0.44361,0.44333,0.44308,0.44287,0.44269,0.44257,0.44252,0.44253,0.44258,0.44265,0.44273,0.4428,0.44285,0.44285,0.44285,0.44287,0.44292,0.44297,0.44302,0.44305,0.44306,0.44304,0.44298,0.44284,0.44263,0.44238,0.4421,0.44182,0.44156,0.44136,0.44124,0.44121,0.44133,0.4416,0.44197,0.4424,0.44284,0.44324,0.44355,0.44374,0.44375,0.4436,0.44337,0.44307,0.44268,0.44223,0.44172,0.44116,0.44055,0.4399,0.43917,0.43833,0.43742,0.43645,0.43547,0.4345,0.43356,0.43268,0.4319,0.43115,0.43036,0.42957,0.42878,0.42803,0.42734,0.42681,0.42645,0.42618,0.42589,0.42549,0.42489,0.42422,0.42368,0.42318,0.42266,0.42204,0.42125,0.42022,0.41887,0.41715,0.41489,0.41211,0.40893,0.40548,0.40191,0.39835,0.39492,0.39177,0.38903,0.38648,0.38385,0.3812,0.37862,0.37617,0.37391,0.37192,0.37026,0.369,0.36822,0.36789,0.36791,0.36821,0.36869,0.36927,0.36986,0.37039,0.37075,0.37109,0.37156,0.37214,0.37278,0.37343,0.37406,0.37463,0.37509,0.37541,0.37563,0.37579,0.37592,0.37601,0.37607,0.37609,0.37609,0.37606,0.37601,0.37591,0.37573,0.37549,0.3752,0.37489,0.37457,0.37427,0.374,0.37379,0.37357,0.37333,0.37308,0.37285,0.37268,0.37259,0.37259,0.37264,0.37272,0.37283,0.37293,0.37301,0.37311,0.37328,0.3735,0.37374,0.37398,0.3742,0.37439,0.37451,0.37455,0.37448,0.37433,0.3741,0.37384,0.37355,0.37326,0.37299,0.37277,0.37262,0.37254,0.3725,0.37249,0.3725,0.37252,0.37255,0.37258,0.37259,0.3726,0.37261,0.37263,0.37265,0.37267,0.37269,0.3727,0.37271,0.37271,0.37269,0.37267,0.37265,0.37262,0.37259,0.37257,0.37255,0.37254,0.37254,0.37257,0.37263,0.37272,0.37282,0.37292,0.373,0.37306,0.37309,0.37306,0.37297,0.3728,0.37258,0.37233,0.37207,0.37182,0.37161,0.37145,0.37136,0.37136,0.37141,0.3715,0.37161,0.3717,0.37177,0.37183,0.37192,0.37203,0.37214,0.37226,0.37235,0.37245,0.37254,0.37264,0.37274,0.37283,0.37292,0.373,0.37306,0.37311,0.37315,0.3732,0.37325,0.37329,0.37333,0.37337,0.37339,0.3734,0.37339,0.37335,0.37326,0.37314,0.37299,0.37285,0.37271,0.37259,0.37251,0.37247,0.37249,0.37253,0.3726,0.37269,0.3728,0.37293,0.37307,0.37322,0.37338,0.37356,0.37376,0.37399,0.37422,0.37446,0.37471,0.37495,0.37518,0.37539,0.3756,0.37582,0.37604,0.37625,0.37647,0.37667,0.37686,0.37704,0.37719,0.3772,0.377,0.37666,0.37627,0.37589,0.37561,0.3755,0.37564,0.3761,0.37665,0.3771,0.37755,0.37811,0.37889,0.37999,0.38154,0.38363,0.38638,0.39002,0.39458,0.39984,0.40559,0.41161,0.41769,0.42362,0.42918,0.43417,0.43899,0.44412,0.4494,0.45467,0.45978,0.46457,0.46888,0.47256,0.47544,0.47753,0.479,0.47993,0.48043,0.48059,0.48052,0.4803,0.48004,0.47984,0.47947,0.47872,0.47768,0.47641,0.47502,0.47358,0.47216,0.47087,0.46977,0.4687,0.46748,0.46616,0.4648,0.46347,0.46222,0.46112,0.46023,0.4596,0.45928,0.45922,0.45936,0.45963,0.45999,0.46036,0.46069,0.46093,0.461,0.46096,0.46089,0.46079,0.46066,0.46051,0.46034,0.46013,0.4599,0.45965,0.45928,0.45876,0.45817,0.45758,0.45708,0.45673,0.45656,0.4565,0.4565,0.45653,0.45656,0.45653,0.45648,0.45646,0.45646,0.45647,0.45648,0.45647,0.45644,0.45637,0.45625,0.45608,0.45586,0.4556,0.45531,0.45501,0.45471,0.45442,0.45415,0.45392,0.4537,0.45349,0.45329,0.45309,0.4529,0.45272,0.45256,0.45242,0.4523,0.45219,0.45209,0.452,0.45192,0.45184,0.45176,0.45169,0.45163,0.45157,0.45155,0.4516,0.45171,0.45183,0.45196,0.45207,0.45213,0.45213,0.45204,0.45184,0.45155,0.45119,0.45077,0.45033,0.44987,0.44942,0.44899,0.44862,0.44828,0.44795,0.44763,0.44733,0.44705,0.44679,0.44656,0.44636,0.4462,0.44634,0.44692,0.44768,0.44837,0.44874,0.44855,0.44817,0.44801,0.44785,0.44746,0.44665,0.4452,0.443,0.44017,0.43684,0.43313,0.42918,0.42509,0.42101,0.41705,0.41335,0.40956,0.40538,0.40094,0.3964,0.3919,0.38759,0.38361,0.38011,0.37725,0.37494,0.373,0.37138,0.37006,0.369,0.36817,0.36754,0.36707,0.36673,0.36669,0.36705,0.36773,0.36863,0.36967,0.37076,0.3718,0.37271,0.37339,0.37397,0.37459,0.37525,0.37592,0.37656,0.37716,0.3777,0.37815,0.37849,0.37875,0.37897,0.37915,0.37929,0.37937,0.3794,0.37936,0.37926,0.37908,0.37875,0.37825,0.37763,0.37692,0.37619,0.37547,0.37482,0.37429,0.37391,0.37363,0.37335,0.37309,0.37286,0.37268,0.37257,0.37262,0.37286,0.3732,0.37356,0.37388,0.37407,0.37418,0.37432,0.37446,0.37461,0.37473,0.37483,0.37487,0.37486,0.37476,0.37457,0.37428,0.37393,0.37355,0.37316,0.37279,0.37248,0.37225,0.37208,0.37191,0.37176,0.37162,0.37151,0.37142,0.37136,0.37133,0.37134,0.37141,0.37158,0.37181,0.37207,0.37234,0.3726,0.37282,0.37297,0.37303,0.37301,0.37293,0.37281,0.37266,0.37248,0.37229,0.37209,0.37189,0.3717,0.3715,0.37124,0.37095,0.37065,0.37035,0.37006,0.36982,0.36963,0.36951,0.36946,0.36945,0.36949,0.36955,0.36964,0.36975,0.36986,0.36997,0.37008,0.3702,0.37034,0.37049,0.37066,0.37083,0.371,0.3712,0.37145,0.37173,0.372,0.37224,0.3724,0.37251,0.37261,0.37269,0.37275,0.3728,0.37284,0.37286,0.37288,0.37287,0.37284,0.37274,0.37261,0.37245,0.37228,0.37212,0.37198,0.37187,0.37182,0.3718,0.37181,0.37183,0.37187,0.37193,0.372,0.37208,0.37219,0.3723,0.37243,0.37259,0.37277,0.37297,0.37318,0.3734,0.37363,0.37386,0.37409,0.37433,0.37459,0.37486,0.37513,0.3754,0.37566,0.3759,0.37612,0.3763,0.37627,0.37594,0.37542,0.37481,0.37424,0.37381,0.37364,0.37383,0.3745,0.37556,0.37685,0.37838,0.38014,0.38214,0.38439,0.38689,0.38965,0.39265,0.39637,0.40099,0.40609,0.41127,0.41613,0.42025,0.42411,0.42832,0.43264,0.43686,0.44075,0.44409,0.44693,0.44948,0.45176,0.45381,0.45565,0.45731,0.45882,0.46021,0.4615,0.46265,0.46362,0.46442,0.46507,0.4656,0.46603,0.46638,0.46666,0.46692,0.46705,0.46697,0.46674,0.46638,0.46594,0.46544,0.46494,0.46446,0.46405,0.46366,0.46323,0.46277,0.46229,0.46179,0.46128,0.46076,0.46026,0.45976,0.45924,0.45867,0.45807,0.45745,0.45683,0.45622,0.45565,0.45513,0.45468,0.45431,0.454,0.45376,0.45356,0.45339,0.45324,0.45311,0.45298,0.45283,0.45267,0.45251,0.45234,0.45218,0.45202,0.45186,0.4517,0.45155,0.4514,0.45129,0.45123,0.4512,0.45117,0.45112,0.45102,0.4508,0.45047,0.45009,0.44972,0.44943,0.44929,0.44929,0.44936,0.44949,0.44967,0.44988,0.45011,0.45034,0.45056,0.45074,0.45097,0.45127,0.45163,0.452,0.45235,0.45266,0.45289,0.45299,0.45295,0.4527,0.45223,0.4516,0.45087,0.45009,0.44932,0.44862,0.44805,0.44765,0.44742,0.44731,0.44729,0.44734,0.44745,0.44758,0.44771,0.44783,0.4479,0.44798,0.44812,0.44828,0.44844,0.44859,0.44869,0.44873,0.44868,0.44851,0.4482,0.44776,0.44723,0.44664,0.44604,0.44544,0.4449,0.44445,0.44412,0.44401,0.44412,0.44439,0.44475,0.44511,0.44541,0.44557,0.44552,0.44518,0.44466,0.44407,0.44338,0.44258,0.44162,0.44049,0.43913,0.43753,0.43575,0.43384,0.43185,0.42985,0.42775,0.42547,0.42303,0.42046,0.41778,0.41502,0.41221,0.40937,0.40653,0.40344,0.39994,0.39618,0.39231,0.38848,0.38485,0.38156,0.37877,0.37663,0.37509,0.37398,0.37324,0.37278,0.37256,0.37249,0.37251,0.37256,0.37257,0.37273,0.37324,0.374,0.37491,0.3759,0.37685,0.37769,0.37831,0.37863,0.37866,0.37853,0.37827,0.37793,0.37753,0.37713,0.37677,0.37647,0.3763,0.37619,0.37607,0.37595,0.37583,0.37572,0.37562,0.37553,0.37546,0.37541,0.3754,0.37543,0.37549,0.37557,0.37567,0.37576,0.37585,0.37592,0.37597,0.376,0.37602,0.37603,0.37604,0.37603,0.37602,0.37599,0.37595,0.3759,0.37583,0.37576,0.37568,0.37559,0.37549,0.37538,0.37526,0.37513,0.37498,0.37479,0.37457,0.37434,0.37411,0.37388,0.37367,0.37348,0.37332,0.37317,0.37301,0.37283,0.37267,0.37251,0.37239,0.3723,0.37225,0.37227,0.37238,0.3726,0.37289,0.37323,0.37358,0.37392,0.37421,0.37443,0.37453,0.37453,0.37445,0.37432,0.37414,0.37393,0.37373,0.37354,0.37338,0.37327,0.3732,0.37311,0.37303,0.37295,0.37288,0.37283,0.37279,0.37277,0.37278,0.37283,0.37291,0.37301,0.37314,0.37327,0.37342,0.37355,0.37368,0.37378,0.37385,0.37387,0.37388,0.37389,0.37393,0.37401,0.37416,0.37438,0.37463,0.37488,0.37509,0.37524,0.37534,0.37543,0.37551,0.37558,0.37564,0.37569,0.37572,0.37575,0.37577,0.37575,0.3757,0.37562,0.37552,0.37542,0.37531,0.37523,0.37516,0.37514,0.37513,0.37513,0.37514,0.37515,0.37518,0.37522,0.37528,0.37537,0.37548,0.37563,0.3758,0.37601,0.37623,0.37647,0.37672,0.37697,0.37723,0.37747,0.37773,0.37801,0.37831,0.37863,0.37894,0.37924,0.37952,0.37978,0.37999,0.38003,0.37982,0.37944,0.379,0.3786,0.37832,0.37827,0.37854,0.37922,0.38015,0.38115,0.38226,0.38353,0.38501,0.38675,0.38879,0.3912,0.39401,0.39746,0.40159,0.40617,0.41094,0.41567,0.42011,0.42494,0.43067,0.43682,0.44291,0.44846,0.453,0.45689,0.46075,0.46449,0.46805,0.47133,0.47426,0.47676,0.47874,0.48012,0.48069,0.48041,0.47946,0.47803,0.4763,0.47445,0.47266,0.47112,0.47001,0.46912,0.46814,0.46712,0.46608,0.46507,0.46413,0.46331,0.46263,0.46213,0.46181,0.4616,0.46149,0.46147,0.4615,0.46159,0.4617,0.46183,0.46195,0.46215,0.46247,0.46289,0.46335,0.46383,0.46427,0.46465,0.46491,0.46501,0.465,0.46492,0.46479,0.46462,0.46441,0.46416,0.4639,0.46361,0.46332,0.46296,0.4625,0.46195,0.46136,0.46076,0.46019,0.45966,0.45923,0.45891,0.45877,0.45879,0.4589,0.45904,0.45911,0.45907,0.459,0.459,0.45903,0.45904,0.45899,0.45885,0.45857,0.45817,0.45769,0.45714,0.45656,0.45596,0.45538,0.45483,0.45436,0.4539,0.45341,0.45291,0.45241,0.45195,0.45152,0.45115,0.45087,0.45067,0.45063,0.45074,0.45097,0.45128,0.45162,0.45197,0.45228,0.4525,0.4526,0.45263,0.45264,0.45264,0.45263,0.4526,0.45256,0.4525,0.45242,0.45232,0.45216,0.45189,0.45156,0.45118,0.4508,0.45044,0.45013,0.4499,0.44978,0.44984,0.45008,0.45045,0.45088,0.45132,0.45171,0.452,0.45213,0.45204,0.45189,0.45183,0.4518,0.45172,0.45154,0.45119,0.45061,0.44972,0.44847,0.44678,0.44466,0.44219,0.43946,0.43655,0.43353,0.43049,0.4275,0.42465,0.4218,0.41881,0.4157,0.41251,0.40927,0.40602,0.40279,0.39961,0.39653,0.39336,0.38995,0.38642,0.38287,0.3794,0.37613,0.37315,0.37056,0.36848,0.36682,0.3654,0.36422,0.36327,0.36254,0.36204,0.36174,0.36165,0.36176,0.36232,0.36351,0.36516,0.36711,0.3692,0.37128,0.37319,0.37476,0.37583,0.37649,0.37692,0.37717,0.37728,0.37728,0.37722,0.37712,0.37703,0.37699,0.37694,0.37681,0.37662,0.37639,0.37615,0.37589,0.37566,0.37546,0.37532,0.37522,0.37514,0.37508,0.37503,0.37498,0.37493,0.37488,0.37482,0.37474,0.37466,0.3746,0.37454,0.37447,0.37439,0.3743,0.37414,0.37391,0.37366,0.37342,0.37322,0.3731,0.37304,0.37301,0.37301,0.37301,0.37303,0.37307,0.37311,0.37315,0.3732,0.37328,0.37339,0.37354,0.3737,0.37386,0.37401,0.37415,0.37425,0.3743,0.3743,0.37428,0.37423,0.37416,0.37408,0.37399,0.3739,0.37381,0.37374,0.37366,0.37357,0.37347,0.37337,0.37326,0.37315,0.37305,0.37295,0.37287,0.37277,0.37264,0.37249,0.37234,0.3722,0.3721,0.37205,0.37206,0.37216,0.37237,0.37269,0.37309,0.37355,0.37403,0.3745,0.37492,0.37528,0.37553,0.3757,0.37583,0.37593,0.376,0.37603,0.37603,0.376,0.37593,0.37582,0.3756,0.37523,0.37479,0.37434,0.37398,0.37376,0.37366,0.37359,0.37354,0.37352,0.37351,0.37351,0.37355,0.37363,0.37376,0.37391,0.37408,0.37425,0.37441,0.37454,0.37465,0.37471,0.37473,0.37474,0.37474,0.37474,0.37475,0.37479,0.37486,0.37498,0.37515,0.37537,0.37562,0.3759,0.37619,0.37649,0.37677,0.37704,0.37727,0.37744,0.37753,0.37756,0.37758,0.3776,0.37767,0.37781,0.37806,0.37844,0.37888,0.37932,0.37978,0.38028,0.38084,0.38148,0.38222,0.3831,0.38411,0.38509,0.38591,0.38667,0.38749,0.38849,0.38978,0.39147,0.39368,0.39651,0.40013,0.4045,0.40946,0.41484,0.42048,0.42621,0.43188,0.43733,0.44238,0.44789,0.45443,0.46139,0.46818,0.47418,0.4788,0.48245,0.48588,0.48897,0.49163,0.49373,0.49515,0.49563,0.4951,0.49377,0.49185,0.48957,0.48713,0.48475,0.48264,0.48101,0.47958,0.47794,0.47616,0.47429,0.47238,0.47052,0.46874,0.46711,0.4657,0.46444,0.46327,0.46217,0.46115,0.46021,0.45936,0.45858,0.45789,0.45729,0.45681,0.45646,0.45622,0.45606,0.45596,0.45589,0.45582,0.45574,0.45562,0.4555,0.45542,0.45537,0.45534,0.4553,0.45524,0.45514,0.455,0.45478,0.45448,0.4541,0.45365,0.45317,0.45267,0.45217,0.45169,0.45126,0.4509,0.45062,0.45039,0.45021,0.45006,0.44994,0.44981,0.44968,0.44952,0.44933,0.4491,0.44886,0.44861,0.44835,0.4481,0.44784,0.4476,0.44737,0.44715,0.44695,0.44676,0.44657,0.44638,0.44618,0.44597,0.44574,0.44549,0.44522,0.44492,0.44459,0.44424,0.44389,0.44354,0.44321,0.44291,0.44264,0.44241,0.44223,0.44206,0.44191,0.44179,0.4417,0.44164,0.44161,0.44163,0.44168,0.44178,0.44194,0.44213,0.44235,0.44259,0.44282,0.44303,0.44322,0.44336,0.44348,0.44361,0.44374,0.44386,0.44397,0.44405,0.44411,0.44414,0.44412,0.44408,0.44403,0.44397,0.44389,0.44378,0.44366,0.4435,0.44332,0.44309,0.44289,0.44275,0.44264,0.44252,0.44235,0.44211,0.44175,0.44124,0.44055,0.43972,0.4388,0.43779,0.43668,0.43545,0.4341,0.43264,0.43108,0.4294,0.4276,0.42567,0.42359,0.42125,0.41862,0.41575,0.41272,0.40958,0.40642,0.40328,0.40025,0.39738,0.39443,0.39121,0.38782,0.38441,0.38109,0.37799,0.37524,0.37296,0.37128,0.37025,0.36977,0.36973,0.37004,0.37058,0.37125,0.37195,0.37257,0.373,0.37343,0.37408,0.37487,0.37574,0.37663,0.37745,0.37815,0.37866,0.37891,0.3789,0.37871,0.37838,0.37795,0.37748,0.37699,0.37654,0.37616,0.3759,0.37571,0.37554,0.37538,0.37523,0.37508,0.37494,0.37481,0.37468,0.37456,0.37445,0.37436,0.37427,0.3742,0.37413,0.37408,0.37404,0.37402,0.374,0.37397,0.37391,0.37384,0.37378,0.37375,0.37375,0.37383,0.37398,0.37415,0.37432,0.37444,0.37455,0.37469,0.37486,0.37503,0.37521,0.37538,0.37553,0.37564,0.37571,0.37574,0.37574,0.37571,0.37566,0.37559,0.37552,0.37544,0.37536,0.37528,0.3752,0.37508,0.37495,0.37481,0.37466,0.37451,0.37437,0.37425,0.37416,0.37407,0.37396,0.37386,0.37376,0.37368,0.37362,0.37361,0.37364,0.37373,0.37392,0.37423,0.37463,0.37507,0.37552,0.37596,0.37635,0.37666,0.37685,0.37694,0.37697,0.37694,0.37688,0.37677,0.37663,0.37646,0.37626,0.37606,0.37578,0.37539,0.37493,0.37442,0.37391,0.37343,0.37301,0.37268,0.37247,0.37239,0.37238,0.37242,0.3725,0.3726,0.3727,0.37288,0.37321,0.37361,0.37401,0.37437,0.3746,0.37473,0.37483,0.37491,0.37497,0.37501,0.37504,0.37507,0.37509,0.37511,0.37512,0.37508,0.37502,0.37495,0.37488,0.37481,0.37477,0.37476,0.37479,0.37486,0.37493,0.37501,0.37512,0.37524,0.37539,0.37557,0.37578,0.37603,0.3762,0.37624,0.3762,0.37614,0.37612,0.3762,0.37645,0.37692,0.37769,0.37857,0.37941,0.38029,0.38129,0.38247,0.38393,0.38573,0.38795,0.39067,0.39409,0.39827,0.40303,0.40821,0.41362,0.41911,0.4245,0.42962,0.43431,0.43897,0.44401,0.44924,0.45451,0.45964,0.46445,0.46878,0.47245,0.47528,0.47728,0.47866,0.47957,0.48012,0.48048,0.48078,0.48052,0.47936,0.47765,0.47575,0.47404,0.47287,0.47196,0.47085,0.46961,0.46828,0.46695,0.46567,0.46451,0.46353,0.4628,0.46232,0.46203,0.46188,0.46186,0.4619,0.46199,0.46207,0.46211,0.46208,0.46202,0.46201,0.46202,0.46204,0.46205,0.46203,0.46196,0.46183,0.46161,0.46126,0.46075,0.46013,0.45945,0.45874,0.45805,0.45743,0.45691,0.45653,0.45631,0.45618,0.45614,0.45616,0.45623,0.45632,0.45642,0.45652,0.45658,0.45667,0.45682,0.45703,0.45726,0.45749,0.4577,0.45786,0.45795,0.45796,0.45789,0.45778,0.45763,0.45744,0.45722,0.45696,0.45666,0.45633,0.45596,0.45557,0.45516,0.45472,0.45425,0.45375,0.45322,0.45255,0.45171,0.45079,0.44986,0.44903,0.44838,0.44781,0.44722,0.44661,0.44601,0.44545,0.44496,0.44455,0.44425,0.44409,0.44412,0.44433,0.44468,0.44514,0.44567,0.44621,0.44673,0.44719,0.44755,0.44786,0.44819,0.44854,0.44888,0.4492,0.44948,0.44971,0.44987,0.44995,0.44992,0.44979,0.44958,0.44932,0.44903,0.44874,0.44847,0.44825,0.4481,0.44808,0.44819,0.44839,0.44864,0.44887,0.44904,0.44911,0.44903,0.44874,0.44828,0.44772,0.44706,0.4463,0.44546,0.44455,0.44355,0.44249,0.44137,0.44014,0.43876,0.43725,0.43566,0.43401,0.43232,0.43062,0.42895,0.42733,0.42586,0.42453,0.42324,0.42186,0.4203,0.41842,0.41634,0.41423,0.41205,0.40976,0.40736,0.40479,0.40184,0.39839,0.3946,0.39066,0.38672,0.38296,0.37955,0.37665,0.37443,0.37288,0.3718,0.37113,0.3708,0.37072,0.37083,0.37105,0.37131,0.37153,0.37191,0.37262,0.37356,0.37464,0.37577,0.37684,0.37777,0.37845,0.3788,0.37891,0.37896,0.37896,0.37891,0.37884,0.37875,0.37865,0.37856,0.37848,0.37841,0.37835,0.37828,0.37822,0.37816,0.3781,0.37804,0.37798,0.37792,0.37787,0.37782,0.37777,0.37774,0.3777,0.37766,0.37762,0.37759,0.37755,0.37752,0.37751,0.37752,0.37754,0.37755,0.37754,0.3775,0.37743,0.37732,0.37718,0.37703,0.37686,0.37669,0.37652,0.37631,0.37604,0.37573,0.37543,0.37515,0.37493,0.37474,0.37453,0.37431,0.37411,0.37391,0.37375,0.37363,0.37356,0.37356,0.37364,0.37381,0.37404,0.37431,0.37461,0.37489,0.37516,0.37537,0.37551,0.37561,0.37571,0.37581,0.3759,0.37598,0.37605,0.3761,0.37612,0.37612,0.37606,0.37594,0.37577,0.37557,0.37535,0.37514,0.37494,0.37477,0.37465,0.37456,0.37448,0.37441,0.37434,0.37429,0.37425,0.37423,0.37422,0.37423,0.37427,0.37433,0.37441,0.3745,0.37461,0.37472,0.37484,0.37495,0.37506,0.37519,0.37534,0.37551,0.37569,0.37588,0.37606,0.37624,0.37639,0.37652,0.37662,0.37668,0.37671,0.37673,0.37674,0.37674,0.37676,0.37679,0.37684,0.37691,0.37698,0.37705,0.37713,0.37721,0.37732,0.37744,0.37759,0.37777,0.37798,0.37823,0.37851,0.37881,0.37912,0.37943,0.37974,0.38004,0.38032,0.38056,0.38076,0.38094,0.38111,0.38128,0.38146,0.38167,0.38191,0.3822,0.38244,0.38257,0.38264,0.38271,0.38285,0.38311,0.38354,0.38422,0.38519,0.38633,0.38752,0.38881,0.39022,0.39181,0.39363,0.39571,0.3981,0.40085,0.40413,0.408,0.41234,0.417,0.42185,0.42674,0.43156,0.43615,0.44038,0.44463,0.44926,0.45408,0.45894,0.46364,0.46801,0.47188,0.47508,0.47742,0.47879,0.47935,0.47936,0.47905,0.47869,0.4785,0.47795,0.47656,0.47467,0.47265,0.47086,0.46965,0.46887,0.46813,0.46742,0.46674,0.46608,0.46544,0.46482,0.46421,0.4636,0.46298,0.46232,0.46163,0.46093,0.46023,0.45954,0.45886,0.45822,0.45762,0.45701,0.45635,0.45568,0.455,0.45435,0.45375,0.45323,0.4528,0.45251,0.45238,0.4524,0.45255,0.45278,0.45306,0.45333,0.45358,0.45375,0.45381,0.4538,0.4538,0.45381,0.4538,0.45378,0.45373,0.45366,0.45355,0.4534,0.45317,0.45284,0.45244,0.45198,0.4515,0.45102,0.45056,0.45014,0.44979,0.44952,0.44931,0.44915,0.44902,0.44891,0.4488,0.44869,0.44854,0.44836,0.44813,0.44785,0.44756,0.44726,0.44698,0.44674,0.44649,0.44621,0.44591,0.44564,0.44541,0.44525,0.44517,0.44513,0.44513,0.44516,0.44522,0.44531,0.44541,0.44552,0.44563,0.44581,0.44607,0.4464,0.44674,0.44707,0.44735,0.44753,0.44758,0.44746,0.44714,0.44664,0.446,0.44527,0.44451,0.44375,0.44306,0.44247,0.44204,0.44179,0.44169,0.4417,0.44178,0.44188,0.44195,0.44197,0.44187,0.44163,0.44144,0.44147,0.44162,0.44175,0.44177,0.44156,0.441,0.43999,0.43841,0.43615,0.43326,0.42987,0.4261,0.42208,0.41793,0.41378,0.40975,0.40597,0.40197,0.39737,0.3924,0.38728,0.38227,0.37759,0.37348,0.37016,0.36789,0.36672,0.36638,0.36662,0.36716,0.36774,0.36811,0.36887,0.37056,0.37276,0.37506,0.37705,0.37832,0.37902,0.3796,0.38005,0.3804,0.38067,0.38086,0.381,0.38109,0.38115,0.38118,0.38117,0.38111,0.38102,0.38089,0.38072,0.38052,0.3803,0.38004,0.37969,0.37922,0.37865,0.37801,0.37735,0.37668,0.37606,0.37549,0.37503,0.37461,0.37417,0.37372,0.3733,0.37291,0.3726,0.37236,0.37224,0.37225,0.37245,0.37285,0.3734,0.37403,0.3747,0.37535,0.37592,0.37636,0.37663,0.37671,0.37669,0.37658,0.37641,0.37622,0.37602,0.37585,0.37572,0.37568,0.37569,0.3757,0.37572,0.37574,0.37577,0.37581,0.37586,0.37591,0.376,0.37614,0.37632,0.37652,0.37672,0.37691,0.37708,0.3772,0.37726,0.37729,0.37731,0.37732,0.37731,0.37729,0.37725,0.37718,0.37709,0.37697,0.37679,0.37653,0.3762,0.37584,0.37547,0.37511,0.37477,0.37449,0.37429,0.37413,0.37398,0.37384,0.37373,0.37365,0.3736,0.3736,0.37365,0.37375,0.37395,0.37425,0.37462,0.37505,0.37551,0.37596,0.37638,0.37675,0.37703,0.37725,0.37744,0.37761,0.37776,0.3779,0.37802,0.37813,0.37824,0.37835,0.37846,0.37856,0.37865,0.37872,0.37879,0.37883,0.37886,0.37887,0.37886,0.3788,0.3787,0.37855,0.37839,0.37821,0.37805,0.3779,0.3778,0.37775,0.37773,0.3777,0.37768,0.37767,0.37771,0.37779,0.37795,0.37821,0.37853,0.37885,0.37916,0.3794,0.37961,0.37986,0.38014,0.38042,0.38068,0.38092,0.38111,0.38124,0.38129,0.38128,0.38123,0.38115,0.38105,0.38094,0.38083,0.38072,0.38063,0.38055,0.38045,0.38029,0.3801,0.37988,0.37966,0.37947,0.37932,0.37923,0.37923,0.37913,0.37878,0.37828,0.37772,0.37721,0.37682,0.37665,0.3768,0.37735,0.37828,0.37949,0.38098,0.38276,0.38485,0.38725,0.38997,0.39302,0.3964,0.40052,0.40558,0.41133,0.4175,0.42384,0.43009,0.43599,0.44127,0.44568,0.44952,0.45326,0.45682,0.46016,0.46321,0.46592,0.46824,0.4701,0.47145,0.47198,0.47164,0.47075,0.46962,0.46857,0.4679,0.4672,0.46598,0.46449,0.46296,0.46163,0.46073,0.46015,0.45961,0.4591,0.45863,0.45819,0.45778,0.45739,0.45703,0.4567,0.45642,0.45624,0.45612,0.45604,0.45599,0.45592,0.45583,0.45569,0.45547,0.45517,0.4548,0.45439,0.45395,0.45349,0.45304,0.45261,0.45222,0.45187,0.45159,0.45136,0.45117,0.451,0.45086,0.45072,0.45058,0.45042,0.45023,0.45,0.44972,0.44941,0.44908,0.44874,0.44842,0.44812,0.44785,0.44764,0.44749,0.44738,0.4473,0.44725,0.44723,0.44722,0.44722,0.44723,0.44723,0.44723,0.44722,0.44722,0.44723,0.44726,0.44732,0.44742,0.44757,0.44777,0.44812,0.44864,0.44925,0.44983,0.45031,0.45058,0.45072,0.45084,0.45093,0.45099,0.451,0.45096,0.45085,0.45067,0.45041,0.45011,0.44975,0.44935,0.44891,0.44845,0.44797,0.44741,0.44672,0.44595,0.44514,0.44433,0.44359,0.44294,0.44243,0.44212,0.44202,0.44208,0.44228,0.44255,0.44285,0.44314,0.44337,0.44349,0.44346,0.44344,0.44358,0.44381,0.44406,0.44424,0.44428,0.44411,0.44365,0.44283,0.44167,0.44028,0.4387,0.43696,0.43512,0.43321,0.43127,0.42936,0.42751,0.42566,0.42371,0.42167,0.41952,0.41728,0.41493,0.41247,0.40991,0.40724,0.40402,0.40001,0.39548,0.3907,0.38596,0.38153,0.37768,0.37469,0.37283,0.37186,0.37127,0.371,0.37097,0.37111,0.37135,0.3716,0.3718,0.37187,0.37195,0.37221,0.37261,0.37311,0.37365,0.37419,0.37469,0.3751,0.37538,0.37556,0.37573,0.37586,0.37598,0.37606,0.37611,0.37612,0.3761,0.37603,0.3759,0.3757,0.37544,0.37514,0.37483,0.37453,0.37425,0.37402,0.37385,0.37374,0.37365,0.37358,0.37352,0.37348,0.37345,0.37342,0.3734,0.37338,0.37337,0.37338,0.37341,0.37344,0.37347,0.3735,0.37351,0.37351,0.37347,0.37342,0.37335,0.37328,0.3732,0.37311,0.37302,0.37294,0.37286,0.37278,0.37272,0.37265,0.37259,0.37254,0.37249,0.37245,0.37241,0.37238,0.37235],"name":"PhenoCam GCC","showlegend":true,"type":"scatter","mode":"line","marker":{"color":"rgba(31,119,180,1)","line":{"color":"rgba(31,119,180,1)"}},"error_y":{"color":"rgba(31,119,180,1)"},"error_x":{"color":"rgba(31,119,180,1)"},"line":{"color":"rgba(31,119,180,1)"},"xaxis":"x","yaxis":"y","frame":null},{"x":["2009-05-02","2010-04-25","2011-05-07","2012-04-30","2013-05-04","2014-05-10","2015-05-05","2016-05-11","2017-05-10","2018-05-07","2019-05-11","2020-05-17"],"y":[0.3889,0.38978,0.39489,0.39693,0.39734,0.39458,0.39265,0.39746,0.4045,0.39827,0.40085,0.40052],"type":"scatter","mode":"markers","name":"Spring Dates","marker":{"color":"rgba(255,127,14,1)","line":{"color":"rgba(255,127,14,1)"}},"error_y":{"color":"rgba(255,127,14,1)"},"error_x":{"color":"rgba(255,127,14,1)"},"line":{"color":"rgba(255,127,14,1)"},"xaxis":"x","yaxis":"y","frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->
Now we can see the transition date for each year of interest and the annual patterns of Gcc.

However, if you want more control over the parameters used during processing, you can run through the three default processing steps as implemented in download_phenocam() and set parameters manually.

Of particular interest is the option to specify your own threshold used in determining transition dates.

What would be a reasonable threshold for peak greenness?  Or autumn onset?  Look at the ts dataset and phenocamr package and come up with a threshold.  Use the same code to plot it here:



```r
# #some hint code
# #what does 'rising' versus 'falling' denote?
# #what threshold should you choose?
# #td <- phenophases("butte_GR_1000_3day.csv",
# #            internal = TRUE,
# #            upper_thresh = 0.8)
fall <- td[td$direction == "falling" & td$gcc_value == "gcc_90",]
#Now generate a fall dataframe, what metrics should you use?
```

### Comparing phenology across vegetation types

Let's load in a function to make plotting smoother.  I've dropped it here in the markdown so that you can edit it and re-run it as you see fit:


```r
gcc_plot = function(gcc, spring, fall){
  unix = "1970-01-01"

  p = plot_ly(
    data = gcc,
    x = ~ date,
    y = ~ gcc_90,
    showlegend = FALSE,
    type = 'scatter',
    mode = 'line'
  ) %>%
    add_trace(
      y = ~ smooth_gcc_90,
      mode = "lines",
      line = list(width = 2, color = "rgb(120,120,120)"),
      name = "Gcc loess fit",
      showlegend = TRUE
    ) %>%
    # SOS spring
    # 10%
    add_trace(
      data = spring,
      x = ~ as.Date(transition_10),
      y = ~ threshold_10,
      mode = "markers",
      type = "scatter",
      marker = list(color = "#7FFF00", symbol = "circle"),
      name = "SOS (10%)",
      showlegend = TRUE
    ) %>%
    add_segments(x = ~ as.Date(transition_10_lower_ci),
                 xend = ~ as.Date(transition_10_upper_ci),
                 # y = ~ 0,
                 # yend = ~ 1,
                 y = ~ threshold_10,
                 yend = ~ threshold_10,
                 line = list(color = "#7FFF00"),
                 name = "SOS (10%) - CI"
    ) %>%
    # 25 %
    add_trace(
      x = ~ as.Date(transition_25),
      y = ~ threshold_25,
      mode = "markers",
      type = "scatter",
      marker = list(color = "#66CD00", symbol = "square"),
      showlegend = TRUE,
      name = "SOS (25%)"
    ) %>%
    add_segments(x = ~ as.Date(transition_25_lower_ci),
                 xend = ~ as.Date(transition_25_upper_ci),
                 y = ~ threshold_25,
                 yend = ~ threshold_25,
                 line = list(color = "#66CD00"),
                 name = "SOS (25%) - CI"
    ) %>%
    # 50 %
    add_trace(
      x = ~ as.Date(transition_50),
      y = ~ threshold_50,
      mode = "markers",
      type = "scatter",
      marker = list(color = "#458B00", symbol = "diamond"),
      showlegend = TRUE,
      name = "SOS (50%)"
    ) %>%
    add_segments(x = ~ as.Date(transition_50_lower_ci),
                 xend = ~ as.Date(transition_50_upper_ci),
                 y = ~ threshold_50,
                 yend = ~ threshold_50,
                 line = list(color = "#458B00"),
                 name = "SOS (50%) - CI"
    ) %>%

    # EOS fall
    # 50%
    add_trace(
      data = fall,
      x = ~ as.Date(transition_50),
      y = ~ threshold_50,
      mode = "markers",
      type = "scatter",
      marker = list(color = "#FFB90F", symbol = "diamond"),
      showlegend = TRUE,
      name = "EOS (50%)"
    ) %>%
    add_segments(x = ~ as.Date(transition_50_lower_ci),
                 xend = ~ as.Date(transition_50_upper_ci),
                 y = ~ threshold_50,
                 yend = ~ threshold_50,
                 line = list(color = "#FFB90F"),
                 name = "EOS (50%) - CI"
    ) %>%
    # 25 %
    add_trace(
      x = ~ as.Date(transition_25),
      y = ~ threshold_25,
      mode = "markers",
      type = "scatter",
      marker = list(color = "#CD950C", symbol = "square"),
      showlegend = TRUE,
      name = "EOS (25%)"
    ) %>%
    add_segments(x = ~ as.Date(transition_25_lower_ci),
                 xend = ~ as.Date(transition_25_upper_ci),
                 y = ~ threshold_25,
                 yend = ~ threshold_25,
                 line = list(color = "#CD950C"),
                 name = "EOS (25%) - CI"
    ) %>%
    # 10 %
    add_trace(
      x = ~ as.Date(transition_10),
      y = ~ threshold_10,
      mode = "markers",
      marker = list(color = "#8B6508", symbol = "circle"),
      showlegend = TRUE,
      name = "EOS (10%)"
    ) %>%
    add_segments(x = ~ as.Date(transition_10_lower_ci),
                 xend = ~ as.Date(transition_10_upper_ci),
                 y = ~ threshold_10,
                 yend = ~ threshold_10,
                 line = list(color = "#8B6508"),
                 name = "EOS (10%) - CI"
    )
  return (p)
}
```



```r
gcc_p = gcc_plot(df, spring, fall)
gcc_p <- gcc_p %>%
  layout(
    legend = list(x = 0.9, y = 0.9),
    xaxis = list(
      type = 'date',
      tickformat = " %B<br>%Y",
      title='Year'),

    yaxis = list(
      title = 'PhenoCam GCC'
    ))

gcc_p
```

```
## Warning: Ignoring 3239 observations
```

```
## Warning: `group_by_()` is deprecated as of dplyr 0.7.0.
## Please use `group_by()` instead.
## See vignette('programming') for more help
## This warning is displayed once every 8 hours.
## Call `lifecycle::last_warnings()` to see where this warning was generated.
```

```
## Warning: Can't display both discrete & non-discrete data on same axis
```

<!--html_preserve--><div id="htmlwidget-c5b3ad816eb0d9901452" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-c5b3ad816eb0d9901452">{"x":{"visdat":{"8beee9acec1":["function () ","plotlyVisDat"],"8bee557be864":["function () ","data"],"8bee39d62914":["function () ","data"]},"cur_data":"8bee39d62914","attrs":{"8beee9acec1":{"x":{},"y":{},"showlegend":false,"mode":"line","alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"scatter"},"8beee9acec1.1":{"x":{},"y":{},"showlegend":true,"mode":"lines","alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"scatter","line":{"width":2,"color":"rgb(120,120,120)"},"name":"Gcc loess fit","inherit":true},"8bee557be864":{"x":{},"y":{},"showlegend":true,"mode":"markers","alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"scatter","marker":{"color":"#7FFF00","symbol":"circle"},"name":"SOS (10%)","inherit":true},"8bee557be864.1":{"x":{},"y":{},"showlegend":false,"mode":"lines","alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"scatter","xend":{},"yend":{},"line":{"color":"#7FFF00"},"name":"SOS (10%) - CI","inherit":true},"8bee557be864.2":{"x":{},"y":{},"showlegend":true,"mode":"markers","alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"scatter","marker":{"color":"#66CD00","symbol":"square"},"name":"SOS (25%)","inherit":true},"8bee557be864.3":{"x":{},"y":{},"showlegend":false,"mode":"lines","alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"scatter","xend":{},"yend":{},"line":{"color":"#66CD00"},"name":"SOS (25%) - CI","inherit":true},"8bee557be864.4":{"x":{},"y":{},"showlegend":true,"mode":"markers","alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"scatter","marker":{"color":"#458B00","symbol":"diamond"},"name":"SOS (50%)","inherit":true},"8bee557be864.5":{"x":{},"y":{},"showlegend":false,"mode":"lines","alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"scatter","xend":{},"yend":{},"line":{"color":"#458B00"},"name":"SOS (50%) - CI","inherit":true},"8bee39d62914":{"x":{},"y":{},"showlegend":true,"mode":"markers","alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"scatter","marker":{"color":"#FFB90F","symbol":"diamond"},"name":"EOS (50%)","inherit":true},"8bee39d62914.1":{"x":{},"y":{},"showlegend":false,"mode":"lines","alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"scatter","xend":{},"yend":{},"line":{"color":"#FFB90F"},"name":"EOS (50%) - CI","inherit":true},"8bee39d62914.2":{"x":{},"y":{},"showlegend":true,"mode":"markers","alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"scatter","marker":{"color":"#CD950C","symbol":"square"},"name":"EOS (25%)","inherit":true},"8bee39d62914.3":{"x":{},"y":{},"showlegend":false,"mode":"lines","alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"scatter","xend":{},"yend":{},"line":{"color":"#CD950C"},"name":"EOS (25%) - CI","inherit":true},"8bee39d62914.4":{"x":{},"y":{},"showlegend":true,"mode":"markers","alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"scatter","marker":{"color":"#8B6508","symbol":"circle"},"name":"EOS (10%)","inherit":true},"8bee39d62914.5":{"x":{},"y":{},"showlegend":false,"mode":"lines","alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"scatter","xend":{},"yend":{},"line":{"color":"#8B6508"},"name":"EOS (10%) - CI","inherit":true}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"legend":{"x":0.9,"y":0.9},"xaxis":{"domain":[0,1],"automargin":true,"type":"date","tickformat":" %B<br>%Y","title":"Year"},"yaxis":{"domain":[0,1],"automargin":true,"title":"PhenoCam GCC"},"hovermode":"closest","showlegend":true},"source":"A","config":{"showSendToCloud":false},"data":[{"x":["2008-04-05","2008-04-08","2008-04-11","2008-04-14","2008-04-17","2008-04-20","2008-04-23","2008-04-26","2008-04-29","2008-05-02","2008-05-05","2008-05-08","2008-05-11","2008-05-14","2008-05-17","2008-05-20","2008-05-23","2008-05-26","2008-05-29","2008-06-01","2008-06-04","2008-06-07","2008-06-10","2008-06-13","2008-06-16","2008-06-19","2008-06-22","2008-06-25","2008-06-28","2008-07-01","2008-07-04","2008-07-07","2008-07-10","2008-07-13","2008-07-16","2008-07-19","2008-07-22","2008-07-25","2008-07-28","2008-07-31","2008-08-03","2008-08-06","2008-08-09","2008-08-12","2008-08-15","2008-08-18","2008-08-21","2008-08-24","2008-08-27","2008-08-30","2008-09-02","2008-09-05","2008-09-08","2008-09-11","2008-09-14","2008-09-17","2008-09-20","2008-09-23","2008-09-26","2008-09-29","2008-10-02","2008-10-05","2008-10-08","2008-10-11","2008-10-14","2008-10-17","2008-10-20","2008-10-23","2008-10-26","2008-10-29","2008-11-01","2008-11-04","2008-11-07","2008-11-10","2008-11-13","2008-11-16","2008-11-19","2008-11-22","2008-11-25","2008-11-28","2008-12-01","2008-12-04","2008-12-07","2008-12-10","2008-12-16","2008-12-19","2008-12-22","2008-12-25","2008-12-28","2008-12-31","2009-01-02","2009-01-05","2009-01-08","2009-01-11","2009-01-14","2009-01-17","2009-01-20","2009-01-23","2009-01-26","2009-01-29","2009-02-01","2009-02-04","2009-02-07","2009-02-10","2009-02-13","2009-02-16","2009-02-19","2009-02-22","2009-02-25","2009-02-28","2009-03-03","2009-03-06","2009-03-09","2009-03-12","2009-03-15","2009-03-18","2009-03-21","2009-03-24","2009-03-27","2009-03-30","2009-04-02","2009-04-05","2009-04-08","2009-04-11","2009-04-14","2009-04-17","2009-04-20","2009-04-23","2009-04-26","2009-04-29","2009-05-02","2009-05-05","2009-05-08","2009-05-11","2009-05-14","2009-05-17","2009-05-20","2009-05-23","2009-05-26","2009-05-29","2009-06-01","2009-06-04","2009-06-07","2009-06-10","2009-06-13","2009-06-16","2009-06-19","2009-06-22","2009-06-25","2009-06-28","2009-07-01","2009-07-04","2009-07-07","2009-07-10","2009-07-13","2009-07-16","2009-07-19","2009-07-22","2009-07-25","2009-07-28","2009-07-31","2009-08-03","2009-08-06","2009-08-09","2009-08-12","2009-08-15","2009-08-18","2009-08-21","2009-08-24","2009-08-27","2009-08-30","2009-09-02","2009-09-05","2009-09-08","2009-09-11","2009-09-14","2009-09-17","2009-09-20","2009-09-23","2009-09-26","2009-09-29","2009-10-02","2009-10-05","2009-10-08","2009-10-11","2009-10-14","2009-10-17","2009-10-20","2009-10-23","2009-10-26","2009-10-29","2009-11-01","2009-11-04","2009-11-07","2009-11-10","2009-11-13","2009-11-16","2009-11-19","2009-11-22","2009-11-25","2009-11-28","2009-12-01","2009-12-04","2009-12-07","2009-12-10","2009-12-13","2009-12-16","2009-12-19","2009-12-22","2009-12-25","2009-12-28","2009-12-31","2010-01-02","2010-01-05","2010-01-08","2010-01-11","2010-01-14","2010-01-17","2010-01-20","2010-01-23","2010-01-26","2010-01-29","2010-02-01","2010-02-04","2010-02-07","2010-02-10","2010-02-13","2010-02-16","2010-02-19","2010-02-22","2010-02-25","2010-02-28","2010-03-03","2010-03-06","2010-03-09","2010-03-12","2010-03-15","2010-03-18","2010-03-21","2010-03-24","2010-03-27","2010-03-30","2010-04-02","2010-04-05","2010-04-08","2010-04-11","2010-04-14","2010-04-17","2010-04-20","2010-04-23","2010-04-26","2010-04-29","2010-05-02","2010-05-05","2010-05-11","2010-05-14","2010-05-17","2010-05-20","2010-05-23","2010-05-26","2010-05-29","2010-06-01","2010-06-04","2010-06-07","2010-06-10","2010-06-13","2010-06-16","2010-06-19","2010-06-22","2010-06-25","2010-06-28","2010-07-01","2010-07-04","2010-07-07","2010-07-10","2010-07-13","2010-07-16","2010-07-19","2010-07-22","2010-07-25","2010-07-28","2010-07-31","2010-08-03","2010-08-06","2010-08-09","2010-08-12","2010-08-15","2010-08-18","2010-08-21","2010-08-24","2010-08-27","2010-08-30","2010-09-02","2010-09-05","2010-09-08","2010-09-11","2010-09-14","2010-09-17","2010-09-20","2010-09-23","2010-09-26","2010-09-29","2010-10-02","2010-10-05","2010-10-08","2010-10-11","2010-10-14","2010-10-17","2010-10-20","2010-10-23","2010-10-26","2010-10-29","2010-11-01","2010-11-04","2010-11-07","2010-11-10","2010-11-13","2010-11-16","2010-11-19","2010-11-22","2010-11-25","2010-11-28","2010-12-01","2010-12-04","2010-12-07","2010-12-10","2010-12-13","2010-12-16","2010-12-19","2010-12-22","2010-12-25","2010-12-28","2010-12-31","2011-01-02","2011-01-05","2011-01-08","2011-01-11","2011-01-14","2011-01-17","2011-01-20","2011-01-23","2011-01-26","2011-01-29","2011-02-01","2011-02-04","2011-02-07","2011-02-10","2011-02-13","2011-02-16","2011-02-19","2011-02-22","2011-02-25","2011-02-28","2011-03-03","2011-03-06","2011-03-09","2011-03-12","2011-03-15","2011-03-18","2011-03-21","2011-03-24","2011-03-27","2011-03-30","2011-04-02","2011-04-05","2011-04-08","2011-04-11","2011-04-14","2011-04-17","2011-04-20","2011-04-23","2011-04-26","2011-04-29","2011-05-02","2011-05-05","2011-05-08","2011-05-11","2011-05-14","2011-05-17","2011-05-20","2011-05-23","2011-05-26","2011-05-29","2011-06-01","2011-06-04","2011-06-07","2011-06-10","2011-06-13","2011-06-16","2011-06-19","2011-06-22","2011-06-25","2011-06-28","2011-07-01","2011-07-04","2011-07-07","2011-07-10","2011-07-13","2011-07-16","2011-07-19","2011-07-22","2011-07-25","2011-07-28","2011-07-31","2011-08-03","2011-08-06","2011-08-09","2011-08-12","2011-08-15","2011-08-18","2011-08-21","2011-08-24","2011-08-27","2011-08-30","2011-09-02","2011-09-05","2011-09-08","2011-09-11","2011-09-14","2011-09-17","2011-09-20","2011-09-23","2011-09-26","2011-09-29","2011-10-02","2011-10-05","2011-10-08","2011-10-11","2011-10-14","2011-10-17","2011-10-20","2011-10-23","2011-10-26","2011-10-29","2011-11-01","2011-11-04","2011-11-07","2011-11-10","2011-11-13","2011-11-16","2011-11-19","2011-11-22","2011-11-25","2011-11-28","2011-12-01","2011-12-04","2011-12-07","2011-12-10","2011-12-13","2011-12-16","2011-12-19","2011-12-22","2011-12-25","2011-12-28","2011-12-31","2012-01-02","2012-01-05","2012-01-08","2012-01-11","2012-01-14","2012-01-17","2012-01-20","2012-01-23","2012-01-26","2012-01-29","2012-02-01","2012-02-04","2012-02-07","2012-02-10","2012-02-13","2012-02-16","2012-02-19","2012-02-22","2012-02-25","2012-02-28","2012-03-02","2012-03-05","2012-03-08","2012-03-11","2012-03-14","2012-03-17","2012-03-20","2012-03-23","2012-03-26","2012-03-29","2012-04-01","2012-04-04","2012-04-07","2012-04-10","2012-04-13","2012-04-16","2012-04-19","2012-04-22","2012-04-25","2012-04-28","2012-05-01","2012-05-04","2012-05-07","2012-05-10","2012-05-13","2012-05-16","2012-05-19","2012-05-22","2012-05-25","2012-05-28","2012-05-31","2012-06-03","2012-06-06","2012-06-09","2012-06-12","2012-06-15","2012-06-18","2012-06-21","2012-06-24","2012-06-27","2012-06-30","2012-07-03","2012-07-06","2012-07-09","2012-07-12","2012-07-15","2012-07-18","2012-07-21","2012-07-24","2012-07-27","2012-07-30","2012-08-02","2012-08-05","2012-08-08","2012-08-11","2012-08-14","2012-08-17","2012-08-20","2012-08-23","2012-08-26","2012-08-29","2012-09-01","2012-09-04","2012-09-07","2012-09-10","2012-09-13","2012-09-16","2012-09-19","2012-09-22","2012-09-25","2012-09-28","2012-10-01","2012-10-04","2012-10-07","2012-10-10","2012-10-13","2012-10-16","2012-10-19","2012-10-22","2012-10-25","2012-10-28","2012-10-31","2012-11-03","2012-11-06","2012-11-09","2012-11-12","2012-11-15","2012-11-18","2012-11-21","2012-11-24","2012-11-27","2012-11-30","2012-12-03","2012-12-06","2012-12-09","2012-12-12","2012-12-15","2012-12-18","2012-12-21","2012-12-24","2012-12-27","2012-12-30","2013-01-02","2013-01-05","2013-01-08","2013-01-11","2013-01-14","2013-01-17","2013-01-20","2013-01-23","2013-01-26","2013-01-29","2013-02-01","2013-02-04","2013-02-07","2013-02-10","2013-02-13","2013-02-16","2013-02-19","2013-02-22","2013-02-25","2013-02-28","2013-03-03","2013-03-06","2013-03-09","2013-03-12","2013-03-15","2013-03-18","2013-03-21","2013-03-24","2013-03-27","2013-03-30","2013-04-02","2013-04-05","2013-04-08","2013-04-11","2013-04-14","2013-04-17","2013-04-20","2013-04-23","2013-04-26","2013-04-29","2013-05-02","2013-05-05","2013-05-08","2013-05-11","2013-05-14","2013-05-17","2013-05-20","2013-05-23","2013-05-26","2013-05-29","2013-06-01","2013-06-04","2013-06-07","2013-06-10","2013-06-13","2013-06-16","2013-06-19","2013-06-22","2013-06-25","2013-06-28","2013-07-01","2013-07-04","2013-07-07","2013-07-10","2013-07-13","2013-07-16","2013-07-19","2013-07-22","2013-07-25","2013-07-28","2013-07-31","2013-08-03","2013-08-06","2013-08-09","2013-08-12","2013-08-15","2013-08-18","2013-08-21","2013-08-24","2013-08-27","2013-08-30","2013-09-02","2013-09-05","2013-09-08","2013-09-11","2013-09-14","2013-09-17","2013-09-20","2013-09-23","2013-09-26","2013-09-29","2013-10-02","2013-10-05","2013-10-08","2013-10-11","2013-10-14","2013-10-17","2013-10-20","2013-10-23","2013-10-26","2013-10-29","2013-11-01","2013-11-04","2013-11-07","2013-11-10","2013-11-13","2013-11-16","2013-11-19","2013-11-22","2013-11-25","2013-11-28","2013-12-01","2013-12-04","2013-12-07","2013-12-10","2013-12-13","2013-12-16","2013-12-19","2013-12-22","2013-12-25","2013-12-28","2013-12-31","2014-01-02","2014-01-05","2014-01-08","2014-01-11","2014-01-14","2014-01-17","2014-01-20","2014-01-23","2014-01-26","2014-01-29","2014-02-01","2014-02-04","2014-02-07","2014-02-10","2014-02-13","2014-02-16","2014-02-19","2014-02-22","2014-02-25","2014-02-28","2014-03-03","2014-03-06","2014-03-09","2014-03-12","2014-03-15","2014-03-18","2014-03-21","2014-03-24","2014-03-27","2014-03-30","2014-04-02","2014-04-05","2014-04-08","2014-04-11","2014-04-14","2014-04-17","2014-04-20","2014-04-23","2014-04-26","2014-04-29","2014-05-02","2014-05-05","2014-05-08","2014-05-11","2014-05-14","2014-05-17","2014-05-20","2014-05-23","2014-05-26","2014-05-29","2014-06-01","2014-06-04","2014-06-07","2014-06-10","2014-06-13","2014-06-16","2014-06-19","2014-06-22","2014-06-25","2014-06-28","2014-07-01","2014-07-04","2014-07-07","2014-07-10","2014-07-13","2014-07-16","2014-07-19","2014-07-22","2014-07-25","2014-07-28","2014-07-31","2014-08-03","2014-08-06","2014-08-09","2014-08-12","2014-08-15","2014-08-18","2014-08-21","2014-08-24","2014-08-27","2014-08-30","2014-09-02","2014-09-05","2014-09-08","2014-09-11","2014-09-14","2014-09-17","2014-09-20","2014-09-23","2014-09-26","2014-09-29","2014-10-02","2014-10-05","2014-10-08","2014-10-11","2014-10-14","2014-10-17","2014-10-20","2014-10-23","2014-10-26","2014-10-29","2014-11-01","2014-11-04","2014-11-07","2014-11-10","2014-11-13","2014-11-16","2014-11-19","2014-11-22","2014-11-25","2014-12-01","2014-12-04","2014-12-07","2014-12-10","2014-12-13","2014-12-16","2014-12-19","2014-12-22","2014-12-25","2014-12-28","2014-12-31","2015-01-02","2015-01-05","2015-01-08","2015-01-11","2015-01-14","2015-01-17","2015-01-20","2015-01-23","2015-01-26","2015-01-29","2015-02-01","2015-02-04","2015-02-07","2015-02-10","2015-02-13","2015-02-16","2015-02-19","2015-02-22","2015-02-25","2015-02-28","2015-03-03","2015-03-06","2015-03-09","2015-03-12","2015-03-15","2015-03-18","2015-03-21","2015-03-24","2015-03-27","2015-03-30","2015-04-02","2015-04-05","2015-04-08","2015-04-11","2015-04-14","2015-04-17","2015-04-20","2015-04-23","2015-04-26","2015-04-29","2015-05-02","2015-05-05","2015-05-08","2015-05-11","2015-05-14","2015-05-17","2015-05-20","2015-05-23","2015-05-26","2015-05-29","2015-06-01","2015-06-04","2015-06-07","2015-06-10","2015-06-13","2015-06-16","2015-06-19","2015-06-22","2015-06-25","2015-06-28","2015-07-01","2015-07-04","2015-07-07","2015-07-10","2015-07-13","2015-07-16","2015-07-19","2015-07-22","2015-07-25","2015-07-28","2015-07-31","2015-08-03","2015-08-06","2015-08-09","2015-08-12","2015-08-15","2015-08-18","2015-08-21","2015-08-24","2015-08-27","2015-08-30","2015-09-02","2015-09-05","2015-09-08","2015-09-11","2015-09-14","2015-09-17","2015-09-20","2015-09-23","2015-09-26","2015-09-29","2015-10-02","2015-10-05","2015-10-08","2015-10-11","2015-10-14","2015-10-17","2015-10-20","2015-10-23","2015-10-26","2015-10-29","2015-11-01","2015-11-04","2015-11-07","2015-11-10","2015-11-13","2015-11-16","2015-11-19","2015-11-22","2015-11-25","2015-11-28","2015-12-01","2015-12-04","2015-12-07","2015-12-10","2015-12-13","2015-12-16","2015-12-19","2015-12-22","2015-12-25","2015-12-28","2015-12-31","2016-01-02","2016-01-05","2016-01-08","2016-01-11","2016-01-14","2016-01-17","2016-01-20","2016-01-23","2016-01-26","2016-01-29","2016-02-01","2016-02-04","2016-02-07","2016-02-10","2016-02-13","2016-02-16","2016-02-19","2016-02-22","2016-02-25","2016-02-28","2016-03-02","2016-03-05","2016-03-08","2016-03-11","2016-03-14","2016-03-17","2016-03-20","2016-03-23","2016-03-26","2016-03-29","2016-04-01","2016-04-04","2016-04-07","2016-04-10","2016-04-13","2016-04-16","2016-04-19","2016-04-22","2016-04-25","2016-04-28","2016-05-01","2016-05-04","2016-05-07","2016-05-10","2016-05-13","2016-05-16","2016-05-19","2016-05-22","2016-05-25","2016-05-28","2016-05-31","2016-06-03","2016-06-06","2016-06-09","2016-06-12","2016-06-15","2016-06-18","2016-06-21","2016-06-24","2016-06-27","2016-06-30","2016-07-03","2016-07-06","2016-07-09","2016-07-12","2016-07-15","2016-07-18","2016-07-21","2016-07-24","2016-07-27","2016-07-30","2016-08-02","2016-08-05","2016-08-08","2016-08-11","2016-08-14","2016-08-17","2016-08-20","2016-08-23","2016-08-26","2016-08-29","2016-09-01","2016-09-04","2016-09-07","2016-09-10","2016-09-13","2016-09-16","2016-09-19","2016-09-22","2016-09-25","2016-09-28","2016-10-01","2016-10-04","2016-10-07","2016-10-10","2016-10-13","2016-10-16","2016-10-19","2016-10-22","2016-10-25","2016-10-28","2016-10-31","2016-11-03","2016-11-06","2016-11-09","2016-11-12","2016-11-15","2016-11-18","2016-11-21","2016-11-24","2016-11-27","2016-11-30","2016-12-03","2016-12-06","2016-12-09","2016-12-12","2016-12-15","2016-12-18","2016-12-21","2016-12-24","2016-12-27","2016-12-30","2017-01-02","2017-01-05","2017-01-08","2017-01-11","2017-01-14","2017-01-17","2017-01-20","2017-01-23","2017-01-26","2017-01-29","2017-02-01","2017-02-04","2017-02-07","2017-02-10","2017-02-13","2017-02-16","2017-02-19","2017-02-22","2017-02-25","2017-02-28","2017-03-03","2017-03-06","2017-03-09","2017-03-12","2017-03-15","2017-03-18","2017-03-21","2017-03-24","2017-03-27","2017-03-30","2017-04-02","2017-04-05","2017-04-08","2017-04-11","2017-04-14","2017-04-17","2017-04-20","2017-04-23","2017-04-26","2017-04-29","2017-05-02","2017-05-05","2017-05-08","2017-05-11","2017-05-14","2017-05-17","2017-05-20","2017-05-23","2017-05-26","2017-05-29","2017-06-01","2017-06-04","2017-06-07","2017-06-10","2017-06-13","2017-06-16","2017-06-19","2017-06-22","2017-06-25","2017-06-28","2017-07-01","2017-07-04","2017-07-07","2017-07-10","2017-07-13","2017-07-16","2017-07-19","2017-07-22","2017-07-25","2017-07-28","2017-07-31","2017-08-03","2017-08-06","2017-08-09","2017-08-12","2017-08-15","2017-08-18","2017-08-21","2017-08-24","2017-08-27","2017-08-30","2017-09-02","2017-09-05","2017-09-08","2017-09-11","2017-09-14","2017-09-17","2017-09-20","2017-09-23","2017-09-26","2017-09-29","2017-10-02","2017-10-05","2017-10-08","2017-10-11","2017-10-14","2017-10-17","2017-10-20","2017-10-23","2017-10-26","2017-10-29","2017-11-01","2017-11-04","2017-11-07","2017-11-10","2017-11-13","2017-11-16","2017-11-19","2017-11-22","2017-11-25","2017-11-28","2017-12-01","2017-12-04","2017-12-07","2017-12-10","2017-12-13","2017-12-16","2017-12-19","2017-12-22","2017-12-25","2017-12-28","2017-12-31","2018-01-02","2018-01-05","2018-01-08","2018-01-11","2018-01-14","2018-01-17","2018-01-20","2018-01-23","2018-01-26","2018-01-29","2018-02-01","2018-02-04","2018-02-07","2018-02-10","2018-02-13","2018-02-16","2018-02-19","2018-02-22","2018-02-25","2018-02-28","2018-03-03","2018-03-06","2018-03-09","2018-03-12","2018-03-15","2018-03-18","2018-03-21","2018-03-24","2018-03-27","2018-03-30","2018-04-02","2018-04-05","2018-04-08","2018-04-11","2018-04-14","2018-04-17","2018-04-20","2018-04-23","2018-04-26","2018-04-29","2018-05-02","2018-05-05","2018-05-08","2018-05-11","2018-05-14","2018-05-17","2018-05-20","2018-05-23","2018-05-26","2018-05-29","2018-06-01","2018-06-04","2018-06-07","2018-06-10","2018-06-13","2018-06-16","2018-06-19","2018-06-22","2018-06-25","2018-06-28","2018-07-01","2018-07-04","2018-07-07","2018-07-10","2018-07-13","2018-07-16","2018-07-19","2018-07-22","2018-07-25","2018-07-28","2018-07-31","2018-08-03","2018-08-06","2018-08-09","2018-08-12","2018-08-15","2018-08-18","2018-08-21","2018-08-24","2018-08-27","2018-08-30","2018-09-02","2018-09-05","2018-09-08","2018-09-11","2018-09-14","2018-09-17","2018-09-20","2018-09-23","2018-09-26","2018-09-29","2018-10-02","2018-10-05","2018-10-08","2018-10-11","2018-10-14","2018-10-17","2018-10-20","2018-10-23","2018-10-26","2018-10-29","2018-11-01","2018-11-04","2018-11-07","2018-11-10","2018-11-13","2018-11-28","2018-12-01","2018-12-04","2018-12-07","2018-12-10","2018-12-13","2018-12-16","2018-12-19","2018-12-22","2018-12-25","2018-12-28","2018-12-31","2019-01-02","2019-01-05","2019-01-08","2019-01-11","2019-01-14","2019-01-17","2019-01-20","2019-01-23","2019-01-29","2019-02-01","2019-02-04","2019-02-07","2019-02-10","2019-02-13","2019-02-16","2019-02-19","2019-02-22","2019-02-25","2019-02-28","2019-03-03","2019-03-06","2019-03-09","2019-03-12","2019-03-15","2019-03-18","2019-03-21","2019-03-24","2019-03-27","2019-03-30","2019-04-02","2019-04-05","2019-04-08","2019-04-11","2019-04-14","2019-04-17","2019-04-20","2019-04-23","2019-04-26","2019-04-29","2019-05-02","2019-05-05","2019-05-08","2019-05-11","2019-05-14","2019-05-17","2019-05-20","2019-05-23","2019-05-26","2019-05-29","2019-06-01","2019-06-04","2019-06-07","2019-06-10","2019-06-13","2019-06-16","2019-06-19","2019-06-22","2019-06-25","2019-06-28","2019-07-01","2019-07-04","2019-07-07","2019-07-10","2019-07-13","2019-07-16","2019-07-19","2019-07-22","2019-07-25","2019-07-28","2019-07-31","2019-08-03","2019-08-06","2019-08-09","2019-08-12","2019-08-15","2019-08-18","2019-08-21","2019-08-24","2019-08-27","2019-08-30","2019-09-02","2019-09-05","2019-09-08","2019-09-11","2019-09-14","2019-09-17","2019-09-20","2019-09-23","2019-09-26","2019-09-29","2019-10-02","2019-10-05","2019-10-08","2019-10-11","2019-10-14","2019-10-17","2019-10-23","2019-10-26","2019-10-29","2019-11-01","2019-11-04","2019-11-07","2019-11-10","2019-11-13","2019-11-16","2019-11-19","2019-11-22","2019-11-25","2019-11-28","2019-12-01","2019-12-04","2019-12-07","2019-12-10","2019-12-13","2019-12-16","2019-12-19","2019-12-22","2019-12-25","2019-12-28","2019-12-31","2020-01-02","2020-01-05","2020-01-08","2020-01-11","2020-01-14","2020-01-17","2020-01-20","2020-01-23","2020-01-26","2020-01-29","2020-02-01","2020-02-04","2020-02-07","2020-02-10","2020-02-13","2020-02-16","2020-02-19","2020-02-22","2020-02-25","2020-02-28","2020-03-02","2020-03-05","2020-03-08","2020-03-11","2020-03-14","2020-03-17","2020-03-20","2020-03-23","2020-03-26","2020-03-29","2020-04-01","2020-04-04","2020-04-07","2020-04-10","2020-04-13","2020-04-16","2020-04-19","2020-05-04","2020-05-07","2020-05-10","2020-05-13","2020-05-16","2020-05-19","2020-05-22","2020-05-25","2020-05-28","2020-05-31","2020-06-03","2020-06-06","2020-06-09","2020-06-12","2020-06-15","2020-06-18","2020-06-21","2020-06-24","2020-06-27","2020-06-30","2020-07-03","2020-07-06","2020-07-09","2020-07-12","2020-07-15","2020-07-18","2020-07-21","2020-07-24","2020-07-27","2020-07-30","2020-08-02","2020-08-05","2020-08-08","2020-08-11","2020-08-14","2020-08-17","2020-08-20","2020-08-23","2020-08-26","2020-08-29","2020-09-01","2020-09-04","2020-09-07","2020-09-10","2020-09-13","2020-09-16","2020-09-19","2020-09-22","2020-09-25","2020-09-28","2020-10-01","2020-10-04","2020-10-07","2020-10-10","2020-10-13"],"y":[0.35909,0.36557,0.36554,0.36537,0.37027,0.3708,0.37058,0.37208,0.36901,0.37264,0.37909,0.39558,0.40069,0.42004,0.43538,0.43521,0.43893,0.4585,0.4578,0.46991,0.47149,0.4625,0.44934,0.44908,0.44893,0.44486,0.45703,0.45444,0.44772,0.44275,0.44916,0.44139,0.43981,0.44227,0.43696,0.44033,0.44643,0.4399,0.4353,0.43618,0.43762,0.44057,0.43764,0.43769,0.43497,0.43208,0.43049,0.43416,0.43195,0.43595,0.43466,0.43542,0.4373,0.44057,0.43762,0.43256,0.42536,0.42969,0.44281,0.43916,0.43482,0.42634,0.42557,0.41312,0.41114,0.40081,0.38423,0.37726,0.37438,0.34399,0.33894,0.33929,0.35486,0.36392,0.36789,0.37016,0.36801,0.36754,0.36713,0.37033,0.36803,0.36824,0.36701,0.36532,0.36625,0.36523,0.36735,0.36992,0.36409,0.36771,0.36785,0.36717,0.362,0.3646,0.36541,0.36633,0.36376,0.36857,0.3678,0.36303,0.36879,0.36663,0.3687,0.37149,0.36784,0.36824,0.36847,0.36733,0.36794,0.36765,0.36589,0.36989,0.36858,0.3692,0.37091,0.36995,0.36967,0.36965,0.36969,0.36808,0.36905,0.36832,0.37036,0.37154,0.37201,0.37253,0.37193,0.37194,0.37621,0.37972,0.38657,0.39548,0.41295,0.42068,0.43611,0.45175,0.45122,0.4621,0.46594,0.46323,0.45875,0.45856,0.45421,0.46746,0.45164,0.45324,0.45647,0.4589,0.45214,0.44671,0.43979,0.43278,0.43063,0.43311,0.43079,0.43591,0.43437,0.43986,0.44472,0.4365,0.44193,0.4355,0.43226,0.43063,0.43671,0.43154,0.43124,0.43991,0.42993,0.43001,0.43826,0.42453,0.42291,0.42609,0.43693,0.42706,0.42737,0.41752,0.42822,0.42986,0.42403,0.42051,0.42298,0.42217,0.4194,0.40535,0.40433,0.39109,0.37848,0.34386,0.34686,0.35532,0.3594,0.36859,0.37405,0.37087,0.37257,0.37242,0.37173,0.36775,0.37138,0.37102,0.37108,0.36957,0.37115,0.36955,0.36928,0.36627,0.36847,0.36895,0.36636,0.36596,0.35991,0.36677,0.36739,0.36814,0.3701,0.36918,0.36606,0.36869,0.36848,0.36622,0.36834,0.36811,0.36714,0.36836,0.36875,0.36285,0.36876,0.3687,0.36151,0.36682,0.36933,0.371,0.37152,0.37032,0.37163,0.37366,0.3738,0.37363,0.37086,0.37102,0.37594,0.37694,0.3774,0.37663,0.37704,0.37297,0.37808,0.38202,0.3896,0.39112,0.442,0.44022,0.46093,0.4598,0.46432,0.46923,0.46479,0.45823,0.45668,0.45179,0.44669,0.44758,0.45052,0.45844,0.44225,0.44074,0.43983,0.4436,0.43971,0.43143,0.43533,0.44001,0.44877,0.44318,0.43617,0.43862,0.43934,0.43419,0.43006,0.42961,0.43633,0.43142,0.43366,0.43133,0.43133,0.43158,0.43989,0.43956,0.4248,0.42361,0.43224,0.4246,0.42807,0.43173,0.42956,0.4271,0.42286,0.42309,0.42792,0.43107,0.43015,0.42282,0.41221,0.39698,0.38751,0.38075,0.37059,0.37073,0.35614,0.35503,0.3577,0.35984,0.36799,0.37307,0.37562,0.37443,0.37374,0.37479,0.37427,0.3711,0.3709,0.37008,0.37034,0.3712,0.36564,0.36977,0.37216,0.37228,0.36887,0.37029,0.37369,0.37013,0.36997,0.36969,0.36791,0.36857,0.36744,0.36522,0.36641,0.36803,0.36729,0.36813,0.3704,0.36859,0.36809,0.3719,0.37345,0.3712,0.37021,0.37262,0.36839,0.3713,0.36539,0.37048,0.36954,0.36938,0.37311,0.3714,0.37008,0.37015,0.37056,0.37131,0.37099,0.37332,0.37392,0.37389,0.37333,0.3736,0.37493,0.37651,0.37969,0.37983,0.38372,0.39108,0.40215,0.44258,0.44499,0.44671,0.46647,0.46473,0.48271,0.46654,0.45778,0.45708,0.47214,0.46109,0.4609,0.45011,0.4628,0.45156,0.44611,0.44308,0.45127,0.44322,0.44295,0.44234,0.44018,0.44405,0.44175,0.45194,0.44306,0.44014,0.44067,0.44084,0.44109,0.43629,0.45202,0.43788,0.43926,0.43626,0.43765,0.42937,0.43753,0.4386,0.44245,0.43199,0.43571,0.42547,0.43492,0.43814,0.43074,0.43215,0.43762,0.43565,0.41709,0.41432,0.42346,0.40858,0.41259,0.39794,0.38847,0.38547,0.37853,0.37551,0.36757,0.3584,0.37039,0.37064,0.37617,0.37399,0.37473,0.37746,0.3762,0.37434,0.37133,0.37378,0.37283,0.37375,0.37252,0.37303,0.37049,0.37065,0.37127,0.37319,0.37254,0.37374,0.37351,0.37028,0.37196,0.37104,0.36995,0.37316,0.37236,0.37388,0.37079,0.3717,0.3727,0.37058,0.36918,0.37074,0.37129,0.37019,0.3722,0.36394,0.37108,0.37372,0.37548,0.37495,0.37462,0.37781,0.37849,0.3767,0.37494,0.37397,0.37665,0.37547,0.37577,0.37835,0.38116,0.3809,0.38927,0.38589,0.38476,0.39771,0.40386,0.43327,0.4417,0.46189,0.47864,0.47118,0.48555,0.47945,0.46678,0.46122,0.46242,0.45853,0.45318,0.465,0.44951,0.45343,0.453,0.45266,0.44802,0.4476,0.4454,0.45014,0.44486,0.44682,0.4484,0.44555,0.45413,0.4455,0.45493,0.44807,0.44594,0.45423,0.44172,0.45127,0.44512,0.44415,0.43719,0.4394,0.43956,0.4349,0.44086,0.44908,0.44531,0.43391,0.43016,0.43027,0.44154,0.42929,0.43251,0.43358,0.43816,0.42322,0.41221,0.41165,0.40702,0.40102,0.38018,0.35538,0.36623,0.37612,0.38188,0.37899,0.37728,0.37821,0.37974,0.37677,0.3759,0.3771,0.37513,0.37332,0.37438,0.37499,0.37248,0.37079,0.3743,0.37244,0.36899,0.37328,0.37251,0.37355,0.36855,0.37279,0.3736,0.37312,0.37244,0.37358,0.37004,0.37488,0.36907,0.37019,0.36897,0.37258,0.37099,0.37146,0.37124,0.37395,0.37406,0.37402,0.37261,0.36628,0.37177,0.37086,0.37017,0.3734,0.37312,0.3726,0.37305,0.37051,0.37263,0.37271,0.37523,0.37284,0.37467,0.37499,0.37428,0.3758,0.37689,0.37748,0.37676,0.37804,0.37997,0.38203,0.38663,0.41862,0.44951,0.44286,0.44608,0.45814,0.48115,0.46895,0.47135,0.46783,0.46445,0.47403,0.46115,0.47119,0.45494,0.45766,0.4528,0.4574,0.45343,0.45875,0.44898,0.44638,0.45164,0.44385,0.4442,0.44465,0.44395,0.44666,0.44133,0.44082,0.4399,0.4389,0.45509,0.44223,0.43831,0.44233,0.43865,0.43794,0.44334,0.45118,0.44862,0.43502,0.43483,0.44165,0.43641,0.43068,0.42875,0.42593,0.42592,0.4244,0.41921,0.42901,0.41643,0.411,0.4064,0.38609,0.37442,0.36909,0.3694,0.36817,0.37252,0.36966,0.37201,0.37393,0.37489,0.37854,0.37699,0.37601,0.37376,0.3741,0.37363,0.3754,0.37287,0.37129,0.37053,0.37314,0.37638,0.37714,0.37273,0.37467,0.37269,0.36825,0.37401,0.3726,0.37245,0.37466,0.3733,0.37268,0.36996,0.37174,0.37239,0.37693,0.37209,0.37199,0.37257,0.37087,0.36949,0.37157,0.37389,0.37316,0.37306,0.37076,0.37267,0.37419,0.37435,0.37343,0.37329,0.37236,0.3717,0.37244,0.37346,0.37329,0.37329,0.37467,0.37611,0.37754,0.37408,0.37821,0.37786,0.37858,0.37702,0.37798,0.37848,0.38105,0.39413,0.40944,0.44142,0.4482,0.47905,0.47517,0.48113,0.47216,0.48751,0.46835,0.47755,0.47797,0.46107,0.45808,0.45637,0.46064,0.45864,0.46109,0.47005,0.45814,0.45431,0.45958,0.45857,0.45612,0.45557,0.45373,0.46041,0.45318,0.46196,0.45219,0.44952,0.4589,0.44965,0.44883,0.45923,0.44914,0.45076,0.45214,0.45219,0.451,0.4468,0.45869,0.45302,0.44141,0.44528,0.4401,0.44585,0.45154,0.4533,0.44739,0.43601,0.42572,0.41962,0.40043,0.3783,0.37956,0.36964,0.36552,0.36392,0.37003,0.37129,0.37561,0.3776,0.37564,0.37745,0.37887,0.38111,0.37838,0.3781,0.37367,0.36656,0.37336,0.37562,0.37379,0.37537,0.37507,0.37564,0.37332,0.37521,0.37059,0.37055,0.37213,0.36958,0.37235,0.37329,0.3739,0.37146,0.37415,0.37248,0.36921,0.36954,0.37063,0.36862,0.36858,0.37167,0.37003,0.37185,0.37083,0.37135,0.37311,0.37419,0.37411,0.37195,0.37099,0.37077,0.374,0.37122,0.37136,0.37435,0.37301,0.3724,0.37478,0.37676,0.37783,0.37681,0.37713,0.37501,0.3763,0.37916,0.38375,0.40109,0.43205,0.43528,0.44798,0.45237,0.4506,0.46135,0.46138,0.47971,0.45992,0.4676,0.46182,0.46099,0.47106,0.4552,0.46705,0.45417,0.45476,0.45368,0.45108,0.46025,0.45134,0.44977,0.44846,0.45817,0.45001,0.44824,0.45189,0.45073,0.44936,0.44639,0.4465,0.45989,0.44995,0.4516,0.45815,0.4486,0.44479,0.44561,0.4486,0.44304,0.44628,0.45689,0.45538,0.44367,0.4417,0.44071,0.43903,0.45021,0.45109,0.43997,0.44401,0.43046,0.43283,0.41929,0.41977,0.40928,0.39857,0.38536,0.33899,0.35048,0.37836,0.37854,0.37806,0.37805,0.37701,0.37602,0.37726,0.37786,0.37518,0.37568,0.37431,0.37558,0.3754,0.37748,0.37411,0.37658,0.37856,0.37367,0.37509,0.37493,0.37413,0.37547,0.37363,0.37359,0.36992,0.37199,0.37227,0.37455,0.37403,0.37677,0.37456,0.37373,0.3705,0.37021,0.37428,0.37454,0.3744,0.37292,0.3752,0.37159,0.37332,0.37698,0.37621,0.3767,0.37639,0.37375,0.37543,0.37396,0.37556,0.37906,0.3716,0.37749,0.3754,0.3764,0.37882,0.38087,0.38137,0.38018,0.37889,0.38065,0.38195,0.38132,0.3892,0.41293,0.41712,0.42994,0.45271,0.47169,0.4839,0.4802,0.47789,0.47994,0.46052,0.46816,0.46091,0.46135,0.46234,0.46053,0.46887,0.46152,0.45649,0.46066,0.48013,0.45833,0.46869,0.45851,0.45547,0.45843,0.45626,0.46306,0.46613,0.45571,0.44908,0.46146,0.4555,0.45559,0.45159,0.44541,0.45177,0.44806,0.4568,0.45001,0.45834,0.45531,0.44433,0.43978,0.46774,0.44954,0.43847,0.45622,0.45377,0.45437,0.43995,0.45234,0.43193,0.43168,0.40648,0.40544,0.38956,0.39765,0.37909,0.3762,0.34971,0.3515,0.36062,0.37263,0.37755,0.37593,0.37616,0.37624,0.37704,0.37743,0.37636,0.37413,0.37557,0.37433,0.37229,0.37574,0.37598,0.37615,0.3709,0.3704,0.37389,0.37068,0.37705,0.37475,0.37416,0.3747,0.37033,0.37537,0.37423,0.3735,0.37369,0.37328,0.36994,0.37114,0.37178,0.37545,0.37644,0.37761,0.377,0.37375,0.37545,0.37554,0.3719,0.37141,0.37393,0.37531,0.37659,0.37433,0.37397,0.37604,0.37264,0.37622,0.37979,0.37844,0.3791,0.3772,0.37934,0.3793,0.38417,0.38946,0.39763,0.39381,0.39857,0.41317,0.44274,0.4664,0.49167,0.48662,0.50251,0.48394,0.49246,0.48601,0.46645,0.46266,0.47007,0.47098,0.45595,0.45466,0.45214,0.45719,0.45145,0.46426,0.45227,0.4603,0.45035,0.44954,0.44725,0.45729,0.45092,0.44555,0.44647,0.45309,0.44406,0.44363,0.44917,0.44896,0.44372,0.44102,0.43965,0.44273,0.44135,0.44671,0.43994,0.43949,0.44295,0.44444,0.44896,0.44305,0.44304,0.44639,0.43474,0.43829,0.45531,0.43884,0.43739,0.43072,0.42829,0.42447,0.4182,0.40921,0.40462,0.3853,0.37268,0.36396,0.36929,0.36976,0.37681,0.37709,0.37948,0.3784,0.37696,0.37833,0.37833,0.37324,0.37107,0.3746,0.37803,0.37464,0.37395,0.37327,0.37118,0.37466,0.37285,0.37851,0.37693,0.37414,0.37259,0.37843,0.3735,0.3772,0.37433,0.37403,0.37472,0.37149,0.37299,0.37531,0.37555,0.37637,0.37827,0.37772,0.37823,0.37301,0.37409,0.3692,0.37357,0.37242,0.37415,0.37422,0.37557,0.37589,0.37575,0.37496,0.37392,0.37351,0.37528,0.37775,0.37536,0.37544,0.37885,0.37867,0.38062,0.38405,0.38709,0.39504,0.42206,0.42691,0.44884,0.47607,0.48267,0.48007,0.47307,0.47852,0.47904,0.46485,0.46133,0.46621,0.45857,0.46147,0.46263,0.45863,0.46925,0.46117,0.45965,0.45814,0.45426,0.45759,0.45706,0.45048,0.45806,0.46482,0.45582,0.45461,0.45825,0.45736,0.45179,0.45492,0.45292,0.45078,0.44235,0.44204,0.44573,0.44617,0.4453,0.44566,0.44959,0.4519,0.44831,0.4512,0.4517,0.44156,0.45141,0.44395,0.45047,0.44851,0.44796,0.44621,0.43285,0.42662,0.42728,0.42631,0.41905,0.41587,0.40176,0.35074,0.35199,0.36979,0.37226,0.37894,0.37996,0.37876,0.37766,0.37717,0.37847,0.37999,0.37803,0.37634,0.37609,0.37816,0.37807,0.37707,0.3788,0.37624,0.37448,0.37489,0.37488,0.37273,0.37522,0.37204,0.37435,0.37904,0.37754,0.37581,0.37317,0.37701,0.37233,0.37626,0.37384,0.37524,0.37472,0.3721,0.37521,0.37596,0.37815,0.37538,0.37696,0.37604,0.37678,0.37834,0.37716,0.37682,0.37859,0.37817,0.38238,0.37897,0.38509,0.38166,0.38284,0.38314,0.38543,0.38563,0.39056,0.41052,0.40505,0.41808,0.43917,0.4581,0.46838,0.486,0.49063,0.47335,0.46676,0.46808,0.46735,0.46193,0.46837,0.45937,0.46444,0.45456,0.45435,0.45337,0.45371,0.45408,0.45074,0.45149,0.45295,0.46365,0.4484,0.4523,0.45027,0.44919,0.45044,0.4499,0.44614,0.44637,0.44924,0.44809,0.44276,0.44534,0.44113,0.44738,0.44884,0.44164,0.45407,0.45097,0.44041,0.43785,0.44111,0.44078,0.43703,0.44789,0.44078,0.43771,0.43471,0.42094,0.41275,0.36922,0.36306,0.35647,0.37066,0.3815,0.3808,0.38026,0.38002,0.38096,0.37961,0.38023,0.38023,0.38031,0.37612,0.37767,0.37522,0.36532,0.37201,0.37365,0.37493,0.37945,0.38007,0.3789,0.36713,0.37637,0.37408,0.37768,0.38083,0.37764,0.37326,0.37546,0.37886,0.378,0.37606,0.37712,0.3755,0.37136,0.3692,0.37616,0.37574,0.37589,0.37716,0.37871,0.37658,0.37838,0.37748,0.38008,0.3803,0.37821,0.37804,0.37708,0.37662,0.3778,0.3803,0.37802,0.37996,0.38025,0.38312,0.38219,0.37975,0.37963,0.37987,0.3818,0.38019,0.38165,0.38782,0.40787,0.43116,0.44975,0.46664,0.47044,0.46843,0.46972,0.46472,0.47326,0.45451,0.45643,0.45628,0.4549,0.45691,0.4642,0.45445,0.44897,0.45419,0.45169,0.4486,0.4564,0.44967,0.44722,0.44759,0.44776,0.45082,0.44528,0.44558,0.44613,0.45047,0.44872,0.44409,0.45084,0.45046,0.4566,0.45238,0.44583,0.44382,0.44938,0.44739,0.44045,0.43968,0.43925,0.43974,0.45042,0.45002,0.43793,0.43949,0.43084,0.42859],"showlegend":false,"mode":"line","type":"scatter","marker":{"color":"rgba(31,119,180,1)","line":{"color":"rgba(31,119,180,1)"}},"error_y":{"color":"rgba(31,119,180,1)"},"error_x":{"color":"rgba(31,119,180,1)"},"line":{"color":"rgba(31,119,180,1)"},"xaxis":"x","yaxis":"y","frame":null},{"x":["2008-01-06","2008-01-07","2008-01-08","2008-01-09","2008-01-10","2008-01-11","2008-01-12","2008-01-13","2008-01-14","2008-01-15","2008-01-16","2008-01-17","2008-01-18","2008-01-19","2008-01-20","2008-01-21","2008-01-22","2008-01-23","2008-01-24","2008-01-25","2008-01-26","2008-01-27","2008-01-28","2008-01-29","2008-01-30","2008-01-31","2008-02-01","2008-02-02","2008-02-03","2008-02-04","2008-02-05","2008-02-06","2008-02-07","2008-02-08","2008-02-09","2008-02-10","2008-02-11","2008-02-12","2008-02-13","2008-02-14","2008-02-15","2008-02-16","2008-02-17","2008-02-18","2008-02-19","2008-02-20","2008-02-21","2008-02-22","2008-02-23","2008-02-24","2008-02-25","2008-02-26","2008-02-27","2008-02-28","2008-02-29","2008-03-01","2008-03-02","2008-03-03","2008-03-04","2008-03-05","2008-03-06","2008-03-07","2008-03-08","2008-03-09","2008-03-10","2008-03-11","2008-03-12","2008-03-13","2008-03-14","2008-03-15","2008-03-16","2008-03-17","2008-03-18","2008-03-19","2008-03-20","2008-03-21","2008-03-22","2008-03-23","2008-03-24","2008-03-25","2008-03-26","2008-03-27","2008-03-28","2008-03-29","2008-03-30","2008-03-31","2008-04-01","2008-04-02","2008-04-03","2008-04-04","2008-04-05","2008-04-06","2008-04-07","2008-04-08","2008-04-09","2008-04-10","2008-04-11","2008-04-12","2008-04-13","2008-04-14","2008-04-15","2008-04-16","2008-04-17","2008-04-18","2008-04-19","2008-04-20","2008-04-21","2008-04-22","2008-04-23","2008-04-24","2008-04-25","2008-04-26","2008-04-27","2008-04-28","2008-04-29","2008-04-30","2008-05-01","2008-05-02","2008-05-03","2008-05-04","2008-05-05","2008-05-06","2008-05-07","2008-05-08","2008-05-09","2008-05-10","2008-05-11","2008-05-12","2008-05-13","2008-05-14","2008-05-15","2008-05-16","2008-05-17","2008-05-18","2008-05-19","2008-05-20","2008-05-21","2008-05-22","2008-05-23","2008-05-24","2008-05-25","2008-05-26","2008-05-27","2008-05-28","2008-05-29","2008-05-30","2008-05-31","2008-06-01","2008-06-02","2008-06-03","2008-06-04","2008-06-05","2008-06-06","2008-06-07","2008-06-08","2008-06-09","2008-06-10","2008-06-11","2008-06-12","2008-06-13","2008-06-14","2008-06-15","2008-06-16","2008-06-17","2008-06-18","2008-06-19","2008-06-20","2008-06-21","2008-06-22","2008-06-23","2008-06-24","2008-06-25","2008-06-26","2008-06-27","2008-06-28","2008-06-29","2008-06-30","2008-07-01","2008-07-02","2008-07-03","2008-07-04","2008-07-05","2008-07-06","2008-07-07","2008-07-08","2008-07-09","2008-07-10","2008-07-11","2008-07-12","2008-07-13","2008-07-14","2008-07-15","2008-07-16","2008-07-17","2008-07-18","2008-07-19","2008-07-20","2008-07-21","2008-07-22","2008-07-23","2008-07-24","2008-07-25","2008-07-26","2008-07-27","2008-07-28","2008-07-29","2008-07-30","2008-07-31","2008-08-01","2008-08-02","2008-08-03","2008-08-04","2008-08-05","2008-08-06","2008-08-07","2008-08-08","2008-08-09","2008-08-10","2008-08-11","2008-08-12","2008-08-13","2008-08-14","2008-08-15","2008-08-16","2008-08-17","2008-08-18","2008-08-19","2008-08-20","2008-08-21","2008-08-22","2008-08-23","2008-08-24","2008-08-25","2008-08-26","2008-08-27","2008-08-28","2008-08-29","2008-08-30","2008-08-31","2008-09-01","2008-09-02","2008-09-03","2008-09-04","2008-09-05","2008-09-06","2008-09-07","2008-09-08","2008-09-09","2008-09-10","2008-09-11","2008-09-12","2008-09-13","2008-09-14","2008-09-15","2008-09-16","2008-09-17","2008-09-18","2008-09-19","2008-09-20","2008-09-21","2008-09-22","2008-09-23","2008-09-24","2008-09-25","2008-09-26","2008-09-27","2008-09-28","2008-09-29","2008-09-30","2008-10-01","2008-10-02","2008-10-03","2008-10-04","2008-10-05","2008-10-06","2008-10-07","2008-10-08","2008-10-09","2008-10-10","2008-10-11","2008-10-12","2008-10-13","2008-10-14","2008-10-15","2008-10-16","2008-10-17","2008-10-18","2008-10-19","2008-10-20","2008-10-21","2008-10-22","2008-10-23","2008-10-24","2008-10-25","2008-10-26","2008-10-27","2008-10-28","2008-10-29","2008-10-30","2008-10-31","2008-11-01","2008-11-02","2008-11-03","2008-11-04","2008-11-05","2008-11-06","2008-11-07","2008-11-08","2008-11-09","2008-11-10","2008-11-11","2008-11-12","2008-11-13","2008-11-14","2008-11-15","2008-11-16","2008-11-17","2008-11-18","2008-11-19","2008-11-20","2008-11-21","2008-11-22","2008-11-23","2008-11-24","2008-11-25","2008-11-26","2008-11-27","2008-11-28","2008-11-29","2008-11-30","2008-12-01","2008-12-02","2008-12-03","2008-12-04","2008-12-05","2008-12-06","2008-12-07","2008-12-08","2008-12-09","2008-12-10","2008-12-11","2008-12-12","2008-12-13","2008-12-14","2008-12-15","2008-12-16","2008-12-17","2008-12-18","2008-12-19","2008-12-20","2008-12-21","2008-12-22","2008-12-23","2008-12-24","2008-12-25","2008-12-26","2008-12-27","2008-12-28","2008-12-29","2008-12-30","2008-12-31","2009-01-01","2009-01-02","2009-01-03","2009-01-04","2009-01-05","2009-01-06","2009-01-07","2009-01-08","2009-01-09","2009-01-10","2009-01-11","2009-01-12","2009-01-13","2009-01-14","2009-01-15","2009-01-16","2009-01-17","2009-01-18","2009-01-19","2009-01-20","2009-01-21","2009-01-22","2009-01-23","2009-01-24","2009-01-25","2009-01-26","2009-01-27","2009-01-28","2009-01-29","2009-01-30","2009-01-31","2009-02-01","2009-02-02","2009-02-03","2009-02-04","2009-02-05","2009-02-06","2009-02-07","2009-02-08","2009-02-09","2009-02-10","2009-02-11","2009-02-12","2009-02-13","2009-02-14","2009-02-15","2009-02-16","2009-02-17","2009-02-18","2009-02-19","2009-02-20","2009-02-21","2009-02-22","2009-02-23","2009-02-24","2009-02-25","2009-02-26","2009-02-27","2009-02-28","2009-03-01","2009-03-02","2009-03-03","2009-03-04","2009-03-05","2009-03-06","2009-03-07","2009-03-08","2009-03-09","2009-03-10","2009-03-11","2009-03-12","2009-03-13","2009-03-14","2009-03-15","2009-03-16","2009-03-17","2009-03-18","2009-03-19","2009-03-20","2009-03-21","2009-03-22","2009-03-23","2009-03-24","2009-03-25","2009-03-26","2009-03-27","2009-03-28","2009-03-29","2009-03-30","2009-03-31","2009-04-01","2009-04-02","2009-04-03","2009-04-04","2009-04-05","2009-04-06","2009-04-07","2009-04-08","2009-04-09","2009-04-10","2009-04-11","2009-04-12","2009-04-13","2009-04-14","2009-04-15","2009-04-16","2009-04-17","2009-04-18","2009-04-19","2009-04-20","2009-04-21","2009-04-22","2009-04-23","2009-04-24","2009-04-25","2009-04-26","2009-04-27","2009-04-28","2009-04-29","2009-04-30","2009-05-01","2009-05-02","2009-05-03","2009-05-04","2009-05-05","2009-05-06","2009-05-07","2009-05-08","2009-05-09","2009-05-10","2009-05-11","2009-05-12","2009-05-13","2009-05-14","2009-05-15","2009-05-16","2009-05-17","2009-05-18","2009-05-19","2009-05-20","2009-05-21","2009-05-22","2009-05-23","2009-05-24","2009-05-25","2009-05-26","2009-05-27","2009-05-28","2009-05-29","2009-05-30","2009-05-31","2009-06-01","2009-06-02","2009-06-03","2009-06-04","2009-06-05","2009-06-06","2009-06-07","2009-06-08","2009-06-09","2009-06-10","2009-06-11","2009-06-12","2009-06-13","2009-06-14","2009-06-15","2009-06-16","2009-06-17","2009-06-18","2009-06-19","2009-06-20","2009-06-21","2009-06-22","2009-06-23","2009-06-24","2009-06-25","2009-06-26","2009-06-27","2009-06-28","2009-06-29","2009-06-30","2009-07-01","2009-07-02","2009-07-03","2009-07-04","2009-07-05","2009-07-06","2009-07-07","2009-07-08","2009-07-09","2009-07-10","2009-07-11","2009-07-12","2009-07-13","2009-07-14","2009-07-15","2009-07-16","2009-07-17","2009-07-18","2009-07-19","2009-07-20","2009-07-21","2009-07-22","2009-07-23","2009-07-24","2009-07-25","2009-07-26","2009-07-27","2009-07-28","2009-07-29","2009-07-30","2009-07-31","2009-08-01","2009-08-02","2009-08-03","2009-08-04","2009-08-05","2009-08-06","2009-08-07","2009-08-08","2009-08-09","2009-08-10","2009-08-11","2009-08-12","2009-08-13","2009-08-14","2009-08-15","2009-08-16","2009-08-17","2009-08-18","2009-08-19","2009-08-20","2009-08-21","2009-08-22","2009-08-23","2009-08-24","2009-08-25","2009-08-26","2009-08-27","2009-08-28","2009-08-29","2009-08-30","2009-08-31","2009-09-01","2009-09-02","2009-09-03","2009-09-04","2009-09-05","2009-09-06","2009-09-07","2009-09-08","2009-09-09","2009-09-10","2009-09-11","2009-09-12","2009-09-13","2009-09-14","2009-09-15","2009-09-16","2009-09-17","2009-09-18","2009-09-19","2009-09-20","2009-09-21","2009-09-22","2009-09-23","2009-09-24","2009-09-25","2009-09-26","2009-09-27","2009-09-28","2009-09-29","2009-09-30","2009-10-01","2009-10-02","2009-10-03","2009-10-04","2009-10-05","2009-10-06","2009-10-07","2009-10-08","2009-10-09","2009-10-10","2009-10-11","2009-10-12","2009-10-13","2009-10-14","2009-10-15","2009-10-16","2009-10-17","2009-10-18","2009-10-19","2009-10-20","2009-10-21","2009-10-22","2009-10-23","2009-10-24","2009-10-25","2009-10-26","2009-10-27","2009-10-28","2009-10-29","2009-10-30","2009-10-31","2009-11-01","2009-11-02","2009-11-03","2009-11-04","2009-11-05","2009-11-06","2009-11-07","2009-11-08","2009-11-09","2009-11-10","2009-11-11","2009-11-12","2009-11-13","2009-11-14","2009-11-15","2009-11-16","2009-11-17","2009-11-18","2009-11-19","2009-11-20","2009-11-21","2009-11-22","2009-11-23","2009-11-24","2009-11-25","2009-11-26","2009-11-27","2009-11-28","2009-11-29","2009-11-30","2009-12-01","2009-12-02","2009-12-03","2009-12-04","2009-12-05","2009-12-06","2009-12-07","2009-12-08","2009-12-09","2009-12-10","2009-12-11","2009-12-12","2009-12-13","2009-12-14","2009-12-15","2009-12-16","2009-12-17","2009-12-18","2009-12-19","2009-12-20","2009-12-21","2009-12-22","2009-12-23","2009-12-24","2009-12-25","2009-12-26","2009-12-27","2009-12-28","2009-12-29","2009-12-30","2009-12-31","2010-01-01","2010-01-02","2010-01-03","2010-01-04","2010-01-05","2010-01-06","2010-01-07","2010-01-08","2010-01-09","2010-01-10","2010-01-11","2010-01-12","2010-01-13","2010-01-14","2010-01-15","2010-01-16","2010-01-17","2010-01-18","2010-01-19","2010-01-20","2010-01-21","2010-01-22","2010-01-23","2010-01-24","2010-01-25","2010-01-26","2010-01-27","2010-01-28","2010-01-29","2010-01-30","2010-01-31","2010-02-01","2010-02-02","2010-02-03","2010-02-04","2010-02-05","2010-02-06","2010-02-07","2010-02-08","2010-02-09","2010-02-10","2010-02-11","2010-02-12","2010-02-13","2010-02-14","2010-02-15","2010-02-16","2010-02-17","2010-02-18","2010-02-19","2010-02-20","2010-02-21","2010-02-22","2010-02-23","2010-02-24","2010-02-25","2010-02-26","2010-02-27","2010-02-28","2010-03-01","2010-03-02","2010-03-03","2010-03-04","2010-03-05","2010-03-06","2010-03-07","2010-03-08","2010-03-09","2010-03-10","2010-03-11","2010-03-12","2010-03-13","2010-03-14","2010-03-15","2010-03-16","2010-03-17","2010-03-18","2010-03-19","2010-03-20","2010-03-21","2010-03-22","2010-03-23","2010-03-24","2010-03-25","2010-03-26","2010-03-27","2010-03-28","2010-03-29","2010-03-30","2010-03-31","2010-04-01","2010-04-02","2010-04-03","2010-04-04","2010-04-05","2010-04-06","2010-04-07","2010-04-08","2010-04-09","2010-04-10","2010-04-11","2010-04-12","2010-04-13","2010-04-14","2010-04-15","2010-04-16","2010-04-17","2010-04-18","2010-04-19","2010-04-20","2010-04-21","2010-04-22","2010-04-23","2010-04-24","2010-04-25","2010-04-26","2010-04-27","2010-04-28","2010-04-29","2010-04-30","2010-05-01","2010-05-02","2010-05-03","2010-05-04","2010-05-05","2010-05-06","2010-05-07","2010-05-08","2010-05-09","2010-05-10","2010-05-11","2010-05-12","2010-05-13","2010-05-14","2010-05-15","2010-05-16","2010-05-17","2010-05-18","2010-05-19","2010-05-20","2010-05-21","2010-05-22","2010-05-23","2010-05-24","2010-05-25","2010-05-26","2010-05-27","2010-05-28","2010-05-29","2010-05-30","2010-05-31","2010-06-01","2010-06-02","2010-06-03","2010-06-04","2010-06-05","2010-06-06","2010-06-07","2010-06-08","2010-06-09","2010-06-10","2010-06-11","2010-06-12","2010-06-13","2010-06-14","2010-06-15","2010-06-16","2010-06-17","2010-06-18","2010-06-19","2010-06-20","2010-06-21","2010-06-22","2010-06-23","2010-06-24","2010-06-25","2010-06-26","2010-06-27","2010-06-28","2010-06-29","2010-06-30","2010-07-01","2010-07-02","2010-07-03","2010-07-04","2010-07-05","2010-07-06","2010-07-07","2010-07-08","2010-07-09","2010-07-10","2010-07-11","2010-07-12","2010-07-13","2010-07-14","2010-07-15","2010-07-16","2010-07-17","2010-07-18","2010-07-19","2010-07-20","2010-07-21","2010-07-22","2010-07-23","2010-07-24","2010-07-25","2010-07-26","2010-07-27","2010-07-28","2010-07-29","2010-07-30","2010-07-31","2010-08-01","2010-08-02","2010-08-03","2010-08-04","2010-08-05","2010-08-06","2010-08-07","2010-08-08","2010-08-09","2010-08-10","2010-08-11","2010-08-12","2010-08-13","2010-08-14","2010-08-15","2010-08-16","2010-08-17","2010-08-18","2010-08-19","2010-08-20","2010-08-21","2010-08-22","2010-08-23","2010-08-24","2010-08-25","2010-08-26","2010-08-27","2010-08-28","2010-08-29","2010-08-30","2010-08-31","2010-09-01","2010-09-02","2010-09-03","2010-09-04","2010-09-05","2010-09-06","2010-09-07","2010-09-08","2010-09-09","2010-09-10","2010-09-11","2010-09-12","2010-09-13","2010-09-14","2010-09-15","2010-09-16","2010-09-17","2010-09-18","2010-09-19","2010-09-20","2010-09-21","2010-09-22","2010-09-23","2010-09-24","2010-09-25","2010-09-26","2010-09-27","2010-09-28","2010-09-29","2010-09-30","2010-10-01","2010-10-02","2010-10-03","2010-10-04","2010-10-05","2010-10-06","2010-10-07","2010-10-08","2010-10-09","2010-10-10","2010-10-11","2010-10-12","2010-10-13","2010-10-14","2010-10-15","2010-10-16","2010-10-17","2010-10-18","2010-10-19","2010-10-20","2010-10-21","2010-10-22","2010-10-23","2010-10-24","2010-10-25","2010-10-26","2010-10-27","2010-10-28","2010-10-29","2010-10-30","2010-10-31","2010-11-01","2010-11-02","2010-11-03","2010-11-04","2010-11-05","2010-11-06","2010-11-07","2010-11-08","2010-11-09","2010-11-10","2010-11-11","2010-11-12","2010-11-13","2010-11-14","2010-11-15","2010-11-16","2010-11-17","2010-11-18","2010-11-19","2010-11-20","2010-11-21","2010-11-22","2010-11-23","2010-11-24","2010-11-25","2010-11-26","2010-11-27","2010-11-28","2010-11-29","2010-11-30","2010-12-01","2010-12-02","2010-12-03","2010-12-04","2010-12-05","2010-12-06","2010-12-07","2010-12-08","2010-12-09","2010-12-10","2010-12-11","2010-12-12","2010-12-13","2010-12-14","2010-12-15","2010-12-16","2010-12-17","2010-12-18","2010-12-19","2010-12-20","2010-12-21","2010-12-22","2010-12-23","2010-12-24","2010-12-25","2010-12-26","2010-12-27","2010-12-28","2010-12-29","2010-12-30","2010-12-31","2011-01-01","2011-01-02","2011-01-03","2011-01-04","2011-01-05","2011-01-06","2011-01-07","2011-01-08","2011-01-09","2011-01-10","2011-01-11","2011-01-12","2011-01-13","2011-01-14","2011-01-15","2011-01-16","2011-01-17","2011-01-18","2011-01-19","2011-01-20","2011-01-21","2011-01-22","2011-01-23","2011-01-24","2011-01-25","2011-01-26","2011-01-27","2011-01-28","2011-01-29","2011-01-30","2011-01-31","2011-02-01","2011-02-02","2011-02-03","2011-02-04","2011-02-05","2011-02-06","2011-02-07","2011-02-08","2011-02-09","2011-02-10","2011-02-11","2011-02-12","2011-02-13","2011-02-14","2011-02-15","2011-02-16","2011-02-17","2011-02-18","2011-02-19","2011-02-20","2011-02-21","2011-02-22","2011-02-23","2011-02-24","2011-02-25","2011-02-26","2011-02-27","2011-02-28","2011-03-01","2011-03-02","2011-03-03","2011-03-04","2011-03-05","2011-03-06","2011-03-07","2011-03-08","2011-03-09","2011-03-10","2011-03-11","2011-03-12","2011-03-13","2011-03-14","2011-03-15","2011-03-16","2011-03-17","2011-03-18","2011-03-19","2011-03-20","2011-03-21","2011-03-22","2011-03-23","2011-03-24","2011-03-25","2011-03-26","2011-03-27","2011-03-28","2011-03-29","2011-03-30","2011-03-31","2011-04-01","2011-04-02","2011-04-03","2011-04-04","2011-04-05","2011-04-06","2011-04-07","2011-04-08","2011-04-09","2011-04-10","2011-04-11","2011-04-12","2011-04-13","2011-04-14","2011-04-15","2011-04-16","2011-04-17","2011-04-18","2011-04-19","2011-04-20","2011-04-21","2011-04-22","2011-04-23","2011-04-24","2011-04-25","2011-04-26","2011-04-27","2011-04-28","2011-04-29","2011-04-30","2011-05-01","2011-05-02","2011-05-03","2011-05-04","2011-05-05","2011-05-06","2011-05-07","2011-05-08","2011-05-09","2011-05-10","2011-05-11","2011-05-12","2011-05-13","2011-05-14","2011-05-15","2011-05-16","2011-05-17","2011-05-18","2011-05-19","2011-05-20","2011-05-21","2011-05-22","2011-05-23","2011-05-24","2011-05-25","2011-05-26","2011-05-27","2011-05-28","2011-05-29","2011-05-30","2011-05-31","2011-06-01","2011-06-02","2011-06-03","2011-06-04","2011-06-05","2011-06-06","2011-06-07","2011-06-08","2011-06-09","2011-06-10","2011-06-11","2011-06-12","2011-06-13","2011-06-14","2011-06-15","2011-06-16","2011-06-17","2011-06-18","2011-06-19","2011-06-20","2011-06-21","2011-06-22","2011-06-23","2011-06-24","2011-06-25","2011-06-26","2011-06-27","2011-06-28","2011-06-29","2011-06-30","2011-07-01","2011-07-02","2011-07-03","2011-07-04","2011-07-05","2011-07-06","2011-07-07","2011-07-08","2011-07-09","2011-07-10","2011-07-11","2011-07-12","2011-07-13","2011-07-14","2011-07-15","2011-07-16","2011-07-17","2011-07-18","2011-07-19","2011-07-20","2011-07-21","2011-07-22","2011-07-23","2011-07-24","2011-07-25","2011-07-26","2011-07-27","2011-07-28","2011-07-29","2011-07-30","2011-07-31","2011-08-01","2011-08-02","2011-08-03","2011-08-04","2011-08-05","2011-08-06","2011-08-07","2011-08-08","2011-08-09","2011-08-10","2011-08-11","2011-08-12","2011-08-13","2011-08-14","2011-08-15","2011-08-16","2011-08-17","2011-08-18","2011-08-19","2011-08-20","2011-08-21","2011-08-22","2011-08-23","2011-08-24","2011-08-25","2011-08-26","2011-08-27","2011-08-28","2011-08-29","2011-08-30","2011-08-31","2011-09-01","2011-09-02","2011-09-03","2011-09-04","2011-09-05","2011-09-06","2011-09-07","2011-09-08","2011-09-09","2011-09-10","2011-09-11","2011-09-12","2011-09-13","2011-09-14","2011-09-15","2011-09-16","2011-09-17","2011-09-18","2011-09-19","2011-09-20","2011-09-21","2011-09-22","2011-09-23","2011-09-24","2011-09-25","2011-09-26","2011-09-27","2011-09-28","2011-09-29","2011-09-30","2011-10-01","2011-10-02","2011-10-03","2011-10-04","2011-10-05","2011-10-06","2011-10-07","2011-10-08","2011-10-09","2011-10-10","2011-10-11","2011-10-12","2011-10-13","2011-10-14","2011-10-15","2011-10-16","2011-10-17","2011-10-18","2011-10-19","2011-10-20","2011-10-21","2011-10-22","2011-10-23","2011-10-24","2011-10-25","2011-10-26","2011-10-27","2011-10-28","2011-10-29","2011-10-30","2011-10-31","2011-11-01","2011-11-02","2011-11-03","2011-11-04","2011-11-05","2011-11-06","2011-11-07","2011-11-08","2011-11-09","2011-11-10","2011-11-11","2011-11-12","2011-11-13","2011-11-14","2011-11-15","2011-11-16","2011-11-17","2011-11-18","2011-11-19","2011-11-20","2011-11-21","2011-11-22","2011-11-23","2011-11-24","2011-11-25","2011-11-26","2011-11-27","2011-11-28","2011-11-29","2011-11-30","2011-12-01","2011-12-02","2011-12-03","2011-12-04","2011-12-05","2011-12-06","2011-12-07","2011-12-08","2011-12-09","2011-12-10","2011-12-11","2011-12-12","2011-12-13","2011-12-14","2011-12-15","2011-12-16","2011-12-17","2011-12-18","2011-12-19","2011-12-20","2011-12-21","2011-12-22","2011-12-23","2011-12-24","2011-12-25","2011-12-26","2011-12-27","2011-12-28","2011-12-29","2011-12-30","2011-12-31","2012-01-01","2012-01-02","2012-01-03","2012-01-04","2012-01-05","2012-01-06","2012-01-07","2012-01-08","2012-01-09","2012-01-10","2012-01-11","2012-01-12","2012-01-13","2012-01-14","2012-01-15","2012-01-16","2012-01-17","2012-01-18","2012-01-19","2012-01-20","2012-01-21","2012-01-22","2012-01-23","2012-01-24","2012-01-25","2012-01-26","2012-01-27","2012-01-28","2012-01-29","2012-01-30","2012-01-31","2012-02-01","2012-02-02","2012-02-03","2012-02-04","2012-02-05","2012-02-06","2012-02-07","2012-02-08","2012-02-09","2012-02-10","2012-02-11","2012-02-12","2012-02-13","2012-02-14","2012-02-15","2012-02-16","2012-02-17","2012-02-18","2012-02-19","2012-02-20","2012-02-21","2012-02-22","2012-02-23","2012-02-24","2012-02-25","2012-02-26","2012-02-27","2012-02-28","2012-02-29","2012-03-01","2012-03-02","2012-03-03","2012-03-04","2012-03-05","2012-03-06","2012-03-07","2012-03-08","2012-03-09","2012-03-10","2012-03-11","2012-03-12","2012-03-13","2012-03-14","2012-03-15","2012-03-16","2012-03-17","2012-03-18","2012-03-19","2012-03-20","2012-03-21","2012-03-22","2012-03-23","2012-03-24","2012-03-25","2012-03-26","2012-03-27","2012-03-28","2012-03-29","2012-03-30","2012-03-31","2012-04-01","2012-04-02","2012-04-03","2012-04-04","2012-04-05","2012-04-06","2012-04-07","2012-04-08","2012-04-09","2012-04-10","2012-04-11","2012-04-12","2012-04-13","2012-04-14","2012-04-15","2012-04-16","2012-04-17","2012-04-18","2012-04-19","2012-04-20","2012-04-21","2012-04-22","2012-04-23","2012-04-24","2012-04-25","2012-04-26","2012-04-27","2012-04-28","2012-04-29","2012-04-30","2012-05-01","2012-05-02","2012-05-03","2012-05-04","2012-05-05","2012-05-06","2012-05-07","2012-05-08","2012-05-09","2012-05-10","2012-05-11","2012-05-12","2012-05-13","2012-05-14","2012-05-15","2012-05-16","2012-05-17","2012-05-18","2012-05-19","2012-05-20","2012-05-21","2012-05-22","2012-05-23","2012-05-24","2012-05-25","2012-05-26","2012-05-27","2012-05-28","2012-05-29","2012-05-30","2012-05-31","2012-06-01","2012-06-02","2012-06-03","2012-06-04","2012-06-05","2012-06-06","2012-06-07","2012-06-08","2012-06-09","2012-06-10","2012-06-11","2012-06-12","2012-06-13","2012-06-14","2012-06-15","2012-06-16","2012-06-17","2012-06-18","2012-06-19","2012-06-20","2012-06-21","2012-06-22","2012-06-23","2012-06-24","2012-06-25","2012-06-26","2012-06-27","2012-06-28","2012-06-29","2012-06-30","2012-07-01","2012-07-02","2012-07-03","2012-07-04","2012-07-05","2012-07-06","2012-07-07","2012-07-08","2012-07-09","2012-07-10","2012-07-11","2012-07-12","2012-07-13","2012-07-14","2012-07-15","2012-07-16","2012-07-17","2012-07-18","2012-07-19","2012-07-20","2012-07-21","2012-07-22","2012-07-23","2012-07-24","2012-07-25","2012-07-26","2012-07-27","2012-07-28","2012-07-29","2012-07-30","2012-07-31","2012-08-01","2012-08-02","2012-08-03","2012-08-04","2012-08-05","2012-08-06","2012-08-07","2012-08-08","2012-08-09","2012-08-10","2012-08-11","2012-08-12","2012-08-13","2012-08-14","2012-08-15","2012-08-16","2012-08-17","2012-08-18","2012-08-19","2012-08-20","2012-08-21","2012-08-22","2012-08-23","2012-08-24","2012-08-25","2012-08-26","2012-08-27","2012-08-28","2012-08-29","2012-08-30","2012-08-31","2012-09-01","2012-09-02","2012-09-03","2012-09-04","2012-09-05","2012-09-06","2012-09-07","2012-09-08","2012-09-09","2012-09-10","2012-09-11","2012-09-12","2012-09-13","2012-09-14","2012-09-15","2012-09-16","2012-09-17","2012-09-18","2012-09-19","2012-09-20","2012-09-21","2012-09-22","2012-09-23","2012-09-24","2012-09-25","2012-09-26","2012-09-27","2012-09-28","2012-09-29","2012-09-30","2012-10-01","2012-10-02","2012-10-03","2012-10-04","2012-10-05","2012-10-06","2012-10-07","2012-10-08","2012-10-09","2012-10-10","2012-10-11","2012-10-12","2012-10-13","2012-10-14","2012-10-15","2012-10-16","2012-10-17","2012-10-18","2012-10-19","2012-10-20","2012-10-21","2012-10-22","2012-10-23","2012-10-24","2012-10-25","2012-10-26","2012-10-27","2012-10-28","2012-10-29","2012-10-30","2012-10-31","2012-11-01","2012-11-02","2012-11-03","2012-11-04","2012-11-05","2012-11-06","2012-11-07","2012-11-08","2012-11-09","2012-11-10","2012-11-11","2012-11-12","2012-11-13","2012-11-14","2012-11-15","2012-11-16","2012-11-17","2012-11-18","2012-11-19","2012-11-20","2012-11-21","2012-11-22","2012-11-23","2012-11-24","2012-11-25","2012-11-26","2012-11-27","2012-11-28","2012-11-29","2012-11-30","2012-12-01","2012-12-02","2012-12-03","2012-12-04","2012-12-05","2012-12-06","2012-12-07","2012-12-08","2012-12-09","2012-12-10","2012-12-11","2012-12-12","2012-12-13","2012-12-14","2012-12-15","2012-12-16","2012-12-17","2012-12-18","2012-12-19","2012-12-20","2012-12-21","2012-12-22","2012-12-23","2012-12-24","2012-12-25","2012-12-26","2012-12-27","2012-12-28","2012-12-29","2012-12-30","2012-12-31","2013-01-01","2013-01-02","2013-01-03","2013-01-04","2013-01-05","2013-01-06","2013-01-07","2013-01-08","2013-01-09","2013-01-10","2013-01-11","2013-01-12","2013-01-13","2013-01-14","2013-01-15","2013-01-16","2013-01-17","2013-01-18","2013-01-19","2013-01-20","2013-01-21","2013-01-22","2013-01-23","2013-01-24","2013-01-25","2013-01-26","2013-01-27","2013-01-28","2013-01-29","2013-01-30","2013-01-31","2013-02-01","2013-02-02","2013-02-03","2013-02-04","2013-02-05","2013-02-06","2013-02-07","2013-02-08","2013-02-09","2013-02-10","2013-02-11","2013-02-12","2013-02-13","2013-02-14","2013-02-15","2013-02-16","2013-02-17","2013-02-18","2013-02-19","2013-02-20","2013-02-21","2013-02-22","2013-02-23","2013-02-24","2013-02-25","2013-02-26","2013-02-27","2013-02-28","2013-03-01","2013-03-02","2013-03-03","2013-03-04","2013-03-05","2013-03-06","2013-03-07","2013-03-08","2013-03-09","2013-03-10","2013-03-11","2013-03-12","2013-03-13","2013-03-14","2013-03-15","2013-03-16","2013-03-17","2013-03-18","2013-03-19","2013-03-20","2013-03-21","2013-03-22","2013-03-23","2013-03-24","2013-03-25","2013-03-26","2013-03-27","2013-03-28","2013-03-29","2013-03-30","2013-03-31","2013-04-01","2013-04-02","2013-04-03","2013-04-04","2013-04-05","2013-04-06","2013-04-07","2013-04-08","2013-04-09","2013-04-10","2013-04-11","2013-04-12","2013-04-13","2013-04-14","2013-04-15","2013-04-16","2013-04-17","2013-04-18","2013-04-19","2013-04-20","2013-04-21","2013-04-22","2013-04-23","2013-04-24","2013-04-25","2013-04-26","2013-04-27","2013-04-28","2013-04-29","2013-04-30","2013-05-01","2013-05-02","2013-05-03","2013-05-04","2013-05-05","2013-05-06","2013-05-07","2013-05-08","2013-05-09","2013-05-10","2013-05-11","2013-05-12","2013-05-13","2013-05-14","2013-05-15","2013-05-16","2013-05-17","2013-05-18","2013-05-19","2013-05-20","2013-05-21","2013-05-22","2013-05-23","2013-05-24","2013-05-25","2013-05-26","2013-05-27","2013-05-28","2013-05-29","2013-05-30","2013-05-31","2013-06-01","2013-06-02","2013-06-03","2013-06-04","2013-06-05","2013-06-06","2013-06-07","2013-06-08","2013-06-09","2013-06-10","2013-06-11","2013-06-12","2013-06-13","2013-06-14","2013-06-15","2013-06-16","2013-06-17","2013-06-18","2013-06-19","2013-06-20","2013-06-21","2013-06-22","2013-06-23","2013-06-24","2013-06-25","2013-06-26","2013-06-27","2013-06-28","2013-06-29","2013-06-30","2013-07-01","2013-07-02","2013-07-03","2013-07-04","2013-07-05","2013-07-06","2013-07-07","2013-07-08","2013-07-09","2013-07-10","2013-07-11","2013-07-12","2013-07-13","2013-07-14","2013-07-15","2013-07-16","2013-07-17","2013-07-18","2013-07-19","2013-07-20","2013-07-21","2013-07-22","2013-07-23","2013-07-24","2013-07-25","2013-07-26","2013-07-27","2013-07-28","2013-07-29","2013-07-30","2013-07-31","2013-08-01","2013-08-02","2013-08-03","2013-08-04","2013-08-05","2013-08-06","2013-08-07","2013-08-08","2013-08-09","2013-08-10","2013-08-11","2013-08-12","2013-08-13","2013-08-14","2013-08-15","2013-08-16","2013-08-17","2013-08-18","2013-08-19","2013-08-20","2013-08-21","2013-08-22","2013-08-23","2013-08-24","2013-08-25","2013-08-26","2013-08-27","2013-08-28","2013-08-29","2013-08-30","2013-08-31","2013-09-01","2013-09-02","2013-09-03","2013-09-04","2013-09-05","2013-09-06","2013-09-07","2013-09-08","2013-09-09","2013-09-10","2013-09-11","2013-09-12","2013-09-13","2013-09-14","2013-09-15","2013-09-16","2013-09-17","2013-09-18","2013-09-19","2013-09-20","2013-09-21","2013-09-22","2013-09-23","2013-09-24","2013-09-25","2013-09-26","2013-09-27","2013-09-28","2013-09-29","2013-09-30","2013-10-01","2013-10-02","2013-10-03","2013-10-04","2013-10-05","2013-10-06","2013-10-07","2013-10-08","2013-10-09","2013-10-10","2013-10-11","2013-10-12","2013-10-13","2013-10-14","2013-10-15","2013-10-16","2013-10-17","2013-10-18","2013-10-19","2013-10-20","2013-10-21","2013-10-22","2013-10-23","2013-10-24","2013-10-25","2013-10-26","2013-10-27","2013-10-28","2013-10-29","2013-10-30","2013-10-31","2013-11-01","2013-11-02","2013-11-03","2013-11-04","2013-11-05","2013-11-06","2013-11-07","2013-11-08","2013-11-09","2013-11-10","2013-11-11","2013-11-12","2013-11-13","2013-11-14","2013-11-15","2013-11-16","2013-11-17","2013-11-18","2013-11-19","2013-11-20","2013-11-21","2013-11-22","2013-11-23","2013-11-24","2013-11-25","2013-11-26","2013-11-27","2013-11-28","2013-11-29","2013-11-30","2013-12-01","2013-12-02","2013-12-03","2013-12-04","2013-12-05","2013-12-06","2013-12-07","2013-12-08","2013-12-09","2013-12-10","2013-12-11","2013-12-12","2013-12-13","2013-12-14","2013-12-15","2013-12-16","2013-12-17","2013-12-18","2013-12-19","2013-12-20","2013-12-21","2013-12-22","2013-12-23","2013-12-24","2013-12-25","2013-12-26","2013-12-27","2013-12-28","2013-12-29","2013-12-30","2013-12-31","2014-01-01","2014-01-02","2014-01-03","2014-01-04","2014-01-05","2014-01-06","2014-01-07","2014-01-08","2014-01-09","2014-01-10","2014-01-11","2014-01-12","2014-01-13","2014-01-14","2014-01-15","2014-01-16","2014-01-17","2014-01-18","2014-01-19","2014-01-20","2014-01-21","2014-01-22","2014-01-23","2014-01-24","2014-01-25","2014-01-26","2014-01-27","2014-01-28","2014-01-29","2014-01-30","2014-01-31","2014-02-01","2014-02-02","2014-02-03","2014-02-04","2014-02-05","2014-02-06","2014-02-07","2014-02-08","2014-02-09","2014-02-10","2014-02-11","2014-02-12","2014-02-13","2014-02-14","2014-02-15","2014-02-16","2014-02-17","2014-02-18","2014-02-19","2014-02-20","2014-02-21","2014-02-22","2014-02-23","2014-02-24","2014-02-25","2014-02-26","2014-02-27","2014-02-28","2014-03-01","2014-03-02","2014-03-03","2014-03-04","2014-03-05","2014-03-06","2014-03-07","2014-03-08","2014-03-09","2014-03-10","2014-03-11","2014-03-12","2014-03-13","2014-03-14","2014-03-15","2014-03-16","2014-03-17","2014-03-18","2014-03-19","2014-03-20","2014-03-21","2014-03-22","2014-03-23","2014-03-24","2014-03-25","2014-03-26","2014-03-27","2014-03-28","2014-03-29","2014-03-30","2014-03-31","2014-04-01","2014-04-02","2014-04-03","2014-04-04","2014-04-05","2014-04-06","2014-04-07","2014-04-08","2014-04-09","2014-04-10","2014-04-11","2014-04-12","2014-04-13","2014-04-14","2014-04-15","2014-04-16","2014-04-17","2014-04-18","2014-04-19","2014-04-20","2014-04-21","2014-04-22","2014-04-23","2014-04-24","2014-04-25","2014-04-26","2014-04-27","2014-04-28","2014-04-29","2014-04-30","2014-05-01","2014-05-02","2014-05-03","2014-05-04","2014-05-05","2014-05-06","2014-05-07","2014-05-08","2014-05-09","2014-05-10","2014-05-11","2014-05-12","2014-05-13","2014-05-14","2014-05-15","2014-05-16","2014-05-17","2014-05-18","2014-05-19","2014-05-20","2014-05-21","2014-05-22","2014-05-23","2014-05-24","2014-05-25","2014-05-26","2014-05-27","2014-05-28","2014-05-29","2014-05-30","2014-05-31","2014-06-01","2014-06-02","2014-06-03","2014-06-04","2014-06-05","2014-06-06","2014-06-07","2014-06-08","2014-06-09","2014-06-10","2014-06-11","2014-06-12","2014-06-13","2014-06-14","2014-06-15","2014-06-16","2014-06-17","2014-06-18","2014-06-19","2014-06-20","2014-06-21","2014-06-22","2014-06-23","2014-06-24","2014-06-25","2014-06-26","2014-06-27","2014-06-28","2014-06-29","2014-06-30","2014-07-01","2014-07-02","2014-07-03","2014-07-04","2014-07-05","2014-07-06","2014-07-07","2014-07-08","2014-07-09","2014-07-10","2014-07-11","2014-07-12","2014-07-13","2014-07-14","2014-07-15","2014-07-16","2014-07-17","2014-07-18","2014-07-19","2014-07-20","2014-07-21","2014-07-22","2014-07-23","2014-07-24","2014-07-25","2014-07-26","2014-07-27","2014-07-28","2014-07-29","2014-07-30","2014-07-31","2014-08-01","2014-08-02","2014-08-03","2014-08-04","2014-08-05","2014-08-06","2014-08-07","2014-08-08","2014-08-09","2014-08-10","2014-08-11","2014-08-12","2014-08-13","2014-08-14","2014-08-15","2014-08-16","2014-08-17","2014-08-18","2014-08-19","2014-08-20","2014-08-21","2014-08-22","2014-08-23","2014-08-24","2014-08-25","2014-08-26","2014-08-27","2014-08-28","2014-08-29","2014-08-30","2014-08-31","2014-09-01","2014-09-02","2014-09-03","2014-09-04","2014-09-05","2014-09-06","2014-09-07","2014-09-08","2014-09-09","2014-09-10","2014-09-11","2014-09-12","2014-09-13","2014-09-14","2014-09-15","2014-09-16","2014-09-17","2014-09-18","2014-09-19","2014-09-20","2014-09-21","2014-09-22","2014-09-23","2014-09-24","2014-09-25","2014-09-26","2014-09-27","2014-09-28","2014-09-29","2014-09-30","2014-10-01","2014-10-02","2014-10-03","2014-10-04","2014-10-05","2014-10-06","2014-10-07","2014-10-08","2014-10-09","2014-10-10","2014-10-11","2014-10-12","2014-10-13","2014-10-14","2014-10-15","2014-10-16","2014-10-17","2014-10-18","2014-10-19","2014-10-20","2014-10-21","2014-10-22","2014-10-23","2014-10-24","2014-10-25","2014-10-26","2014-10-27","2014-10-28","2014-10-29","2014-10-30","2014-10-31","2014-11-01","2014-11-02","2014-11-03","2014-11-04","2014-11-05","2014-11-06","2014-11-07","2014-11-08","2014-11-09","2014-11-10","2014-11-11","2014-11-12","2014-11-13","2014-11-14","2014-11-15","2014-11-16","2014-11-17","2014-11-18","2014-11-19","2014-11-20","2014-11-21","2014-11-22","2014-11-23","2014-11-24","2014-11-25","2014-11-26","2014-11-27","2014-11-28","2014-11-29","2014-11-30","2014-12-01","2014-12-02","2014-12-03","2014-12-04","2014-12-05","2014-12-06","2014-12-07","2014-12-08","2014-12-09","2014-12-10","2014-12-11","2014-12-12","2014-12-13","2014-12-14","2014-12-15","2014-12-16","2014-12-17","2014-12-18","2014-12-19","2014-12-20","2014-12-21","2014-12-22","2014-12-23","2014-12-24","2014-12-25","2014-12-26","2014-12-27","2014-12-28","2014-12-29","2014-12-30","2014-12-31","2015-01-01","2015-01-02","2015-01-03","2015-01-04","2015-01-05","2015-01-06","2015-01-07","2015-01-08","2015-01-09","2015-01-10","2015-01-11","2015-01-12","2015-01-13","2015-01-14","2015-01-15","2015-01-16","2015-01-17","2015-01-18","2015-01-19","2015-01-20","2015-01-21","2015-01-22","2015-01-23","2015-01-24","2015-01-25","2015-01-26","2015-01-27","2015-01-28","2015-01-29","2015-01-30","2015-01-31","2015-02-01","2015-02-02","2015-02-03","2015-02-04","2015-02-05","2015-02-06","2015-02-07","2015-02-08","2015-02-09","2015-02-10","2015-02-11","2015-02-12","2015-02-13","2015-02-14","2015-02-15","2015-02-16","2015-02-17","2015-02-18","2015-02-19","2015-02-20","2015-02-21","2015-02-22","2015-02-23","2015-02-24","2015-02-25","2015-02-26","2015-02-27","2015-02-28","2015-03-01","2015-03-02","2015-03-03","2015-03-04","2015-03-05","2015-03-06","2015-03-07","2015-03-08","2015-03-09","2015-03-10","2015-03-11","2015-03-12","2015-03-13","2015-03-14","2015-03-15","2015-03-16","2015-03-17","2015-03-18","2015-03-19","2015-03-20","2015-03-21","2015-03-22","2015-03-23","2015-03-24","2015-03-25","2015-03-26","2015-03-27","2015-03-28","2015-03-29","2015-03-30","2015-03-31","2015-04-01","2015-04-02","2015-04-03","2015-04-04","2015-04-05","2015-04-06","2015-04-07","2015-04-08","2015-04-09","2015-04-10","2015-04-11","2015-04-12","2015-04-13","2015-04-14","2015-04-15","2015-04-16","2015-04-17","2015-04-18","2015-04-19","2015-04-20","2015-04-21","2015-04-22","2015-04-23","2015-04-24","2015-04-25","2015-04-26","2015-04-27","2015-04-28","2015-04-29","2015-04-30","2015-05-01","2015-05-02","2015-05-03","2015-05-04","2015-05-05","2015-05-06","2015-05-07","2015-05-08","2015-05-09","2015-05-10","2015-05-11","2015-05-12","2015-05-13","2015-05-14","2015-05-15","2015-05-16","2015-05-17","2015-05-18","2015-05-19","2015-05-20","2015-05-21","2015-05-22","2015-05-23","2015-05-24","2015-05-25","2015-05-26","2015-05-27","2015-05-28","2015-05-29","2015-05-30","2015-05-31","2015-06-01","2015-06-02","2015-06-03","2015-06-04","2015-06-05","2015-06-06","2015-06-07","2015-06-08","2015-06-09","2015-06-10","2015-06-11","2015-06-12","2015-06-13","2015-06-14","2015-06-15","2015-06-16","2015-06-17","2015-06-18","2015-06-19","2015-06-20","2015-06-21","2015-06-22","2015-06-23","2015-06-24","2015-06-25","2015-06-26","2015-06-27","2015-06-28","2015-06-29","2015-06-30","2015-07-01","2015-07-02","2015-07-03","2015-07-04","2015-07-05","2015-07-06","2015-07-07","2015-07-08","2015-07-09","2015-07-10","2015-07-11","2015-07-12","2015-07-13","2015-07-14","2015-07-15","2015-07-16","2015-07-17","2015-07-18","2015-07-19","2015-07-20","2015-07-21","2015-07-22","2015-07-23","2015-07-24","2015-07-25","2015-07-26","2015-07-27","2015-07-28","2015-07-29","2015-07-30","2015-07-31","2015-08-01","2015-08-02","2015-08-03","2015-08-04","2015-08-05","2015-08-06","2015-08-07","2015-08-08","2015-08-09","2015-08-10","2015-08-11","2015-08-12","2015-08-13","2015-08-14","2015-08-15","2015-08-16","2015-08-17","2015-08-18","2015-08-19","2015-08-20","2015-08-21","2015-08-22","2015-08-23","2015-08-24","2015-08-25","2015-08-26","2015-08-27","2015-08-28","2015-08-29","2015-08-30","2015-08-31","2015-09-01","2015-09-02","2015-09-03","2015-09-04","2015-09-05","2015-09-06","2015-09-07","2015-09-08","2015-09-09","2015-09-10","2015-09-11","2015-09-12","2015-09-13","2015-09-14","2015-09-15","2015-09-16","2015-09-17","2015-09-18","2015-09-19","2015-09-20","2015-09-21","2015-09-22","2015-09-23","2015-09-24","2015-09-25","2015-09-26","2015-09-27","2015-09-28","2015-09-29","2015-09-30","2015-10-01","2015-10-02","2015-10-03","2015-10-04","2015-10-05","2015-10-06","2015-10-07","2015-10-08","2015-10-09","2015-10-10","2015-10-11","2015-10-12","2015-10-13","2015-10-14","2015-10-15","2015-10-16","2015-10-17","2015-10-18","2015-10-19","2015-10-20","2015-10-21","2015-10-22","2015-10-23","2015-10-24","2015-10-25","2015-10-26","2015-10-27","2015-10-28","2015-10-29","2015-10-30","2015-10-31","2015-11-01","2015-11-02","2015-11-03","2015-11-04","2015-11-05","2015-11-06","2015-11-07","2015-11-08","2015-11-09","2015-11-10","2015-11-11","2015-11-12","2015-11-13","2015-11-14","2015-11-15","2015-11-16","2015-11-17","2015-11-18","2015-11-19","2015-11-20","2015-11-21","2015-11-22","2015-11-23","2015-11-24","2015-11-25","2015-11-26","2015-11-27","2015-11-28","2015-11-29","2015-11-30","2015-12-01","2015-12-02","2015-12-03","2015-12-04","2015-12-05","2015-12-06","2015-12-07","2015-12-08","2015-12-09","2015-12-10","2015-12-11","2015-12-12","2015-12-13","2015-12-14","2015-12-15","2015-12-16","2015-12-17","2015-12-18","2015-12-19","2015-12-20","2015-12-21","2015-12-22","2015-12-23","2015-12-24","2015-12-25","2015-12-26","2015-12-27","2015-12-28","2015-12-29","2015-12-30","2015-12-31","2016-01-01","2016-01-02","2016-01-03","2016-01-04","2016-01-05","2016-01-06","2016-01-07","2016-01-08","2016-01-09","2016-01-10","2016-01-11","2016-01-12","2016-01-13","2016-01-14","2016-01-15","2016-01-16","2016-01-17","2016-01-18","2016-01-19","2016-01-20","2016-01-21","2016-01-22","2016-01-23","2016-01-24","2016-01-25","2016-01-26","2016-01-27","2016-01-28","2016-01-29","2016-01-30","2016-01-31","2016-02-01","2016-02-02","2016-02-03","2016-02-04","2016-02-05","2016-02-06","2016-02-07","2016-02-08","2016-02-09","2016-02-10","2016-02-11","2016-02-12","2016-02-13","2016-02-14","2016-02-15","2016-02-16","2016-02-17","2016-02-18","2016-02-19","2016-02-20","2016-02-21","2016-02-22","2016-02-23","2016-02-24","2016-02-25","2016-02-26","2016-02-27","2016-02-28","2016-02-29","2016-03-01","2016-03-02","2016-03-03","2016-03-04","2016-03-05","2016-03-06","2016-03-07","2016-03-08","2016-03-09","2016-03-10","2016-03-11","2016-03-12","2016-03-13","2016-03-14","2016-03-15","2016-03-16","2016-03-17","2016-03-18","2016-03-19","2016-03-20","2016-03-21","2016-03-22","2016-03-23","2016-03-24","2016-03-25","2016-03-26","2016-03-27","2016-03-28","2016-03-29","2016-03-30","2016-03-31","2016-04-01","2016-04-02","2016-04-03","2016-04-04","2016-04-05","2016-04-06","2016-04-07","2016-04-08","2016-04-09","2016-04-10","2016-04-11","2016-04-12","2016-04-13","2016-04-14","2016-04-15","2016-04-16","2016-04-17","2016-04-18","2016-04-19","2016-04-20","2016-04-21","2016-04-22","2016-04-23","2016-04-24","2016-04-25","2016-04-26","2016-04-27","2016-04-28","2016-04-29","2016-04-30","2016-05-01","2016-05-02","2016-05-03","2016-05-04","2016-05-05","2016-05-06","2016-05-07","2016-05-08","2016-05-09","2016-05-10","2016-05-11","2016-05-12","2016-05-13","2016-05-14","2016-05-15","2016-05-16","2016-05-17","2016-05-18","2016-05-19","2016-05-20","2016-05-21","2016-05-22","2016-05-23","2016-05-24","2016-05-25","2016-05-26","2016-05-27","2016-05-28","2016-05-29","2016-05-30","2016-05-31","2016-06-01","2016-06-02","2016-06-03","2016-06-04","2016-06-05","2016-06-06","2016-06-07","2016-06-08","2016-06-09","2016-06-10","2016-06-11","2016-06-12","2016-06-13","2016-06-14","2016-06-15","2016-06-16","2016-06-17","2016-06-18","2016-06-19","2016-06-20","2016-06-21","2016-06-22","2016-06-23","2016-06-24","2016-06-25","2016-06-26","2016-06-27","2016-06-28","2016-06-29","2016-06-30","2016-07-01","2016-07-02","2016-07-03","2016-07-04","2016-07-05","2016-07-06","2016-07-07","2016-07-08","2016-07-09","2016-07-10","2016-07-11","2016-07-12","2016-07-13","2016-07-14","2016-07-15","2016-07-16","2016-07-17","2016-07-18","2016-07-19","2016-07-20","2016-07-21","2016-07-22","2016-07-23","2016-07-24","2016-07-25","2016-07-26","2016-07-27","2016-07-28","2016-07-29","2016-07-30","2016-07-31","2016-08-01","2016-08-02","2016-08-03","2016-08-04","2016-08-05","2016-08-06","2016-08-07","2016-08-08","2016-08-09","2016-08-10","2016-08-11","2016-08-12","2016-08-13","2016-08-14","2016-08-15","2016-08-16","2016-08-17","2016-08-18","2016-08-19","2016-08-20","2016-08-21","2016-08-22","2016-08-23","2016-08-24","2016-08-25","2016-08-26","2016-08-27","2016-08-28","2016-08-29","2016-08-30","2016-08-31","2016-09-01","2016-09-02","2016-09-03","2016-09-04","2016-09-05","2016-09-06","2016-09-07","2016-09-08","2016-09-09","2016-09-10","2016-09-11","2016-09-12","2016-09-13","2016-09-14","2016-09-15","2016-09-16","2016-09-17","2016-09-18","2016-09-19","2016-09-20","2016-09-21","2016-09-22","2016-09-23","2016-09-24","2016-09-25","2016-09-26","2016-09-27","2016-09-28","2016-09-29","2016-09-30","2016-10-01","2016-10-02","2016-10-03","2016-10-04","2016-10-05","2016-10-06","2016-10-07","2016-10-08","2016-10-09","2016-10-10","2016-10-11","2016-10-12","2016-10-13","2016-10-14","2016-10-15","2016-10-16","2016-10-17","2016-10-18","2016-10-19","2016-10-20","2016-10-21","2016-10-22","2016-10-23","2016-10-24","2016-10-25","2016-10-26","2016-10-27","2016-10-28","2016-10-29","2016-10-30","2016-10-31","2016-11-01","2016-11-02","2016-11-03","2016-11-04","2016-11-05","2016-11-06","2016-11-07","2016-11-08","2016-11-09","2016-11-10","2016-11-11","2016-11-12","2016-11-13","2016-11-14","2016-11-15","2016-11-16","2016-11-17","2016-11-18","2016-11-19","2016-11-20","2016-11-21","2016-11-22","2016-11-23","2016-11-24","2016-11-25","2016-11-26","2016-11-27","2016-11-28","2016-11-29","2016-11-30","2016-12-01","2016-12-02","2016-12-03","2016-12-04","2016-12-05","2016-12-06","2016-12-07","2016-12-08","2016-12-09","2016-12-10","2016-12-11","2016-12-12","2016-12-13","2016-12-14","2016-12-15","2016-12-16","2016-12-17","2016-12-18","2016-12-19","2016-12-20","2016-12-21","2016-12-22","2016-12-23","2016-12-24","2016-12-25","2016-12-26","2016-12-27","2016-12-28","2016-12-29","2016-12-30","2016-12-31","2017-01-01","2017-01-02","2017-01-03","2017-01-04","2017-01-05","2017-01-06","2017-01-07","2017-01-08","2017-01-09","2017-01-10","2017-01-11","2017-01-12","2017-01-13","2017-01-14","2017-01-15","2017-01-16","2017-01-17","2017-01-18","2017-01-19","2017-01-20","2017-01-21","2017-01-22","2017-01-23","2017-01-24","2017-01-25","2017-01-26","2017-01-27","2017-01-28","2017-01-29","2017-01-30","2017-01-31","2017-02-01","2017-02-02","2017-02-03","2017-02-04","2017-02-05","2017-02-06","2017-02-07","2017-02-08","2017-02-09","2017-02-10","2017-02-11","2017-02-12","2017-02-13","2017-02-14","2017-02-15","2017-02-16","2017-02-17","2017-02-18","2017-02-19","2017-02-20","2017-02-21","2017-02-22","2017-02-23","2017-02-24","2017-02-25","2017-02-26","2017-02-27","2017-02-28","2017-03-01","2017-03-02","2017-03-03","2017-03-04","2017-03-05","2017-03-06","2017-03-07","2017-03-08","2017-03-09","2017-03-10","2017-03-11","2017-03-12","2017-03-13","2017-03-14","2017-03-15","2017-03-16","2017-03-17","2017-03-18","2017-03-19","2017-03-20","2017-03-21","2017-03-22","2017-03-23","2017-03-24","2017-03-25","2017-03-26","2017-03-27","2017-03-28","2017-03-29","2017-03-30","2017-03-31","2017-04-01","2017-04-02","2017-04-03","2017-04-04","2017-04-05","2017-04-06","2017-04-07","2017-04-08","2017-04-09","2017-04-10","2017-04-11","2017-04-12","2017-04-13","2017-04-14","2017-04-15","2017-04-16","2017-04-17","2017-04-18","2017-04-19","2017-04-20","2017-04-21","2017-04-22","2017-04-23","2017-04-24","2017-04-25","2017-04-26","2017-04-27","2017-04-28","2017-04-29","2017-04-30","2017-05-01","2017-05-02","2017-05-03","2017-05-04","2017-05-05","2017-05-06","2017-05-07","2017-05-08","2017-05-09","2017-05-10","2017-05-11","2017-05-12","2017-05-13","2017-05-14","2017-05-15","2017-05-16","2017-05-17","2017-05-18","2017-05-19","2017-05-20","2017-05-21","2017-05-22","2017-05-23","2017-05-24","2017-05-25","2017-05-26","2017-05-27","2017-05-28","2017-05-29","2017-05-30","2017-05-31","2017-06-01","2017-06-02","2017-06-03","2017-06-04","2017-06-05","2017-06-06","2017-06-07","2017-06-08","2017-06-09","2017-06-10","2017-06-11","2017-06-12","2017-06-13","2017-06-14","2017-06-15","2017-06-16","2017-06-17","2017-06-18","2017-06-19","2017-06-20","2017-06-21","2017-06-22","2017-06-23","2017-06-24","2017-06-25","2017-06-26","2017-06-27","2017-06-28","2017-06-29","2017-06-30","2017-07-01","2017-07-02","2017-07-03","2017-07-04","2017-07-05","2017-07-06","2017-07-07","2017-07-08","2017-07-09","2017-07-10","2017-07-11","2017-07-12","2017-07-13","2017-07-14","2017-07-15","2017-07-16","2017-07-17","2017-07-18","2017-07-19","2017-07-20","2017-07-21","2017-07-22","2017-07-23","2017-07-24","2017-07-25","2017-07-26","2017-07-27","2017-07-28","2017-07-29","2017-07-30","2017-07-31","2017-08-01","2017-08-02","2017-08-03","2017-08-04","2017-08-05","2017-08-06","2017-08-07","2017-08-08","2017-08-09","2017-08-10","2017-08-11","2017-08-12","2017-08-13","2017-08-14","2017-08-15","2017-08-16","2017-08-17","2017-08-18","2017-08-19","2017-08-20","2017-08-21","2017-08-22","2017-08-23","2017-08-24","2017-08-25","2017-08-26","2017-08-27","2017-08-28","2017-08-29","2017-08-30","2017-08-31","2017-09-01","2017-09-02","2017-09-03","2017-09-04","2017-09-05","2017-09-06","2017-09-07","2017-09-08","2017-09-09","2017-09-10","2017-09-11","2017-09-12","2017-09-13","2017-09-14","2017-09-15","2017-09-16","2017-09-17","2017-09-18","2017-09-19","2017-09-20","2017-09-21","2017-09-22","2017-09-23","2017-09-24","2017-09-25","2017-09-26","2017-09-27","2017-09-28","2017-09-29","2017-09-30","2017-10-01","2017-10-02","2017-10-03","2017-10-04","2017-10-05","2017-10-06","2017-10-07","2017-10-08","2017-10-09","2017-10-10","2017-10-11","2017-10-12","2017-10-13","2017-10-14","2017-10-15","2017-10-16","2017-10-17","2017-10-18","2017-10-19","2017-10-20","2017-10-21","2017-10-22","2017-10-23","2017-10-24","2017-10-25","2017-10-26","2017-10-27","2017-10-28","2017-10-29","2017-10-30","2017-10-31","2017-11-01","2017-11-02","2017-11-03","2017-11-04","2017-11-05","2017-11-06","2017-11-07","2017-11-08","2017-11-09","2017-11-10","2017-11-11","2017-11-12","2017-11-13","2017-11-14","2017-11-15","2017-11-16","2017-11-17","2017-11-18","2017-11-19","2017-11-20","2017-11-21","2017-11-22","2017-11-23","2017-11-24","2017-11-25","2017-11-26","2017-11-27","2017-11-28","2017-11-29","2017-11-30","2017-12-01","2017-12-02","2017-12-03","2017-12-04","2017-12-05","2017-12-06","2017-12-07","2017-12-08","2017-12-09","2017-12-10","2017-12-11","2017-12-12","2017-12-13","2017-12-14","2017-12-15","2017-12-16","2017-12-17","2017-12-18","2017-12-19","2017-12-20","2017-12-21","2017-12-22","2017-12-23","2017-12-24","2017-12-25","2017-12-26","2017-12-27","2017-12-28","2017-12-29","2017-12-30","2017-12-31","2018-01-01","2018-01-02","2018-01-03","2018-01-04","2018-01-05","2018-01-06","2018-01-07","2018-01-08","2018-01-09","2018-01-10","2018-01-11","2018-01-12","2018-01-13","2018-01-14","2018-01-15","2018-01-16","2018-01-17","2018-01-18","2018-01-19","2018-01-20","2018-01-21","2018-01-22","2018-01-23","2018-01-24","2018-01-25","2018-01-26","2018-01-27","2018-01-28","2018-01-29","2018-01-30","2018-01-31","2018-02-01","2018-02-02","2018-02-03","2018-02-04","2018-02-05","2018-02-06","2018-02-07","2018-02-08","2018-02-09","2018-02-10","2018-02-11","2018-02-12","2018-02-13","2018-02-14","2018-02-15","2018-02-16","2018-02-17","2018-02-18","2018-02-19","2018-02-20","2018-02-21","2018-02-22","2018-02-23","2018-02-24","2018-02-25","2018-02-26","2018-02-27","2018-02-28","2018-03-01","2018-03-02","2018-03-03","2018-03-04","2018-03-05","2018-03-06","2018-03-07","2018-03-08","2018-03-09","2018-03-10","2018-03-11","2018-03-12","2018-03-13","2018-03-14","2018-03-15","2018-03-16","2018-03-17","2018-03-18","2018-03-19","2018-03-20","2018-03-21","2018-03-22","2018-03-23","2018-03-24","2018-03-25","2018-03-26","2018-03-27","2018-03-28","2018-03-29","2018-03-30","2018-03-31","2018-04-01","2018-04-02","2018-04-03","2018-04-04","2018-04-05","2018-04-06","2018-04-07","2018-04-08","2018-04-09","2018-04-10","2018-04-11","2018-04-12","2018-04-13","2018-04-14","2018-04-15","2018-04-16","2018-04-17","2018-04-18","2018-04-19","2018-04-20","2018-04-21","2018-04-22","2018-04-23","2018-04-24","2018-04-25","2018-04-26","2018-04-27","2018-04-28","2018-04-29","2018-04-30","2018-05-01","2018-05-02","2018-05-03","2018-05-04","2018-05-05","2018-05-06","2018-05-07","2018-05-08","2018-05-09","2018-05-10","2018-05-11","2018-05-12","2018-05-13","2018-05-14","2018-05-15","2018-05-16","2018-05-17","2018-05-18","2018-05-19","2018-05-20","2018-05-21","2018-05-22","2018-05-23","2018-05-24","2018-05-25","2018-05-26","2018-05-27","2018-05-28","2018-05-29","2018-05-30","2018-05-31","2018-06-01","2018-06-02","2018-06-03","2018-06-04","2018-06-05","2018-06-06","2018-06-07","2018-06-08","2018-06-09","2018-06-10","2018-06-11","2018-06-12","2018-06-13","2018-06-14","2018-06-15","2018-06-16","2018-06-17","2018-06-18","2018-06-19","2018-06-20","2018-06-21","2018-06-22","2018-06-23","2018-06-24","2018-06-25","2018-06-26","2018-06-27","2018-06-28","2018-06-29","2018-06-30","2018-07-01","2018-07-02","2018-07-03","2018-07-04","2018-07-05","2018-07-06","2018-07-07","2018-07-08","2018-07-09","2018-07-10","2018-07-11","2018-07-12","2018-07-13","2018-07-14","2018-07-15","2018-07-16","2018-07-17","2018-07-18","2018-07-19","2018-07-20","2018-07-21","2018-07-22","2018-07-23","2018-07-24","2018-07-25","2018-07-26","2018-07-27","2018-07-28","2018-07-29","2018-07-30","2018-07-31","2018-08-01","2018-08-02","2018-08-03","2018-08-04","2018-08-05","2018-08-06","2018-08-07","2018-08-08","2018-08-09","2018-08-10","2018-08-11","2018-08-12","2018-08-13","2018-08-14","2018-08-15","2018-08-16","2018-08-17","2018-08-18","2018-08-19","2018-08-20","2018-08-21","2018-08-22","2018-08-23","2018-08-24","2018-08-25","2018-08-26","2018-08-27","2018-08-28","2018-08-29","2018-08-30","2018-08-31","2018-09-01","2018-09-02","2018-09-03","2018-09-04","2018-09-05","2018-09-06","2018-09-07","2018-09-08","2018-09-09","2018-09-10","2018-09-11","2018-09-12","2018-09-13","2018-09-14","2018-09-15","2018-09-16","2018-09-17","2018-09-18","2018-09-19","2018-09-20","2018-09-21","2018-09-22","2018-09-23","2018-09-24","2018-09-25","2018-09-26","2018-09-27","2018-09-28","2018-09-29","2018-09-30","2018-10-01","2018-10-02","2018-10-03","2018-10-04","2018-10-05","2018-10-06","2018-10-07","2018-10-08","2018-10-09","2018-10-10","2018-10-11","2018-10-12","2018-10-13","2018-10-14","2018-10-15","2018-10-16","2018-10-17","2018-10-18","2018-10-19","2018-10-20","2018-10-21","2018-10-22","2018-10-23","2018-10-24","2018-10-25","2018-10-26","2018-10-27","2018-10-28","2018-10-29","2018-10-30","2018-10-31","2018-11-01","2018-11-02","2018-11-03","2018-11-04","2018-11-05","2018-11-06","2018-11-07","2018-11-08","2018-11-09","2018-11-10","2018-11-11","2018-11-12","2018-11-13","2018-11-14","2018-11-15","2018-11-16","2018-11-17","2018-11-18","2018-11-19","2018-11-20","2018-11-21","2018-11-22","2018-11-23","2018-11-24","2018-11-25","2018-11-26","2018-11-27","2018-11-28","2018-11-29","2018-11-30","2018-12-01","2018-12-02","2018-12-03","2018-12-04","2018-12-05","2018-12-06","2018-12-07","2018-12-08","2018-12-09","2018-12-10","2018-12-11","2018-12-12","2018-12-13","2018-12-14","2018-12-15","2018-12-16","2018-12-17","2018-12-18","2018-12-19","2018-12-20","2018-12-21","2018-12-22","2018-12-23","2018-12-24","2018-12-25","2018-12-26","2018-12-27","2018-12-28","2018-12-29","2018-12-30","2018-12-31","2019-01-01","2019-01-02","2019-01-03","2019-01-04","2019-01-05","2019-01-06","2019-01-07","2019-01-08","2019-01-09","2019-01-10","2019-01-11","2019-01-12","2019-01-13","2019-01-14","2019-01-15","2019-01-16","2019-01-17","2019-01-18","2019-01-19","2019-01-20","2019-01-21","2019-01-22","2019-01-23","2019-01-24","2019-01-25","2019-01-26","2019-01-27","2019-01-28","2019-01-29","2019-01-30","2019-01-31","2019-02-01","2019-02-02","2019-02-03","2019-02-04","2019-02-05","2019-02-06","2019-02-07","2019-02-08","2019-02-09","2019-02-10","2019-02-11","2019-02-12","2019-02-13","2019-02-14","2019-02-15","2019-02-16","2019-02-17","2019-02-18","2019-02-19","2019-02-20","2019-02-21","2019-02-22","2019-02-23","2019-02-24","2019-02-25","2019-02-26","2019-02-27","2019-02-28","2019-03-01","2019-03-02","2019-03-03","2019-03-04","2019-03-05","2019-03-06","2019-03-07","2019-03-08","2019-03-09","2019-03-10","2019-03-11","2019-03-12","2019-03-13","2019-03-14","2019-03-15","2019-03-16","2019-03-17","2019-03-18","2019-03-19","2019-03-20","2019-03-21","2019-03-22","2019-03-23","2019-03-24","2019-03-25","2019-03-26","2019-03-27","2019-03-28","2019-03-29","2019-03-30","2019-03-31","2019-04-01","2019-04-02","2019-04-03","2019-04-04","2019-04-05","2019-04-06","2019-04-07","2019-04-08","2019-04-09","2019-04-10","2019-04-11","2019-04-12","2019-04-13","2019-04-14","2019-04-15","2019-04-16","2019-04-17","2019-04-18","2019-04-19","2019-04-20","2019-04-21","2019-04-22","2019-04-23","2019-04-24","2019-04-25","2019-04-26","2019-04-27","2019-04-28","2019-04-29","2019-04-30","2019-05-01","2019-05-02","2019-05-03","2019-05-04","2019-05-05","2019-05-06","2019-05-07","2019-05-08","2019-05-09","2019-05-10","2019-05-11","2019-05-12","2019-05-13","2019-05-14","2019-05-15","2019-05-16","2019-05-17","2019-05-18","2019-05-19","2019-05-20","2019-05-21","2019-05-22","2019-05-23","2019-05-24","2019-05-25","2019-05-26","2019-05-27","2019-05-28","2019-05-29","2019-05-30","2019-05-31","2019-06-01","2019-06-02","2019-06-03","2019-06-04","2019-06-05","2019-06-06","2019-06-07","2019-06-08","2019-06-09","2019-06-10","2019-06-11","2019-06-12","2019-06-13","2019-06-14","2019-06-15","2019-06-16","2019-06-17","2019-06-18","2019-06-19","2019-06-20","2019-06-21","2019-06-22","2019-06-23","2019-06-24","2019-06-25","2019-06-26","2019-06-27","2019-06-28","2019-06-29","2019-06-30","2019-07-01","2019-07-02","2019-07-03","2019-07-04","2019-07-05","2019-07-06","2019-07-07","2019-07-08","2019-07-09","2019-07-10","2019-07-11","2019-07-12","2019-07-13","2019-07-14","2019-07-15","2019-07-16","2019-07-17","2019-07-18","2019-07-19","2019-07-20","2019-07-21","2019-07-22","2019-07-23","2019-07-24","2019-07-25","2019-07-26","2019-07-27","2019-07-28","2019-07-29","2019-07-30","2019-07-31","2019-08-01","2019-08-02","2019-08-03","2019-08-04","2019-08-05","2019-08-06","2019-08-07","2019-08-08","2019-08-09","2019-08-10","2019-08-11","2019-08-12","2019-08-13","2019-08-14","2019-08-15","2019-08-16","2019-08-17","2019-08-18","2019-08-19","2019-08-20","2019-08-21","2019-08-22","2019-08-23","2019-08-24","2019-08-25","2019-08-26","2019-08-27","2019-08-28","2019-08-29","2019-08-30","2019-08-31","2019-09-01","2019-09-02","2019-09-03","2019-09-04","2019-09-05","2019-09-06","2019-09-07","2019-09-08","2019-09-09","2019-09-10","2019-09-11","2019-09-12","2019-09-13","2019-09-14","2019-09-15","2019-09-16","2019-09-17","2019-09-18","2019-09-19","2019-09-20","2019-09-21","2019-09-22","2019-09-23","2019-09-24","2019-09-25","2019-09-26","2019-09-27","2019-09-28","2019-09-29","2019-09-30","2019-10-01","2019-10-02","2019-10-03","2019-10-04","2019-10-05","2019-10-06","2019-10-07","2019-10-08","2019-10-09","2019-10-10","2019-10-11","2019-10-12","2019-10-13","2019-10-14","2019-10-15","2019-10-16","2019-10-17","2019-10-18","2019-10-19","2019-10-20","2019-10-21","2019-10-22","2019-10-23","2019-10-24","2019-10-25","2019-10-26","2019-10-27","2019-10-28","2019-10-29","2019-10-30","2019-10-31","2019-11-01","2019-11-02","2019-11-03","2019-11-04","2019-11-05","2019-11-06","2019-11-07","2019-11-08","2019-11-09","2019-11-10","2019-11-11","2019-11-12","2019-11-13","2019-11-14","2019-11-15","2019-11-16","2019-11-17","2019-11-18","2019-11-19","2019-11-20","2019-11-21","2019-11-22","2019-11-23","2019-11-24","2019-11-25","2019-11-26","2019-11-27","2019-11-28","2019-11-29","2019-11-30","2019-12-01","2019-12-02","2019-12-03","2019-12-04","2019-12-05","2019-12-06","2019-12-07","2019-12-08","2019-12-09","2019-12-10","2019-12-11","2019-12-12","2019-12-13","2019-12-14","2019-12-15","2019-12-16","2019-12-17","2019-12-18","2019-12-19","2019-12-20","2019-12-21","2019-12-22","2019-12-23","2019-12-24","2019-12-25","2019-12-26","2019-12-27","2019-12-28","2019-12-29","2019-12-30","2019-12-31","2020-01-01","2020-01-02","2020-01-03","2020-01-04","2020-01-05","2020-01-06","2020-01-07","2020-01-08","2020-01-09","2020-01-10","2020-01-11","2020-01-12","2020-01-13","2020-01-14","2020-01-15","2020-01-16","2020-01-17","2020-01-18","2020-01-19","2020-01-20","2020-01-21","2020-01-22","2020-01-23","2020-01-24","2020-01-25","2020-01-26","2020-01-27","2020-01-28","2020-01-29","2020-01-30","2020-01-31","2020-02-01","2020-02-02","2020-02-03","2020-02-04","2020-02-05","2020-02-06","2020-02-07","2020-02-08","2020-02-09","2020-02-10","2020-02-11","2020-02-12","2020-02-13","2020-02-14","2020-02-15","2020-02-16","2020-02-17","2020-02-18","2020-02-19","2020-02-20","2020-02-21","2020-02-22","2020-02-23","2020-02-24","2020-02-25","2020-02-26","2020-02-27","2020-02-28","2020-02-29","2020-03-01","2020-03-02","2020-03-03","2020-03-04","2020-03-05","2020-03-06","2020-03-07","2020-03-08","2020-03-09","2020-03-10","2020-03-11","2020-03-12","2020-03-13","2020-03-14","2020-03-15","2020-03-16","2020-03-17","2020-03-18","2020-03-19","2020-03-20","2020-03-21","2020-03-22","2020-03-23","2020-03-24","2020-03-25","2020-03-26","2020-03-27","2020-03-28","2020-03-29","2020-03-30","2020-03-31","2020-04-01","2020-04-02","2020-04-03","2020-04-04","2020-04-05","2020-04-06","2020-04-07","2020-04-08","2020-04-09","2020-04-10","2020-04-11","2020-04-12","2020-04-13","2020-04-14","2020-04-15","2020-04-16","2020-04-17","2020-04-18","2020-04-19","2020-04-20","2020-04-21","2020-04-22","2020-04-23","2020-04-24","2020-04-25","2020-04-26","2020-04-27","2020-04-28","2020-04-29","2020-04-30","2020-05-01","2020-05-02","2020-05-03","2020-05-04","2020-05-05","2020-05-06","2020-05-07","2020-05-08","2020-05-09","2020-05-10","2020-05-11","2020-05-12","2020-05-13","2020-05-14","2020-05-15","2020-05-16","2020-05-17","2020-05-18","2020-05-19","2020-05-20","2020-05-21","2020-05-22","2020-05-23","2020-05-24","2020-05-25","2020-05-26","2020-05-27","2020-05-28","2020-05-29","2020-05-30","2020-05-31","2020-06-01","2020-06-02","2020-06-03","2020-06-04","2020-06-05","2020-06-06","2020-06-07","2020-06-08","2020-06-09","2020-06-10","2020-06-11","2020-06-12","2020-06-13","2020-06-14","2020-06-15","2020-06-16","2020-06-17","2020-06-18","2020-06-19","2020-06-20","2020-06-21","2020-06-22","2020-06-23","2020-06-24","2020-06-25","2020-06-26","2020-06-27","2020-06-28","2020-06-29","2020-06-30","2020-07-01","2020-07-02","2020-07-03","2020-07-04","2020-07-05","2020-07-06","2020-07-07","2020-07-08","2020-07-09","2020-07-10","2020-07-11","2020-07-12","2020-07-13","2020-07-14","2020-07-15","2020-07-16","2020-07-17","2020-07-18","2020-07-19","2020-07-20","2020-07-21","2020-07-22","2020-07-23","2020-07-24","2020-07-25","2020-07-26","2020-07-27","2020-07-28","2020-07-29","2020-07-30","2020-07-31","2020-08-01","2020-08-02","2020-08-03","2020-08-04","2020-08-05","2020-08-06","2020-08-07","2020-08-08","2020-08-09","2020-08-10","2020-08-11","2020-08-12","2020-08-13","2020-08-14","2020-08-15","2020-08-16","2020-08-17","2020-08-18","2020-08-19","2020-08-20","2020-08-21","2020-08-22","2020-08-23","2020-08-24","2020-08-25","2020-08-26","2020-08-27","2020-08-28","2020-08-29","2020-08-30","2020-08-31","2020-09-01","2020-09-02","2020-09-03","2020-09-04","2020-09-05","2020-09-06","2020-09-07","2020-09-08","2020-09-09","2020-09-10","2020-09-11","2020-09-12","2020-09-13","2020-09-14","2020-09-15","2020-09-16","2020-09-17","2020-09-18","2020-09-19","2020-09-20","2020-09-21","2020-09-22","2020-09-23","2020-09-24","2020-09-25","2020-09-26","2020-09-27","2020-09-28","2020-09-29","2020-09-30","2020-10-01","2020-10-02","2020-10-03","2020-10-04","2020-10-05","2020-10-06","2020-10-07","2020-10-08","2020-10-09","2020-10-10","2020-10-11","2020-10-12","2020-10-13","2020-10-14","2020-10-15","2020-10-16","2020-10-17","2020-10-18","2020-10-19","2020-10-20","2020-10-21","2020-10-22","2020-10-23","2020-10-24","2020-10-25","2020-10-26","2020-10-27","2020-10-28","2020-10-29","2020-10-30","2020-10-31","2020-11-01","2020-11-02","2020-11-03","2020-11-04","2020-11-05","2020-11-06","2020-11-07","2020-11-08","2020-11-09","2020-11-10","2020-11-11","2020-11-12","2020-11-13","2020-11-14","2020-11-15","2020-11-16","2020-11-17","2020-11-18","2020-11-19","2020-11-20","2020-11-21","2020-11-22","2020-11-23","2020-11-24","2020-11-25","2020-11-26","2020-11-27","2020-11-28","2020-11-29","2020-11-30","2020-12-01","2020-12-02","2020-12-03","2020-12-04","2020-12-05","2020-12-06","2020-12-07","2020-12-08","2020-12-09","2020-12-10","2020-12-11","2020-12-12","2020-12-13","2020-12-14","2020-12-15","2020-12-16","2020-12-17","2020-12-18","2020-12-19","2020-12-20","2020-12-21","2020-12-22","2020-12-23","2020-12-24","2020-12-25","2020-12-26","2020-12-27","2020-12-28","2020-12-29","2020-12-30","2020-12-31","2021-01-01","2021-01-02","2021-01-03","2021-01-04","2021-01-05","2021-01-06","2021-01-07","2021-01-08","2021-01-09","2021-01-10","2021-01-11"],"y":[0.37247,0.37247,0.37247,0.3724,0.37233,0.37226,0.37221,0.37216,0.37211,0.37207,0.37203,0.372,0.37197,0.37195,0.37193,0.37192,0.37191,0.3719,0.37189,0.37189,0.37188,0.37187,0.37187,0.37187,0.37187,0.37187,0.37187,0.37187,0.37186,0.37186,0.37184,0.37182,0.3718,0.37177,0.37174,0.37172,0.37171,0.37171,0.37173,0.37176,0.37182,0.37188,0.37196,0.37203,0.37211,0.37218,0.37224,0.37228,0.37231,0.37232,0.37232,0.37232,0.37232,0.37232,0.37232,0.37235,0.37239,0.37245,0.37254,0.37264,0.37275,0.37287,0.37298,0.3731,0.3732,0.37329,0.37338,0.37348,0.37358,0.37368,0.37378,0.37386,0.37394,0.37399,0.37403,0.3741,0.37425,0.37442,0.37455,0.37459,0.37449,0.37423,0.37387,0.37344,0.37298,0.37253,0.37212,0.37167,0.3711,0.37045,0.36977,0.36908,0.36844,0.36789,0.36746,0.36719,0.36707,0.36705,0.3671,0.36722,0.3674,0.36762,0.36788,0.36816,0.36844,0.36864,0.36871,0.3687,0.3687,0.36876,0.36896,0.36935,0.37002,0.37101,0.37231,0.37382,0.37554,0.37745,0.37955,0.38184,0.38429,0.38691,0.38969,0.39279,0.39632,0.40017,0.40423,0.4084,0.41256,0.41661,0.42043,0.42393,0.42729,0.43077,0.43428,0.43777,0.44117,0.44441,0.44742,0.45015,0.45252,0.45462,0.45657,0.45834,0.45992,0.46129,0.46243,0.46331,0.46393,0.46426,0.46399,0.46302,0.46164,0.46013,0.45877,0.45784,0.45698,0.45575,0.45435,0.45294,0.45172,0.45087,0.45039,0.45014,0.45006,0.4501,0.4502,0.45032,0.45039,0.45036,0.45019,0.44987,0.44949,0.44904,0.44854,0.44801,0.44745,0.44688,0.44632,0.44577,0.44521,0.44462,0.44401,0.4434,0.44281,0.44226,0.44177,0.44136,0.44104,0.44082,0.44068,0.44058,0.44052,0.44049,0.44045,0.44039,0.44031,0.44017,0.44,0.43982,0.43964,0.43945,0.43927,0.43909,0.43891,0.43874,0.43857,0.43843,0.43832,0.43822,0.43814,0.43805,0.43795,0.43782,0.43766,0.43746,0.43719,0.43683,0.43642,0.43597,0.43551,0.43505,0.43463,0.43427,0.43398,0.43372,0.43342,0.43312,0.43286,0.43267,0.43257,0.43261,0.43277,0.43299,0.43326,0.43354,0.43378,0.43406,0.43447,0.43497,0.4355,0.43602,0.4365,0.43688,0.43714,0.43721,0.4371,0.43682,0.43644,0.43598,0.4355,0.43503,0.43461,0.43429,0.43411,0.43409,0.43419,0.43437,0.43459,0.43481,0.43499,0.43509,0.43507,0.43489,0.43469,0.43459,0.43454,0.43447,0.43431,0.43399,0.43346,0.43265,0.43149,0.42998,0.42818,0.42613,0.42387,0.42144,0.41887,0.41621,0.4135,0.41077,0.40785,0.40461,0.40112,0.39745,0.39369,0.3899,0.38616,0.38256,0.37916,0.37568,0.37187,0.36789,0.36391,0.36007,0.35653,0.35345,0.35099,0.34931,0.34844,0.34822,0.34845,0.34897,0.34957,0.35008,0.35109,0.35305,0.35553,0.35812,0.36041,0.36199,0.36307,0.36414,0.36518,0.36616,0.36706,0.36787,0.36855,0.3691,0.36948,0.36967,0.3697,0.36959,0.36939,0.36913,0.36884,0.36856,0.36833,0.36818,0.36806,0.36789,0.36769,0.36747,0.36725,0.36703,0.36682,0.36665,0.36653,0.36648,0.36652,0.36663,0.36679,0.36699,0.36719,0.36739,0.36757,0.3677,0.36799,0.36858,0.36936,0.37022,0.37104,0.37171,0.37212,0.37217,0.37172,0.37101,0.37029,0.36959,0.3689,0.36824,0.3676,0.36699,0.36641,0.36588,0.36544,0.36514,0.36494,0.36483,0.36479,0.3648,0.36483,0.36487,0.3649,0.36497,0.36511,0.36531,0.36551,0.3657,0.36584,0.36593,0.366,0.36608,0.36615,0.36625,0.36636,0.3665,0.36667,0.36685,0.36704,0.36724,0.36743,0.36761,0.36777,0.36791,0.36805,0.3682,0.36835,0.36851,0.36866,0.36879,0.3689,0.36897,0.369,0.36897,0.36887,0.36871,0.36852,0.36831,0.3681,0.36792,0.36777,0.36768,0.36764,0.36761,0.3676,0.3676,0.36762,0.36765,0.3677,0.36777,0.36785,0.36797,0.36814,0.36834,0.36856,0.36879,0.36901,0.36922,0.36939,0.36952,0.36962,0.3697,0.36977,0.36982,0.36986,0.36988,0.36989,0.36988,0.36986,0.3698,0.36969,0.36955,0.36938,0.36921,0.36906,0.36893,0.36886,0.36885,0.36889,0.36897,0.36908,0.3692,0.36933,0.36947,0.36962,0.36981,0.37003,0.37025,0.37048,0.3707,0.37085,0.37089,0.37088,0.37085,0.37085,0.37091,0.37109,0.37142,0.37195,0.37254,0.3731,0.37367,0.37432,0.37509,0.37607,0.37729,0.37882,0.38072,0.38305,0.3858,0.3889,0.39225,0.3958,0.39945,0.40315,0.4068,0.41033,0.41402,0.41811,0.42245,0.42693,0.43139,0.43572,0.43977,0.44342,0.44652,0.44919,0.4516,0.45378,0.45572,0.45744,0.45895,0.46025,0.46136,0.46228,0.46289,0.46311,0.46302,0.4627,0.46223,0.46167,0.46111,0.46063,0.46029,0.46003,0.45972,0.45938,0.45902,0.45864,0.45826,0.45789,0.45754,0.45721,0.45695,0.45674,0.45654,0.45634,0.45608,0.45574,0.45528,0.45466,0.45385,0.45279,0.45149,0.45,0.44838,0.44671,0.44505,0.44346,0.44199,0.44072,0.43952,0.43824,0.43694,0.43566,0.43446,0.43339,0.4325,0.43183,0.43146,0.43143,0.43175,0.43233,0.4331,0.43397,0.43487,0.43571,0.43643,0.43693,0.43732,0.43775,0.43819,0.43862,0.439,0.43932,0.43955,0.43965,0.43962,0.43938,0.43894,0.43835,0.43766,0.43692,0.43618,0.43549,0.43491,0.43449,0.43419,0.43394,0.43374,0.43357,0.43344,0.43333,0.43324,0.43316,0.43308,0.43305,0.4331,0.4332,0.43332,0.43344,0.43352,0.43353,0.43345,0.43325,0.43285,0.43228,0.43163,0.43097,0.4304,0.43,0.42975,0.42953,0.42933,0.42913,0.42893,0.42869,0.42845,0.42823,0.42803,0.42785,0.42768,0.42752,0.42737,0.42723,0.42709,0.42696,0.42681,0.42664,0.42647,0.42628,0.42607,0.42585,0.42561,0.42536,0.42519,0.42517,0.42524,0.42537,0.42548,0.42552,0.42545,0.42521,0.42474,0.42419,0.42371,0.42322,0.42266,0.42197,0.42109,0.41995,0.41849,0.41665,0.41424,0.41124,0.40778,0.40399,0.4,0.39595,0.39197,0.3882,0.38478,0.38133,0.37754,0.37356,0.36957,0.36572,0.36217,0.35911,0.35668,0.35505,0.35435,0.35447,0.35524,0.3565,0.35807,0.35978,0.36146,0.36294,0.36405,0.36519,0.36671,0.3684,0.37004,0.37142,0.37232,0.37271,0.37278,0.37266,0.37244,0.37226,0.37221,0.37222,0.37211,0.37192,0.37167,0.3714,0.37112,0.37087,0.37068,0.37056,0.37052,0.37051,0.37053,0.37055,0.37058,0.3706,0.3706,0.37058,0.37051,0.3704,0.37028,0.37014,0.36998,0.36981,0.36964,0.36946,0.36927,0.36909,0.36888,0.36862,0.36833,0.36802,0.3677,0.36738,0.36708,0.36682,0.36659,0.36639,0.36617,0.36596,0.36576,0.36559,0.36546,0.36539,0.36538,0.36547,0.36565,0.3659,0.3662,0.36653,0.36686,0.36717,0.36743,0.36764,0.36779,0.36793,0.36806,0.36817,0.36826,0.36834,0.36839,0.36841,0.36841,0.36836,0.36823,0.36808,0.36791,0.36778,0.3677,0.36769,0.36772,0.36776,0.36781,0.36785,0.36785,0.36783,0.36781,0.36779,0.36777,0.36775,0.36772,0.36768,0.36764,0.36758,0.36747,0.36731,0.36711,0.36689,0.36667,0.36646,0.36628,0.36616,0.3661,0.36611,0.36616,0.36625,0.36636,0.36651,0.36668,0.36687,0.36708,0.36731,0.36758,0.36792,0.3683,0.36872,0.36916,0.3696,0.37002,0.37041,0.37075,0.37104,0.37131,0.37155,0.37176,0.37195,0.37212,0.37227,0.3724,0.37252,0.3726,0.37265,0.37268,0.3727,0.37272,0.37276,0.37282,0.37292,0.37307,0.37328,0.37353,0.37381,0.37411,0.37442,0.37472,0.375,0.37526,0.37548,0.37558,0.37553,0.37539,0.37521,0.37503,0.37491,0.37491,0.37507,0.37545,0.37583,0.37603,0.37618,0.3764,0.37682,0.37754,0.37869,0.38039,0.38276,0.38592,0.38978,0.39418,0.39894,0.40392,0.40893,0.4138,0.41839,0.42251,0.42657,0.43101,0.43565,0.44035,0.44496,0.44931,0.45326,0.45664,0.4593,0.46129,0.46279,0.46386,0.46458,0.46502,0.46523,0.46529,0.46527,0.46523,0.46497,0.46429,0.46328,0.46205,0.4607,0.45931,0.45798,0.45682,0.45591,0.45518,0.45446,0.45376,0.45309,0.45243,0.4518,0.45119,0.4506,0.45003,0.44953,0.44913,0.44879,0.44849,0.44821,0.44791,0.44757,0.44717,0.44668,0.44599,0.44509,0.44409,0.44307,0.44213,0.44139,0.44067,0.43985,0.439,0.43822,0.43761,0.43727,0.4372,0.43733,0.43762,0.43802,0.43847,0.43892,0.43933,0.43964,0.43981,0.43995,0.44018,0.44046,0.44076,0.44103,0.44125,0.44136,0.44134,0.44115,0.44072,0.44005,0.43922,0.43827,0.43728,0.43631,0.43542,0.43466,0.43412,0.43372,0.43338,0.43309,0.43284,0.43263,0.43244,0.43228,0.43213,0.43199,0.43192,0.43195,0.43206,0.43223,0.43244,0.43266,0.43288,0.43307,0.43321,0.43333,0.43346,0.43361,0.43373,0.43384,0.43389,0.43389,0.43382,0.43366,0.43336,0.43293,0.4324,0.43181,0.43119,0.43058,0.43001,0.42952,0.42915,0.42885,0.42857,0.4283,0.42805,0.42783,0.42765,0.4276,0.42773,0.42795,0.42819,0.42836,0.42838,0.42826,0.4281,0.4279,0.42769,0.42747,0.42726,0.42708,0.42692,0.42682,0.4269,0.42722,0.42769,0.4282,0.42867,0.429,0.42909,0.42885,0.42818,0.42712,0.42579,0.42422,0.42243,0.42045,0.41831,0.41602,0.41362,0.41113,0.40833,0.40507,0.40148,0.39769,0.39381,0.38999,0.38634,0.38298,0.38006,0.37737,0.37468,0.37203,0.36948,0.36709,0.36491,0.363,0.36141,0.3602,0.3594,0.35899,0.35889,0.35905,0.35942,0.35994,0.36054,0.36118,0.36179,0.36259,0.36375,0.36517,0.36675,0.36839,0.36998,0.37142,0.37261,0.37345,0.374,0.37442,0.37472,0.37494,0.37509,0.3752,0.37514,0.37485,0.37441,0.37393,0.37349,0.37319,0.37296,0.37266,0.37231,0.37194,0.37156,0.37119,0.37084,0.37054,0.3703,0.37012,0.36997,0.36985,0.36976,0.36969,0.36965,0.36962,0.36961,0.36962,0.36965,0.36973,0.36985,0.36999,0.37015,0.37031,0.37045,0.37058,0.37067,0.37075,0.37083,0.37091,0.37098,0.37103,0.37106,0.37106,0.37103,0.37096,0.37085,0.37072,0.37056,0.37039,0.3702,0.37,0.3698,0.3696,0.36936,0.36907,0.36875,0.3684,0.36806,0.36773,0.36744,0.36721,0.36705,0.36695,0.36689,0.36687,0.36687,0.36689,0.36694,0.367,0.36707,0.36715,0.36726,0.3674,0.36757,0.36776,0.36797,0.36819,0.36841,0.36863,0.36884,0.36905,0.3693,0.36956,0.36983,0.3701,0.37035,0.37058,0.37078,0.37093,0.37105,0.37117,0.37128,0.37137,0.37145,0.37149,0.37151,0.37149,0.37144,0.37131,0.37109,0.3708,0.37047,0.37013,0.36981,0.36952,0.3693,0.36917,0.36912,0.36912,0.36916,0.36923,0.36932,0.36942,0.36953,0.36964,0.36973,0.36983,0.36996,0.37012,0.37029,0.37046,0.37062,0.37077,0.37089,0.37097,0.37101,0.37099,0.37094,0.37087,0.3708,0.37073,0.3707,0.3707,0.37076,0.37088,0.37105,0.37124,0.37147,0.3717,0.37194,0.37217,0.37239,0.37258,0.37273,0.37285,0.37296,0.37307,0.37321,0.37338,0.37355,0.37365,0.37374,0.37384,0.37401,0.37428,0.37447,0.37446,0.37434,0.3742,0.37412,0.3742,0.37453,0.37521,0.37632,0.3778,0.37954,0.38152,0.38375,0.3862,0.38888,0.39178,0.39489,0.39819,0.402,0.40647,0.41144,0.41671,0.42211,0.42747,0.43259,0.4373,0.44141,0.44515,0.44881,0.45234,0.45568,0.45878,0.46158,0.46402,0.46606,0.46762,0.46867,0.46923,0.4694,0.46927,0.46893,0.46845,0.46794,0.46747,0.46714,0.4668,0.46627,0.4656,0.46482,0.46398,0.46313,0.4623,0.46155,0.4609,0.46031,0.45968,0.45902,0.45833,0.45761,0.45687,0.45611,0.45533,0.45455,0.45371,0.45281,0.45189,0.45098,0.45013,0.44937,0.44867,0.44796,0.44726,0.44658,0.44595,0.44539,0.4449,0.44445,0.44405,0.44371,0.44341,0.44317,0.44297,0.44283,0.44273,0.44273,0.44283,0.44301,0.44324,0.44349,0.44373,0.44393,0.44407,0.44411,0.44406,0.44395,0.4438,0.44361,0.4434,0.44319,0.44297,0.44277,0.44259,0.44243,0.44226,0.44209,0.44192,0.44175,0.44159,0.44144,0.44131,0.44119,0.44112,0.44111,0.44113,0.44117,0.44119,0.44118,0.44112,0.44099,0.44075,0.44038,0.43989,0.4393,0.43866,0.43801,0.43738,0.43683,0.43639,0.43609,0.43595,0.43595,0.43603,0.43618,0.43635,0.43651,0.43663,0.43667,0.4366,0.43644,0.43624,0.43601,0.43578,0.43557,0.43538,0.43512,0.43472,0.43425,0.43378,0.43338,0.43312,0.43307,0.43322,0.43351,0.43388,0.43427,0.43461,0.43486,0.43495,0.43481,0.43449,0.43406,0.43353,0.43291,0.4322,0.43142,0.43056,0.42965,0.42867,0.42763,0.42649,0.42527,0.42397,0.42259,0.42114,0.41962,0.41805,0.41642,0.41473,0.41299,0.41119,0.40935,0.40747,0.40556,0.40361,0.40164,0.39965,0.39749,0.39504,0.39242,0.38969,0.38694,0.38428,0.38177,0.37952,0.3776,0.37593,0.37437,0.37293,0.37163,0.37047,0.36948,0.36865,0.368,0.36755,0.36739,0.36759,0.36805,0.36871,0.36949,0.37032,0.37112,0.37183,0.37235,0.37288,0.37359,0.37436,0.3751,0.3757,0.37606,0.37615,0.37605,0.37583,0.37556,0.37532,0.37518,0.37507,0.37491,0.3747,0.37447,0.37422,0.37396,0.37373,0.37352,0.37335,0.37322,0.37309,0.37298,0.37287,0.37278,0.37268,0.3726,0.37251,0.37243,0.37234,0.37223,0.37212,0.372,0.37189,0.3718,0.37173,0.37168,0.37166,0.3717,0.3718,0.37194,0.37209,0.37225,0.37239,0.37249,0.37255,0.37254,0.37251,0.37245,0.37237,0.37228,0.37218,0.37209,0.37201,0.37194,0.37189,0.37183,0.37176,0.3717,0.37165,0.37161,0.37158,0.37156,0.37157,0.37161,0.3717,0.37182,0.37196,0.37211,0.37224,0.37235,0.37242,0.37244,0.3724,0.37232,0.37221,0.37208,0.37196,0.37186,0.37174,0.37157,0.37139,0.37121,0.37105,0.37093,0.37083,0.37073,0.37061,0.37049,0.37037,0.37025,0.37015,0.37006,0.36999,0.36993,0.36987,0.36982,0.36979,0.36978,0.36981,0.36987,0.36998,0.37015,0.37039,0.3707,0.37108,0.37151,0.37196,0.37242,0.37288,0.37331,0.37371,0.3741,0.37451,0.37494,0.37537,0.37577,0.37614,0.37645,0.37668,0.37683,0.37688,0.37685,0.37675,0.37661,0.37644,0.37627,0.37612,0.37601,0.37596,0.3759,0.37579,0.37565,0.3755,0.37537,0.37528,0.37527,0.37535,0.37556,0.37588,0.37627,0.37673,0.37724,0.3778,0.3784,0.37902,0.37965,0.38029,0.38075,0.38099,0.38117,0.38144,0.38198,0.38294,0.38403,0.38494,0.38587,0.38701,0.38856,0.39071,0.39354,0.39693,0.40078,0.40498,0.40942,0.41399,0.41857,0.42307,0.42737,0.4319,0.43703,0.44254,0.4482,0.45379,0.4591,0.46389,0.46795,0.47107,0.47329,0.4749,0.47598,0.4766,0.47686,0.47685,0.47663,0.47631,0.47595,0.4753,0.47411,0.47252,0.47066,0.46865,0.46664,0.46476,0.46314,0.46191,0.46097,0.46014,0.45939,0.45872,0.45811,0.45755,0.45701,0.4565,0.45599,0.4555,0.45504,0.4546,0.45418,0.45377,0.45337,0.45296,0.45254,0.4521,0.45164,0.45116,0.45069,0.45022,0.44976,0.44933,0.44893,0.44857,0.44826,0.44796,0.44763,0.4473,0.447,0.44676,0.44661,0.44656,0.44659,0.44668,0.4468,0.44694,0.44706,0.44721,0.44743,0.44769,0.44799,0.4483,0.4486,0.44888,0.44911,0.44927,0.4494,0.44952,0.44963,0.44972,0.44979,0.44984,0.44986,0.44984,0.44978,0.44968,0.44957,0.44944,0.44929,0.4491,0.44888,0.44862,0.44831,0.44797,0.44754,0.44701,0.44641,0.44577,0.4451,0.44443,0.44378,0.44318,0.44265,0.44216,0.44167,0.44118,0.44072,0.44029,0.43992,0.43962,0.4394,0.43928,0.4393,0.43949,0.43979,0.44014,0.4405,0.44082,0.44105,0.44113,0.44103,0.44072,0.44026,0.43969,0.43904,0.43835,0.43765,0.43698,0.43638,0.43586,0.43548,0.43522,0.43505,0.43493,0.43483,0.43474,0.4346,0.4344,0.43411,0.43378,0.43349,0.4332,0.43287,0.43245,0.43191,0.43122,0.43032,0.42919,0.42786,0.42639,0.42477,0.42301,0.42109,0.41903,0.4168,0.41441,0.41186,0.40892,0.40547,0.40167,0.3977,0.39371,0.38988,0.38636,0.38332,0.38093,0.37903,0.37733,0.37583,0.37453,0.37343,0.37252,0.37181,0.37128,0.37094,0.37102,0.37166,0.3727,0.37402,0.37546,0.37689,0.37815,0.37912,0.37965,0.37979,0.37973,0.37952,0.37919,0.3788,0.37837,0.37796,0.37761,0.37735,0.37715,0.37693,0.3767,0.37647,0.37623,0.37599,0.37575,0.37552,0.3753,0.37508,0.37485,0.37463,0.37441,0.37421,0.37402,0.37385,0.37368,0.37351,0.37336,0.3732,0.37305,0.37291,0.37277,0.37263,0.3725,0.37239,0.37228,0.37218,0.3721,0.37202,0.37196,0.37191,0.37186,0.37182,0.37179,0.37177,0.37176,0.37176,0.37176,0.37179,0.37184,0.37191,0.372,0.37209,0.37219,0.37227,0.37234,0.37239,0.37245,0.37252,0.37261,0.37271,0.3728,0.37288,0.37294,0.37297,0.37296,0.37289,0.37276,0.37258,0.37237,0.37214,0.37191,0.3717,0.37151,0.37136,0.37124,0.3711,0.37097,0.37083,0.37071,0.3706,0.37052,0.37047,0.37046,0.3705,0.37061,0.37076,0.37095,0.37116,0.37138,0.37159,0.37179,0.37196,0.37214,0.37238,0.37263,0.37286,0.37303,0.3731,0.37307,0.37298,0.37285,0.3727,0.37255,0.37243,0.37229,0.37208,0.37181,0.37152,0.37122,0.37094,0.37071,0.37054,0.37046,0.37048,0.3706,0.37078,0.371,0.37125,0.37151,0.37175,0.37195,0.37209,0.37218,0.37224,0.37228,0.37231,0.37233,0.37235,0.37237,0.3724,0.37245,0.3725,0.37254,0.37258,0.37262,0.37266,0.3727,0.37276,0.37284,0.37293,0.37305,0.37319,0.37334,0.3735,0.37367,0.37385,0.37402,0.3742,0.37436,0.37451,0.37465,0.37478,0.37491,0.37504,0.37518,0.37532,0.37548,0.37566,0.37573,0.37561,0.37537,0.37509,0.37483,0.37467,0.37468,0.37493,0.37548,0.37602,0.3763,0.37659,0.37713,0.37816,0.37994,0.38256,0.38583,0.38953,0.39343,0.39734,0.40103,0.40492,0.40946,0.41447,0.41977,0.42516,0.43048,0.43555,0.44017,0.44417,0.4477,0.451,0.45407,0.45691,0.4595,0.46184,0.46393,0.46575,0.4673,0.46855,0.46951,0.47022,0.47071,0.47103,0.47121,0.47129,0.4713,0.4713,0.47116,0.47077,0.47019,0.46946,0.46864,0.46777,0.46691,0.46611,0.46541,0.46473,0.46395,0.46309,0.4622,0.46129,0.4604,0.45955,0.45878,0.45811,0.45753,0.45702,0.45656,0.45614,0.45574,0.45536,0.45496,0.45455,0.45411,0.45364,0.45316,0.45266,0.45216,0.45165,0.45114,0.45062,0.4501,0.44958,0.44906,0.44852,0.44798,0.44745,0.44693,0.44644,0.44598,0.44557,0.44521,0.44488,0.44455,0.44422,0.44391,0.44361,0.44333,0.44308,0.44287,0.44269,0.44257,0.44252,0.44253,0.44258,0.44265,0.44273,0.4428,0.44285,0.44285,0.44285,0.44287,0.44292,0.44297,0.44302,0.44305,0.44306,0.44304,0.44298,0.44284,0.44263,0.44238,0.4421,0.44182,0.44156,0.44136,0.44124,0.44121,0.44133,0.4416,0.44197,0.4424,0.44284,0.44324,0.44355,0.44374,0.44375,0.4436,0.44337,0.44307,0.44268,0.44223,0.44172,0.44116,0.44055,0.4399,0.43917,0.43833,0.43742,0.43645,0.43547,0.4345,0.43356,0.43268,0.4319,0.43115,0.43036,0.42957,0.42878,0.42803,0.42734,0.42681,0.42645,0.42618,0.42589,0.42549,0.42489,0.42422,0.42368,0.42318,0.42266,0.42204,0.42125,0.42022,0.41887,0.41715,0.41489,0.41211,0.40893,0.40548,0.40191,0.39835,0.39492,0.39177,0.38903,0.38648,0.38385,0.3812,0.37862,0.37617,0.37391,0.37192,0.37026,0.369,0.36822,0.36789,0.36791,0.36821,0.36869,0.36927,0.36986,0.37039,0.37075,0.37109,0.37156,0.37214,0.37278,0.37343,0.37406,0.37463,0.37509,0.37541,0.37563,0.37579,0.37592,0.37601,0.37607,0.37609,0.37609,0.37606,0.37601,0.37591,0.37573,0.37549,0.3752,0.37489,0.37457,0.37427,0.374,0.37379,0.37357,0.37333,0.37308,0.37285,0.37268,0.37259,0.37259,0.37264,0.37272,0.37283,0.37293,0.37301,0.37311,0.37328,0.3735,0.37374,0.37398,0.3742,0.37439,0.37451,0.37455,0.37448,0.37433,0.3741,0.37384,0.37355,0.37326,0.37299,0.37277,0.37262,0.37254,0.3725,0.37249,0.3725,0.37252,0.37255,0.37258,0.37259,0.3726,0.37261,0.37263,0.37265,0.37267,0.37269,0.3727,0.37271,0.37271,0.37269,0.37267,0.37265,0.37262,0.37259,0.37257,0.37255,0.37254,0.37254,0.37257,0.37263,0.37272,0.37282,0.37292,0.373,0.37306,0.37309,0.37306,0.37297,0.3728,0.37258,0.37233,0.37207,0.37182,0.37161,0.37145,0.37136,0.37136,0.37141,0.3715,0.37161,0.3717,0.37177,0.37183,0.37192,0.37203,0.37214,0.37226,0.37235,0.37245,0.37254,0.37264,0.37274,0.37283,0.37292,0.373,0.37306,0.37311,0.37315,0.3732,0.37325,0.37329,0.37333,0.37337,0.37339,0.3734,0.37339,0.37335,0.37326,0.37314,0.37299,0.37285,0.37271,0.37259,0.37251,0.37247,0.37249,0.37253,0.3726,0.37269,0.3728,0.37293,0.37307,0.37322,0.37338,0.37356,0.37376,0.37399,0.37422,0.37446,0.37471,0.37495,0.37518,0.37539,0.3756,0.37582,0.37604,0.37625,0.37647,0.37667,0.37686,0.37704,0.37719,0.3772,0.377,0.37666,0.37627,0.37589,0.37561,0.3755,0.37564,0.3761,0.37665,0.3771,0.37755,0.37811,0.37889,0.37999,0.38154,0.38363,0.38638,0.39002,0.39458,0.39984,0.40559,0.41161,0.41769,0.42362,0.42918,0.43417,0.43899,0.44412,0.4494,0.45467,0.45978,0.46457,0.46888,0.47256,0.47544,0.47753,0.479,0.47993,0.48043,0.48059,0.48052,0.4803,0.48004,0.47984,0.47947,0.47872,0.47768,0.47641,0.47502,0.47358,0.47216,0.47087,0.46977,0.4687,0.46748,0.46616,0.4648,0.46347,0.46222,0.46112,0.46023,0.4596,0.45928,0.45922,0.45936,0.45963,0.45999,0.46036,0.46069,0.46093,0.461,0.46096,0.46089,0.46079,0.46066,0.46051,0.46034,0.46013,0.4599,0.45965,0.45928,0.45876,0.45817,0.45758,0.45708,0.45673,0.45656,0.4565,0.4565,0.45653,0.45656,0.45653,0.45648,0.45646,0.45646,0.45647,0.45648,0.45647,0.45644,0.45637,0.45625,0.45608,0.45586,0.4556,0.45531,0.45501,0.45471,0.45442,0.45415,0.45392,0.4537,0.45349,0.45329,0.45309,0.4529,0.45272,0.45256,0.45242,0.4523,0.45219,0.45209,0.452,0.45192,0.45184,0.45176,0.45169,0.45163,0.45157,0.45155,0.4516,0.45171,0.45183,0.45196,0.45207,0.45213,0.45213,0.45204,0.45184,0.45155,0.45119,0.45077,0.45033,0.44987,0.44942,0.44899,0.44862,0.44828,0.44795,0.44763,0.44733,0.44705,0.44679,0.44656,0.44636,0.4462,0.44634,0.44692,0.44768,0.44837,0.44874,0.44855,0.44817,0.44801,0.44785,0.44746,0.44665,0.4452,0.443,0.44017,0.43684,0.43313,0.42918,0.42509,0.42101,0.41705,0.41335,0.40956,0.40538,0.40094,0.3964,0.3919,0.38759,0.38361,0.38011,0.37725,0.37494,0.373,0.37138,0.37006,0.369,0.36817,0.36754,0.36707,0.36673,0.36669,0.36705,0.36773,0.36863,0.36967,0.37076,0.3718,0.37271,0.37339,0.37397,0.37459,0.37525,0.37592,0.37656,0.37716,0.3777,0.37815,0.37849,0.37875,0.37897,0.37915,0.37929,0.37937,0.3794,0.37936,0.37926,0.37908,0.37875,0.37825,0.37763,0.37692,0.37619,0.37547,0.37482,0.37429,0.37391,0.37363,0.37335,0.37309,0.37286,0.37268,0.37257,0.37262,0.37286,0.3732,0.37356,0.37388,0.37407,0.37418,0.37432,0.37446,0.37461,0.37473,0.37483,0.37487,0.37486,0.37476,0.37457,0.37428,0.37393,0.37355,0.37316,0.37279,0.37248,0.37225,0.37208,0.37191,0.37176,0.37162,0.37151,0.37142,0.37136,0.37133,0.37134,0.37141,0.37158,0.37181,0.37207,0.37234,0.3726,0.37282,0.37297,0.37303,0.37301,0.37293,0.37281,0.37266,0.37248,0.37229,0.37209,0.37189,0.3717,0.3715,0.37124,0.37095,0.37065,0.37035,0.37006,0.36982,0.36963,0.36951,0.36946,0.36945,0.36949,0.36955,0.36964,0.36975,0.36986,0.36997,0.37008,0.3702,0.37034,0.37049,0.37066,0.37083,0.371,0.3712,0.37145,0.37173,0.372,0.37224,0.3724,0.37251,0.37261,0.37269,0.37275,0.3728,0.37284,0.37286,0.37288,0.37287,0.37284,0.37274,0.37261,0.37245,0.37228,0.37212,0.37198,0.37187,0.37182,0.3718,0.37181,0.37183,0.37187,0.37193,0.372,0.37208,0.37219,0.3723,0.37243,0.37259,0.37277,0.37297,0.37318,0.3734,0.37363,0.37386,0.37409,0.37433,0.37459,0.37486,0.37513,0.3754,0.37566,0.3759,0.37612,0.3763,0.37627,0.37594,0.37542,0.37481,0.37424,0.37381,0.37364,0.37383,0.3745,0.37556,0.37685,0.37838,0.38014,0.38214,0.38439,0.38689,0.38965,0.39265,0.39637,0.40099,0.40609,0.41127,0.41613,0.42025,0.42411,0.42832,0.43264,0.43686,0.44075,0.44409,0.44693,0.44948,0.45176,0.45381,0.45565,0.45731,0.45882,0.46021,0.4615,0.46265,0.46362,0.46442,0.46507,0.4656,0.46603,0.46638,0.46666,0.46692,0.46705,0.46697,0.46674,0.46638,0.46594,0.46544,0.46494,0.46446,0.46405,0.46366,0.46323,0.46277,0.46229,0.46179,0.46128,0.46076,0.46026,0.45976,0.45924,0.45867,0.45807,0.45745,0.45683,0.45622,0.45565,0.45513,0.45468,0.45431,0.454,0.45376,0.45356,0.45339,0.45324,0.45311,0.45298,0.45283,0.45267,0.45251,0.45234,0.45218,0.45202,0.45186,0.4517,0.45155,0.4514,0.45129,0.45123,0.4512,0.45117,0.45112,0.45102,0.4508,0.45047,0.45009,0.44972,0.44943,0.44929,0.44929,0.44936,0.44949,0.44967,0.44988,0.45011,0.45034,0.45056,0.45074,0.45097,0.45127,0.45163,0.452,0.45235,0.45266,0.45289,0.45299,0.45295,0.4527,0.45223,0.4516,0.45087,0.45009,0.44932,0.44862,0.44805,0.44765,0.44742,0.44731,0.44729,0.44734,0.44745,0.44758,0.44771,0.44783,0.4479,0.44798,0.44812,0.44828,0.44844,0.44859,0.44869,0.44873,0.44868,0.44851,0.4482,0.44776,0.44723,0.44664,0.44604,0.44544,0.4449,0.44445,0.44412,0.44401,0.44412,0.44439,0.44475,0.44511,0.44541,0.44557,0.44552,0.44518,0.44466,0.44407,0.44338,0.44258,0.44162,0.44049,0.43913,0.43753,0.43575,0.43384,0.43185,0.42985,0.42775,0.42547,0.42303,0.42046,0.41778,0.41502,0.41221,0.40937,0.40653,0.40344,0.39994,0.39618,0.39231,0.38848,0.38485,0.38156,0.37877,0.37663,0.37509,0.37398,0.37324,0.37278,0.37256,0.37249,0.37251,0.37256,0.37257,0.37273,0.37324,0.374,0.37491,0.3759,0.37685,0.37769,0.37831,0.37863,0.37866,0.37853,0.37827,0.37793,0.37753,0.37713,0.37677,0.37647,0.3763,0.37619,0.37607,0.37595,0.37583,0.37572,0.37562,0.37553,0.37546,0.37541,0.3754,0.37543,0.37549,0.37557,0.37567,0.37576,0.37585,0.37592,0.37597,0.376,0.37602,0.37603,0.37604,0.37603,0.37602,0.37599,0.37595,0.3759,0.37583,0.37576,0.37568,0.37559,0.37549,0.37538,0.37526,0.37513,0.37498,0.37479,0.37457,0.37434,0.37411,0.37388,0.37367,0.37348,0.37332,0.37317,0.37301,0.37283,0.37267,0.37251,0.37239,0.3723,0.37225,0.37227,0.37238,0.3726,0.37289,0.37323,0.37358,0.37392,0.37421,0.37443,0.37453,0.37453,0.37445,0.37432,0.37414,0.37393,0.37373,0.37354,0.37338,0.37327,0.3732,0.37311,0.37303,0.37295,0.37288,0.37283,0.37279,0.37277,0.37278,0.37283,0.37291,0.37301,0.37314,0.37327,0.37342,0.37355,0.37368,0.37378,0.37385,0.37387,0.37388,0.37389,0.37393,0.37401,0.37416,0.37438,0.37463,0.37488,0.37509,0.37524,0.37534,0.37543,0.37551,0.37558,0.37564,0.37569,0.37572,0.37575,0.37577,0.37575,0.3757,0.37562,0.37552,0.37542,0.37531,0.37523,0.37516,0.37514,0.37513,0.37513,0.37514,0.37515,0.37518,0.37522,0.37528,0.37537,0.37548,0.37563,0.3758,0.37601,0.37623,0.37647,0.37672,0.37697,0.37723,0.37747,0.37773,0.37801,0.37831,0.37863,0.37894,0.37924,0.37952,0.37978,0.37999,0.38003,0.37982,0.37944,0.379,0.3786,0.37832,0.37827,0.37854,0.37922,0.38015,0.38115,0.38226,0.38353,0.38501,0.38675,0.38879,0.3912,0.39401,0.39746,0.40159,0.40617,0.41094,0.41567,0.42011,0.42494,0.43067,0.43682,0.44291,0.44846,0.453,0.45689,0.46075,0.46449,0.46805,0.47133,0.47426,0.47676,0.47874,0.48012,0.48069,0.48041,0.47946,0.47803,0.4763,0.47445,0.47266,0.47112,0.47001,0.46912,0.46814,0.46712,0.46608,0.46507,0.46413,0.46331,0.46263,0.46213,0.46181,0.4616,0.46149,0.46147,0.4615,0.46159,0.4617,0.46183,0.46195,0.46215,0.46247,0.46289,0.46335,0.46383,0.46427,0.46465,0.46491,0.46501,0.465,0.46492,0.46479,0.46462,0.46441,0.46416,0.4639,0.46361,0.46332,0.46296,0.4625,0.46195,0.46136,0.46076,0.46019,0.45966,0.45923,0.45891,0.45877,0.45879,0.4589,0.45904,0.45911,0.45907,0.459,0.459,0.45903,0.45904,0.45899,0.45885,0.45857,0.45817,0.45769,0.45714,0.45656,0.45596,0.45538,0.45483,0.45436,0.4539,0.45341,0.45291,0.45241,0.45195,0.45152,0.45115,0.45087,0.45067,0.45063,0.45074,0.45097,0.45128,0.45162,0.45197,0.45228,0.4525,0.4526,0.45263,0.45264,0.45264,0.45263,0.4526,0.45256,0.4525,0.45242,0.45232,0.45216,0.45189,0.45156,0.45118,0.4508,0.45044,0.45013,0.4499,0.44978,0.44984,0.45008,0.45045,0.45088,0.45132,0.45171,0.452,0.45213,0.45204,0.45189,0.45183,0.4518,0.45172,0.45154,0.45119,0.45061,0.44972,0.44847,0.44678,0.44466,0.44219,0.43946,0.43655,0.43353,0.43049,0.4275,0.42465,0.4218,0.41881,0.4157,0.41251,0.40927,0.40602,0.40279,0.39961,0.39653,0.39336,0.38995,0.38642,0.38287,0.3794,0.37613,0.37315,0.37056,0.36848,0.36682,0.3654,0.36422,0.36327,0.36254,0.36204,0.36174,0.36165,0.36176,0.36232,0.36351,0.36516,0.36711,0.3692,0.37128,0.37319,0.37476,0.37583,0.37649,0.37692,0.37717,0.37728,0.37728,0.37722,0.37712,0.37703,0.37699,0.37694,0.37681,0.37662,0.37639,0.37615,0.37589,0.37566,0.37546,0.37532,0.37522,0.37514,0.37508,0.37503,0.37498,0.37493,0.37488,0.37482,0.37474,0.37466,0.3746,0.37454,0.37447,0.37439,0.3743,0.37414,0.37391,0.37366,0.37342,0.37322,0.3731,0.37304,0.37301,0.37301,0.37301,0.37303,0.37307,0.37311,0.37315,0.3732,0.37328,0.37339,0.37354,0.3737,0.37386,0.37401,0.37415,0.37425,0.3743,0.3743,0.37428,0.37423,0.37416,0.37408,0.37399,0.3739,0.37381,0.37374,0.37366,0.37357,0.37347,0.37337,0.37326,0.37315,0.37305,0.37295,0.37287,0.37277,0.37264,0.37249,0.37234,0.3722,0.3721,0.37205,0.37206,0.37216,0.37237,0.37269,0.37309,0.37355,0.37403,0.3745,0.37492,0.37528,0.37553,0.3757,0.37583,0.37593,0.376,0.37603,0.37603,0.376,0.37593,0.37582,0.3756,0.37523,0.37479,0.37434,0.37398,0.37376,0.37366,0.37359,0.37354,0.37352,0.37351,0.37351,0.37355,0.37363,0.37376,0.37391,0.37408,0.37425,0.37441,0.37454,0.37465,0.37471,0.37473,0.37474,0.37474,0.37474,0.37475,0.37479,0.37486,0.37498,0.37515,0.37537,0.37562,0.3759,0.37619,0.37649,0.37677,0.37704,0.37727,0.37744,0.37753,0.37756,0.37758,0.3776,0.37767,0.37781,0.37806,0.37844,0.37888,0.37932,0.37978,0.38028,0.38084,0.38148,0.38222,0.3831,0.38411,0.38509,0.38591,0.38667,0.38749,0.38849,0.38978,0.39147,0.39368,0.39651,0.40013,0.4045,0.40946,0.41484,0.42048,0.42621,0.43188,0.43733,0.44238,0.44789,0.45443,0.46139,0.46818,0.47418,0.4788,0.48245,0.48588,0.48897,0.49163,0.49373,0.49515,0.49563,0.4951,0.49377,0.49185,0.48957,0.48713,0.48475,0.48264,0.48101,0.47958,0.47794,0.47616,0.47429,0.47238,0.47052,0.46874,0.46711,0.4657,0.46444,0.46327,0.46217,0.46115,0.46021,0.45936,0.45858,0.45789,0.45729,0.45681,0.45646,0.45622,0.45606,0.45596,0.45589,0.45582,0.45574,0.45562,0.4555,0.45542,0.45537,0.45534,0.4553,0.45524,0.45514,0.455,0.45478,0.45448,0.4541,0.45365,0.45317,0.45267,0.45217,0.45169,0.45126,0.4509,0.45062,0.45039,0.45021,0.45006,0.44994,0.44981,0.44968,0.44952,0.44933,0.4491,0.44886,0.44861,0.44835,0.4481,0.44784,0.4476,0.44737,0.44715,0.44695,0.44676,0.44657,0.44638,0.44618,0.44597,0.44574,0.44549,0.44522,0.44492,0.44459,0.44424,0.44389,0.44354,0.44321,0.44291,0.44264,0.44241,0.44223,0.44206,0.44191,0.44179,0.4417,0.44164,0.44161,0.44163,0.44168,0.44178,0.44194,0.44213,0.44235,0.44259,0.44282,0.44303,0.44322,0.44336,0.44348,0.44361,0.44374,0.44386,0.44397,0.44405,0.44411,0.44414,0.44412,0.44408,0.44403,0.44397,0.44389,0.44378,0.44366,0.4435,0.44332,0.44309,0.44289,0.44275,0.44264,0.44252,0.44235,0.44211,0.44175,0.44124,0.44055,0.43972,0.4388,0.43779,0.43668,0.43545,0.4341,0.43264,0.43108,0.4294,0.4276,0.42567,0.42359,0.42125,0.41862,0.41575,0.41272,0.40958,0.40642,0.40328,0.40025,0.39738,0.39443,0.39121,0.38782,0.38441,0.38109,0.37799,0.37524,0.37296,0.37128,0.37025,0.36977,0.36973,0.37004,0.37058,0.37125,0.37195,0.37257,0.373,0.37343,0.37408,0.37487,0.37574,0.37663,0.37745,0.37815,0.37866,0.37891,0.3789,0.37871,0.37838,0.37795,0.37748,0.37699,0.37654,0.37616,0.3759,0.37571,0.37554,0.37538,0.37523,0.37508,0.37494,0.37481,0.37468,0.37456,0.37445,0.37436,0.37427,0.3742,0.37413,0.37408,0.37404,0.37402,0.374,0.37397,0.37391,0.37384,0.37378,0.37375,0.37375,0.37383,0.37398,0.37415,0.37432,0.37444,0.37455,0.37469,0.37486,0.37503,0.37521,0.37538,0.37553,0.37564,0.37571,0.37574,0.37574,0.37571,0.37566,0.37559,0.37552,0.37544,0.37536,0.37528,0.3752,0.37508,0.37495,0.37481,0.37466,0.37451,0.37437,0.37425,0.37416,0.37407,0.37396,0.37386,0.37376,0.37368,0.37362,0.37361,0.37364,0.37373,0.37392,0.37423,0.37463,0.37507,0.37552,0.37596,0.37635,0.37666,0.37685,0.37694,0.37697,0.37694,0.37688,0.37677,0.37663,0.37646,0.37626,0.37606,0.37578,0.37539,0.37493,0.37442,0.37391,0.37343,0.37301,0.37268,0.37247,0.37239,0.37238,0.37242,0.3725,0.3726,0.3727,0.37288,0.37321,0.37361,0.37401,0.37437,0.3746,0.37473,0.37483,0.37491,0.37497,0.37501,0.37504,0.37507,0.37509,0.37511,0.37512,0.37508,0.37502,0.37495,0.37488,0.37481,0.37477,0.37476,0.37479,0.37486,0.37493,0.37501,0.37512,0.37524,0.37539,0.37557,0.37578,0.37603,0.3762,0.37624,0.3762,0.37614,0.37612,0.3762,0.37645,0.37692,0.37769,0.37857,0.37941,0.38029,0.38129,0.38247,0.38393,0.38573,0.38795,0.39067,0.39409,0.39827,0.40303,0.40821,0.41362,0.41911,0.4245,0.42962,0.43431,0.43897,0.44401,0.44924,0.45451,0.45964,0.46445,0.46878,0.47245,0.47528,0.47728,0.47866,0.47957,0.48012,0.48048,0.48078,0.48052,0.47936,0.47765,0.47575,0.47404,0.47287,0.47196,0.47085,0.46961,0.46828,0.46695,0.46567,0.46451,0.46353,0.4628,0.46232,0.46203,0.46188,0.46186,0.4619,0.46199,0.46207,0.46211,0.46208,0.46202,0.46201,0.46202,0.46204,0.46205,0.46203,0.46196,0.46183,0.46161,0.46126,0.46075,0.46013,0.45945,0.45874,0.45805,0.45743,0.45691,0.45653,0.45631,0.45618,0.45614,0.45616,0.45623,0.45632,0.45642,0.45652,0.45658,0.45667,0.45682,0.45703,0.45726,0.45749,0.4577,0.45786,0.45795,0.45796,0.45789,0.45778,0.45763,0.45744,0.45722,0.45696,0.45666,0.45633,0.45596,0.45557,0.45516,0.45472,0.45425,0.45375,0.45322,0.45255,0.45171,0.45079,0.44986,0.44903,0.44838,0.44781,0.44722,0.44661,0.44601,0.44545,0.44496,0.44455,0.44425,0.44409,0.44412,0.44433,0.44468,0.44514,0.44567,0.44621,0.44673,0.44719,0.44755,0.44786,0.44819,0.44854,0.44888,0.4492,0.44948,0.44971,0.44987,0.44995,0.44992,0.44979,0.44958,0.44932,0.44903,0.44874,0.44847,0.44825,0.4481,0.44808,0.44819,0.44839,0.44864,0.44887,0.44904,0.44911,0.44903,0.44874,0.44828,0.44772,0.44706,0.4463,0.44546,0.44455,0.44355,0.44249,0.44137,0.44014,0.43876,0.43725,0.43566,0.43401,0.43232,0.43062,0.42895,0.42733,0.42586,0.42453,0.42324,0.42186,0.4203,0.41842,0.41634,0.41423,0.41205,0.40976,0.40736,0.40479,0.40184,0.39839,0.3946,0.39066,0.38672,0.38296,0.37955,0.37665,0.37443,0.37288,0.3718,0.37113,0.3708,0.37072,0.37083,0.37105,0.37131,0.37153,0.37191,0.37262,0.37356,0.37464,0.37577,0.37684,0.37777,0.37845,0.3788,0.37891,0.37896,0.37896,0.37891,0.37884,0.37875,0.37865,0.37856,0.37848,0.37841,0.37835,0.37828,0.37822,0.37816,0.3781,0.37804,0.37798,0.37792,0.37787,0.37782,0.37777,0.37774,0.3777,0.37766,0.37762,0.37759,0.37755,0.37752,0.37751,0.37752,0.37754,0.37755,0.37754,0.3775,0.37743,0.37732,0.37718,0.37703,0.37686,0.37669,0.37652,0.37631,0.37604,0.37573,0.37543,0.37515,0.37493,0.37474,0.37453,0.37431,0.37411,0.37391,0.37375,0.37363,0.37356,0.37356,0.37364,0.37381,0.37404,0.37431,0.37461,0.37489,0.37516,0.37537,0.37551,0.37561,0.37571,0.37581,0.3759,0.37598,0.37605,0.3761,0.37612,0.37612,0.37606,0.37594,0.37577,0.37557,0.37535,0.37514,0.37494,0.37477,0.37465,0.37456,0.37448,0.37441,0.37434,0.37429,0.37425,0.37423,0.37422,0.37423,0.37427,0.37433,0.37441,0.3745,0.37461,0.37472,0.37484,0.37495,0.37506,0.37519,0.37534,0.37551,0.37569,0.37588,0.37606,0.37624,0.37639,0.37652,0.37662,0.37668,0.37671,0.37673,0.37674,0.37674,0.37676,0.37679,0.37684,0.37691,0.37698,0.37705,0.37713,0.37721,0.37732,0.37744,0.37759,0.37777,0.37798,0.37823,0.37851,0.37881,0.37912,0.37943,0.37974,0.38004,0.38032,0.38056,0.38076,0.38094,0.38111,0.38128,0.38146,0.38167,0.38191,0.3822,0.38244,0.38257,0.38264,0.38271,0.38285,0.38311,0.38354,0.38422,0.38519,0.38633,0.38752,0.38881,0.39022,0.39181,0.39363,0.39571,0.3981,0.40085,0.40413,0.408,0.41234,0.417,0.42185,0.42674,0.43156,0.43615,0.44038,0.44463,0.44926,0.45408,0.45894,0.46364,0.46801,0.47188,0.47508,0.47742,0.47879,0.47935,0.47936,0.47905,0.47869,0.4785,0.47795,0.47656,0.47467,0.47265,0.47086,0.46965,0.46887,0.46813,0.46742,0.46674,0.46608,0.46544,0.46482,0.46421,0.4636,0.46298,0.46232,0.46163,0.46093,0.46023,0.45954,0.45886,0.45822,0.45762,0.45701,0.45635,0.45568,0.455,0.45435,0.45375,0.45323,0.4528,0.45251,0.45238,0.4524,0.45255,0.45278,0.45306,0.45333,0.45358,0.45375,0.45381,0.4538,0.4538,0.45381,0.4538,0.45378,0.45373,0.45366,0.45355,0.4534,0.45317,0.45284,0.45244,0.45198,0.4515,0.45102,0.45056,0.45014,0.44979,0.44952,0.44931,0.44915,0.44902,0.44891,0.4488,0.44869,0.44854,0.44836,0.44813,0.44785,0.44756,0.44726,0.44698,0.44674,0.44649,0.44621,0.44591,0.44564,0.44541,0.44525,0.44517,0.44513,0.44513,0.44516,0.44522,0.44531,0.44541,0.44552,0.44563,0.44581,0.44607,0.4464,0.44674,0.44707,0.44735,0.44753,0.44758,0.44746,0.44714,0.44664,0.446,0.44527,0.44451,0.44375,0.44306,0.44247,0.44204,0.44179,0.44169,0.4417,0.44178,0.44188,0.44195,0.44197,0.44187,0.44163,0.44144,0.44147,0.44162,0.44175,0.44177,0.44156,0.441,0.43999,0.43841,0.43615,0.43326,0.42987,0.4261,0.42208,0.41793,0.41378,0.40975,0.40597,0.40197,0.39737,0.3924,0.38728,0.38227,0.37759,0.37348,0.37016,0.36789,0.36672,0.36638,0.36662,0.36716,0.36774,0.36811,0.36887,0.37056,0.37276,0.37506,0.37705,0.37832,0.37902,0.3796,0.38005,0.3804,0.38067,0.38086,0.381,0.38109,0.38115,0.38118,0.38117,0.38111,0.38102,0.38089,0.38072,0.38052,0.3803,0.38004,0.37969,0.37922,0.37865,0.37801,0.37735,0.37668,0.37606,0.37549,0.37503,0.37461,0.37417,0.37372,0.3733,0.37291,0.3726,0.37236,0.37224,0.37225,0.37245,0.37285,0.3734,0.37403,0.3747,0.37535,0.37592,0.37636,0.37663,0.37671,0.37669,0.37658,0.37641,0.37622,0.37602,0.37585,0.37572,0.37568,0.37569,0.3757,0.37572,0.37574,0.37577,0.37581,0.37586,0.37591,0.376,0.37614,0.37632,0.37652,0.37672,0.37691,0.37708,0.3772,0.37726,0.37729,0.37731,0.37732,0.37731,0.37729,0.37725,0.37718,0.37709,0.37697,0.37679,0.37653,0.3762,0.37584,0.37547,0.37511,0.37477,0.37449,0.37429,0.37413,0.37398,0.37384,0.37373,0.37365,0.3736,0.3736,0.37365,0.37375,0.37395,0.37425,0.37462,0.37505,0.37551,0.37596,0.37638,0.37675,0.37703,0.37725,0.37744,0.37761,0.37776,0.3779,0.37802,0.37813,0.37824,0.37835,0.37846,0.37856,0.37865,0.37872,0.37879,0.37883,0.37886,0.37887,0.37886,0.3788,0.3787,0.37855,0.37839,0.37821,0.37805,0.3779,0.3778,0.37775,0.37773,0.3777,0.37768,0.37767,0.37771,0.37779,0.37795,0.37821,0.37853,0.37885,0.37916,0.3794,0.37961,0.37986,0.38014,0.38042,0.38068,0.38092,0.38111,0.38124,0.38129,0.38128,0.38123,0.38115,0.38105,0.38094,0.38083,0.38072,0.38063,0.38055,0.38045,0.38029,0.3801,0.37988,0.37966,0.37947,0.37932,0.37923,0.37923,0.37913,0.37878,0.37828,0.37772,0.37721,0.37682,0.37665,0.3768,0.37735,0.37828,0.37949,0.38098,0.38276,0.38485,0.38725,0.38997,0.39302,0.3964,0.40052,0.40558,0.41133,0.4175,0.42384,0.43009,0.43599,0.44127,0.44568,0.44952,0.45326,0.45682,0.46016,0.46321,0.46592,0.46824,0.4701,0.47145,0.47198,0.47164,0.47075,0.46962,0.46857,0.4679,0.4672,0.46598,0.46449,0.46296,0.46163,0.46073,0.46015,0.45961,0.4591,0.45863,0.45819,0.45778,0.45739,0.45703,0.4567,0.45642,0.45624,0.45612,0.45604,0.45599,0.45592,0.45583,0.45569,0.45547,0.45517,0.4548,0.45439,0.45395,0.45349,0.45304,0.45261,0.45222,0.45187,0.45159,0.45136,0.45117,0.451,0.45086,0.45072,0.45058,0.45042,0.45023,0.45,0.44972,0.44941,0.44908,0.44874,0.44842,0.44812,0.44785,0.44764,0.44749,0.44738,0.4473,0.44725,0.44723,0.44722,0.44722,0.44723,0.44723,0.44723,0.44722,0.44722,0.44723,0.44726,0.44732,0.44742,0.44757,0.44777,0.44812,0.44864,0.44925,0.44983,0.45031,0.45058,0.45072,0.45084,0.45093,0.45099,0.451,0.45096,0.45085,0.45067,0.45041,0.45011,0.44975,0.44935,0.44891,0.44845,0.44797,0.44741,0.44672,0.44595,0.44514,0.44433,0.44359,0.44294,0.44243,0.44212,0.44202,0.44208,0.44228,0.44255,0.44285,0.44314,0.44337,0.44349,0.44346,0.44344,0.44358,0.44381,0.44406,0.44424,0.44428,0.44411,0.44365,0.44283,0.44167,0.44028,0.4387,0.43696,0.43512,0.43321,0.43127,0.42936,0.42751,0.42566,0.42371,0.42167,0.41952,0.41728,0.41493,0.41247,0.40991,0.40724,0.40402,0.40001,0.39548,0.3907,0.38596,0.38153,0.37768,0.37469,0.37283,0.37186,0.37127,0.371,0.37097,0.37111,0.37135,0.3716,0.3718,0.37187,0.37195,0.37221,0.37261,0.37311,0.37365,0.37419,0.37469,0.3751,0.37538,0.37556,0.37573,0.37586,0.37598,0.37606,0.37611,0.37612,0.3761,0.37603,0.3759,0.3757,0.37544,0.37514,0.37483,0.37453,0.37425,0.37402,0.37385,0.37374,0.37365,0.37358,0.37352,0.37348,0.37345,0.37342,0.3734,0.37338,0.37337,0.37338,0.37341,0.37344,0.37347,0.3735,0.37351,0.37351,0.37347,0.37342,0.37335,0.37328,0.3732,0.37311,0.37302,0.37294,0.37286,0.37278,0.37272,0.37265,0.37259,0.37254,0.37249,0.37245,0.37241,0.37238,0.37235],"showlegend":true,"mode":"lines","type":"scatter","line":{"color":"rgb(120,120,120)","width":2},"name":"Gcc loess fit","marker":{"color":"rgba(255,127,14,1)","line":{"color":"rgba(255,127,14,1)"}},"error_y":{"color":"rgba(255,127,14,1)"},"error_x":{"color":"rgba(255,127,14,1)"},"xaxis":"x","yaxis":"y","frame":null},{"x":["2009-04-27","2010-04-20","2011-05-01","2012-04-21","2013-04-30","2014-05-07","2015-05-01","2016-05-06","2017-05-01","2018-05-02","2019-05-03","2020-05-12"],"y":[0.37729,0.37754,0.37954,0.38198,0.38256,0.38363,0.38214,0.38501,0.38591,0.38393,0.38633,0.38485],"showlegend":true,"mode":"markers","type":"scatter","marker":{"color":"#7FFF00","symbol":"circle","line":{"color":"rgba(44,160,44,1)"}},"name":"SOS (10%)","error_y":{"color":"rgba(44,160,44,1)"},"error_x":{"color":"rgba(44,160,44,1)"},"line":{"color":"rgba(44,160,44,1)"},"xaxis":"x","yaxis":"y","frame":null},{"x":["2009-04-23","2009-04-30",null,"2010-04-11","2010-04-23",null,"2011-04-29","2011-05-04",null,"2012-04-14","2012-04-26",null,"2013-04-28","2013-05-02",null,"2014-05-05","2014-05-09",null,"2015-04-29","2015-05-03",null,"2016-05-03","2016-05-09",null,"2017-04-27","2017-05-06",null,"2018-04-30","2018-05-05",null,"2019-04-29","2019-05-07",null,"2020-05-11","2020-05-15"],"y":[0.37729,0.37729,null,0.37754,0.37754,null,0.37954,0.37954,null,0.38198,0.38198,null,0.38256,0.38256,null,0.38363,0.38363,null,0.38214,0.38214,null,0.38501,0.38501,null,0.38591,0.38591,null,0.38393,0.38393,null,0.38633,0.38633,null,0.38485,0.38485],"showlegend":false,"mode":"lines","type":"scatter","line":{"color":"#7FFF00"},"name":"SOS (10%) - CI","marker":{"color":"rgba(214,39,40,1)","line":{"color":"rgba(214,39,40,1)"}},"error_y":{"color":"rgba(214,39,40,1)"},"error_x":{"color":"rgba(214,39,40,1)"},"xaxis":"x","yaxis":"y","frame":null},{"x":["2009-05-02","2010-04-25","2011-05-07","2012-04-30","2013-05-04","2014-05-10","2015-05-05","2016-05-11","2017-05-10","2018-05-07","2019-05-11","2020-05-17"],"y":[0.3889,0.38978,0.39489,0.39693,0.39734,0.39458,0.39265,0.39746,0.4045,0.39827,0.40085,0.40052],"showlegend":true,"mode":"markers","type":"scatter","marker":{"color":"#66CD00","symbol":"square","line":{"color":"rgba(148,103,189,1)"}},"name":"SOS (25%)","error_y":{"color":"rgba(148,103,189,1)"},"error_x":{"color":"rgba(148,103,189,1)"},"line":{"color":"rgba(148,103,189,1)"},"xaxis":"x","yaxis":"y","frame":null},{"x":["2009-05-01","2009-05-04",null,"2010-04-24","2010-04-27",null,"2011-05-05","2011-05-09",null,"2012-04-29","2012-05-02",null,"2013-05-03","2013-05-06",null,"2014-05-09","2014-05-12",null,"2015-05-04","2015-05-07",null,"2016-05-10","2016-05-13",null,"2017-05-09","2017-05-11",null,"2018-05-06","2018-05-09",null,"2019-05-10","2019-05-13",null,"2020-05-16","2020-05-18"],"y":[0.3889,0.3889,null,0.38978,0.38978,null,0.39489,0.39489,null,0.39693,0.39693,null,0.39734,0.39734,null,0.39458,0.39458,null,0.39265,0.39265,null,0.39746,0.39746,null,0.4045,0.4045,null,0.39827,0.39827,null,0.40085,0.40085,null,0.40052,0.40052],"showlegend":false,"mode":"lines","type":"scatter","line":{"color":"#66CD00"},"name":"SOS (25%) - CI","marker":{"color":"rgba(140,86,75,1)","line":{"color":"rgba(140,86,75,1)"}},"error_y":{"color":"rgba(140,86,75,1)"},"error_x":{"color":"rgba(140,86,75,1)"},"xaxis":"x","yaxis":"y","frame":null},{"x":["2009-05-10","2010-05-01","2011-05-13","2012-05-07","2013-05-10","2014-05-16","2015-05-11","2016-05-18","2017-05-16","2018-05-13","2019-05-18","2020-05-22"],"y":[0.41811,0.41839,0.42211,0.42737,0.42516,0.42918,0.42025,0.43067,0.43733,0.42962,0.43156,0.43009],"showlegend":true,"mode":"markers","type":"scatter","marker":{"color":"#458B00","symbol":"diamond","line":{"color":"rgba(227,119,194,1)"}},"name":"SOS (50%)","error_y":{"color":"rgba(227,119,194,1)"},"error_x":{"color":"rgba(227,119,194,1)"},"line":{"color":"rgba(227,119,194,1)"},"xaxis":"x","yaxis":"y","frame":null},{"x":["2009-05-08","2009-05-11",null,"2010-04-29","2010-05-02",null,"2011-05-11","2011-05-14",null,"2012-05-05","2012-05-08",null,"2013-05-08","2013-05-11",null,"2014-05-14","2014-05-17",null,"2015-05-09","2015-05-12",null,"2016-05-16","2016-05-19",null,"2017-05-14","2017-05-17",null,"2018-05-11","2018-05-14",null,"2019-05-16","2019-05-19",null,"2020-05-20","2020-05-23"],"y":[0.41811,0.41811,null,0.41839,0.41839,null,0.42211,0.42211,null,0.42737,0.42737,null,0.42516,0.42516,null,0.42918,0.42918,null,0.42025,0.42025,null,0.43067,0.43067,null,0.43733,0.43733,null,0.42962,0.42962,null,0.43156,0.43156,null,0.43009,0.43009],"showlegend":false,"mode":"lines","type":"scatter","line":{"color":"#458B00"},"name":"SOS (50%) - CI","marker":{"color":"rgba(127,127,127,1)","line":{"color":"rgba(127,127,127,1)"}},"error_y":{"color":"rgba(127,127,127,1)"},"error_x":{"color":"rgba(127,127,127,1)"},"xaxis":"x","yaxis":"y","frame":null},{"x":["2019-10-12","2018-10-22","2017-10-22","2016-10-17","2015-10-18","2014-10-11","2013-10-03","2012-10-08","2011-10-11","2010-10-07","2009-10-11","2008-10-13"],"y":[0.4261,0.42453,0.42567,0.4218,0.42046,0.42509,0.42266,0.4168,0.42114,0.41362,0.41665,0.41077],"showlegend":true,"mode":"markers","type":"scatter","marker":{"color":"#FFB90F","symbol":"diamond","line":{"color":"rgba(188,189,34,1)"}},"name":"EOS (50%)","error_y":{"color":"rgba(188,189,34,1)"},"error_x":{"color":"rgba(188,189,34,1)"},"line":{"color":"rgba(188,189,34,1)"},"xaxis":"x","yaxis":"y","frame":null},{"x":["2019-10-14","2019-10-11",null,"2018-10-26","2018-10-19",null,"2017-10-24","2017-10-20",null,"2016-10-19","2016-10-16",null,"2015-10-21","2015-10-17",null,"2014-10-13","2014-10-10",null,"2013-10-08","2013-09-26",null,"2012-10-10","2012-10-06",null,"2011-10-14","2011-10-09",null,"2010-10-09","2010-10-05",null,"2009-10-14","2009-10-10",null,"2008-10-20","2008-10-05"],"y":[0.4261,0.4261,null,0.42453,0.42453,null,0.42567,0.42567,null,0.4218,0.4218,null,0.42046,0.42046,null,0.42509,0.42509,null,0.42266,0.42266,null,0.4168,0.4168,null,0.42114,0.42114,null,0.41362,0.41362,null,0.41665,0.41665,null,0.41077,0.41077],"showlegend":false,"mode":"lines","type":"scatter","line":{"color":"#FFB90F"},"name":"EOS (50%) - CI","marker":{"color":"rgba(23,190,207,1)","line":{"color":"rgba(23,190,207,1)"}},"error_y":{"color":"rgba(23,190,207,1)"},"error_x":{"color":"rgba(23,190,207,1)"},"xaxis":"x","yaxis":"y","frame":null},{"x":["2019-10-19","2018-11-02","2017-10-30","2016-10-25","2015-10-26","2014-10-18","2013-10-13","2012-10-15","2011-10-23","2010-10-14","2009-10-18","2008-10-20"],"y":[0.39737,0.40184,0.40328,0.39653,0.39618,0.3964,0.40191,0.39371,0.39965,0.38999,0.39197,0.38616],"showlegend":true,"mode":"markers","type":"scatter","marker":{"color":"#CD950C","symbol":"square","line":{"color":"rgba(31,119,180,1)"}},"name":"EOS (25%)","error_y":{"color":"rgba(31,119,180,1)"},"error_x":{"color":"rgba(31,119,180,1)"},"line":{"color":"rgba(31,119,180,1)"},"xaxis":"x","yaxis":"y","frame":null},{"x":["2019-10-20","2019-10-17",null,"2018-11-03","2018-10-30",null,"2017-10-31","2017-10-28",null,"2016-10-26","2016-10-23",null,"2015-10-27","2015-10-24",null,"2014-10-19","2014-10-16",null,"2013-10-14","2013-10-11",null,"2012-10-16","2012-10-13",null,"2011-10-25","2011-10-21",null,"2010-10-15","2010-10-12",null,"2009-10-19","2009-10-16",null,"2008-10-25","2008-10-13"],"y":[0.39737,0.39737,null,0.40184,0.40184,null,0.40328,0.40328,null,0.39653,0.39653,null,0.39618,0.39618,null,0.3964,0.3964,null,0.40191,0.40191,null,0.39371,0.39371,null,0.39965,0.39965,null,0.38999,0.38999,null,0.39197,0.39197,null,0.38616,0.38616],"showlegend":false,"mode":"lines","type":"scatter","line":{"color":"#CD950C"},"name":"EOS (25%) - CI","marker":{"color":"rgba(255,127,14,1)","line":{"color":"rgba(255,127,14,1)"}},"error_y":{"color":"rgba(255,127,14,1)"},"error_x":{"color":"rgba(255,127,14,1)"},"xaxis":"x","yaxis":"y","frame":null},{"x":["2019-10-21","2018-11-05","2017-11-03","2016-10-29","2015-10-30","2014-10-21","2013-10-17","2012-10-19","2011-10-28","2010-10-17","2009-10-22","2008-10-23"],"y":[0.38728,0.39066,0.39121,0.38287,0.38156,0.38361,0.38903,0.38093,0.38694,0.38006,0.37754,0.37568],"showlegend":true,"mode":"markers","type":"scatter","marker":{"color":"#8B6508","symbol":"circle","line":{"color":"rgba(44,160,44,1)"}},"name":"EOS (10%)","error_y":{"color":"rgba(44,160,44,1)"},"error_x":{"color":"rgba(44,160,44,1)"},"line":{"color":"rgba(44,160,44,1)"},"xaxis":"x","yaxis":"y","frame":null},{"x":["2019-10-22","2019-10-19",null,"2018-11-06","2018-11-03",null,"2017-11-05","2017-11-01",null,"2016-10-30","2016-10-27",null,"2015-10-31","2015-10-28",null,"2014-10-22","2014-10-19",null,"2013-10-18","2013-10-15",null,"2012-10-21","2012-10-17",null,"2011-10-30","2011-10-26",null,"2010-10-19","2010-10-15",null,"2009-10-23","2009-10-20",null,"2008-10-29","2008-10-17"],"y":[0.38728,0.38728,null,0.39066,0.39066,null,0.39121,0.39121,null,0.38287,0.38287,null,0.38156,0.38156,null,0.38361,0.38361,null,0.38903,0.38903,null,0.38093,0.38093,null,0.38694,0.38694,null,0.38006,0.38006,null,0.37754,0.37754,null,0.37568,0.37568],"showlegend":false,"mode":"lines","type":"scatter","line":{"color":"#8B6508"},"name":"EOS (10%) - CI","marker":{"color":"rgba(214,39,40,1)","line":{"color":"rgba(214,39,40,1)"}},"error_y":{"color":"rgba(214,39,40,1)"},"error_x":{"color":"rgba(214,39,40,1)"},"xaxis":"x","yaxis":"y","frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->



What is the difference in 25% greenness onset for your first site? #hint, look at the spring dataframe you just generated



```r
#some hints to get you started
# d=spring$transition_25
# d=as.Date(d)
# d
```



```r
#more code hints
# dates_split <- data.frame(date = d,
#                  year = as.numeric(format(d, format = "%Y")),
#                  month = as.numeric(format(d, format = "%m")),
#                  day = as.numeric(format(d, format = "%d")))
```



Generate a plot of smoothed gcc and transition dates for your two sites and subplot them.  What do you notice?



```r
#some hint code for subplotting in plot_ly:
#p <- subplot(p1, p2, nrows=2)
#p
```

### In Class Hands-on Coding: Comparing phenology of the same plant function type (PFT) across climate space

As Dr. Richardson mentioned in his introduction lecture, the same plant functional types (e.g. grasslands) can have very different phenologogical cycles.  Let's pick two phenocam grassland sites: one from a tropical climate (kamuela), and one from an arid climate (konza):



```r
GrassSites=GrassSites['filter for your sites']
```

Now pull data for those sites via `phenocamr` or the `phenocamapi`



```r
print('code here')
```

```
## [1] "code here"
```

Now let's create a subplot of your grasslands to compare phenology, some hint code below:



```r
#some hint code for subplotting in plot_ly:
#p <- subplot(p1, p2, nrows=2)
#p
```

Once you have a subplot of grassland phenology across 2 climates answer the following questions in your markdown:
1. What seasonal patterns do you see?
2. Do you think you set your thresholds correctly for transition dates/phenophases?  How might that very as a function of climate?
3. What are the challenges of forecasting or modeling tropical versus arid grasslands?


## Digital Repeat Photography Coding Lab


### Quantifying haze and redness to evaluate California wildfires

1. Pull mid-day imagery for September 1-7th, 2019 and 2020 for the canopy-level camera `NEON.D17.SOAP.DP1.00033`.  Create a 2-panel plot showing those images in 2019 (left) and 2020 (right).

2. Use the `hazeR` package to quantify the haze in each of those images.  Print a summary of your results.

3. Generate a density function RGB plot for your haziest image in 2020, and one for the same date in 2019.  Create a 2-panel plot showing 2019 on the left and 2020 on the right.  

4. Pull timesseries data via the `phenocamapi` package.  Calculate the difference in the rcc90 between 2019 and 2020 over the same time period as your images.

5. Create a summary plot showing haze as a bar and the differenece in rcc90 from *question 4* as a timersies.

6. Answer the following questions:

  + Does the `hazeR` package pick up smokey images?
  
  + If you were to use color coordinates, which color band would be most useful to highlight smoke and why?
  
  **Optional Bonus Points:** 
  Repeat the above calculations for the understory camera on the same tower `NEON.D17.SOAP.DP1.00042` and produce the same plots.  Which camera is 'better' and capturing wildfire?  Why do you think that is so?
  
## **Intro to PhenoCam Culmination Activity**

Write up a 1-page summary of a project that you might want to explore using PhenoCam data over the duration of this course. Include the types of PhenoCam (and other data) that you will need to implement this project. Save this summary as you will be refining and adding to your ideas over the course of the semester.