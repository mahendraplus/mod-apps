<html>

<head>

<meta name="viewport" content="width=device-width, initial-scale=1.0">

 <title>Border live</title>

 <style>

 @import url('https://fonts.googleapis.com/css2?family=Handlee&display=swap');

.data{

color: #00ff04;

font-family: 'Handlee', cursive;

text-align: center;

border: 0.5px solid blue;

  border-radius: 50px 0px 50px 0px;

  padding: 15px;

  width: 90%;

  margin: auto;

}

#clock{

color: #00ff04;

font-family: 'Handlee', cursive;

margin: 0px 0px -23px 350px;

width: 10px;

}

.text{

color: white;

font-family: 'Handlee', cursive;

margin: auto;

  width: 30%;

  border: 0.5px solid orange;

  border-radius: 50px 0px 50px 0px;

  padding: 10px;

  text-align: center;

  background: linear-gradient(20deg,yellow,red);

}

.hr{

border: 0.1px solid red;

}

.shadow 

{

	position: absolute;

  left: calc(50% - 208.5px);

  top: calc(50% - 410px);

	width: 98%;

	height: 820px;

  border-radius: 5px 5px 40px 40px;

	background: linear-gradient(0deg,black,black);

}

.shadow:before,

.shadow:after

{

	content: '';

  border-radius: 5px 5px 40px 40px;

	position: absolute;

	top: -2px;

	left: -2px;

	background: linear-gradient(45deg,#fb0094,#0000ff,#00ff00,#ff0000,#fb0094,#0000ff,#00ff00,#ff0000);

	background-size: 400%;

	width: calc(100% + 4px);

	height: calc(100% + 4px);;

	z-index: -1;

	animation: animate 15s linear infinite;

}

.shadow:after 

{

	filter: blur(5px);

}

@keyframes animate

{

	0%

	{

		background-position: 0 0;

	}

	50%

	{

		background-position: 400% 0;

	}

	100%

	{

		background-position: 0 0;

	}

}

 </style>

</head>

<body onload="startTime()">

<div class="main">

<div class="shadow">

<hr class="hr">

<p id="clock">Time</p>

<h3 class="text">M 4 U . Y T</h3>

<hr class="hr">

<div class="data">

<h3>How to get client IP address using JavaScript ?</h3>

<p>n simple language, an IP address is a combination of numbers that uniquely identifies one’s system. It’s like a house has an address to get an mail, just like that your computer has an address to receive the data from the web. The word protocol refers to some set guidelines which need to be followed while browsing for global connectivity. The networking part of the Internet is defined by exact specifications (guidelines) for connecting on the Internet.</p>

</div>

</div>

</div>

<script>

function startTime() {

  var today = new Date();

  var h = today.getHours();

  var m = today.getMinutes();

  var s = today.getSeconds();

  m = checkTime(m);

  s = checkTime(s);

  document.getElementById('clock').innerHTML =

  h + ":" + m + ":" + s;

  var t = setTimeout(startTime, 500);

}

function checkTime(i) {

  if (i < 10) {i = "0" + i};  // add zero in front of numbers < 10

  return i;

}

</script>

</body>

</html>

