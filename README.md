# The BIG-DATA project
Interactive map showing access to basic services: 
Objective: Show in an interactive map the number of different basic services per H3 unit (https://www.uber.com/en-ES/blog/h3/) for the cities of Pavia and Cagliari. 
kepler.gl-hexagon.png

Example of basic services:
Health: hospital, pharmacy, dentist, ...
Education: School, Kindergarten, University, library
Food: Supermarket, Market,...
Security: Police, fire fighters...
Public services: Post office, City council
Sports: Pool, gym, ...

Tentative Workflow: Download the data from openstreetmap, investigating which is the best way to do it (e.g GeoFabric, Overpass) and the services available, process it (e.g in Python + PySpark) to get the POIs and location and load it to Spark, group the data per H3 cell. Use elasticsearch to index/find per cell h3 the type of service (health, education) and represent it as a Kepler.gl map.
