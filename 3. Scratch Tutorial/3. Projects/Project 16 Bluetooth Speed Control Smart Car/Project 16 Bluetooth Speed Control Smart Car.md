# Project 16 Bluetooth Speed Control Smart Car

![](/media/8abdadfa2fc462bdcc0542df52a793e3.jpeg)

**1.Description**

In this project, we will use a Bluetooth to adjust the speed of the
smart car. We empower to define a variable speeds and change it to
change the speed of the smart car. 

**2.Flow Chart**

![](/media/90ab1f7fb1e16ad3c018b1c631e407c3.png)

**3.Wiring Diagram**

![](/media/61be6959693b2111639252ea45ec60fc.png)

1\. GND, VCC, SDA and SCL of the 8\*8 LED board are connected to G（GND),
V（VCC), A4 and A5 of the expansion board.

2\. The RXD, TXD, GND and VCC of the Bluetooth module are respectively
connected to TX, RX, G and 5V on the 8833 motor driver expansion board,
while the STATE and BRK pins of the Bluetooth module do not need to be
connected. 

3\. The servo is connected to G, V and A3. The brown wire is interfaced
with Gnd(G), the red wire is interfaced with 5V(V) and the orange wire
is interfaced with A3.

4\. The power is connected to the BAT port

**4.Test Code**

Before writing the code, it is necessary to import the library files of
the 8x16 LED board and the servo. The specific steps are as follows: 

Click ![](/media/9964e0b31fc9846a7f64c57f51e47152.png)to enter the extension library interface of
sensors/modules/components, then search for“Matrix 8\*16
Aip1640”module![](/media/8637cbe988d4acbada4ed934b7064a42.png)and click it. In this way, "Not
loaded" changes to "loaded", indicating that the“Matrix 8\*16
Aip1640”module was added successfully. 

![](/media/127e14cd4e1988b0a21bb028de41bf76.png)

Click ![](/media/29916972665d35bfb34914b6144e28aa.png)to return to the code editor interface, the
instruction block of the added “Matrix 8\*16”module and “Servo”component
can be seen in the module area. 

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

10. ![](/media/37331f93041cde6c67777b6abc0ad7ac.png)

Complete Test Code

![](/media/fe904a2480da446815f201fc6d783029.png)

![](/media/8d6b30a178ab478105856f7db29d8168.png)

![](/media/e359e96c51ebd3377489c73adc2776f8.png)

![](/media/7294805d8e3090ed73593ac11403b124.png)

![](/media/5e6fad3605ecb86468fe88574fc0c7ad.png)

![](/media/5e6fad3605ecb86468fe88574fc0c7ad.png)

**5.Test Result**

After successfully uploading the code to the V4.0 board, connect the
wirings according to the wiring diagram, power on the external power
then turn the DIP switch to ON. Pairing the APP with Bluetooth, the
smart car can be controlled to move by the APP.

Press![](/media/049343f587e0e7cf19fe8b665d735321.png), the car will speed up, press
![](/media/264f77cce6018584b54f46676fee4247.png), the car will slow down, and the 8\*16 LED board
will display the corresponding status pattern of the smart car.

Before uploading the test code, you need to remove the Bluetooth module,
otherwise the code will fail to be uploaded.  Connect the Bluetooth
module after uploading the code successfully.
