Fil.tr
======

##Index##

* **[Syntax](#syntax)**
	* [Main](#main) 
	* [Environment](#environment-e) 
	* [Filter](#filter-f)
	* [Data](#data-d)
* **[Filters](#filters)**
	* [Lang Filter](#lang-filter)
	* [Orientation Filter](#orientation-filter)
	* [OS Filter](#os-filter)
	* [Random Filter](#random-filter)
	* [Retina Filter](#retina-filter)
	


##Syntax##


###Main###
 
<_Here is the description of the environment_>

```javascript
	{
		"e" : [environment],
  		"f" : [filters]
	}     		 
```

[_go on top_](#index)
 
###Environment `e`###

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
  				}
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

[_go on top_](#index)
  
###Filter `f`###

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

[_go on top_](#index)
	
###Data `d`###

<_Here is the description of the filter_>
	
```javascript
  	"d" : {
  		"type" : _dataType_,
  		"content" : _dataContent_
  	}
```

[_go on top_](#index)
	
##Filters##

###Lang Filter###

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
	
[_go on top_](#index)
	
###Orientation Filter###

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

[_go on top_](#index)
	
###OS Filter###

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

[_go on top_](#index)

###Random Filter###

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
	
[_go on top_](#index)

###Retina Filter###

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

[_go on top_](#index)
 

