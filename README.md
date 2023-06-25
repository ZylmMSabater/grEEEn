<!DOCTYPE html>
<html>
<head>
<title>grEEEn Web</title>
<style>
  .bg {
    background-image: url("Golden Pothos BG.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
  }
</style>
</head>


<body style="background-color: #b7cdb8;">


<p style="font-family: arial black; font-size:500%; text-align: center; position: relative; top: -0.5em;">
<img src="https://i.ibb.co/sqcxFXJ/Golden-Pothos.png" alt="Golden Pothos.png" width="153.6" height="153.6"">

gr<span style="color: #5370fd;">E</span><span style="color: #f40600;">E</span><span style="color: #4f8c46;">E</span>n
</p>

<p style="font-family: arial; font-size: 120%; text-align: center;">
<strong><i>Epipremnum aureum</i> (Golden Pothos) Requirements: </strong><br>
1. Light: >200ft-c (high-light areas), 75-200ft-c (med.-light), 25-75ft-c (low-light) <br>
2. Temperature: 65degF (night), 75degF (day) <br>
3. Relative Humidity: 25-49% <br>
4. Water: when surface is dry (every 1-2 weeks) <br>

<br><br>
<style>
hr {color: white; border-style: solid;}
</style>
<hr>
<br><br>
</p>

<p style="font-family: arial; font-size:150%; text-align: center;">
<b>Temperature and Humidity Sensor (AM2320) Readings</b> <br><br>

<iframe width="450" height="260" style="border: 1px solid #cccccc;" src="https://thingspeak.com/channels/2166518/charts/1?bgcolor=%23ffffff&color=%23508c46&dynamic=true&results=60&title=Temperature&type=line&yaxis=Degree+Celcius"></iframe>
<iframe width="450" height="260" style="border: 1px solid #cccccc;" src="https://thingspeak.com/channels/2166518/charts/2?bgcolor=%23ffffff&color=%23508c46&dynamic=true&results=60&title=Humidity&type=line&yaxis=%25+Relative+Humidity"></iframe>
<br><br>
</p>

<p style="font-family: arial; font-size:150%; text-align: center;">
<b>Temperature and Humidity Sensor (AM2320) Indicators</b> <br>
<span style="font-size: 80%;"><strong>Legend: </strong><br>
1. Direct Fan: 0 (off), 1 (direct), 2 (oscillating) <br>
2. Ceiling Fan: 0 (off), 1 (CW, circulates warm air), 2 (CC, pushes cool air) <br>
3. Humidity Tray: 0 (off), 1 (drain), 2 (pump) <br>
4. Moisture Absorber Tray: 0 (close), 1 (open) <br>
<span>
<br>
<iframe width="260" height="260" style="border: 1px solid #cccccc;" src="https://thingspeak.com/channels/2166518/widgets/676179"></iframe>
<iframe width="260" height="260" style="border: 1px solid #cccccc;" src="https://thingspeak.com/channels/2166518/widgets/676180"></iframe>
<iframe width="260" height="260" style="border: 1px solid #cccccc;" src="https://thingspeak.com/channels/2166518/widgets/676181"></iframe>
<iframe width="260" height="260" style="border: 1px solid #cccccc;" src="https://thingspeak.com/channels/2166518/widgets/676182"></iframe>
<br>

<p style="font-family: arial; font-size:150%; text-align: center;">
<b>Light Sensor (BH1750) Readings</b> <br><br>

<iframe width="450" height="260" style="border: 1px solid #cccccc;" src="https://thingspeak.com/channels/2149974/charts/1?bgcolor=%23ffffff&color=%23d62020&dynamic=true&results=60&title=Light+level&type=line&xaxis=Time&yaxis=Lux"></iframe>
<iframe width="450" height="260" style="border: 1px solid #cccccc;" src="https://thingspeak.com/channels/2149974/widgets/676195"></iframe>

<br><br>
</p>



<br><br>
<style>
hr {color: white; border-style: solid;}
</style>
<hr>
<br><br>
</p>

<p style="font-family: arial; font-size: 120%; text-align: center;">
<br>
About: An indoor plant monitoring application that tracks plant health, state solutions, and measure effects on close environment. Used AM2320, BH1750, and SGP30 sensors, ESP8266 Wi-Fi Modules, STM32F411RE as master, and Thingspeak as server. Chose <i>Epipremnum aureum</i> (Golden Pothos) as it has the most positive effects on indoor environment.
<br><br>
(c) John Danielle Castor (jtcastor1@up.edu.ph), Airick Miguel Reyes-Gonzales (@up.edu.ph), Zylm Sabater (@up.edu.ph); June 25, 2023<br>
<br><br>
</p>


</body>
</html>
