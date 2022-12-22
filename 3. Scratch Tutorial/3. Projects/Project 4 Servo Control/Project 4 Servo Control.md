# Project 4 Servo Control

**1.Description**

![](/media/8dd66d175b0611c729f696cc1c8b773c.jpeg)Servo motor is a position control rotary
actuator. It mainly consists of a housing, a circuit board, a core-less
motor, a gear and a position sensor. Its working principle is that the
servo receives the signal sent by MCUs or receivers and produces a
reference signal with a period of 20ms and width of 1.5ms, then compares
the acquired DC bias voltage to the voltage of the potentiometer and
obtain the voltage difference output.

![](/media/7ecb524389b2518fe48035c8c220f8f9.png)In general, servo has three lines in brown, red
and orange. The brown wire is grounded, the red one is a positive pole
line and the orange one is a signal line.

The rotation angle of servo motor is controlled by regulating the duty
cycle of PWM (Pulse-Width Modulation) signal. The standard cycle of PWM
signal is 20ms (50Hz). Theoretically, the width is distributed
between 1ms-2ms, but in fact, it's between 0.5ms-2.5ms. The width
corresponds the rotation angle from 0° to 180°. But note that for
different brand motors, the same signal may have different rotation
angles. 

![](/media/49467dfa70799401a5a5acc691014aee.png)

The corresponding servo angles are shown below:

![](/media/ddc74f62dc936c925d28d70a1a9c2214.png)

**2.Specification**

  - Working voltage: DC 4.8V \~ 6V

  - Operating angle range: about 180 ° (at 500 → 2500 μsec)

  - Pulse width range: 500 → 2500 μsec

  - No-load speed: 0.12 ± 0.01 sec / 60 (DC 4.8V) 0.1 ± 0.01 sec / 60
    (DC 6V)

  - No-load current: 200 ± 20mA (DC 4.8V) 220 ± 20mA (DC 6V)

  - Stopping torque: 1.3 ± 0.01kg · cm (DC 4.8V) 1.5 ± 0.1kg · cm (DC
    6V)

  - Stop current: ≦ 850mA (DC 4.8V) ≦ 1000mA (DC 6V)

  - Standby current: 3 ± 1mA (DC 4.8V) 4 ± 1mA (DC 6V)

**3.Components**

<table>
<tbody>
<tr class="odd">
<td>Keyestudio 4.0 Development Board *1</td>
<td>Keyestudio 8833 Motor Driver Expansion Board *1</td>
<td>Servo*1</td>
</tr>
<tr class="even">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/6131c8d782756fe051b0ef0210a76d03.png" style="width:1.27292in;height:0.91875in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/5e291db96125e27f380e8caf79e8015a.png" style="width:1.09375in;height:0.95625in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/8dd66d175b0611c729f696cc1c8b773c.jpeg" style="width:1.5in;height:1.25in" /></td>
</tr>
<tr class="odd">
<td>18650 Battery Holder*1</td>
<td>USB Cable*1</td>
<td>18650 Battery*2（self-provided）</td>
</tr>
<tr class="even">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/635b8724dc3e7a27f940b3953ed4536d.jpeg" style="width:1.17708in;height:0.59514in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/4f8d5af6dee9016b45d975adb2391d37.png" style="width:1.22986in;height:0.45486in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/a71e914713386795b1ea73826bec6c86.jpeg" style="width:0.45764in;height:1.25417in" /><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/a71e914713386795b1ea73826bec6c86.jpeg" style="width:0.42292in;height:1.15833in" /></td>
</tr>
</tbody>
</table>

**4.Wiring Diagram**

![](/media/3220a5b142da47a3473390a8a04ce35e.png)

Wiring note: The servo is connected to G（GND）、V（VCC）and A3, the brown
line of servo is linked with Gnd(G), the red one is connected to 5v(V)
and the orange one is attached to A3.

The servo is obliged to connect to the external power due to its high
demand for driving servo current. Generally, the current of development
board is not big enough. If without connecting the external power, the
development board could be burnt.

**5.Test Code**

Before writing the code, it is necessary to import the servo library
file. The specific steps are as follows: 

Click ![](/media/9964e0b31fc9846a7f64c57f51e47152.png)to enter the extension library interface of
sensors/modules/components, then look for "Servo"![](/media/cdc90dd33e0419b3b7744f57fa0749b9.png)
component and click it. In this way, "Not Loaded" changes to "loaded",
indicating that "Servo" component was added successfully. 

![](/media/df2c1b5606accfcb3cdde0c3a0107d29.png)

Click ![](/media/29916972665d35bfb34914b6144e28aa.png)to go back to the code editor, and in the
modules area you can see the "Servo" component directive block added. 

![](/media/7ebbbdaaff4897c1968285ef51dca6f3.png)

You can drag blocks to edit. Blocks listed below are for your

1.  ![](/media/5b04350e0310955ee2ecd48338f556a3.png)

2.  ![](/media/7dd97d17b785de17e6c9362fa32e2a74.png)

3.  ![](/media/69724a2063fa25e0f142e1eb48efd40f.png)

4.  ![](/media/e149b45054fe94196dea220b319cb0bf.png)

Complete Test Code

![](/media/cd9c5bf92fa92f6276eadfcf888011c6.png)

**6.Test Result**

After successfully uploading the code to the V4.0 board, connect the
wirings according to the wiring diagram, and power on the external
power. After powering on, turn the dip switch to the "ON" end, then
servo will swing in the range of 0° to 180°.
