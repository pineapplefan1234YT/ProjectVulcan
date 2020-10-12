---
description: 'A step by step guide on connecting your robot and moving.'
---

# Getting Started

{% hint style="info" %}
Control or Expansion Hub colours

| Colour                  | When    | Explanation                                                                                                                                    |
|-------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Blue                    | On boot | Battery connected, waiting for signal from driver station                                                                                      |
| Blue                    | Anytime | Waiting for a signal from the driver station                                                                                                   |
| Green                   | Anytime | Power connected, communication with driver station successful                                                                                  |
| Blue Blinking           | Anytime | Connection is timing out : Will become blue when connection resumes                                                                            |
| Orange Blinking         | Anytime | Battery voltage is under 7V. This usually means it is getting power from a phone. Check the battery is powered on and your switch is set to on |
| Green and Blue Blinking | Anytime | Hub has power, and communication with the driver station. The number of blue flashes is the Hub address - Default of 2                         |
{% endhint %}

## Parts


Heres a list of things you are going to need in order to have a working test:
- A phone for your driver station (DS)
- Either a Control Hub **or** an Expansion Hub with a phone connected to it (RC)
- A motor, along with a power cable (Red/Black with thick White clip on both ends) and a data cable (4 pins, Red Blue Black White wires)
- A servo, along with a servo data cable (3 pins, Black Black and White wires)
- A charged battery, along with a power cable (Red/Black with Yellow clips on either end)

-----

# Connecting cables

You'll need to make sure cables are in the right ports. A full diagram of all cables can be found [here](https://cdn11.bigcommerce.com/s-t3eo8vwp22/images/stencil/500x500/products/391/1330/Control_Hub_Wiring_Reference_Sheet_Website_Photo__13208.1563821357.png?c=2).

{% hint style="warning" %}
The image is the wiring guide for a Control Hub, however the wires are the same for an Expansion Hub. The only additional cable is the phone cable at the back of the Hub.
{% endhint %}

Find your Expansion or Control Hub.

The cables you need to add are as follows:
- Connect the battery into one of the 2 power slots in the upper left of the Hub. There will only be one slot that the cable can fit in. You can add a switch here as well.
- If you are using an Expansion Hub, connect the phone using 2 different cables. Place a USB to USB Micro into into the back of the Hub. Connect a phone to this using a feminine USB on one end, and the adapter needed for your team's phone on the other.
- Place the servo into port `0` in the front slots. There is a long line of many different servo connections, but it is easier to use `0`. It may be the wrong way around, but you can flip it later if it does not spin.
- The motor needs 2 wires. Place the red and black wire into motor port `0`, and the data wire into the slot nearest to it. It may be hard to get the wires in place. The other end of each cable will plug into a motor.

-----

# Connecting the phones - Expansion Hub

You need 2 phones, RC (Robot Controler) and DS (Driver Station).
Both of these deviced need to communicate in order to drive your robot.

Firstly, the RC is plugged into the expansion hub, and the DS has nothing plugged in yet.
The RC will create a WiFi signal, which can be connected to by a number of devices. You will need your DS, and optionally a computer or laptop.

On your RC, click in the top right, and select `Program and Manage`. This screen contains your connection name and password. Make sure not to share this with other teams.

Open the settings app on your DS, and head to WiFi. Select your WiFi network and join it. In the future, you may not need to do this step, as the 2 phones are paired and will prompt you to accept or decline a connection.

With this connection, if you return to your Driver Station app, you should see the Expansion Hub have a Green light (see colour coding above).

-----

# Configuration

Click in the top right and select Configure Robot.
This is where you assign devices and names.

Create a new configuration.
Next, add an Expansion or Control Hub. Just click `scan` at the top and wait until one is detected. If it does not appear, this could be either a connection issue, or faulty wires.
Select "Expansion Hub 2" or similar if you are prompted with it.

You need to add a few things on this page. Refer to the [Wiring guide](https://cdn11.bigcommerce.com/s-t3eo8vwp22/images/stencil/500x500/products/391/1330/Control_Hub_Wiring_Reference_Sheet_Website_Photo__13208.1563821357.png?c=2) if you need advice on where things go.
- Motors / port `0` - Add the type of motor you plugged in, usually found on the product label. Give it the name `motor` if you are using the example code in the next step.
- Servos / port `0` - Add the type of servo you plugged in, most likely you want the one called `servo`. Give it the name `servo` if you are using the example code in the next step.

-----

# Programming

Next up is to add some code.
If you are on a computer or laptop, you can edit code and settings at `192.168.49.1:8080`. You need to be connected to the phone's WiFi.

Here is an example which will do 2 things:

![Code example](https://github.com/pineapplefan1234YT/ProjectVulcan/blob/master/assets/Images/New.png?raw=true)
[Download here](https://github.com/pineapplefan1234YT/ProjectVulcan/blob/master/assets/Code/New.blk)

- Spin a motor constantly
- Spin a servo left, then right
- Loop

Click "Save OP Mode" in the top left to save your code. It will update on the app automatically, no restart required.
On your DC, select the right dropdown, and choose "New".
If new does not appear, try restarting the app, checking your code was saved, and you are connected to the phone's WiFi

Hit the **Init**ialise button, then the play button to run the code. Click it again to stop.

{% hint style="info" %}
The left dropdown means Autonomous scripts. This can be chosen when editing code.
The right dropdown means TeleOP, or Driver Controlled.
{% endhint %}

If this does not happen there are a few things to check.

Any errors on the phone:
Missing device errors can be common. Just check your configuration uses the name "motor" and "servo" in port `0` of their respective category.