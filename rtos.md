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

`_http://gnu-mcu-eclipse.netlify.com/v4-neon-updates/`

	At the time of this write-up: v4.3.3-201804191501.
5. Start Eclipse and select directory _eclipse_workspace_ when asked
6. Then goto Help > Install New Software...
7. In the `_Work with` Click on 'Add'
8. In the name field, put in GNU MCU Eclipse Plugin and for Location:

`_http://gnu-mcu-eclipse.netlify.com/v4-neon-updates/`

	from step 4.
9. After Eclipse loads up the GNU MCU C/C++ software list, select the following:
- GNU MCU C/C++ ARM Cross Compiler
- GNU MCU C/C++ Generic Cortex-M Project Template
- GNU MCU C/C++ J-Link Debugging
- GNU MCU C/C++ OpenOCD Debugging
- GNU MCU C/C++ Packs (Experimental)
- GNU MCU C/C++ QEMU Debugging
- GNU MCU C/C++ STM32Fx Project Templates
Then click Next > Next > Accept terms of license agreement > Finish. Eclipse will install all the software selected.
10. If you need to install for Windows, you'll need make, rm, mkdir etc. Goto the link in Step 4 and select `_windows-build-tools`.
11. Select the required release and install it into your 'software_and_toolchain' directory. If you encounter an error, use:

`_https://www.dropbox.com/s/cfmk4bpjzce5rek/echonotfound.mp4?dl=0`

12. 




[jekyll-organization]: https://github.com/jekyll