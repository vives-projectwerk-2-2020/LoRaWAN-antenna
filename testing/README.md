# TESTING

## Testing the right length and values for the matching network

Soldered on C1 and C2 capacitors of 2.2pF. A value of 12nH was taken for the coil.
The total length of the last piece of the antenna is 1.25 cm. (measured from the outer corner)

![result](./img/board_result.jpeg)

In the figure below you can see that at 868MHz the VSWR is 1.112. This is 0.28% reflection of your power sent to your antenna.

![test6](./img/test6.png)

## Making the board with lora module

The antenna scratched to the correct length and soldered the components on it.
The pins are properly soldered so that they can be connected to the main board.
This is the frond:

![front](./img/board_with_lora-module.jpeg)

And this is the back:

![back](./img/board_with_lora-module_back.jpeg)

## Testing the board with the main board

The PCB board connected to the main board. Then loaded the software into the Nucleo. The software comes from here: [LoRaWan-example](https://github.com/vives-projectwerk-2-2020/LoRaWAN-example).

In the setting.h something has to be changed about the pins. This is how it should look for the little nucleo:

![pins_settings.h](./img/pins.png)

Added a device on TTN and put the keys in a file settings.h as described in the LoRaWan-example.

Here you can see the communication over the port with Putty:

![putty](./img/putty.png)

Below you can see that there is a connection with TTN:

![status_connection](./img/connection.png)

And here you see 2 boards connected to each other:

![result](./img/board_result2.jpeg)

## Test the range with original antennas

On the following images you can see where there was connection with TTN. The gateway I use is a Dragino LG02, at the moment the original antennas are still on it.

point 1: 1,1km. The antennas see each other here.

![point1](./img/punt1.png)

point 2: 1,76km. The antennas did not see each other, there was a large concrete storage place in front of it.

![point2](./img/punt2.png)

## Test the range with a better antenna on the gateway

The antenna is now 10m high. The test setup can be found in the following 2 images.
In the box is the gateway (LG02 from dragino). One of the original antennas is disconnected and connected to a bigger antenna. This is an omnidirectional antenna with 3dB gain.
The antenna is mounted via a bracket on the pole.

![test](./img/test_opstelling.jpg)
![test](./img/opstelling.jpeg)

The range is now much better, it is doubled. Distances of 3.20 km are now possible, you can see this on the map below.
The points below are points where connections to TTN could be made. At the points you can always see the distance in bird's eye view.

![rangeTest2Map](./img/rangeTest2.png)

## Test the different between the PCB antenna and the previous antenna

Below you see the circuit:

![circuit](./img/circuit.jpeg)

Here you can see where there was signal with TTN. You can see that the range with that previous antenna is much smaller.
This means that the PCB antenna is an improvement on the previous antenna.

![BadAntenna](./img/rangeTestBadAntenna.png)
