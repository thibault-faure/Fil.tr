Fil.tr
======

##Index##

* **[Syntax](#syntax)**
	* [Filter API](#filter-api) 
	* [Environment](#environment-e) 
	* [Filter](#filter-f)
	* [Data](#data-d)
* **[Filters](#filters)**
	* [Country Filter](#country-filter)
	* [Device Filter](#device-filter)
	* [Lang Filter](#lang-filter)
	* [Orientation Filter](#orientation-filter)
	* [OS Filter](#os-filter)
	* [Random Filter](#random-filter)
	* [Retina Filter](#retina-filter)
	* [Time Filter](#time-filter)
	* [Weekdays Filter](#weekdays-filter)
	* [Stat Filter](#stat-filter)
	


##Syntax##


###Filter API###
 
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
			"timezoneOffser":"-120",
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

###Country Filter###

<_Here is the description of the filter_>

```javascript
  	{
  		"name" : "COUNTRY",
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
	
You can filter all countries in the [ISO Country codes list](http://www.iso.org/iso/country_codes/iso_3166_code_lists/country_names_and_code_elements.htm).
 	
[_go on top_](#index)

###Device Filter###

<_Here is the description of the filter_>

```javascript
 	{
 		"name" : "DEVICE",
  		"res" : [
  			{
  				"if" : "mobile",
	  			"then" : d
  			},
  			{
  				"if" : "computer",
  				"then" : d,
  			}
  		],
  		"default" : d
 	}    
```
You can filter the following list of languages : 

	* "mobile"
	* "tablet"
	* "computer"
	
[_go on top_](#index)

###Lang Filter###

<_Here is the description of the filter_>

```javascript
  	{
  		"name" : "LANG",
		"res" : [
			{
	  			"if" : "US",
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
 		"name" : "ORIENTATION",
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
 			"name" : "OS",
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
 		"name" : "RANDOM",
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
  		"name" : "RETINA",
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

###Time Filter###

<_Filter a period of time_>

```javascript
 	{
 		"name" : "Time",
  		"res" : [
  			{
  				"if" : {
  								"from" : DATE,
  								"to" : DATE
  							},
	  			"then" : d
  			},
  		],
  		"default" : d, 
  		"options" : {
  			"time" : "server"
  		}
 	}    
```

<<<<<<< HEAD
Define intervals with "-". You can define intervals between Date, hours, seconds …

To define a start-date, use "YYY:MM:DD hh:mm:ss-".

To define an end-date, use "-YYY:MM:DD hh:mm:ss".
=======
Date must be defined using the following pattern : "YYYY:MM:DD hh:mm:ss".

You can omit any left-part of both dates in order to create smaller period.
>>>>>>> a5cc1536d47f43feda7e5b69f4e38f22a59d2f9d

Time option is available with these values:

	* "server" - The time and date reference is based on current time and date in UTC/GMT. This is the default option.
	* "local"  - The time and date reference is based on current time and date in the user time zone.
	* "UTC+\*" - The time and date reference is based on current time and date in UTC+\* zone _(from UTC-12 to UTC+14)_
	
[_go on top_](#index)

###Weekdays Filter###

<_Here is the description of the filter_>

```javascript
 	{
 		"name" : "WEEKDAY",
  		"res" : [
  			{
  				"if" : "1",
	  			"then" : d
  			},
  			{
  				"if" : "2/7",
  				"then" : d,
  			}
  			{
  				"if" : "3-5",
  				"then" : d,
  			}
  		],
  		"default" : d, 
  		"options" : {
  			"time" : "server"
  		}
 	}    
```

The weekday number, from 1 through 7, beginning with Monday and ending with Sunday.

Intervals with "-". _(eg. For "from Wednesday to Friday" use "3-5")_

Different weekdays for the same data with "/". _(eg. For "Tuesday AND Sunday" use "2/7")_

Time option is available with these values:

	* "server" - The time and date reference is based on current time and date in UTC/GMT. This is the default option.
	* "local"  - The time and date reference is based on current time and date in the user time zone.
	* "UTC+\*" - The time and date reference is based on current time and date in UTC+\* zone _(from UTC-12 to UTC+14)_
	
[_go on top_](#index)

###Stat Filter###

_The stat filter decision is made depending on the number of visits (or visitors) of this filter_

```javascript
 	{
 		"type" : "STAT",
  		"res" : [
  			{
  				"if" : "-1000",
	  			"then" : d
  			},
  			{
  				"if" : "1001-1999",
  				"then" : d,
  			}
  			{
  				"if" : "2000-",
  				"then" : d,
  			}
  		],
  		"default" : d, 
  		"options" : {
  			"stat" : "view"
  		}
 	}    
```

Define intervals with "-".

Define an "up-to" value starting with "-"

Define a "from" value ending with "-"

Stat option is available with these values:

	* "view"    - The decision is made depending on the number of visits (or visitors).
	* "visitor" - The decision is made depending on the number of visits (or visitors).


