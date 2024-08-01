# Overview

This chapter provides an overview of the four main pages of the [Urban Analyst
platform](https://urbananalyst.city):

- The [summarise page](https://urbananalyst.city/summarise) provides summary
  overviews for each city of key statistical properties and relationships with
  other cities;
- The [compare page](https://urbananalyst.city/compare) compares aggregate
  statistics for all cities;
- The [map page](https://urbananalyst.city/maps) shows interactive maps for
  each city;
- The [transform page](https://urbananalyst.city/transform) shows the effect of
  transforming any chosen city to become more like other cities.

The best place to start is the [Summarise
page](https://urbananalyst.city/summarise). The summary for any chosen city
will indicate which properties of the other pages are most important. Each of
the latter three pages also includes a pop-up "guided tour" explaining the key
features. These tours will automatically start the first time a page is opened,
or can be manually opened by clicking on the "Help" button on any of the main
pages.

----

## Summarise

The [Summarise page](https://urbananalyst.city/summarise) provides an overview
of the general statistical properties of any chosen UA city. Statistics for
each chosen city are compared with those for all other cities, and textual
summaries generated for all statistics which are significantly different.
Summaries are provided not just for individual statistics, but for the
strengths of relationship between all pairs of statistics.

The values described in this initial part of the [Summarise
page](https://urbananalyst.city/summarise) indicate which statistics might be
particularly worth examining in both the
[Compare](https://urbananalyst.city/compare) and the [Map
](https://urbananalyst.city/map) pages.

The [Summarise page](https://urbananalyst.city/summarise) also includes a
section describing the best "Target city" for each chosen city. As explained
there, the best target city is the city which is best in all the ways that the
chosen city is worse than average. This target city, and corresponding
variables described there, indicate which cities and variables might be
particularly worth examining in the [Transform
page](https://urbananalyst.city/transform).


----

## Compare

The [Compare page](https://urbananalyst.city/compare) enables comparisons
between all UA cities, both in terms of single variables and relationships
between any selected pair of variables. A pull-down panel enables each variable
or "layer" to be selected. The page then displays a graphical representation of
values of the chosen layer for all cities. As in all UA pages, lower values are
generally better than higher values. The control panel includes an "Explain
Layer" button which opens a text panel explaining details of the chosen
variable.

### Single and Paired Variables

The control panel of the [compare page](https://urbananalyst.city/compare)
includes an option to select "paired" variables. The resultant graphs then
display the strength of relationship between any chosen *pair* of variables.
For example, choosing social index and the nature index will display the
strength of relationship between access to natural spaces and social
disadvantage. Both of these variables are measured such that low values are
better than high values. A positive relationship between the two would then
mean that lower social disadvantage is coupled with better access to natural
spaces, while high social disadvantage is coupled with worse access to natural
spaces. Conversely, a negative relationship would indicate that higher social
disadvantage was coupled with better access to natural resources. Or, in the
words brought up by clicking the "Explain Layer" button, "Low values indicate
that good access to natural spaces is coupled with disadvantageous social
conditions."

----

## Map

The [Map page](https://urbananalyst.city/map) shows interactive maps for each
city, with values for all UA variables displayed in small polygons. These
polygons are defined by city-specific assessments of spatial disadvantage.
Berlin, for example, regularly measures a compound index of social disadvantage
aggregated into XX polygons. The map for Berlin uses these polygons provided by
the city to aggregate all measured variables. The variables are described in a
[subsequent chapter](./variables.md).

Details of the polygons for each city can be seen by selecting the "Social"
layer in the Map page and then clicking on the "Explain Layer" button.

As in all UA measurements, lower values of all variables are generally better
than higher values. Colour scales on all maps thus generally display lower
values in brighter, yellow colours, while higher values are displayed in
darker, blue or violet colours. The control panel includes an "Explain Layer"
button which opens a text panel explaining details of the chosen variable.

----

## Transform

The [Transform page](https://urbananalyst.city/transform) enables the
properties of any chosen city to be transformed to reflect equivalent
properties of some chosen "target" city. This page is best explained by an
example. Looking at the [Compare page](https://urbananalyst.city/compare) for
the "bike index" shows that Berlin has relatively poor bicycle infrastructure,
while Paris is a very good city for cyclists. The
[Transform page](https://urbananalyst.city/transform) can be used to visualise
how Berlin could best transform its current bicycle infrastructure to have an
overall distribution across the whole city equivalent to Paris. Conversely,
Paris has poorer access to natural spaces than Berlin, and the page could also
be used to examine how Paris could best transform its access to natural spaces
so that it functioned more like Berlin.

Urban Analyst values displayed in the [Map page](https://urbananalyst.city/map)
are aggregated from generally hundreds of thousands of individual calculations
at every street junction in each city. For the chosen variable, subsets of
these individual data points are sampled from each city, and the statistical
distribution for the chosen city is then transformed by changing each point by
the smallest amount possible so that they reflect the distribution in the
target city. These values are then aggregated into the polygons defined for the
city, to produce a visual representation of the least-cost transformation that
would be necessary for the city to have the same distribution as that of the
target city. The transformation algorithm is described in detail in the final
[*Software and Algorithms* chapter](./software.md).

### Extra Layers

The [Transform page](https://urbananalyst.city/transform) includes an
additional button labelled *Extra Layers*. The transformations described above
described transforming single layers or variables. The *Extra Layers* panel
enables transformations not just of single chosen variables, but also of their
relationships with other variables. Examining the [Compare
page](https://urbananalyst.city/compare), for example, shows that not only does
Paris provide poorer access to natural spaces than Berlin, but also that Berlin
has a better relationship between access to natural spaces and social
disadvantage. (This can be seen by clicking on the "*Paired*" layer option and
selecting those two layers.) The *Extra Layers* panel can be used in this case
to examine not just how Paris might best transform its access to nature to look
more like Berlin, but also how it might also improve its relationship between
access to nature and social disadvantage.

By default, values of *Extra Layers* are automatically selected as those which
have better relationships in the chosen target city. These default values will
thus change for each choice of target city and focal layer. It may be necessary
to click on the "Reset" button in the *Extra Layers* panel to update this
default selection after changing any of these options.

### Output Layer

Finally, the [Transform page](https://urbananalyst.city/transform) also has an
*Output Layer* option at the bottom of the control panel. This enables results
of the transformation algorithm to be displayed in one of four ways:

1. *Original* to show original values, prior to transformation;
2. *Transformed* to show the actual transformed values;
3. *Absolute* to show the absolute value by which each are in the city would
   have to be transformed to match the distribution in the target city; and
4. *Relative*, which displays the absolute transformation values relative to
   the original, untransformed values.
