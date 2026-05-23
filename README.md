<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Yerowan</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial;
}

body{
background:black;
height:100vh;
overflow:hidden;
display:flex;
justify-content:center;
align-items:center;
}

#login{
position:absolute;
width:100%;
height:100%;
background:black;
display:flex;
justify-content:center;
align-items:center;
flex-direction:column;
z-index:5;
}

input{
padding:15px;
width:250px;
border:none;
outline:none;
border-radius:15px;
text-align:center;
font-size:20px;
margin-bottom:15px;
}

button{
padding:12px 30px;
border:none;
border-radius:15px;
font-size:18px;
cursor:pointer;
background:white;
}

#main{
display:none;
width:100%;
height:100%;
justify-content:center;
align-items:center;
background:black;
}

img{
width:100%;
height:100%;
object-fit:cover;
}

.fade{
animation:fade 2s;
}

@keyframes fade{
from{
opacity:0;
}
to{
opacity:1;
}
}

</style>
</head>

<body>

<div id="login">

<h1 style="color:white;margin-bottom:20px;">
Enter Password
</h1>

<input type="password" id="password" placeholder="Password">

<button onclick="checkPass()">
Open
</button>

</div>

<div id="main" class="fade">

<img src="photo.jpg">

<audio id="music" autoplay loop>
<source src="music.mp3" type="audio/mpeg">
</audio>

</div>

<script>

function checkPass(){

let pass = document.getElementById("password").value;

if(pass === "161125"){

document.getElementById("login").style.display="none";

document.getElementById("main").style.display="flex";

document.getElementById("music").play();

}else{

alert("Wrong Password");

}

}

</script>

</body>
</html>
