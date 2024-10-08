Introduction
###############

`Urban Analyst (UA) <https://urbananalyst.city>`_ analyses the structure and
function of cities across the world. Each city can be viewed as an `interactive
map <https://urbananalyst.city/maps>`_ displaying several different properties
or variables. These include socio-demographic conditions and the structure and
function of transport systems. The platform also analyses relationships between
individual variables, such as between socio-demographic conditions and
frequency of transport services, or between distances to nearest schools and
access to natural spaces.

UA also provides `statistical comparisons <https://urbananalyst.city/compare>`_
between all cities, enabling comparisons across all UA cities of single
variables, as well as relationships between any pair of variables, such as
transport and socio-demographic disadvantage. 

Finally, UA enables cities to "learn" from one another, by visualising how the
properties of any chosen city can best be transformed to become more like the
properties of any other chosen city. Paris, for example, has better bicycle
infrastructure than Berlin, and the UA transformation algorithm can calculate
how Berlin can most easily transform its bicycle infrastructure to become more
like Paris. Values for every area in Berlin are then displayed as the
proportional increase in bicycle infrastructure which would be necessary for
the whole city to have infrastructure equivalent to Paris.

How does it work?
*****************

Urban Analyst presents a variety of :ref:`variables<UA Variables>` for each
city analysed, as well as relationships between these variables. Values for
each variable are derived at every street intersection in each city. These
values are then aggregated into the polygons shown in the |map-page-short| and
|transform-pages|, and across entire cities for the values shown in the
|comp-page|. Aggregations are always weighted by local population densities, so
that all UA values represent values *per person* as experienced in each city.
Details are provided in the |data-chapter-short| and |sw-chapters|.

.. |comp-page| raw:: html

   <a href="https://urbananalyst.city/compare">
   <em>Compare</em> page</a>

.. |map-page-short| raw:: html

   <a href="https://urbananalyst.city/map">
   <em>Map</em></a>

.. |transform-pages| raw:: html

   <a href="https://urbananalyst.city/transform">
   <em>Transform</em> pages</a>

.. |data-chapter-short| raw:: html

   <a href="https://docs.urbananalyst.city/content/data.html">
   <em>Data Sources</em></a>

.. |sw-chapters| raw:: html

   <a href="https://docs.urbananalyst.city/content/software.html">
   <em>Software and Algorithms</em> chapters</a>


How many calculations are involved?
***********************************

The values presented in Urban Analyst are derived from estimates of travel
times from every point in each city to every other point using any combination
of possible modes of transport. The following table summarises numbers of
street intersections, public transport ("PT") stops, and calculations for a
selection of Urban Analyst cities.

.. list-table:: Numbers of calculations
   :header-rows: 1

   * - | city
     - | intersections
       | (thousands)
     - | PT stops
     - | PT calcs
       | (millions)
     - | routing calcs
       | (millions)
   * - Berlin
     - 360
     - 9,302
     - 173
     - 150
   * - Hamburg
     - 192
     - 4,585
     - 42
     - 56
   * - London
     - 506
     - 20,072
     - 806
     - 160
   * - Paris
     - 313
     - 29,393
     - 1,728
     - 124


One way to appreciate the scale of these calculations is through comparison
with commercial alternatives. One service, *traveltime.com*, charges a flat
subscription fee of €540 per month for a maximum of 60 requests per minute.
That rate would permit 31.5 million queries per year. The city of Hamburg, for
example, would then take almost 2,000 years to calculate, and would cost
€12 million. Google also offers a commercial routing service, limited to a
maximum of 500,000 queries per month, for a total price of US$2,000. At that
rate, the analyses for Hamburg would cost US$224 million.

The results presented in Urban Analyst are simply not possible using commercial
tools, or indeed any other open source tools. These analyses truly are uniquely
powerful, and provide a depth of insight into how people move through cities
not available in any other way.


Can I access the full data?
***************************

Not directly, but feel free to open a `GitHub
issue <https://github.com/mpadge/UrbanAnalyst/issues>`_ to start a discussion
about requesting full data sources.
