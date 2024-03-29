A compact USB-C to UART bridge with independent UART IO power rail utlizing the CH343 chip

Main features:

  1.UART interface I/O powered independently, never worry about backfeeding again.

  2.High baud rate. Maximum speed up to 6Mbps.

  3.Supports USB CDC driver. No annoying driver instalation anymore.

  4.Correctly implemented USB-C port, you can use any cable you like.
  (some badly designed USB-C device tends to lack the two 5.1k pull-down resistor, or shorts two cc pin together, causing the device to become unusable when using certain C to C cables)

  5.Compact. (2cm x 2.6cm)

![image](https://github.com/RathBee/USBC-Serial/assets/157344506/da4f36a1-c0ac-4012-ae22-c6ad6ea70610)




![image](https://github.com/RathBee/USBC-Serial/assets/157344506/88921067-cd8d-46bf-85a6-ad80e239f427)


Warning: Do not try to power you external circuit with this board's 3.3V pin, the CH343's internal regulator can only handle 10mA of current.
Instead, this pin should only be used to power the CH343's internal UART transciver. 

You can short the 5V pin to the VIO pin to get 5V level UART output. It's the same for 3.3V.

You can also power the CH343's UART transciver using your own power supply, for example, your MCU's power supply(assuming you are connecting this board to a MCU).
This way, you can have arbitary UART voltage level ranging from 1.7V to 5.5V. And you don't have to worry about backfeeding.
