## Route Planner Project

### Project Objective
Plot a path between two points using **open street map**.

### OpenStreetMap
[OpenStreetMap](https://www.openstreetmap.org/#map=6/26.805/30.246).

The OpenStreetMap project is an open-source, collaborative endeavor to create free, user-generated maps of every part of the world. These maps are similar to the maps in Google Maps or the Apple Maps app, but they are completely generated by individuals who volunteer to perform ground surveys of their local environment.

### OpenStreetMap Data

OpenStreetMap data can come in several different formats. The data that is used for this project comes in the form of an OSM XML file (.osm file), [OpenStreetMap Wiki](https://wiki.openstreetmap.org/wiki/Main_Page). 


### Data Types Overview
There are three element types which are used in this project **Nodes, Ways, and Relations.**

**<u>Node</u>**
A [node](https://wiki.openstreetmap.org/wiki/Node) is one of the most basic elements in the OpenStreetMap data model. Each node indicates a single point with an **identifier id**, **latitude lat**, and **longitude lon**. There are other XML attributes in a node element that won't be relevant to this project, such as the user id and the timestamp when the node was added to the data set. Additionally, a node can have several **tags** which provide additional information.

**<u>Way</u>**
A [way](https://wiki.openstreetmap.org/wiki/Way) is an ordered list of nodes that represents a feature in the map. This feature could be a road, or a boundary of a park, or some other feature in the map. Each way has at least one **tag** which denotes some information about the way, and each way also belongs to at least one **relation**.

**<u>Relation</u>**
A [relation](https://wiki.openstreetmap.org/wiki/Relation) is a data structure which documents a relationship between other data elements. Examples from the **OpenStreetMap wiki** include:

`A route relation which lists the ways that form a major highway, cycle route, or bus route.`

`A multipolygon that describes an area with holes, where the outer and inner boundaries of the area are given by two ways.`

**Example**
Consider the following example from the [OpenStreetMap wiki](https://wiki.openstreetmap.org/wiki/Tag:waterway%3Driverbank) of mapping a large river with distinct banks on either side of the river. In the image below, nodes are used to provide the coordinates of points along the banks of the river. Multiple nodes are then connected using ways; there are ways which form closed sections of the river, labeled as "Areas" in the image below. Another way is used to represent the island in the middle of the river. These ways are then grouped together using a relation, which represents the entire river.
![alt text](image.png)

---

**Disclamier**
Both the code to parse the OSM data and the data structures which are used to store the data in This project is used from [IO2D OpenStreetMap example](https://github.com/cpp-io2d/P0267_RefImpl/tree/master/P0267_RefImpl/Samples/maps).