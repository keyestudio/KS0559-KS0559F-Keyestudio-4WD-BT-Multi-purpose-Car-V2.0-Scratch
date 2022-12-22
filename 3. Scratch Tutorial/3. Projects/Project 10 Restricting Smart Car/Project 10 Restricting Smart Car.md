# Project 10 Restricting Smart Car

![](/media/644a1976bf17a6b64e0aed1a7240ff1e.jpeg)

**1.Description**

In this project, we look to combine the knowledge of a line tracking
sensor and motor driver modules to make a restricting smart car.  In the
experiment, we aim to use the line tracking sensor to detect whether
there is a black line around the smart car, and then control the
rotation of the two motors according to the detection results in a way
that lock the smart car in a circle drawn in black line.

**2.Flow Chart**

The specific logic of the restricting 4WD smart car is shown in the
table.

<table>
<tbody>
<tr class="odd">
<td>Detection</td>
<td>Line-tracking sensor in the middle</td>
<td>Black line detected: in high level</td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td>White line detected: in low level</td>
</tr>
<tr class="odd">
<td></td>
<td>Line-tracking sensor on the left</td>
<td>Black line detected: in high level</td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td>White line detected: in low level</td>
</tr>
<tr class="odd">
<td></td>
<td>Line-tracking sensor on the right</td>
<td>Black line detected: in high level</td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td>White line detected: in low level</td>
</tr>
<tr class="odd">
<td>Condition</td>
<td>Movement</td>
<td></td>
</tr>
<tr class="even">
<td>All the three line-tracking sensors don’t detect black lines</td>
<td>Move forward</td>
<td></td>
</tr>
<tr class="odd">
<td>Any of the three line-tracking sensors detect black lines</td>
<td><p>Step back</p>
<p>Then rotate left</p></td>
<td></td>
</tr>
</tbody>
</table>

**3.Wiring Diagram**

![](/media/88422b5f1464ad447e28ccbb8c39a8d4.png)

G, V, S1, S2 and S3 of the line tracking sensor are connected to G（GND),
V（VCC), D11, D7 and D8 of the sensor expansion board.

The power is connected to the BAT port

**4.Test Code**

You can drag blocks to edit. Blocks listed below are for your reference

1.  ![](/media/8de1b04be1ba147dd242c66bddeacacc.png)

2.  ![](/media/e48288f5b46e3e1c78489cb9d9b86333.png)

3.  ![](/media/801d176b32bc87904b8545ecf80874fc.png)

4.  ![](/media/6d2182caa9c17435c65ed3ff6c250a01.png)

5.  ![](/media/5aa8407b0ed182b18f227c8e1ec9a0b4.png)

6.  ![](/media/57bace827fac289b0e98eb4773436a1c.png)

Complete Test Code

![](/media/81bbee811546c34e845fc372c89fdaef.png)

![](/media/a42ec602a6d61f30b5dd0970309e18c4.png)

**5.Test Result**

After successfully uploading the code to the V4.0 board, connect the
wirings according to the wiring diagram, power on the external power
then turn the DIP switch to ON. Put the smart car in the black circle,
then it will move solely in the circle.
