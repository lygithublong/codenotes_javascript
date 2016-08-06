# display div while hide others onclick
Basic syntax is: $(selector).action()
   * A $ sign to define/access jQuery
   * A (selector) to "query (or find)" HTML elements
   * A jQuery action() to be performed on the element(s)
Examples:
* $(this).hide() - hides the current element.
* $("p").hide() - hides all <p> elements.
* $(".test").hide() - hides all elements with class="test".
* $("#test").hide() - hides the element with id="test".

As the .click() method is just a shorthand for .on( "click", handler ), detaching is possible using .off( "click" ). 

##method-1
```
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
</head>
<div id="imgWrap">
    <img id="img1" class="Active" data-box="div1"/>
    <img id="img2" data-box="div2"/>
    <img id="img3" data-box="div3"/>
    <img id="img4" data-box="div4"/>
</div>

<div id="divWrap">
    <div id="div1" class="Active">1</div>
    <div id="div2">2</div>
    <div id="div3">3</div>
    <div id="div4">4</div>
</div>
<script>
$('img').on('click', function () {
  var divID = $(this).attr('data-box');
  $(this).addClass('Active').siblings().removeClass('Active');
  $('#' + divID).addClass('Active').siblings().removeClass('Active');
})
</script>
```


#  FizzBuzz
```
for (i=1; i<=20; i++)
{
  if(i%5==0 && i%3==0) 
  {
    console.log("FizzBuzz");
  } 
  else if(i%3==0)
  {
    console.log("Fizz");
  }
  else if (i%5==0)
  {
    console.log("Buzz");
  } 
  else 
  {
    console.log(i);
  }
}
``` 
