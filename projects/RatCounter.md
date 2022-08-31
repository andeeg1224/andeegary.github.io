---
layout: project
type: project
image: img/ratcounter/arduino.png
title: "Rat Counter"
date: 2020
published: true
labels:
  - Arduino
  - C
  - MIT AppInventor
summary: "An Arduino based project that uses motion sensors to keep track of the times a rat passed through a certain area and sent the data to an android app."
---
<html>
<body>
<style>
div.a {
	text-align: center;
}
</style>
<div class="text-center p-4">
  <img width="60%" src="../img/ratcounter/arduino.png" class="img-thumbnail" >
</div>
 The goal of this project was to incorporate an Arduino with other hardware and connect it to an app that we created using MIT AppInventor. At the start we went through som basic tutrials with our Arduino and MITAppInventor to become familiar with them before getting into the project. The idea for Rat Counter came from conservation work that uses rat tunnels and wanted a way to track how many rats pass through these tunnels. Using various motion sensors we set it up so anytime a rat sized thing had run past the sensor it would keep a counter and increment each time. The Arduino circuit created for this project is shown below. 
 <div class="text-center p-4">
  <img width="60%" src="../img/ratcounter/RatCounterCircuit.png" class="img-thumbnail" >
</div>
The next stage of this project was creating an app that could connect to the Arduino. Bluetooth was used for 
