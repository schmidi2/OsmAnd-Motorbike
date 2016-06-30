# OsmAnd-Motorbike
OsmAnd customizations for Motorbike use.

* Optimized for the Panasonic Toughpad JT-B1.
* Should work on all Android devices with GPS.
* Does not work on iOS currently.
* This repo shall be a pull request to the original OsmAnd project one day.


**_This software is currently in alpha state and therefore cannot yust be installed and used. Help and ideas are welcome._**



## Repository Layout

**rendering/Motorbike.render.xml**
* OsmAnd Map Rendering Theme optimized for touring view.
* Onroad / Offroad mode view.
* High contrast colors. 
* Only relevant elements are displayed.
* Interesting roads have a highlighted color.
* Dead-end roads are 
* Not useful in cities.


**routing/Motorbike.routing.xml**
* Routing profile for Motorbike.
* Option "Find the most exciting winding roads".
* Penalties for uninteresting roads like straight roads or roads with a very low speed limit. 
  Dont penalty motorways in general, because a straight motorways is still better than a straight primary road.
* When a calculated route is left, recalculate without forcing to turn and without "turning" over a service road. 
* POIs?


**Conversion script for OSM files**
* Tag all roads with dead-end by foot, offroad and onroad.
* Insert tag with meters until dead-end?
* Convert non-dead-end roads (of type highway=service|residential|road) to unclassified roads, 
  but only if they don't have a low speed limit like 30km/h.
  These roads are important and shall be better visible on the map.
* Convert dead-end roads shorter than 1km to service roads.
  These roads are less important and must not be highlighted on the map.
  Exception: The roads end to an interesting POI like a view point.
* Tag interesting roads and apply a scala: 0-9
  Penalties for uninteresting roads like straight roads or roads with a very low speed limit. 
  Dont penalty motorways in general, because a straight motorways is still better than a straight primary road.
  Penalties for footcrossing, roads near shops/malls, road in citiy/village areas

 
**OsmAndMapCreator configuration file**
* Add/Remove tags for the OsmAnd File *.odf
* Make a lite, Motorcylce optimized ODF for better rendering performance? 
  Remove addresses, houses, public transports, textes and pois, we dont need.


**plugins/Osmand-TouringPlugin/**
* Plugin called "Touring Routing".
* On the fly routing. Where you are heading on. Option: Time and route when you arrive at home.
* Permanent Routing compass: Show when  turn and which roads are 
* Route planer: Select start, end and arrive-time.
* Recalculate an alternate route. 
* Remember driven roads and exclude them from future routings.

Compass
```  
           N        Shows compass-direction where you currently heading on and on what road type you are. 
		   |
    S 1km  |        Possible road in 1km on right side, goes south (bgcolor:pink, motorway) 
           |
    W 300  |        Possible road in 300m on right side, goes west (bgcolor:red, interesting road)
           |
           | D 50   Possible road in 50m on left side, goes north (bgcolor:grey, its a death end)
```  


**Plugin "Interesting POIs"**
*  Predefined List of POIs, which are relevant to motorbikers. Others are not displayed.
*  E.g. race circuits, view points, mountain pass, etc.


**Plugin "Switch VIEW"**
Klick screen to change VIEW
 - Near View Zoom
 - Wide View Zoom
 - POI view
 - Travel Routing View Fullscreen



## Installation instructions

1.  Install Android
   (I recommend the Pay Version)
2.  Download Global Map
3.  Activate and configure Motorbike profile
   (Developer Mode)
4.  Install Rendering
5.  Install Routing


  
## Panasonic Toughpad JT-B1
On Motorbike my *Navigation Assistant* is a Panasonic Toughpad JT-B1. The sceen of this waterproof tablet is matted and has a good brightness to use in direct sunlight. And it runs Android so you can choose your apps and customize them the way you want. Sadly, this seems to be the only device matching my requirements at the moment.

A new Panasonic Toughpad is very expensive, but you will find some used devices on eBay and others.

If you know similar devices, please let me know.



## Links
* OsmAnd Homepage: http://gwww.osmand.net
* OsmAnd main Github: https://github.com/osmandapp/Osmand
