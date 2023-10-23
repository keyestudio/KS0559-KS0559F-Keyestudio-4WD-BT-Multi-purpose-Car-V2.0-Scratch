# Project 2: Adjust LED Brightness

**1.Description**

In previous lesson, we control LED on and off and make it blink.

In this project, we will control LED’s brightness through PWM simulating breathing effect.

PWM is a means of controlling the analog output via digital means. Digital control is used to generate square waves with different duty cycles (a signal that constantly switches between high and low levels) to control the analog output. In general, the input voltages of ports are 0V and 5V.

What if the 3V is required? Or a switch among 1V, 3V and 3.5V? We cannot change resistors constantly. For this reason, we resort to PWM.

![](/media/bbcfcb9ae56abb7e80ee587246fc4be9.GIF)

For the Arduino digital port voltage output, there are only LOW and HIGH, which correspond to the voltage output of 0V and 5V. You can define LOW as 0 and HIGH as 1, and let the Arduino output five hundred 0 or 1 signals within 1s.

If all of the output five hundred are 1, that is 5V; if all of which are 0, that is 0V. If output 010101010101 in this way then the output port is 2.5V, which is like showing movie. The movie we watch are not completely continuous. It actually outputs 25 pictures per second. In this case, the human can’t see it, neither does PWM. If we want different voltage, we need to control the ratio of 0 and 1. The more 0,1 signals output per unit time, the more accurate the control.

PWM is a technology that uses digital methods to obtain analog quantities.  Digital control enables to form a square wave, the square wave signal only has on and off two states (high and low).  A voltage ranging from 0 to 5V can be simulated by controlling the ratio of on to off duration.  The time spent on (technically called high level) is called pulse width, so PWM is also called pulse width modulation. 

![](/media/553f3d1b6ca04e1aa0479841dd075fa2.png)

The green vertical bars represent one period of the square wave. The value written in each analogWrite(value) corresponds to a percentage, which is also called Duty Cycle. This percentage refers to the ratio of time occupied by the high level in a cycle, that is, duty cycle = high level time/cycle time. 

 In the figure, from top to bottom, the duty cycle of the first square wave is 0%, and the corresponding value is 0, and the LED brightness is the lowest, that is, off state.  The longer the high level lasts, the brighter it will be.  Therefore, the value of the last duty cycle of 100% is 255, and the LED is the brightest.  50% is the brightest half, and 25% is darker.  

PWM is more used to adjust the brightness of LED lights or the rotation speed of the motors, and the wheels speed driven by the motors can be easily controlled. When playing with some Arduino robots, the benefits of PWM can be better reflected. 

**2. Components**

<table>
<tbody>
<tr class="odd">
<td>Keyestudio 4.0 Development Board *1</td>
<td>Keyestudio 8833 Motor Driver Expansion Board *1</td>
<td>Red LED Module*1</td>
</tr>
<tr class="even">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/6131c8d782756fe051b0ef0210a76d03.png" style="width:1.27292in;height:0.91875in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/5e291db96125e27f380e8caf79e8015a.png" style="width:1.09375in;height:0.95625in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/7aacff28b0cb9b99f0dbcbf22eb309e4.png" style="width:0.91111in;height:0.61111in" /></td>
</tr>
<tr class="odd">
<td>3P F-F Dupont Wire*1</td>
<td>USB Cable*1</td>
<td></td>
</tr>
<tr class="even">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/e9aaac06e62418ecca6eaba97a9ec518.png" style="width:1.03056in;height:0.66667in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS0559-KS0559F-Keyestudio-4WD-BT-Multi-purpose-Car-V2.0-Scratch/master/media/4f8d5af6dee9016b45d975adb2391d37.png" style="width:1.38611in;height:0.5125in" /></td>
<td></td>
</tr>
</tbody>
</table>
**3. Wiring Diagram**

Keep the wiring-up unchanged.

![](/media/d29f513cc3561c7a3c3b05105e8a9ad3.png)

**4. Test Code**

You can drag blocks to edit. Blocks listed below are for your reference

1.  ![](/media/de8ccd3cb6621f0eb89a8514a9fd8452.png)

2.  ![](/media/8baabdf297623fa64b5c955fdfd157a7.png)

3.  ![](/media/659b8a45b8e8d271226d9a25034aedfd.png)

4.  ![](/media/32fa60879a4c3dff51e6d7f41f4ef788.png)

5.  ![](/media/ea9de6f7dacf67ca226e3633b100489a.png)

6.  ![](/media/c7ca2817ccd2cb3b3afab69e093eb458.png)

Complete Test Code

![](/media/4d4b4fdfe6027bc2d7c84624ec7df774.png)

**5. Test Result**

After successfully uploading the code to the V4.0 board, connect the wirings according to the wiring diagram, and use a USB cable to connect the computer to power the board. After powering on, you will see that the LED gradually changes from bright to dark, like human’s breath, rather than turning on and off immediately.

**6. Extension Practice**

Keep pins of the LED unchanged, then change code(values behind wait)

![](/media/40181afff1ac8568f7155803529f5136.png)

Upload the code to the development board, then the LED will blink more slowly.
