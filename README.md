# Campus Map
This is a full-stack project I built when I was taking Software Design and Implementation class. <br/>
This application is host on DigitalOcean under my domin name: <a href="http://www.jinghua.website/map" target="_blank">www.jinghua.website/map</a>

## Features:
- **Shortest Path**: <br>
  When user selects two buildings, server-side will run A* search on the graph model and return the shortest path back to client-side.
- **Auto-complete**:<br>
    When user click on a input box, a list of suggested locations will be displayed(currently
    the full list of buildings, but can be optimized using recommendation algorithm).
    When user starts typing, client side will send the input string back to the
    server and server will send back a list of matched buildings.
- **Turn-by-turn Navigation**:<br>
    When a path is returned from the server, client side will display a turn-by-turn navigation
    which indicates the how to get from one vertex to the next vertex on the campus map.
- **Zoomable**：<br>
    User can zoom in and zoom out to the center of the current view port by using the zoom
    buttons or scrolling.
- **Zoom to Path**: <br>
    When start and end are selected, map will display the path and zoom in to the path and a
    turn-by-turn navigation will be displayed on the sidebar.
- **Draggable**: <br>
    User can drag the map to relocate the center of the map.
- **Find Nearest Building**: <br>
    When user double click a point on the map, the application can find the nearest building
    on the map using KD-Tree.

## Client-side
- Front-end is bulit with React and Ant Design UI library for development efficiency
- I implemented the drag-and-drop feature with Canvas and x/y offset since I couldn't find elegant library that can handle the job.

# Server-side
- With Java Spark, I implemented the MVC design pattern for better modularity and less coupling
- The main techincal difficulty is to build all the low-level models and data structures, such priority queue, balanced tree, and genetic graph, from strach. A lot of 
 software engineering strategies was used to ensure correctness,
including test-driven porgramming, unit test, integration test, representation invariance, abstract function, proof, as well as detail documentation.  

# Hosting
- Host on DigitalOcean with Nginx as reverse proxy
