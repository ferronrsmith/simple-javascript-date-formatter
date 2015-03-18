a very simple implementation of a javascript data formatter

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!--

@author : Ferron Hanse
@date : 11/2/2011
@licence : Do no Evil!

-->

<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en">
<head>
	<script type="text/javascript" src="date.js"></script>
	<script type="text/javascript">
	
	
	//default
	console.log((new Date()).format('yyyy'));
	// returns 2011
	
	//standard
	console.log((new Date()).format('mmm dd yy hh:nn:ss a/p'));
	//returns Nov 02 11 11:23:16 am

	//short date
	console.log((new Date()).format('mm/dd/yy'));
	//returns 11/02/11
	
	//medium date
	console.log((new Date()).format('mmm dd, yyyy'));
	//returns Nov 02, 2011
	
	//medium date
	console.log((new Date()).format('mmmm dd, yyyy'));
	//returns November 02, 2011
	
	//full date
	console.log((new Date()).format('dddd, mmmm dd, yyyy'));
	//returns Wednesday, November 02, 2011
	
	//shortTime
	console.log((new Date()).format('hh:nn a/p'));
	//returns 11:23 am
	
	//mediumTime
	console.log((new Date()).format('hh:nn:ss a/p'));
	//returns 11:23:16 am
	
	//isoDate
	console.log((new Date()).format('yyyy-mm-dd'));
	//returns 2011-11-02
	
	// parse date in 2012/2/2 format
	console.log(("2012/2/2").parse('/').format('dddd, mmmm dd, yyyy'));
	
	// Year - Month - Day
	console.log(("2012-2-2").parse('-').format('dddd, mmmm dd, yyyy'));

	</script>
</head>
<body>
	
</body>
</html>
```