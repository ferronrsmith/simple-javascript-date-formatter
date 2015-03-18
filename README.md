# simple-javascript-date-formatter

```javascript
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
```
