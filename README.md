OLED 12864 Display Demo.

The OLED is driven by I2C bus.

The maximum I2C speed on the STM32F103 is 400 KHz.

A full screen refresh would take about 81 ms.

I used the demo from the vendor directly. 

Environment:
MDK5.24, ARMCC 5.06, -O3 -Otime
HAL Library

STM32F103 clock source uses a 8 MHz crystal and PLL to get a 72 MHz system clock.

TODO:
1.Optimize the pixel writing logic. A whole screen display buffer and DMA transfer should be used.
This would boost the speed performance at least 100%. Although I have not done the experiment.

2.Use a more advantage MCU with I2C speed higher than the 400 KHz limit on the STM32F103.

3.Rework the hardware of the display module. This module also supports SPI mode which is much faster than the I2C interface.

After all, the buffer and DMA should be implemented first.
