# Notes

## CSS

CSS'e bu girilecek:

```
#diskriptif {
  color: navy;
  font-size: 18px;
}
```
border yaratmak icin:
``` <style>
  .thin-red-border {
    border-color: red;
    border-width: 5px;
    border-style: solid;
  }
</style>
```
yan yana resim eklemek:

 ```<div class="row">
      <div class="col-sm-6">
    <img src="https://placeholdit.imgix.net/~text?txtsize=33&txt=350%C3%97150&w=350&h=150" alt="Newspaper website" id="cerceve">
      </div>
      <div class="col-sm-6">
        <img src="https://placeholdit.imgix.net/~text?txtsize=33&txt=350%C3%97150&w=350&h=150" alt="Magazine Website" id="cerceve">
      </div>
    </div>
    ```
## Javascript
  
Switch statement:
'''  
switch(val) {
        case 1:
        case 2:
        case 3:
          result = "1, 2, or 3";
          break;
        case 4:
          result = "4 alone";
          }
    ''''
##objects and array edition
    Write a function which takes an album's id (like 2548), a property prop (like "artist" or "tracks"), and a value (like "Addicted to Love") to modify the data in this collection.

If prop isn't "tracks" and value isn't empty (""), update or set the value for that record album's property.

Your function must always return the entire collection object.

There are several rules for handling incomplete data:

If prop is "tracks" but the album doesn't have a "tracks" property, create an empty array before adding the new value to the album's corresponding property.

If prop is "tracks" and value isn't empty (""), push the value onto the end of the album's existing tracks array.

If value is empty (""), delete the given prop property from the album.
Use bracket notation when accessing object properties with variables.

Push is an array method you can read about on Mozilla Developer Network.

You may refer back to Manipulating Complex Objects Introducing JavaScript Object Notation (JSON) for a refresher.
    
    var collection = {
    "2548": {
      "album": "Slippery When Wet",
      "artist": "Bon Jovi",
      "tracks": [ 
        "Let It Rock", 
        "You Give Love a Bad Name" 
      ]
    },
    "2468": {
      "album": "1999",
      "artist": "Prince",
      "tracks": [ 
        "1999", 
        "Little Red Corvette" 
      ]
    },
    "1245": {
      "artist": "Robert Palmer",
      "tracks": [ ]
    },
    "5439": {
      "album": "ABBA Gold"
    }
    };
    
    function updateRecords(id, prop, value) {
    if (prop!="tracks" && value!="")
    {
      collection[id][prop]=value;
    }
    else if (prop=="tracks" && collection[id].hasOwnProperty(prop)==0)
    {
      var erey=[];
      erey.push(value);
      collection[id][prop]=erey;
     
      
    }
    else if (prop == "tracks" && value!="") {
      collection[id].tracks.push(value);
    }
    else if ( value== "") {
      delete collection[id][prop];
      }
  
      return collection;
    }

##for loops yall:

// Setup
var myArray = [];

// Only change code below this line.
for (var i=1; i<6; i++) {
  myArray.push(i);
}

##nested for loops:

function multiplyAll(arr) {
  var product = 1;
  // Only change code below this line
  for (var i=0; i<arr.length; i++) {
    for (var j=0; j<arr[i].length; j++)
      {
        product= product*arr[i][j];
      }
  }
  // Only change code above this line
  return product;
}

// Modify values below to test your code
multiplyAll([[1,2],[3,4],[5,6,7]]);
