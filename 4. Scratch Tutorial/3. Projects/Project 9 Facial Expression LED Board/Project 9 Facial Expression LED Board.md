# Project 9 Facial Expression LED Board



![](/media/7d4e720c582dfaaeb730f284fd93ca6b.png)

**1. Description** 

How fun it is if a expression board is added to the robot. And the Keyestudio 8\*16 LED board can do the trick. With the help of it, you could design facial expressions, images, patterns and other displays by yourselves.

The 8\*16 LED board comes with 128 LEDs. The data of the microprocessor(Arduino) communicates with the AiP1640 through a two-wire bus interface. Therefore, it can control the on and off of 128 LEDs on the module, so as to make the dot matrix on the module to display the pattern you need. A HX-2.54 4Pin cable is provided for your convenience of wiring.

**2. Specification**

  - Working voltage: DC 3.3-5V

  - Power loss: 400mW

  - Oscillation frequency: 450KHz

  - Drive current: 200mA

  - Working temperature: -40\~80℃

  - Communication mode: I2C
    
    **3. Circuit Diagram**

![](/media/edf6c77d05904eebbaa89d557e9e9c1a.png)

**4. Working Principle**

How to control each LED of the 8\*16 dot matrix? It is known that each byte has 8 bits and each bit is 0 or 1. when it is 0, LED is off while when it is 1 LED is on. One byte can control one column of the LED,and naturally 16 bytes can control 16 columns of LEDs, that’s the 8\*16 dot matrix.

**Pins description and communication protocol**

The data of the microprocessor (Arduino) communicates with the AiP1640 through a two-wire bus cable.

The communication protocol diagram is as follows (SCLK) is SCL, (DIN) is SDA.

![](/media/ea2bab37f23c09453c680590b84653d6.png)

①The starting condition for data input: SCL is high level and SDA changes from high to low.

②For data command setting, there are methods as shown in the figure below.

In our sample program, select the way to **add 1 to the address automatically**, the binary value is 0100 0000 and the corresponding hexadecimal value is 0x40.

<table>
<tbody>
<tr class="odd">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/7e326d7edc877ea2509cbf8649f82d99.png" style="width:5.60972in;height:1.94306in" /></td>
</tr>
</tbody>
</table>

③For address command setting, the address can be selected as shown below.

The first 00H is selected in our sample program, and the binary number 1100 0000 corresponds to the hexadecimal 0xc0.

<table>
<tbody>
<tr class="odd">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/e6da87c9f6056f849c973edec5456f3e.png" style="width:4.53056in;height:3.70069in" /></td>
</tr>
</tbody>
</table>

④The requirement for data input is that when SCL is at high level when inputting data, the signal on SDA must remain unchanged. Only when the clock signal on SCL is at low level, can the signal on SDA be changed. The input of data is the low bit first, and the high bit later.

⑤The condition for the end of data transmission is that when SCL is at low level, SDA at low level and SCL at high level, the level of SDA becomes high.

⑥Display control, set different pulse width, pulse width can be selected as shown in the figure below

In the example, the pulse width is 4/16, and the hexadecimal corresponding to 1000 1010 is 0x8A

<table>
<tbody>
<tr class="odd">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/ad238f413988f77bcf074a5642a5061d.png" style="width:6.6in;height:2.95556in" /></td>
</tr>
</tbody>
</table>

**Instructions for the use of modulus tool**

The dot matrix tool uses the online version, and the link is :http://dotmatrixtool.com/\#

①Enter the link and the page appears as shown below

![](/media/354693b5679a2615c62e99b7025d6355.png)

②The dot matrix is 8\*16, so adjust the height to 8 and width to 16, as shown in the figure below

![](/media/5f0278d66ade370e871b447d360d6e7b.png)

③Generate hexadecimal data from the pattern

As shown in the figure below, press the left mouse button to select, right click to cancel; draw the pattern you want, click Generate, and the hexadecimal data we need will be generated.

![](/media/586e88bf13c61b0918046437ed7f6796.png)

**3. Components**

<table>
<tbody>
<tr class="odd">
<td>Keyestudio 4.0 Development Board *1</td>
<td>Keyestudio 8833 Motor Driver Expansion Board *1</td>
<td>Keyestudio 8x16 LED Panel*1</td>
</tr>
<tr class="even">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/0a1b9d802a0c5b268e6d1be462a3254b.png" style="width:1.74097in;height:1.25694in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/b9a74e7634f522d93379112665f936d2.png" style="width:1.58958in;height:1.39028in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/170dd306deacf806cc5e99a381f90f7e.png" style="width:1.74861in;height:0.80278in" /></td>
</tr>
<tr class="odd">
<td>USB Cable*1</td>
<td>HX-2.54 4P Dupont Wire 200mm *1</td>
<td></td>
</tr>
<tr class="even">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/4f8d5af6dee9016b45d975adb2391d37.png" style="width:1.80208in;height:0.66667in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/7aef4f312385ac4f544e533ba456219c.png" style="width:1.85764in;height:0.41806in" /></td>
<td></td>
</tr>
</tbody>
</table>
**4. Wiring Diagram**

