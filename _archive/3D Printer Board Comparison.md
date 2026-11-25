# 3D Printer Board Comparison

**Human:**
Looking to buy a 3D printer board.  Wha the pro and con of RAMPS 1.4, RAMPS 1.6, MKS GEN V1.4

***

**Assistant:**

When considering different 3D printer control boards, it's important to look at their specifications, compatibility, and user experience. Here are some general pros and cons for each of the mentioned boards:

<strong>RAMPS 1.4:</strong>

<em>Pros:</em>

- Affordable and widely used.
- Open source design.
- Compatible with a variety of stepper drivers (A4988, DRV8825, etc.).
- Modularity - easy to replace faulty components.
- Supports a wide variety of 3D printers.


<em>Cons:</em>

- Lower power capacity than newer versions or other boards.
- Not pre-assembled, requires soldering skills.
- Poor thermal handling, might need active cooling for the MOSFETS.
- Limited future expansion due to lesser auxiliary ports.
- The connectors for the heated bed and the extruders can melt if you're running high currents.


<strong>RAMPS 1.6:</strong>

<em>Pros:</em>

- Higher power capacity than RAMPS 1.4.
- Better thermal performance.
- More robust power connectors to prevent melting issues seen on the 1.4 version.
- Also modular like 1.4, easy to replace faulty components.
- Similar compatibility to RAMPS 1.4.


<em>Cons:</em>

- Still requires assembly and soldering skills.
- Some users report quality control issues.
- Limited future expansion due to lesser auxiliary ports.
- While improved, it's still not the most robust board in terms of power delivery and thermal management.


<strong>MKS GEN V1.4:</strong>

<em>Pros:</em>

- Integrates the RAMPS 1.4 and Arduino Mega 2560 on a single board which improves stability and performance.
- Stronger power supply system and wider range of modification.
- Can use 24V, allowing for higher power and heated bed temperatures.
- Supports a variety of stepper drivers.
- Comes with more auxiliary ports allowing for future expansion.
- Generally more reliable due to better manufacturing quality.


<em>Cons:</em>

- Typically more expensive than RAMPS boards.
- Fewer community resources because it's not as widely used as RAMPS.
- Some versions may have firmware compatibility issues.
- Not as modular as RAMPS, so replacing faulty components can be more challenging.


Remember to consider these factors based on what you require. For example, if you're planning to upgrade or add more components in the future, you might need a board with more auxiliary ports. If you're inexperienced with electronics, you might want a pre-assembled board. Additionally, consider your budget and the kind of support you might need from the community.


***

**Human:**
2 / 2
Is the MKS TinyBee better than those listed above?

***

**Assistant:**

As of my knowledge cutoff in September 2021, the MKS TinyBee control board was not available, so I don't have specific details about its features, pros, or cons.

However, here's a general way to evaluate it compared to the others:

1. 
<strong>Hardware Capabilities:</strong> What kind of processors does it use? How many and what type of motor drivers can it support? Does it have enough expansion ports for your needs?

2. 
<strong>Software Compatibility:</strong> Is it compatible with common 3D printer software like Marlin, Repetier, or Klipper?

3. 
<strong>Community Support:</strong> Is there a large community of users who can provide help and troubleshooting? Are there readily available resources, such as tutorials and forums?

4. 
<strong>Ease of Use:</strong> Is it easy to install and setup? Does it come pre-assembled or require soldering?

5. 
<strong>Quality and Reliability:</strong> What's the build quality like? Does it have any known issues or failure points?

6. 
<strong>Price:</strong> How does it compare to the other boards in terms of cost?



In conclusion, I would recommend doing some research into the MKS TinyBee to see if it suits your specific needs and how it compares to the other options you're considering. If it has been released post my knowledge cutoff in September 2021, user reviews and the manufacturer's specifications should provide you with the necessary information.


***

**Human:**
Can the RAMP 1.6 support TMC drivers with a 12V power supply

***

**Assistant:**

Yes, the RAMPS 1.6 board can indeed support Trinamic's TMC stepper motor drivers, like the TMC2100, TMC2130, TMC2208, and others, with a 12V power supply.

Trinamic's TMC drivers are known for their quiet operation and high accuracy, and they are a popular choice for upgrading 3D printers. While the TMC drivers can operate at voltages higher than 12V, they can work perfectly fine within this voltage.

