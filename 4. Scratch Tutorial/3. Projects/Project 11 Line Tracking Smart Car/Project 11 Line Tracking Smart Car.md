# Project 11 Line Tracking Smart Car

![](/media/eff7a15e697e8b78bde391f806ea024d.png)

**1. Description**

Based on the working principle of the line tracking sensor, we empower to make a line tracking smart car.

In this project, we detect whether there is a black line at the bottom of the smart car through a line tracking sensor, and then control the rotation of the two groups of motors according to the detection results in a way that controls the smart car to walk along the black line. 

**2. Flow Chart**

<table>
<tbody>
<tr class="odd">
<td><strong>Detection</strong></td>
<td>Middle tracking sensor</td>
<td>detects black line：HIGH</td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td>detects white line：LOW</td>
</tr>
<tr class="odd">
<td></td>
<td>Left tracking sensor</td>
<td>detects black line：HIGH</td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td>detects white line：LOW</td>
</tr>
<tr class="odd">
<td></td>
<td>Right tracking sensor</td>
<td>detects black line：HIGH</td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td>detects white line：LOW</td>
</tr>
<tr class="odd">
<td><strong>Condition 1</strong></td>
<td><strong>Condition</strong> 2 Detect the left and the right tracking sensor</td>
<td>Status</td>
</tr>
<tr class="even">
<td>Middle tracking sensor detects black line</td>
<td>left tracking sensor detects black line; right sensor detects white line</td>
<td>Turn left</td>
</tr>
<tr class="odd">
<td></td>
<td>left tracking sensor detects white line; right sensor detects black line</td>
<td>Turn right</td>
</tr>
<tr class="even">
<td></td>
<td>left and right tracking sensor detect black line</td>
<td>Advance</td>
</tr>
<tr class="odd">
<td></td>
<td>left and right tracking sensor detect white line</td>
<td>Advance</td>
</tr>
<tr class="even">
<td>Middle tracking sensor detects white line</td>
<td>left tracking sensor detects black line; right sensor detects white line</td>
<td>Turn left</td>
</tr>
<tr class="odd">
<td></td>
<td>left tracking sensor detects white line; right sensor detects black line</td>
<td>Turn right</td>
</tr>
<tr class="even">
<td></td>
<td>left and right tracking sensor detect black line</td>
<td>Stop</td>
</tr>
<tr class="odd">
<td></td>
<td>left and right tracking sensor detect white line</td>
<td>Stop</td>
</tr>
</tbody>
</table>
**3. Wiring Diagram**

![](/media/88422b5f1464ad447e28ccbb8c39a8d4.png)

G, V, S1, S2 and S3 of the line tracking sensor are connected to G（GND), V（VCC), D11, D7 and D8 of the sensor expansion board.

The power is connected to the BAT port

**4. Test Code**

You can drag blocks to edit. Blocks listed below are for your reference

1.  ![](/media/8de1b04be1ba147dd242c66bddeacacc.png)

2.  ![](/media/e4033e0b7378d3c8b30a40b9d4d2aa36.png)

3.  ![](/media/5091e131d3b5c2f217fbf82e6a4ad079.png)

4.  ![](/media/5aa8407b0ed182b18f227c8e1ec9a0b4.png)

5.  ![](/media/fec93c7b8b089de709fd50575931519c.png)

Complete Test Code

![](/media/9290b200fe56d3b00574a52e803c4cbf.png)

![](/media/1dc3a946cf6a26057317c29229cf1233.png)

![](/media/abd0d4efc97cc05c7a1eb843ffb1ed92.png)

**5. Test Result**

After successfully uploading the code to the V4.0 board, connect the wirings according to the wiring diagram, power on the external power then turn the DIP switch to ON. Then the smart car will walk along the lines.
