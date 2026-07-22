---
layout: post
title: Fresnel Map
description: A new equal-area thematic mapping technique
permalink: portfolio/FresnelMap/
img: /img/zoom_fresnel_map_portfolio.png
---

The Fresnel Map is a novel equal-area thematic mapping technique in which data is aggregated and visualised to doughnut-shaped zones that have the same area as the central circle. 

Created in early 2020 during my doctoral research, it is inspired by Augustin-Jean Fresnel and Lionel March, who applied similar geometric techniques in architecture and civil engineering. The Codex Atlanticus 221v-b also depicts a diagram with a set of crescent-shaped zones that are equal in area.

An open source R package, <a href="https://github.com/lbuk/fmap">fmap</a>, has been created to produce Fresnel Maps and is available on Github. More information about this mapping technique can be found in my <a href="https://discovery.ucl.ac.uk/id/eprint/10192942/">PhD thesis</a>. 

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
	<img class="col" src="{{ site.baseurl }}/img/example_fresnel_map.png" alt="Fresnel Map of cholera deaths around the Broad Street Pump in Soho, using equal-area annuli to aggregate John Snow's data"/>
</div>

<div class="col three caption">
	An example of the Fresnel Map. fmap has been used to aggregate and map cholera deaths around the Broad Street Pump in Soho using digitised data from John Snow's seminal study. Data Source: <a href="https://blog.rtwilson.com/john-snows-famous-cholera-analysis-data-in-modern-gis-formats/">Robin Wilson's Blog</a>.
</div>

<b>Publications</b>
<br>
Bolton, L.T. (2024). <i>Cartographies of rooftop housing: techniques for mapping airspace development in London</i>. Ph. D Thesis. University College London. Available at: <a href="https://discovery.ucl.ac.uk/id/eprint/10192942/" style="background-color: transparent; color: #666; font-weight: 100;">https://discovery.ucl.ac.uk/id/eprint/10192942/</a> (Accessed: 28 June 2024). | <a href="https://discovery.ucl.ac.uk/id/eprint/10192942/">View Thesis</a>
