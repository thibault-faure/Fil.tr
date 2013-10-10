#QR Code API#

The QR Code API requests are based on this JSON :

	{
		data : {
			type : "",
			data : {}
		},
		setting : {}
	}

##Data object##

###"Type" - STRING###

* url
* text
* geoloc
* smsto
* wifi
* vcard
* email
* calendar
* call

###"data" - OBJECT###

**Type : url**

	data : {
		type : "url",
		data : {
			URL : ""
		}
	}

**Type : text**

	data : {
		type : "text",
		data : {
			TEXT : ""
		}
	}

**Type : geoloc**

	data : {
		type : "geoloc",
		data : {
			LAT : "",
			LONG : ""
		}
	}

**Type : smsto**

	data : {
		type : "smsto",
		data : {
			TEL : "",
			MESSAGE : ""
		}
	}

**Type : wifi**

	data : {
		type : "wifi",
		data : {
			TYPE : "WEP"/"WPA"/"nopass",
			NETWORK : "",
			PASSWORD : ""
		}
	}
	
**Type : vcard**

	data : {
		type : "vcard",
		data : {
			firstname : "",
			name : "",
			email;internet : "",
			email;home;internet : "",
			tel;cell : "",
			tel;work : "",
			tel;home : "",
			url : "",
			title : "",
			org : "",
			adr : "",
			pc : "",
			city : "",
			country : ""
		}
	}

**Type : email**

	data : {
		type : "email",
		data : {
			EMAIL : "",
			EMAIL_OBJ : "",
			EMAIL_CORPS : ""
		}
	}

**Type : calendar**

	data : {
		type : "calendar",
		data : {
			TITLE : "",
			LIEU : "",
			DATE_DEBUT : "",
			DATE_FIN : ""
		}
	}
	
**Type : call**

	data : {
		type : "call",
		data : {
			PHONE : ""
		}
	}


##Setting object##

	{
		LAYOUT : {},
		EYES : {},
		LOGO : {},
		BACKGROUND : {},
		E : "",
		BODY_TYPE : INT,
		ARRONDI : INT,
		QUIET_ZONE : BOOLEAN
	}
###LAYOUT - OBJECT###

	LAYOUT : {
		GRADIENT_TYPE : "",
		COLOR1 : "",
		COLOR2 : "",
		RAYON : INT,
		X1 : INT,
		Y1 : INT,
		X2 : INT,
		Y2 : INT,
		COLORBG : "",
		COLOR_SHADOW : "",
		X_SHADOW : INT,
		Y_SHADOW : INT,
		FORCE_SHADOW : ""
	}
	
**GRADIENT_TYPE - STRING**

* From up to down : "HORI"
* From left to right: "VERT"
* Diagonal top left to bottom right: "DIAG1"
* Diagonal bottom left to top right: "DIAG2"
* Radial outward from the center: "RADI"
* Linear without repeating the pattern, setting requires two distinct points of start and end: "LIN_ACY"
* Linear with pattern repeat, requires setting two distinct points of start and end: "LIN_CYC"
* Without repetition of the pattern ,requires setting a starting point and a radius: "RAD_ACY"
* With repetition of the pattern, requires setting a starting point and a radius x1: "RAD_CYC"

**COLORBG**

Can be transparent

**FORCE_SHADOW**

Strength of the shadowing.

_Note: FORCE_SHADOW is a shortcut for X_SHADOW/Y_SHADOW_

* "L" : Low (value is 5)
* "M" : Medium (value is 7)
* "S" : Strong (value is 10)


###EYES###

	EYES : {
		COLOR_EHG : "",
		COLOR_EHD : "",
		COLOR_EB : "",
		COLOR_IHG : "",
		COLOR_IHD : "",
		COLOR_IB : "",
		EYE_TYPE : ""
	}

**EYE_TYPE**

* Square: "Simple"
* Diamond: "Diamond"
* Roundness: "ER_IC"
* Roundess "ER_IR"
* True circle "ES_IC"
* Right circle "LLRight"
* Left eye: "LLLeft"
* Shield "Shield"
* Cushion "SFLeaves"
* Star "SFLeavesC"
* Leaf "Spike"
* Sieve: "Turned"
* Dots: "S_Circle"
* Wave "Wave"
* Sharp "Sharp"
* Curved "ECurve_ICurve"
	
###LOGO###
	
	LOGO : {
		L_NAME : "",
		L_X_Norm : FLOAT,
		L_Y_Norm : FLOAT,
		L_WIDTH : FLOAT,
		L_LENGTH : FLOAT,
		EXCAVATE : BOOLEAN
	}

**L_X_Norm & L_Y_Norm**

The upper corner of the logo in the QR Code as a percentage. Set to 2 to have it centered.


###BACKGROUND###

	LOGO : {
		IMAGE_BACKGROUND : "",
		ENLIGHTMENT : FLOAT,
		CONTRAST : FLOAT
	}

**ENLIGHTMENT & CONTRAST - float**

0 <= x <= 2	
		
###E - STRING###

QR Code redundancy : 

* Low : "L"
* Medium : "M"
* Quality : "Q"
* Strong : "H"

###BODY_TYPE - INT###

Modules look : 

* Square : 0
* Light roundness : 1 ("ARRONDI" required)
* Medium roundness : 1 ("ARRONDI" required)
* Strong roundness : 1 ("ARRONDI" required)
* Sieve : 2
* Angular : 3
* Painting : 4
* Dots : 5
* Arrow : 6
* Classy : 7
* Rectangular : 8


###ARRONDI - INT###

0 <= x <= 10
