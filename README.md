# OsmAnd-Motorbike
OsmAnd customizations for Motorbike use.
Optimized for the Panasonic Toughpad JT-B1.
Works on all Android deviceses where OsmAnd
Doenst work on iOS currently.

rendering/Motorbike.render.xml
  Map Rendering Theme optimized for touring view.
  High contrast colors. 
  Only relevant elements are displayed.
  Interessting roads have some nice colors
  It shall best show 


routing/Motorbike.routing.xml
  Penalties for uninteresting roads (straight roads, slow zones). 
    Dont penalty motorways, because a straight motorways is still better than a straight primary road.
  POIs?
  

Converting script for osm-file
  Tag all roads with deathend's by foot, offroad, onroad
  Convert non-deathend highway=service|road|residential to highway=unclassified, if they are not limited to 30km/h
  "Sackgasse zu service wenn kürzer als 500.sonst mit farblich markieren"
  "Service,road etc ohne sackgasse zu unclassified ausser wenn es 30,40er zonen sind."
  
  
OsmAndMapCreator configuration file
  Add/Remove tags for the OsmAnd File *.odf


plugins/Osmand-TouringPlugin/
Plugin "Touring Routing"
  On the fly routing. Where you are heading on. Option: Time and route when you arrive at home.
  Permanent Routing compass: Show when  turn and which roads are 
  
           N        Shows compass-direction where you currently heading on and on what road type you are. 
		   |
    S 1km  |        Possible road in 1km on right side, goes south (bgcolor:pink, motorway) 
           |
    W 300  |        Possible road in 300m on right side, goes west (bgcolor:red, interesting road)
           |
           | D 50   Possible road in 50m on left side, goes north (bgcolor:grey, its a death end)
  
  Route planer: Select start, end and arrive-time.

  
Plugin "Interesting POIs"
  Predefined List of POIs, which are relevant to motorbikers. Others are not displayed.
  E.g. race circuits, view points, mountain pass, etc.


Installation instructions

  Install Android
   (I recommend the Pay Version)
  Download Global Map
  Activate and configure Motorbike profile
   (Developer Mode)
  Install Rendering
  Install Routing

  
Recommendations for the Panasonic Toughpad JT-B1

  Disable / Enable
  
