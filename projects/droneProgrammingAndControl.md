---
layout: project
type: project
image: img/droneProgrammingAndControl/drone.png
title: "Drone Programming and Control"
date: 2021
published: true
labels:
  - Python
  - ArduPilot
  - QGroundControl
  - VirtualBox
summary: "Throughout this project we did various simulation drone flights before programming an actual drone to fly a set course around a park."
---

<div class="text-center p-4">
  <img width="60%" src="../img/droneProgrammingAndControl/drone.png" class="img-thumbnail" >
</div>
The goal of this project was to program a drone with Python to be able to do a mission autonomously. To get used to the code and practice with the commands we would first run simulations in a virtual machine with VirtualBox. We used an Ubuntu Linux OS to run our test code and flight simulations. We did various flight simulations such as a simple takeoff and land, a goto mission, and various others. Shown below is a script used for one of our simulations and the output of a simple takeoff simulation.

```python
from dronekit import connect
vehicle = connect('0.0.0.0:14550', wait_ready=True)

def arm_and_takeoff(aTargetAltitude):
    print("Basic pre-arm checks")
    # Don't try to arm until autopilot is ready
    while not vehicle.is_armable:
        print(" Waiting for vehicle to initialise...")
        time.sleep(1)

    print("Arming motors")
    # Copter should arm in GUIDED mode
    vehicle.mode = VehicleMode("GUIDED")
    vehicle.armed = True

    # Confirm vehicle armed before attempting to take off
    while not vehicle.armed:
        print(" Waiting for arming...")
        time.sleep(1)

    print("Taking off!")
    vehicle.simple_takeoff(aTargetAltitude)  # Take off to target altitude

    # Wait until the vehicle reaches a safe height before processing the goto
    #  (otherwise the command after Vehicle.simple_takeoff will execute
    #   immediately).
    while True:
        print(" Altitude: ", vehicle.location.global_relative_frame.alt)
        # Break and return from function just below target altitude.
        if vehicle.location.global_relative_frame.alt >= aTargetAltitude * 0.95:
            print("Reached target altitude")
            break
        time.sleep(1)

arm_and_takeoff(3)```
<div class="text-center p-4">
  <img width="60%" src="../img/droneProgrammingAndControl/Takeoff 40.png" class="img-thumbnail" >
</div>
