---
layout: post
title: Subdivision Data
description: A data structure for recording building subdivision by floor
permalink: portfolio/SubdivisionData/
img: /img/numbers.png
---

Planning data is mostly unstructured, messy and two-dimensional. The creation of structured, machine-readable data on building subdivision is a challenge for urban practitioners.

A solution to this problem is to record subdivision using a simple and machine-readable data structure that consists of a list of numbers. Each number represents the floor of a building. The encoding of the numbers illustrates whether subdivision has occurred on a floor or alternatively the number of homes added or subtracted.

This new technique could be utilised by planners and designers to provide structured data on building subdivision. The data can be added to spreadsheets, for instance, as a new variable to describe subdivision by floor. Inspired by the work of Steadman, Martin and March in field of architectural design, the technique could be deployed to provide data on housing density.

<div class="col">
	<img class="col" src="{{ site.baseurl }}/img/subdivision_vectors.png" alt="" title=""/>
</div>

<div class="col three caption">
	Using binary encoding to record subdivision by floor from lowest on the left to highest on the right. An encoding of zero means that no subdivision has taken place on that floor. A one indicates that the floor has been subdivided. Here, subdivision has occurred on the third and sixth floors. It would be encoded in a dataset simply as 001001.
</div>

<br>

<div class="col">
	<img class="col" src="{{ site.baseurl }}/img/subdivision_vectors_homes.png" alt="" title=""/>
</div>

<div class="col three caption">
	Each floor is encoded with the number of homes added or removed due to subdivision or new extensions. This diagram illustrates that zero homes have been added on the first floor and eight homes have been added on the top floor.</div>
