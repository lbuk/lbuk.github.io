---
layout: post
title: Fresnel Map
description: A new equal-area thematic mapping technique
permalink: portfolio/FresnelMap/
img: /img/zoom_fresnel_map_portfolio.png
---

The Codex Atlanticus 221v-b depicts a diagram with a set of consecutive circles. Each crescent has the same area as the central circle. Utilised by the likes of Fresnel and March, this geometric technique has been applied in multiple spheres such as architecture and civil engineering.

I utilised Fresnel's circles as part of a novel mapping technique in which each 'doughnut' (or annuli) has the same area as the central circle. This visual technique, created in early 2020 during my doctoral research, is well-suited to addressing the Modifiable Areal Unit Problem (MAUP). More information can be found in my <a href="https://discovery.ucl.ac.uk/id/eprint/10192942/">PhD thesis</a>.

An open source R package, <a href="https://github.com/lbuk/fmap">fmap</a>, has been created to produce Fresnel Maps and is available on Github. 

```
library(fmap)
library(sf)
library(dplyr)

# Load the sf datasets of cholera deaths and Soho pumps
data(cholera_deaths, soho_pumps)

# Filter the Broad Street Pump from the Soho pumps dataset
bstreet_pump <- soho_pumps %>% filter(soho.pump == "Broad Street")

# Visualise the Fresnel Map
fmap_plot(radius_inner = 125, ncircles = 8, geo_centre = bstreet_pump, geo_points = cholera_deaths, sum = "cholera.deaths")
```

<div class="col">
	<img class="col" src="{{ site.baseurl }}/img/example_fmap.png" alt="" title=""/>
</div>

<div class="col three caption">
	An example of the Fresnel Map. fmap has been used to aggregate and map cholera deaths around the Broad Street Pump in Soho using digitised data from John Snow's seminal study. Each concentric circular zone (or annuli) is equal in area. Data Source: <a href="https://blog.rtwilson.com/john-snows-famous-cholera-analysis-data-in-modern-gis-formats/">Robin Wilson's Blog</a>.
</div>
