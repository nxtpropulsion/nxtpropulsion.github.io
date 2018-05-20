---
layout: page
title: RTOS
permalink: /rtos/
---

FreeRTOS Setup Notes on the STM32F4X - will work for Windows/Linux/MacOS

1. Create two folders in directory of choice:
+ eclipse_workspace
+ software_and_toolchain
2. Download **Eclipse IDE for C/C++ Developers** via [Eclipse](http://www.eclipse.org). At the time of this write-up: Oxygen 3a - May 19, 2018.
3. Download **Cross-Toolchain for ARM Cortex Processor** via [ARM Developer](https://developer.arm.com/open-source/gnu-toolchain/gnu-rm/downloads). At the time of this write-up: Version 7-2017-q4-major (Released: December 18, 2017). Extract into _software_and_toolchain_.
4. Download **GNU ARM Eclipse Plugins** via [GNU MCU Eclipse](https://github.com/gnu-mcu-eclipse). Or install manually via URL in Eclipse IDE using (see Step 6)
{% highlight ruby %}
`_http://gnu-mcu-eclipse.netlify.com/v4-neon-updates/`
At the time of this write-up: v4.3.3-201804191501.




[jekyll-organization]: https://github.com/jekyll