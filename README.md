# taotao1
<!doctype html>
<html>
	<head>
		<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
		<title>happy birthday!</title>
		<style>
		body
			{
				margin:0;
				background:#000;
			}
h1{
  position:absolute;
  width: 100%;
top:50%;
  text-align: center;
  transform:translateY(-50%);
  font-family: 'Love Ya Like A Sister', cursive;
  font-size: 40px;
  color: #c70012;
  padding: 0 20px;
}
h1 span{
    font-size:30px;
}
h1 p{
    font-size:30px;
  position:absolute;
}
		#wrap
			{
				width:300px;
				height:400px;
				position: relative;
				margin: 300px auto;
				-webkit-perspective:3000px;
				-moz-perspective:3000px;
				-ms-transform:perspective(3000px);
				-ms-perspective:3000px;
			}
		#head
			{
				width:100%;
				height:100%;
				position: absolute;
				-webkit-transform-style: preserve-3d;
				-webkit-animation:donghua 15s linear 0s infinite;
				-moz-transform-style: preserve-3d;
				-moz-animation:donghua 15s linear 0s infinite;
				-ms-transform-style: preserve-3d;
				-ms-animation:donghua 25s linear 0s infinite;
			}
		#head div
			{	
				position: absolute;
				top:0;
				left:0;
				width:300px;
				height:400px;
				border:1px solid #000
				text-align: center;
				line-height:100px;
			}
		#head div:nth-child(1)
			{
				-webkit-transform:rotateY(0deg) translateZ(400px);
				-moz-transform:rotateY(0deg) translateZ(400px);
				-ms-transform:rotateY(0deg) translateZ(400px);
				background:url(images/01.png);
				background-size:cover;
			}
		#head div:nth-child(2)
			{
				-webkit-transform:rotateY(36deg) translateZ(500px);
				-moz-transform:rotateY(36deg) translateZ(500px);
				-ms-transform:rotateY(36deg) translateZ(500px);
				background:url(images/02.png
);
				background-size:cover;
			}
			
		#head div:nth-child(3)
			{
				-webkit-transform:rotateY(72deg) translateZ(400px);
				-moz-transform:rotateY(72deg) translateZ(400px);
				-ms-transform:rotateY(72deg) translateZ(400px);
				background:url(images/03.png);
				background-size:cover;
			}
			
		#head div:nth-child(4)
			{
				-webkit-transform:rotateY(108deg) translateZ(500px);
				-moz-transform:rotateY(108deg) translateZ(500px);
				-ms-transform:rotateY(108deg) translateZ(500px);
				background:url(images/04.png);
				background-size:cover;
			}
		#head div:nth-child(5)
			{
				-webkit-transform:rotateY(144deg) translateZ(400px);
				-moz-transform:rotateY(144deg) translateZ(400px);
				-ms-transform:rotateY(144deg) translateZ(400px);
				background:url(images/05.png);
				background-size:cover;
			}
		#head div:nth-child(6)
			{
				-webkit-transform:rotateY(180deg) translateZ(500px);
				-moz-transform:rotateY(180deg) translateZ(500px);
				-ms-transform:rotateY(180deg) translateZ(500px);
				background:url(images/06.png);
				background-size:cover;
			}
		#head div:nth-child(7)
			{
				-webkit-transform:rotateY(216deg) translateZ(400px);
				-moz-transform:rotateY(216deg) translateZ(400px);
				-ms-transform:rotateY(216deg) translateZ(400px);
				background:url(images/07.png);
				background-size:cover;
			}
		#head div:nth-child(8)
			{
				-webkit-transform:rotateY(252deg) translateZ(500px);
				-moz-transform:rotateY(252deg) translateZ(500px);
				-ms-transform:rotateY(252deg) translateZ(500px);
				background:url(images/08.png);
				background-size:cover;
			}
		#head div:nth-child(9)
			{
				-webkit-transform:rotateY(288deg) translateZ(400px);
				-moz-transform:rotateY(288deg) translateZ(400px);
				-ms-transform:rotateY(288deg) translateZ(400px);
				background:url(images/09.png);
				background-size:cover;
			}
		#head div:nth-child(10)
			{
				-webkit-transform:rotateY(324deg) translateZ(500px);
				-moz-transform:rotateY(324deg) translateZ(500px);
				-ms-transform:rotateY(324deg) translateZ(500px);
				background:url(images/10.png);
				background-size:cover;
			}
		@-webkit-keyframes donghua{
			0%{transform:rotateX(5deg) rotateY(360deg)}
			50%{transform:rotateX(-5deg) rotateY(180deg)}
			100%{transform:rotateX(5deg) rotateY(0deg)}
		}
		@-moz-keyframes donghua{
			0%{transform:rotateY(10deg) rotateY(0deg)}
			50%{transform:rotateY(-10deg) rotateY(180deg)}
			100%{transform:rotateY(10deg) rotateY(360deg)}
		}
		@-ms-keyframes donghua{
			0%{transform:rotateY(10deg) rotateY(0deg)}
			50%{transform:rotateY(-10deg) rotateY(180deg)}
			100%{transform:rotateY(10deg) rotateY(360deg)}
		}
		</style>
	</head>
	<body>
