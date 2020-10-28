# Class D Amplifier Build Notes 4/26/20
 
**Design Notes:**

This amplifier uses the [TPA3122](https://www.ti.com/lit/ds/symlink/tpa3122d2.pdf) IC to do the heavy lifting.  It is a stereo class D amp that is capable of driving up to 15w per channel.  In this circuit it is designed for 4Ω speakers in a stereo configuration.

At a high level, the circuit takes an input signal and converts it into a high-frequency square wave.  The high frequencies are then filtered out using an LC lowpass filter leaving the amplified version of the original signal to be transmitted to the speakers.  

The circuit operates on 12v with pins 1 and 10 supplying power to the Left and Right channels internal H-bridges. These are not powered internally by the AVCC pins which are powered separately on pins 16  and 17.  The shutdown pin is connected to 12v and mute is connected to ground as the circuit doesn’t include external controls.  The ‘Left In’ and ‘Right In’ pins are connected to a 3.5mm input jack through 1uF caps for filtering out the low frequencies of the input signal.   
 
![](https://i.imgur.com/d0a92PQ.png)
![](https://i.imgur.com/zwzfxDJ.png)

 
Other notable connections are on Pins 14 and 15 which are used to set the overall gain of the amplifier.  The TPA3122 allows for 4 configurations as outlined in the table below.  The circuit is currently configured for a gain of 26 dB however could easily be adjusted within the schematic for a lower/higher gain.  
![](https://i.imgur.com/w8fQGXr.png)


Pins 12 and 19 emit the Left and Right signals and are followed by an LC filter and coupling capacitor.
The circuit is designed in a 4 ohm, Single Ended (SE) configuration with the LC filter spec’d according to the datasheet for optimal performance.   
![](https://i.imgur.com/2poCqrB.png)

# **Milling Process**

**Top Layer:** The top layer only serves to add labeling.  If they’re not desired, this can be skipped. 
Bits: 1/32”
Mill Time: ~2 ½ mins

**Bottom Layer:**
Bits: 1/32” 
Mill Time: ~7 ½ mins

# **Build Process**

It’s easiest to solder the board in the following order: 

```
1.	SMD Components 
2.	Dip Socket
3.	Audio Jack 
4.	Barrel Jack 
5.	Screw Terminals
6.	Inductors
7.	Electrolytic Caps
```




