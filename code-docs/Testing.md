---
description: 'Get help with programming your robot, simple scripts can be found here.'
---

# Testing
### Getting started

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