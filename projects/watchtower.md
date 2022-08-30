---
layout: project
type: project
image: img/watchtower/Watchtower.png
title: "WatchTower"
date: 2022
published: true
labels:
  - Raspbery Pi
  - IBM Cloud
  - JavaScript
summary: "Watchtower takes data from the Beach Safety API and sends it from a cloud application to a Raspberry Pi where it will display the current beach conditions."
---

<div class="text-center p-4">
  <img width="60%" src="../img/watchtower/IBMCloudFlow.png" class="img-thumbnail" >
</div>

Watchtower was a project done using tools such as IBM Cloud, Raspberry Pi, and JavaScript. The main goal of the project was to use an API and retrieve the data into our cloud application and be able to send data from the cloud application to the Raspberry Pi device. To do this project we used the Hawaii Beach Safety API and pulled the beach conditions into our IBM Cloud. The next step was being able to process the specific beaches we wanted to track and send to the Raspberry Pi. The IBM Cloud would parse the data from a JSON file and send the data of a specific beach to each of the connected Raspberry Pi devices. The cloud also created an HTTP endpoint that presented the conditions of the beaches that were sent to the Raspberry Pi devices. 
<div class="text-center p-4">
  <img width="60%" src="../img/watchtower/HTTP Endpoint.png" class="img-thumbnail" >
 </div>
The next step of this project was the Raspberry Pi device to process the data and display the condition of the beach. For this we created a homemade wheel that displayed the four possible conditions and an arrow that would be attached to a motor. The Raspberry Pi would be connected to a motor that would turn a variable number of degrees based on the beach conditions. The homemade arrow was attached to the motor and pointed to the corresponding beach conditions.
<div class="text-center p-4">
  <img width="60%" src="../img/watchtower/RaspberryPiFlow.png" class="img-thumbnail" >
 </div>
This project was a group of four where we split ourself into two groups where two worked on the Raspberyy Pi side of the project, and my group which worked with the beach safety API and the cloud application. I worked with parsing the JSON data and having functions to pull specific beaches and send the data to the Raspberry Pi devices and create the HTTP endpoint. In this experience I learned how to bring data from a cloud server and be able to pass it to a small computer (Raspberry Pi) where it would take the data and perform different actions based on the data received.
