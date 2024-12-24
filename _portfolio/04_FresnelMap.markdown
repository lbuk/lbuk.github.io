---
layout: post
title: Fresnel Map
description: A new equal-area thematic mapping technique
permalink: portfolio/FresnelMap/
img: /img/zoom_fresnel_map_portfolio.png
---

The Codex Atlanticus 221v-b depicts a diagram with a set of consecutive circles. Each crescent has the same area as the central circle. Utilised by the likes of Fresnel and March, this geometric technique has been applied in various fields including architecture and civil engineering.

Here, Fresnel's circles have been utilised as part of a novel mapping technique. This technique, created in early 2020, is well-suited to addressing the Modifiable Areal Unit Problem (MAUP), in which geographic data is aggregated to administrative areas such as boroughs that may be unequal in terms of area. An open source R package, <a href="https://github.com/lbuk/fmap">fmap</a>, has been created to produce Fresnel Maps.

The Fresnel Map has been centred on Bromley by Bow in London. The concentric circular zones have been mapped thematically using an illustrative dataset. Each 'doughnut' (or annuli) has the same area as the central circle. The points-based data has been aggregated and thematically mapped to each equal-area zone.

<br>

<div class="col">
	<img class="col" src="{{ site.baseurl }}/img/bromley_by_bow_fresnel_map.jpeg" alt="" title=""/>
</div>

<div class="col three caption">
	The Fresnel Map.
</div>

fmap is an R package for creating Fresnel Maps, or thematic maps with equal-area concentric circular zones (or annuli). The Fresnel Map is a new mapping technique that could be utilised as an alternative way of addressing the Modifiable Areal Unit Problem's scale effect. fmap can be installed via <a href="https://github.com/lbuk/fmap">Github</a>.

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
	Using fmap to aggregate and map cholera deaths around the Broad Street Pump in Soho using digitised data from John Snow's seminal study. Each concentric circular zone (or annuli) is equal in area. Data Source: <a href="https://blog.rtwilson.com/john-snows-famous-cholera-analysis-data-in-modern-gis-formats/">Robin Wilson's Blog</a>.
</div>
