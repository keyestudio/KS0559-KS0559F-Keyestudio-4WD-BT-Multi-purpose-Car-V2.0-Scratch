# Project 15 Bluetooth Control Smart Car

![](/media/8abdadfa2fc462bdcc0542df52a793e3.jpeg)

**1. Description**

We’ve learned the basic knowledge of Bluetooth. And in this lesson, we will make a Bluetooth control smart car. In this project, we aim to regard the mobile phone as the transmitter (host), and the smart car connected to the BT24 Bluetooth module (slave) as the receiver and use the mobile APP to control the smart car via the Bluetooth. 

**2. APP Control Button**

<table>
<tbody>
<tr class="odd">
<td>Key</td>
<td>Function</td>
<td></td>
</tr>
<tr class="even">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/3b4076135ebca73f47c4ff8d7785dc17.png" style="width:0.86736in;height:0.29514in" /></td>
<td>Pair the DX-BT24 5.1 Bluetooth module</td>
<td></td>
</tr>
<tr class="odd">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/3b4076135ebca73f47c4ff8d7785dc17.png" style="width:0.99653in;height:0.28403in" /></td>
<td>Disconnect Bluetooth</td>
<td></td>
</tr>
<tr class="even">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/3b4076135ebca73f47c4ff8d7785dc17.png" style="width:0.46806in;height:0.48611in" /></td>
<td>Control Character</td>
<td>Function</td>
</tr>
<tr class="odd">
<td></td>
<td><p>Press: F</p>
<p>Release: S</p></td>
<td>Press the button, the car goes front; release to stop</td>
</tr>
<tr class="even">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/3b4076135ebca73f47c4ff8d7785dc17.png" style="width:0.46875in;height:0.46597in" /></td>
<td><p>Press: L</p>
<p>Release: S</p></td>
<td>Press the button, the car turns left; release to stop</td>
</tr>
<tr class="odd">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/3b4076135ebca73f47c4ff8d7785dc17.png" style="width:0.45069in;height:0.46736in" /></td>
<td><p>Press: R</p>
<p>Release: S</p></td>
<td>Press the button, the car turns right; release to stop</td>
</tr>
<tr class="even">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/3b4076135ebca73f47c4ff8d7785dc17.png" style="width:0.45208in;height:0.475in" /></td>
<td><p>Press: B</p>
<p>Release: S</p></td>
<td>Press the button, the car goes back; release to stop</td>
</tr>
<tr class="odd">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/049343f587e0e7cf19fe8b665d735321.png" style="width:0.95833in;height:0.52153in" /></td>
<td><p>Press: a</p>
<p>Release: S</p></td>
<td>Click to speed up，255(maximum)</td>
</tr>
<tr class="even">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/264f77cce6018584b54f46676fee4247.png" style="width:0.96875in;height:0.53819in" /></td>
<td><p>Press: d</p>
<p>Release: S</p></td>
<td>Click to slow down，0(minimum)</td>
</tr>
<tr class="odd">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/3b4076135ebca73f47c4ff8d7785dc17.png" style="width:0.59931in;height:0.59514in" /></td>
<td>Click to start the mobile phone gravity sensing; click again to exit</td>
<td></td>
</tr>
<tr class="even">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/98b616f6b64e044150932624040ba20b.png" style="width:0.59097in;height:0.61319in" /></td>
<td>Click to send X, click again to send S</td>
<td>Start line tracking function; click again to exit</td>
</tr>
<tr class="odd">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/84d5bb67fc8d6dfcc2aa950adc71dd21.png" style="width:0.59028in;height:0.6125in" /></td>
<td>Click to send Y, click again to send S</td>
<td>Start obstacle avoidance function, click again to exit</td>
</tr>
<tr class="even">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/070f44577bcc6532cda2d9fdcfaf455f.png" style="width:0.59028in;height:0.64653in" /></td>
<td>Click to send U, click again to send S</td>
<td>Start ultrasonic follow function; click again to exit</td>
</tr>
<tr class="odd">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/6eed80e22c0b1264f2407fc6a5e93af2.png" style="width:0.56597in;height:0.64583in" /></td>
<td>Click to send G, click again to send S</td>
<td>Start restricting function; click again to exit</td>
</tr>
</tbody>
</table>
**3. Flow Chart**

![img](media/wps1.png)

**4. Wiring Diagram**

![](/media/61be6959693b2111639252ea45ec60fc.png)

1.  GND, VCC, SDA and SCL of the 8\*8 LED board are connected to G（GND), V（VCC), A4 and A5 of the expansion board.
    
1.  The RXD, TXD, GND and VCC of the Bluetooth module are respectively connected to TX, RX, G and 5V on the 8833 motor driver expansion board, while the STATE and BRK pins of the Bluetooth module do not need to be connected. 
    
1.  The servo is connected to G, V and A3. The brown wire is interfaced with Gnd(G), the red wire is interfaced with 5V(V) and
    the orange wire is interfaced with A3.
    
1.  The power is connected to the BAT port
    
    
    
    **5. Test Code**
    
    Before writing the code, it is necessary to import the library files of the 8x16 LED board and the servo. The specific steps are as follows: 
    
    Click ![](/media/9964e0b31fc9846a7f64c57f51e47152.png)to enter the extension library interface of sensors/modules/components, then search for“Matrix 8\*16 Aip1640”module![](/media/8637cbe988d4acbada4ed934b7064a42.png)and click it. In this way, "Not loaded" changes to "loaded", indicating that the“Matrix 8\*16 Aip1640”module was added successfully. 
    
    ![](/media/127e14cd4e1988b0a21bb028de41bf76.png)

Click ![](/media/29916972665d35bfb34914b6144e28aa.png)to return to the code editor interface, the instruction block of the added“Matrix 8\*16”module and “Servo”component can be seen in the module area. 

![](/media/3e43fa27a995102b75b521bee5f118f6.png)

You can drag blocks to edit. Blocks listed below are for your reference

1.  ![](/media/8de1b04be1ba147dd242c66bddeacacc.png)

2.  ![](/media/1f98f44522f0d08b8d41a81109f91bee.png)

3.  ![](/media/3b4fb768cbf7e0b80fa55cb15aa932b7.png)

4.  ![](/media/53c2dbc1af206a888f95f58b31000ab2.png)

5.  ![](/media/b8cd07dc2e6c7b02feaf0f5c77663d79.png)

6.  ![](/media/7dfb5907a76ed97c980b6ab043fdd8e5.png)

7.  ![](/media/7edfd4978b8054c947ff3dadc915a9fb.png)

8.  ![](/media/5aa8407b0ed182b18f227c8e1ec9a0b4.png)

9.  ![](/media/fe7a594ea953fcfd3353c49f0f83fd3c.png)

Complete Test Code

![](/media/af401ffdf3c22fd7e94ec4d68b2cce0e.png)

![](/media/93c60a97940e572229ac88dced00d442.png)

![](/media/9437030ddd7deae4f086926104f25231.png)

![](/media/7d882ac05c9378e794eafe09d5878c99.png)

![](/media/fa1637ec96ae350fd72f7e1384ad31c5.png)

**6. Test Result**

After successfully uploading the code to the V4.0 board, connect the wirings according to the wiring diagram, power on the external power then turn the DIP switch to ON.

Inset the BT module and open your cellphone to connect the Bluetooth to control the smart car. The can will move forward, backward, turn left and right and stop. Also the 8\*8 LED board will show the corresponding pattern.

Remove the BT module when you are uploading the code, otherwise you will fail to upload it.
