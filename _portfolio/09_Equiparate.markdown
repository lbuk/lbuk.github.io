---
layout: post
title: equiparate
description: An R package for comparing the density of buildings and spaces
permalink: portfolio/Equiparate/
img: /img/equiparate_equal_units_nrow4_ncol3_units4_ii.png
---

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
