# Project 14 IR Remote Control Smart Car

![](/media/ff2fec813f8765e1bcd593b37b9c0a4f.jpeg)

**1. Description**

In this project, we will make an IR remote control smart car and press the button on the IR remote control to drive the car to move.

**2. Flow Chart**

**The specific logic of IR remote control smart car is shown below:**

<table>
<tbody>
<tr class="odd">
<td><strong>Initial setup</strong></td>
<td>LED board displays smile face</td>
<td></td>
</tr>
<tr class="even">
<td>Remote control</td>
<td>Key value</td>
<td>Key state</td>
</tr>
<tr class="odd">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/b11dc5ffa6cccebc6088e5d557d76daf.png" style="width:0.57292in;height:0.61458in" /></td>
<td>FF629D</td>
<td>Go front</td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td>8*8 LED board shows front icon</td>
</tr>
<tr class="odd">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/ae8110034aacb083151cfd882ee599ba.png" style="width:0.57292in;height:0.58333in" /></td>
<td>FFA857</td>
<td>Back</td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td>8*8 LED board shows back icon</td>
</tr>
<tr class="odd">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/bce9cba2c6d2465fbcce570ad4210eba.png" style="width:0.5625in;height:0.58333in" /></td>
<td>FF22DD</td>
<td>Rotate to left</td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>8*8 LED board shows</p>
<p>leftward icon</p></td>
</tr>
<tr class="odd">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/ad907a618af86f30d52986bbbd57ba76.png" style="width:0.5625in;height:0.57292in" /></td>
<td>FFC23D</td>
<td>Rotate to right</td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td>8*8 LED board shows rightward icon</td>
</tr>
<tr class="odd">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/9716a4ed61a4064d2f47a7b73eccaf87.png" style="width:0.5625in;height:0.54167in" /></td>
<td>FF02FD</td>
<td>Stop</td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td>8*8 LED board shows“STOP”</td>
</tr>
</tbody>
</table>
**3. Wiring Diagram**

![](/media/9d8b58dff14fe22b5c87514db944530c.png)

1.  GND, VCC, SDA and SCL of the 8\*8 LED board module are connected to G（GND), V（VCC), A4 and A5 of the expansion board.
    
2.  As the IR receiver is integrated on the 8833 motor driver expansion board, there is no need for additional wiring. The pins of the IR receiver on the 8833 board are G (GND), V (VCC) and D3 respectively. 
    
2.  The servo is connected to G, V and A3. The brown wire is interfaced with Gnd(G), the red wire is interfaced with 5V(V) and
    the orange wire is interfaced with A3.
    
2.  The power is connected to the BAT port
    
    **4. Test Code**
    
    Before writing the code, it is necessary to import the library files of the ultrasonic sensor, 8x16 LED board and the servo. The specific steps are as follows: 
    
    Click ![](/media/9964e0b31fc9846a7f64c57f51e47152.png)to enter the extension library interface of sensors/modules/components, then search for“ir remote”sensor![](/media/229086011fb4f87f3a882e514b043bb7.png)and click it. In this way, "Not loaded" changes to "loaded", indicating that the“ir remote”sensor was added successfully. 
    
    ![](/media/52ed0e6f7d436d17d18168c4704f5e98.png)

Click ![](/media/29916972665d35bfb34914b6144e28aa.png)to return to the code editor interface, the instruction block of the added “ir remote”sensor,“Matrix 8\*16”module and “Servo”component can be seen in the module area. 

![](/media/2fc4d2dc95c4936f1ef5a9f56444b88c.png)

You can drag blocks to edit. Blocks listed below are for your reference

1.  ![](/media/8de1b04be1ba147dd242c66bddeacacc.png)

2.  ![](/media/1f98f44522f0d08b8d41a81109f91bee.png)

3.  ![](/media/a9042e77ebe3009fbb7653bef3429b66.png)

4.  ![](/media/53c2dbc1af206a888f95f58b31000ab2.png)

5.  ![](/media/b8cd07dc2e6c7b02feaf0f5c77663d79.png)

6.  ![](/media/51e30aa2aca3a7da67ee4f0f81c7dad1.png)

7.  ![](/media/7fa69de5a88479434d48a38b7c9bc300.png)

8.  ![](/media/da0a6a378abbd5fd3a4a3466ceaa37c9.png)

Complete Test Code

![](/media/52a61de1aca0ddeaac1baf364cc4e3fb.png)

![](/media/a16017d78df50d09931e6f1261b6154c.png)

![](/media/1587c67c0425bca672078700dd14460f.png)

![](/media/1a02d997bed11414cabc4a02eb3c3009.png)

![](/media/14247d440f27c4a4d5e682e7aadf36e9.png)

**5. Test Result**

After successfully uploading the code to the V4.0 board, connect the wirings according to the wiring diagram, power on the external power then turn the DIP switch to ON. Then we enable to use the IR remote control drive the car to move to and the 8X16 LED board will display the corresponding status pattern.
