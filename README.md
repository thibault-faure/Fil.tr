Fil.tr
======
**Syntax**
----

* **Main data:**

	```javascript
  		{
  			"e" : [environment],
	  		"f" : [filters]
  		}    
	```
 
* **Environment `e`**

	<_Here is the description of the environment_>
	
	```javascript
  		"e" : {
  			"global" : {
  				"datetime":"2013-05-28T14:07:13.877Z",
				"referrer": "http://google.com",
				"cookies": String,
				"dimensions":{
					"width":1280,
					"availWidth":1280,
					"height":800,
					"availHeight":708
				},
  			},
  			"geolocation" : {
  				"available" : Bool,
  				"position" : {
  					"timestamp":1369750038552,
					"coords":{
						"speed":null,
						"heading":null,
						"altitudeAccuracy":null,
						"accuracy":37,
						"altitude":null,
						"longitude":1.3855798,
						"latitude":43.565891199999996
  				},
  				"error" : {}
  			},
  			"features" : {
  				"audio" : Bool,
  				"dragAndDrop" : Bool,
  				"fileApi" : Bool,
  				"localStorage" : Bool,
  				"retina" : Bool,
  				"sessionStorage" : Bool,
  				"undo" : Bool,
  				"video" : Bool
  			}
	  	}
	```
  
* **Filter `f`**

	<_Here is the description of the filter_>
	
	```javascript
  		"f" : {
  			"name" : _filterName_
  			"res" : [
  				{
  					"if" : _conditionValue_,
  					"then" : d
  				}
  			],
  			default : d,
  			options : {
  				"_optionKey_" : _optionValue_
  			}
  	  	}
	```
* **Data `d`**

	<_Here is the description of the filter_>
	
	```javascript
  		"d" : {
  			"type" : _dataType_,
  			"content" : _dataContent_
  	  	}
	```
