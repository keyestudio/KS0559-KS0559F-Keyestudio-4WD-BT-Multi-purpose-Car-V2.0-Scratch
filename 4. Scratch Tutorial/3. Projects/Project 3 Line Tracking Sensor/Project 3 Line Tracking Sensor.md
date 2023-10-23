# Project 3: Line Tracking Sensor

![](/media/d37c24e508361ab86b019135ab6950a9.png)

**1.Description** 

The tracking sensor is actually an infrared sensor. The component used here is the TCRT5000 infrared tube. Its working principle is to use different reflectivity of infrared light to colors, then convert the strength of the reflected signal into a current signal.

During the process of detection, black is active at HIGH level while white is active at LOW level. The detection height is 0-3 cm.

Keyestudio 3-channel line tracking module has integrated 3 sets of TCRT5000 infrared tubes on a board, which is more convenient for wiring and control.

By rotating the adjustable potentiometer on the sensor, it can adjust the detection sensitivity of the sensor.

**2. Specification**

![](/media/0b3433af5abda1ab4137e2c078e4b8e7.jpeg)Operating Voltage: 3.3-5V (DC)

Interface: 5PIN

Output Signal: Digital signal

Detection Height: 0-3 cm

Note: Before testing, rotate the potentiometer on the sensor to adjust the detection sensitivity.  The sensitivity is best when adjusting the LED to a threshold between ON and OFF. 

**3. Components**

<table>
<tbody>
<tr class="odd">
<td>Keyestudio 4.0 Development Board *1</td>
<td>Keyestudio 8833 Motor Driver Expansion Board *1</td>
<td>Red LED Module*1</td>
<td></td>
</tr>
<tr class="even">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/6131c8d782756fe051b0ef0210a76d03.png" style="width:1.27292in;height:0.91875in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/5e291db96125e27f380e8caf79e8015a.png" style="width:1.09375in;height:0.95625in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/7aacff28b0cb9b99f0dbcbf22eb309e4.png" style="width:0.91111in;height:0.61111in" /></td>
<td></td>
</tr>
<tr class="odd">
<td>5P Dupont Wire*1</td>
<td>USB Cable*1</td>
<td>3P Dupont Wire*1</td>
<td>Keyestudio Line Tracking Sensor*1</td>
</tr>
<tr class="even">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/635b8724dc3e7a27f940b3953ed4536d.jpeg" style="width:1.70764in;height:0.18333in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/4f8d5af6dee9016b45d975adb2391d37.png" style="width:1.25208in;height:0.46319in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/e9aaac06e62418ecca6eaba97a9ec518.png" style="width:1.03056in;height:0.66667in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/635b8724dc3e7a27f940b3953ed4536d.jpeg" style="width:0.99375in;height:0.79514in" /></td>
</tr>
</tbody>
</table>
**4. Wiring Diagram**

![](/media/6426516400b21d7fbe1d9a1a58a1808b.png)

G, V, S1, S2 and S3 of the line tracking sensor are connected to G（GND), V（VCC), D11, D7 and D8 of the sensor expansion board.

**5. Test Code**

You can drag blocks to edit. Blocks listed below are for your reference

1.  ![](/media/5ad9eb9c639b74f8271a55079dcf845c.png)

2.  ![](/media/b1e2059ec06fcfc9423fa6287eb998ef.png)

3.  ![](/media/700cb0ecc14cbccd6e367c5098360f08.png)

4.  ![](/media/271423c55b5f147796beb344eed7e9cf.png)

5.  ![](/media/1a6838765472e3cd3836abb5202d9ab1.png)

Complete Test Code

![](/media/5d25ae3ae8d4e7acc4c2a870315c998b.png)

![](/media/43325e91f8d86baeec6a5dfe9879325e.png)

**6. Test Result**

After successfully uploading the code to the V4.0 board, connect the wirings according to the wiring diagram, and use a USB cable to connect the computer to power the board.

After powering on, click![](/media/9011f20d83897d7a5936793c4ae142fc.png)to set the baud rate to 9600 and you will view status of three line tracking sensors. When no signals are received, the value is 1. If we cover the sensor with a white paper, the value will be 0.

![](/media/2fd58c7a9f95fb9f694edf03e755042f.png)

![](/media/5630032421adf9446d51b770f0e7f8af.png)

**7. Extension Practice**

After knowing its working principle, you can connect an LED to D9 so as to control LED by it.

![](/media/52e2c2da94936d1febef0464f1e31cbb.png)

You can drag blocks to edit. Blocks listed below are for your reference

1.  ![](/media/5ad9eb9c639b74f8271a55079dcf845c.png)

2.  ![](/media/b1e2059ec06fcfc9423fa6287eb998ef.png)

3.  ![](/media/574854f4d96c40a85e1db549d85f14f4.png)

4.  ![](/media/9077c0d059f7a4d3277f10ccb4e962fb.png)

5.  ![](/media/1a6838765472e3cd3836abb5202d9ab1.png)

（6）![](/media/80e9c514357c63f4791c72220829b673.png)

（7）![](/media/b10e1897e99af2c1ade6c09da6c30dba.png)

Complete Test Code

![](/media/005a1621f24024fa6042e84f0d796ba3.png)

![](/media/3b63d2e99f53da8d099af6df0bd8bbd9.png)

After successfully uploading the code to the V4.0 board, connect the wirings according to the wiring diagram, and use a USB cable to connect the computer to power the board.

After powering on, make a paper close to the sensor, then we can find the LED light up when covering the line tracking sensor.
