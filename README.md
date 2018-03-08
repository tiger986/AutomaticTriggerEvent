## An event that automatically triggers an element
#### JS code
```javascript
//JQ的方法
	$(function(){
		
		$(".d1").click(function(){
			alert("d1的点击事件");
		});
		
		$(".d1").trigger("click");	
		
	})
	
	//JS的方法
	var div2 = document.getElementById("div2");
	
	div2.onclick = function(){
		alert("d2的点击事件")
	}
	
	if(document.all){//IE
		div2.click();
	}else {//其它浏览器
		var e = document.createEvent("MouseEvents");
		e.initEvent("click", true, true);
		div2.dispatchEvent(e);
	}
