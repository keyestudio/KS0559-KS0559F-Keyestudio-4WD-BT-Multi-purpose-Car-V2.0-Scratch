# Project 12 Ultrasonic Following Smart Car

![](/media/a3beaada39eb1471b7df6d9788e2bea3.png)

**1.Description**

In this project, we will look to detect the distance between the 4WD
smart car and the obstacles ahead through an ultrasonic sensor to drive
two motors in a way that make the car move and make the 8\*8 LED board
show a smile facial pattern.

**2.Flow Chart**

<table>
<tbody>
<tr class="odd">
<td>Detection</td>
<td>Measured distance of front obstacles</td>
<td>distance（unit：cm）</td>
</tr>
<tr class="even">
<td>Setting</td>
<td>8*16 LED board shows a smile pattern.</td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td>Set servo to 90°</td>
<td></td>
</tr>
<tr class="even">
<td>Condition</td>
<td>distance≥20 and distance≤50</td>
<td></td>
</tr>
<tr class="odd">
<td>Status</td>
<td>Go forward</td>
<td></td>
</tr>
<tr class="even">
<td>Condition</td>
<td>distance＞10 and distance＜20</td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td>distance＞50</td>
<td></td>
</tr>
<tr class="even">
<td>Condition</td>
<td>stop</td>
<td></td>
</tr>
<tr class="odd">
<td>Condition</td>
<td>distance≤10</td>
<td></td>
</tr>
<tr class="even">
<td>Condition</td>
<td>Go back</td>
<td></td>
</tr>
</tbody>
</table>

**3.Wiring Diagram**

![](/media/568a66655a14dd34afd8cb1e6ae5951c.png)

Wiring up：

1\. GND, VCC, SDA and SCL of the 8\*8 LED board are connected to G（GND),
V（VCC), A4 and A5 of the expansion board.

2\. VCC, Trig, Echo and Gnd of the ultrasonic sensor are connected to
5V(V), D12(S), D13(S) and Gnd(G)

3\. The servo is connected to G, V and A3. The brown wire is interfaced
with Gnd(G), the red wire is interfaced with 5V(V) and the orange wire
is interfaced with A3.

4\. The power is connected to the BAT port

**4.Test Code**

Before writing the code, it is necessary to import the library files of
the ultrasonic sensor, 8x16 LED board and the servo. The specific steps
are as follows: 

Click ![](/media/9964e0b31fc9846a7f64c57f51e47152.png)to enter the extension library interface of
sensors/modules/components, then search
for“Ultrasonic”sensor![](/media/e3485f63f426d9a126afa3c95c3b0be8.png)and click it. In this
way, "Not loaded" changes to "loaded", indicating that
the“Ultrasonic”sensor was added successfully. 

![](/media/cba9add907a200ae92f7a5cf2ef3df56.png)

The 8x16 LED board and servo library files are added in the same way as
the ultrasonic sensor.

Click ![](/media/29916972665d35bfb34914b6144e28aa.png)to return to the code editor interface, the
instruction block of the added “Ultrasonic”sensor,“Matrix 8\*16”module
and “Servo”component can be seen in the module area. 

![](/media/9fafe2ef7b999b200d6de6e40bc5cdc0.png)

You can drag blocks to edit. Blocks listed below are for your reference

1.  ![](/media/8de1b04be1ba147dd242c66bddeacacc.png)

2.  ![](/media/f6fb93211f786d023eb77eb210eae454.png)

3.  ![](/media/b8cd07dc2e6c7b02feaf0f5c77663d79.png)

4.  ![](/media/904732a3bfdb65a5ef0207d40b3abcc6.png)

5.  ![](/media/5aa8407b0ed182b18f227c8e1ec9a0b4.png)

6.  ![](/media/73a12c947f4323aea6152cf9c88116f4.png)

7.  ![](/media/72f725bac7ba927b55e3a9eea3b1a660.png)

8.  ![](/media/7fa69de5a88479434d48a38b7c9bc300.png)

9.  ![](/media/e620ad9d563aa29f9aa9d84ddf9f4f14.png)

Complete Test Code

![](/media/6b8a4a730d002c413b8bd657af1e6b80.png)

![](/media/3cca3162c3e9e49924dba6a5ce5bb130.png)

![](/media/47a1afdd6798deef89bfa827147faf01.png)

**5.Test Result**

After successfully uploading the code to the V4.0 board, connect the
wirings according to the wiring diagram, power on the external power
then turn the DIP switch to ON. Set the servo to 90°，the smart car will
move with the obstacles and the 8X16 LED board will show“smile”.
