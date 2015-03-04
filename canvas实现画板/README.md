# moby4
使用canvas实现一个画板
<!DOCTYPE html> 
<html> 
    <head> 
        <title></title> 
        <meta http-equiv="Content-Type" content="text/html; charset=UTF-8"> 
        <style type="text/css">
        	#yellowBtn{ 
    width: 80px; 
    background-color: yellow; 
} 
#redBtn{ 
    width: 80px; 
    background-color: red; 
} 
#blueBtn{ 
    width: 80px; 
    background-color: blue; 
} 
#greenBtn{ 
    width: 80px; 
    background-color: green; 
} 
#whiteBtn{ 
    width: 80px; 
    background-color: white; 
    color: black; 
} 
#blackBtn{ 
    width: 80px; 
    background-color: black; 
    color: white; 
} 
#exportBtn{ 
    width: 80px; 
    background-color: navy; 
    color: magenta; 
}
        </style>
    </head> 
    <body> 
        <canvas id="myCanvas" width="600" height="300"> 
            这个<a href="http://www.it165.net/edu/ewl/" target="_blank" class="keylink">浏览器</a>不支持Canvas标签 
        </canvas><br/> 
        <button id="yellowBtn"  = "yellow";'>Yellow</button> 
        <button id="redBtn"  = "red";'>Red</button> 
        <button id="blueBtn"  = "blue";'>Blue</button> 
        <button id="greenBtn"  = "green";'>Green</button> 
        <button id="whiteBtn"  = "white";'>White</button> 
        <button id="blackBtn"  = "black";'>Black</button> 
        <button id="exportBtn"         <br/> 
        <img src="" id="image_png" width="600" height="300"/> 
        <script type="text/javascript"> 
            var canvas = document.getElementById("myCanvas"); 
            var ctx = canvas.getContext("2d"); 
            //画一个黑色矩形 
            ctx.fillStyle = "black"; 
            ctx.fillRect(0,0,600,300); 
            //按下标记 
            var onoff = false; 
            var oldx = -10; 
            var oldy = -10; 
            //设置颜色 
            var lineColor = "white"; 
            //设置线宽 
            var lineW = 4; 
            //添加鼠标移动事件 
            canvas.addEventListener("mousemove", draw, true); 
            //添加鼠标按下事件 
            canvas.addEventListener("mousedown", down, false); 
            //添加鼠标弹起事件 
            canvas.addEventListener("mouseup",up, false); 
                
            function down(event){ 
                onoff = true; 
                oldx = event.pageX - 10; 
                oldy = event.pageY - 10; 
            } 
                
            function up(event){ 
                onoff = false; 
            } 
                
            function draw(event){ 
                if(onoff === true){ 
                    var newx = event.pageX - 10; 
                    var newy = event.pageY - 10; 
                        
                    ctx.beginPath(); 
                    ctx.moveTo(oldx, oldy); 
                    ctx.lineTo(newx, newy); 
                    ctx.strokeStyle = lineColor; 
                    ctx.lineWidth = lineW; 
                    ctx.lineCap = "round"; 
                    ctx.stroke(); 
                        
                    oldx = newx; 
                    oldy = newy; 
                } 
            } 
            function copyImage(event){ 
                var image_png_ canvas.toDataURL("image /png"); 
                document.getElementById("image_png"). image_png_src; 
             } 
        </script> 
    </body> 
</html>
