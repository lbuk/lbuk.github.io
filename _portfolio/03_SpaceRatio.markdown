---
layout: post
title: Space Ratio and the Space Ratio Chart
description: A novel measure of density potentials
permalink: portfolio/SpaceRatio/
img: /img/space_ratio_chart_example_zoom.png
---

Space Ratio is a novel technique that describes the ratio of the existing density to the permissible density (Bolton, 2021). Space Ratio calculates density potentials: the lower the Space Ratio, the more room there is for residential extensions, for instance. 

If utilised cautiously and contextually, Bolton (2024) states that Space Ratio could be deployed by planners and designers to compare density scenarios and facilitate sustainable densification. 

<div class="col">
	<img class="col" src="{{ site.baseurl }}/img/portfolio_space_ratio_formula.png" alt="Space Ratio formula showing the ratio of existing density to permissible density"/>
</div>

<div class="col three caption">
	Space Ratio formula.
</div>

<br>

The Space Ratio Chart is a technique for visualising Space Ratio that can also be customised using different scenarios and a range of measures denoting density potentials. 

<div class="col">
	<img class="col" src="{{ site.baseurl }}/img/space_ratio_chart.png" alt="Space Ratio Chart showing density variables FAR, H, DPH, GSI and PPH with corresponding Space Ratio values"/>
</div>

<div class="col three caption">
	An example of the Space Ratio Chart.
</div>

<br>

Space Ratio Charts can be generated in R using the <a href="https://github.com/lbuk/spaceratio">spaceratio</a> package on Github.

```
library(spaceratio)

# Density variables
d_var <- c("FAR", "H", "DPH")

# Space Ratios
s_val <- c(0.91, 0.83, 1)

# Visualise the Space Ratio Chart
spaceratio(density_var = d_var, space_ratio = s_val, output = 'plot')
```

<div class="col">
	<img class="col" src="{{ site.baseurl }}/img/portfolio_spaceratio_example.png" alt="Example output of the spaceratio R package showing a Space Ratio Chart"/>
</div>

<div class="col three caption">
	An example output of the spaceratio package showing the Space Ratio Chart.
</div>

The journal article on Space Ratio and the Space Ratio Chart can be accessed via <a href="https://doi.org/10.1016/j.scs.2021.103356">Sustainable Cities and Society</a>. More information can also be found in my <a href="https://discovery.ucl.ac.uk/id/eprint/10192942/">PhD thesis</a>.

<br>

<b>Publications</b>
<br>
Bolton, L.T. (2024). <i>Cartographies of rooftop housing: techniques for mapping airspace development in London</i>. Ph. D Thesis. University College London. Available at: <a href="https://discovery.ucl.ac.uk/id/eprint/10192942/" style="background-color: transparent; color: #666; font-weight: 100;">https://discovery.ucl.ac.uk/id/eprint/10192942/</a> (Accessed: 28 June 2024). | <a href="https://discovery.ucl.ac.uk/id/eprint/10192942/">View Thesis</a>
<br>
<br>
Bolton, L.T. (2021). 'Space ratio: a measure of density potentials in the built environment', <i>Sustainable Cities and Society</i>, 75, p.103356. doi: 10.1016/j.scs.2021.103356. | <a href="https://doi.org/10.1016/j.scs.2021.103356">View Article</a>
