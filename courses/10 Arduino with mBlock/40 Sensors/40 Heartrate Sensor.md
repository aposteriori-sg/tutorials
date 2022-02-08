Heart Rate Sensor
---

![](images/heartsensor.jpg)

- Measures amount of light passing through skin
- Amount of light changes with blood flow
- Provides analog voltage signal

![](images/heartsample.jpg)

Note how the Voltage rises above mid-point (512 in case of reading in through A0-A5 analog inputs) on every pulse.

## Wiring & Coding

### Pin Connections

![](images/heartpins.jpg)

![](images/heartwiring.jpg)

![](images/heartcode.jpg)

- Plot Sensor Voltage reading as a timeline to create a Heart Monitor
- Need to convert Input reading (0-1023) to a Y (-150 to 150) on the cartesian (XY) coordinate system of the Stage
- Plot using any sprite

![](images/pen.jpg)
![](images/pen2.jpg)
![](images/pen3.jpg)
<hr>

![](images/heartmoncode.jpg)

<hr>

![](images/heartmoncode2.jpg)
