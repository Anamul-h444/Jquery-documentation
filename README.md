# Jquery documentaion
#### What is Jquery
<p>jQuery is a lightweight, "write less, do more", JavaScript library.

The purpose of jQuery is to make it much easier to use JavaScript on your website.

jQuery takes a lot of common tasks that require many lines of JavaScript code to accomplish, and wraps them into methods that you can call with a single line of code.

jQuery also simplifies a lot of the complicated things from JavaScript, like AJAX calls and DOM manipulation.

The jQuery library contains the following features:

- HTML/DOM manipulation
- CSS manipulation
- HTML event methods
- Effects and animations
- AJAX
- Utilities </p>

#### Adding Jquery in Html Project
Link: https://jquery.com/download/  
-> Go to Goolgel CDN  
-> Go to Jquery  
-> Copy 3. X snippet for leatest CDN.  
CDN: (Before Js File use CDN for Use Jquery)   
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>  

#### Jquery basic syntax  
`$(selector).actionName(access timing here)`  
-> $  -> Determine Jquery  
Example:  $(this).hide(2000) - hides the current element with 2000 mili seconds.  

#### The Document Ready Event
1. All Jquery method write into document ready event.  
2. This prevent execute Jquery before document to be ready.  
3. If you use this you will able to use CDN in head section. Otherwise use CDN under the body section before js folder.  

###### Syntax of document ready event:  
```js
$(document).ready(function(){
    //jquery method write here....
});

//Description: When document is ready you work with jquery method.

```

###### Short Syntax of document ready event:  
```js
$(function(){
    //jquery method write here....
});

//Description: When document is ready you work with jquery method.

```

#### Jquery selectors

<p>jQuery selectors allow you to select and manipulate HTML element(s).

jQuery selectors are used to "find" (or select) HTML elements based on their name, id, classes, types, attributes, values of attributes and much more (Element Selctor, id selector, class selector, attribuite selector etc). It's based on the existing CSS Selectors, and in addition, it has some own custom selectors.

All selectors in jQuery start with the dollar sign and parentheses: $(). </p>


#### Jquery Event
##### Syntax:
```js
$(selector).eventMethod(function(){
    // action goes here....
})
```
##### Example:
```js
$(document).ready(function(){
  $("p").click(function(){
    $(this).hide();
  });

  $("#p1").hover(function(){
    alert("You entered p1!");
});
```
The Common Events are:  
-> click        - By clicking triger function.  
-> dblclick      - By double clicking triger function.  
-> mouseenter    - when mouse enter trigger function.  
-> mouseleave    - when mouse leave triger function.  
-> hover         - By hover trigger function.  
-> focus         - By click input trigger function.  
-> blur          - Click input by not input data trigger function.   

##### The on() event method
By on() method you can write many event in one selector.

##### Example:
```js
$("p").on({
  mouseenter: function(){
    $(this).css("background-color", "lightgray");
  },
  mouseleave: function(){
    $(this).css("background-color", "lightblue");
  },
  click: function(){
    $(this).css("background-color", "yellow");
  }
});
```

#### Jquery Effects
-> hide(speed, callback)    
-> show(speed, callback)   
-> toggle (speed, callback) -> toggle means by click hide/show.    
-> fadeIn(speed, callback)  
-> fadeOut(speed, callback)  
-> fadeToggle(speed, callback)  
-> fadeTo(speed, callback)  -> The jQuery fadeTo() method allows fading to a given opacity (value between 0 and 1).  
-> slideDown(speed, callback)  
-> slideUp(speed, callback)  
-> slideToggle(speed, callback)  

#### Jquery Callback effect
A callback function is executed after the current effect is finished.  
Typical syntax: $(selector).hide(speed,callback);  

##### Example:
```js
$("button").click(function(){
  $("p").hide("slow", function(){
    alert("The paragraph is now hidden");
  });
});
```
#### Jquery Chaining effect
Chaining allows us to run multiple jQuery methods (on the same element) within a single statement.    

##### Example:
```js
$("button").click(function(){
  $("#p1").css("color", "red").slideUp(2000).slideDown(2000);
});

// Description: when page load 1. change selector color 2. slide up 3. slide down.
```

#### Jquery HTML
##### Set content
-> text() - Replace text.  
-> html() - Replace text with executiin html code.  
-> val() - Replace of form or any other.  

##### Example:
```js
text replace:  
$("h1").text("I am changing by text method");
$(".my-div").text("Hello change by class");

text replace with many selector:  
$(".my-div, h1").text("Change by many selector");

text replace with use html code:  
$(".my-div").html("<b>I am change tex and use html code by html method</b>");

text add after tag:  
$("h1").append("I am add after h1");

text add before tag:  
$("h1").prepend("I am add before h1");

create paragraph and add after tag:  
var createparagraph=$("<p></p>").text("I am create paragraph and add after html p tag");
//$("p").after(createparagraph);

create paragraph and add before tag:  
var createparagraph=$("<p></p>").text("I am create paragraph and add before html p tag");
$("p").before(createparagraph);

Change value from input fiele by val():
<input type="text" id="test3" value="Mickey Mouse">
$("#btn3").click(function(){
    $("#test3").val("Dolly Duck");
  });
```

##### Jquery Remove
-> remove() - Removes the selected element (and its child elements)    
-> empty() -  Removes the child elements from the selected element  

##### Jquery Css Classes
-> addClass     - Adds one or more classes to the selected elements.  
-> removeClass() - Removes one or more classes from the selected elements.  
-> toggleClass() - Toggles between adding/removing classes from the selected elements. 
css()            - css() - Sets or returns the style attribute.  

###### Css() method explain:
The css() method sets or returns one or more style properties for the selected elements.  
Syntax:  
css({"propertyname":"value","propertyname":"value",...});  
Note: Must use cotation in property and value.

##### Example:
`$("p").css({"background-color": "yellow", "font-size": "200%"});`

#### Jquery animate() mathod Link:  
https://www.w3schools.com/jquery/jquery_animate.asp