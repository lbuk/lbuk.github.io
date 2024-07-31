---
layout: post
title: fmap
description: An R package for creating Fresnel Maps
permalink: portfolio/Fmap/
img: /img/zoom_example_fmap.png
---

fmap is an R package for creating <a href="https://www.liamthomasbolton.com/portfolio/FresnelMap/">Fresnel Maps</a>, or thematic maps with equal-area concentric circular zones (or annuli). The Fresnel Map is a new mapping technique that could be utilised as an alternative way of addressing the Modifiable Areal Unit Problem's scale effect. fmap can be installed via <a href="https://github.com/lbuk/fmap">Github</a>.

```
library(fmap)

# Load the sf datasets of cholera deaths and Soho pumps
data(cholera_deaths, soho_pumps)

# Filter the Broad Street Pump from the Soho pumps dataset
bstreet_pump = soho_pumps %>% filter(soho.pump == "Broad Street")

# Visualise the Fresnel Map
fmap_plot(radius_inner = 125, ncircles = 8, geo_centre = bstreet_pump, geo_points = cholera_deaths, sum = "cholera.deaths")
```

<div class="col">
	<img class="col" src="{{ site.baseurl }}/img/example_fmap.png" alt="" title=""/>
</div>

<div class="col three caption">
	Using <a href="https://github.com/lbuk/fmap">fmap</a> to aggregate and map cholera deaths around the Broad Street Pump in Soho using digitised data from John Snow's seminal study. Each concentric circular zone (or annuli) is equal in area. Data Source: <a href="https://blog.rtwilson.com/john-snows-famous-cholera-analysis-data-in-modern-gis-formats/">Robin Wilson's Blog</a>.
</div>