However, keep in mind that while the drivers themselves can support a 12V power supply, certain 3D printer components, especially heated beds, may benefit from a 24V power supply due to better heat up times. You should consider this aspect depending on your specific needs.

Also, remember that each specific TMC driver model might require different wiring or firmware configuration, so it's essential to follow the correct setup for the TMC driver model you are using. Some drivers, such as TMC2130, offer advanced features like sensorless homing, but setting up these features may require additional wiring and firmware configuration.

Another point to consider is that TMC drivers can run quite hot, and in a board where the drivers are user-replaceable (like the RAMPS), sufficient cooling may be required to keep the drivers operating reliably.


***

**Human:**
Do I need an external MOFSET for the heatbed using either RAMPS 1.4 or RAMPS 1.6?

***

**Assistant:**

Whether you need an external MOSFET for the heated bed of your 3D printer when using either the RAMPS 1.4 or 1.6 depends on a few factors:

1. 
<strong>Power Requirements:</strong> If your heated bed is pulling more current than the RAMPS board can handle, then you will need an external MOSFET. Both the RAMPS 1.4 and 1.6 can handle about 11-15 Amps of current on the heated bed power connector. If your heated bed draws more than that, an external MOSFET is recommended.

2. 
<strong>Safety:</strong> Even if your heated bed's power requirements are within the limits of the RAMPS board, it's often safer to use an external MOSFET. This can help prevent the board from overheating and failing, which can potentially damage other components or even cause a fire in extreme cases.

3. 
<strong>Reliability:</strong> Over time, drawing high currents through the board can lead to wear and tear, reducing its lifespan. Using an external MOSFET can help ensure that your board lasts longer.



So, while it may not always be strictly necessary, using an external MOSFET for the heated bed when using a RAMPS 1.4 or 1.6 board is usually a good idea, particularly for safety and reliability.


***

**Human:**
How about the MKS Gen V1.4, would a external mofset be advisable on the 12V heatbed

***

**Assistant:**

The MKS GEN V1.4 board is generally considered to have better power handling capabilities than the RAMPS 1.4 or 1.6 due to its superior design and component quality. This makes it more capable of handling the currents required by a heated bed without an external MOSFET. However, there are still a few factors to consider:

1. 
<strong>Power Requirements:</strong> Check the current draw of your heated bed. If it's within the board's specifications (should be around 15-20 Amps for the MKS Gen V1.4), then it should be fine without an external MOSFET. However, if it's higher, an external MOSFET would be required.

2. 
<strong>Safety:</strong> Using an external MOSFET can provide an additional layer of safety by reducing the current flowing through the board. This can help prevent overheating and potential board failure.

3. 
<strong>Reliability and Longevity:</strong> Reducing the strain on the board by using an external MOSFET can potentially extend the board's lifespan, especially if you're frequently using the heated bed at high temperatures.



In summary, while the MKS Gen V1.4 is more capable than the RAMPS boards when it comes to handling power, whether you need an external MOSFET still depends on your specific setup and requirements. In many cases, it can still be a good idea for safety and reliability, even if it's not strictly necessary.


***

**Human:**
Can the MKS Gen V1.4 support two Z steppers

***

**Assistant:**

Yes, the MKS Gen V1.4 board can indeed support two Z-axis stepper motors.

The board has five motor driver slots, labeled X, Y, Z, E0, and E1 (E0 and E1 are for extruders). If you want to use two stepper motors for the Z-axis, you can plug one into the Z slot and the other into the E1 slot.

You will then need to modify your firmware (such as Marlin) to configure the E1 driver as a second Z driver. This way, both Z-axis motors will move in sync.

Alternatively, if your Z-axis motors don't draw too much current, you can wire both of them into the Z driver slot using a splitter cable. This method doesn't require any firmware changes but you should ensure the combined current draw of the motors doesn't exceed the rating of the stepper driver or the board.

Remember to always double-check the current requirements of your stepper motors and compare them to the ratings of your stepper drivers and control board to avoid any potential damage.


***

**Human:**
Can the RAMPS 1.6 support two Z steppers?

***

**Assistant:**

Yes, the RAMPS 1.6 board can support two Z-axis stepper motors, similar to the MKS Gen V1.4.

