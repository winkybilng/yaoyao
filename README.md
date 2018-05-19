# yaoyao01
<!DOCTYPE html>
<html>
<head>
	<title>yaoyao01</title>
	<style type="text/css">
		.form{
			margin: 25px 10px;

		}
		.name{
			font-weight: bold;
			margin: 15px;
		}
		.kuang{
			border: 1px solid #778899;
			outline: none;
			border-radius: 5px;
			-moz-border-radius:5px;
			height: 25px;
			width: 300px;
		}
		.submit{
			margin: 10px;
			height: 28px;
			width: 50px;
			background-color: #436EEE;
			color: white;
			font-weight: bold;
			border-radius: 5px;
			-moz-border-radius:5px;
			outline: none;
		}
		.check{
			margin-left: 70px;
			font-family: 70%;
			color: #778899;
		}
		.success .kuang{
			border: 1px solid green;
		}
		.success .check{
			color:green;
		}
		.erro .kuang{
			border: 1px solid red;
		}
		.erro .check{
			color: red;
		}
	</style>
</head>
<body>
	<form class="form">
		<div id="sum">
			<b for="name0" class="name">名称</b>
			<input type="text" class="kuang" id="name0"  onfocus="myFunction(this)">
			<button type="button" class="submit" id="submit">验证</button>
		<div class="check" id="check">
			必填，长度为4到16个字符
		</div>
		</div>
	</form>
	<script type="text/javascript">
		var reg= /^[\u4E00-\u9FA5A-Za-z0-9 ]+$/;
		function myFunction(x){
			x.value="";
			document.getElementById("sum").className="";
			document.getElementById("check").innerHTML = "必填，长度为4到16个字符";
		}
		document.getElementById("submit").onclick=function(){
			if (reg.test(document.getElementById("name0").value)&&document.getElementById("name0").value.length>3&&document.getElementById("name0").value.length<17) {
			document.getElementById("sum").className="success";	
			document.getElementById("check").innerHTML = "名称格式正确";
			} else {
			document.getElementById("sum").className="erro";
			document.getElementById("check").innerHTML = "姓名格式错误";
			}

		};

	</script>
</body>
</html>
