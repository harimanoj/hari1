# hari1

<!DOCTYPE html>
<html lang="en">
<head>
  <title>User Registration or login form</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
  <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
  <style>
  input[type=text], input[type=password] {
    width: 25%;
    padding: 10px 20px;
    margin: 8px 2px;
    display: inline-block;
    border: 1px solid #ccc;
    box-sizing: border-box;
}
.go{
width:75px;
padding: 10px;
border:1px solid #ccc;
border-radius: 25px;
background-color:black ;
color: white;
}
.login{
padding: .5%;
background-color:#ccc; 
}
hr { 
    display: block;
 
    border-style: inset;
    border-width: 1px; 
    width: 25%;
    hr:before,
    hr:after{
    content:"or"
    }
}
.inputs{
margin-bottom: 20px;
display: table;
}
.rlabel{
margin-top: 
}


  </style>
  
</head>
<body onload="Captcha()">
<form class="login" action="" >

<div class="container">

   <label for="uname" style=" margin-left:12.5%;"><b >Email ID</b></label>
    
      <label for="psw" style=" margin-left:21%;" ><b>Password</b></label>
     
	  </div>
	  <div class="container" >
	  <lable><b>Already Registered?</b></lable>
	  
	   <input type="email" style="height:40px; width: 290px;"   placeholder="   Enter Email ID" name="email" required>
	 
	   <input type="password"   placeholder="Enter Password" name="psw" required>
        
      <button type="submit" class="go">GO</button>
      
	  </div>
	  
	  
	  
	  
	  
	  </form>
	
	 <div style="width: 100%; height: 10px; border-bottom: 1px solid black; text-align: center">
      <span style="font-size: 15px; background-color: #F3F5F6; ">
        OR
      </span>
    </div>
    
	<div class="container">
	<div style="display: inline-block;margin-right: 100px"  >
	
	<label style="margin-top: 30px;margin-bottom: 10px;" >Register As*</label>
	<select class="inputs" style="width: 200px" ><option value="0">select member type</select>
	
	<label >Email ID*</label>
	<input class="inputs" type="email" placeholder="***@***.com"/>
	
	<label >Password*</label>
	<input class="inputs" style="display: table; width: 200px; margin-bottom: 20px;" type="password" placeholder=""/>
	
	<label>Full name</label>
	<input  type="text" style="display:table;width: 200px; margin-bottom: 20px;"  placeholder="first name"/>
	
	<label>Display name</label>
	<input  type="text" style="display:table;width: 200px; margin-bottom: 20px;"  placeholder=""/>
	
	<label>CAPTCHA*</label>
	<input type="text" id= "mainCaptcha" style="width:200px; display: table; "  readonly="true"  /> 
	</div>
	
	<div style="display: inline-block; margin-right: 100px;"   >
	<label >Confirm Password*</label>
	<input class="inputs" style="display:table;width: 200px; margin-bottom: 20px;" type="password" placeholder=""/>
	
	<label> </label>
	<input  type="text" style="display:table;width: 200px; margin-bottom: 20px;"  placeholder="middle name"/>
	
	<label>Mobile number*</label>
	<input  type="number" style="display:table;width: 200px; height: 40px; margin-top: 10px;   margin-bottom: 20px;"  placeholder="first name"/>
	
	<label>Enter code here*</label>
	<input type="text" id="txtInput"  style="display: table;"/>
	</div>
	
	
	<div style="display: inline-block; "   >
	<label> </label>
	<input  type="text" style="display:table;width: 200px; margin-bottom:20px;"  placeholder="last name"/>
	
	<label>Gender*</label>
	<select class="inputs" style="width:200px; height: 40px; margin-top: 10px;" ><option value="0"></select>
	
	<label>  </label>
	
	</div>
	<div class="container">
	<form action="">
	<div class="row1">
	<div class="col-lg-6">
	<label>Email ID</label>
	<div class="row">
	<div class="col-lg-4">
	<label>Already registertred</label>
		</div>
	<div class="col-lg-8">
	<input type="email" name="email">
	</div>
	</div>
	</div>
	<div class="col-lg-6">
	<label>Password</label>
	<div class="row">
	
	</div>
	
	</div>
	
	</div>
	</div>	
	</form>	
	</div>
	
	  </body>
	  <script type="text/javascript">
                 function Captcha(){
                     var alpha = new Array('A','B','C','D','E','F','G','H','I','J','K','L','M','N','O','P','Q','R','S','T','U','V','W','X','Y','Z','a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z');
                     var i;
                     for (i=0;i<6;i++){
                       var a = alpha[Math.floor(Math.random() * alpha.length)];
                       var b = alpha[Math.floor(Math.random() * alpha.length)];
                       var c = alpha[Math.floor(Math.random() * alpha.length)];
                       var d = alpha[Math.floor(Math.random() * alpha.length)];
                       var e = alpha[Math.floor(Math.random() * alpha.length)];
                       var f = alpha[Math.floor(Math.random() * alpha.length)];
                       var g = alpha[Math.floor(Math.random() * alpha.length)];
                      }
                    var code = a + ' ' + b + ' ' + ' ' + c + ' ' + d + ' ' + e + ' '+ f + ' ' + g;
                    document.getElementById("mainCaptcha").value = code
                  }
                  function ValidCaptcha(){
                      var string1 = removeSpaces(document.getElementById('mainCaptcha').value);
                      var string2 = removeSpaces(document.getElementById('txtInput').value);
                      if (string1 == string2){
                        return true;
                      }
                      else{ 
                    	  alert("Enter Valid Captcha!");
                    	  Captcha();
                        return false;
                      }
                  }
                  function removeSpaces(string){
                    return string.split(' ').join('');
                  }
</script>
	  </html>
	  
	  
