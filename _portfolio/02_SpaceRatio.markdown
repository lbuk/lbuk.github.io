---
layout: post
title: Space Ratio and the Space Ratio Chart
description: Measuring and mapping urban density potentials
permalink: portfolio/SpaceRatio/
img: /img/space_ratio_chart_example_zoom.png
---

Space Ratio is a novel technique that describes the ratio of the existing density to the permissible density (Bolton, 2021). Space Ratio calculates density potentials: the lower the Space Ratio, the more room there is for residential extensions, for instance.

<div class="col">
	<img class="col" src="{{ site.baseurl }}/img/portfolio_space_ratio_formula.png" alt="" title=""/>
</div>

<div class="col three caption">
	Space Ratio formula.
</div>

<br>

The Space Ratio Chart is a technique for visualising Space Ratio that can also be customised using different scenarios and a range of measures denoting density potentials. 

<div class="col">
	<img class="col" src="{{ site.baseurl }}/img/space_ratio_chart.png" alt="" title=""/>
</div>

<div class="col three caption">
	An example of the Space Ratio Chart.
</div>

If utilised cautiously and contextually, Bolton (2021) states that Space Ratio could be deployed by planners and designers to compare density scenarios and facilitate sustainable densification. The journal article on Space Ratio and the Space Ratio Chart can be accessed via <a href="https://doi.org/10.1016/j.scs.2021.103356">Sustainable Cities and Society</a>.

<br>

**Publication**\
Bolton, L.T. (2021). 'Space ratio: a measure of density potentials in the built environment', _Sustainable Cities and Society_, 75, p.103356. doi: 10.1016/j.scs.2021.103356.

<br>

# spaceratio
Space Ratio Charts can be generated in R using the <a href="https://github.com/lbuk/spaceratio">spaceratio</a> package. Published in 2023, the R package can be installed via Github.

```
library(spaceratio)

# Density variables
d_var = c("FAR", "H", "DPH")

# Space Ratios
s_val = c(0.91, 0.83, 1)

# Space Ratio Chart
spaceratio(density_var = d_var, space_ratio = s_val, output = 'plot')
```

<div class="col">
	<img class="col" src="{{ site.baseurl }}/img/portfolio_spaceratio_example.png" alt="" title=""/>
</div>

<div class="col three caption">
	An example output of the spaceratio package showing the Space Ratio Chart.
</div>