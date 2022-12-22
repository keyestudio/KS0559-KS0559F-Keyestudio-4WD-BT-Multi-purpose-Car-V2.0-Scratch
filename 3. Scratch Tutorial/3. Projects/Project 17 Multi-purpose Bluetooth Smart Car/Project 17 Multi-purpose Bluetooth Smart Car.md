# Project 17 Multi-purpose Bluetooth Smart Car

![](/media/2c1198e0ebd7c31622b7438469fb572c.jpeg)

**1.Description**

In previous projects, the car only performs a single function. However,
in this lesson, we will integrate all of its functions via a Bluetooth.

**2.Flow Chart**

![](/media/73f4da1e321bc29282d3b2f5cb3168dd.png)

**3.Wiring Diagram**

![](/media/fce8edd349ddbcfe02e6f27feb73e90f.png)

1\. GND, VCC, SDA and SCL of the 8\*8 LED board are connected to G（GND),
V（VCC), A4 and A5 of the expansion board.

2\. The RXD, TXD, GND and VCC of the Bluetooth module are respectively
connected to TX, RX, G and 5V on the 8833 motor driver expansion board,
while the STATE and BRK pins of the Bluetooth module do not need to be
connected. 

3\. The servo is connected to G, V and A3. The brown wire is interfaced
with Gnd(G), the red wire is interfaced with 5V(V) and the orange wire
is interfaced with A3.

4\. G, V, S1, S2 and S3 of the line tracking sensor are connected to
G（GND), V（VCC), D11, D7 and D8 of the sensor expansion board.

5\. VCC, Trig, Echo and Gnd of the ultrasonic sensor are connected to
5V(V), D12(S), D13(S) and Gnd(G)

6\. The power is connected to the BAT port

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

Click ![](/media/29916972665d35bfb34914b6144e28aa.png)to return to the code editor interface, the
instruction block of the added “Ultrasonic”sensor,“Matrix 8\*16”module
and “Servo”component can be seen in the module area. 

![](/media/9fafe2ef7b999b200d6de6e40bc5cdc0.png)

Complete Test Code

![](/media/7acbfe6b628a17d114f2195b80d35de3.png)

**5.Test Result**

After successfully uploading the code to the V4.0 board, connect the
wirings according to the wiring diagram, power on the external power
then turn the DIP switch to ON.

After the Bluetooth module is plugged into the APP and the mobile APP is
successfully connected to the Bluetooth, the smart car can be controlled
by the mobile APP.  We can achieve the corresponding functions by
pressing the corresponding buttons on the mobile APP. 

Before uploading the test code, you need to remove the Bluetooth module,
otherwise the code will fail to be uploaded.  Connect the Bluetooth
module after uploading the code successfully.
