---
layout: post
title: Urban Permutations
description: Software for exploring and visualising building densities using permutations
permalink: portfolio/UrbanPermutations/
img: /img/zoom_datavis_example_extension_elevations_elevate_ii.png
---

Permutations can be used to explore building elevations and densities. I developed two software packages - equiparate and elevate - to explore and visualise different urban scenarios. 

elevate is an R package for visualising building elevations using permutations and bar charts. It creates small multiple bar charts that depict the abstracted building elevations and prints the number of potential combinations in the console. elevate can be installed via <a href="https://github.com/lbuk/elevate">Github</a>.

```
library(elevate)

# Vector of storeys per building
storeys = c(4, 3, 5, 4)

# Visualise potential elevations based on maximum number of storeys per extension
extension_elevations(storeys = storeys, max_permitted_extstorey = 2, output = 'plot')
```

<div class="col">
	<img class="col" src="{{ site.baseurl }}/img/datavis_example_extension_elevations_elevate.png" alt="" title=""/>
</div>

<div class="col three caption">
	Visualising potential rooftop extension elevations using elevate and the maximum number of storeys per rooftop extension.
</div>

equiparate is an R package for comparing the density of buildings and spaces. It can also be utilised to compare the adaptability of built space. Building on the work of Martin and March and Terzidis, it utilises permutations and abstracts space using heatmaps. It can be installed via <a href="https://github.com/lbuk/equiparate">Github</a>.

```
library(equiparate)

# Visualise heatmaps with an equal number of units
equal_units(nrow = 4, ncol = 3, units = 4)
```

<div class="col">
	<img class="col" src="{{ site.baseurl }}/img/equiparate_equal_units_nrow4_ncol3_units4.png" alt="" title=""/>
</div>

<div class="col three caption">
	Floorplans with an equal number of units using equiparate.
</div>
