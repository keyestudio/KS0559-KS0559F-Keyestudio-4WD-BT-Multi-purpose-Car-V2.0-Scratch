# Project 13 Ultrasonic Obstacle Avoidance Smart Car

![](/media/fd4044796307f709987b9d2e215e0911.png)

**1. Description**

In this project, we aim to make an ultrasonic obstacle avoidance smart car. We will use the ultrasonic to detect the distance from the obstacle, which can be used to control the servo to rotate so as to make the car move. Meanwhile, the 8X16 LED board will display the corresponding status pattern.

**2. Flow Chart**

**The specific logic of ultrasonic obstacle avoidance smart car is shown below:**

<table>
<tbody>
<tr class="odd">
<td>Detection</td>
<td><p>measured distance of front obstacle</p>
<p>set servo to 90°</p></td>
<td>distance（unit：cm）</td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td>measured distance of left obstacle（set servo to 160°）</td>
<td>a1（unit：cm）</td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>measured distance of right obstacle</p>
<p>（set servo to 20°）</p></td>
<td>a2（unit：cm）</td>
<td></td>
</tr>
<tr class="even">
<td>Setting</td>
<td>set the initial angle of servo to 90°</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>Condition1</td>
<td>Status</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>a＜20</td>
<td>Stop for 1000ms；set the angle of servo to 160°，read a1，delay in 500ms；set the angle of servo to 20°，read a2，delay in 500ms</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td>Condition 2</td>
<td>Status</td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>a1＜50</p>
<p>or</p>
<p>a2＜50</p></td>
<td>Compare a1and a2</td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td>Condition 3</td>
<td>Status</td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td>a1＞a2</td>
<td>Set the angle of servo to 90°，rotate to left for 700ms and go front</td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td>a1＜a2</td>
<td>Set the angle of servo to 90°，rotate to right for 700ms, go front</td>
</tr>
<tr class="even">
<td></td>
<td>Condition 2</td>
<td>Status</td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>a1≥50</p>
<p>and</p>
<p>a2≥50</p></td>
<td>Random</td>
<td>Set the angle of servo to 90°，rotate to left for 700ms and go front</td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td>Set the angle of servo to 90°，rotate to right for 700ms, go front</td>
</tr>
<tr class="odd">
<td>Condition1</td>
<td>Status</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>a≥20</td>
<td>Go forward</td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

\`

**3. Wiring Diagram**

![](/media/568a66655a14dd34afd8cb1e6ae5951c.png)

1\. GND, VCC, SDA and SCL of the 8\*8 LED board module are connected to G（GND), V（VCC), A4 and A5 of the expansion board.

2\. VCC, Trig, Echo and Gnd of the ultrasonic sensor are connected to 5V(V), D12(S), D13(S) and Gnd(G)

3\. The servo is connected to G, V and A3. The brown wire is interfaced with Gnd(G), the red wire is interfaced with 5V(V) and the orange wire is interfaced with A3.

4\. The power is connected to the BAT port

**4. Test Code**

Before writing the code, it is necessary to import the library files of the ultrasonic sensor , 8x16 LED board and the servo. The specific steps are as follows: 

Click ![](/media/9964e0b31fc9846a7f64c57f51e47152.png)to enter the extension library interface of
sensors/modules/components, then search for “Ultrasonic” sensor![](/media/e3485f63f426d9a126afa3c95c3b0be8.png)and click it. In this way, "Not loaded" changes to "loaded", indicating that the“Ultrasonic”sensor was added successfully. 

![](/media/cba9add907a200ae92f7a5cf2ef3df56.png)

Click ![](/media/29916972665d35bfb34914b6144e28aa.png)to return to the code editor interface, the instruction block of the added “Ultrasonic”sensor,“Matrix 8\*16”module and “Servo”component can be seen in the module area. 

![](/media/9fafe2ef7b999b200d6de6e40bc5cdc0.png)

You can drag blocks to edit. Blocks listed below are for your reference

1.  ![](/media/8de1b04be1ba147dd242c66bddeacacc.png)

2.  ![](/media/5dcbd405806b8e341505d7316246dbdd.png)

3.  ![](/media/996c8d4e5dd9620757dfb097329e7d5d.png)

4.  ![](/media/b8cd07dc2e6c7b02feaf0f5c77663d79.png)

5.  ![](/media/904732a3bfdb65a5ef0207d40b3abcc6.png)

6.  ![](/media/5aa8407b0ed182b18f227c8e1ec9a0b4.png)

7.  ![](/media/73a12c947f4323aea6152cf9c88116f4.png)

8.  ![](/media/e620ad9d563aa29f9aa9d84ddf9f4f14.png)

9.  ![](/media/72f725bac7ba927b55e3a9eea3b1a660.png)

10. ![](/media/7fa69de5a88479434d48a38b7c9bc300.png)

Complete Test Code

![](/media/485126683555be4840a1aa5c0cd2dad7.png)

![](/media/fe5ec565a0cf02d27877820176df3c70.png)

![](/media/29e0fc7d438de2dcc0731b7079b697b6.png)

![](/media/f59de27be3bf0146487d9f7b0ad32e8c.png)

**5. Test Result**

After successfully uploading the code to the V4.0 board, connect the wirings according to the wiring diagram, power on the external power then turn the DIP switch to ON.

The smart car moves forward and automatically avoids obstacles. When there is no road ahead, the servo will drive the ultrasonic sensor to scan the left, middle and right distances, and the car will turn to the open side. Meanwhile, the 8X16 LED board will display the corresponding status pattern.
