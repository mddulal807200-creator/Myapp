<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Private App</title>
<style>
body{
margin:0;
font-family:Arial;
background:#0f6b50;
color:white;
text-align:center;
}
.hidden{display:none;}
input{
padding:10px;
width:200px;
}
button{
padding:10px;
margin-top:10px;
}
.card{
background:white;
color:black;
margin:15px;
padding:15px;
border-radius:10px;
}
</style>
</head>
<body>

<div id="login">
<h2>🔐 Secure Login</h2>
<input type="password" id="pin" placeholder="Enter PIN">
<br><br>
<button onclick="login()">Login</button>
</div>

<div id="portal" class="hidden">
<h2>ROKIBUL HASSAN</h2>
<p>ID-2447788665</p>
<p id="clock"></p>

<div class="card">Business Status: Active</div>
<div class="card">Monthly Report: 18%</div>

<button onclick="logout()">Logout</button>
</div>

<script>
const PIN="2447";

function login(){
if(document.getElementById("pin").value===PIN){
document.getElementById("login").classList.add("hidden");
document.getElementById("portal").classList.remove("hidden");
}else{
alert("Wrong PIN");
}
}

function logout(){
location.reload();
}

setInterval(function(){
document.getElementById("clock").innerHTML=new Date().toLocaleString();
},1000);
</script>

</body>
</html> Myapp
