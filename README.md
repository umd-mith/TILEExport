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
I. For including into TILE source:  
Make sure to include the necessary header files for TILE, which are for jQuery, the jQuery UI, the jQuery UI ColorPicker plugin, and the TILE 1.0 source:

	<!-- CSS styles -->
	<link rel="stylesheet" href="style.css" type="text/css" media="screen, projection" charset="utf-8">
	<!-- Necessary JS files -->
	<script type="text/javascript" language="javascript" src="jquery-1.4.2.min.js"></script>
	<script type="text/javascript" language="javascript" src="tile1.0.js"></script>
	

After adding all of the necessary files into the header, make sure to include 

	<script type="text/javascript" language="javascript" src="export1.0.js"></script>
	<script type="text/javascript" language="javascript" src="exportJSONXML.js"></script>
	
After adding the necessary files, you will need to insert the Export dialog plugin into the instance of TILE that you are instantiating somewhere in the HTML body or in another script area in the header. Inside export1.0.js, there is a TILE wrapper called *ExportTile*. The API for this wrapper is listed in the *API* section of this readme. You need to somehow insert this wrapper into TILE and we do this by adding *ExportTile* to the TILE_ENGINE constructor in the *toolSet* array, as shown here:

	<script type="text/javascript">
		// Insert the plugin into the TILE_ENGINE toolSet parameter
		var engine=new TILE_ENGINE({toolSet:[ExportTile]});
	
	</script>
	
API
===
_export1.0.js_ is a wrapper for TILE. It includes a start() and loadJSON() functions, which are standard for TILE plugin wrappers. 

*start*(engine {Object})  
Sets up the necessary elements and function calls. Gets passed engine by default, which is the public 
version of the TILE source code. (See TILE_ENGINE API for more details)

*loadJSON*()
Not used 

*transformTEI*(xml {String})
Takes passed XML string and parses it into TEI. Returns string representing TEI-formatted XML.

*useScript*(file {String})