![](/media/cec50fec4a335b6922e4c6694a133bc1.png)

The GND, VCC, SDA, and SCL of the 8x16 LED light board are respectively connected to the keyestudio sensor expansion board-(GND), + (VCC), A4, A5 for two-wire serial communication.

(Note: Though it is connected with the IIC pin of Arduino, this module is not for IIC communication. And the IO port here is to simulate I2C communication and can be connected with any two pins ).

**5. Test Code**

Before writing the code, it is necessary to import the library file of the 8x16 LED board. The specific steps are as follows: 

Click ![](/media/9964e0b31fc9846a7f64c57f51e47152.png)to enter the extension library interface of sensors/modules/components, then search for“Matrix 8\*16 Aip1640”module![](/media/8637cbe988d4acbada4ed934b7064a42.png)and click it. In this way, "Not loaded" changes to "loaded", indicating that“Matrix 8\*16 Aip1640”module was added
successfully. 

![](/media/127e14cd4e1988b0a21bb028de41bf76.png)

Click ![](/media/29916972665d35bfb34914b6144e28aa.png)to return to the code editor interface, the instruction block of the added “Matrix 8\*16”module can be seen in the module area. 

![](/media/922bf5d5fbf96610282b32f3c9c14971.png)

You can drag blocks to edit. Blocks listed below are for your reference

1.  ![](/media/8de1b04be1ba147dd242c66bddeacacc.png)

2.  ![](/media/578c34f5ab25d39b836f9ea4f06b02dd.png)

Complete Test Code

![](/media/0390b1394e45bddbff7a4a3bb31b9da5.png)

**6. Test Result**

After successfully uploading the code to the V4.0 board, connect the wirings according to the wiring diagram, then turn the DIP switch to ON, a smile-shaped pattern will be displayed on the LED board.

> ![](/media/95bb011957896b12285fc6763137bb9a.png)

**7. Code Explanation**

We use the modulus tool we just learned, http://dotmatrixtool.com/\#, to make the dot matrix display the start pattern, going forward, and stop and then clear the pattern. The time interval is 2000 ms.

<table>
<tbody>
<tr class="odd">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/0fd4831db288e04e75828346ea66a3f5.png" style="width:1.33819in;height:0.75278in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/1b9e4afc5744776a7af20176e1b32b6d.png" style="width:1.75278in;height:0.79653in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/31ab1346c58438ca95c990e4ff963c0d.png" style="width:1.70208in;height:0.77431in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/805a32dcd1652607c6fc73d4359ee019.png" style="width:1.69236in;height:0.76667in" /></td>
</tr>
</tbody>
</table>

Instruction block for smiley face![](/media/466e6b8796314b88b4aa7e1f56732e2f.png)

Instruction block for expression：![](/media/7bfda0805b4349c1f2687e76c1c15ee5.png)

Instruction block for heart ![](/media/93888e5641635f57dcee6ce59353f5c3.png)

Instruction block for going forward![](/media/6e103bd81805ff52dc634f23acadcc5b.png)

Instruction block for **stepping back** ![](/media/8f2a48dee36375daed80f25c9fd5ba23.png)

Instruction block for **turning left** ![](/media/266011f56c8e77c888c570c39c3b9394.png)

Instruction block for **turning right** ![](/media/55a102107a3043f3d4864f08e8994a25.png)

Instruction block for **stop**![](/media/e0eacf741f929f05ff52943e315ea957.png)

Instruction block for **clearing screen**![](/media/3ad4fa1dc6625864e15f7c955f41e4bd.png)

![](/media/cec50fec4a335b6922e4c6694a133bc1.png)

You can drag blocks to edit. Blocks listed below are for your reference

（1）![](/media/8de1b04be1ba147dd242c66bddeacacc.png)

（2）![](/media/578c34f5ab25d39b836f9ea4f06b02dd.png)

（3）![](/media/cbbc7e90fb2d317eba462f2cbbb2864d.png)

Complete Test Code

![](/media/885c4abdba95f6b753fcee95aecbbdda.png)

After uploading test code, the facial expression board shows these patterns orderly and repeats this sequence.

<table>
<tbody>
<tr class="odd">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/95bb011957896b12285fc6763137bb9a.png" style="width:2.54167in;height:1.86944in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/6016e34c9182c8f86e1856ac0d9ec090.png" style="width:1.86667in;height:1.81597in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/c7f628da0a04bfe4687b52d0b21791a2.png" style="width:1.80903in;height:1.8in" /></td>
</tr>
</tbody>
</table>
