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
