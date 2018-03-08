## An event that automatically triggers an element
#### JS code
```javascript
//JQ method
$(function(){		
    $(".d1").click(function(){
	alert("d1's click events");
    });	
    $(".d1").trigger("click");			
})
	
//JS method
var div2 = document.getElementById("div2");
div2.onclick = function(){
    alert("d2's click events")
}	
if(document.all){//IE
    div2.click();
}else {//Other browsers
    var e = document.createEvent("MouseEvents");
    e.initEvent("click", true, true);
    div2.dispatchEvent(e);
}
