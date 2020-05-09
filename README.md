# The LoRaWAN-antenna board

Below you see the antenna board. The PCB antenna on this is suitable for a frequency around 868MHz.

![Antenna board](./img/Antenna_board.png)

Due the mismatches in impedance, some of the signal is reflected. You can solve this by doing 2 things.
Adjust the length of the antenna and add a matching network.

You can adjust the length here, by scratching away some copper at the end of the antenna. The total length of the last piece of the antenna is 1,25 cm. (measured from the outer corner) See the image below for clarification.

![Antenna board](./img/distance.png)

The dimensions of the PCB are also very important. If the dimensions are different from here, you must again determine the length and the matching network.



Below you can see that the VSWR at 868MHz is 1.112.

![VSWR](./img/VSWR.png)


De antenne die gebruikt moet worden:
![](./img/antenne_868MHz.jpg)

Als er antennes te kort zijn, dan is dit de 2de beste antenne:
![](./img/antenne_backup_868MHz.jpg)