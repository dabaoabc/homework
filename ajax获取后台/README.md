# moby1
ajax获取后台数据
<!DOCTYPE html>
<html> 
	<head>
		<meta charset="utf-8" />
		<title></title>
        
	</head>
	<body>
	
        <ul class="e_focus_slides clrfix">
	    <li class="slides-list fl">
                <ul id="page clrfix">
                   <li class="page-list fl">
                      <div class="favicon">
                          <img id="img1" src="" alt="" />
                              <span class="zhezhao pngfix"></span>
                      </div>
                     <p id="userName1"></p>
                   </li>
                  <li class="page-list fl">
            <div class="favicon">
                <img id="img2" src="" alt="" />
                <span class="zhezhao pngfix">
                </span>
            </div>
            <p id="userName2">
                
            </p>
        </li>
        <li class="page-list fl">
            <div class="favicon">
                <img id="img3" src="" alt="" />
                <span class="zhezhao pngfix">
                </span>
            </div>
            <p id="userName3">
                
            </p>
        </li>
        <li class="page-list fl">
            <div class="favicon">
                <img id="img4" src="" alt="" />
                <span class="zhezhao pngfix">
                </span>
            </div>
            <p id="userName4">
                
            </p>
        </li>
    </ul>
</li>
</ul>
<script type="text/javascript">
          var data = {
        "ret":true, 
        "errcode":0, 
        "errmsg":"success", 
        "ver":1, 
        "data":{
            "page":3,
            "travelers":[
                {"nickName":"andycall","userImg":"..."},
                {"nickName":"boolean93","userImg":"..."},
                {"nickName":"zeroling","userImg":"..."},
                {"nickName":"lecion","userImg":"..."}
            ],
            "travelerCnt":48,
            "size":20
        }
    }
     document.getElementById("userName1").innerHTML=data.data.travelers[0].nickName;
     document.getElementById("userName2").innerHTML=data.data.travelers[1].nickName;
     document.getElementById("userName3").innerHTML=data.data.travelers[2].nickName;
     document.getElementById("userName4").innerHTML=data.data.travelers[3].nickName;
     document.getElementById("page clrfix").setAttribute("data-page",data.data.page)
     document.getElementById("page clrfix").setAttribute("data-travelerCnt",data.data.travelerCnt)
     document.getElementById("page clrfix").setAttribute("data-size",data.data.size)
     document.getElementById("img1").setAttribute("src",data.data.travelers[0].userImg)
     document.getElementById("img2").setAttribute("src",data.data.travelers[1].userImg)
     document.getElementById("img3").setAttribute("src",data.data.travelers[2].userImg)
     document.getElementById("img4").setAttribute("src",data.data.travelers[3].userImg)
        </script>
	</body>
</html>
