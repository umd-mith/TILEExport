TILE Export Plugin
-----------------

Author: Grant Dickie  
MITH, 2011

exportJSONXML.js is code taken from the web to transform a generic JSON object into XML. 

Requires:  
TILE Source (tile1.0.js)  
jQuery  

Installing
===
I. For this version:  
Make sure to include the necessary header files (Note: we are using the default style for TILE in style.css):

	<!-- CSS styles -->
	<link rel="stylesheet" href="style.css" type="text/css" media="screen, projection" charset="utf-8">
	<!-- Necessary JS files -->
	<script type="text/javascript" language="javascript" src="jquery-1.4.2.min.js"></script>
	<script type="text/javascript" language="javascript" src="tile1.0.js"></script>
	<script type="text/javascript" language="javascript" src="export1.0.js"></script>
	<script type="text/javascript" language="javascript" src="exportJSONXML.js"></script>


API
===
export1.0.js is a wrapper for TILE. It includes a start() and loadJSON() functions, which are standard for TILE plugin wrappers. 

start(engine {Object})  
Sets up the necessary elements and function calls. Gets passed engine by default, which is the public 
version of the TILE source code. (See TILE_ENGINE API for more details)

loadJSON()
Not used 

transformTEI(xml {String})
Takes passed XML string and parses it into TEI. Returns string representing TEI-formatted XML.

useScript(file {String})

