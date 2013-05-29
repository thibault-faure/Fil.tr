Fil.tr
======

**Index**
----
* **[Syntax](#syntax)**
	* [Main](#main) 
	* [Environment](#environment) 
	* [Filter](#filter)
	* [Data](#data)
* **[Filters](#filters)**
	* [Lang Filter](#langFilter)
	* [Orientation Filter](#orientationFilter)
	* [OS Filter](#osFilter)
	* [Random Filter](#randomFilter)
	* [Retina Filter](#retinaFilter)
	


**[Syntax](id:syntax)**
----

###[Main](id:main)###

	<_Here is the description of the environment_>

	```javascript
  		{
  			"e" : [environment],
	  		"f" : [filters]
  		}    
	```
 
###[Environment](id:environment) `e`###

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
  
###[Filter](id:filter) `f`###

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
  			"default" : d,
  			"options" : {
  				"_optionKey_" : _optionValue_
  			}
  	  	}
	```
###[Data](id:data) `d`**

	<_Here is the description of the filter_>
	
	```javascript
  		"d" : {
  			"type" : _dataType_,
  			"content" : _dataContent_
  	  	}
	```
	
**[Filters](id:filters)**
----

###[Lang Filter](id:langFilter)###

	<_Here is the description of the filter_>

	```javascript
  		{
  			"type" : "LANG",
	  		"res" : [
	  			{
	  				"if" : "EN",
		  			"then" : d
	  			},
	  			{
	  				"if" : "FR",
	  				"then" : d,
	  			}
	  		],
	  		"default" : d,
  		}    
	```
	
	You can filter the following list of languages : 
	* English - "EN"
	* French - "FR"
	* Spanish - "ES"
	* Arabic - "AR"
	* Russian - "RU"
	* Chinese (Simplified) - "ZH"
	* Portuguese - "PT"
	* Japanese - "JA"
	* Hindi - "HI"
	* Greek - "EL"
		

###[Orientation Filter](id:orientationFilter)###

	<_Here is the description of the filter_>

	```javascript
  		{
  			"type" : "ORIENTATION",
	  		"res" : [
	  			{
	  				"if" : "portrait",
		  			"then" : d
	  			},
	  			{
	  				"if" : "landscape",
	  				"then" : d,
	  			}
	  		],
	  		"default" : d,
	  		"options" : {
				"mobileOnly" : Bool
	  		}
  		}    
	```
	
###[OS Filter](id:osFilter)###

	<_Here is the description of the filter_>

	```javascript
  		{
  			"type" : "OS",
	  		"res" : [
	  			{
	  				"if" : "iOS",
		  			"then" : d
	  			},
	  			{
	  				"if" : "android",
	  				"then" : d,
	  			}
	  		],
	  		"default" : d,
  		}    
	```
	
	You can filter the following list of OS : 
	* "iOS"
	* "Android"
	* "Windows Phone"
	* "BlackBerry"
	* "Mac Os X"
	* "Windows"


###[Random Filter](id:randomFilter)###

	<_Here is the description of the filter_>

	```javascript
  		{
  			"type" : "RANDOM",
	  		"res" : [
	  			{
	  				"if" : "80",
		  			"then" : d
	  			},
	  			{
	  				"if" : "10",
	  				"then" : d,
	  			}
	  		],
	  		"default" : d
  		}    
	```

###[Retina Filter](id:retinaFilter)###

	<_Here is the description of the filter_>

	```javascript
  		{
  			"type" : "RETINA",
	  		"res" : [
	  			{
	  				"if" : true,
		  			"then" : d
	  			},
	  			{
	  				"if" : false,
	  				"then" : d,
	  			}
	  		]
  		}    
	```
	
 
