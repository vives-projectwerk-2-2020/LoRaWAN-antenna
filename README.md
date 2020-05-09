# The LoRaWAN-antenna board

This is the explanation of how the antenna PCB board came, and how you can make one yourself.
This PCB must be connected to the main PCB, as you can see below.

![on main board](./img/onMainBoard.png)

based on [this](http://www.ti.com/lit/an/swra228c/swra228c.pdf) design

## Explanation of the Antenna PCB board

Below you see the antenna board. The PCB antenna on this is suitable for a frequency around 868MHz.

![Antenna board](./img/Antenna_board.png)

Due the mismatches in impedance, some of the signal is reflected. You can solve this by doing 2 things.
Adjust the length of the antenna and add a matching network.

### Adjust length

You can adjust the length here, by scratching away some copper at the end of the antenna. The total length of the last piece of the antenna is 1,25 cm. (measured from the outer corner) See the image below for clarification.

![Antenna board](./img/distance.png)

By adjusting the length of the antenna, the antenna is now al more suitable for 868MHz.

### Matching network

By adding a matching network now, we can improve the impedance of the antenna more.
You can observe the maching network below. This consists of 2 capacitors and 1 coil. The values of the capacitors are 2,2pF. The value of the coil is 12nF.

![matching network](./img/matching_network.png)

The network for adjusting the impedance is a PI network. The left side of the math unit is connected to the antenna output of the RF95 (pin 9). The right side of the unit is connected to the antenna.

![PI-network](./img/PI-network.png)

The dimensions of the PCB are also very important. If the dimensions are different from here, you must again determine the length and the matching network.

Due to mismatches in impedance, some of the signal is reflected. The ratio of the input to the reflected signal is called the Voltage Standing Wave Ratio (VSWR). This ratio can also be measured in dB, and expressed as Return Loss.

Below you can see that the VSWR at 868MHz is 1.112. This mean that you're return lose is 25.510dB. This is very good, because now less than 1% of the power goes back to the module. This means that more than 99% of the power is used for the communication.

![VSWR](./img/VSWR.png)

### RF95

Below you see the RF95 module. All pins are brought out through the pins. Except the pin that goes to the antenna.
This PCB is then clicked on the main PCB.

![RF95 pinout](./img/RF95-pinout.png)

### schematic and print in Eagle

Here you can see the schematic drawn in Eagle. At the top you see the pins, these are then connected to the main PCB. below that you see the RF95 chip.
In the middle you see the matching network, which ensures a correct impedance.
The square block on the right is the symbol for your antenna. It is a symbol whose foodprint is the shape of the antenna.

![schematic](./img/schematic.png)

Below you can see what the PCB looks like in eagle.

![PCB](./img/PCB.png)

## Make it yourself

### Develop the PCB

first you need to develop the PCB. You can do this by sending a zip to a manufacturer. Like for example with this manufacturer. [JLCPCB](https://jlcpcb.com/)
The ZIP file is located here in the root and is called 'LoRaWAN_antenna.zip'. You can download and upload this on the manufacturer's website. If you want to make changes to the PCB you can edit it in the folder 'eagle'.


If you then have your PCB, you can start soldering.
You should not scratch the antenna anymore, I have already adjusted this in the last version.
For soldering it is best to start with the RF95 module and then the capacitors and the coil.
Then solder the pins on the last.
