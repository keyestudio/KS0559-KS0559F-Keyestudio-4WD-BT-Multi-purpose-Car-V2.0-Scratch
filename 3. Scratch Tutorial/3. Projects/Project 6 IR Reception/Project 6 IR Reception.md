# Project 6 IR Reception

![](/media/f247e1010aa68c1e58e16b332680698a.png)**1.Description** There is no doubt that infrared
remote control is ubiquitous in daily life. It is used to control
various household appliances, such as TVs, stereos, video recorders and
satellite signal receivers. Infrared remote control is composed of
infrared transmitting and infrared receiving systems, that is, an
infrared remote control and infrared receiving module and a single-chip
microcomputer capable of decoding.  

![](/media/df5f1c28b8863b42ff94a36a6d81b933.png)

The 38K infrared carrier signal emitted by remote controller is encoded
by the encoding chip in the remote controller. It is composed of a
section of pilot code, user code, user inverse code, data code, and data
inverse code. The time interval of the pulse is used to distinguish
whether it is 0 or 1 signal and the encoding is made up of these 0, 1
signals.

The user code of the same remote control is constant while the data code
can distinguish the key.

When the remote control button is pressed, the remote control sends out
an infrared carrier signal. When the IR receiver receives the signal,
the program will decode the carrier signal and determines which key is
pressed. The MCU decodes the received 01 signal, thereby judging what
key is pressed by the remote control.

Infrared receiver we use is an infrared receiver module. Mainly composed
of an infrared receiver head, which is a device that integrates
reception, amplification, and demodulation. Its internal IC has
completed demodulation, and can achieve from infrared reception to
output and be compatible with TTL signals.

Additionally, it is suitable for infrared remote control and infrared
data transmission. The infrared receiving module made by the receiver
has only three pins, signal line, VCC and GND. It is very convenient to
communicate with Arduino and other microcontrollers.

**2.Specification**

![](/media/f247e1010aa68c1e58e16b332680698a.png)Operating Voltage: 3.3-5V（DC）

Output Signal: Digital signal

Receiving Angle: 90 degrees

![](/media/5ad0f889b39646ecb13664511479efc8.png)Frequency: 38khz

Receiving Distance: 10m

The right picture shows the real product and circuit diagram of the
infrared receiver

**3.Components**

<table>
<tbody>
<tr class="odd">
<td>Keyestudio 4.0 Development Board *1</td>
<td>Keyestudio 8833 Motor Driver Expansion Board *1</td>
<td>Red LED Module*1</td>
</tr>
<tr class="even">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/6131c8d782756fe051b0ef0210a76d03.png" style="width:1.27292in;height:0.91875in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/5e291db96125e27f380e8caf79e8015a.png" style="width:1.09375in;height:0.95625in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/7aacff28b0cb9b99f0dbcbf22eb309e4.png" style="width:0.91111in;height:0.61111in" /></td>
</tr>
<tr class="odd">
<td>3P F-F Dupont Wire*1</td>
<td>USB Cable*1</td>
<td></td>
</tr>
<tr class="even">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/e9aaac06e62418ecca6eaba97a9ec518.png" style="width:1.03056in;height:0.66667in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/4f8d5af6dee9016b45d975adb2391d37.png" style="width:1.38611in;height:0.5125in" /></td>
<td></td>
</tr>
</tbody>
</table>

Since the 8833 board integrates with the IR receiver, it doesn’t need
wiring up.

Pins of IR receiver module are G(GND）, V（VCC）and D3.

**4.Test Code**

Before writing the code, it is necessary to import the library file of
the IR receiver sensor. The specific steps are as follows: 

Click ![](/media/9964e0b31fc9846a7f64c57f51e47152.png)to enter the extension library interface of
sensors/modules/components, then search for“ir remote”
sensor![](/media/229086011fb4f87f3a882e514b043bb7.png) and click it. In this way, "Not loaded"
changes to "loaded", indicating that ir remote”sensor was added
successfully. 

![](/media/52ed0e6f7d436d17d18168c4704f5e98.png)

Click ![](/media/29916972665d35bfb34914b6144e28aa.png)to return to the code editor interface, the
instruction block of the added “ir remote”sensor can be seen in the
module area. 

![](/media/9f3467140d92cacbb3521d7a11945bc2.png)

You can drag blocks to edit. Blocks listed below are for your reference

1.  ![](/media/8de1b04be1ba147dd242c66bddeacacc.png)

2.  ![](/media/e9da5ac1d1d68eaec6db176ee61326ee.png)

3.  ![](/media/5a48421831518ea8e0c00be83cf4edf4.png)

4.  ![](/media/7fbfc1f04fbf08609fe34b47e09e4e29.png)

Complete Test Code

![](/media/90978855cddd94c161f9ed02f85b0674.png)

**5.Test Result**

After successfully uploading the code to the V4.0 board, connect the
wirings according to the wiring diagram, then connect the computer via a
USB cable to power the board. After powering on, click
![](/media/9011f20d83897d7a5936793c4ae142fc.png)to set baud rate to 9600.

Take out the remote control, and send signal to the infrared receiver
sensor. You can see the key value of the corresponding key, if the key
time is too long, FFFFFFFF is prone to garbled characters.

![](/media/5c01c594a5a11511cf52466eb5f27e45.png)

The keys value of remote control are shown below.

> ![](/media/ebcf0cb2055f7784505f76ceeaef9f47.jpeg)

**6.Extension Practice**

We have decoded the key value of the IR remote control. How about
controlling LED by the measured value? We could design an experiment.

Attach an LED to D9, then press the keys of remote control to make LED
light on and off.

![](/media/2138e6654076fc28e1715cebf9a87795.png)

You can drag blocks to edit. Blocks listed below are for your reference

1.  ![](/media/8de1b04be1ba147dd242c66bddeacacc.png)

2.  ![](/media/e9da5ac1d1d68eaec6db176ee61326ee.png)

3.  ![](/media/ba67c48d67b1c9753fca82964c9dddc7.png)

4.  ![](/media/7fbfc1f04fbf08609fe34b47e09e4e29.png)

5.  ![](/media/f8b75df8ccea3efe1cd3ea383b0f88f2.png)

6.  ![](/media/7406d60c93cdba0b13ded27cba718ec7.png)

7.  ![](/media/d7be3fa06a1456d46472fffd61823c73.png)

8.  ![](/media/136120d5e20a595a82d7ef8ecfa17c5d.png)

Complete Test Code

![](/media/57149c79243ff22aa00ff2c54dd4f70b.png)

After successfully uploading the code to the V4.0 board, connect the
wirings according to the wiring diagram, then connect the computer via a
USB cable to power the board. After powering on, press the OK key on
remote control can make the LED on and off.