The RAMPS 1.6 board has five stepper driver slots typically designated for X, Y, Z, E0, and E1 (E0 and E1 are for extruders). The Z slot on the RAMPS board actually has two sets of pin headers, meaning it can directly support two Z stepper motors without requiring any wiring modifications or firmware changes. You just need to have two stepper drivers (such as A4988 or DRV8825) for the Z-axis.

Alternatively, similar to the MKS Gen V1.4, you could also use the E1 slot for the second Z-axis motor. This would require a firmware change to designate the E1 driver as a second Z driver.

As always, make sure the total current of the motors does not exceed the capacity of the stepper drivers and the board. The Z-axis motors in most 3D printers don't draw too much current, so in most cases, either method should work fine.


***

**Human:**
I need to replace the board in a Prusa MK2S.  The preferred board is RAMBo mini, could I use a RANMPS or MKS instead as they all seem based on similar technology

***

**Assistant:**

Yes, you can replace the RAMBo mini board in a Prusa MK2S with a RAMPS or MKS board, but there are a few important factors to consider:

1. 
<strong>Firmware:</strong> The Prusa MK2S uses a specific version of the Marlin firmware that's customized for its hardware. If you switch to a RAMPS or MKS board, you'll need to update the firmware to match the new board's configuration. This involves changing the settings for the board, stepper drivers, endstops, etc., in the firmware, and then flashing the updated firmware to the new board. You will need some knowledge of firmware editing to do this.

2. 
<strong>Connectors:</strong> The connectors on the RAMPS or MKS board may not match the connectors on the Prusa MK2S. You may need to replace or adapt some connectors to make everything fit.

3. 
<strong>Mounting:</strong> The RAMPS or MKS board may not fit in the same space as the RAMBo mini. You might need to design and print a new mount for the new board.

4. 
<strong>Features:</strong> The RAMBo mini has some features, like support for an LCD and SD card, that may not be present on all RAMPS or MKS boards. If you use these features, you'll need to ensure your new board supports them.

5. 
<strong>Power:</strong> The Prusa MK2S can run on 12V or 24V power. You'll need to ensure that the new board, stepper drivers, and other components can handle the same voltage. Also, remember to adjust the Vref for the stepper drivers if necessary.



So, while it is possible to replace the RAMBo mini with a RAMPS or MKS board, it may not be a straightforward swap. You'll need to be comfortable with firmware editing, soldering (if necessary), and potentially designing and printing new parts. If you are, then this could be an interesting and educational project. If not, it might be easier to simply replace the RAMBo mini with another RAMBo mini.


***

**Human:**
Okay, which is better then RAMPS 1.6 or MKS Gen V1.4?

***

**Assistant:**

Choosing between the RAMPS 1.6 and MKS Gen V1.4 depends on your specific needs and level of expertise. Here's a comparison of the two boards:

<strong>RAMPS 1.6</strong>

<em>Pros:</em>

- Open source and widely used, which means lots of community support.
- More affordable.
- Highly modular: each part (Arduino Mega, stepper drivers, MOSFETs) can be replaced separately.


<em>Cons:</em>

- Lower power handling capacity and potential for connector melting if pushed too hard.
- Requires assembly and soldering skills.
- Does not integrate the Arduino Mega 2560 on the board, making it larger in size.


<strong>MKS Gen V1.4</strong>

<em>Pros:</em>

- Integrates the Arduino Mega 2560 and RAMPS 1.4 into one board, improving stability and reducing overall size.
- Has a more robust power supply system, which can handle higher current loads more safely.
- Generally comes with better quality components and manufacturing.
- Supports a wider range of modification and future expansion.


<em>Cons:</em>

- Typically more expensive than RAMPS boards.
- Not as modular as RAMPS, so replacing faulty components can be more challenging.
- May have fewer community resources because it's not as widely used as RAMPS.


The MKS Gen V1.4 is generally considered to be an upgrade over the RAMPS 1.6 due to its integrated design and improved power handling. However, if cost is a significant factor, or if you like the modularity and widespread community support of the RAMPS boards, the RAMPS 1.6 could be a better choice.

Both boards are compatible with the Marlin firmware, so from a software standpoint, there's not much difference between the two.

Remember to also consider the specific requirements of your 3D printer, such as how many stepper drivers you need and the power requirements of your heated bed and hotend.


***

Exported on 5 June 2023 12:04 am.