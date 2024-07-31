---
layout: post
title: elevate
description: An R package for creating charts of building elevations using permutations
permalink: portfolio/Elevate/
img: /img/zoom_datavis_example_extension_elevations_elevate_ii.png
---

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