<h1 id="h1"></h1>
<canvas></canvas> <!--canvas 画布-->
<div id="wrap">
			<div id="head">
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
				<div></div>
			</div>
		</div>


<script>
var canvas = document.querySelector("canvas"),
  ctx = canvas.getContext("2d");

var ww,wh;

function onResize(){
  ww = canvas.width = window.innerWidth;
  wh = canvas.height = window.innerHeight;
}

ctx.strokeStyle = "red";
ctx.shadowBlur = 25;
ctx.shadowColor = "hsla(0, 100%, 60%,0.5)";

var precision = 100;
var hearts = [];
var mouseMoved = false;
function onMove(e){
  mouseMoved = true;
  if(e.type === "touchmove"){
    hearts.push(new Heart(e.touches[0].clientX, e.touches[0].clientY));
    hearts.push(new Heart(e.touches[0].clientX, e.touches[0].clientY));
  }
  else{
    hearts.push(new Heart(e.clientX, e.clientY));
    hearts.push(new Heart(e.clientX, e.clientY));
  }
}
var Heart = function(x,y){
  this.x = x || Math.random()*ww;
  this.y = y || Math.random()*wh;
  this.size = Math.random()*2 + 1;
  this.shadowBlur = Math.random() * 10;
  this.speedX = (Math.random()+0.2-0.6) * 8;
  this.speedY = (Math.random()+0.2-0.6) * 8;
  this.speedSize = Math.random()*0.05 + 0.01;
  this.opacity = 1;
  this.vertices = [];
  for (var i = 0; i < precision; i++) {
    var step = (i / precision - 0.5) * (Math.PI * 2);
    var vector = {
      x : (15 * Math.pow(Math.sin(step), 3)),
      y : -(13 * Math.cos(step) - 5 * Math.cos(2 * step) - 2 * Math.cos(3 * step) - Math.cos(4 * step)) 
    }
    this.vertices.push(vector);
  }
}

Heart.prototype.draw = function(){
  this.size -= this.speedSize;
  this.x += this.speedX;
  this.y += this.speedY;
  ctx.save();
  ctx.translate(-1000,this.y);
  ctx.scale(this.size, this.size);
  ctx.beginPath();
  for (var i = 0; i < precision; i++) {
    var vector = this.vertices[i];
    ctx.lineTo(vector.x, vector.y);
  }
  ctx.globalAlpha = this.size;
  ctx.shadowBlur = Math.round((3 - this.size) * 10);
  ctx.shadowColor = "hsla(0, 100%, 60%,0.5)";
  ctx.shadowOffsetX = this.x + 1000;
  ctx.globalCompositeOperation = "screen"
  ctx.closePath();
  ctx.fill()
  ctx.restore();
};



function render(a){
  requestAnimationFrame(render);

  hearts.push(new Heart())
  ctx.clearRect(0,0,ww,wh);
  for (var i = 0; i < hearts.length; i++) {
    hearts[i].draw();
    if(hearts[i].size <= 0){
      hearts.splice(i,1);
      i--;
    }
  }
}


onResize();
window.addEventListener("mousemove", onMove);
window.addEventListener("touchmove", onMove);
window.addEventListener("resize", onResize);
requestAnimationFrame(render);

window.onload=function starttime(){

        time(h1,'2021/10/3');     // 生日时间
        ptimer = setTimeout(starttime,1000); // 添加计时器

		
}

    function time(obj,futimg){
        var nowtime = new Date().getTime(); // 现在时间转换为时间戳
        var futruetime =  new Date(futimg).getTime(); // 未来时间转换为时间戳
        
		
		var msec= futruetime-nowtime;//倒计时，还差多久生日
        
		var time = (msec/1000);  // 毫秒/1000
        
        var day = parseInt(time/86400); // 天  24*60*60*1000 
		
        var hour = parseInt(time/3600)-24*day;    // 小时 60*60 总小时数-过去的小时数=现在的小时数 
		
        var minute = parseInt(time%3600/60); // 分 -(day*24) 以60秒为一整份 取余 剩下秒数 秒数/60 就是分钟数
	   
        var second = parseInt(time%60);  // 以60秒为一整份 取余 剩下秒数
		
        obj.innerHTML="陶淘老师<br>距离今年生日还有：<br>"+day+"天"+hour+"小时"+minute+"分"+second+"秒"+"了<br><span>祝好</span><p>下<br>滑<br>有<br>惊<br>喜</p>"
        
        

        return true;
    }
</script>
<audio autoplay="autoplay" loop="loop" preload="auto"
            src="http://music.163.com/song/media/outer/url?id=1337065812.mp3">       
</audio>	
	</body>
</html>
